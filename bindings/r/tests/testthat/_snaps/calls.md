# subset

    Code
      node_children_print(node)
    Output
      S-Expression
      (subset [(1, 0), (1, 8)]
        function: (identifier [(1, 0), (1, 3)])
        arguments: (arguments [(1, 3), (1, 8)]
          open: "[" [(1, 3), (1, 4)]
          argument: (argument [(1, 4), (1, 7)]
            value: (identifier [(1, 4), (1, 7)])
          )
          close: "]" [(1, 7), (1, 8)]
        )
      )
      
      Text
      foo[bar]
      
      S-Expression
      (subset [(2, 0), (2, 9)]
        function: (identifier [(2, 0), (2, 3)])
        arguments: (arguments [(2, 3), (2, 9)]
          open: "[" [(2, 3), (2, 4)]
          argument: (argument [(2, 4), (2, 5)]
            value: (float [(2, 4), (2, 5)])
          )
          (comma [(2, 5), (2, 6)])
          argument: (argument [(2, 7), (2, 8)]
            value: (float [(2, 7), (2, 8)])
          )
          close: "]" [(2, 8), (2, 9)]
        )
      )
      
      Text
      foo[1, 2]
      
      S-Expression
      (subset [(3, 0), (3, 8)]
        function: (identifier [(3, 0), (3, 3)])
        arguments: (arguments [(3, 3), (3, 8)]
          open: "[" [(3, 3), (3, 4)]
          argument: (argument [(3, 4), (3, 5)]
            value: (float [(3, 4), (3, 5)])
          )
          (comma [(3, 5), (3, 6)])
          close: "]" [(3, 7), (3, 8)]
        )
      )
      
      Text
      foo[1, ]
      
      S-Expression
      (subset [(4, 0), (4, 9)]
        function: (identifier [(4, 0), (4, 3)])
        arguments: (arguments [(4, 3), (4, 9)]
          open: "[" [(4, 3), (4, 4)]
          argument: (argument [(4, 4), (4, 5)]
            value: (float [(4, 4), (4, 5)])
          )
          (comma [(4, 5), (4, 6)])
          (comma [(4, 6), (4, 7)])
          close: "]" [(4, 8), (4, 9)]
        )
      )
      
      Text
      foo[1,, ]
      
      S-Expression
      (subset [(5, 0), (5, 9)]
        function: (identifier [(5, 0), (5, 3)])
        arguments: (arguments [(5, 3), (5, 9)]
          open: "[" [(5, 3), (5, 4)]
          argument: (argument [(5, 4), (5, 5)]
            value: (float [(5, 4), (5, 5)])
          )
          (comma [(5, 5), (5, 6)])
          (comma [(5, 6), (5, 7)])
          argument: (argument [(5, 7), (5, 8)]
            value: (float [(5, 7), (5, 8)])
          )
          close: "]" [(5, 8), (5, 9)]
        )
      )
      
      Text
      foo[1,,2]
      
      S-Expression
      (subset [(6, 0), (6, 15)]
        function: (identifier [(6, 0), (6, 3)])
        arguments: (arguments [(6, 3), (6, 15)]
          open: "[" [(6, 3), (6, 4)]
          argument: (argument [(6, 4), (6, 7)]
            name: (identifier [(6, 4), (6, 5)])
            "=" [(6, 5), (6, 6)]
            value: (float [(6, 6), (6, 7)])
          )
          (comma [(6, 7), (6, 8)])
          (comma [(6, 8), (6, 9)])
          argument: (argument [(6, 9), (6, 12)]
            name: (identifier [(6, 9), (6, 10)])
            "=" [(6, 10), (6, 11)]
            value: (float [(6, 11), (6, 12)])
          )
          (comma [(6, 12), (6, 13)])
          argument: (argument [(6, 13), (6, 14)]
            value: (float [(6, 13), (6, 14)])
          )
          close: "]" [(6, 14), (6, 15)]
        )
      )
      
      Text
      foo[x=1,,y=3,4]
      
      S-Expression
      (subset [(7, 0), (7, 5)]
        function: (identifier [(7, 0), (7, 3)])
        arguments: (arguments [(7, 3), (7, 5)]
          open: "[" [(7, 3), (7, 4)]
          close: "]" [(7, 4), (7, 5)]
        )
      )
      
      Text
      foo[]
      

