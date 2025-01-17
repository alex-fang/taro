# Taro

[![](https://img.shields.io/node/v/@tarojs/cli.svg?style=flat-square)](https://www.npmjs.com/package/@tarojs/cli)
[![](https://img.shields.io/npm/v/@tarojs/taro.svg?style=flat-square)](https://www.npmjs.com/package/@tarojs/taro)
[![](https://img.shields.io/npm/l/@tarojs/taro.svg?style=flat-square)](https://www.npmjs.com/package/@tarojs/taro)
[![](https://img.shields.io/npm/dt/@tarojs/taro.svg?style=flat-square)](https://www.npmjs.com/package/@tarojs/taro)
[![](https://img.shields.io/travis/NervJS/taro.svg?style=flat-square)](https://travis-ci.org/NervJS/taro)

> 👽 Taro['tɑ:roʊ]，泰罗·奥特曼，宇宙警备队总教官，实力最强的奥特曼。

## 简介

**Taro** 是一套遵循 [React](https://reactjs.org/) 语法规范的 **多端开发** 解决方案。现如今市面上端的形态多种多样，Web、React-Native、微信小程序等各种端大行其道，当业务要求同时在不同的端都要求有所表现的时候，针对不同的端去编写多套代码的成本显然非常高，这时候只编写一套代码就能够适配到多端的能力就显得极为需要。

使用 **Taro**，我们可以只书写一套代码，再通过 **Taro** 的编译工具，将源代码分别编译出可以在不同端（微信/百度/支付宝/字节跳动小程序、H5、React-Native 等）运行的代码。

## 学习资源

[awesome-taro](https://github.com/NervJS/awesome-taro)

掘金小册：[Taro 多端开发实现原理与实战](https://juejin.im/book/5b73a131f265da28065fb1cd?referrer=5ba228f16fb9a05d3251492d)

## 社区共享

[Taro 交流社区——让每一次交流都被沉淀](http://taro-club.jd.com/)

[Taro 物料市场——让每一个轮子产生价值](http://taro-ext.jd.com/)

## 使用案例

Taro 已经投入了我们的生产环境中使用，业界也在广泛地使用 Taro 开发多端应用。

<a href="https://nervjs.github.io/taro-user-cases/"><img src="https://raw.githubusercontent.com/NervJS/taro-user-cases/master/user-cases.jpg" /></a>

[征集更多优秀案例](https://github.com/NervJS/taro/issues/244)

## Taro 特性

#### React 语法风格

Taro 的语法规则基于 React 规范，它采用与 React 一致的组件化思想，组件生命周期与 React 保持一致，同时在书写体验上也尽量与 React 类似，支持使用 JSX 语法，让代码具有更丰富的表现力。

代码示例

```javascript
import Taro, { Component } from '@tarojs/taro'
import { View, Button } from '@tarojs/components'

export default class Index extends Component {
  constructor () {
    super(...arguments)
    this.state = {
      title: '首页',
      list: [1, 2, 3]
    }
  }

  componentWillMount () {}

  componentDidMount () {}

  componentWillUpdate (nextProps, nextState) {}

  componentDidUpdate (prevProps, prevState) {}

  shouldComponentUpdate (nextProps, nextState) {
    return true
  }

  add = (e) => {
    // dosth
  }

  render () {
    return (
      <View className='index'>
        <View className='title'>{this.state.title}</View>
        <View className='content'>
          {this.state.list.map(item => {
            return (
              <View className='item'>{item}</View>
            )
          })}
          <Button className='add' onClick={this.add}>添加</Button>
        </View>
      </View>
    )
  }
}
```

#### 快速开发微信小程序

Taro 立足于微信小程序开发，众所周知小程序的开发体验并不是非常友好，比如小程序中无法使用 npm 来进行第三方库的管理，无法使用一些比较新的 ES 规范等等，针对小程序端的开发弊端，Taro 具有以下的优秀特性：

✅ 支持使用 npm/yarn 安装管理第三方依赖。

✅ 支持使用 ES7/ES8 甚至更加新的 ES 规范，一切都可自行配置。

✅ 支持使用 CSS 预编译器，例如 Sass 等。

✅ 支持使用 Redux 进行状态管理。

✅ 支持使用 Mobx 进行状态管理。

✅ 小程序 API 优化，异步 API Promise 化等等。

#### 支持多端开发转化

Taro 方案的初心就是为了打造一个多端开发的解决方案。目前 Taro 代码可以支持转换到 **微信/百度/支付宝/字节跳动小程序** 、 **H5 端** 以及 **移动端（React-Native）**。

<div align="center"><img src="https://storage.360buyimg.com/taro-resource/platforms.jpg?v=1"/></div>

## 更多功能
如果你还想 Taro 支持新的特性，请使用 [FeatHub](https://feathub.com/NervJS/taro) 进行投票，我们将综合考虑投票结果等因素来确定开发的优先级。

[![Feature Requests](https://cloud.githubusercontent.com/assets/390379/10127973/045b3a96-6560-11e5-9b20-31a2032956b2.png)](http://feathub.com/NervJS/taro)

[![Feature Requests](http://feathub.com/NervJS/taro?format=svg)](http://feathub.com/NervJS/taro)

## 🤝 参与共建 [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

请参考[贡献指南](https://nervjs.github.io/taro/docs/CONTRIBUTING.html).

> 强烈推荐阅读 [《提问的智慧》](https://github.com/ryanhanwu/How-To-Ask-Questions-The-Smart-Way)、[《如何向开源社区提问题》](https://github.com/seajs/seajs/issues/545) 和 [《如何有效地报告 Bug》](http://www.chiark.greenend.org.uk/%7Esgtatham/bugs-cn.html)、[《如何向开源项目提交无法解答的问题》](https://zhuanlan.zhihu.com/p/25795393)，更好的问题更容易获得帮助。

[![Let's fund issues in this repository](https://issuehunt.io/static/embed/issuehunt-button-v1.svg)](https://issuehunt.io/repos/128624453)

## 特别鸣谢

[![nanjingboy](https://avatars1.githubusercontent.com/u/1390888?s=100&v=4)](https://github.com/nanjingboy/) | [![jsNewbee](https://avatars3.githubusercontent.com/u/20449400?s=100&v=4)](https://github.com/js-newbee/)
:---:|:---:
[nanjingboy](https://github.com/nanjingboy/) | [jsNewbee](https://github.com/js-newbee/)

## 贡献者们

<a href="https://github.com/NervJS/taro/graphs/contributors"><img src="https://opencollective.com/taro/contributors.svg?width=890&button=false" /></a>

## 开发计划

[开发计划](./PLANS.md)

## 更新日志

本项目遵从 [Angular Style Commit Message Conventions](https://gist.github.com/stephenparish/9941e89d80e2bc58a153)，更新日志由 `conventional-changelog` 自动生成。完整日志请点击 [CHANGELOG.md](./CHANGELOG.md)。

## 开发交流

[官方交流微信群](https://github.com/NervJS/taro/issues/198)

## License

MIT License

Copyright (c) O2Team

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
22157
24346
23931
18812
2364
24796
19152
7821
18689
3407
22031
29923
502
18875
21601
15899
24771
21062
7231
27983
25794
7726
25680
32470
6598
14523
12379
11047
6898
3059
12367
18809
15282
16091
8601
22867
1717
5011
9607
27685
12296
31494
20331
7571
14453
10158
7526
20211
23340
24917
15649
20801
16926
27917
3115
961
30105
15775
15760
24606
26160
23292
6098
6991
14932
2804
15510
29637
3634
8433
21460
15608
32089
2135
25479
26497
7712
30404
1482
28010
9422
9587
31828
9831
25585
12944
18280
15678
21434
6108
14760
6592
24263
31437
31287
24489
30891
23063
29134
23456
4797
1035
2862
16820
27452
24125
13445
12136
1572
25325
3874
8389
10673
27118
11373
22106
745
23067
19828
22651
5549
21610
20704
16532
27535
20121
30810
4414
23379
217
19005
17595
10611
29228
18384
18971
24193
17463
19001
15603
6162
5418
6037
29763
2040
29024
31432
6044
21587
17983
766
19865
20900
17314
29275
4656
19513
22606
10680
14808
23184
31644
4815
491
9521
25256
11355
24552
9954
511
14605
22284
2530
29397
22768
8503
18476
798
18447
4647
28950
4207
9713
11237
4430
28353
4456
31834
11186
752
13148
9581
16080
9461
31441
22077
5930
2401
25697
24709
1169
27451
5326
1073
23665
22939
8865
10324
21313
4838
149
22424
1797
6737
25862
9718
22482
16275
1766
10364
7217
31788
26368
2181
6616
2170
24337
2161
1660
26027
1937
25706
16727
26576
13639
6347
32558
32051
19501
16828
29909
29852
22945
3621
18474
29796
32102
25714
20422
5956
17179
24751
7943
15350
20808
9175
17452
29400
26508
14839
16879
20399
5761
9691
31682
19465
7064
15887
31357
29568
1271
17002
30340
776
17792
5747
299
22357
19427
29163
17693
9532
23530
7442
25875
