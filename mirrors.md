# Mirrors for Chinese Developers


<style>

    .code-block {
        background-color: #f7f7f7;
        border: 1px solid #ddd;
        border-radius: 4px;
        padding: 10px;
        font-family: Consolas, Monaco, 'Andale Mono', monospace;
        font-size: 14px;
        line-height: 1.5;
        white-space: pre-wrap;
        overflow-x: auto;
    }
</style>


## Programming Languages

### Python

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

<selector :options="mirrors['python']" v-model="urls['python']">
</selector>

<div class="code-block">
# once
> pip3 install some-package -i {{urls["python"]}}
> pip3 config set global.index-url {{urls["python"]}}
> pip3 config get global.index-url
{{urls["python"]}}
</div>

---

### Go

![Go](https://img.shields.io/badge/go-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white)

<selector :options="mirrors['go']" v-model="urls['go']">
</selector>


<div class="code-block">
> go env -w GOPROXY={{urls["go"]}},direct
</div>

---


### Java

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)

---


### Node.js

![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)

<selector :options="mirrors['npm']" v-model="urls['npm']">
</selector>


![NPM](https://img.shields.io/badge/NPM-%23CB3837.svg?style=for-the-badge&logo=npm&logoColor=white)

<div class="code-block">
# use mirror once
> npm install -g yarn --registry={{urls["npm"]}}
# set mirror
> npm config set registry {{urls["npm"]}}
# verify mirror
> npm config get registry
{{urls["npm"]}}
</div>

---

![Yarn](https://img.shields.io/badge/yarn-%232C8EBB.svg?style=for-the-badge&logo=yarn&logoColor=white)

<div class="code-block">
> yarn config set registry {{urls["npm"]}} -g
> yarn config get registry
{{urls["npm"]}}
</div>

---


## Operating Systems

### Ubuntu 

![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)

[Tsinghua](https://mirrors.tuna.tsinghua.edu.cn/help/ubuntu/)

---

### Alpine 

![Alpine Linux](https://img.shields.io/badge/Alpine_Linux-%230D597F.svg?style=for-the-badge&logo=alpine-linux&logoColor=white)

<selector :options="mirrors['alpine']" v-model="urls['alpine']">
</selector>

<div class="code-block">
> sed -i 's/dl-cdn.alpinelinux.org/{{urls["alpine"]}}/g' /etc/apk/repositories
</div>

---
