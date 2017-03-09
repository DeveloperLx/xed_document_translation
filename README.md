# xed_document_translation

#### [原文地址](https://developer.apple.com/legacy/library/documentation/Darwin/Reference/ManPages/man1/xed.1.html) 翻译：[DeveloperLx](http://weibo.com/DeveloperLx)

# xed

<pre class="manpages" onbeforecopy="prepForCopy();" oncopy="cleanupFromCopy();"><tt>

<b>名称</b>
     <b>xed</b> -- Xcode文本编辑调用的工具。

<b>概要</b>
     <b>xed</b> [<b>-xcwrbhv</b>] [<b>-l</b> <u>lineno</u>] [<u>file</u> <u>...</u>]

<b>描述</b>
	<b>xed</b>通过标注输入的内容，启动Xcode应用，并打开给定的文档，或打开一个新的无标题的文档。

<b>选项</b>
	<b>xed</b>的选项类似那些其它的文本编辑的命令行工具：

	-x, --launch
		启动Xcode来打开一个新的空的未保存的文件，没有从标准输入中读取。

    -c, --create
     	创建在文件列表中的任何尚未存在的文件。如果没有使用--launch选项，标准输入将被读取并被“管道”（pipe to）到上一个被创建的文件中。

    -w, --wait
     	在退出前等待文件被关闭。<b>xed</b>将闲置在run loop中，来等待一个来自Xcode的通知，这个通知会在每一个文件被关闭时发送，并且在所有文件都被关闭后才退出。当从脚本中调用xed时，是非常有用的。

    -l, --line &lt;number&gt;
     	在上次打开的文件中选择给定的行。

    -b, --background
     	打开Xcode但不激活它；调用<b>xed</b>的进程仍保留在前台。

    -h, --help
     	打印一个用法的概述。

    -v, --version
     	打印<b>xed</b>的版本号

    [file...]
     	一个文件路径的列表。存在的文件会被打开；当且仅当传递了--create标记时，不存在的文件将被创建。如果没有文件来传参，标注的输入就会被读取并被“管道”（pipe to）到一个新的无标题的文档中（unless传了--launch选项）。如果--create和至少一个不存在的文件名被传参，则最后一个文件将会被创建，填到标准输入中，然后打开。

<b>历史</b>
	<b>xed</b>是在Mac OS X 10.5 和 Xcode 3.0 中被引入的。

Mac OS                         2013年10月11日                      
</tt></pre>