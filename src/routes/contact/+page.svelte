<script>  
	import { fade } from 'svelte/transition';
	
	let skills = [
    {
      title: "Svelte",
      description: "Self-taught Svelte engineer for front-end development.",
      imageUrl: "https://upload.wikimedia.org/wikipedia/commons/1/1b/Svelte_Logo.svg",
			strength: 50
    },
		{
			title: "React",
      description: "ReactJS skills learned in University for full-stack web-app development.",
      imageUrl: "https://upload.wikimedia.org/wikipedia/commons/4/47/React.svg",
			strength: 80
    },
    {
			title: "Angular",
      description: "AngularJS skills learned in University for full-stack web-app development",
      imageUrl: "https://upload.wikimedia.org/wikipedia/commons/c/cf/Angular_full_color_logo.svg",
			strength: 80
    },
  ];
</script>

{#each skills as skill}
<div in:fade class="box">
		<div class="hero">
			<h2>
				{skill.title}
			</h2>
				<img src="{skill.imageUrl}" width="50" height="50" alt="Logo Placeholder">
			<br>
			<p>
				{skill.description}
			</p>
			<br>
			<div class="skillbar {skill.title}">
				<h3>
					Experience: {skill.strength}%
				</h3>
			</div>
		</div>
</div>
{/each}
<style>
 .box {
    width: 300px;
    border: medium rgb(0, 0, 0);
    padding: 5vh;
    border-radius: 0.5vh;
	 	margin: 10vh;
	 	border-style: groove dotted ridge;
  }
	h3{
		text-align:left;
		padding-left:1em;
	}
	.skillbar {
		text-align: right; /* Right-align text */
		padding-top: 10px; /* Add top padding */
		padding-bottom: 10px; /* Add bottom padding */
		color: white; /* White text color */
		width: 100%; /* Full width */
		background-color: #ddd; /* Grey background */
		border:medium rgb(0, 0, 0);
		border-style: dashed;
	}
	.Svelte {width: 65%; background-color: #FF3C00;} /* Svelte Orange - Coquelicot */
	.Angular {width: 80%; background-color: #B52E31;} /* Angular Red - American Red */
	.React {width: 80%; background-color: #61DBFB;} /* React Blue - Crayola Sky Blue */
	
</style>
