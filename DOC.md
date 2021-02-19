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

+ globalCollateralRatio()

    理论质押率
    
+ mint(address collateralToken, uint256 collateralAmount, uint256 minimumReceived)

    100% 抵押物增发
    
    @collateralToken           抵押物代币
    
    @collateralAmount          抵押物数量
    
    @minimumReceived           最小允许收到的数量

+ mint(uint256 shareAmount, uint256 minimumReceived)

    100% KUN抵押增发
    
    @shareAmount     KUN的数量
    
    @minimumReceived 最小允许收到的数量

+ mint(address collateralToken, uint256 collateralAmount, uint256 shareAmount, uint256 minimumReceived)
    
    混合抵押增发
    
    @collateralToken 抵押物代币
    
    @collateralAmount 抵押物数量
    
    @shareAmount KUN数量
    
    @minimumReceived 最小允许收到的数量
