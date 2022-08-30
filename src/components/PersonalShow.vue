<template>
	<div style="width:55%;margin:0 auto;height:99.9vh">
		<h5>Team Member Information</h5>
		<h1 style="height: 80px;margin:3% 0 0 3%;">Tim</h1>
		<div style="height: 100%;">
			<!-- head -->
			<div style="border-bottom: 2px solid lightgray;display: flex;justify-content: space-between;">
				<span><span style="line-height: 30px;height:30px;vertical-align: bottom;">Description</span>
				</span>
			</div>
			<!-- part1 -->
			<div class="bor" style="display: flex;justify-content: space-between;margin-top: 1%;min-height:250px;max-height:450px;">
				<div style="width:65%;">
					<ul class="ful">
						<li>
							hello im tom!
						</li>
					</ul>
				</div>
				<div style="width:30%;display: flex;align-items: center;justify-content: center;">
					<img class="yuanxing" src="../assets/bob.png"  alt="null"/>
				</div>
			</div>
			<!-- part2 -->
			<div style="border-bottom: 2px solid lightgray;display: flex;justify-content: space-between;margin-top:2%;">
				<span><span style="line-height: 30px;height:30px;vertical-align: bottom;">Personal Goals</span>
				</span>
			</div>
			<div style="min-height:30%;max-height:45%;margin-top: 1%;border-bottom: 2px solid lightgray;" class="bor">
				<ul class="ful2">
					<li v-for="(item,index) in goals" :key="index">Goal {{index+1}}:    {{item}}</li>
				</ul>
			</div>
			<!-- footer -->
			<h1 style="margin:3% 0 0 3%;">Personal Task Status</h1>
			<div style="height: 40%;">
				
				<ul class="ful3">
					<li><h3>In progress</h3></li>
					<li>Task1:prepare midterm exam</li>
					<li>Task2: complete midterm exam</li>
					<li>Task3</li>
				</ul>
				<ul class="ful3">
					<li><h3>Future</h3></li>
					<li>Task1:complete final exam</li>
					<li>Task2</li>
					<li>Task3</li>
				</ul>
				<ul class="ful3">
					<li><h3>Done</h3></li>
					<li>Task1</li>
				</ul>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'PersonalShow',
		props: {

		},
		data() {
			return {
				goals: ['go shop mart with mum!'],
			}
		},
		methods: {
			
		},

	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	tr {
		height: 5%;
	}

	td {
		width: 50%;
	}

	tr:nth-of-type(2),
	tr:nth-of-type(4) {
		background-color: lightgray;
	}
	.ful3{
		margin-top:3%;
	}
.ful3>li{
	margin-left:5%;
	height:30px;
	list-style: none;
}
	button {
		width: 60px;
		height: 30px;
	}

	.ful {
		width: 100%;
		margin: 8% 0 0 2%;
	}

	.ful2 {
		text-align: center;
		width: 100%;
		margin: 2% 0 0 2%;
	}

	.ful>li {
		list-style: none;
		min-height:30px;max-height: 70px;
		margin: 2% 0;
		width: 90%;
		display: flex;
		justify-content: space-between;
		
		overflow-y:scroll;
	}

	.ful2>li {
		list-style: none;
		min-height:30px;max-height: 70px;
		margin: 2% 0;
		display: flex;
		overflow-y:scroll;
		justify-content: space-between;
	}

	.imgicon {
		width: 20px;
		height: 20px;
	}

	.yuanxing {
		width: 200px;
		height: 200px;
		border: 1px solid black;
		margin: 5px 5px 5px 0;
		position: absolute;
		border-radius: 110px;
	}
</style>
