"use client";

import { useState } from "react";

export default function Page() {
  const [vip, setVip] = useState(false);

  return (
    <div style={{ padding: 20, background: "#0f172a", color: "white", minHeight: "100vh" }}>
      
      <h1>📊 Trading Signals App</h1>

      <button onClick={() => setVip(!vip)} style={{ padding: 10, marginTop: 10 }}>
        {vip ? "VIP Active 🔥" : "Activate VIP"}
      </button>

      <div style={{ marginTop: 20 }}>
        <h2>📈 Signals</h2>

        <div style={{ background: "#1e293b", padding: 10, marginTop: 10 }}>
          EUR/USD - BUY 🟢
        </div>

        <div style={{ background: "#1e293b", padding: 10, marginTop: 10 }}>
          GBP/USD - SELL 🔴
        </div>
      </div>

      {vip && (
        <div style={{ marginTop: 20, padding: 10, background: "purple" }}>
          🔥 VIP MODE ACTIVE
        </div>
      )}

    </div>
  );
}
