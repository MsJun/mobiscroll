# mobiscroll
手机日期插件mobiscroll
        
        <link rel="stylesheet" type="text/css" href="mobiscroll.custom-2.5.0.min.css" />
        <script type="text/javascript" src="jquery.js"></script>
        <script type="text/javascript" src="mobiscroll.core-2.5.2.js"></script>
        <script type="text/javascript" src="mobiscroll.datetime-2.5.1.js"></script>
        
        
       <input type="text" id="scroller" name="service_time" value="" placeholder="请选择婚礼时间" name="destination" />

      //日历插件
      $(function(){
          var currYear = (new Date()).getFullYear();
          //初始化日期控件
          var opt = {
             preset: 'date', //日期，可选：date\datetime\time\tree_list\image_text\select
             theme: 'android-ics light', //皮肤样式，可选：default\android\android-ics light\android-ics\ios\jqm\sense-ui\wp light\wp
             display: 'bubble', //显示方式 ，可选：modal\inline\bubble\top\bottom
             mode: 'scroller', //日期选择模式，可选：scroller\clickpick\mixed
             lang:'zh',
             dateFormat: 'yyyy-mm-dd', // 日期格式
            setText: '确定', //确认按钮名称
            cancelText: '取消',//取消按钮名籍我
            dateOrder: 'yyyymmdd', //面板中日期排列格式
            dayText: '日', monthText: '月', yearText: '年', //面板中年月日文字
            headerText:"请选择婚礼时间",
            startYear:currYear, //开始年份
            endYear:currYear + 10 //结束年份
            //支持callback方法，支持定义callbackTime单位是毫秒
        }; 
        $("html元素").mobiscroll(opt);
    });
