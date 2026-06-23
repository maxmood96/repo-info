## `sapmachine:jre-alpine-3.22`

```console
$ docker pull sapmachine@sha256:9c6944a2cbb4f38133effe5a2db6c6e36b0fcbbcd9e459941c0e3998117cccc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:jre-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:9bfd2995e00414408af6fb22359d4ba495958759c16451d945cb9d7720c3c227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63126004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3b85e0eb36303eeac69a4b8ba85c87fd457d4ce03910e751e470858d99aa9d`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:08:02 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-26-jre=26.0.1-r0 # buildkit
# Mon, 22 Jun 2026 20:08:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-sapmachine-jre
# Mon, 22 Jun 2026 20:08:02 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700dfaa455cef0cfaf3a9c0792761e55424f6d934ef85d4d0bd585fa478de069`  
		Last Modified: Mon, 22 Jun 2026 20:08:14 GMT  
		Size: 59.3 MB (59338409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fc2492bb1e38f75319fc5d30ffb8a5b5eef51cb1596c6ba4e995e32a6f9c4add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 KB (437503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9068a1a17e2424c6843e97a3d9a9fc2da4aa6636c90d8b00270960ef75859db`

```dockerfile
```

-	Layers:
	-	`sha256:295de21c37a70420fa2cadbb7aa5e0a4b7942e52ff7915de420f7a9ce2f74f43`  
		Last Modified: Mon, 22 Jun 2026 20:08:12 GMT  
		Size: 430.2 KB (430222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac94f7d3ec5a4ec275c13aef74c1826f165924e55ef79f4edaea820e2c7a91bf`  
		Last Modified: Mon, 22 Jun 2026 20:08:12 GMT  
		Size: 7.3 KB (7281 bytes)  
		MIME: application/vnd.in-toto+json
