## `sapmachine:lts-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:d269d52d0a22d6458f299d1ec2869cd8fb1fb1ffd4ceb8648fe50dad1052be25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:180db0092652551fcfffb8dada755e93c9798cf8ed7990d0ff7eac54da776387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90032393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6ce2731d15f784c2ac2e66ec7f7c7225e6f3e81f7c50c10492973e462a4ed1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707b9f8579bbf6cee9c8b99047b1d7b5064874032e9734b1b54ea05125e02326`  
		Last Modified: Fri, 19 Jul 2024 18:00:13 GMT  
		Size: 60.3 MB (60327240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:960c2ac67e646eeab1537a9e27b78ae2d57caf5d1ea6b2689984a48fdc37ded1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc42a983eae90dece481e96b3f476cbc892888f1201c7e620e5bc6d793cb394`

```dockerfile
```

-	Layers:
	-	`sha256:15bd907c2770b1f7dbbefe24d110efd461c9e49dccbc5123f8e34af7d9f61c94`  
		Last Modified: Fri, 19 Jul 2024 18:00:13 GMT  
		Size: 2.4 MB (2363084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9ef0ed94b5dc973ff7388f01bc4a7d860b716d4d12562800626ebec97332b15`  
		Last Modified: Fri, 19 Jul 2024 18:00:13 GMT  
		Size: 10.2 KB (10196 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:327b41cae6798a0b4036d17368e43bb52c23f8e0498a1be13143e05c76718fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88208359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdfbae48768dba0cfbf5da51738de8eab79880e37ec2121782429fb31e273d70`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacecb7848c61b10ec23031360a18b2b9f1ff00927eb700f9e7b9e6ef5db42df`  
		Last Modified: Wed, 26 Jun 2024 00:04:55 GMT  
		Size: 59.4 MB (59365316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:230a6a1637a6f5d982b6abfb4cba4e14b6b0edcb48df1f6d675cb825f5293c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2346739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3861d60d15a5562ec988381a1b36b06ce5de28d214474c03f3c11a2f1b4ce0f4`

```dockerfile
```

-	Layers:
	-	`sha256:1fc1c481ff8ee8b779d3dbc3ed81d5a72ab0b199fa30c13cca0032e159bd8945`  
		Last Modified: Wed, 26 Jun 2024 00:04:53 GMT  
		Size: 2.3 MB (2336165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd3b3a47c6dd8fad47c3bfce66aa84d99120f2f39c5c6c488025cac8b1b6f381`  
		Last Modified: Wed, 26 Jun 2024 00:04:53 GMT  
		Size: 10.6 KB (10574 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:cab5229214bfebc2711ad92454ef363bc4dcb038df0107d2e77097e83a8e7031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96460644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975fba314106fe0f824218c6695155a2557cdddfef5bd77a15d9fdad91cf8550`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712430a2058ee81ac6cd8fe19fae1844486337a13920098b462858b30b85f272`  
		Last Modified: Wed, 26 Jun 2024 00:30:12 GMT  
		Size: 62.0 MB (61954615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f1ab6b1c5499d91f3ac730f8e45cf9b52c35013c8f941fcfc8f9b4e163aa91bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2349887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7bbc29c690ba52359ef7fe191cc56e8378a40e32e5c6dfd7005f448c6c5428`

```dockerfile
```

-	Layers:
	-	`sha256:4aa8ada83acbd521eb2862db3c11d15d21fda84451799cdabdfba1f7f2773c5d`  
		Last Modified: Wed, 26 Jun 2024 00:30:09 GMT  
		Size: 2.3 MB (2339605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c93eaab090696a3735e2fba6f84fca83f33d5311e4c302193b5856da0fa1324`  
		Last Modified: Wed, 26 Jun 2024 00:30:09 GMT  
		Size: 10.3 KB (10282 bytes)  
		MIME: application/vnd.in-toto+json
