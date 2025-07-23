import yfinance as yf
import pandas as pd
import matplotlib.pyplot as plt
from datetime import datetime, timedelta

# --- CONFIGURACIÓN ---
ticker_symbol = "AAPL"
end_date = datetime.today()
start_date = end_date - timedelta(days=60)  # Últimos 2 meses

# --- DESCARGA DE DATOS ---
df = yf.download(ticker_symbol, start=start_date, end=end_date)

# --- LIMPIEZA ---
df = df.reset_index()

# --- GRÁFICO DE LÍNEA ---
plt.figure(figsize=(12, 6))
plt.plot(df['Date'], df['Close'], marker='o', linestyle='-', linewidth=2)

plt.title(f'Evolución del precio de cierre de {ticker_symbol}\n(Últimos 2 meses)')
plt.xlabel('Fecha')
plt.ylabel('Precio de cierre (USD)')
plt.grid(True)
plt.xticks(rotation=45)
plt.tight_layout()
plt.show()