# subset2

    Code
      node_children_print(node)
    Output
      S-Expression
      (subset2 [(1, 0), (1, 8)]
        function: (identifier [(1, 0), (1, 3)])
        arguments: (arguments [(1, 3), (1, 8)]
          open: "[[" [(1, 3), (1, 5)]
          argument: (argument [(1, 5), (1, 6)]
            value: (identifier [(1, 5), (1, 6)])
          )
          close: "]]" [(1, 6), (1, 8)]
        )
      )
      
      Text
      foo[[x]]
      
      S-Expression
      (subset2 [(2, 0), (2, 11)]
        function: (identifier [(2, 0), (2, 3)])
        arguments: (arguments [(2, 3), (2, 11)]
          open: "[[" [(2, 3), (2, 5)]
          argument: (argument [(2, 5), (2, 6)]
            value: (identifier [(2, 5), (2, 6)])
          )
          (comma [(2, 6), (2, 7)])
          argument: (argument [(2, 8), (2, 9)]
            value: (identifier [(2, 8), (2, 9)])
          )
          close: "]]" [(2, 9), (2, 11)]
        )
      )
      
      Text
      foo[[x, y]]
      
      S-Expression
      (subset2 [(3, 0), (3, 9)]
        function: (identifier [(3, 0), (3, 3)])
        arguments: (arguments [(3, 3), (3, 9)]
          open: "[[" [(3, 3), (3, 5)]
          argument: (argument [(3, 5), (3, 6)]
            value: (identifier [(3, 5), (3, 6)])
          )
          (comma [(3, 6), (3, 7)])
          close: "]]" [(3, 7), (3, 9)]
        )
      )
      
      Text
      foo[[x,]]
      
      S-Expression
      (subset2 [(4, 0), (4, 10)]
        function: (identifier [(4, 0), (4, 3)])
        arguments: (arguments [(4, 3), (4, 10)]
          open: "[[" [(4, 3), (4, 5)]
          argument: (argument [(4, 5), (4, 6)]
            value: (identifier [(4, 5), (4, 6)])
          )
          (comma [(4, 6), (4, 7)])
          (comma [(4, 7), (4, 8)])
          close: "]]" [(4, 8), (4, 10)]
        )
      )
      
      Text
      foo[[x,,]]
      
      S-Expression
      (subset2 [(5, 0), (5, 11)]
        function: (identifier [(5, 0), (5, 3)])
        arguments: (arguments [(5, 3), (5, 11)]
          open: "[[" [(5, 3), (5, 5)]
          argument: (argument [(5, 5), (5, 6)]
            value: (identifier [(5, 5), (5, 6)])
          )
          (comma [(5, 6), (5, 7)])
          (comma [(5, 7), (5, 8)])
          argument: (argument [(5, 8), (5, 9)]
            value: (identifier [(5, 8), (5, 9)])
          )
          close: "]]" [(5, 9), (5, 11)]
        )
      )
      
      Text
      foo[[x,,y]]
      
      S-Expression
      (subset2 [(6, 0), (6, 7)]
        function: (identifier [(6, 0), (6, 3)])
        arguments: (arguments [(6, 3), (6, 7)]
          open: "[[" [(6, 3), (6, 5)]
          close: "]]" [(6, 5), (6, 7)]
        )
      )
      
      Text
      foo[[]]
      

# subset and subset2 precedence

    Code
      node_children_print(node)
    Output
      S-Expression
      (subset2 [(1, 0), (1, 9)]
        function: (identifier [(1, 0), (1, 1)])
        arguments: (arguments [(1, 1), (1, 9)]
          open: "[[" [(1, 1), (1, 3)]
          argument: (argument [(1, 3), (1, 7)]
            value: (subset [(1, 3), (1, 7)]
              function: (identifier [(1, 3), (1, 4)])
              arguments: (arguments [(1, 4), (1, 7)]
                open: "[" [(1, 4), (1, 5)]
                argument: (argument [(1, 5), (1, 6)]
                  value: (float [(1, 5), (1, 6)])
                )
                close: "]" [(1, 6), (1, 7)]
              )
            )
          )
          close: "]]" [(1, 7), (1, 9)]
        )
      )
      
      Text
      a[[b[1]]]
      
      S-Expression
      (subset [(2, 0), (2, 9)]
        function: (identifier [(2, 0), (2, 1)])
        arguments: (arguments [(2, 1), (2, 9)]
          open: "[" [(2, 1), (2, 2)]
          argument: (argument [(2, 2), (2, 8)]
            value: (subset2 [(2, 2), (2, 8)]
              function: (identifier [(2, 2), (2, 3)])
              arguments: (arguments [(2, 3), (2, 8)]
                open: "[[" [(2, 3), (2, 5)]
                argument: (argument [(2, 5), (2, 6)]
                  value: (float [(2, 5), (2, 6)])
                )
                close: "]]" [(2, 6), (2, 8)]
              )
            )
          )
          close: "]" [(2, 8), (2, 9)]
        )
      )
      
      Text
      a[b[[1]]]
      

# switch

    Code
      node_children_print(node)
    Output
      S-Expression
      (call [(1, 0), (6, 1)]
        function: (identifier [(1, 0), (1, 6)])
        arguments: (arguments [(1, 6), (6, 1)]
          open: "(" [(1, 6), (1, 7)]
          argument: (argument [(1, 7), (1, 10)]
            value: (identifier [(1, 7), (1, 10)])
          )
          (comma [(1, 10), (1, 11)])
          argument: (argument [(2, 2), (2, 7)]
            name: (identifier [(2, 2), (2, 3)])
            "=" [(2, 4), (2, 5)]
            value: (float [(2, 6), (2, 7)])
          )
          (comma [(2, 7), (2, 8)])
          argument: (argument [(3, 2), (3, 9)]
            name: (string [(3, 2), (3, 5)]
              "\"" [(3, 2), (3, 3)]
              content: (string_content [(3, 3), (3, 4)])
              "\"" [(3, 4), (3, 5)]
            )
            "=" [(3, 6), (3, 7)]
            value: (float [(3, 8), (3, 9)])
          )
          (comma [(3, 9), (3, 10)])
          argument: (argument [(4, 2), (4, 5)]
            name: (identifier [(4, 2), (4, 3)])
            "=" [(4, 4), (4, 5)]
          )
          (comma [(4, 6), (4, 7)])
          argument: (argument [(5, 2), (5, 3)]
            value: (float [(5, 2), (5, 3)])
          )
          close: ")" [(6, 0), (6, 1)]
        )
      )
      
      Text
      switch(foo,
        x = 1,
        "y" = 2,
        z = ,
        3
      )
      

