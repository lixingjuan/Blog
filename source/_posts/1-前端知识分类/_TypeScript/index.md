# 函数类型

重载，重载允许一个函数接受不同数量或类型的参数时，做出不同的处理；
举例：输入为数字的时候，输出也应该为数字，输入为字符串的时候，输出也应该为字符串，ts写法：

```js
function reverse(x: number): number;    // 把精准的写在前面
function reverse(x: string): string;    // 把精准的写在前面
function reverse(x: number | string): number | string {
    if (typeof x === 'number') {
        return Number(x.toString().split('').reverse().join(''));
    } else if (typeof x === 'string') {
        return x.split('').reverse().join('');
    }
}
```