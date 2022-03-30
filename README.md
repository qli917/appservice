# appservi

普通下载
 HikAppUtil.Builder().setDownLoadBean(DownLoadBean().apply {
            //设置请求下载结构体，可变数据  既可以传单独DownLoadBean  可以传 DownLoadBean[]  数组 如果单个结构体 框架会动匹配单独下载任务 如果是数组 框架会自动并行执行多个下载任务
            url = ""  // 下载地址
            fileName = "" // 注意一定要是文件名加后缀  eg：image.png  demo.apk video.mp4
        }).build().enqueue() // 初始化参数成功后 正在发起下载请求 enqueue
