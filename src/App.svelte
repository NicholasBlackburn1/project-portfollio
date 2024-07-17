<!-- App.svelte -->

<svelte:head>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css">
</svelte:head>

<script>
    let posts = [
        {
            id: 1,
            title: 'First Post',
            content: 'This is the content of the first post.'
        },
        {
            id: 2,
            title: 'Second Post',
            content: 'This is the content of the second post.'
        },
        {
            id: 3,
            title: 'Third Post',
            content: 'This is the content of the third post.'
        }
    ];
</script>

<main class="container mt-4">
    <div class="row">
        <div class="col-md-8">
            <h1 class="mb-4">Svelte Blog</h1>
            {#each posts as post}
                <div class="card mb-4">
                    <div class="card-body">
                        <h5 class="card-title">{post.title}</h5>
                        <p class="card-text">{post.content}</p>
                    </div>
                </div>
            {/each}
        </div>
        <div class="col-md-4">
            <div class="card">
                <div class="card-body">
                    <h5 class="card-title">About Me</h5>
                    <p class="card-text">This is where you can write about yourself or add a profile.</p>
                </div>
            </div>
        </div>
    </div>
</main>

<style>
    main {
        text-align: center;
    }

    h1 {
        color: #ff3e00;
        font-size: 2.5rem;
    }

    .card {
        border: none;
    }

    .card-body {
        padding: 1.25rem;
    }
</style>