* ##### ID的设置包括媒体ID和用户ID设置，都可以在初始化的时候设置（详情请查看 [初始化](/sdk使用/初始化.md) 章节），也可以单独设置。媒体ID还可以

##### 在`AndroidManifest.xml`文件中设置（详情请查看 [媒体ID配置](/sdk集成/媒体ID配置.md) 章节）

```
              媒体ID: 多盟后台申请的 ID , 是媒体的唯一标示

              用户ID: 开发者用户体系中，用户的唯一识别标识，没有可以不设置
```

* ##### 设置方法如下：

```java
 /**
     * 更新用户ID
     * @param activity
     * @param userID
     */
    public void updateUserID(Activity activity,String userID) {
        IndependentVideoConfigDataManager.shareInstance(activity).setUserID(userID);
    }

    /**
     *更新媒体ID
     * @param activity
     * @param publishid
     */
    public void updatePublishID(Activity activity,String publishid) {
        IndependentVideoConfigDataManager.shareInstance(activity).setPublisherID(publishid);
    }
```

* ##### 实例：

```java
 IndependentVideoManager.newInstance().updateUserID(activity,用户id);
 IndependentVideoManager.newInstance().updatePublishID(activity,媒体id);
```



