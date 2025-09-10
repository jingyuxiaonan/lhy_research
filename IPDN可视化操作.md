### IPDN可视化操作

- **进入服务器**，到`/media/cmy/Projects/lhy_work/IPDN`路径下
- **启动环境**`conda activate lhy_ipdn`
- **生成ply文件：**根据`pre_results`下拥有的文件来决定创建哪个模型【目前有best（原论文的best模型）和我跑出来的ifa模型 】哪个数据集（scanrefer/multi3drefer）的可视化结果
  - 如果是scanrefer，则使用`visualize_scan.py`创建，直接运行即可
  - 如果是multi3drefer，则使用`visualize_multi.py`创建，直接运行即可
  - 注意，以上俩文件都可以根据`NAMES_TO_PROCESS`参数决定创建哪些模型的结果
- **生成html文件：**在`visualizations`中有了对应结果文件后用`python compare_visuals.py --scan_dir /media/cmy/Projects/lhy_work/IPDN/data/scannetv2/val`命令执行【我当前只针对scan数据集搞了生成html的文件，multi后续会有的，先搞scan】
- **可视化查看：**终端执行`python3 -m http.server 8000`，然后选择在**本地**【用`http://localhost:8000/visuals_results/`网址进去】或者服务器上【下图的**在编辑器中预览**】查看，然后就是挑好的结果咯，就是我们准确预测但是best没有预测对的，或者俩都没预测对，但我们的相对更和文本相关

![image-20250910095910559](/Users/lihaiyang/Library/Application Support/typora-user-images/image-20250910095910559.png)

