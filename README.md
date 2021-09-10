# markdown-img01



&nbsp; 
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 

&nbsp; 
&nbsp; 
&nbsp; 
&nbsp; 






















































# git 从分支拉取代码到本地，并修改后提取代码到该分支

![](https://cdn.jsdelivr.net/gh/archted/markdown-img01@2021082604/img/%E6%8E%A8%E8%8D%90%E7%AE%97%E6%B3%95%E5%B7%A5%E7%A8%8B%E5%B8%88%E6%8A%80%E8%83%BD%E6%A0%91.png)

\*\*

进入新一家公司，该公司用Git，从未用过Git的我显的有点懵圈。结合网上的资料整理了一下做一下备忘录，以便以后有不时之需！！！

\*\*  
1：在本地创建任意文件夹,  
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190328120123510.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzI5OTA3ODg1,size_16,color_FFFFFF,t_70)  
2:在该文件夹中右键选择 Git Bash Here （这些都是基于你已经正确安装Git的情况下！）  
3：在弹出框中输入：git init（初始化本地仓库）  



![在这里插入图片描述](https://cdn.jsdelivr.net/gh/archted/markdown-img@main/img/20190328120153554.png)  
4：输入你的项目地址：git remote add origin 地址！就是下图那个地址![在这里插入图片描述](https://img-blog.csdnimg.cn/20190328122242601.png)  
5： git fetch origin 分支名称（一切正常的情况下会让你输入用户名，密码。密码是不会显示出来的。）  
![在这里插入图片描述](https://cdn.jsdelivr.net/gh/archted/markdown-img@main/img/20190328122352220.png)  
![在这里插入图片描述](https://cdn.jsdelivr.net/gh/archted/markdown-img@main/img/20190328122407739.png)  
6：创建本地分支并切换到本地分支：git checkout -b 本地分支名 origin/远程分支名 （红色本地，黄色远程）。本地，远程写同一个名字就可以！写上就行不需要你创建文件夹  
![在这里插入图片描述](https://cdn.jsdelivr.net/gh/archted/markdown-img@main/img/2019032812243180.png)  
7：更新分支代码：git pull origin 远程分支名  
![在这里插入图片描述](https://cdn.jsdelivr.net/gh/archted/markdown-img@main/img/20190328122702444.png)  
8：现在你就可以对你拉取的代码随意修改了！  
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190328154709621.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzI5OTA3ODg1,size_16,color_FFFFFF,t_70)  
9：代码提交，查看需提交的代码：git status  
![在这里插入图片描述](https://cdn.jsdelivr.net/gh/archted/markdown-img@main/img/20190328122926772.png)  
10:“git add .”add加点是所有的文件都提交暂缓区，“git add 路径”，提交部分！

```
01 ： git add -A  提交所有变化

02： git add -u  提交被修改(modified)和被删除(deleted)文件，不包括新文件(new)

03 ： git add .  提交新文件(new)和被修改(modified)文件，不包括被删除(deleted)文件
```

11：git commit -m “备注”，主要是将暂存区里的改动给提交到本地的版本库。  
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190328123303473.png)  
12：git push origin 分支名，推送本地分支到远程分支（PS：**推送之前最好先更新一遍代码！防止覆盖！！**）  
![在这里插入图片描述](https://cdn.jsdelivr.net/gh/archted/markdown-img@main/img/20190328123435274.png)  
13：全图奉上！![在这里插入图片描述](https://cdn.jsdelivr.net/gh/archted/markdown-img@main/img/20190328123656762.png)  
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190328123816531.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzI5OTA3ODg1,size_16,color_FFFFFF,t_70)

