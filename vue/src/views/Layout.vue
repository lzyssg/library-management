<template>
    <div>
        <!--头部区域-->
        <div style="height: 60px; line-height: 60px; background-color: white; margin-bottom: 2px;">
        <img src="@/assets/logo.png" alt="" style="width: 40px; position:relative; top: 10px; left: 20px">
        <span style="margin-left:25px; font-size: 24px">图书馆</span>
        </div>

        <!--侧边栏和主体-->
        <div style="display: flex">
            <!--侧边栏导航-->
            <div style="width: 200px; min-height: calc(100vh-62vh); overflow: hidden; margin-right: 2px; background-color: white;">
            
                <el-menu :default-active="$route.path" router class="el-menu-demo" >
                    <el-menu-item index="/">
                        <i class="el-icon-eleme">
                            <span>首页</span>
                        </i>
                    </el-menu-item>
                        <el-submenu index="user">
                            <template slot="title">
                                <i class="el-icon-more">
                                    <span>成员管理</span>
                                </i>
                            </template>
                            <el-menu-item index="/addUser">会员添加</el-menu-item>
                            <el-menu-item index="/userList">会员列表</el-menu-item>
                        </el-submenu>

                        <!--管理员-->
                        <el-submenu index="admin">
                            <template slot="title">
                                <i class="el-icon-user">
                                    <span>管理员管理</span>
                                </i>
                            </template>
                            <el-menu-item index="/addAdmin">管理员添加</el-menu-item>
                            <el-menu-item index="/adminList">管理员列表</el-menu-item>
                        </el-submenu>
                    
                </el-menu>
            </div>

            <!--主体数据-->
            <div style="flex: 1; background-color: white; padding: 10px;">
                <router-view/>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    name: 'Layout.vue'
    
}
</script>

<style scoped>

</style>