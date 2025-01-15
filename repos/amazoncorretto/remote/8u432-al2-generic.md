## `amazoncorretto:8u432-al2-generic`

```console
$ docker pull amazoncorretto@sha256:84b6ea3dec3e59a9223a3be5c575c74f8229980ed21a9abf88b3f7b446965d21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u432-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:93eb19ae0cb47c2c143abe2c1ab8a8dd9452898814458d52791da82b86cd09ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138198357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbe03af79e677cd58825124ca259ad4c6e510b92e1790d99e00dd4f08b38e57`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=1.8.0_432.b06-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Fri, 10 Jan 2025 22:01:24 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41f411e0d334645f31261059c924866a66afcdef7098bc359491a78469d619f`  
		Last Modified: Tue, 14 Jan 2025 20:45:44 GMT  
		Size: 75.6 MB (75562527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2dfcc0e18869bd0274f52cfb6d69b2b26be2dc092a3a06c5b77d87d723cedd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90a5aa61a99692edff1a7f8b5bea460dd330ae00becd37008188470b449d7fb`

```dockerfile
```

-	Layers:
	-	`sha256:9a43307194e7d84c1dc2e7479ff97cd58253ccd5db18239c05c950c66d9f691e`  
		Last Modified: Sat, 11 Jan 2025 02:29:07 GMT  
		Size: 5.4 MB (5359564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78416cf9d605670ec874ff9ee09d5a7ba24dcf8486e447fabcf79bab0a223c1b`  
		Last Modified: Sat, 11 Jan 2025 02:29:07 GMT  
		Size: 11.6 KB (11570 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u432-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0e3e442f365b1f33087e3c4de3fccaeab41d135b0e4e9541b29717d62f401b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124259731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218b88c42146fa56014d8e9f9fcd08ed272dbeb327bcd54f6c110478207731aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=1.8.0_432.b06-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Tue, 14 Jan 2025 20:35:27 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ee146c9a56ad020ab6e742508a6b4173854c4d74cac5e45ed0ba7c5de719c6`  
		Last Modified: Sat, 11 Jan 2025 02:55:45 GMT  
		Size: 59.7 MB (59669426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4c737fd5f133f29ddf13476297f5d1cf101ce2261862d2158cec1a96fc69b64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5349797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dd1497791151782c879a6a6b79fadf10fabcdaa42e25bfdb822f589cbdade9`

```dockerfile
```

-	Layers:
	-	`sha256:d98bc1eb27876b69b9ff5e1b7dcea563cffd6771f9281c26368334b54a15fa86`  
		Last Modified: Tue, 14 Jan 2025 22:29:45 GMT  
		Size: 5.3 MB (5338063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53a389ca23b2fc6171be115589a079d314456b2a0c18bf3f0caf62c5722d8537`  
		Last Modified: Tue, 14 Jan 2025 22:30:03 GMT  
		Size: 11.7 KB (11734 bytes)  
		MIME: application/vnd.in-toto+json
