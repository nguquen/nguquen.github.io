---
layout: post
comments: yes
title: Gõ tiếng Việt trong sublime trên linux
description: Sublime Text&#58; 'BoGo, you complete me &#58;3'. Gõ tiếng Việt trong sublime trên linux chưa bao giờ thuận tiện và dễ dàng hơn...
tags: [sublime, bogo]
---

Gõ tiếng Việt trong sublime từng gặp khó khăn trên linux vì nó không hỗ trợ bộ gõ ibus, 1 số chiêu giang hồ từng sử dụng để gõ được tiếng Việt, như:

- Plugin [InputHelper](https://github.com/xgenvn/InputHelper): plugin này sẽ bật 1 popup nhỏ chứa 1 textbox cũng nho nhỏ để người dùng gõ tiếng Việt vào, sau đó mới insert vào sublime, khá là bất tiện.

- Plugin [VN_IME](https://github.com/yehnkay/VN_IME): plugin này bắt sự kiện modified nội dung và thực hiện việc bỏ dấu tiếng Việt bằng thuật toán riêng, đây cũng chính là nhược điểm của plugin này vì thuật toán chưa hoàn thiện, có nhiều lỗi phát sinh.

##### Sublime Text: 'BoGo, you complete me :3'

Gõ tiếng Việt trong Sublime Text với plugin [Sublime-Bogo](https://github.com/pirackr/Sublime-Bogo): Trên list issue của [VN_IME](https://github.com/yehnkay/VN_IME) có 1 bạn đề nghị dùng bogo-python để xử lý việc bỏ dấu tiếng Việt nhưng tác giả chưa thực hiện. Lúc này trong đầu mình đang nhen nhóm ý tưởng viết 1 plugin riêng cho sublime dùng engine bogo-python :sure:, nhưng trước khi start mình google 1 lượt để tránh trùng ý tưởng với người khác, và không biết nên vui mừng hay cụt hứng khi mình tìm ra plugin [Sublime-Bogo](https://github.com/pirackr/Sublime-Bogo), theo commit log thì plugin này chỉ mới được phát triển cách đây 1 tháng :3. Hý hửng cài thử và kết quả... thật toẹt vời, post này được mình viết trên sublime sử dụng [Sublime-Bogo](https://github.com/pirackr/Sublime-Bogo) để gõ tiếng Việt nhá nhá :3. Gõ tiếng Việt trong sublime trên linux chưa bao giờ thuận tiện và dễ dàng hơn :sexy:

##### Có thể bạn biết rồi, cách cài plugin cho sublime text:

##### Cài Package Control:

###### 1. Mở Sublime Text Console:

{% highlight pycon %}ctrl+`{% endhighlight %}

###### 2. Tùy vào Sublime Text 2/3 mà dán và chạy đoạn code tương ứng:

- Sublime Text 2

{% highlight pycon %}
import urllib2,os,hashlib; h = '7183a2d3e96f11eeadd761d777e62404' + 'e330c659d4bb41d3bdf022e94cab3cd0'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); os.makedirs( ipp ) if not os.path.exists(ipp) else None; urllib2.install_opener( urllib2.build_opener( urllib2.ProxyHandler()) ); by = urllib2.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); open( os.path.join( ipp, pf), 'wb' ).write(by) if dh == h else None; print('Error validating download (got %s instead of %s), please try manual install' % (dh, h) if dh != h else 'Please restart Sublime Text to finish installation')
{% endhighlight %}

- Sublime Text 3

{% highlight pycon %}
import urllib.request,os,hashlib; h = '7183a2d3e96f11eeadd761d777e62404' + 'e330c659d4bb41d3bdf022e94cab3cd0'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
{% endhighlight %}

##### Cài Sublime-Bogo:

- Mở Package Control bằng phím tắt: ctrl + shift + p

- Chọn Package Control: Install Package

- Search BoGo và cài đặt :3