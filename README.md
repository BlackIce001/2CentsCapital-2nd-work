Draw Down w.r.t. FD

It’s assumed you are familiar with very basic trading concepts: mainly buy, sell and thus pnl. We will assume day trading for the purpose of this exercise where all positions are closed by end of day and we have a pnl number for the day. This daily pnl time series will be the input. 

Please read about equity-curve, drawdown (DD) on google if not already familiar with. We are interested in our trading account balance. Daily pnl gets credited to or debited from the account. One can plot x-axis as date and y-axis as account balance, this is the “equity-curve” for our purpose. Whenever there is a -ve pnl, balance goes down, i.e. in DD, till account balance makes a new high, i.e. out of DD. This duration between two consecutive peaks is DD streak/duration (DDS)

Now we introduce a slight twist. We want to measure account DD w.r.t. a fixed deposit. e.g. let’s say FD is paying 0.01% return every day then whenever pnl < 0.01%, it goes in DD. To come out of DD new peak has to be > (previous peak + DDS*0.01).

Given a daily pnl time series and daily FD rate, task is to find
●	Maximum DD (w.r.t FD) and maximum DDS (w.r.t. FD). Note that they might occur at different times, Max DD doesn’t mean DDS was maximum or vice-versa
●	DD streak stats
●	Profit streak stats

You may assume
●	Initial Account Balance - 100000
●	FD return on non trading days is zero

You may still find some variables/conditions not well defined, e.g. what are streak stats. This is intentional and you are expected to make wise and practical inferences & assumptions. Please clearly state any such assumptions made. Please use python and pandas.

Example daily pnl csv 
DD, Max DD and DDS for few initial rows (assuming FD rate of 0.01%)
