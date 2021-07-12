npm i在运行命令的目录中下载指定的包到node_modules
npm i -S等同于npm i --save, 在运行命令的目录中下载指定的包到node_modules, 如果package.json存在的话, 同时写入到package.json的dependencies字段
npm i -D等同于npm i --save-dev, 在运行命令的目录中下载指定的包到node_modules, 如果package.json存在的话, 同时写入到package.json的devDependencies字段