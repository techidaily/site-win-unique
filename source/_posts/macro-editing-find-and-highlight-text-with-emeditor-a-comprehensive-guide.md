---
title: "Macro Editing: Find & Highlight Text with EmEditor - A Comprehensive Guide"
date: 2024-10-07T08:25:36.171Z
updated: 2024-10-11T10:32:06.840Z
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
<li><a href="https://article-knowledge.techidaily.com/new-2024-approved-calculating-gb-in-one-days-movie-duration/"><u>[New] 2024 Approved Calculating GB in One Day's Movie Duration</u></a></li>
<li><a href="https://facebook-video-recording.techidaily.com/new-2024-approved-unveil-secrets-to-speedy-caption-design-in-facebook-media/"><u>[New] 2024 Approved Unveil Secrets to Speedy Caption Design in Facebook Media</u></a></li>
<li><a href="https://youtube-data.techidaily.com/ed-online-aggregators-for-securing-affiliates-on-googles-platform/"><u>[Updated] Online Aggregators for Securing Affiliates on Google's Platform</u></a></li>
<li><a href="https://extra-resources.techidaily.com/fast-track-photo-and-video-editing-via-mobile-luts/"><u>Fast-Track Photo & Video Editing via Mobile LUTs</u></a></li>
<li><a href="https://easy-unlock-android.techidaily.com/how-to-unlock-nokia-c210-phone-password-without-factory-reset-by-drfone-android/"><u>How to Unlock Nokia C210 Phone Password Without Factory Reset?</u></a></li>
<li><a href="https://bypass-frp.techidaily.com/in-2024-how-to-bypass-frp-from-realme-narzo-n53-by-drfone-android/"><u>In 2024, How to Bypass FRP from Realme Narzo N53?</u></a></li>
<li><a href="https://extra-lessons.techidaily.com/leveraging-xml-and-ttml-for-cutting-edge-srt-creation-processes/"><u>Leveraging XML & TTML for Cutting-Edge SRT Creation Processes</u></a></li>
<li><a href="https://win-unique.techidaily.com/stay-on-the-safe-side-why-skip-windows-11-and-what-to-use-in-its-place-tech-advice-hub/"><u>Stay on the Safe Side: Why Skip Windows 11 and What to Use in Its Place | Tech Advice Hub</u></a></li>
<li><a href="https://fox-info.techidaily.com/step-by-step-live-stream-via-network-in-vlc-for-2024/"><u>Step-by-Step Live Stream via Network in VLC for 2024</u></a></li>
<li><a href="https://win-unique.techidaily.com/step-by-step-tutorial-building-a-flawless-windows-11-virtual-environment/"><u>Step-by-Step Tutorial: Building a Flawless Windows 11 Virtual Environment</u></a></li>
<li><a href="https://win-unique.techidaily.com/stuck-with-an-older-os-and-considering-windows-11-try-this-wise-move-tips-from-zdnet/"><u>Stuck with an Older OS and Considering Windows 11? Try This Wise Move | Tips From ZDNet</u></a></li>
<li><a href="https://win-unique.techidaily.com/the-importance-of-a-trusted-platform-module-tpm-for-windows-11-compatibility-and-security-explained/"><u>The Importance of a Trusted Platform Module (TPM) for Windows 11 Compatibility and Security Explained</u></a></li>
<li><a href="https://win-unique.techidaily.com/top-ranking-laptops-and-desktops-comparing-apple-dell-and-other-brands-insights-from-zdnet/"><u>Top-Ranking Laptops & Desktops : Comparing Apple, Dell, and Other Brands - Insights From ZDNet</u></a></li>
<li><a href="https://win-unique.techidaily.com/uncover-advanced-trackpad-hacks-for-pc-pros-essential-tips-you-cant-afford-to-miss/"><u>Uncover Advanced TrackPad Hacks for PC Pros! Essential Tips You Can't Afford to Miss</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2130871/7443" target="_top" id="2130871">
  <img src="//a.impactradius-go.com/display-ad/7443-2130871" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2130871/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

