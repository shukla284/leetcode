上上周面了uber的onsite， 毫无算法，跪了。。发一下面经为之后的面试攒攒人品。

最开始网投，recruiter联系了我让我做一下coding challenge。我看了一下给的一些题目，觉得挺麻烦的就走了另外一个选项，给他们发了一个我以前写过的代码。没想到随便发的一个C写的web proxy代码竟然过了于是约电面。

电面

电面是一个美国小哥，开始聊了聊简历之后给了一道系统设计题，设计一个Service可以输入用户location查询附近的公交站台和所有即将到这些站台的公交车。我随便和他扯了一些系统设计的还有优化算法之类的东西，后来让我写一个控制访问API频率（Ratelimit）的function， 用了一个Queue写完就结束了。

之后没多久recruiter联系我让我去onsite，给了200 uber credit， 但是只限路线起点或目的地时uber公司才可以用（太抠门）。

Onsite 

到公司recruiter带我到了uber拐角的一个小会议室就开始面试了，Uber公司看起来还是很不错的。四轮面试：

第一个人 ： 让我设计一个 Netflix， follow up 很多 比如如何限制同一个用户多处登录不能同时看一个资源，如何实现根据用户的网速调整清晰度，怎么热门推荐等等。

第二个人 ： 进来直接不闲聊直接让我打开自己电脑开始写一些代码，设计一个 Excel ， 每个cell里面是一个String。 一开始想当然说可以直接用二维矩阵存，后来改成list of lists， 最后改成了HashMap。后续还有evaluate一个string相关的问题（给了黑盒evaluate函数，对每个cell实现evaluate和支持修改）。

第三个人 ： 纯聊简历，干聊project，面试官没有准备一道题，到最后我就已经是在找话说了。

第四个人 ： 好像是个小领导，先问了问我有没有问题，后来问了一些知识点问题，python有哪些语言特性等等之类的。

最后recruiter总结问我觉得怎么样，我说觉得很好我很喜欢uber，问我如果给我offer我能不能很快接受，I said yes。





有人问九章君，怎么今天又发Uber的面经？其实是九章君最近真的看到很多人都在发Uber面经，也听说最近U家发offer发得比较疯狂，觉得U家今年的招聘力度应该不小。所以特意再发一次U家面经，提醒大家明年开春了赶紧试着投投看。
另外，九章君有一个友情提醒，U家的最后一面往往是约一个manager聊天，有的童鞋觉得应该已经过了，只是聊聊天认识一下，结果聊着聊着就聊挂了。九章君提醒大家面Uber的时候，最后的manager聊天，一定好好准备一下，否则挂了都不知道挂在哪fr。
电面
sudoku solver。

Onsite 1
1.1 anagrams，秒了。

1.2 input String

123@gmail.com...we23--898##job@uber.com^^^2134nn..uber@hello.edu.cn
output 返回所有合理的address。java写到后来没写完，但是思路被认可。

Onsite 2
input(String[] str1, String[] str2) 返回match str2里任一个的所有str1中的元素（白板）。
比如说str2是“hiw”，“abc”； str1是“hiw2”，“3hiw”， “def”，“abc1”，应该返回“hiw2”，“3hiw”，“abc1”。这题交流不顺畅，写出来一种方法，他看半天不懂，解释了半天，他似懂非懂，又说我的方法不efficient，最后我似乎明白他要考啥，我说了一个treemap来解决的办法，他说ok，没时间再写code了，也不知道是不是真的ok。

Onsite 3
聊messaging system，聊背景。考了个algorithm题。一个array，返回一个最短subarray，其sum是target。
我说brutal force可解，但time O（n^2），应该还有更好的方法，憋了好久没办法，后来给了提示才想到，用个hashMap，把从第一个元素开始，任一元素解释的sum hash了，<sum, 截至index>，再从第一个开始累积accu_sum，看有没有accu_sum + target在hashtable的。 于是写了code，被告知ok。

Onsite 4
manager聊天，聊背景，聊知识。