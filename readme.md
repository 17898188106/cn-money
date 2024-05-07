
## CN-MONEY 插件
> 组件名：``cn-money``，代码块： cnMoney。

cn-money 组件一般封装金额的显示方式，用于金额、价格格式化显示等，可以在转换为人民币大写显示

### 平台差异说明

如无特殊说明，则全平台支持

### 组件使用注意事项

为了避免错误使用，给大家带来不好的开发体验，请在使用组件前仔细阅读下面的注意事项，可以帮你避免一些必要的错误使用。

- 组件内部没有依赖其它组件
- 在 `HBuilderX` 低版本中，可能会出现组件显示不正常的问题，请升级最新的 `HBuilderX` 或者 `cli`
- 如使用过程中有任何问题，或者您对uni-ui有一些好的建议，联系 gxyxd@qq.com

### 基本用法 

```html
<!-- 默认显示 -->
<cn-money :money="52013.14"></cn-money>

<!-- 加大主字体 -->
<cn-money :money="9168.45" :size="48"></cn-money>

<!-- 改变颜色 -->
<cn-money :money="4168.25" :size="38" color="#9397a4"></cn-money>

<!-- 删除线 -->
<cn-money :money="7168.39" color="#9397a4" original></cn-money>

<!-- 千分位 -->
<cn-money :money="16852013.14" thousandth></cn-money>
			 
<!-- 人民币大写 -->
<cn-money :money="502.00" rmb></cn-money>

```

```javascript
import cnMoney from '@/components/cn-money/cn-money.vue';

export default {
	components: {
		cnMoney
	},
	data() {
		return {}
	}
}

```

### cn-money 属性说明

**cnMoney 属性说明：**

属性名			|类型		|默认值		|	说明																					
---				|----		|---		|	---	
money			|Number		|0			|	显示的金额
padding			|String		|0			|	内边框
margin  		|Number		|0			|	外边框
size			|Number		|28			|	主文字大小，单位rpx
color  			|String 	|#e41f19 	|	字体颜色
unit			|String		|¥			|	金额单位	
showUnit		|Boolean	|true		|	是否显示金额单位
unitPosition	|String		|left		|	单位显示位置，left或right，只有showUnit为true时有效，right的时候¥自动转为元
showZeroDecimal	|Boolean	|true		|	金额小数为零时是否显示
thousandth		|Boolean	|false		|	是否显示千分位
original		|Boolean	|false		|	是否显示删除线	
rmb	 			|Boolean	|false		|	是否转换为人民币大写

**cn-money 事件说明：**

事件称名			|	说明						|	返回参数			
---				|	---						|	---	


### 插件预览地址

[麦诗生活商城](https://spxg.cdwzit.com/jd/index.html)