# calls

    Code
      node_children_print(node)
    Output
      S-Expression
      (call [(1, 0), (1, 3)]
        function: (identifier [(1, 0), (1, 1)])
        arguments: (arguments [(1, 1), (1, 3)]
          open: "(" [(1, 1), (1, 2)]
          close: ")" [(1, 2), (1, 3)]
        )
      )
      
      Text
      f()
      
      S-Expression
      (call [(2, 0), (2, 4)]
        function: (identifier [(2, 0), (2, 1)])
        arguments: (arguments [(2, 1), (2, 4)]
          open: "(" [(2, 1), (2, 2)]
          argument: (argument [(2, 2), (2, 3)]
            value: (identifier [(2, 2), (2, 3)])
          )
          close: ")" [(2, 3), (2, 4)]
        )
      )
      
      Text
      f(x)
      
      S-Expression
      (call [(3, 0), (3, 6)]
        function: (identifier [(3, 0), (3, 1)])
        arguments: (arguments [(3, 1), (3, 6)]
          open: "(" [(3, 1), (3, 2)]
          argument: (argument [(3, 2), (3, 5)]
            value: (binary_operator [(3, 2), (3, 5)]
              lhs: (float [(3, 2), (3, 3)])
              operator: "+" [(3, 3), (3, 4)]
              rhs: (float [(3, 4), (3, 5)])
            )
          )
          close: ")" [(3, 5), (3, 6)]
        )
      )
      
      Text
      f(1+1)
      
      S-Expression
      (call [(4, 0), (4, 8)]
        function: (identifier [(4, 0), (4, 1)])
        arguments: (arguments [(4, 1), (4, 8)]
          open: "(" [(4, 1), (4, 2)]
          argument: (argument [(4, 2), (4, 7)]
            value: (binary_operator [(4, 2), (4, 7)]
              lhs: (float [(4, 2), (4, 3)])
              operator: "~" [(4, 4), (4, 5)]
              rhs: (float [(4, 6), (4, 7)])
            )
          )
          close: ")" [(4, 7), (4, 8)]
        )
      )
      
      Text
      f(1 ~ 1)
      
      S-Expression
      (call [(5, 0), (5, 6)]
        function: (identifier [(5, 0), (5, 1)])
        arguments: (arguments [(5, 1), (5, 6)]
          open: "(" [(5, 1), (5, 2)]
          argument: (argument [(5, 2), (5, 3)]
            value: (identifier [(5, 2), (5, 3)])
          )
          (comma [(5, 3), (5, 4)])
          close: ")" [(5, 5), (5, 6)]
        )
      )
      
      Text
      f(x, )
      
      S-Expression
      (call [(6, 0), (6, 7)]
        function: (identifier [(6, 0), (6, 1)])
        arguments: (arguments [(6, 1), (6, 7)]
          open: "(" [(6, 1), (6, 2)]
          argument: (argument [(6, 2), (6, 3)]
            value: (identifier [(6, 2), (6, 3)])
          )
          (comma [(6, 3), (6, 4)])
          (comma [(6, 4), (6, 5)])
          argument: (argument [(6, 5), (6, 6)]
            value: (identifier [(6, 5), (6, 6)])
          )
          close: ")" [(6, 6), (6, 7)]
        )
      )
      
      Text
      f(x,,y)
      
      S-Expression
      (call [(7, 0), (7, 7)]
        function: (identifier [(7, 0), (7, 1)])
        arguments: (arguments [(7, 1), (7, 7)]
          open: "(" [(7, 1), (7, 2)]
          argument: (argument [(7, 2), (7, 3)]
            value: (identifier [(7, 2), (7, 3)])
          )
          (comma [(7, 3), (7, 4)])
          argument: (argument [(7, 5), (7, 6)]
            value: (identifier [(7, 5), (7, 6)])
          )
          close: ")" [(7, 6), (7, 7)]
        )
      )
      
      Text
      f(x, y)
      
      S-Expression
      (call [(8, 0), (8, 11)]
        function: (identifier [(8, 0), (8, 1)])
        arguments: (arguments [(8, 1), (8, 11)]
          open: "(" [(8, 1), (8, 2)]
          argument: (argument [(8, 2), (8, 3)]
            value: (identifier [(8, 2), (8, 3)])
          )
          (comma [(8, 3), (8, 4)])
          argument: (argument [(8, 5), (8, 10)]
            name: (identifier [(8, 5), (8, 6)])
            "=" [(8, 7), (8, 8)]
            value: (float [(8, 9), (8, 10)])
          )
          close: ")" [(8, 10), (8, 11)]
        )
      )
      
      Text
      f(x, y = 2)
      
      S-Expression
      (call [(9, 0), (9, 12)]
        function: (identifier [(9, 0), (9, 1)])
        arguments: (arguments [(9, 1), (9, 12)]
          open: "(" [(9, 1), (9, 2)]
          argument: (argument [(9, 2), (9, 11)]
            name: (identifier [(9, 2), (9, 3)])
            "=" [(9, 4), (9, 5)]
            value: (binary_operator [(9, 6), (9, 11)]
              lhs: (float [(9, 6), (9, 7)])
              operator: "+" [(9, 8), (9, 9)]
              rhs: (float [(9, 10), (9, 11)])
            )
          )
          close: ")" [(9, 11), (9, 12)]
        )
      )
      
      Text
      f(x = 1 + 1)
      
      S-Expression
      (call [(10, 0), (10, 9)]
        function: (identifier [(10, 0), (10, 1)])
        arguments: (arguments [(10, 1), (10, 9)]
          open: "(" [(10, 1), (10, 2)]
          argument: (argument [(10, 2), (10, 3)]
            value: (identifier [(10, 2), (10, 3)])
          )
          (comma [(10, 3), (10, 4)])
          argument: (argument [(10, 5), (10, 8)]
            name: (identifier [(10, 5), (10, 6)])
            "=" [(10, 7), (10, 8)]
          )
          close: ")" [(10, 8), (10, 9)]
        )
      )
      
      Text
      f(x, y =)
      
      S-Expression
      (call [(11, 0), (11, 11)]
        function: (identifier [(11, 0), (11, 1)])
        arguments: (arguments [(11, 1), (11, 11)]
          open: "(" [(11, 1), (11, 2)]
          argument: (argument [(11, 2), (11, 10)]
            value: (call [(11, 2), (11, 10)]
              function: (identifier [(11, 2), (11, 4)])
              arguments: (arguments [(11, 4), (11, 10)]
                open: "(" [(11, 4), (11, 5)]
                argument: (argument [(11, 5), (11, 6)]
                  value: (identifier [(11, 5), (11, 6)])
                )
                (comma [(11, 6), (11, 7)])
                argument: (argument [(11, 8), (11, 9)]
                  value: (identifier [(11, 8), (11, 9)])
                )
                close: ")" [(11, 9), (11, 10)]
              )
            )
          )
          close: ")" [(11, 10), (11, 11)]
        )
      )
      
      Text
      f(f2(x, y))
      
      S-Expression
      (call [(12, 0), (12, 4)]
        function: (identifier [(12, 0), (12, 1)])
        arguments: (arguments [(12, 1), (12, 4)]
          open: "(" [(12, 1), (12, 2)]
          (comma [(12, 2), (12, 3)])
          close: ")" [(12, 3), (12, 4)]
        )
      )
      
      Text
      f(,)
      
      S-Expression
      (call [(13, 0), (13, 5)]
        function: (identifier [(13, 0), (13, 1)])
        arguments: (arguments [(13, 1), (13, 5)]
          open: "(" [(13, 1), (13, 2)]
          argument: (argument [(13, 2), (13, 3)]
            value: (identifier [(13, 2), (13, 3)])
          )
          (comma [(13, 3), (13, 4)])
          close: ")" [(13, 4), (13, 5)]
        )
      )
      
      Text
      f(x,)
      
      S-Expression
      (call [(14, 0), (14, 5)]
        function: (identifier [(14, 0), (14, 1)])
        arguments: (arguments [(14, 1), (14, 5)]
          open: "(" [(14, 1), (14, 2)]
          (comma [(14, 2), (14, 3)])
          argument: (argument [(14, 3), (14, 4)]
            value: (identifier [(14, 3), (14, 4)])
          )
          close: ")" [(14, 4), (14, 5)]
        )
      )
      
      Text
      f(,y)
      
      S-Expression
      (call [(15, 0), (15, 6)]
        function: (identifier [(15, 0), (15, 1)])
        arguments: (arguments [(15, 1), (15, 6)]
          open: "(" [(15, 1), (15, 2)]
          argument: (argument [(15, 2), (15, 4)]
            name: (identifier [(15, 2), (15, 3)])
            "=" [(15, 3), (15, 4)]
          )
          (comma [(15, 4), (15, 5)])
          close: ")" [(15, 5), (15, 6)]
        )
      )
      
      Text
      f(x=,)
      
      S-Expression
      (call [(16, 0), (16, 8)]
        function: (identifier [(16, 0), (16, 1)])
        arguments: (arguments [(16, 1), (16, 8)]
          open: "(" [(16, 1), (16, 2)]
          argument: (argument [(16, 2), (16, 6)]
            name: (string [(16, 2), (16, 5)]
              "\"" [(16, 2), (16, 3)]
              content: (string_content [(16, 3), (16, 4)])
              "\"" [(16, 4), (16, 5)]
            )
            "=" [(16, 5), (16, 6)]
          )
          (comma [(16, 6), (16, 7)])
          close: ")" [(16, 7), (16, 8)]
        )
      )
      
      Text
      f("x"=,)
      
      S-Expression
      (call [(17, 0), (17, 6)]
        function: (identifier [(17, 0), (17, 1)])
        arguments: (arguments [(17, 1), (17, 6)]
          open: "(" [(17, 1), (17, 2)]
          (comma [(17, 2), (17, 3)])
          argument: (argument [(17, 3), (17, 5)]
            name: (identifier [(17, 3), (17, 4)])
            "=" [(17, 4), (17, 5)]
          )
          close: ")" [(17, 5), (17, 6)]
        )
      )
      
      Text
      f(,y=)
      
      S-Expression
      (comment [(19, 0), (19, 36)])
      
      Text
      # Dots as unnamed and named argument
      
      S-Expression
      (call [(20, 0), (20, 6)]
        function: (identifier [(20, 0), (20, 1)])
        arguments: (arguments [(20, 1), (20, 6)]
          open: "(" [(20, 1), (20, 2)]
          argument: (argument [(20, 2), (20, 5)]
            value: (dots [(20, 2), (20, 5)])
          )
          close: ")" [(20, 5), (20, 6)]
        )
      )
      
      Text
      f(...)
      
      S-Expression
      (call [(21, 0), (21, 11)]
        function: (identifier [(21, 0), (21, 1)])
        arguments: (arguments [(21, 1), (21, 11)]
          open: "(" [(21, 1), (21, 2)]
          (comma [(21, 2), (21, 3)])
          argument: (argument [(21, 4), (21, 7)]
            value: (dots [(21, 4), (21, 7)])
          )
          (comma [(21, 7), (21, 8)])
          argument: (argument [(21, 9), (21, 10)]
            value: (float [(21, 9), (21, 10)])
          )
          close: ")" [(21, 10), (21, 11)]
        )
      )
      
      Text
      f(, ..., 1)
      
      S-Expression
      (call [(22, 0), (22, 10)]
        function: (identifier [(22, 0), (22, 1)])
        arguments: (arguments [(22, 1), (22, 10)]
          open: "(" [(22, 1), (22, 2)]
          argument: (argument [(22, 2), (22, 9)]
            name: (dots [(22, 2), (22, 5)])
            "=" [(22, 6), (22, 7)]
            value: (float [(22, 8), (22, 9)])
          )
          close: ")" [(22, 9), (22, 10)]
        )
      )
      
      Text
      f(... = 1)
      
      S-Expression
      (call [(23, 0), (23, 10)]
        function: (identifier [(23, 0), (23, 1)])
        arguments: (arguments [(23, 1), (23, 10)]
          open: "(" [(23, 1), (23, 2)]
          argument: (argument [(23, 2), (23, 7)]
            name: (dots [(23, 2), (23, 5)])
            "=" [(23, 6), (23, 7)]
          )
          (comma [(23, 8), (23, 9)])
          close: ")" [(23, 9), (23, 10)]
        )
      )
      
      Text
      f(... = ,)
      
      S-Expression
      (call [(24, 0), (24, 12)]
        function: (identifier [(24, 0), (24, 1)])
        arguments: (arguments [(24, 1), (24, 12)]
          open: "(" [(24, 1), (24, 2)]
          argument: (argument [(24, 2), (24, 11)]
            name: (dots [(24, 2), (24, 5)])
            "=" [(24, 6), (24, 7)]
            value: (dots [(24, 8), (24, 11)])
          )
          close: ")" [(24, 11), (24, 12)]
        )
      )
      
      Text
      f(... = ...)
      
      S-Expression
      (comment [(26, 0), (26, 37)])
      
      Text
      # `..i` as unnamed and named argument
      
      S-Expression
      (call [(27, 0), (27, 6)]
        function: (identifier [(27, 0), (27, 1)])
        arguments: (arguments [(27, 1), (27, 6)]
          open: "(" [(27, 1), (27, 2)]
          argument: (argument [(27, 2), (27, 5)]
            value: (dot_dot_i [(27, 2), (27, 5)])
          )
          close: ")" [(27, 5), (27, 6)]
        )
      )
      
      Text
      f(..1)
      
      S-Expression
      (call [(28, 0), (28, 11)]
        function: (identifier [(28, 0), (28, 1)])
        arguments: (arguments [(28, 1), (28, 11)]
          open: "(" [(28, 1), (28, 2)]
          (comma [(28, 2), (28, 3)])
          argument: (argument [(28, 4), (28, 7)]
            value: (dot_dot_i [(28, 4), (28, 7)])
          )
          (comma [(28, 7), (28, 8)])
          argument: (argument [(28, 9), (28, 10)]
            value: (float [(28, 9), (28, 10)])
          )
          close: ")" [(28, 10), (28, 11)]
        )
      )
      
      Text
      f(, ..1, 1)
      
      S-Expression
      (call [(29, 0), (29, 10)]
        function: (identifier [(29, 0), (29, 1)])
        arguments: (arguments [(29, 1), (29, 10)]
          open: "(" [(29, 1), (29, 2)]
          argument: (argument [(29, 2), (29, 9)]
            name: (dot_dot_i [(29, 2), (29, 5)])
            "=" [(29, 6), (29, 7)]
            value: (float [(29, 8), (29, 9)])
          )
          close: ")" [(29, 9), (29, 10)]
        )
      )
      
      Text
      f(..1 = 1)
      
      S-Expression
      (call [(30, 0), (30, 10)]
        function: (identifier [(30, 0), (30, 1)])
        arguments: (arguments [(30, 1), (30, 10)]
          open: "(" [(30, 1), (30, 2)]
          argument: (argument [(30, 2), (30, 7)]
            name: (dot_dot_i [(30, 2), (30, 5)])
            "=" [(30, 6), (30, 7)]
          )
          (comma [(30, 8), (30, 9)])
          close: ")" [(30, 9), (30, 10)]
        )
      )
      
      Text
      f(..1 = ,)
      
      S-Expression
      (call [(31, 0), (31, 12)]
        function: (identifier [(31, 0), (31, 1)])
        arguments: (arguments [(31, 1), (31, 12)]
          open: "(" [(31, 1), (31, 2)]
          argument: (argument [(31, 2), (31, 11)]
            name: (dot_dot_i [(31, 2), (31, 5)])
            "=" [(31, 6), (31, 7)]
            value: (dot_dot_i [(31, 8), (31, 11)])
          )
          close: ")" [(31, 11), (31, 12)]
        )
      )
      
      Text
      f(..1 = ..1)
      

