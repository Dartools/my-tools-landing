# my-tools-landing
Cloudflare Worker - 落地页 + 可视化后台。

本代码由Gemini编写，一套又有完整可视化后台的落地页。

使用 Cloudflare Worker 和 Workers KV，免费搭建带可视化后台的工具展示以及提示分享网站，无需服务器，

**部署教程：**

在 Cloudflare Worker 中创建 Worker，选择“从hello world开始”

<img width="1862" height="1012" alt="image" src="https://github.com/user-attachments/assets/7c349ec5-8d45-4992-b11f-76c908d17d53" />

给它起个名字（例如 my-tools-landing），点击部署。

部署成功后，点击 编辑代码。

删除 编辑器里默认的所有代码。

粘贴 我上面提供的 worker.js 代码。

保存并部署

**创建 KV 空间**

名字随便取，比如 MY_TOOLS_DB

<img width="1862" height="1012" alt="image" src="https://github.com/user-attachments/assets/66455213-05cd-463f-a46b-b815618004cb" />

再回到 Workers & Pages，绑定到你的 Worker

<img width="1862" height="1012" alt="image" src="https://github.com/user-attachments/assets/e0b052a6-dccd-469f-b71e-1e5112c8b74d" />

添加绑定，选择 KV命名空间

<img width="923" height="813" alt="image" src="https://github.com/user-attachments/assets/feaca6d2-064b-414b-9435-0e7e04afcc6d" />

变量名称必须填 DB , KV命名空间选择刚刚创建的 MY_TOOLS_DB

<img width="716" height="396" alt="image" src="https://github.com/user-attachments/assets/aeb91467-6441-48c0-b322-0d44d7ed0a51" />

**设置后台密码**

在 Workers 和 Pages 设置中，找到【变量和机密】

<img width="1862" height="1012" alt="image" src="https://github.com/user-attachments/assets/3534c927-f012-451d-8de3-8befc49592a8" />

点击【添加】，选择类型【密钥】，变量名称填【ADMIN_PASS】。

值那里自己填一个密码 比如 123456，这个就是后台密码！

<img width="394" height="502" alt="image" src="https://github.com/user-attachments/assets/44a40e6a-a935-46e5-999f-5f1989d9ada7" />

