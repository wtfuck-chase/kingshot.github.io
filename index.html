<!DOCTYPE html>
<html>
<head>
    <title>Kingshot POS - RYS Elite</title>
    <style>
        body { font-family: sans-serif; background: #121212; color: #e0e0e0; padding: 20px; }
        .container { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; }
        .pos-panel, .dashboard { background: #1e1e1e; padding: 20px; border-radius: 8px; border: 1px solid #333; }
        h2 { color: #00ffcc; border-bottom: 1px solid #333; padding-bottom: 10px; }
        input, select { width: 100%; padding: 10px; margin: 10px 0; background: #2a2a2a; border: 1px solid #444; color: white; }
        .grid-buttons { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
        button { padding: 15px; cursor: pointer; font-weight: bold; border-radius: 4px; border: none; transition: 0.2s; }
        .tier-btn { background: #007bff; color: white; }
        .tier-btn:hover { background: #0056b3; }
        .tier-btn span { display: block; font-size: 10px; opacity: 0.8; }
        table { width: 100%; border-collapse: collapse; margin-top: 20px; }
        th, td { text-align: left; padding: 12px; border-bottom: 1px solid #333; }
        th { background: #252525; }
        .export-btn { background: #28a745; color: white; width: 100%; margin-top: 20px; }
    </style>
</head>
<body>

<h1>⛈️ RYS INTERNAL POS</h1>

<div class="container">
    <div class="pos-panel">
        <h2>Register Transaction</h2>
        <label>Search Player ID/Name</label>
        <input type="text" id="playerRef" placeholder="Enter ID (e.g. 1001)">
        
        <label>Select Key Pack</label>
        <div class="grid-buttons">
            <button class="tier-btn" onclick="addSale(600, 99.99)">TIER 5<span>600 Keys | $99.99</span></button>
            <button class="tier-btn" onclick="addSale(300, 49.99)">TIER 4<span>300 Keys | $49.99</span></button>
            <button class="tier-btn" onclick="addSale(120, 19.99)">TIER 3<span>120 Keys | $19.99</span></button>
            <button class="tier-btn" onclick="addSale(60, 9.99)">TIER 2<span>60 Keys | $9.99</span></button>
            <button class="tier-btn" onclick="addSale(30, 4.99)">TIER 1<span>30 Keys | $4.99</span></button>
        </div>
        <button class="export-btn" onclick="exportData()">DOWNLOAD MONTHLY CSV</button>
    </div>

    <div class="dashboard">
        <h2>Live Leaderboard</h2>
        <table id="leaderboard">
            <thead>
                <tr>
                    <th>Player ID</th>
                    <th>Total Keys</th>
                    <th>Total Spend</th>
                </tr>
            </thead>
            <tbody></tbody>
        </table>
    </div>
</div>

<script>
    let sales = JSON.parse(localStorage.getItem('rys_sales')) || [];

    function addSale(keys, price) {
        const id = document.getElementById('playerRef').value;
        if (!id) return alert("Enter a Player ID first!");
        
        sales.push({ id, keys, price, date: new Date().toISOString() });
        localStorage.setItem('rys_sales', JSON.stringify(sales));
        updateDashboard();
    }

    function updateDashboard() {
        const totals = {};
        sales.forEach(s => {
            if (!totals[s.id]) totals[s.id] = { keys: 0, price: 0 };
            totals[s.id].keys += s.keys;
            totals[s.id].price += s.price;
        });

        const sorted = Object.entries(totals).sort((a,b) => b[1].price - a[1].price);
        const tbody = document.querySelector('#leaderboard tbody');
        tbody.innerHTML = sorted.map(([id, data]) => `
            <tr>
                <td>${id}</td>
                <td>${data.keys}</td>
                <td>$${data.price.toFixed(2)}</td>
            </tr>
        `).join('');
    }

    function exportData() {
        let csv = "Date,PlayerID,Keys,Price\n";
        sales.forEach(s => csv += `${s.date},${s.id},${s.keys},${s.price}\n`);
        const blob = new Blob([csv], { type: 'text/csv' });
        const url = window.URL.createObjectURL(blob);
        const a = document.createElement('a');
        a.setAttribute('href', url);
        a.setAttribute('download', 'RYS_Monthly_Report.csv');
        a.click();
    }

    updateDashboard();
</script>
</body>
</html>
