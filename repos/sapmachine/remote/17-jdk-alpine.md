## `sapmachine:17-jdk-alpine`

```console
$ docker pull sapmachine@sha256:4e54c9b67bb9f8a2a629c5722f63e476dd5eb9fc243c0495c42ca50c45dc52b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jdk-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:77daf65236cf992a1ff2d5141dd002488d11aba33918ce2c0bd80075997e1306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.2 MB (206151702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b138e6863dab1447ac9c7c55c83a91fb974a97f399696899e737c3f4ce8a56a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 20:04:58 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jdk=17.0.18-r0 # buildkit
# Wed, 21 Jan 2026 20:04:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jdk
# Wed, 21 Jan 2026 20:04:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28eb907fecd64ef4f6e1ef8090f905db0405752b5058aba868c9f3b592dbd107`  
		Last Modified: Wed, 21 Jan 2026 20:05:19 GMT  
		Size: 202.3 MB (202349250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:24404b5e8191d59cea760cd515e28475d4d87716d423106e144210d2e88cb440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.3 KB (520266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a864b31cb9324ebe1db54a42a8c34cd5989b1b9e835532b5227f6df9e2b5496d`

```dockerfile
```

-	Layers:
	-	`sha256:e61c0fa3f1d2837b1e799c1f2d14bf0d4aed61bbf191ff55c2b66efb84a5e65b`  
		Last Modified: Wed, 21 Jan 2026 20:05:14 GMT  
		Size: 511.4 KB (511359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0796b455af38786d1b2f2aae1fc9c66fe75628afe01d76f9c2933da08dea13b6`  
		Last Modified: Wed, 21 Jan 2026 22:06:27 GMT  
		Size: 8.9 KB (8907 bytes)  
		MIME: application/vnd.in-toto+json
