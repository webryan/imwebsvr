# IMWeb Svr

## Stack
1. `hapi` , basic framework
2. `q-template`, template engine
3. `inner plugin`, from tsw

## todo
- 文件目录规则
- 基本的plugin适配
- L5,上报支持
- course list 支持
- src 构建统一

## 目录分布的原因
`src` : 主要考虑到我们是基于同构设计整站体系，故我们的静态源码应该是会出现在项目目录中的，所有有src目录。但是src目录不会发布到服务器。

`views`: 由于 `src`的存在这个目录也就比较特殊了，因为可能是从src构建出来的，所以 `src`, `public`,`views` 放到同级目录。 

`public`: 通过 `src`构建出来的纯前端文件，应该发到CDN，此处可以用作失败切换逻辑。

`server`: 这个才是真个project的主要内容

> `server/route` : route目录,这个再考虑下，是目录方式还是文件方式
