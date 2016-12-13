### 处理dataFrame数据

问题：

\`\`\` python

import pandas as pd

df = pd.DataFrame\({'$a': \[1\], '$b': \[1\], '$c': \[1\], '$d': \[1\], '$e': \[1\]}\)

\`\`\`

解决办法：

方法一：

\`\`\`  python

\# ①暴力

df.columns = \['a', 'b', 'c', 'd', 'e'\]

\# ②修改

df.columns = df.columns.str.strip\('$'\)

\# ③修改

df.columns = df.columns.map\(lambda x:x\[1:\]\)

\`\`\`

方法二：

\`\`\`python

\# ④暴力（好处：也可只修改特定的列）

df.rename\(columns=\('$a': 'a', '$b': 'b', '$c': 'c', '$d': 'd', '$e': 'e'}, inplace=True\)

\# ⑤修改

df.rename\(columns=lambda x:x.replace\('$',''\), inplace=True\)

\`\`\`

a

* \[ \] a task list item

* \[ \] list syntax required

* \[ \] normal \*\*formatting\*\*, @mentions, \#1234 refs

* \[ \] incomplete

* \[x\] completed


\| taaa \| aaa  \| aaa  \|

\| :--: \| :--: \| :--: \|

\|  11  \|  11  \| 222  \|

\|  33  \|  44  \|  4   \|

\|  5   \|  5   \|  5   \|

\[^footnote\]: Here is the \*text\* of the \*\*footnote\*\*.

\[Google\]: [http://google.com/](http://google.com/)

