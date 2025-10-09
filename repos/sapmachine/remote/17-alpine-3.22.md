## `sapmachine:17-alpine-3.22`

```console
$ docker pull sapmachine@sha256:461bbc5e9a10bea2b45f9724903e8f1fc25f64e6d7ff2bd346100d3d7b7f8d21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:1f6a92f0bf4bd29baeed94bcfc2c6970b5d696dfa11d4a2def9bf98f4f66f6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204875512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52180f611a1791e05001213604ef651f974aa60539b59e1ced28ae65025a0d44`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:35 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 06:09:35 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add nss sapmachine-17-jdk=17.0.16-r0 # buildkit
# Mon, 11 Aug 2025 06:09:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jdk
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9c1fe58840ce91b2630e66dc3284ab0c4940bb9360715a059c63a8b0c05cd6`  
		Last Modified: Thu, 09 Oct 2025 00:05:34 GMT  
		Size: 201.1 MB (201073060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4d3abd4e5aa5396f60fdaafe7f6ff37b842cfb16b20dde77382527d8b4c0647d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.5 KB (516509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefdd6445e8a3a0c0684cf5d10fc009129f4d345673bd5bd18bd25b30d12f7c3`

```dockerfile
```

-	Layers:
	-	`sha256:71aabc6f8baf335759224683bfdc9a34d2997a28675554d0c3adceea6bdbcc1b`  
		Last Modified: Thu, 09 Oct 2025 00:04:34 GMT  
		Size: 507.6 KB (507551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:866ec4b568d067133f28ed33ea0e8772e43f5a462a2b0464bf3dc626c78b774b`  
		Last Modified: Thu, 09 Oct 2025 00:04:34 GMT  
		Size: 9.0 KB (8958 bytes)  
		MIME: application/vnd.in-toto+json
