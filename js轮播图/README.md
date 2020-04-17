## 注意：  
1. 在用addEventListener的时候要注意，通过getElementByClassName或者ById的方式获取的元素不是单个元素，而是nodeLIst，
所以要通过数组索引方式正确拿取要添加事件侦听的元素