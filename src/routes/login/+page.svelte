<script>
	import Navbar from "$lib/components/Navbar.svelte";

    let username = "";
    let password = "";
  
    function handleSubmit() {

      // ส่งข้อมูลไปยังเซิร์ฟเวอร์หรือทำการลงทะเบียนตามที่คุณต้องการ
      alert("Registration successful");
    }
  </script>
  
  <Navbar />
  <main class="min-h-screen flex items-center justify-center bg-gray-100">
    <div class="bg-white p-8 shadow-md rounded-md w-full sm:w-96">
      <h1 class="text-2xl font-semibold mb-4">Login</h1>
      <form on:submit={handleSubmit}>
        <div class="mb-4">
          <label for="username" class="block font-medium mb-1">Username</label>
          <input
            type="text"
            id="username"
            bind:value={username}
            class="w-full border rounded-md px-3 py-2 focus:outline-none focus:ring focus:border-blue-300"
            required
          />
        </div>
        <div class="mb-4">
          <label for="password" class="block font-medium mb-1">Password</label>
          <input
            type="password"
            id="password"
            bind:value={password}
            class="w-full border rounded-md px-3 py-2 focus:outline-none focus:ring focus:border-blue-300"
            required
          />
        </div>
        <button
          type="submit"
          class="w-full bg-blue-500 text-white py-2 rounded-md hover:bg-blue-600 focus:outline-none focus:ring focus:ring-blue-300"
        >
          Login
        </button>
      </form>
    </div>
  </main>

  