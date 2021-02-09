<template>
	<el-container>
		<!-- 侧边栏 -->
		<el-aside
			width="200px"
			style="height: 100vh; background-color: #545c64"
		>
			<el-image
				style="
					width: 100%;
					height: 60px;
					background-color: white;
					border: 1px solid #ebebeb;
				"
				src="../src/assets/logo.png"
				fit="scale-down"
			></el-image>
			<el-menu
				default-active="2"
				@open="handleOpen"
				@close="handleClose"
				background-color="#545c64"
				text-color="#fff"
				active-text-color="#ffd04b"
				style="width: 100%"
			>
				<el-submenu index="1">
					<div slot="title">
						<i class="el-icon-location"></i>
						<span>导航一</span>
					</div>
					<el-menu-item-group title="分组一">
						<el-menu-item index="1-1">选项1</el-menu-item>
						<el-menu-item index="1-2">选项2</el-menu-item>
					</el-menu-item-group>
					<el-menu-item-group title="分组2">
						<el-menu-item index="1-3">选项3</el-menu-item>
					</el-menu-item-group>
					<el-submenu index="1-4">
						<template slot="title">选项4</template>
						<el-menu-item index="1-4-1">选项1</el-menu-item>
					</el-submenu>
				</el-submenu>
				<el-menu-item index="2">
					<i class="el-icon-menu"></i>
					<span slot="title">导航二</span>
				</el-menu-item>
				<el-menu-item index="3">
					<i class="el-icon-document"></i>
					<span slot="title">导航三</span>
				</el-menu-item>
				<el-menu-item index="4">
					<i class="el-icon-setting"></i>
					<span slot="title">导航四</span>
				</el-menu-item>
			</el-menu>
		</el-aside>
		<el-container>
			<!-- 导航栏 -->
			<el-header style="padding: 0">
				<el-menu
					text-color="#545c64"
					active-text-color="#32a1ff"
					mode="horizontal"
					style="
						justify-content: flex-end;
						display: flex;
						align-items: center;
					"
				>
					<el-submenu index="1">
						<template slot="title">导航一</template>
						<el-menu-item-group title="分组一">
							<el-menu-item index="1-1">选项1</el-menu-item>
							<el-menu-item index="1-2">选项2</el-menu-item>
						</el-menu-item-group>
						<el-menu-item-group title="分组2">
							<el-menu-item index="1-3">选项3</el-menu-item>
						</el-menu-item-group>
						<el-submenu index="1-4">
							<template slot="title">选项4</template>
							<el-menu-item index="1-4-1">选项1</el-menu-item>
						</el-submenu>
					</el-submenu>
					<el-menu-item index="2">
						<i class="el-icon-menu"></i>
						<span slot="title">导航二</span>
					</el-menu-item>
					<el-menu-item index="3">
						<i class="el-icon-document"></i>
						<span slot="title">导航三</span>
					</el-menu-item>
					<el-menu-item index="4">
						<i class="el-icon-setting"></i>
						<span slot="title">导航四</span>
					</el-menu-item>
				</el-menu>
			</el-header>

			<!-- 主页面 -->
			<el-main> </el-main>
		</el-container>
	</el-container>
</template>

<script>
export default {
	methods: {
		startHacking() {
			this.$notify({
				title: "It works!",
				type: "success",
				message:
					"We've laid the ground work for you. It's time for you to build something epic!",
				duration: 5000,
			});
		},
		handleOpen(key, keyPath) {
			console.log(key, keyPath);
		},
		handleClose(key, keyPath) {
			console.log(key, keyPath);
		},
	},
};
</script>

<style>
body {
	margin: auto;
}
#app {
	font-family: Helvetica, sans-serif;
	text-align: center;
}
.el-main {
	background-color: #f5f5f5;
}
.el-menu {
	border: none;
}
</style>
