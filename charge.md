{{indexmenu_n>3}}

# 计费说明

罗马计费包括以下部分：

## 接入费用

私有网络接入罗马时，系统会创建接入点，接入费用即为接入点的费用（UCloud侧无接入费用）。

  - 计费方式: 按年、按月。
  - 付费方式: 按年、按月（均为预付费）。
  - 计费公式: 接入费用 = 接入时长 \* 接入单价。

## 网络费用

即接入罗马的私有网络间各互通链路的网络使用费用。

  - 计费方式: **按月峰值**，**按日峰值**（暂未开放）（为后付费）。
  - 付费方式: **月结**（对应按月峰值），**日结**（对应按日峰值）。
  - 说明:



``` 
  -**保底带宽**
      * 保底带宽为最低消费带宽。
      * 计算公式: 保底带宽 = 保底百分比 * 互通链路最大带宽（四舍五入，且不小于1M）。
      * 保底百分比: 20%。
  -**按月峰值**（带宽）
      * 账单周期: 月，当月的账单将在次月月初出具并扣费。
      * 计费公式: 费用 =（保底带宽 * 互通链路带宽价格 * 链路存在天数占当月天数的百分比）+（月峰值带宽 * 互通链路带宽价格 * 链路存在天数占当月天数的百分比）。
      * 使用时长: 至少使用一天。
      * 月峰值带宽: 以 **5 分钟为粒度采样**，采集链路**双向流量**，计算双向在 5 分钟内的最大带宽，取**入方向和出方向**中**较大的带宽**作为采样点带宽值。次月月初将所有的采样点按峰值从高到低排序，取最高峰点带宽，**月峰值带宽=最高峰点带宽-保底带宽**，月峰值带宽不小于0。
  -**按日峰值**（带宽）（暂未开放）
      * 账单周期: 天，当天的账单将在次日出具并扣费。
      * 计费公式: 费用 = （保底带宽 * 互通链路带宽价格 * 1） +（日峰值带宽 * 互通链路带宽价格 * 1），其中1为链路存在天数。
      * 使用时长: 至少使用一天。
      * 日峰值带宽: 以 **1 分钟为粒度采样**，采集链路**双向流量**，计算双向在 1 分钟内的最大带宽，取**入方向和出方向**中**较大的带宽**作为采样点带宽值。得到全天所有采样点后，按从高到低排序，取最高峰点带宽，**日峰值带宽=最高峰点带宽-保底带宽**，日峰值带宽不小于0。
```