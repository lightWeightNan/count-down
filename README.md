# count-down
实现时间的倒计时，像促销活动的时间倒计时
//具体几个处理方法
function FreshTime()
{
        var endtime=new Date("2017/9/3,12:20:12");//结束时间
        var nowtime = new Date();//当前时间
        var lefttime=parseInt(endtime.getTime()-nowtime.getTime()); 
        d= parseInt(lefttime/(1000*60*60*24));
       
        h=parseInt(lefttime/(1000*60*60)%24);
        m=  parseInt(lefttime/(1000*60)%60);
        s=  parseInt(lefttime/1000%60);
       
        document.getElementById("LeftTime").innerHTML=d+"天"+h+"小时"+m+"分"+s+"秒";
        if(lefttime<=0){
        document.getElementById("LeftTime").innerHTML="团购已结束";
        clearInterval(sh);
        }
}
   FreshTime()
   var sh;
   sh=setInterval(FreshTime,500);
