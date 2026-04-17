## `sapmachine:jre-alpine-3.22`

```console
$ docker pull sapmachine@sha256:f696d2ef1fec0c61d423f0ca5f0f5939b045d7159aac7bae26370f20fc4516f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:jre-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:d73b99635614b7e2355efb17642cceda01e22eddfda4ff8c5f5d2cfbb34285a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63145592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c38b84dd0ca5f332cef0cdef04800353dc06aad99a1eadf4069cc466ed8bf1`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:33:35 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-26-jre=26-r0 # buildkit
# Fri, 17 Apr 2026 00:33:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-sapmachine-jre
# Fri, 17 Apr 2026 00:33:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad93db08c82aa74be14989b55994ec44da0e9265872d57442784676f03e5bf4`  
		Last Modified: Fri, 17 Apr 2026 00:33:47 GMT  
		Size: 59.3 MB (59337403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:da13cbb21141299b95f540d256ee0a9433b5db5ed1674c705d5c6c75f82f10ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.8 KB (436798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c875816aa5d1610a1deb3bd3ae37f2f48de8bb3b46a30615397d822df654024`

```dockerfile
```

-	Layers:
	-	`sha256:3256d13ea906ca8c26fbdfe3375031a4d4d95cda2ebf6b98c963fe50b8a97edb`  
		Last Modified: Fri, 17 Apr 2026 00:33:45 GMT  
		Size: 429.9 KB (429863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36e4d8fec38a39bdb07c3851ea7f3503b00418f3de4a1f25b174bdc6dcfedeb0`  
		Last Modified: Fri, 17 Apr 2026 00:33:45 GMT  
		Size: 6.9 KB (6935 bytes)  
		MIME: application/vnd.in-toto+json
