---
title: "Macro Editing: Find & Highlight Text with EmEditor - A Comprehensive Guide"
date: 2024-11-24T00:50:04.608Z
updated: 2024-12-01T04:46:42.721Z
tags:
  - product
categories:
  - emeditor
thumbnail: https://thmb.techidaily.com/58d6990fb1aba3befeda20029d053fd2dc8e67729321f3227eadd737a516d064.jpg
---

## Macro Editing: Find & Highlight Text with EmEditor - A Comprehensive Guide

Viewing 8 posts - 1 through 8 (of 8 total)

* Author  
Posts
* November 23, 2008 at 12:14 am [#6648](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/2bfa57107170d3c133129829a740038d?s=80&d=identicon&r=g)masha](https://www.emeditor.com/forums/users/masha/ "View masha's profile")  
Member  
Hello  
 How to change color and style of given lines or characters ?  
 I want to to highlight and/or underscore some words and lines as a result of some analysis performed in my macro (and external tools executed from the macro).  
November 23, 2008 at 2:29 am [#6652](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a5eb599d531317d793c9094332d63e0d?s=80&d=identicon&r=g)webern](https://www.emeditor.com/forums/users/webern/ "View webern's profile")  
Member  
EmEditor has an ability to highlight words with RegExp.  
 Also you may check Macro Reference for three **Highlight** objects and three **Font** objects.  
November 23, 2008 at 10:37 am [#6654](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/2bfa57107170d3c133129829a740038d?s=80&d=identicon&r=g)masha](https://www.emeditor.com/forums/users/masha/ "View masha's profile")  
Member  
Is it possible to highight lines having their numbers ?  
 For example, my macro runs Lint or compiler, parses its output and got an array of line numbers.  
 Then I want to see them underlined (or with red background) in editor.  
November 24, 2008 at 7:19 pm [#6663](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
> masha wrote:  
> Is it possible to highight lines having their numbers ?  
>  
> For example, my macro runs Lint or compiler, parses its output and got an array of line numbers.  
> Then I want to see them underlined (or with red background) in editor.  
 If you want to highlght line numbers so they become mouse-clickable, you need to write a single-line JavaScript macro:  
 document.HighlightTag = true;  
 and run this macro when you need it.  
 You might need to adjust the Tag Format in the Edit tab of Customize dialog box (on Tools menu).  
November 24, 2008 at 10:12 pm [#6666](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/2bfa57107170d3c133129829a740038d?s=80&d=identicon&r=g)masha](https://www.emeditor.com/forums/users/masha/ "View masha's profile")  
Member  
No, it is not what I want.  
 I have array of integers in my macro, let’s say \[10,12,20,34,41\].  
 And I want to have different look of those lines in the editor window.  
 For example, if the numbers could be lines with compiler warnings.  
 it is weird to click each line in output window to find it in editor window (altought sometimes it is useful too). Much better to have the lines highlihted in the editor window.  
 Also, some tools (notably Visual C++ run with /analyze command line switch) may output a few lines numbers for each error or warning, thus make unuseful location the errors by the tag regexp.  
 May by the solution is to write a plugin to hook the points where emeditor calls WinAPI to draw the text. But it seems to be a quite complex hack.  
November 25, 2008 at 12:56 am [#6668](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
> masha wrote:  
> No, it is not what I want.  
> I have array of integers in my macro, let’s say \[10,12,20,34,41\].  
> And I want to have different look of those lines in the editor window.  
> For example, if the numbers could be lines with compiler warnings.  
> it is weird to click each line in output window to find it in editor window (altought sometimes it is useful too). Much better to have the lines highlihted in the editor window.  
>  
> Also, some tools (notably Visual C++ run with /analyze command line switch) may output a few lines numbers for each error or warning, thus make unuseful location the errors by the tag regexp.  
>  
> May by the solution is to write a plugin to hook the points where emeditor calls WinAPI to draw the text. But it seems to be a quite complex hack.  
 OK. In Configuration Properties, select Highlight (1) tab, and then you can enter a regular expression to highlight certain numbers. For instance, ^\[0-9\]+? will select first numbers at each line.  
November 25, 2008 at 8:13 am [#6670](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/2bfa57107170d3c133129829a740038d?s=80&d=identicon&r=g)masha](https://www.emeditor.com/forums/users/masha/ "View masha's profile")  
Member  
I do not need to hightlight the numbers itself, i want to highlihg the lines.  
 having \[10,12,20,34,41\] I want to highligt tenth, twelfth, twentieth, thirtyfourth and fourtyfirst LINES, but not the numbers.  
 I know that the could be regexp like (10|12|20|34|41), but there is no the numbers in the text.  
November 25, 2008 at 9:48 pm [#6676](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
> masha wrote:  
> I do not need to hightlight the numbers itself, i want to highlihg the lines.  
> having \[10,12,20,34,41\] I want to highligt tenth, twelfth, twentieth, thirtyfourth and fourtyfirst LINES, but not the numbers.  
> I know that the could be regexp like (10|12|20|34|41), but there is no the numbers in the text.  
 In this case, you cannot change the color of particular line numbers. Howerver you can toggle bookmarks on particualr lines if you would like. Bookmarks can be set by using SetBookmark Method (Selection Object) if you write a macro.
* Author  
Posts

Viewing 8 posts - 1 through 8 (of 8 total)

* You must be logged in to reply to this topic.

<ins class="adsbygoogle"
     style="display:block"
     data-ad-format="autorelaxed"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="1223367746"></ins>

<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="8358498916"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>

<span class="atpl-alsoreadstyle">Also read:</span>
<div><ul>
<li><a href="https://tiktok-videos.techidaily.com/updated-2024-approved-commanding-attention-with-the-most-powerful-tiktok-caption-strategies/"><u>[Updated] 2024 Approved Commanding Attention with the Most Powerful TikTok Caption Strategies</u></a></li>
<li><a href="https://remote-screen-capture.techidaily.com/updated-elevating-your-podcast-game-mastering-video-and-audio-techniques-on-zoom/"><u>[Updated] Elevating Your Podcast Game Mastering Video and Audio Techniques on Zoom</u></a></li>
<li><a href="https://video-capture.techidaily.com/updated-the-full-laptop-screencapture-experience/"><u>[Updated] The Full Laptop ScreenCapture Experience</u></a></li>
<li><a href="https://android-pokemon-go.techidaily.com/3-ways-for-android-pokemon-go-spoofing-on-oppo-a38-drfone-by-drfone-virtual-android/"><u>3 Ways for Android Pokemon Go Spoofing On Oppo A38 | Dr.fone</u></a></li>
<li><a href="https://win-unique.techidaily.com/effective-strategies-for-configuring-amazon-s3-acls-enhancing-security-and-permission-control/"><u>Effective Strategies for Configuring Amazon S3 ACLs: Enhancing Security & Permission Control</u></a></li>
<li><a href="https://win-unique.techidaily.com/estrategias-efectivas-para-localizar-carpetas-perdidas-e-inconsultas-en-los-sistemas-operativos-windows-tanto-la-version-10-como-11/"><u>Estrategias Efectivas Para Localizar Carpetas Perdidas E Inconsultas en Los Sistemas Operativos Windows: Tanto La Versión 10 Como 11</u></a></li>
<li><a href="https://win-unique.techidaily.com/guida-passo-passo-per-eseguire-il-backup-dei-file-su-un-disco-rigido-esterno-in-windows-11/"><u>Guida Passo-Passo per Eseguire Il Backup Dei File Su Un Disco Rigido Esterno in Windows 11</u></a></li>
<li><a href="https://android-unlock.techidaily.com/in-2024-unlock-your-lava-storm-5gs-potential-the-top-20-lock-screen-apps-you-need-to-try-by-drfone-android/"><u>In 2024, Unlock Your Lava Storm 5Gs Potential The Top 20 Lock Screen Apps You Need to Try</u></a></li>
<li><a href="https://instagram-videos.techidaily.com/insta-growth-hacks-todays-essential-hashtags-guide/"><u>Insta Growth Hacks Today's Essential Hashtags Guide</u></a></li>
<li><a href="https://win-unique.techidaily.com/professionelle-methoden-zur-rettung-ihrer-dateien-auf-einem-formatierten-usb-stick/"><u>Professionelle Methoden Zur Rettung Ihrer Dateien Auf Einem Formatierten USB-Stick</u></a></li>
<li><a href="https://win-unique.techidaily.com/quick-fix-guide-how-to-successfully-move-all-pictures-from-an-iphone-1213/"><u>Quick Fix Guide: How to Successfully Move All Pictures From an iPhone 12/13</u></a></li>
<li><a href="https://win-unique.techidaily.com/restoring-lost-notes-from-notions-trash-bin-using-the-myrecover-app-a-step-by-step-guide/"><u>Restoring Lost Notes From Notion's Trash Bin Using the MyRecover App - A Step-by-Step Guide.</u></a></li>
<li><a href="https://buynow-reviews.techidaily.com/score-the-best-prices-exceptional-discounts-on-benq-display-equipment-prime-day-edition/"><u>Score the Best Prices: Exceptional Discounts on BenQ Display Equipment - Prime Day Edition</u></a></li>
<li><a href="https://games-able.techidaily.com/style-meets-substance-in-game-accessories/"><u>Style Meets Substance in Game Accessories</u></a></li>
<li><a href="https://win-unique.techidaily.com/tecnicas-efectivas-de-restauracion-de-documentos-borrados-en-sistemas-operativos-windows/"><u>Técnicas Efectivas De Restauración De Documentos Borrados en Sistemas Operativos Windows</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/15Ju8Cb4UZ8?si=5wdiQXdz1BOxIkDH" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

