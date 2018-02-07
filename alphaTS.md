alphaTS
===================

[![BSD License][bsdlicense-button]][bsdlicense]
[![Code of Conduct][codeofconduct-button]][Code of Conduct]

[bsdlicense-button]: http://img.shields.io/badge/license-BSD-yellow.svg
[bsdlicense]: http://opensource.org/licenses/BSD-3-Clause
[codeofconduct-button]: https://img.shields.io/badge/code%20of%20conduct-contributor%20covenant-green.svg?style=flat-square
[Code of Conduct]: https://github.com/Python-Markdown/markdown/blob/master/CODE_OF_CONDUCT.md

我们在这里定义我们交易所需的所有alpha数据。我们将alphaTS表示为一个文件夹，里面包含了每一支股票以单独文件形式保存的alpha数据。



1. 使用daily数据计算的alphas

   1. gpdsLiquidity: GPDS股票大师单支股票流动性
      $$
      GPDS_t=\frac{|R_{t}|}{TR_{t}}
      $$

   2. absMom30d: 相对于30日前股票自身的动量
      $$
      MOM_t=ln(\frac{close_t}{close_{t-30}})
      $$

   3. absATR30d: 过去30日Absolute ATR波动率

   4. volSpikes3d: 放量指标
      $$
      VS_t=\frac{volume}{sma(delay(volume,1),3)}
      $$

   5. dbxOHLC: 当日单边性
      $$
      DBX_t=\frac{close_t-open_t}{(high_t-low_t)+0.001}
      $$

   6. revOpenVol10d: 过去10日的开盘价与成交量背离指标。出自Alpha101的alpha6
      $$
      Corr_t=-1*correlation(open,volume,10)
      $$

   7. revVwapVol10d: 过去10日的价量背离指标
      $$
      Corr_t=-1*correlation(vwap,volume,10)
      $$

   8. revVVol10d: 过去10日的量幅背离指标
      $$
      Corr_t=-1*correlation(high/low,volume,10)
      $$

   9. gapOpening: 当日开盘缺口指标

   10. volCross_9_12_26: 成交量金叉

   11. hlcBounceNumeric6d: 过去6日反弹强度的走势(numeric)

   12. hlcBounceSigned6d: 过去6日反弹强度的走势(signed)
       ![HLCBOUNCE](imgs/hlcbounce.PNG)

       ​

2. 使用daily cross-sectional数据计算的alphas

   1. 随机排名

      ​

3. 使用Intraday数据计算的daily alphas

   1. 日内收益率偏度

