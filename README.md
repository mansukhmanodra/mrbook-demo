<!DOCTYPE html>
<html lang="en" data-theme="light">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>MrBook Admin Dashboard</title>
  <style>
    :root {
      --bg-light: #f4f6f8;
      --bg-dark: #121212;
      --text-light: #1f1f1f;
      --text-dark: #ffffff;
      --primary: #007bff;
      --card-light: #ffffff;
      --card-dark: #1e1e1e;
    }
    [data-theme="light"] {
      --bg: var(--bg-light);
      --text: var(--text-light);
      --card: var(--card-light);
    }
    [data-theme="dark"] {
      --bg: var(--bg-dark);
      --text: var(--text-dark);
      --card: var(--card-dark);
    }
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: var(--bg);
      color: var(--text);
      transition: background-color 0.3s, color 0.3s;
    }
    header {
      background: var(--primary);
      color: white;
      padding: 1rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    nav {
      width: 200px;
      background: #343a40;
      color: white;
      height: 100vh;
      position: fixed;
      top: 60px;
      left: 0;
      padding-top: 1rem;
    }
    nav a {
      display: block;
      color: white;
      text-decoration: none;
      padding: 10px 20px;
    }
    nav a:hover {
      background: #495057;
    }
    main {
      margin-left: 200px;
      padding: 2rem;
    }
    .card {
      background: var(--card);
      border-radius: 8px;
      padding: 1rem;
      margin-bottom: 1rem;
      box-shadow: 0 2px 8px rgba(0,0,0,0.05);
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 1rem;
    }
    .theme-toggle {
      background: white;
      color: #007bff;
      border: none;
      padding: 8px 12px;
      cursor: pointer;
      border-radius: 5px;
    }
  </style>
</head>
<body>

  <header>
    <h1>MrBook – Admin Dashboard</h1>
    <button class="theme-toggle" onclick="toggleTheme()">🌗 Toggle Theme</button>
  </header>

  <nav>
    <a href="#">Dashboard</a>
    <a href="#">Sales</a>
    <a href="#">GST Reports</a>
    <a href="#">Delivery Challan</a>
    <a href="#">Customers</a>
    <a href="#">Settings</a>
  </nav>

  <main>
    <h2>Overview</h2>
    <div class="grid">
      <div class="card">
        <h3>Today's Sales</h3>
        <p>₹12,500</p>
      </div>
      <div class="card">
        <h3>GST Collected</h3>
        <p>₹2,100</p>
      </div>
      <div class="card">
        <h3>Pending Invoices</h3>
        <p>5</p>
      </div>
      <div class="card">
        <h3>Challans Issued</h3>
        <p>3</p>
      </div>
    </div>

    <h2>Quick Links</h2>
    <div class="grid">
      <div class="card">
        <h4>Create Invoice</h4>
        <p>Generate invoice with HSN & GST.</p>
      </div>
      <div class="card">
        <h4>Generate Challan</h4>
        <p>Delivery Challan with auto serials.</p>
      </div>
      <div class="card">
        <h4>GSTR Reports</h4>
        <p>Export GSTR-1, GSTR-3B easily.</p>
      </div>
      <div class="card">
        <h4>Customer Ledger</h4>
        <p>Track payments and dues.</p>
      </div>
    </div>
  </main>

  <script>
    function toggleTheme() {
      const current = document.documentElement.getAttribute('data-theme');
      document.documentElement.setAttribute('data-theme', current === 'light' ? 'dark' : 'light');
    }
  </script>

</body>
</html>

