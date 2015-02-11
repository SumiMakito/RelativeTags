RelativeTags
=============

A efficient tag-category solution for MySQL databases.

一个为MySQL数据库准备的高效的标签分类系统。

#### APIs

*Only list main APIs at here.*

*仅列出主要API*

* search_tag.php?tag=<int>&json=1

* * Return items marked with the given tag as JSON.(Single tag only.)

* * 以JSON格式返回标有标签的物品。(仅支持单标签查询)

##### Union Mode 并集模式

> In theory, the items collection returned from union mode is the largest.
> 理论上来说，并集模式返回的物品集合应该是最大的。

* union_search_tag.php?tag=<int[]>&json=1

* * Return items which have one of the given tag(s)s as JSON.(Suppprt multi-tag search)

* * 以JSON格式返回带有给出标签中的一个或多个标签的物品。(支持多标签联合查询)

##### Intersection Mode 交集模式

> In theory, the items collection returned from intersection mode is the smallest.
> 理论上来说，交集模式返回的物品集合应该是最小的。

* intersection_search_tag.php?tag=<int[]>&json=1

* * Return items which have all the given tag(s) as JSON.(Suppprt multi-tag search)

* * 以JSON格式返回带有给出所有标签的物品。(支持多标签联合查询)

##### Relative Mode 相关性模式

* relative_search_tag.php?tag=<int[]>&json=1

* * Return items which have high relative with the given tag(s) as JSON.(Support multi-tag search)

* * 以JSON格式返回与给定标签有高相关性的物品。(支持多标签联合查询)

##### Relativity 相关性计算

> In this section, the relativity is a double(data type) between 0 and 100.
> 在这个区域，相关性的值是一个在0与100之间的双精度浮点数。

* tag_relativity.php?tag=<int[1|2]>&json=1

* * If one tag is given, program will return the relativity between the given tag and others one by one as JSON.

* * 如果只给出了一个标签，程序将返回该标签与其他每个标签的相关性。

* * If two tags are given, program will return the relativity between the given tags as JSON.

* * 如果给出了两个标签，程序将返回这两个标签的相关性。

###### Copyright(c)2014-2015 Sumi Makito.