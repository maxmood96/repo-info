## `sapmachine:21-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:6b13945b35fa1c6c5f7d1e1dd4f78e4d87417d6f5cd73cdc99f23c9e6744b092
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:2ef51c7481178c61abbd8c2aeff6f11463dd672bdb426c8bd4c9e1973bb7ccf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89203079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc0ea408178bb51dd2fff6a957f8d4095aecb5a6bd270575819cb8b42f4e6ce`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4af2a641751dd64a4d635295ac50bf0b641dfb18748db45ecd5669369d3d4e9`  
		Last Modified: Wed, 16 Oct 2024 18:58:37 GMT  
		Size: 59.7 MB (59667391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:20c34c5952f821fe892527c29653ab1c3ce23a283cfa34a0253a28ddf3cb89b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2404705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7a10416b81c6531a339b24f4bf5a2502b905e393f18acd0f26be61b3200974`

```dockerfile
```

-	Layers:
	-	`sha256:7f6b118eec38ef8a684d9dc0ded505ea0a19fa2d99eff2bb47b1a1d15e314c81`  
		Last Modified: Wed, 16 Oct 2024 18:58:36 GMT  
		Size: 2.4 MB (2395441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acb81018d5ec9f80de272e727819fae635b553f76e75c96f497cc45bb53cdbdc`  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8189e498fc64861218379efbc8e851ed1eb092153e058c2af6448d71ff3e6a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86128003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815f2326232a7eb0e8bbd5b17fee8258dd46274ef0a193e2eca8ceeb7cf2d9e1`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c529c45fd23323fbc19aab17578acb43465c309f4755405d64222bb6fb1c8d85`  
		Last Modified: Wed, 16 Oct 2024 19:20:15 GMT  
		Size: 58.8 MB (58769674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1e4184f23b98cdb41d9019a8b2da96b25c6bb71d75dd0debf4b960e08b4659d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2404531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599306ad304aa4a5b136233d821fc898811fcbce5af27117979c6aa7252b3b3a`

```dockerfile
```

-	Layers:
	-	`sha256:4911733740bcd4698f6680500f47effee904636ddd6fb586ee33c15ea1f3b332`  
		Last Modified: Wed, 16 Oct 2024 19:20:13 GMT  
		Size: 2.4 MB (2395145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0553313dcf8ddea63ce1ea27ea9e97fe1c9da9c0cc620911265b7f2f196c3528`  
		Last Modified: Wed, 16 Oct 2024 19:20:13 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:53946b545784030144407a2daa618efccf3c82ce4257f61cb1c939a2b9aff662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95683953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9771d5b20c68833a25d2c00e02f64342740dc6e8f3b1818f1d3748656eabc0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dff85634cbb17e92359536e08e856793a8036c26d0d989dd5cb7f59de753ce3`  
		Last Modified: Wed, 16 Oct 2024 19:37:10 GMT  
		Size: 61.2 MB (61235711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b8eed027a4ccc95f2feb71ff58bf3bbdc09c1190a3feed99a925e0c5d853063a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2408746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79b1e56fa6af1c6ca70a928bdf5d8a54de13deb725a54ec492b6f374a485696`

```dockerfile
```

-	Layers:
	-	`sha256:21a1b4a34a2fa4e8574dc2adb270ca71adea685f127cbf1bf0d73f7cc9c63b24`  
		Last Modified: Wed, 16 Oct 2024 19:37:09 GMT  
		Size: 2.4 MB (2399432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0f709fef128c455ed4497cbfc842f27120f554ceb8aeda6ade7664a79cd4776`  
		Last Modified: Wed, 16 Oct 2024 19:37:08 GMT  
		Size: 9.3 KB (9314 bytes)  
		MIME: application/vnd.in-toto+json
