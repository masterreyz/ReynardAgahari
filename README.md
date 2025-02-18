# ReynardAgahari

# Ini Risk Calculator dan Position Sizing
ticker = (str(input('Ticker name:\n')))
# print(type(ticker))
purchase_price = int(input('Harga beli saham per share:\n'))

stop_loss_price = int(input('Stop loss price per share:\n'))

max_loss_per_share = int(purchase_price - stop_loss_price)

capital = int(input('Capital akun sekuritas anda:\n'))

max_loss_per_trade = int(input('Max loss per trade:\n'))
# print(type(max_loss_per_trade))
two_persen_risk = int(2 / 100 * capital)
print(f"Max risk 2% capital = {two_persen_risk}")

position_sizing_1 = two_persen_risk / max_loss_per_share
position_sizing_1_lot = float(position_sizing_1 / 100)
print(f"Jadi menurut 2% risk, max beli: {position_sizing_1_lot} lot")
