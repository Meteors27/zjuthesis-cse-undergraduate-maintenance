# 控制科学与工程本科生毕业设计论文模板使用说明

## 各阶段通用
1. 封面和页眉里采用`浙江大学本科生毕业论文（设计）`而不是`浙江大学本科生毕业论文`
    - 重写 `\TitleTypeName`
    - 提供 `page\undergraduate\final\major\cse\cover.tex`
    - 提供 `page\undergraduate\proposal\major\cse\cover.tex`

## 三合一

三合一与通用模板的不同之处有：
1. 目录里外文翻译和原文不需要包含二级标题
    - 额外提供 `\hiddenTocSucsec` 和 `\showTocSucsec` 命令
    - 在 `body\undergraduate\proposal\content.tex` 中使用
        ```latex
        % `thesis` content
        \inputbody{proposal/review/review}
        \inputbody{proposal/proposal/proposal}
        \hiddenTocSucsec
        \inputbody{proposal/translation/translation}
        \inputbody{proposal/original/original}
        \showTocSubsec
        ```
2. 外文翻译摘要部分的格式要求
    - 提供 `\translationheader{译文题目}{引文关键字}{摘要}{关键字}` 命令
    - 在 `body\undergraduate\proposal\translation\translation.tex` 中使用
        ```latex
        \translationheader{译文题目}{zjuthesisrules}{摘要}{关键字}
        % 译文题目：译文题目
        % 原文题目：浙江大学本科生毕业论文（设计）编写规则
        % 原文来源：浙江大学本科生院. 浙江大学本科生毕业论文（设计）编写规则[EB/OL]. 2018. http://bksy.zju.edu.cn/attachments/2018-01/01-1517384518-1149149.pdf
        % 
        %     摘要：摘要
        %     关键字：关键字
        ```