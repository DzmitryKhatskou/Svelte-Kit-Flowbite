<script>
  let name = "";
  let email = "";
  let message = "";

  function handleSubmit() {
    // Add your logic for handling form submission here
    console.log("Submitting form...");
    console.log("Name:", name);
    console.log("Email:", email);
    console.log("Message:", message);

    // Additional actions such as sending data to a server
    // can be added here or within the handleSubmit() function
  }
</script>

<div class="max-w-md mx-auto">
  <h2 class="text-2xl font-bold mb-4">Contact Me</h2>
  <form class="space-y-4" on:submit|preventDefault={handleSubmit}>
    <div>
      <label class="block mb-2" for="name">Name</label>
      <input
        class="w-full border border-gray-300 rounded p-2"
        type="text"
        id="name"
        bind:value={name}
        required
      />
    </div>
    <div>
      <label class="block mb-2" for="email">Email</label>
      <input
        class="w-full border border-gray-300 rounded p-2"
        type="email"
        id="email"
        bind:value={email}
        required
      />
    </div>
    <div>
      <label class="block mb-2" for="message">Message</label>
      <textarea
        class="w-full border border-gray-300 rounded p-2"
        id="message"
        bind:value={message}
        required
      />
    </div>
    <div>
      <button class="bg-blue-500 text-white rounded px-4 py-2" type="submit"
        >Submit</button
      >
    </div>
  </form>
</div>
