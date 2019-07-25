{{indexmenu_n>5}}

# VPC（UCloud）撤消接入

## 步骤一、私有网络撤消接入

:\!:**<span class="underline">此步骤需在 UCloud 控制台操作</span>**

从 UCloud 控制台进入“**罗马**” \>
"**接入管理**"，将鼠标移入已接入的私有网络的**右上角**，会显示“**撤消接入**”，点击“**撤消接入**”。

![](/images/operation/私有网络撤消接入.png)

注：也可在私有网络详情的“**概览页面**”中点击“**撤消接入**”按钮。

## 步骤二、手动删除路由条目

:\!:**<span class="underline">此步骤需在阿里云平台操作</span>**

若没有**手动接入**到罗马的阿里云 VPC，则不需要此步操作。

若已有**手动接入**到罗马的阿里云 VPC，则需要在阿里云平台对这些 VPC 的路由表的路由条目进行手动删除（仅删除这些 VPC
的路由表中对应于步骤一撤消接入的 VPC 的子网网段的路由条目）
[前往阿里云VPC管理页面](https://vpc.console.aliyun.com/vpc)

![](/images/operation/删除路由规则.png)

**注：由于手动接入阿里云 VPC 到罗马时，操作较为繁琐，且对其他 VPC 的接入及撤消流程都制造了额外的操作步骤，因此，接入阿里云 VPC
到罗马时，强烈建议使用 [](/network/roma/operation/ali_auto_access)**