<div class="post-content">
<p>搭建 V2Ray 看这篇文章就够了！这是最详细的 V2Ray 搭建教程，详细的图文教程确保你可以百分百成功搭建 V2Ray 使用。</p>

<h2 id="前言">前言</h2>

<p>此 V2Ray 教程完完全全是为小白准备的，从购买 VPS 到使用 SSH 登录并使用 V2Ray 一键安装脚本配置 V2Ray</p>

<p>详细的图文教程确保你可以百分百成功搭建 V2Ray 使用，哪怕你是第一次接触这些陌生的东西。</p>

<p>由于 V2Ray 的配置对于小白来说是非常不友好的，</p>

<p>所以此 V2Ray 教程的 V2Ray 服务器端配置将会使用我本人撰写的 <a href="https://github.com/233boy/v2ray/wiki/V2Ray一键安装脚本" target="_blank">V2Ray一键安装脚本</a></p>

<p>这是一个对小白友好的 V2Ray 一键脚本，简化 V2Ray 安装和管理，你还可以快速打开 BBR 来优化 V2Ray</p>

<h2 id="v2ray">V2Ray</h2>

<p>官网：<a href="https://www.v2fly.org/" target="_blank">https://www.v2fly.org/</a></p>

<p><a href="https://www.v2fly.org/" target="_blank">V2Ray(Project V)</a> 相对于 Shadowsocks，V2Ray 更像全能选手，拥有更多可选择的协议 / 传输载体 (Socks、HTTP、TLS、TCP、mKCP、WebSocket )，还有强大的路由功能，不仅仅于此，它亦包含 Shadowsocks 组件，你只需要安装 V2Ray，你就可以使用所有的 V2Ray 相关的特性包括使用 Shadowsocks，由于 V2Ray 是使用 GO 语言所撰写的，天生的平台部署优势，下载即可使用，当然啦，由于 V2Ray 的配置相对来说是很繁琐的，毫无夸张的说</p>

<p>但是有了本人所写的 <a href="https://github.com/233boy/v2ray/wiki/V2Ray一键安装脚本" target="_blank">V2Ray一键安装脚本</a> 加持下，使用 V2Ray 便会显得轻松多了。</p>

<h2 id="流程">流程</h2>

<p>总结一下此文章的大致流程，此 V2Ray 教程可百分百帮助你搭建 V2Ray 使用，哪怕你是第一次接触这些陌生的东西。</p>

<ul>
<li>购买一个 VPS<br />
想要搭建 V2Ray，就必须要拥有一台 VPS。<br /></li>
<li>获取 VPS 信息<br />
我们必须要知道 VPS IP 地址，root 用户密码，SSH 端口<br /></li>
<li>安装 Xshell<br />
Xshell 是一个 SSH 客户端，要登录 VPS，当然需要 SSH 客户端<br /></li>
<li>登录 VPS<br />
使用 Xshell 配置 VPS SSH 信息，然后登录<br /></li>
<li>安装 V2Ray<br />
极速安装，全程自动<br /></li>
<li>V2Ray 安装完成<br />
此时你可以使用客户端配置 V2Ray 使用了<br /></li>
<li>V2Ray 高级玩法<br />
配置 VMess-WS-TLS ， VLESS-gRPC-TLS，动态端口等<br />
<br /></li>
</ul>

<h2 id="购买一个vps">购买一个VPS</h2>

<p>想要搭建 V2Ray， 拥有一个 VPS 是必需的。</p>

<p>我们推荐使用：<a href="https://on.affpass.com/go/bwg" target="_blank">搬瓦工（Bandwagon Host）</a> VPS 来搭建 V2Ray</p>

<p>搬瓦工是一个对中国用户极度友好的 VPS 商家，有香港，CN2 GIA 优化线路，并且支持支付宝付款，当然也是支持退款的！</p>


<h2 id="安装-v2ray">安装 V2Ray</h2>

