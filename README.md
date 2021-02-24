# Amortizing and Accreting Caps and Floors Valuation Practical Guide

Overview
An amortizing cap is an interest rate cap whose notional principal amount declines during the life of the contract whereas an accreting cap is an interest rate cap whose notional principal amount increases during the life of the contract. Similarly, an amortizing floor is an interest rate floor whose notional principal amount declines during the life of the contract whereas an accreting floor is an interest rate floor whose notional principal amount increases during the life of the contract. 

An interest rate cap is a financial contract between two parties that provides an interest rate ceiling or cap on the floating rate payments. It consists of a series of European call options (caplets) on interest rates. An amortizing cap is an interest rate cap whose notional principal amount declines during the life of the contract whereas an accreting cap is an interest rate cap whose notional principal amount increases during the life of the contract.

An amortizing cap is primarily used to hedge loans whose principal declines on a scheduled basis while an accreting cap is primarily used to hedge construction loans whose principal increases on a scheduled basis to meet the expanding working capital requirements. Amortizing caps are frequently purchased by issuers of floating rate debt where the loan principal declines during the life. Similarly accreting caps are frequently purchased by issuers of floating rate debt where the loan principal increases during the life. The holders wish to protect themselves from the increased financing costs that would result from a rise in interest rates. This presentation gives an overview of interest rate amortizing or accreting cap products and valuation model. 


KeyWords
amortizing cap, amortizing floor, accreting cap, accreting floor, Interest rate cap, interest rate floor, caplet, floorlet, valuation, Black model, finance, financial product


	Interest Rate Amortizing or Accreting Cap Introduction
	An interest rate cap is a financial contract between two parties that provides an interest rate ceiling or cap on the floating rate payments.
	An interest rate cap actually consists of a series of European call options (caplets) on interest rates. 
	An amortizing cap is an interest rate cap whose notional principal amount declines during the life of the contract.
	An accreting cap is an interest rate cap whose notional principal amount increases during the life of the contract.

	The Benefits of an Amortizing or Accreting Cap
	An amortizing cap is primarily used to hedge loans whose principal declines on a scheduled basis.
	An accreting cap is primarily used to hedge construction loans whose principal increases on a scheduled basis to meet the expanding working capital requirements.
	Amortizing caps are frequently purchased by issuers of floating rate debt where the loan principal declines during the life.
	Amortizing caps are frequently purchased by issuers of floating rate debt where the loan principal increases during the life.
	The holders wish to protect themselves from the increased financing costs that would result from a rise in interest rates.

	Caplet Payoff
	The payoff of a caplet is given by
Payoff=N_i*τ*max(R-K,0)
where N_i – the notional of period i; R – the realized interest rate; K – the strike; τ – the day count fraction.
	Payoff diagram
 

	Valuation
	The analytics is similar to a vanilla cap the principal amount used by each period may be different.
	The present value of an amortizing or accreting cap is given by
PV(0)=∑_(i=1)^n▒〖N_i τ_i D_i (F_i Φ(d_1 )-KΦ(d_2)) 〗
where 
D_i=D(0,T_i) – the discount factor; 
F_i=F(t;T_(i-1),T_i )=(D_(i-1)/D_i -1)/τ_i – the forward rate for period (T_(i-1),T_i).
Φ – the accumulative normal distribution function
d_1,2=(ln⁡(F_i/K)±0.5σ_i^2 T_i)/(σ_i √(T_i ))

	Practical Notes
	Interest rate caps are valued via the Black model in the market.
	The forward rate is simply compounded.
	The first key to value a cap is to generate the cash flows. The cash flow generation is based on the start time, end time and payment frequency, plus calendar (holidays), business convention (e.g., modified following, following, etc.) and whether sticky month end.
	Then you need to construct interest zero rate curve by bootstrapping the most liquid interest rate instruments in the market. The most common used yield curve is continuously compounded.
	Another key for accurately pricing an outstanding cap/floor is to construct an arbitrage-free volatility surface. 
	The accrual period is calculated according to the start date and end date of a cash flow plus day count convention
	The formula above doesn’t contain the last live reset cash flow whose reset date is less than valuation date but payment date is greater than valuation date. The reset value is 
〖PV〗_reset=N_0*τ*max(R-K,0)

   which should be added into the above present value.

	A Real World Example
Cap Terms and Conditions	Notional Schedule
Buy Sell	Sell	9000000	2/6/2015
Strike	0.025	8785714.29	3/31/2015
Trade Date	2/6/2015	8464285.72	6/30/2015
Start Date	2/6/2015	8142857.15	9/30/2015
Maturity Date	2/4/2019	7821428.58	12/31/2015
Currency	USD	7500000.01	3/31/2016
Day Count	dcAct360	7178571.44	6/30/2016
Rate type	Float	6857142.87	9/30/2016
Notional	9000000	6535714.3	12/30/2016
Pay Receive	Pay	6214285.73	3/31/2017
Payment Frequency	1M	5892857.16	6/30/2017
Index Tenor	1M	5571428.59	9/29/2017
Index Type	LIBOR	5250000.02	12/29/2017
		4928571.45	3/30/2018



You can find more details at
https://finpricing.com/knowledge.html
