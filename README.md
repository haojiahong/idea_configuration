# idea 配置同步

**使用条件**
在开始使用 Settings Repository 之前，请确保 Settings Repository 插件已启用。该插件与IntelliJ IDEA 捆绑在一起，默认情况下处于启用状态。如果该插件未启用，请在 Settings / Preferences Dialog 对话框的 Plugins 页上启用它。

**配置 Settings Repository**
**如果要共享 IDE 设置，请执行以下步骤：**

- 在任何托管服务上创建 Git 存储库，例如 Bitbucket 或 GitHub。
- 在安装了要共享其设置的 IntelliJ IDEA 实例的计算机上，导航到 File | Settings Repository。指定创建的远程仓库的 URL，然后点击 Overwrite Remote。
- 在要应用设置的每台计算机上，在 Settings/Preferences dialog 对话框中，展开 Tools 节点并选择 Settings Repository，指定创建的远程仓库的 URL，然后点击 Overwrite Local。
- 如果想要储存库保留远程设置和本地设置的组合，可以点击 Merge。如果检测到任何冲突，将显示一个对话框，可以在其中解决这些冲突。如果要使用本地设置覆盖远程设置，请单击点击 Overwrite Remote。


每次执行 Update Project 或 Push 操作时，或者当关闭项目或退出 IntelliJ IDEA 时，计算机的本地设置将自动与远程仓库中的设置同步。

在第一次同步时，系统将提示您指定用户名和密码。建议使用 access token 进行 GitHub 身份验证。如果由于某种原因，您想要使用用户名和密码而不是 access token，或者您的 Git 托管服务提供商不支持它，建议您配置 Git credentials helper。

如果要禁用自动设置同步，请导航到 File | Settings | Tools | Settings Repository 并禁用 Auto Sync 选项。您可以通过从主菜单选择 VCS | Sync Settings 来手动更新设置。

