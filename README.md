# derpdown
vue js dropdown

### usage:
use `slot="toggle"` and `slot="content"` inside the `<derpdown>` tags
```
<derpdown :align_right=true>
    <a slot="toggle">
        Derpdown toggle
    </a>
    <div slot="content">
        Derpdown toggleable content
    </div>
</derpdown>
```


##### the html inside toggle and content slots can be anything
bulma css example:
```
<derpdown :align_right=true>
    <a slot="toggle" class="px-sm is-large is-white button">
        <figure class="image is-circle is-32x32">
            <img :src="avatar_url"></img>
        </figure>
        <span class="icon">
            <i class="fa fa-angle-down"></i>
        </span>
    </a>
    <div slot="content" class="box">
        <aside class="menu">
            <p class="menu-label" v-text="name"></p>
            <hr>
            <ul class="menu-list">
                <li><a href="settings">Settings</a></li>
                <li><a href="auth/logout">Logout</a></li>
            </ul>
        </aside>
    </div>
</derpdown>

```
