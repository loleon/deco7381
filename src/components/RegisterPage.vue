<template>
	<div
      style="width:99.5%;height:100vh;background-size: cover;background-position: center 0;" :style="{backgroundImage:'url('+src+')'}">
		<div style="width:32%;height:100%;margin:0 auto;">
			<div
          style="height:75%;position: relative;top:5%;background-color: white;box-shadow: 4px 4px 15px grey;border-radius: 10px">
				<div style="text-align: center;width:70%;margin:0 auto;padding-top: 2%;">
					<h1 ><img src="../assets/Team-reg.png"
                    style="height:30px;width:30px;margin-top: 15px" alt="null"/>
					<span
              style="height:60px;vertical-align: top;line-height: 60px;margin-left:7%;font-size: 15px">Sign up</span></h1>
					<div>
						<div style="margin-bottom:2%;">
							<div class="propDiv">Name</div>
							<input type="text" class="minput icons"
                     :style="{backgroundImage:'url('+icon1+')'}" placeholder="Enter your full name" />
						</div>
						<div style="margin-bottom:2%;">
							<div class="propDiv">Email</div>
							<input  type="text" class="minput icons" :style="{backgroundImage:'url('+icon2+')'}" placeholder="Enter your UQ Email" />
							
						</div>
						<div style="margin-bottom:2%;">
							<div class="propDiv">Code</div>
							<input  type="text" id="icon3" class="minput icons"
                      style="width:50%;background-size: 10%;"
                      :style="{backgroundImage:'url('+icon3+')'}"
                      placeholder="press 6 digits" />
							<button
                  style="background-color: rgb(176,38,227);color:white;width:30%;height: 30px;font-size: 10px;margin-left: 4px;border-radius: 5px;margin-top: 1px">Send Code</button>
						</div>
						<div style="margin-bottom:2%;">
							<div class="propDiv">Password</div>
							<input  type="password" visiable class="minput icons" :style="{backgroundImage:'url('+icon4+')'}" placeholder="Enter a 6-18 digits password" />
						</div>
						<div style="margin-bottom:2%;">
							<div class="propDiv">RePassword</div>
							<input  type="password" class="minput icons" :style="{backgroundImage:'url('+icon4+')'}" placeholder="Enter password again" />
						</div>
						<div
                style="font-weight: 400;font-size: 10px;margin-top:3%;">
							<input type="checkbox" class="layers-item-selector"
                     /><span
                style="display: inline-block;margin-bottom: 5px">Tick
              and
              agree</span><a
                href="#"><span
                style="color:blue;margin-left:3%;">《User Privacy
              Policy》</span></a>
						</div>
						<div style="margin-top:4%;">
							<button
                  style="width:60%;height:40px;background-color:rgb(176,38,227);color:white;font-size:13px;border:0;border-radius: 5px">Sign Up</button>
						</div>
						<div style="margin-top:2%;font-weight: 500;font-size: 10px">
							Alreay have accound? <a href="#" style="color:rgb(176,38,227)">Login</a>
						</div>
						
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'RegisterPage',
	props: {

	},
	data() {
		return {
			src: require('../assets/bck-reg.jpg'),
			icon1: require('../assets/nickname.svg'),
			icon2: require('../assets/phone.svg'),
			icon3: require('../assets/email-fill.svg'),
			icon4: require('../assets/LOCK.svg'),
			icon5: require('../assets/LOCK.svg'),
		}
	},
}
</script>

<style scoped>
	.icons{
		background-size: 6%;
		background-repeat: no-repeat;
		background-position: 5px 8px;
    opacity: 60%;

	}
  #icon3{
    background-position: 5px 6px;
  }

	.propDiv{
		text-align: left;
    width: 100%;
    margin-left: 20px;
    font-weight: 500;
    transform-origin: 0 0;
    transform:scale(0.7,0.7);
    font-size: 0.1rem;
	}
	.minput {
		border: 1px solid lightgray;
		width: 80%;
		height: 30px;
		line-height: 40px;
		font-size: 12px;
		border-radius: 5px;
		padding-left:8%;
	}
  a{
    text-decoration: none;
  }
  .layers-item-selector {
    outline: none;
    width: 10px;
    height: 10px;
    margin-top:5px;
    margin-left: 15px;
    margin-right: 5px;
    border: solid 1px black;
    border-radius: 50%;
    font-size: 0.8rem;
    padding: 0;
    cursor:pointer;
    appearance: none;
  }
  .layers-item-selector:checked {
    /* background: #0242c6; */
    background: url("../assets/right.svg") no-repeat;
    background-size: 100% 100%;
    border: solid 0 black;
  }

</style>
