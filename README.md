# WithdrawalTiming

Optimized Timing of Withdrawals based upon your Personalized Portfolios Performance of Tax Deferred, Taxable and Tax Free Investments.

![Screenshot]()

## Description

This application can be run with a trigger URL and API secret of Sequence rules to trigger them immediately.

### Features

- Calls a series of Restful endpoints that return historical daily returns for all investments in your personal portfolios. These are broken into three groups by taxable assett location status: Tax Deferred, Taxable and Tax Free.
- A composite daily closing cost is then computed by applying your personal Percent allocations of each investment assett.
- This data is then scaled between the max and min for the date range under consideration.
- A moving average is then calculated to smooth the results.
- The current composite scaled close is then compared to the last market high for your personal portfolios.
- 
Normal market: If your personal portfolio performance is less than 10% away from its highs, you take a distribution from your investments.
Correction: If your personal portfolio performance is more than 10% away from its highs but less than 20% away from its highs, you take a scaled increment from both investemnt and cash reserves.
Bear market: If the S&P 500 is more than 20% away from its highs, you spend none of your discretionary spending in the next year.

### Built with

- C#
- Alpha Vantage API

## Getting started

### Prerequisites

N/A.

### Install

Install by running the MSI file: <a href="SequenceAPITest Installer.msi" download>Click to Download</a>

### Configure

N/A.

### Usage

- Run interactively from the command line.
![Screenshot](UsageScreenShot1.png)

- Schedule to run repeatedly using Windows Task Scheduler.
![Screenshot](UsageScreenShot2.png)

- Create a shortcut to the command line passing arguments.
![Screenshot](UsageScreenShot3.png)

### Acknowledgements

Thanks to [RestSharp - Simple .NET REST Client](https://github.com/restsharp/RestSharp?tab=readme-ov-file#restsharp---simple-net-rest-client) developers.

### To-do

- [X] Add Idempotency UUID(GUID) generated automatically to constrain the request.
- [ ] Add additional specific response driven error handling

### License

This project is licensed under the [GPL-3.0 License](LICENSE.txt).
