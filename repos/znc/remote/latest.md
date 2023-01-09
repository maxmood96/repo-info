## `znc:latest`

```console
$ docker pull znc@sha256:0baf3bfccf1622e4db41a685579c6c6705bc2de1a5a27a95fc270275d37f2268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:latest` - linux; amd64

```console
$ docker pull znc@sha256:91a3784e46f1a4376ebf74b6dbfb2c45cf8fa030fcf400de5f4cf33fb713a8e3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164440628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6ab9586a38d110a20e4d13e7ba6762883e099833040798face404ff63453c4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:20 GMT
ADD file:e4d600fc4c9c293efe360be7b30ee96579925d1b4634c94332e2ec73f7d8eca1 in / 
# Mon, 09 Jan 2023 17:05:20 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 21:22:10 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Mon, 09 Jan 2023 21:22:10 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Mon, 09 Jan 2023 21:22:10 GMT
ARG MAKEFLAGS=
# Mon, 09 Jan 2023 21:22:10 GMT
ENV ZNC_VERSION=1.8.2
# Mon, 09 Jan 2023 21:26:08 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Mon, 09 Jan 2023 21:26:09 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Mon, 09 Jan 2023 21:26:09 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Mon, 09 Jan 2023 21:26:09 GMT
VOLUME [/znc-data]
# Mon, 09 Jan 2023 21:26:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Jan 2023 21:26:25 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Mon, 09 Jan 2023 21:26:26 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:8921db27df2831fa6eaa85321205a2470c669b855f3ec95d5a3c2b46de0442c9`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.4 MB (3370628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5d8b6b37f44d57259bb006f9b65889c6ea03ea64b4b515a3118d3a41bc8aa5`  
		Last Modified: Mon, 09 Jan 2023 21:26:46 GMT  
		Size: 46.6 MB (46571031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db57db500d6df1351587e84950e21dc0dc36ebf2be1bcfaa4704180210b8b068`  
		Last Modified: Mon, 09 Jan 2023 21:26:38 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291cbdb197592e1d29922f57158268e6c93a82af8f492030b50259afbec70fa3`  
		Last Modified: Mon, 09 Jan 2023 21:26:38 GMT  
		Size: 781.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c730f7de5ad88fff639b156f341691c1bfb870e296b0d57108be1cb1363994`  
		Last Modified: Mon, 09 Jan 2023 21:27:12 GMT  
		Size: 114.5 MB (114497683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1d1928d6116a0055b2604036d51ac756085b340888e26618455820ab2bb2fc`  
		Last Modified: Mon, 09 Jan 2023 21:26:55 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:778842b6b401fd9cd612a0854a776b03514705904190f39429c4a571c8c6dfe6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144005181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233cb4c41aca9755540342185c41e57349b899d49e8731c37b6e7fc3af14fe8c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 22 Nov 2022 22:55:46 GMT
ADD file:132c76d7f7dae2f51f589ee460f1870a2cec6e9dc7ff8e38e88fcee2cfbe70da in / 
# Tue, 22 Nov 2022 22:55:46 GMT
CMD ["/bin/sh"]
# Fri, 25 Nov 2022 20:50:12 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 25 Nov 2022 20:50:12 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 25 Nov 2022 20:50:13 GMT
ARG MAKEFLAGS=
# Fri, 25 Nov 2022 20:50:13 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 25 Nov 2022 20:54:52 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 25 Nov 2022 20:54:53 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 25 Nov 2022 20:54:53 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 25 Nov 2022 20:54:53 GMT
VOLUME [/znc-data]
# Fri, 25 Nov 2022 20:54:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Nov 2022 20:55:20 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 25 Nov 2022 20:55:21 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:c2eb4db52fbe1266a78d8c185d33544a2916faa7d82fb5f50909fe233e0579da`  
		Last Modified: Tue, 22 Nov 2022 22:56:39 GMT  
		Size: 3.1 MB (3107138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfea187da9da04dbf1f34f8fdc2085e55af691ff8886511a3371b8d57374cf1b`  
		Last Modified: Fri, 25 Nov 2022 20:55:54 GMT  
		Size: 44.8 MB (44756326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c12b41228ce051be01651ad4644188a240dc23e1c0439dd1afbecd7f55a384`  
		Last Modified: Fri, 25 Nov 2022 20:55:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae795b7b96f9e88694d26f838367db3475b90b0b60e0d60bccc174466e8868a`  
		Last Modified: Fri, 25 Nov 2022 20:55:45 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c14a7d9b426380f984a89bb827006c4bfb3d0d618e79df9e9738390bc674944`  
		Last Modified: Fri, 25 Nov 2022 20:56:26 GMT  
		Size: 96.1 MB (96140460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b2dc49ccc42715d920cf5b60d2af53e4b7e0257ad5be731dd5efad232c222d`  
		Last Modified: Fri, 25 Nov 2022 20:56:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:2bafc5670c009fb52e81137ebe821c6de22f323b5ffabd00d57d0df75652a4e1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153288386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2883d6bba9b909562a000168ca651a52fcdc38d8b2032bc9d919af8d35c96fb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 09 Jan 2023 17:04:48 GMT
ADD file:3080f19f39259a4b77cc53975de0184c78d4335ceb9ffb77a2838d0539ad6f85 in / 
# Mon, 09 Jan 2023 17:04:49 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 19:16:16 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Mon, 09 Jan 2023 19:16:16 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Mon, 09 Jan 2023 19:16:17 GMT
ARG MAKEFLAGS=
# Mon, 09 Jan 2023 19:16:17 GMT
ENV ZNC_VERSION=1.8.2
# Mon, 09 Jan 2023 19:19:39 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Mon, 09 Jan 2023 19:19:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Mon, 09 Jan 2023 19:19:40 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Mon, 09 Jan 2023 19:19:40 GMT
VOLUME [/znc-data]
# Mon, 09 Jan 2023 19:19:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Jan 2023 19:20:00 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Mon, 09 Jan 2023 19:20:02 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:a9eaa45ef418e883481a13c7d84fa9904f2ec56789c52a87ba5a9e6483f2b74f`  
		Last Modified: Mon, 09 Jan 2023 17:05:12 GMT  
		Size: 3.3 MB (3259241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1a7bf78ba8488ffcb8e702347e8d353e09c6f5b2752202e35038fcfc6a072d`  
		Last Modified: Mon, 09 Jan 2023 19:20:21 GMT  
		Size: 46.2 MB (46152657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036cf60fd34df0dac5ae84e25a8425f8f867c8688e3525fca09e7fa1fd802951`  
		Last Modified: Mon, 09 Jan 2023 19:20:15 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f67a6235f0e6a1e32fd72b1a91ec221405124b966ed6753e49e48b1d5143b3`  
		Last Modified: Mon, 09 Jan 2023 19:20:15 GMT  
		Size: 778.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd618dea82f77805f92146a81ea6e08c22e2181084de2057a3e43a578bede45d`  
		Last Modified: Mon, 09 Jan 2023 19:20:44 GMT  
		Size: 103.9 MB (103875208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40caa18f15a27918a796ec3072c3a935653cb4d23ec067e05794dfc33e9f3d3`  
		Last Modified: Mon, 09 Jan 2023 19:20:31 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
