<template>
	<div class="container_box">
		<div class="title_box">
			{{ title }}
		</div>
		<div class="workspace_box">
			<div class="tools_box">
				<ul class="tools_ul">
					<li class="tools_li tools_choose_type">
						<!-- {{ type }} -->
						<img src="../../static/icon/types.png" class="tools_icon" alt="">
						<ul class="choose_types">
							<li class="type">Chair</li>
							<li class="type">Table</li>
						</ul>
					</li>
					<li class="tools_li">{{ sketch }}</li>
					<li class="tools_li">{{ eraser }}</li>
					<li class="tools_li">{{ undo }}</li>
					<li class="tools_li">{{ cancel }}</li>
					<li class="tools_li">{{ download }}</li>
				</ul>
			</div>
			<div class="sketch_box">

			</div>
			<div class="overall_box">

			</div>
			<div class="part_box">

			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'ShadowGuidance',
	data() {
		return {
			title: '3D Shadow Guidance for Model Generation',
			type: 'type',
			sketch: 'sketch',
			eraser: 'eraser',
			undo: 'undo',
			cancel: 'cancel',
			download: 'download'
		}
	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container_box {
	margin: 0;
	padding: 0;
	width: 100%;
	height: 100%;
	/* background: #a4e2c6; */
	color: #4c8dae;
}

.title_box {
	height: 60px;
	line-height: 60px;
	font-weight: bold;
}

.workspace_box {
	/* padding: 0 10px; */
	/* width: calc(100% - 20px); */
	width: 100%;
	height: calc(100% - 60px);
	/* background: #a4e2c6; */
}

.tools_box {
	width: 100px;
	height: 100%;
	display: inline-block;
	vertical-align: top;
	margin-right: 20px;
	/* border-right: 1px solid red; */
}

.tools_ul {
	margin: 0;
	padding: 0;
}

.tools_ul .tools_li {
	list-style-type: none;
	display: block;
	width: 100%;
	height: 100px;
	line-height: 100px;
	border: 1px solid #4c8dae;
	/* border-top: 0; */
	border-radius: 10px;
	margin: 5px 0;
	font-weight: bold;
}

.tools_icon {
	width: 100%;
	height: 100%;
}

.tools_ul .tools_li:hover {
	cursor: pointer;
	background: #4c8dae;
	color: #fff;
}

.tools_ul .tools_li:first-child {
	/* border-top: 1px solid #fff; */
	margin-top: 0;
}

.tools_choose_type {
	position: relative;
}

.choose_types {
	padding: 10px;
	width: 100px;
	/* border: 1px solid red; */
	position: absolute;
	left: 102px;
	top: 10px;
	border-radius: 10px;
	background: #4c8dae;
	color: #fff;
	display: none;
}

.choose_types .type {
	list-style: none;
	width: 100%;
	/* text-align: center; */
	height: 30px;
	line-height: 30px;
}

.choose_types .type:hover {
	cursor: pointer;
	background: #fff;
	color: #4c8dae;
}

.tools_choose_type:hover .choose_types {
	display: block;
}

.sketch_box {
	width: 35%;
	height: 95%;
	border: 1px solid #4c8dae;
	display: inline-block;
}

.overall_box {
	width: 35%;
	height: 95%;
	border: 1px solid #4c8dae;
	display: inline-block;
}

.part_box {
	width: 20%;
	height: 95%;
	border: 1px solid #4c8dae;
	display: inline-block;
}
</style>
