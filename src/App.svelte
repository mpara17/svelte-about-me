<script>
  let name = "Monica"; // Change this to your name
  let favoriteNumber = 17; // Change this to your favorite number
  let bio = "I am a data analyst with a passion for building cool things!";
  let hobbies = ["Coding", "Reading", "Traveling"]; // List some hobbies
  
  import ImageCard from "./lib/ImageCard.svelte";
  
  let cardData = [
    {
      image:
        "https://cdn.prod.website-files.com/59e16042ec229e00016d3a66/64389b816c805d102971292f_ultimate%20guide%20to%20data%20visualization_blog%20hero.webp",
      title: "Data Visualizations",
      description:
        "I love solving problems and writing code to build data visualizations across the Chicago Tech Scene.",
    },
    {
      image: "https://miro.medium.com/v2/resize:fit:780/1*TyzOHIDBZ4-v7MVoYibH6w.jpeg",
      title: "Reading",
      description: "I love reading books on technology and leadership.",
    },
    {
      image: "https://www.imediasummits.com/hs-fs/hubfs/ORSAU%2024-1.png?width=3000&height=699&name=ORSAU%2024-1.png",
      title: "Traveling",
      description:
        "I had the opportunity to travel across Europe and Australia these past few months",
    },
  ];
</script>

<style>
  :global(body) {
    background-color: white;
    color: blue;
    margin: 0;
    padding: 0;
  }
  
  h1, h2, p {
    color: blue;
    font-family: Arial, sans-serif;
  }
  
  .container {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    text-align: center;
    background-color: white;
  }
  .hobbies {
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
  }
  .hobby {
    background-color: blue;
    color: white;
    padding: 10px 15px;
    border-radius: 5px;
  }
  
  .card-container {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-top: 20px;
    flex-wrap: wrap;
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

 <h2>Some of My Favorite Things</h2>
  <div class="card-container">
    {#each cardData as { image, title, description }}
      <ImageCard {image} {title} {description} />
    {/each}
  </div>
