### Design questions in interview

- 评分标准

  | 考察点   |                | 占比 |
  | -------- | -------------- | ---- |
  | 可行性   | Work Solution  | 25%  |
  | 特定问题 | Special Case   | 20%  |
  | 分析能力 | Analysis       | 25%  |
  | 权衡     | Tradeoff       | 15%  |
  | 知识储备 | Knowledge base | 15%  |

- 4S 分析法
  - Scenario 场景
  - Service 服务
  - Storage 存储
    - DB
      - Relational DB(SQL db)
      - None-relatonal DB(NoSQL)
      - Partition
    - Cache
    - 文件系统
  - Scale 扩展

### Examples

- 设计一个 DNS 的 Cache 结构，要求能够满足每秒 5000 次以上的查询，满足 IP 数据的快速插入，查询的速度要快（题目还给出了一系列的数据，例如站点数总共为 5000 万、IP 地址有 1000 万等）。
- 有 N 台计算机，M 个文件，文件可以以任意方式存放到任意计算机上，文件可任意分割成若干块。假设这 N 台计算机的宕机率小于 1/3，想在宕机时可以从其他未宕机的计算机中完整导出这 M 个文件，求最好的存放与分割策略。
- 假设有 30 台服务器，每台服务器上面都存有上百亿条数据（有可能重复），如何找出这 30 台机器中，根据某关键字，重复出现次数最多的前 100 条？要求使用 Hadoop 来实现。
- 设计一个系统，要求写速度尽可能快，并说明设计原理。
- 设计一个高并发系统，说明架构和关键技术要点。
- 有 25TB 的日志（query-&gt;queryinfo），大小在不断增长，设计一个方案，给出一个 query 能快速返回 queryinfo。