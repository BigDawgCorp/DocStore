<svelte:head>
  <title>Edit</title>
  <meta name="description" content="About this app" />
</svelte:head>
  
<script>
  let inputValue = ""; // Initialize the variable to store the input value

  const handleSubmit = () => {
    // Handle the submission here, e.g., send the value to a server
    alert("Submitted: " + inputValue);
  };
  import TextEditor from "./TextEditor.svelte"; // Import the TextEditor component
</script>

<TextEditor bind:inputValue /> <!-- Bind the inputValue to the TextEditor's inputValue -->

<h2>Standalone Input Box:</h2>
<input
  type="text"
  placeholder="Enter your text here"
  bind:value={inputValue}
/>

<button on:click={handleSubmit} style="margin-top: 10px;">Submit</button>