<p>输入下面命令回车，你可以复制过去，然后在 Xshell 界面按 Shift + Insert 即可粘贴，不能按 Ctrl + V 的。。</p>
<div class="highlight"><pre style="color:#f8f8f2;background-color:#272822;-moz-tab-size:4;-o-tab-size:4;tab-size:4"><code class="language-bash" data-lang="bash">bash &lt;<span style="color:#f92672">(</span>wget -qO- -o- https://git.io/v2ray.sh<span style="color:#f92672">)</span></code></pre></div>
<h2 id="安装完成">安装完成</h2>

<p>当你执行了上面的安装命令，并且没有错误提示的话，那么你就能看到类似下面的图片</p>



<img src="https://vip2.loli.io/2023/05/11/WE8qUsZDgvxTVad.png" alt="V2Ray 脚本安装完成"  loading="lazy" referrerPolicy="no-referrer">


<p>脚本特意弄了一个时间显示，给反馈用来检测安装时间的&hellip;</p>

<p>理论上，绝大多数情况下 15秒内会安装完成</p>

<p>为方便你快速使用，脚本在安装完成后会自动创建一个 VMess-TCP 配置。</p>

<p>此时你可以复制 URL 到相关软件 (例如 v2rayN) 去测试一下是否正常使用。</p>

<p>如果无法正常使用，请尝试使用 <code>v2ray add ss</code> 添加一个 SS 来再测试一下</p>

<h2 id="v2ray-管理面板">V2Ray 管理面板</h2>

<p>现在可以尝试一下输入 <code>v2ray</code> 回车，即可管理 V2Ray</p>



<img src="https://vip2.loli.io/2023/05/11/irKCJBOREU2xdyZ.png" alt="V2Ray 脚本管理面板"  loading="lazy" referrerPolicy="no-referrer">


<p>提示，如果你不想执行任何功能，直接按 Enter 回车退出即可。</p>

<h2 id="无法使用">无法使用</h2>

<p>无法使用一般都是两种情况，一是无法连接上端口，二是客户端内核支持有问题。</p>

<p>如果你的 VPS 有外部防火墙，请确保你已经开放了端口</p>

<p>测试端口是否能连接上：</p>

<p>打开：<a href="https://tcp.ping.pe/" target="_blank">https://tcp.ping.pe/</a></p>

<p>写上你的 VPS IP 跟端口；内容为 ip:端口，示例：<code>1.1.1.1:443</code>，然后点击 <code>Go</code>；或者直接回车</p>

<p>如果显示 successful；证明端口能连接；如果显示 failed；那是无法连接上端口。</p>

<p>提醒，你可以使用 <code>v2ray ip</code> 查看 VPS IP。</p>

<p>关闭防火墙，执行如下命令：</p>

<p><code>systemctl stop firewalld; systemctl disable firewalld; ufw disable</code></p>

<p>关闭防火墙之后再测试一下端口是否通，如果不通，你可能还有外部防火墙没关，<strong>必须要能连接上端口才能正常使用</strong>。</p>

<p>如果能连接上端口，那就继续</p>

<p>使用 <code>v2ray add ss</code> 添加一个 SS 看看能不能正常使用，如果正常使用，证明运行没有问题。</p>

<p>提醒，默认安装的 V2Ray 内核为最新版本</p>

<p>如果无法使用，可能是你客户端的内核太旧</p>

<p>请尝试使用不同的客户端进行测试；比如 v2rayN；v2rayNG 等</p>

<p>请尝试设置 VMessAEAD，某些客户端会有相关选项</p>

<p>某些客户端得把 额外id(alterid) 填写为 0；比如垃圾苹果那边的东西</p>

<p>解决方案一，请尝试将服务器端的内核版本降级</p>

<p>使用 <code>v2ray update core 4.45.2</code> 降级即可</p>

<p>解决方案二，升级客户端内核</p>

<blockquote>
<p>备注，请尽量将客户端内核和服务器端内核保持一致！<strong>内核版本低于 5 可能会出现莫名其妙的问题</strong></p>
</blockquote>

<h2 id="快速入门">快速入门</h2>

<p>本人的 V2Ray 脚本简化了很多流程，例如我们常用的是 (添加、更改、查看、删除) 配置，以下内容让你可以快速掌握使用</p>

<p>添加配置：</p>

<ul>
<li><p><code>v2ray add</code> -&gt; 添加配置</p></li>

<li><p><code>v2ray add ss</code> -&gt; 添加一个 Shadowsocks 配置</p></li>

<li><p><code>v2ray add tcp</code> -&gt; 添加一个 VMess-TCP 配置</p></li>

<li><p><code>v2ray add kcpd</code> -&gt; 添加一个 VMess-mKCP-dynamic-port 动态端口配置</p></li>
</ul>

<p>备注，使用 <code>v2ray add</code> 添加配置的时候，仅 *TLS 相关协议配置必须提供域名，其他均可自动化处理。</p>

<p>如需查看更多 add 参数用法，请查看 V2Ray 脚本说明</p>

<p>&ndash;</p>

<p>更改配置：</p>

<ul>
<li><p><code>v2ray change</code> -&gt; 更改配置</p></li>

<li><p><code>v2ray change tcp</code> -&gt; 更改 TCP 相关配置</p></li>

<li><p><code>v2ray change tcp port auto</code> -&gt; 更改 TCP 相关配置的端口，端口使用自动创建，也可以使用 <code>v2ray port tcp auto</code></p></li>

<li><p><code>v2ray change kcp id auto</code> -&gt; 更改 mKCP 相关配置的 UUID，UUID 使用自动创建，也可以使用 <code>v2ray id tcp auto</code></p></li>
</ul>

<p>如需查看更多 change 参数用法，请查看 V2Ray 脚本说明</p>

<p>&ndash;</p>

<p>查看配置：</p>

<ul>
<li><p><code>v2ray info</code> -&gt; 查看配置</p></li>

<li><p><code>v2ray info tcp</code> -&gt; 查看 TCP 相关配置</p></li>

<li><p><code>v2ray info kcp</code> -&gt; 查看 kcp 相关配置</p></li>
</ul>

<p>&ndash;</p>

<p>删除配置：</p>

<ul>
<li><p><code>v2ray del</code> -&gt; 删除配置</p></li>

<li><p><code>v2ray del kcp</code> -&gt; 删除 KCP 相关配置</p></li>

<li><p><code>v2ray del tcp</code> -&gt; 删除 TCP 相关配置</p></li>
</ul>

<p><strong>提醒，谨慎使用 del 参数</strong></p>

<p>&ndash;</p>

<p>非常棒！你已经掌握最常用的功能 (添加、更改、查看、删除)</p>

<p>add / change / info / del ： 添加、更改、查看、删除</p>

<p>对于绝大多数用户来说</p>

<p>使用 <code>v2ray add</code> 添加配置，使用 <code>v2ray change</code> <code>v2ray info</code> <code>v2ray del</code> 来 (更改、查看、删除) 配置即可。</p>

<blockquote>
<p>提醒，如果只匹配到一个配置时则自动选择该配置，否则将显示匹配到的配置列表，要求选择其中一个配置</p>
</blockquote>

<h2 id="打开-bbr-优化">打开 BBR 优化</h2>

<p>使用：<code>v2ray bbr</code> 便会自动打开 BBR 优化了！非常简单方便</p>

<h2 id="mkcp">mKCP</h2>

<p>mKCP 这个东西其实就是 KCP 协议，反正你知道是能提速的就行，但是不保证都能提速，还能避免 TCP 阻断</p>

<p>使用方法：服务器输入 <code>v2ray add kcp</code> 回车，即可</p>

<p>备注：由于 UDP 的原因也许会被运营商 Qos，这是无解的。</p>

<p>还有就是使用 mKCP 会花费更多流量，请注意！</p>

<h2 id="动态端口">动态端口</h2>

<p>听说使用动态端口可能会对 ISP 封锁端口有点帮助作用。。</p>

<p>使用方法：服务器输入 <code>v2ray add kcpd</code> 回车，即可</p>

<p>也可以使用 <code>v2ray add tcpd</code></p>

<h2 id="vmess-ws-tls">VMess-WS-TLS</h2>

<p>实现 VMess-WS-TLS 超级无敌简单，前提是要拥有一个能正常解析的域名 (并且知道怎么解析域名)</p>

<p>服务器输入 <code>v2ray add ws</code> 回车，输入域名，搞定。</p>

<h2 id="vless-h2-tls">VLESS-H2-TLS</h2>

<p>实现 VLESS-H2-TLS 超级无敌简单，前提是要拥有一个能正常解析的域名 (并且知道怎么解析域名)</p>

<p>服务器输入 <code>v2ray add vh2</code> 回车，输入域名，搞定。</p>

<p>备注，VLESS-H2-TLS 相比 VMess-WS-TLS，在浏览网页时有一些优势，速度是差不多的啦</p>

<h2 id="trojan-grpc-tls">Trojan-gRPC-TLS</h2>

<p>实现 Trojan-gRPC-TLS 超级无敌简单，前提是要拥有一个能正常解析的域名 (并且知道怎么解析域名)</p>

<p>服务器输入 <code>v2ray add tgrpc</code> 回车，输入域名，搞定。</p>

<p>和其他 *TLS 配置的速度差异？有人说快，有人说慢，你自己对比吧</p>

<h2 id="哪个传输协议好">哪个传输协议好？</h2>

<p>心中无杂念，用 TCP</p>

<p>ISP 常作怪，用 动态端口</p>

<p>VPS速度不好，用 mKCP</p>

<p>处子之身，用 *TLS</p>

<h2 id="v2ray-脚本说明">V2Ray 脚本说明</h2>

<p>请看：<a href="https://github.com/233boy/v2ray/wiki/V2Ray一键安装脚本" target="_blank">V2Ray一键安装脚本</a></p>

<p>哎呀，虽然脚本很好用，但是为了你能更加了解掌握各种使用技巧，还是建议看一虾吧！</p>

<h2 id="v2ray-脚本帮助">V2Ray 脚本帮助</h2>

<p>使用：<code>v2ray help</code></p>

<h2 id="反馈问题">反馈问题</h2>

<p>Telegram 群组：<a href="https://t.me/tg233boy" target="_blank">https://t.me/tg233boy</a></p>

<p>Github 反馈：<a href="https://github.com/233boy/v2ray/issues" target="_blank">https://github.com/233boy/v2ray/issues</a></p>

<h2 id="分享">分享</h2>

<p>如果这篇文章对你帮助的话，记得分享给你的小伙伴们哦！</p>

<h2 id="机场备用">机场备用</h2>

<p>为防止自建节点不可用，可考虑购买一个机场作为备用方案，以防止失联</p>

<p>机场推荐： <a href="https://justmysocks.xyz/justmysocks-v2ray/" target="_blank">Just My Socks</a></p>

<p><a href="https://justmysocks.xyz/justmysocks-v2ray/" target="_blank">Just My Socks</a> 是搬瓦工提供的服务，不怕跑路，非国人商家，无须担心 IP 被墙问题。</p>

<p>购买教程：<a href="https://justmysocks.xyz/justmysocks-v2ray/" target="_blank">Just My Socks 购买及使用</a></p>

<h2 id="其他">其他</h2>

<p>请勿违反国家法律法规，否则后果自负！</p>

<p>低调低调低调。</p>

<h2 id="结束">结束</h2>

<p>我有写少了什么吗？我这种小小白萌新看了这教程都觉得很明白了啊。</p>

<p>一次不会，那么就两次，还是不会，那就再来一次。可还是不会啊？大佬请收下我的膝盖。</p>
</div>