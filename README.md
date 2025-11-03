
# Academic Pages

![pages-build-deployment](https://github.com/academicpages/academicpages.github.io/actions/workflows/pages/pages-build-deployment/badge.svg)

Academic Pages is a Github Pages template for academic websites.


# Getting Started

1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Click the "Use this template" button in the top right.
1. On the "New repository" page, enter your repository name as "[your GitHub username].github.io", which will also be your website's URL.
1. Set site-wide configuration and add your content.
1. Upload any files (like PDFs, .zip files, etc.) to the `files/` directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.  
1. Check status by going to the repository settings, in the "GitHub pages" section
1. (Optional) Use the Jupyter notebooks or python scripts in the `markdown_generator` folder to generate markdown files for publications and talks from a TSV file.

See more info at https://academicpages.github.io/

## Running Locally

When you are initially working your website, it is very useful to be able to preview the changes locally before pushing them to GitHub. To work locally you will need to:

### For ubuntu

1. Clone the repository and made updates as detailed above.
1. Make sure you have ruby-dev, bundler, and nodejs installed: `sudo apt install ruby-dev ruby-bundler nodejs`
1. Run `bundle install` to install ruby dependencies. If you get errors, delete Gemfile.lock and try again.
1. Run `jekyll serve -l -H localhost` to generate the HTML and serve it from `localhost:4000` the local server will automatically rebuild and refresh the pages on change.

### For windows

#### 1.克隆仓库到本地
   >git clone https://github.com/qingkaiyang/qingkaiyang.github.io.git
#### 2.安装Ruby
1. 前往官网下载安装Ruby：`https://rubyinstaller.org/downloads/` （选择with Devkit目录下`3.3.x+`版本下载，安装过程无需额外勾选，按照默认勾选即可）
2. 在以管理员身份运行`Start Command Prompt with Ruby`时，注意选择` 3 - MSYS2 and MINGW development toolchain`,如果不小心选择错误，输入`ridk install`打开安装菜单
3. 安装完成后，在 PowerShell 中检查：
   >ruby -v
   >gem -v

   **输出版本号即已完成安装**
#### 3.安装 Bundler
在 PowerShell 中运行：
   >gem install bundler
#### 4.安装 Node.js
1. 前往`https://nodejs.org/en/download`，下载`Windows Installer(.msi)`
2. 高级系统设置->系统变量->将nodejs目录添加到path中
3. 安装完成后，在 PowerShell 中检查：
   >node -v
    npm -v

    **输出版本号即已完成安装**
>Tips:
>如果遇到下述情况：node -v输出版本，npm -v出现下述报错：
>>npm : 无法加载文件 C:\Program Files\nodejs\npm.ps1。未对文件 C:\Program Files\nodejs\npm.ps1 进行数字签名。无法在当前系 统上运行该脚本。有关运行脚本和设置执行策略的详细信息，请参阅 https:/go.microsoft.com/fwlink/?LinkID=135170 中的 about_E xecution_Policies。
>
>解决方案：
>1. 以**管理员身份**打开 PowerShell，输入`Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned`
>2. 再次执行`npm -v`

1. Run `bundle install` to install ruby dependencies. If you get errors, delete Gemfile.lock and try again.
2. Run `jekyll serve -l -H localhost` to generate the HTML and serve it from `localhost:4000` the local server will automatically rebuild and refresh the pages on change.
#### 5.运行项目
1. 打开项目目录PowerShell,输入`bundle install`（*后缀* --verbose可看详细日志，判断是否卡顿）
2. 编译成功后，启动本地预览服务器,输入：
   >bundle exec jekyll serve -l -H localhost



# Maintenance 

Bug reports and feature requests to the template  should be [submitted via GitHub](https://github.com/academicpages/academicpages.github.io/issues/new/choose). For questions concerning how to style the template, please feel free to start a [new discussion on GitHub](https://github.com/academicpages/academicpages.github.io/discussions).

This repository was forked (then detached) by [Stuart Geiger](https://github.com/staeiou) from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/), which is 漏 2016 Michael Rose and released under the MIT License (see LICENSE.md). It is currently being maintained by [Robert Zupko](https://github.com/rjzupkoii) and additional maintainers would be welcomed.

## Bugfixes and enhancements

If you have bugfixes and enhancements that you would like to submit as a pull request, you will need to [fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo) this repository as opposed to using it as a template. This will also allow you to [synchronize your copy](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork) of template to your fork as well.

Unfortunately, one logistical issue with a template theme like Academic Pages that makes it a little tricky to get bug fixes and updates to the core theme. If you use this template and customize it, you will probably get merge conflicts if you attempt to synchronize. If you want to save your various .yml configuration files and markdown files, you can delete the repository and fork it again. Or you can manually patch.
