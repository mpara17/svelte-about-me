<script>
  let name = "Monica"; // Change this to your name
  let favoriteNumber = 17; // Change this to your favorite number
  let bio = "I am a data analyst with a passion for building cool things!";
  let hobbies = ["Coding", "Reading", "Traveling"]; // List some hobbies
</script>

<style>
  h1 {
    color: #2c3e50;
    font-family: Arial, sans-serif;
  }
  .container {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    text-align: center;
  }
  .hobbies {
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
  }
  .hobby {
    background-color: #3498db;
    color: white;
    padding: 10px 15px;
    border-radius: 5px;
  }
</style>

<div class="container">
  <h1>About Me</h1>
  <p>Hello, my name is <strong>{name}</strong>!</p>
  <p>My favorite number is <strong>{favoriteNumber}</strong>.</p>
  <p>{bio}</p>

  <h2>My Hobbies</h2>
  <div class="hobbies">
    {#each hobbies as hobby}
      <div class="hobby">{hobby}</div>
    {/each}
  </div>
</div>
