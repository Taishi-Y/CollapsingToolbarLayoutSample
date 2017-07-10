# CollapsingToolbarLayoutSample


Sample project of using CollapsingToolbarLayout

<img src="https://github.com/Taishi-Y/CollapsingToolbarLayoutSample/blob/master/art/sample.gif?raw=true"
alt="" width="250" border="10" />

#### Key layout file

activity_main.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<android.support.design.widget.CoordinatorLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    >

    <android.support.design.widget.AppBarLayout

        android:theme="@style/ThemeOverlay.AppCompat.Dark.ActionBar"
        android:id="@+id/appbar"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:elevation="20dp">

        <android.support.design.widget.CollapsingToolbarLayout
            android:id="@+id/collapsing_toolbar"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            app:contentScrim="?attr/colorPrimary"

            app:layout_scrollFlags="scroll|exitUntilCollapsed">

            <FrameLayout
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                app:layout_collapseMode="parallax"
                app:layout_collapseParallaxMultiplier="0.7">

                <ImageView
                    android:id="@+id/imgBackdrop"
                    android:src="@drawable/bg"
                    android:layout_width="match_parent"
                    android:layout_height="match_parent"

                    android:adjustViewBounds="true"
                    android:scaleType="fitXY"/>

            </FrameLayout>


        </android.support.design.widget.CollapsingToolbarLayout>

        <android.support.design.widget.CollapsingToolbarLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            app:layout_scrollFlags="scroll|enterAlways"
            android:elevation="20dp">

            <android.support.design.widget.TabLayout
                android:id="@+id/tab_layout"
                android:elevation="20dp"
                style="@style/PinListTabLayout"

                android:layout_width="match_parent"
                android:layout_height="48dp"
                app:layout_collapseMode="pin" />

        </android.support.design.widget.CollapsingToolbarLayout>

    </android.support.design.widget.AppBarLayout>


    <android.support.v4.widget.NestedScrollView
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:fillViewport="true"
        app:layout_behavior="@string/appbar_scrolling_view_behavior">

        <android.support.v4.view.ViewPager
            android:id="@+id/viewPager"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            app:layout_behavior="@string/appbar_scrolling_view_behavior" />
    </android.support.v4.widget.NestedScrollView>

</android.support.design.widget.CoordinatorLayout>

```
