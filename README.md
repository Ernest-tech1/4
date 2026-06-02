def max_dragon_power(n):
    if n == 1:
        return 1
    q, r = divmod(n, 3)
    if r == 0:
        return 3 ** q
    elif r == 1:
        return (3 ** (q - 1)) * 4  # 4 = 2 * 2
    else:  # r == 2
        return (3 ** q) * 2
