## `sapmachine:17-jre-alpine-3.23`

```console
$ docker pull sapmachine@sha256:ccf6eaa47542b36c4bd5cab8ef8d580c02d97c4f2da07b53f3f1814184e245b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jre-alpine-3.23` - linux; amd64

```console
$ docker pull sapmachine@sha256:1764a3929c35a6b09a9b0d694cc551d7adcf09d8ee7f89d8595ab3a5545e5502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59277755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b8605b10b586dd2cf016146cb43c5f654698f6a60e8bbd42185032e685db40`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Mar 2026 17:50:59 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jre=17.0.18-r0 # buildkit
# Wed, 18 Mar 2026 17:50:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jre
# Wed, 18 Mar 2026 17:50:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c287b11df0442b63e0b38bfda9b806e9bfd62f7b16480aedf70883352e30b3d`  
		Last Modified: Wed, 18 Mar 2026 17:51:11 GMT  
		Size: 55.4 MB (55415934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-alpine-3.23` - unknown; unknown

```console
$ docker pull sapmachine@sha256:91b5c0cc58d80700ac0b1cf8ca9f0c13d3491e093615b39d3b616bac4a96b0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.2 KB (434235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2243e0d72ababee897c0b76450cb8164d3b1b3d252fe28372bd0d945524aaea7`

```dockerfile
```

-	Layers:
	-	`sha256:1ca5423db319777cc5fcd49c1f8c18bf26c8b4df79dfd3fa2a3f59c218f1ce82`  
		Last Modified: Wed, 18 Mar 2026 17:51:09 GMT  
		Size: 426.6 KB (426625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe6651e6d5e529d70e8b0dbe41000716a0c3c045bc1d5ffbd8c5c2da32a2d218`  
		Last Modified: Wed, 18 Mar 2026 17:51:09 GMT  
		Size: 7.6 KB (7610 bytes)  
		MIME: application/vnd.in-toto+json
