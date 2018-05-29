 
#  期中作业便签APP
### 主要利用SQLiteOpenHelper辅助类实现对数据库的增删改查，利用listview控件和适配器的建立实现数据列表

### 主要的流程图

![image](https://raw.githubusercontent.com/tj5890063/Note_APP/master/app/src/main/res/drawable-v24/%E4%B8%BB%E8%A6%81%E6%B5%81%E7%A8%8B%E5%9B%BE.png)

### 在本实验中，主要逻辑就是建立的便签存储在数据库的记录中，在主界面用onActivityResult()方法回调接收数据，并进行数据的筛选，绑定数据源，并建立适配器，最后让listview与适配器进行绑定，完成数据的显示。
 
## demo的演示
### 进入初始化界面
 ![image](https://raw.githubusercontent.com/tj5890063/Note_APP/master/app/src/main/res/drawable-v24/%E7%95%8C%E9%9D%A2%E6%88%AA%E5%9B%BE1.png)
 
 总布局为相对布局，其中包含着头部的线性布局和一个图片按钮view.
 
 ### 进入编写便签界面
 ![image](https://raw.githubusercontent.com/tj5890063/Note_APP/master/app/src/main/res/drawable-v24/%E7%BC%96%E5%86%99%E4%BE%BF%E7%AD%BE%E6%88%AA%E5%9B%BE.png)
 
 拥有顶部线性布局和中间2个编辑框.
 
 ### 进行编写第一条内容
 ![image](https://raw.githubusercontent.com/tj5890063/Note_APP/master/app/src/main/res/drawable-v24/%E7%AC%AC%E4%BA%8C%E6%9D%A1.png)
 
### 插入第一条数据到数据库，并在界面中显示内容
![image](https://raw.githubusercontent.com/tj5890063/Note_APP/master/app/src/main/res/drawable-v24/%E7%AC%AC%E4%B8%80%E6%9D%A1%E5%AE%8C%E6%88%90%E7%9A%84%E7%95%8C%E9%9D%A2.png)

### 编写第二条便签
![image](https://raw.githubusercontent.com/tj5890063/Note_APP/master/app/src/main/res/drawable-v24/%E7%AC%AC%E4%BA%8C%E6%9D%A1.png)

### 界面显示的列表
![image](https://raw.githubusercontent.com/tj5890063/Note_APP/master/app/src/main/res/drawable-v24/%E7%AC%AC%E4%BA%8C%E6%9D%A1%E5%AE%8C%E6%88%90.png)

### 方便后面的操作，多插入几条
![image](https://raw.githubusercontent.com/tj5890063/Note_APP/master/app/src/main/res/drawable-v24/%E5%A4%9A%E7%BC%96%E5%86%99%E5%87%A0%E6%9D%A1.png)

###  扩展功能：便签排序(按时间进行排序)
![image](https://raw.githubusercontent.com/tj5890063/Note_APP/master/app/src/main/res/drawable-v24/%E6%8C%89%E6%97%B6%E9%97%B4%E6%8E%92%E5%BA%8F.png)

 按最后更新的时间进行从近到远进行排序，主要利用的Collections的sort方法进行排序.

### 查询操作
![image](https://raw.githubusercontent.com/tj5890063/Note_APP/master/app/src/main/res/drawable-v24/%E6%9F%A5%E8%AF%A2.png)

查询没有存在的便签，会提示没有当前便签存在

### 根据标题查找了名为明天星期三的便签，一共出现2个
![image](https://raw.githubusercontent.com/tj5890063/Note_APP/master/app/src/main/res/drawable-v24/%E6%9F%A5%E8%AF%A2%E6%93%8D%E4%BD%9C.jpg)

### 删除操作
![image](https://raw.githubusercontent.com/tj5890063/Note_APP/master/app/src/main/res/drawable-v24/%E5%88%A0%E9%99%A4%E6%93%8D%E4%BD%9C.png)

删除第二个的便签

### 删除后的界面利用适配器的notifyDataSetChanged()进行更新UI界面
![image](https://raw.githubusercontent.com/tj5890063/Note_APP/master/app/src/main/res/drawable-v24/%E5%88%A0%E9%99%A4%E5%AE%8C%E6%88%90%E5%90%8E.png)

就会显示列表只剩1个名为"明天星期三”的便签
### 修改操作
![image](https://raw.githubusercontent.com/tj5890063/Note_APP/master/app/src/main/res/drawable-v24/%E4%BF%AE%E6%94%B9%E6%93%8D%E4%BD%9C.png)

### 点击修改的图片，进入编写界面，点击完成后，会显示最新更改的时间.
 ![image](https://raw.githubusercontent.com/tj5890063/Note_APP/master/app/src/main/res/drawable-v24/%E4%BF%AE%E6%94%B9%E5%90%8E.png)
 
### 扩展功能：更改背景颜色
选择菜单栏的颜色选项

![image](https://raw.githubusercontent.com/tj5890063/Note_APP/master/app/src/main/res/drawable-v24/%E9%A2%9C%E8%89%B2%E9%80%89%E6%8B%A9.png)
 
### 选择红色
 ![image](https://raw.githubusercontent.com/tj5890063/Note_APP/master/app/src/main/res/drawable-v24/%E7%BA%A2%E8%89%B2.png)
 
### 选择蓝色
 ![image](https://raw.githubusercontent.com/tj5890063/Note_APP/master/app/src/main/res/drawable-v24/%E8%93%9D%E8%89%B2.png)

剩下的其他颜色就不一一演示.

### 便签APP的演示内容大概就是这些，只要掌握数据库的基本操作和熟悉利用listview和适配器以及intent的跳转，还有理解item的内部控件点击事件的操作，就可以完成备忘录的主要内容。



 