# not a call, subset, or subset2

    Code
      node_children_print(node)
    Output
      S-Expression
      (identifier [(1, 0), (1, 1)])
      
      Text
      f
      
      S-Expression
      (parenthesized_expression [(2, 0), (2, 3)]
        open: "(" [(2, 0), (2, 1)]
        body: (identifier [(2, 1), (2, 2)])
        close: ")" [(2, 2), (2, 3)]
      )
      
      Text
      (x)
      
      S-Expression
      (identifier [(4, 0), (4, 3)])
      
      Text
      foo
      
      S-Expression
      (ERROR [(5, 0), (5, 1)]
        (ERROR [(5, 0), (5, 1)])
      )
      
      Text
      [
      
      S-Expression
      (identifier [(5, 1), (5, 4)])
      
      Text
      bar
      
      S-Expression
      (ERROR [(5, 4), (5, 5)]
        (ERROR [(5, 4), (5, 5)])
      )
      
      Text
      ]
      
      S-Expression
      (identifier [(7, 0), (7, 3)])
      
      Text
      foo
      
      S-Expression
      (ERROR [(8, 0), (8, 2)]
        (ERROR [(8, 0), (8, 2)])
      )
      
      Text
      [[
      
      S-Expression
      (identifier [(8, 2), (8, 3)])
      
      Text
      x
      
      S-Expression
      (ERROR [(8, 3), (8, 5)]
        (ERROR [(8, 3), (8, 5)])
      )
      
      Text
      ]]
      

