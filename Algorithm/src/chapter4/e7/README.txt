利用牛顿迭代法求形如 ax^3 + bx^2 + cx + d = 0 方程的根.

提示:
    牛顿迭代法公式为:
        Xn+1 = Xn - f(Xn) / f'(Xn)
    当 Xn 越接近0点时,得到的 Xn+1 也越接近Xn,因此只需判断 |Xn+1 - Xn| 的值即可,当其小于我们需要的精度时,我们就可以说已经找到了解