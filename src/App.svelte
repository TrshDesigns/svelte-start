<!--Script tag used for javascript, we can export 
	variables out of the component like in this 
	example where they are exporting the variable name-->
<script>
	let firstName = "";
	let lastName = "";
	let src = "https://avatars.githubusercontent.com/u/92648615?s=200&v=4";
	let alt = "TheYellowCap";
	
	/*let count = 0;
	let cap = document.getElementById("cap")

	const  incrementCounter = () => {
		count += 1;
	}
	const unknownName = () => {
		name = "unknown"
	}
	*/
	/*const handleInput = (event) => {
		firstName = event.target.value;
	}*/
	
</script>

<!--this is our html tags, this is the code that 
	we export and use when the component is imported
	 in our main js-->

<main>
  <div id="welcome">
    <h1>Hello {firstName}</h1>
    <!--create a button that calls a function called rename-->
    <!-- svelte-ignore a11y-missing-attribute -->
    <!--<button on:click={incrementCounter}><img {alt} {src}></button>
		<h2>Counter: {count}</h2> -->
    <label for="firstName">FirstName</label>
    <input maxlength="10" id="input" type="text" bind:value={firstName} />
    <label for="lastName">LastnName</label>
    <input maxlength="10" id="input" type="text" bind:value={lastName} />

    <!--<button on:click={unknownName}>Set name to unknown</button>-->
  </div>
  <div class="bottomSection">
    <!--a simple user form-->
    <form id="userForm">
      <label for="name">Name:</label>
      <input type="text" id="name" name="name" placeholder="Enter your name" />
      <label for="email">Email:</label>
      <input
        type="email"
        id="email"
        name="email"
        placeholder="Enter your email"
      />
      <label for="message">Message:</label>
      <textarea
        required
        id="message"
        name="message"
        placeholder="Enter your message"
      />
      <br />
      <input type="submit" value="Submit" />
    </form>
    <!-- svelte-ignore a11y-missing-content -->
  </div>
</main>

<!--those are the component styles those will
	 not be applied to other elements with the
	  same clases,tags or ids, those styles are
	   encapsulate for each component-->
<style>
  h1 {
    font-size: 72px;
    text-align: center;
  }
  #welcome {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
    /*add a background gradient from aquamarine to royalblue*/
    background: linear-gradient(to right, aquamarine, royalblue);
    border-bottom: 50px solid rgb(30, 16, 116);
    height: fit-content;
    padding-bottom: 40px;
  }
  .bottomSection {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    /*add a background gradient from pink to green*/
    background: linear-gradient(to top, rgb(175, 24, 107), rgb(30, 16, 116));
    height: fit-content;
    color: white;
  }
  #userForm,
  input, textarea {
    border-radius: 10px;
    padding: 20px;
    backdrop-filter: blur(16px) saturate(180%);
    -webkit-backdrop-filter: blur(16px) saturate(180%);
    background-color: rgba(17, 25, 40, 0.18);
    border-radius: 12px;
    border: 1px solid rgba(255, 255, 255, 0.125);
  }
  label{
	  margin-bottom: 10px;
	  padding:5px;
  }
  #userForm{
	  margin-bottom:40px;
  }
  input:hover, textarea:hover{
	  filter:brightness(1.3);
	  cursor:pointer;
  }
</style>
