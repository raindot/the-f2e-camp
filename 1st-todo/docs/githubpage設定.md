## 需要注意的坑

1. 在npm run build之前要將config/index.js裡邊build配置裡邊的assetsPublicPath: '/'改成assetsPublicPath: './'

2. 將webpack.prod.conf.js 中的removeAttributeQuotes 改為false
