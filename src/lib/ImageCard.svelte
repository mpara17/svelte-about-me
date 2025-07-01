<script>
  export let image;
  export let title;
  export let description;
</script>

<div class="card">
  <img src={image} alt={title} class="card-image" />
  <div class="card-content">
    <h3 class="card-title">{title}</h3>
    <p class="card-description">{description}</p>
  </div>
</div>

<style>
  .card {
    background: white;
    border: 2px solid blue;
    border-radius: 8px;
    overflow: hidden;
    margin: 10px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    transition: transform 0.2s;
    width: 300px;
    height: 400px;
    display: flex;
    flex-direction: column;
  }
  
  .card:hover {
    transform: translateY(-2px);
  }
  
  .card-image {
    width: 100%;
    height: 200px;
    object-fit: cover;
  }
  
  .card-content {
    padding: 15px;
    flex: 1;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  
  .card-title {
    color: blue;
    margin: 0 0 10px 0;
    font-size: 1.2em;
  }
  
  .card-description {
    color: blue;
    margin: 0;
    line-height: 1.4;
  }
</style> 