1. 集中化版本控制系统（Centralized Version Control Systems，简称 CVCS）

   1. 缺陷：单点故障

2. 分布式版本控制系统（Distributed Version Control System，简称 DVCS）

   每一次的克隆操作都是对代码仓库的完整备份。

3. git和其他版本控制系统的主要差别是在于Git对待数据的方式。

   1. 从概念上说，其他大部分系统以文件变更列表的方式储存信息，它们储存的信息看作是一组基本文件和每个文件随时间逐步积累的差异（通常称作基于差异（delta-based）的版本控制）
   2. Git更像是吧数据看作小型文件系统的一系列快照。在Git中，每当你提交更新或保存项目状态时，他对当时的全部文件创建一个快照并保存这个快照的索引。如果文件没有修改，Git不再重新储存文件，而只是保留要给链接指向之前存储的文件。

4. 近乎所有操作都在本地执行

5. Git保证完整性

   1. Git所有的数据再储存前都计算校验和，然后用以校验和引用(SHA-1）。

6. Git一般只添加数据。

   1. 三种状态：已提交（committed）、已修改（modified）和已暂存（staged）
   2. Git项目拥有三个阶段：工作区、暂存区和Git目录。

7. 命令行：只有在命令行模式下才能执行Git的所有命令。

   1. ```powershell
      git config --list --show-origin
      ```

      查看所有配置及所在文件。

   2. ```powershell
      $ git config --list
      user.name=John Doe
      user.email=johndoe@example.com
      color.status=auto
      color.branch=auto
      color.interactive=auto
      color.diff=auto
      
      ```

      列出Git当时能找的配置

   3. ```powershell
      $ git config user.name
      John Doe
      ```

      使用git config <key> 来检查某一项配置

