UniswapIncentive overflow on pre-transfer hooks: Before a token transfer is performed, Fei performs some combination of mint/burn operations via UniswapIncentive.incentivize. Both incentivizeBuy and incentivizeSell calculate buy/sell incentives using overflow-prone math, then mint / burn from the target according to the results. This may have unintended consequences, like allowing a caller to mint tokens before transferring them, or burn tokens from their recipient.

    Recommendation: Ensure casts in getBuyIncentive and getSellPenalty do not overflow

    Major severity finding from Consensys Diligence Audit of Fei Protocol