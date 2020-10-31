#暂时还有问题，请不要使用
#栏目文章
## 说明
- 该插件依赖dsshop项目，而非通用插件
- 支持版本:dshop v1.1.8及以上

## 功能介绍
- 支持为栏目和文章添加缩略图
- 栏目支持无限级分类
- 栏目如果未设置列表，将可以直接当文章用
- 前端展示默认展示所有栏目，且不分父子类目
- 前端展示层级为：栏目列表->文章列表->文章详情或栏目列表->栏目详情
- 栏目文章已做访问次数记录，用户每访问一次文章详情/栏目详情，记一次

## 使用说明
#### 一、 下载article最新版
#### 二、 解压article到项目plugin目录下
#### 三、 登录dshop后台，进入插件列表
#### 四、 在线安装（请保持dshop的目录结构，如已部署到线上，请在本地测试环境安装，因涉及admin和uni-app，不建议在线安装）
#### 五、 进入api目录执行数据库迁移使用

```
php artisan migrate
```
#### 六、 进入数据库，导入 `article/article.sql` SQL文件（sql文件需要按照下图进行修改，也可后台自行添加权限，效果一样）
![](/image/1.png)
![](/image/2.png)
#### 七、 进入后台，为管理员分配权限
#### 八、 使用栏目文章插件，如这是第一个插件，可直接按以下步骤替换目标文件即可，如安装有其它插件，可能存在修改同一文件的可能，请进行文件比对进行手动修改
- `article/example/trade/user/user.vue`->`trade/Dsshop/pages/user/user.vue`
![](/image/3.png)
#### 九、 测试栏目添加和文章添加，前端能正常显示即为安装成功
## 如何更新插件
- 首先请备份项目，升级可能产生问题（如自行修改了涉及到升级的文件、下载的文件不全等问题）
- 首先查看新版本支持的dshop的版本，如果符合，可通过后台直接升级，升级将会自动覆盖原有文件
- 如果升级涉及到手动修改代码部分，升级说明中会进行讲解
## 如何卸载插件
- 插件安装后不建议卸载，因为涉及到多处手动修改的代码
- 可以按以上安装方式反向操作，即可卸载