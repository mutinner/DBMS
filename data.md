### 数据结构
* 数据元素是数据的基本单位
* 一个数据元素由若干个数据项组成
* 数据项是数据的最小单位
* 数据对象是性质相同的数据元素的集合，数据的一个子集
* 逻辑结构
    - 集合
    - 线性结构
    - 树形结构
    - 网状结构
* 逻辑结构的另一种
    - 线性结构和非线性结构
* 物理结构
    - 顺序存储结构(顺序映像)
    - 链式存储结构(非顺序映像)
* 算法特性
    - 有穷性
    - 确定性
    - 可行性
    - 输入输出

* [树、二叉树、森林之间的转换](https://www.cnblogs.com/zhuyf87/archive/2012/11/04/2753950.html)

* 排序

    <table style="text-align: center;">
        <tr style="text-align: center;">
            <td rowspan="2">排序方法</td>
            <td rowspan="2">平均时间</td>
            <td colspan="2">比较次数</td>
            <td colspan="2">移动次数</td>
            <td rowspan="2">稳定性</td>
            <td rowspan="2">附加存储</td>
        </tr>
        <tr>
            <td>最好</td>
            <td>最差</td>
            <td>最好</td>
            <td>最差</td>
        </tr>
        <tr>
            <td>直接插入</td>
            <td>n<sup>2</sup></td>
            <td>n</td>
            <td>n<sup>2</sup></td>
            <td>0</td>
            <td>n<sup>2</sup></td>
            <td>T</td>
            <td>1</td>
        </tr>
        <tr>
            <td>折半插入</td>
            <td>n<sup>2</sup></td>
            <td colspan="2">nlog<sub>2</sub>n</td>
            <td>0</td>
            <td>n<sup>2</sup></td>
            <td>T</td>
            <td>1</td>
        </tr>
        <tr>
            <td>希尔排序</td>
            <td>n<sup>1.3</sup></td>
            <td colspan="2"></td>
            <td>0</td>
            <td></td>
            <td>F</td>
            <td>1</td>
        </tr>
        <tr>
            <td>起泡排序</td>
            <td>n<sup>2</sup></td>
            <td>n</td>
            <td>n<sup>2</sup></td>
            <td>0</td>
            <td>n<sup>2</sup></td>
            <td>T</td>
            <td>1</td>
        </tr>
        <tr>
            <td>快速排序</td>
            <td>nlog<sub>2</sub>n</td>
            <td>nlog<sub>2</sub>n</td>
            <td>n<sup>2</sup></td>
            <td>nlog<sub>2</sub>n</td>
            <td>n<sup>2</sup></td>
            <td>F</td>
            <td>nlog<sub>2</sub>n</td>
        </tr>
        <tr>
            <td>简单选择</td>
            <td>n<sup>2</sup></td>
            <td colspan="2">n<sup>2</sup></td>
            <td>0</td>
            <td>n</td>
            <td>T</td>
            <td>1</td>
        </tr>
        <tr>
            <td>堆排序</td>
            <td>nlog<sub>2</sub>n</td>
            <td colspan="2">nlog<sub>2</sub>n</td>
            <td colspan="2">nlog<sub>2</sub>n</td>
            <td>F</td>
            <td>1</td>
        </tr>
        <tr>
            <td>归并排序</td>
            <td>nlog<sub>2</sub>n</td>
            <td colspan="2">nlog<sub>2</sub>n</td>
            <td colspan="2">nlog<sub>2</sub>n</td>
            <td>T</td>
            <td>n</td>
        </tr>
        <tr>
            <td>基数排序</td>
            <td>d(n+rd)</td>
            <td colspan="4"></td>
            <td>T</td>
            <td>n+rd</td>
        </tr>
    </table>