# not a call, subset, or subset2 due to sequential arguments

    Code
      node_children_print(node)
    Output
      S-Expression
      (call [(1, 0), (1, 6)]
        function: (identifier [(1, 0), (1, 1)])
        arguments: (arguments [(1, 1), (1, 6)]
          open: "(" [(1, 1), (1, 2)]
          (ERROR [(1, 2), (1, 3)]
            (identifier [(1, 2), (1, 3)])
          )
          argument: (argument [(1, 4), (1, 5)]
            value: (identifier [(1, 4), (1, 5)])
          )
          close: ")" [(1, 5), (1, 6)]
        )
      )
      
      Text
      f(x y)
      
      S-Expression
      (subset [(2, 0), (2, 8)]
        function: (identifier [(2, 0), (2, 3)])
        arguments: (arguments [(2, 3), (2, 8)]
          open: "[" [(2, 3), (2, 4)]
          (ERROR [(2, 4), (2, 5)]
            (identifier [(2, 4), (2, 5)])
          )
          argument: (argument [(2, 6), (2, 7)]
            value: (identifier [(2, 6), (2, 7)])
          )
          close: "]" [(2, 7), (2, 8)]
        )
      )
      
      Text
      foo[x y]
      
      S-Expression
      (subset2 [(3, 0), (3, 10)]
        function: (identifier [(3, 0), (3, 3)])
        arguments: (arguments [(3, 3), (3, 10)]
          open: "[[" [(3, 3), (3, 5)]
          (ERROR [(3, 5), (3, 6)]
            (identifier [(3, 5), (3, 6)])
          )
          argument: (argument [(3, 7), (3, 8)]
            value: (identifier [(3, 7), (3, 8)])
          )
          close: "]]" [(3, 8), (3, 10)]
        )
      )
      
      Text
      foo[[x y]]
      
      S-Expression
      (call [(5, 0), (5, 9)]
        function: (identifier [(5, 0), (5, 1)])
        arguments: (arguments [(5, 1), (5, 9)]
          open: "(" [(5, 1), (5, 2)]
          argument: (argument [(5, 2), (5, 3)]
            value: (identifier [(5, 2), (5, 3)])
          )
          (comma [(5, 3), (5, 4)])
          (ERROR [(5, 5), (5, 6)]
            (identifier [(5, 5), (5, 6)])
          )
          argument: (argument [(5, 7), (5, 8)]
            value: (identifier [(5, 7), (5, 8)])
          )
          close: ")" [(5, 8), (5, 9)]
        )
      )
      
      Text
      f(x, y z)
      
      S-Expression
      (subset [(6, 0), (6, 11)]
        function: (identifier [(6, 0), (6, 3)])
        arguments: (arguments [(6, 3), (6, 11)]
          open: "[" [(6, 3), (6, 4)]
          argument: (argument [(6, 4), (6, 5)]
            value: (identifier [(6, 4), (6, 5)])
          )
          (comma [(6, 5), (6, 6)])
          (ERROR [(6, 7), (6, 8)]
            (identifier [(6, 7), (6, 8)])
          )
          argument: (argument [(6, 9), (6, 10)]
            value: (identifier [(6, 9), (6, 10)])
          )
          close: "]" [(6, 10), (6, 11)]
        )
      )
      
      Text
      foo[x, y z]
      
      S-Expression
      (subset2 [(7, 0), (7, 13)]
        function: (identifier [(7, 0), (7, 3)])
        arguments: (arguments [(7, 3), (7, 13)]
          open: "[[" [(7, 3), (7, 5)]
          argument: (argument [(7, 5), (7, 6)]
            value: (identifier [(7, 5), (7, 6)])
          )
          (comma [(7, 6), (7, 7)])
          (ERROR [(7, 8), (7, 9)]
            (identifier [(7, 8), (7, 9)])
          )
          argument: (argument [(7, 10), (7, 11)]
            value: (identifier [(7, 10), (7, 11)])
          )
          close: "]]" [(7, 11), (7, 13)]
        )
      )
      
      Text
      foo[[x, y z]]
      
      S-Expression
      (call [(9, 0), (9, 8)]
        function: (identifier [(9, 0), (9, 1)])
        arguments: (arguments [(9, 1), (9, 8)]
          open: "(" [(9, 1), (9, 2)]
          (comma [(9, 2), (9, 3)])
          (ERROR [(9, 4), (9, 5)]
            (identifier [(9, 4), (9, 5)])
          )
          argument: (argument [(9, 6), (9, 7)]
            value: (identifier [(9, 6), (9, 7)])
          )
          close: ")" [(9, 7), (9, 8)]
        )
      )
      
      Text
      f(, x y)
      
      S-Expression
      (subset [(10, 0), (10, 10)]
        function: (identifier [(10, 0), (10, 3)])
        arguments: (arguments [(10, 3), (10, 10)]
          open: "[" [(10, 3), (10, 4)]
          (comma [(10, 4), (10, 5)])
          (ERROR [(10, 6), (10, 7)]
            (identifier [(10, 6), (10, 7)])
          )
          argument: (argument [(10, 8), (10, 9)]
            value: (identifier [(10, 8), (10, 9)])
          )
          close: "]" [(10, 9), (10, 10)]
        )
      )
      
      Text
      foo[, x y]
      
      S-Expression
      (subset2 [(11, 0), (11, 12)]
        function: (identifier [(11, 0), (11, 3)])
        arguments: (arguments [(11, 3), (11, 12)]
          open: "[[" [(11, 3), (11, 5)]
          (comma [(11, 5), (11, 6)])
          (ERROR [(11, 7), (11, 8)]
            (identifier [(11, 7), (11, 8)])
          )
          argument: (argument [(11, 9), (11, 10)]
            value: (identifier [(11, 9), (11, 10)])
          )
          close: "]]" [(11, 10), (11, 12)]
        )
      )
      
      Text
      foo[[, x y]]
      

