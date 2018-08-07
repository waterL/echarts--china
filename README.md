```
var data; // 传的数据 {name:'北京'， value: '111'}
var province; // 默认省份及对应经纬度
var dataPos;//弹窗显示数据
var dataMark;//标记数据    

var option = {
        title : {
            text: '销量',
            subtext: '纯属虚构',
            x:'center'
        },
        //显示弹窗
        tooltip : {
            trigger: 'item',
            formatter: '{b}'
        },
        //显示工具
        toolbox: {
            show: true,
            orient : 'vertical',
            x: 'right',
            y: 'center',
            feature : {
                mark : {show: true},
                dataView : {show: true, readOnly: false},
                restore : {show: true},
                saveAsImage : {show: true}
            }
        },
        //颜色
        dataRange: {
            min: 0,
            max: 2500,
            x: 'left',
            y: 'bottom',
            text:['高','低'],           // 文本，默认为数值文本
            calculable : true
        },
        series: [
            {
                name: '订单数量',
                type: 'map',
                mapType: 'china',
                roam: false,
                itemStyle:{
                    normal:{label:{show:true}},
                    emphasis:{label:{show:true}}
                },
                //数据
                data: dataPos,
                //显示数量
                markPoint: {
                    itemStyle: {
                        normal: {
                            // 背景颜色
                            color:'skyblue'
                        }
                    },
                    data: dataMark
                },
            },
        ]
    };
```