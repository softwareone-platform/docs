# Invitation

The Invitation Object enables vendors to create an invite.

<table><thead><tr><th width="158">Field Name</th><th width="133">Data Type</th><th>Description</th></tr></thead><tbody><tr><td>extension</td><td>object</td><td><p>The selected <a href="extension/">extension</a>. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "EXT-1111-1111",
    "href": "/extensions/EXT-1111-1111-1111",
    "name": "Adobe Acrobat",
    "icon": "/static/EXT-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td>message</td><td>string</td><td><p>Invitation message.  </p><p>Example: <code>To proceed with granting you access to the Adobe Acrobat extension, please use the invitation link. You’ll be prompted to redeem a code during installation – this is part of our approval process to ensure secure setup.</code></p></td></tr><tr><td>validity</td><td></td><td><p>Invite validity period. Possible values are:</p><ul><li>7d - seven days</li><li>1m - one month</li><li>3m - tree months</li><li>1y - one year</li></ul><p></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "period": "1m"
}
</code></pre></td></tr><tr><td>externalId</td><td>string</td><td><p>External Id correlated with invitation. </p><p>Example: 1256-8765-8456</p></td></tr><tr><td>url</td><td>string</td><td><p>Invitation code URL. </p><p>Example: <code>65221ec9-efa3-4d82-a155-6b01134c1651-3fd6222c-0cc0-4c3d-b128-4ab24f6b7bcc</code></p></td></tr></tbody></table>

### Example response <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
```json
 {
    "extension": {
      "id": "EXT-1111-1111",
      "href": "/extensions/EXT-1111-1111-1111",
      "name": "Adobe Acrobat",
      "icon": "/static/EXT-1111-1111/logo.png"
    },
    "message": "To proceed with granting you access to the Adobe Acrobat extension, please use the invitation link. You’ll be prompted to redeem a code during installation – this is part of our approval process to ensure secure setup.",
    "validity": "1m",    
    "externalId": "1256-8765-8456",
    "code": "65221ec9-efa3-4d82-a155-6b01134c1651-3fd6222c-0cc0-4c3d-b128-4ab24f6b7bcc ",
    ""
 }{
    "created": {
      "at": "2024-01-16T21:30:13.1046031",
      "by": {
        "id": "USR-0000-0001"
      }
    },
    "updated": null
  }
}
```
{% endcode %}
