We do not store/save your data in any way. The data gets processed and, once you log-out, it disappears from our servers. We have no way of looking at your data. We take this very seriously.  

> *We do not store any kind of user data in any way. Your uploaded file is never stored or saved on disk and is fully discarded from RAM after being processed and/or when you close your session. We secure our servers by implementing hardening [best practices.](https://www.cisecurity.org/)*
>
> *We cache the data while a session is active to improve performance. We clear the Streamlit cache automatically after 30 minutes.*
>
> *We do not collect user statistics of any kind: no cookies, no Google Analytics, no trackers, no nothing.*
>
> *We use Streamlit.io services to render our python application. Cookie banners are required in the EU when a website uses cookies for analytics/performance or tracking/marketing. Streamlit services do not use such cookies, which is why we do not have a cookie banner.*

![security](assets/images/security.png)

Our application is developed using Streamlit. As the name implies, Streamlit uses "streams". In their words:

>  *Streamlit isn’t saving your file anywhere. The file uploader takes the stream of bytes coming from the widget and saving it in RAM (like any other piece of data). By not writing to disk, you’re removing a step which takes time, so you’re improving performance.*
>
> *The data lives on until the Streamlit app re-runs from top-to-bottom, which is on each widget interaction.*
>
> *Files are stored in memory (i.e. RAM, not disk), and they get deleted immediately as soon as they’re not needed anymore.*
>
> *This means we remove a file from memory when:*
>
> - *The user uploads another file, replacing the original one*
> - *The user clears the file uploader*
> - *The user closes the browser tab where they uploaded the file*



