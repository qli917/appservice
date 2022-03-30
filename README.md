# appservi

普通下载
 HikAppUtil.Builder().setDownLoadBean(DownLoadBean().apply {
            url = ""  //请求地址
            fileName = ""  //下载文件名字 注意一定要是文件名加后缀  eg：image.png  demo.apk video.mp4
  }).build().enqueue() 
  
setDownLoadBean //设置请求下载结构体，可变数据  既可以传单独DownLoadBean  可以传 DownLoadBean[]  数组 如果单个结构体 框架会动匹配单独下载任务 如果是数组 框架会自动并行执行多个下载任务

//下载回调

HikAppUtil.Builder().setDownLoadBean(DownLoadBean().apply {
            url = ""  
            fileName = "" 
        }).setDownLoadListener(object : DownloadListener {
            override fun onSuccess(path: String?, index: Int) {
                //下载文件成功后  会返回文件本地路径  path
                //下载任务下标   index   
            }

            override fun onFail() {
               //下载失败
            }
        }).build().enqueue() 

