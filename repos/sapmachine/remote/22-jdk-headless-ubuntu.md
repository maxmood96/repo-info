## `sapmachine:22-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:6e63adbba94f71e33599f0dd6ff2fe5d175462839daf775ca9de6ae3a6b813b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:dee8d4bf39c8c9100a23bd23ff434b3cc40920eff01f8db316b873bd184ac279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242313373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121564394fab0f469c4bebf2b01b9decaad4116df96bd6199fa52d71d10d71e7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808e08f294b829b8685025b94d35305507cbefbcfc898ae4f1f19cc26ee02d55`  
		Last Modified: Tue, 25 Jun 2024 22:57:42 GMT  
		Size: 212.6 MB (212608220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:949d2fe21c552a09ced6bb893f604ff82745c1cb3df74d427f15e41cf4f3b878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2196606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d34053513c2bf267adc85343dbdcfbe4aacf1f8d62e9dabea4fd5b90cb30297`

```dockerfile
```

-	Layers:
	-	`sha256:6e51b1872a205262c4193ceac8724f17c0cc426665d99188fd6268242f814252`  
		Last Modified: Tue, 25 Jun 2024 22:57:39 GMT  
		Size: 2.2 MB (2186214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b4f282498d52cf8fd9ec88a3828279c3804cb2edd1f982c1770c8eaf46372d8`  
		Last Modified: Tue, 25 Jun 2024 22:57:39 GMT  
		Size: 10.4 KB (10392 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2f6623ee16ce7dad49ff09d2057af20767867defc83ad8d4ee359e0a6b197481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239427841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541510d0a1df6796807010c9d324a37d144fce49e70d1ee57ec58823e8237764`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d6304826d7b1c8ac8fad88379a2f247ff5909e51af99f55a57683eed64ddeb`  
		Last Modified: Tue, 25 Jun 2024 23:51:27 GMT  
		Size: 210.6 MB (210584798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d63267d8cb7e0abbe7a1b996686397aac2e34a865d5e4529b113f17028ce34e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2196854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21afd808b0a87bceeabf396536a76c190b83416c70c2adf3e68a424de068eec6`

```dockerfile
```

-	Layers:
	-	`sha256:512a70b2d9817025539d687f1e2238437bf1776941561fc6184641374b56d759`  
		Last Modified: Tue, 25 Jun 2024 23:51:23 GMT  
		Size: 2.2 MB (2186101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0041b5a572eb14633d434cb065c01837ab3bdc3f8869948f9d2d1c19ffc3b396`  
		Last Modified: Tue, 25 Jun 2024 23:51:22 GMT  
		Size: 10.8 KB (10753 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1fa37dca2d5cf00d3b5205f54a8541270e992e13454abc9ea056273a80c05895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 MB (248125590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326a7d7eeb5c0f392149546f65f7f9f2b672e90f22ac3dcf143a22013aae8313`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecef3623019aac8f6507320c3cc8651c467b605b8590c18085e5368c0bd27266`  
		Last Modified: Wed, 26 Jun 2024 00:08:29 GMT  
		Size: 213.6 MB (213619561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a0e0627d1bea2318471008107a4d0de44dbcfddfd8f3cf28460671e2ed945b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2198010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0965bfce6110fd9906c5361aca8f1d49bac120f2a1b8786a88602042022a4c5`

```dockerfile
```

-	Layers:
	-	`sha256:819008076444af32300ba6bd6abf5cbd167638bf744a6a6ec9747e5a07cd9cc2`  
		Last Modified: Wed, 26 Jun 2024 00:08:24 GMT  
		Size: 2.2 MB (2187550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ea6bd2d30439180cddc317ea5003b6a44a1c5f2e523945860af4eb6615bd61c`  
		Last Modified: Wed, 26 Jun 2024 00:08:24 GMT  
		Size: 10.5 KB (10460 bytes)  
		MIME: application/vnd.in-toto+json
