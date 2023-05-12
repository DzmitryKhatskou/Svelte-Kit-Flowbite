<script>
  let name = "";
  let email = "";
  let message = "";

  function handleSubmit() {
    // Здесь можно добавить логику для обработки отправки формы
    console.log("Sending...");
    console.log("Name:", name);
    console.log("Email:", email);
    console.log("Сообщение:", message);

    // Дополнительные действия, такие как отправка данных на сервер
    // Можно добавить здесь или в функции handleSubmit()
  }
</script>

<div class="max-w-md mx-auto">
  <h2 class="text-2xl font-bold mb-4">Contact:</h2>
  <form class="space-y-4 text-gray-400" on:submit|preventDefault={handleSubmit}>
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
        >Send</button
      >
    </div>
  </form>
</div>
