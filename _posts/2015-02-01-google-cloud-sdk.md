---
layout: post
comments: yes
title: Cài đặt Google Cloud SDK
description: Google Cloud SDK chứa các công cụ và thư viện cho phép chúng ta dễ dàng tạo và quản lý tài nguyên trên Google Cloud Flatform...
tags: [google,cloud,sdk, zsh]
---

Google Cloud SDK chứa các công cụ và thư viện cho phép chúng ta dễ dàng tạo và quản lý tài nguyên trên Google Cloud Flatform: https://cloud.google.com/sdk/ 

Cài đặt trên Linux / Mac OS:
{% highlight bash %}
curl https://sdk.cloud.google.com | bash
{% endhighlight %}

Trước khi kết thúc cài đặt, chúng ta sẽ được hỏi có add Google Cloud SDK vào system path hay không, và có muốn enable chức năng command-line completion hay không. Nếu chọn yes thì install script sẽ thêm vào file .bash_profile đoạn sau:
{% highlight bash %}
# The next line updates PATH for the Google Cloud SDK.
source '/path/to/google-cloud-sdk/path.bash.inc'

# The next line enables bash completion for gcloud.
source '/path/to/google-cloud-sdk/completion.bash.inc'
{% endhighlight %}

Nếu máy bạn đang dùng zsh thay vì bash thì phải tự sửa file .zshrc:
{% highlight bash %}
# The next line updates PATH for the Google Cloud SDK.
source '/path/to/google-cloud-sdk/path.zsh.inc'

# The next line enables bash completion for gcloud.
source '/path/to/google-cloud-sdk/completion.zsh.inc'
{% endhighlight %}

Nếu có dùng Oh-my-zsh thì phải đưa đoạn update PATH lên trước dòng lệnh: {% ihighlight bash %}source $ZSH/oh-my-zsh.sh{% endihighlight %}
{% highlight bash %}
# The next line updates PATH for the Google Cloud SDK.
source '/Users/thiendev1337/google-cloud-sdk/path.zsh.inc'

source $ZSH/oh-my-zsh.sh

# The next line enables bash completion for gcloud.
source '/path/to/google-cloud-sdk/completion.zsh.inc'
{% endhighlight %}