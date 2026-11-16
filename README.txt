Speedy10 免费网页 App（PWA）
================================

文件：
- index.html：应用本体
- manifest.webmanifest：手机安装信息
- sw.js：离线缓存
- README.txt：部署说明

免费部署（GitHub Pages）：
1. 在 GitHub 新建公开仓库，例如 speedy10-app。
2. 将本 ZIP 解压，把上述三个网页文件上传到仓库根目录（README.txt 可一起上传）。
3. 仓库 Settings → Pages → Build and deployment：
   Source 选择 Deploy from a branch；
   Branch 选择 main，文件夹选择 /(root)，保存。
4. 等待部署完成，打开 https://你的GitHub用户名.github.io/speedy10-app/
5. Android Chrome 打开网址，右上角 ⋮ → 添加到主屏幕/安装应用。

数据读取：
应用会尝试通过公开文本读取代理获取 speedylot88.com 的开奖记录。代理或来源网站可能临时限制访问。
若自动读取失败：打开开奖网页，复制期号及十个号码，回到 App 的“手动导入开奖记录”，按每行
期号,第一名,第二名,第三名,第四名,第五名,第六名,第七名,第八名,第九名,第十名
格式粘贴并导入。

预测和核对：
- 每期只推荐一个 1–10 的号码。
- 只统计每期前三名；综合近期频率、遗漏、短期走势计算参考分。
- 预测基准期之后出现的新一期开奖时，自动检查该号码是否出现在前三名。
- 命中、未中、累计命中率保存在当前浏览器本地（localStorage）。清除浏览器数据会丢失统计。
- 预测是历史统计参考，不保证结果；开奖具有随机性，请理性使用。

注意：
本项目是静态网页，不需要 Replit 订阅、服务器或付费 API。跨域读取由公开代理协助，不能保证长期可用。
