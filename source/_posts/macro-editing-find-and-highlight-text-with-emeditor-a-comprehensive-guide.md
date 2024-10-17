---
title: "Macro Editing: Find & Highlight Text with EmEditor - A Comprehensive Guide"
date: 2024-10-15T17:15:26.759Z
updated: 2024-10-17T16:45:44.036Z
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
<li><a href="https://facebook-video-share.techidaily.com/new-elevate-your-content-visibility-discover-6-thumbnail-designers-best-tools-for-2024/"><u>[New] Elevate Your Content Visibility - Discover 6 Thumbnail Designers' Best Tools for 2024</u></a></li>
<li><a href="https://snapchat-videos.techidaily.com/new-in-2024-how-to-keep-up-the-snapstreak-game/"><u>[New] In 2024, How To Keep Up the Snapstreak Game</u></a></li>
<li><a href="https://desktop-recording.techidaily.com/updated-global-elite-top-12-tools-with-no-time-limit/"><u>[Updated] Global Elite Top 12 Tools With No Time Limit</u></a></li>
<li><a href="https://buynow-help.techidaily.com/comparative-breakdown-why-apples-m1-powered-mac-mini-outshines-its-rivals/"><u>Comparative Breakdown: Why Apple's M1 Powered Mac Mini Outshines Its Rivals</u></a></li>
<li><a href="https://win-unique.techidaily.com/comprehensive-guide-retrieving-deleted-information-on-a-sony-vaio-computer-system/"><u>Comprehensive Guide: Retrieving Deleted Information on a Sony Vaio Computer System</u></a></li>
<li><a href="https://win-unique.techidaily.com/guia-completa-como-rescatar-tu-computadora-con-un-restablecimiento-del-estado-inicial-en-windows-cuenta-10/"><u>Guía Completa: Cómo Rescatar Tu Computadora Con Un Restablecimiento Del Estado Inicial en Windows Cuenta 10</u></a></li>
<li><a href="https://driver-error.techidaily.com/how-to-overcome-access-denied-when-setting-up-a-new-usb-device/"><u>How to Overcome 'Access Denied' When Setting Up a New USB Device</u></a></li>
<li><a href="https://extra-approaches.techidaily.com/mastering-full-rotation-shoots-9-must-follow-rules-for-2024/"><u>Mastering Full-Rotation Shoots 9 Must-Follow Rules for 2024</u></a></li>
<li><a href="https://win-unique.techidaily.com/story-3-the-skip-lesions-misconception/"><u>Story 3: The Skip Lesions Misconception</u></a></li>
<li><a href="https://win-unique.techidaily.com/unable-to-locate-webpage-error-code-404-displayed/"><u>Unable to Locate Webpage: Error Code 404 Displayed</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://25home.pxf.io/c/5597632/2148637/16836" target="_top" id="2148637">
  <img src="//a.impactradius-go.com/display-ad/16836-2148637" border="0" alt="https://techidaily.com" width="125" height="90"/>
</a>
<img height="0" width="0" src="https://25home.pxf.io/i/5597632/2148637/16836" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