# braced expression

    Code
      node_children_print(node)
    Output
      S-Expression
      (braced_expression [(1, 0), (1, 2)]
        open: "{" [(1, 0), (1, 1)]
        close: "}" [(1, 1), (1, 2)]
      )
      
      Text
      {}
      
      S-Expression
      (braced_expression [(3, 0), (3, 3)]
        open: "{" [(3, 0), (3, 1)]
        body: (float [(3, 1), (3, 2)])
        close: "}" [(3, 2), (3, 3)]
      )
      
      Text
      {1}
      
      S-Expression
      (braced_expression [(5, 0), (5, 6)]
        open: "{" [(5, 0), (5, 1)]
        body: (float [(5, 1), (5, 2)])
        body: (float [(5, 4), (5, 5)])
        close: "}" [(5, 5), (5, 6)]
      )
      
      Text
      {1; 2}
      
      S-Expression
      (braced_expression [(7, 0), (8, 2)]
        open: "{" [(7, 0), (7, 1)]
        body: (float [(7, 1), (7, 2)])
        body: (float [(8, 0), (8, 1)])
        close: "}" [(8, 1), (8, 2)]
      )
      
      Text
      {1;
      2}
      
      S-Expression
      (braced_expression [(10, 0), (12, 1)]
        open: "{" [(10, 0), (10, 1)]
        body: (float [(10, 1), (10, 2)])
        body: (float [(11, 0), (11, 1)])
        close: "}" [(12, 0), (12, 1)]
      )
      
      Text
      {1
      2
      }
      
      S-Expression
      (braced_expression [(14, 0), (17, 1)]
        open: "{" [(14, 0), (14, 1)]
        body: (float [(15, 0), (15, 1)])
        body: (float [(16, 0), (16, 1)])
        close: "}" [(17, 0), (17, 1)]
      )
      
      Text
      {
      1
      2
      }
      
      S-Expression
      (comment [(19, 0), (19, 50)])
      
      Text
      # https://github.com/r-lib/tree-sitter-r/issues/44
      
      S-Expression
      (braced_expression [(20, 0), (24, 1)]
        open: "{" [(20, 0), (20, 1)]
        body: (float [(21, 2), (21, 3)])
        body: (float [(22, 0), (22, 1)])
        body: (float [(23, 2), (23, 3)])
        close: "}" [(24, 0), (24, 1)]
      )
      
      Text
      {
        1
      2
        3
      }
      

