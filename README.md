# XRefreshLayout
A refresh layout, can refresh RecyclerView for all LayoutManager, NestedScrollView and Any View that implements NestedScrollChild !



# Feature

- support RecyclerView for all LayoutManager in vertical orientation !
- support NestedScrollView !
- support any view that implements NestedScrollChild !
- support custom refresh header and footer , which means you can make you wanderful animation !
- not support ListView, GridView, ScrollView !



# Screenshot

- refresh RecyclerView for StaggeredGridLayoutManager ：

  ![staggered](/Screenshot/staggered.gif)


- refresh RecyclerView for LinearLayoutManager ：

  ![linear](/Screenshot/linear.gif)

- refresh NestedScrollView ：

  ![nestedscroll](/Screenshot/nestedscroll.gif)




- custom refresh animation! There is two animation style now, I will support more animation in future...

  ![custom_anim](/Screenshot/custom_anim.gif)



# Get Start

- make your layout

  ```xml
  <com.itheima.xrefreshlayout.XRefreshLayout xmlns:android="http://schemas.android.com/apk/res/android"
      android:layout_width="match_parent"
      android:id="@+id/xrefreshLayout"
      android:layout_height="match_parent">

      <android.support.v7.widget.RecyclerView
          android:id="@+id/recyclerview"
          android:layout_width="match_parent"
          android:layout_height="match_parent"/>

  </com.itheima.xrefreshlayout.XRefreshLayout>
  ```

  或者

  ```xml
  <com.itheima.xrefreshlayout.XRefreshLayout xmlns:android="http://schemas.android.com/apk/res/android"
      android:layout_width="match_parent"
      android:id="@+id/xrefreshLayout"
      android:layout_height="match_parent">

      <android.support.v4.widget.NestedScrollView
          android:id="@+id/recyclerview"
          android:layout_width="match_parent"
          android:layout_height="match_parent"/>

  </com.itheima.xrefreshlayout.XRefreshLayout>
  ```

  ​

- set refresh listener

  ```java
  xrefreshLayout.setOnRefreshListener(new XRefreshLayout.OnRefreshListener() {
              @Override
              public void onRefresh() {
              }

              @Override
              public void onLoadMore() {
              }
          });
  ```

- finish refresh

  ```java
  xrefreshLayout.completeRefresh();
  ```

- set custom loadinglayout

  ```java
  //you can see the DefaultLoadingLayout for some help.
  xrefreshLayout.setLoadingLayout(...);
  ```

  ​