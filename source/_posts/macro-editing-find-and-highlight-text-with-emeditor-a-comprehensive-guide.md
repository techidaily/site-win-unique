---
title: "Macro Editing: Find & Highlight Text with EmEditor - A Comprehensive Guide"
date: 2024-11-02T21:51:40.765Z
updated: 2024-11-03T18:11:08.591Z
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
<li><a href="https://instagram-videos.techidaily.com/new-2024-approved-galleryguide-adjusting-post-dimensions-in-instagram/"><u>[New] 2024 Approved GalleryGuide Adjusting Post Dimensions in Instagram</u></a></li>
<li><a href="https://fox-hovers.techidaily.com/new-in-2024-kid-friendly-quadcopters-top-5-selection-guide/"><u>[New] In 2024, Kid-Friendly Quadcopters Top 5 Selection Guide</u></a></li>
<li><a href="https://video-capture.techidaily.com/new-in-2024-unlocking-freenocams-webcam-capturing-capabilities/"><u>[New] In 2024, Unlocking FreenoCam's Webcam Capturing Capabilities</u></a></li>
<li><a href="https://fox-info.techidaily.com/updated-2024-approved-a-comprehensive-guide-to-professional-level-video-editing-on-windows-11/"><u>[Updated] 2024 Approved A Comprehensive Guide to Professional-Level Video Editing on Windows 11</u></a></li>
<li><a href="https://instagram-videos.techidaily.com/updated-2024-approved-detecting-instagram-disconnections-fast/"><u>[Updated] 2024 Approved Detecting Instagram Disconnections Fast</u></a></li>
<li><a href="https://instagram-clips.techidaily.com/2024-approved-from-chords-to-clicks-mastering-music-on-ig/"><u>2024 Approved From Chords to Clicks Mastering Music on IG</u></a></li>
<li><a href="https://win-unique.techidaily.com/1728499822610-windows-10/"><u>遭逢 Windows 10 更新失敗？給你最有效的修正方法列表</u></a></li>
<li><a href="https://win-unique.techidaily.com/comprehensive-tutorial-harnessing-usmt-for-seamless-migration-to-windows-11-plus-a-viable-substitute/"><u>Comprehensive Tutorial: Harnessing USMT for Seamless Migration to Windows 11 - Plus a Viable Substitute!</u></a></li>
<li><a href="https://win-unique.techidaily.com/effective-strategies-for-configuring-amazon-s3-acls-enhancing-security-and-permission-control/"><u>Effective Strategies for Configuring Amazon S3 ACLs: Enhancing Security & Permission Control</u></a></li>
<li><a href="https://fox-info.techidaily.com/in-2024-how-many-seconds-is-a-20mb-video/"><u>In 2024, How Many Seconds Is a 20Mb Video</u></a></li>
<li><a href="https://sim-unlock.techidaily.com/in-2024-how-to-unlock-iphone-11-pro-max-online-here-are-6-easy-ways-by-drfone-ios/"><u>In 2024, How to Unlock iPhone 11 Pro Max Online? Here are 6 Easy Ways</u></a></li>
<li><a href="https://win-unique.techidaily.com/1728477243501-pc/"><u>PCスタックが止まった時の効果的なリカバリ手順 - 衝突を回避する戦略</u></a></li>
<li><a href="https://win-unique.techidaily.com/should-you-perform-a-bios-update-prior-to-upgrading-to-windows-11/"><u>Should You Perform a BIOS Update Prior to Upgrading to Windows 11?</u></a></li>
<li><a href="https://blog-min.techidaily.com/unlock-the-secrets-to-retaining-excellence-while-compressing-your-mp4-files/"><u>Unlock the Secrets to Retaining Excellence While Compressing Your MP4 Files</u></a></li>
<li><a href="https://win-unique.techidaily.com/wiederherstellung-des-papierkorbs-in-windows-10-ein-umfassender-tippgeber/"><u>Wiederherstellung Des Papierkorbs in Windows 10: Ein Umfassender Tippgeber</u></a></li>
<li><a href="https://win-unique.techidaily.com/1728508827007-windows-1011-3/"><u>Windows 10/11の初期化: 起動問題に対する3手ソリューション</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://malaysia-healthcare-travel-council.pxf.io/c/5597632/1576477/17382" target="_top" id="1576477">
  <img src="//a.impactradius-go.com/display-ad/17382-1576477" border="0" alt="https://techidaily.com" width="160" height="90"/>
</a>
<img height="0" width="0" src="https://malaysia-healthcare-travel-council.pxf.io/i/5597632/1576477/17382" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

