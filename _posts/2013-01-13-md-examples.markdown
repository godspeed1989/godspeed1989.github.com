---
layout: page
title : markdown example
categories : [lessons, beginner]
tagline: some markdown examples
---
# H1
followed by some text

## H2
followed by some text

### H3
followed by some text

#### H4
followed by some text

##### H5
followed by some text

###### H6
followed by some text

- ** aaa **  
	123456789

`inline code`

*italics*

**strong font**

"Line" Separator:

--

"Slanted" Separator:

------

|Table Header 1|Table Header 2|Table Header 3|
|--------------|--------------|--------------|
|Content       |Content       |Content       |
|Content       |Content       |Content       |


```c++
#include <iostream>
using namespace std;
int main()
{
	return 0;
}
```

```bash
$sudo apt-get install xxx
$sudo shutdown -h now
```

    $ cowsay -t 1234


Here's a sample "posts list".

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

