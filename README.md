# HuaWeiWeatherView
<br>
这里根据华为手机天气、手机管家等界面特效
<br>
仿出的圆形刻度盘和水波加速球效果
你可以通过
···java
mv.change(200);//动态绘制刻度
···
动态绘制刻度圆盘
<br>
通过调用
···java
mv.moveWaterLine();//让水球动起来
···
让水球动起来
<br>
通过接口回调，动态同步设置背景颜色
···java
 mv.setOnAngleColorListener(onAngleColorListener);
 
 private MyView.OnAngleColorListener onAngleColorListener=new MyView.OnAngleColorListener() {
        @Override
        public void onAngleColorListener(int red, int green) {
            Color color=new Color();
            int c=color.argb(150, red, green, 0);
            //界面背景色
            ll.setBackgroundColor(c);
        }
    };
···

