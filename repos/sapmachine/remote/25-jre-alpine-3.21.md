## `sapmachine:25-jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:fc22ddb46c408930ac28bbd5a6388bab1b25aad7c02223e10b772afc7d25c05e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:25-jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:e6834bb4d95200658aa54b8c19a92f94349932d6dd5b561f9641053264f44b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72649468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ddb34d4b25bf09f4b162f13279786969b0b200de1bb795bf3c959aa3bebb033`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jre=25-r0 # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jre
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1799e0a9f2ef65c6b9f3eca01ac436cf65be343adf2d216a007f6e8c9403371`  
		Last Modified: Wed, 08 Oct 2025 23:20:38 GMT  
		Size: 69.0 MB (69006899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b4ef729a7ee47d84d0e57a2d42359aebbef2dba98c3df797fbb31fefe0d830bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.8 KB (437830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7a1ad745c5a5117a889e9f556a9fc36879e8c1629f841b8b0281b3d1a00270`

```dockerfile
```

-	Layers:
	-	`sha256:dbbcef64f602f5742083406df7615d0dbc635d182457cd66a4851e7eaa9443af`  
		Last Modified: Thu, 09 Oct 2025 00:07:28 GMT  
		Size: 430.5 KB (430520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f64db9eedcf6d95f33686af4e9baa4839d8a94947a981074e059263218e38246`  
		Last Modified: Thu, 09 Oct 2025 00:07:29 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.in-toto+json