# parenthesized expression

    Code
      node_children_print(node)
    Output
      S-Expression
      (parenthesized_expression [(1, 0), (1, 3)]
        open: "(" [(1, 0), (1, 1)]
        body: (float [(1, 1), (1, 2)])
        close: ")" [(1, 2), (1, 3)]
      )
      
      Text
      (1)
      
      S-Expression
      (parenthesized_expression [(2, 0), (2, 5)]
        open: "(" [(2, 0), (2, 1)]
        body: (parenthesized_expression [(2, 1), (2, 4)]
          open: "(" [(2, 1), (2, 2)]
          body: (float [(2, 2), (2, 3)])
          close: ")" [(2, 3), (2, 4)]
        )
        close: ")" [(2, 4), (2, 5)]
      )
      
      Text
      ((1))
      
      S-Expression
      (parenthesized_expression [(3, 0), (3, 7)]
        open: "(" [(3, 0), (3, 1)]
        body: (binary_operator [(3, 1), (3, 6)]
          lhs: (float [(3, 1), (3, 2)])
          operator: "+" [(3, 3), (3, 4)]
          rhs: (float [(3, 5), (3, 6)])
        )
        close: ")" [(3, 6), (3, 7)]
      )
      
      Text
      (1 + 1)
      
      S-Expression
      (parenthesized_expression [(4, 0), (4, 10)]
        open: "(" [(4, 0), (4, 1)]
        body: (call [(4, 1), (4, 9)]
          function: (identifier [(4, 1), (4, 3)])
          arguments: (arguments [(4, 3), (4, 9)]
            open: "(" [(4, 3), (4, 4)]
            argument: (argument [(4, 4), (4, 5)]
              value: (identifier [(4, 4), (4, 5)])
            )
            (comma [(4, 5), (4, 6)])
            argument: (argument [(4, 7), (4, 8)]
              value: (identifier [(4, 7), (4, 8)])
            )
            close: ")" [(4, 8), (4, 9)]
          )
        )
        close: ")" [(4, 9), (4, 10)]
      )
      
      Text
      (fn(a, b))
      
      S-Expression
      (call [(5, 0), (5, 12)]
        function: (identifier [(5, 0), (5, 2)])
        arguments: (arguments [(5, 2), (5, 12)]
          open: "(" [(5, 2), (5, 3)]
          argument: (argument [(5, 3), (5, 6)]
            value: (parenthesized_expression [(5, 3), (5, 6)]
              open: "(" [(5, 3), (5, 4)]
              body: (identifier [(5, 4), (5, 5)])
              close: ")" [(5, 5), (5, 6)]
            )
          )
          (comma [(5, 6), (5, 7)])
          argument: (argument [(5, 8), (5, 11)]
            value: (parenthesized_expression [(5, 8), (5, 11)]
              open: "(" [(5, 8), (5, 9)]
              body: (identifier [(5, 9), (5, 10)])
              close: ")" [(5, 10), (5, 11)]
            )
          )
          close: ")" [(5, 11), (5, 12)]
        )
      )
      
      Text
      fn((a), (b))
      
      S-Expression
      (parenthesized_expression [(6, 0), (8, 2)]
        open: "(" [(6, 0), (6, 1)]
        body: (function_definition [(6, 1), (8, 1)]
          name: "function" [(6, 1), (6, 9)]
          parameters: (parameters [(6, 9), (6, 11)]
            open: "(" [(6, 9), (6, 10)]
            close: ")" [(6, 10), (6, 11)]
          )
          body: (braced_expression [(6, 12), (8, 1)]
            open: "{" [(6, 12), (6, 13)]
            body: (identifier [(7, 2), (7, 6)])
            close: "}" [(8, 0), (8, 1)]
          )
        )
        close: ")" [(8, 1), (8, 2)]
      )
      
      Text
      (function() {
        body
      })
      

# not a parenthesized expression 1

    Code
      node_children_print(node)
    Output
      S-Expression
      (ERROR [(1, 0), (1, 2)]
        "(" [(1, 0), (1, 1)]
        (ERROR [(1, 1), (1, 2)])
      )
      
      Text
      ()
      

# not a parenthesized expression 2

    Code
      node_children_print(node)
    Output
      S-Expression
      (parenthesized_expression [(1, 0), (4, 1)]
        open: "(" [(1, 0), (1, 1)]
        (ERROR [(2, 2), (2, 3)])
        body: (float [(3, 2), (3, 3)])
        close: ")" [(4, 0), (4, 1)]
      )
      
      Text
      (
        1
        2
      )
      

# not a parenthesized expression 3

    Code
      node_children_print(node)
    Output
      S-Expression
      (parenthesized_expression [(1, 0), (1, 6)]
        open: "(" [(1, 0), (1, 1)]
        (ERROR [(1, 1), (1, 3)]
          (ERROR [(1, 2), (1, 3)])
        )
        body: (float [(1, 4), (1, 5)])
        close: ")" [(1, 5), (1, 6)]
      )
      
      Text
      (1; 2)
      

