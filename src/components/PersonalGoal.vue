<template>
	<div style="width:55%;margin:0 auto;height:99.9vh">
		<h1 style="height: 80px;margin:3% 0 0 3%;">Personal Goals</h1>
		<div style="height: 100%;">
			<!-- head -->
			<div style="border-bottom: 2px solid lightgray;display: flex;justify-content: space-between;">
				<span><span style="line-height: 30px;height:30px;vertical-align: bottom;">Upcoming Goals</span>
				<img src="../assets/奖杯1.png" style="width:30px;height:30px;vertical-align: bottom;"  alt="null"/></span>
				<span><a @click="add"><img src="../assets/plus.svg" class="imgicon"
                                   alt="null"/></a></span>
			</div>
			<!-- part1 -->

			<div class="bor" style="display: flex;justify-content: space-between;margin-top: 1%;min-height:250px;">
				<div style="width:65%;">
					<ul class="ful">
						<li v-for="(item,index) in goals" :key="index" v-show="goalsed.indexOf(item)===-1">
							Goal {{index+1}}:    {{item}}
								<div>
									<button id="finish" @click="finish(item,index)"></button>
									<button id="del" @click="del(item)"></button></div>
						</li>
					</ul>
				</div>
				<div style="width:30%;display: flex;align-items: center;justify-content: center;">
					<img class="photo" src="../assets/bob.png"  alt="null"/>
				</div>
			</div>
			<!-- part2 -->
			<div style="border-bottom: 2px solid lightgray;display: flex;justify-content: space-between;margin-top:2%;">
				<span><span style="line-height: 30px;height:30px;vertical-align: bottom;">Achieved Goals</span><img
						src="../assets/奖杯2.png" style="width:30px;height:30px;vertical-align: bottom;"  alt="null"/></span>
			</div>
			<div
          style="min-height:30%;margin-top: 1%;border-bottom: 2px solid lightgray;"
          class="bor">
        <ul class="ful2">
          <li v-for="(item,index) in goalsed" :key="index">Complete Goal
            {{ indexs[index] + 1 }}: {{ item }}
            <div style="float: left;margin-right: 5px"><img
                src="../assets/submit.svg"
                                 style="width: 15px;height:
            15px " alt="null"></div>
          </li>
        </ul>
			</div>
			<!-- footer -->
			<h2 style="margin:3% 0 0 3%;">Personal Health Score
        Detail</h2>
			<div style="height: 40%;">
				<table class="HealthScore"
               style="height:70%;width: 100%;border-spacing:0;">
					<tr>
						<td>Finished Personal Task 1</td>
						<td>+5</td>
					</tr>
					<tr>
						<td>Overdue Personal Task 2</td>
						<td>-5</td>
					</tr>
					<tr>
						<td>Finished Personal Task 3</td>
						<td>+5</td>
					</tr>
					<tr>
						<td>Overdue Personal Task 4</td>
						<td>-5</td>
					</tr>
				</table>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'PersonalGoal',
		props: {

		},
		data() {
			return {
				goals: ['Check Email box',
          'reply Email','today i want to shop mart with my grandma and you?'],
				goalsed: [],indexs:[]
			}
		},
		methods: {
			add() {
				var goal = prompt("Input your goals：");
				if (goal !== '' && goal != null) {
					this.goals.push(goal)
				} else {
					alert('Error')
				}
			},
			finish(item,index){
				this.goalsed.push(item);this.indexs.push(parseInt(index));
			},
			del(item){
				const index=this.goals.indexOf(item)
				this.goals.splice(index,1);
			}
		},

	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	tr {
		height: 3%;
	}

	td {
		width: 45%;
	}

	tr:nth-of-type(2),
	tr:nth-of-type(4) {
		background-color: lightgray;
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
		width: 100%;
		margin: 2% 0 0 2%;
	}

	.ful>li {
		list-style: none;
		min-height:30px;
    max-height: 70px;
    margin: 4% 0;
    font-size: 10px;
		display: flex;
    flex-direction: column;
    justify-content: center;
	}

	.ful2>li {
		list-style: none;
		min-height:30px;
    max-height: 70px;
		margin: 2% 0;
    font-size: 10px;
	}

	.imgicon {
		width: 20px;
		height: 20px;
    cursor: pointer;
    box-shadow: 1px 1px 7px #ffffff;
	}
  .imgicon:active{
    box-shadow: 1px 1px 7px #ffffff;
    transform: translateY(4px);
  }

	.photo {
		width: 200px;
		height: 200px;
		margin: 5px 5px 5px 0;
		position: absolute;
		border-radius: 110px;
	}
  #finish{
    outline: none;
    width: 20px;
    height: 20px;
    margin-top:5px;
    margin-left: 5px;
    margin-right: 5px;
    border: solid 0 black;
    border-radius: 50%;
    font-size: 0.8rem;
    padding: 0;
    background-image: url("../assets/submit.svg");
    background-repeat: no-repeat;
    background-size: 100% 100%;
    cursor: pointer;
    box-shadow: 1px 1px 7px #4242ad;

  }
  #del{
    outline: none;
    width: 20px;
    height: 20px;
    margin-top:5px;
    margin-left: 5px;
    margin-right: 5px;
    border: solid 0 black;
    border-radius: 50%;
    font-size: 0.8rem;
    padding: 0;
    background-image: url("../assets/del.svg");
    background-repeat: no-repeat;
    background-size: 100% 100%;
    cursor: pointer;
    box-shadow: 1px 1px 6px red;

  }
  #finish:active{
    box-shadow: 1px 1px 7px #4242ad;
    transform: translateY(4px);
  }
  #del:active{
    box-shadow: 1px 1px 6px red;
    transform: translateY(4px);
  }

</style>
