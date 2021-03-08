# API DOCUMENTS

+ getCollateralTokens()

    获取抵押物列表

+ getCollateralValue(address token)

    @token 抵押物地址

    获取系统中某种抵押物的价值

+ getTotalCollateralValue()

    获取系统中所有抵押物的总价值

+ getCollateralPrice(address token)

    @token 抵押物地址

    获取抵押物价格

+ getStableTokenPrice()

    获取QSD价格

+ getShareTokenPrice()
    
    获取KUN的价格

+ getExcessCollateralValue()

    获取系统盈余的抵押物价值
    
+ getGapCollateralValue

    获取系统抵押物缺口价值

+ globalCollateralRatio()

    理论质押率
+ getCollateralizedBalance(address token)

    获取池抵押物余额
    
+ mint(address collateralToken, uint256 collateralAmount, uint256 minimumReceived)

    100% 抵押物增发
    
    @collateralToken           抵押物地址
    
    @collateralAmount          抵押物数量
    
    @minimumReceived           最小允许收到的QSD数量

+ mint(uint256 shareAmount, uint256 minimumReceived)

    100% KUN抵押增发
    
    @shareAmount     KUN的数量
    
    @minimumReceived 最小允许收到的QSD数量

+ mint(address collateralToken, uint256 collateralAmount, uint256 shareAmount, uint256 minimumReceived)
    
    混合抵押增发
    
    @collateralToken 抵押物地址
    
    @collateralAmount 抵押物数量
    
    @shareAmount KUN数量
    
    @minimumReceived 最小允许收到的QSD数量
    
   
 + redeem(uint256 stableAmount, address receivedCollateralToken, uint256 minimumReceivedCollateralAmount)
    
    100%赎回抵押物
    
    @stableAmount 要赎回的抵押物价值(QSD的数量)
    
    @receivedCollateralToken 要赎回的抵押物地址
    
    @minimumReceivedCollateralAmount 最小允许收到的抵押物数量
    
    
 + redeem(uint256 stableAmount, address collateralToken, uint256 minimumReceivedCollateralAmount, uint256 minimumReceivedShareAmount)

    混合赎回
    
    @stableAmount 要赎回的抵押物价值(QSD的数量)
    
    @collateralToken 要赎回的抵押物地址
    
    @minimumReceivedCollateralAmount 最小允许收到的抵押物数量
    
    @minimumReceivedShareAmount 最小允许收到的KUN数量
    
 + redeem(uint256 stableAmount, uint256 minimumReceivedShareAmount)

    100%赎回KUN
    
    @stableAmount 要赎回的抵押物价值(QSD的数量)
    
    @minimumReceivedShareAmount 最小允许收到的抵押物数量
    
 + claimCollateral()

    取回抵押物

 + recollateralize(address collateralToken, uint256 collateralAmount, uint256 minimumReceivedShareAmount)

    补充抵押物(再抵押)

    @collateralToken 要补充的抵押物地址
    
    @collateralAmount 要补充的抵押物数量
    
    @minimumReceivedShareAmount 最小允许收到的DBK数量
    
 + buyback(uint256 shareAmount, address receivedCollateralToken)
 
    回购抵押物
    
    @shareAmount 要回购的数量(以KUN计)
    
    @receivedCollateralToken 要回购的抵押物地址
    
 + redeemedShares(address account)

   获取用户在系统中可取回的KUN的余额.
   
 + redeemedCollaterals(address account, address token);
    
   获取用户在系统中可取回的抵押物的余额.


 + exchangeShareBond(uint256 bondAmount)

   DBK 兑换成 KUN
   
   @bondAmount DBK的数量
   
 + mintStableBond(uint256 stableAmount, uint256 minimumReceivedBondAmount)

   以QSD购买稳定币债券(DBQ)
   
   @stableAmount 要购买的数量(以QSD计)
   
   @minimumReceivedBondAmount 最小允许收到的DBQ的数量
   
 + redeemStableBond(uint256 stableAmount, uint256 minimumReceivedStableAmount)

   以DBQ赎回稳定币(QSD)
   
   @stableAmount 要赎回的QSD数量
   
   @minimumReceivedStableAmount 最小允许收到的QSD数量


+ stake(uint256 amount)
    
  活期锁定流动性代币
  
  @amount 锁定数量
  
+ stakeLocked(uint256 amount, uint256 secs)

  定期锁定流动性代币
  
  @amount 锁定数量
  @secs 锁定时间(秒)
  
 + withdraw(uint256 amount)
    
    取回活期锁定的流动性代币
  
    @amount 锁定数量
  
  + withdrawLocked(bytes32 kek_id)

    取回定期锁定的流动性代币
  
    @kek_id 锁仓ID
  
  + getReward()
  
    取回收益
  
  + lockedStakes(address account)

    获取用户的锁定列表
   
