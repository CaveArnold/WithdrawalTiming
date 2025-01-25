# WithdrawalTiming

Optimized Timing of Withdrawals based upon your Personalized Portfolios Performance of Tax Deferred, Taxable and Tax Free Investments.

![Screenshot]()

## Description

This application can be run passing in the portfolio makeup for each taxable portfolio type.
It can then be used to decide optimally for your personal investments where to pull from for any given withdrawal.
It can also be used to deceide optimally for your personal investments let you know when to make a Roth conversion based on a defined percent off the high in your tax deferred investments.

### Features

- Calls a series of Restful endpoints that return historical daily returns for all investments in your personal portfolios. These are broken into three groups by taxable assett location status: Tax Deferred, Taxable and Tax Free.
- A composite daily closing cost is then computed by applying your personal Percent allocations of each investment assett.
- This data is then scaled between the max and min for the date range under consideration.
- A moving average is then calculated to smooth the results.
- The current composite scaled close is then compared to the last market high for your personal portfolios.

  - Normal market: If your personal portfolio performance is less than 10% away from its highs, you take a distribution from your investments.
  - Correction: If your personal portfolio performance is more than 10% away from its highs but less than 20% away from its highs, you take a scaled increment from both investemnt and cash reserves. (e.g. If 14.3% from high then take 43% from investments and 57% from cash.)
  - Bear market: If your personal portfolio performance is more than 20% away from its highs, you take 100% from cash reserves.

### Built with

- Excel
- Alpha Vantage API

## Getting started

### Prerequisites

N/A.

### Install

Download Excel Workbook.

### Configure

N/A.

### Usage

- Update with your personal holdings.

### Acknowledgements



### To-do

- [ ] Automate with C#.


### License

This project is licensed under the [GPL-3.0 License](LICENSE.txt).
