<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>現在の待ち時間</title>

  <style>
    body {
      margin: 0;
      height: 100vh;
      font-family: "Segoe UI", sans-serif;
      color: white;
      display: flex;
      justify-content: center;
      align-items: center;
      background-image: linear-gradient(
          rgba(255,255,255,0.3),
          rgba(255,255,255,0.3)
        ),
        url("https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=1950&q=80");
      background-size: cover;
      background-position: center;
    }

    .panel {
      background: rgba(0,0,0,0.25);
      padding: 50px 70px;
      border-radius: 25px;
      text-align: center;
      backdrop-filter: blur(10px);
    }

    .time {
      font-size: 72px;
      font-weight: bold;
      margin: 20px 0;
    }

    .status {
      font-size: 28px;
      margin-top: 10px;
      font-weight: bold;
    }

    .footer {
      position: fixed;
      left: 20px;
      bottom: 20px;
      font-size: 14px;
      opacity: 0.8;
      line-height: 1.5;
    }
  </style>
</head>
<body>

  <div class="panel">
    <h1>現在の待ち時間</h1>
    <div class="time" id="time">-- 分</div>
    <div class="status" id="status">---</div>
  </div>

  <div class="footer" id="footer">
    最終更新：--  
    <br>
    30分おきに更新されます
  </div>

  <!-- Supabase -->
  <script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>

  <script>
    const statusColors = {
      low: "#4caf50",
      mid: "#ffeb3b",
      high: "#f44336"
    };

    const statusTexts = {
      low: "空いています",
      mid: "やや混雑しています",
      high: "混雑しています"
    };

    // ★ supabase → client に変更（衝突防止）
    const client = supabase.createClient(
      "https://uyedrpfchbsilwtcrkpu.supabase.co",
      "sb_publishable_5yHag-b18StN3FOd4d4D6A_pm76IA5e"
    );

    async function fetchData() {
      const { data, error } = await client
        .from("wait_status")
        .select("*")
        .eq("id", 1)
        .single();

      if (error) {
        console.error("Supabase 読み込みエラー:", error);
        return;
      }

      if (data) {
        document.getElementById("time").textContent = data.minutes + " 分";

        const statusEl = document.getElementById("status");
        statusEl.textContent = statusTexts[data.status];
        statusEl.style.color = statusColors[data.status];

        document.getElementById("footer").innerHTML =
          "最終更新：" + data.updated + "<br>30分おきに更新されます";
      }
    }

    // 10秒ごとに Supabase から最新データを取得
    setInterval(fetchData, 10000);
    fetchData();
  </script>

</body>
</html>
