12. trick
=======================
构造嵌套字典
---------------

::

    >>> from collections import defaultdict
    >>> tree = lambda : defaultdict(tree)
    >>> t = tree()
    >>> t['a']['b'] = 1
    >>> t['c'] = 1
    >>> t['d']['e']['f'] = 10
    >>> t
    defaultdict(<function __main__.<lambda>()>,
                {'a': defaultdict(<function __main__.<lambda>()>, {'b': 1}),
                 'c': 1,
                 'd': defaultdict(<function __main__.<lambda>()>,
                             {'e': defaultdict(<function __main__.<lambda>()>,
                                          {'f': 10})})})

