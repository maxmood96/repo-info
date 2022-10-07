<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `znc`

-	[`znc:1.8`](#znc18)
-	[`znc:1.8-slim`](#znc18-slim)
-	[`znc:1.8.2`](#znc182)
-	[`znc:1.8.2-slim`](#znc182-slim)
-	[`znc:latest`](#znclatest)
-	[`znc:slim`](#zncslim)

## `znc:1.8`

```console
$ docker pull znc@sha256:3392e08b1892be110fcf6164d6734135e4f3194ed259f96bcedd433f9ed0b62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8` - linux; amd64

```console
$ docker pull znc@sha256:35164b10f47970b0059f74dda1ab6e6dc828004ff11aa65bbdac249c7ce6fa0d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138548287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b1acee2da36b45e41bccf8ad06cfea9a255fda8532ffb3fa37160416b40220`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:14 GMT
ADD file:7fd90c097e2c4587dee91726d71abc02fa1aa6a3a3395c862206a4e14e0c299c in / 
# Tue, 09 Aug 2022 17:20:14 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:29:24 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 07 Oct 2022 04:29:24 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 07 Oct 2022 04:29:24 GMT
ARG MAKEFLAGS=
# Fri, 07 Oct 2022 04:29:24 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 07 Oct 2022 04:33:38 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 07 Oct 2022 04:33:39 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 07 Oct 2022 04:33:39 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 07 Oct 2022 04:33:39 GMT
VOLUME [/znc-data]
# Fri, 07 Oct 2022 04:33:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Oct 2022 04:33:53 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 07 Oct 2022 04:33:54 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:72cfd02ff4d01b1f319eed108b53120dea0185b916d2abeb4e6121879cbf7a65`  
		Last Modified: Tue, 09 Aug 2022 17:21:16 GMT  
		Size: 2.8 MB (2827571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0f22044f90ae2a77eb095f28b9428f87de8918f228f9f85339e4cd8aad8850`  
		Last Modified: Fri, 07 Oct 2022 04:34:13 GMT  
		Size: 43.4 MB (43368543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bbd3936fe6a3a35579af2243d727780a9862256c761a2bf141b62fd6d9999e`  
		Last Modified: Fri, 07 Oct 2022 04:34:07 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071b7456cd68899b3f3ec4ab1b6e9e124fb1ea95840688aef6c72bade3d9a4f3`  
		Last Modified: Fri, 07 Oct 2022 04:34:07 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7816457a4059b0065bf58cb940a11bdd7067e636b4976c855f9c8ce40c2134`  
		Last Modified: Fri, 07 Oct 2022 04:34:39 GMT  
		Size: 92.4 MB (92350891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5ad7123205b7247668526fa597cc4a8dabd73cd3ca1e8cc11ad96cca2549c3`  
		Last Modified: Fri, 07 Oct 2022 04:34:26 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8` - linux; arm variant v6

```console
$ docker pull znc@sha256:673942d17d238049782b6536ff5961763ce6a9b719fb98bc4973a7009ff31956
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122175320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285da3395747f306d610542f0fb342593dbdd1dbf5a9a8df85710e708020150f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Jul 2022 22:50:15 GMT
ADD file:19dc757ba128952e4f765f774da40913195379a34f272ac71f3b3a651adf2740 in / 
# Tue, 19 Jul 2022 22:50:16 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 06:33:55 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 20 Jul 2022 06:33:55 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 20 Jul 2022 06:33:56 GMT
ARG MAKEFLAGS=
# Wed, 20 Jul 2022 06:33:56 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 20 Jul 2022 06:45:34 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 20 Jul 2022 06:45:35 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 20 Jul 2022 06:45:36 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 20 Jul 2022 06:45:36 GMT
VOLUME [/znc-data]
# Wed, 20 Jul 2022 06:45:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Jul 2022 06:46:14 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Wed, 20 Jul 2022 06:46:15 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:ecfe29996dc654c28c0e2c4726e34d251c79330ce39875ae8fbb5462d2695d5a`  
		Last Modified: Tue, 19 Jul 2022 22:51:54 GMT  
		Size: 2.6 MB (2625483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04365b0b3e572d8770a83c45266e92f3d8f34ac3c3494d983b7cbcd395cec702`  
		Last Modified: Wed, 20 Jul 2022 06:47:21 GMT  
		Size: 41.6 MB (41648378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08f00686afb3e6c39b2547417fa5b470494c04699317156a97d6950f24233f1`  
		Last Modified: Wed, 20 Jul 2022 06:46:54 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffcadac98083166f77f9a3cfdba4d87184f6bb9a22be883716beb55a21df2d9`  
		Last Modified: Wed, 20 Jul 2022 06:46:54 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f679d213a928d7f35f9c46db04b199ee01565c7c77428f5d79fe539d1ae7b8aa`  
		Last Modified: Wed, 20 Jul 2022 06:48:27 GMT  
		Size: 77.9 MB (77900176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17d52cbfbfc887cba3435df82ddf6dddb7b6ecd490bced0ee19c00f209b4cde`  
		Last Modified: Wed, 20 Jul 2022 06:47:36 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:26076532660c7fd54ff20d515d2aa8171817f31cc8289d29e7f0a901b7943d5e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129838456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c2116f18426a17a35e712c6206dad65a9372b916b4d09af0a75ef7ae740c78`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:59 GMT
ADD file:b501d234551d6b0f6f40b3533140338e5bc0d798a5699409f0fb5974318507d7 in / 
# Tue, 19 Jul 2022 22:40:00 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 03:53:27 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 20 Jul 2022 03:53:28 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 20 Jul 2022 03:53:29 GMT
ARG MAKEFLAGS=
# Wed, 20 Jul 2022 03:53:30 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 20 Jul 2022 03:58:21 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 20 Jul 2022 03:58:22 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 20 Jul 2022 03:58:23 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 20 Jul 2022 03:58:23 GMT
VOLUME [/znc-data]
# Wed, 20 Jul 2022 03:58:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Jul 2022 03:58:48 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Wed, 20 Jul 2022 03:58:50 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:e1e3bb43032bb6c47cf7fce8f9be50ba91100ca9d50c31130e9f56d3664daa23`  
		Last Modified: Tue, 19 Jul 2022 22:40:55 GMT  
		Size: 2.7 MB (2721189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd55e454e62000c5ad2b6c16e772f6d9bedbd9271e3e1c83aaff9ee275f6139`  
		Last Modified: Wed, 20 Jul 2022 03:59:17 GMT  
		Size: 43.2 MB (43215131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9ca440d915b17ccabc0859f57bda8c2d488e6c47d0147ac827e3ce5de9cbb8`  
		Last Modified: Wed, 20 Jul 2022 03:59:10 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4448385224f02cbf34a0c42453e03c59ce7c56730097846156e1604fcc41b86b`  
		Last Modified: Wed, 20 Jul 2022 03:59:10 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1507601b8188cb311b770473dac611f08b9e9ddc7f3bb5f12e9794ac3a0f8a16`  
		Last Modified: Wed, 20 Jul 2022 03:59:44 GMT  
		Size: 83.9 MB (83900877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb93bba8c134f5dcbb73681521c2b9b2ef80b84dadb69b9fbed833e47cb4153`  
		Last Modified: Wed, 20 Jul 2022 03:59:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.8-slim`

```console
$ docker pull znc@sha256:c77f2b539a681fbdd5998c1c8724f62db34aa4178b63a6ee038330e9ce7bbcfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8-slim` - linux; amd64

```console
$ docker pull znc@sha256:1d629e8790c333896a94022e4a7b0fc3f804d135e6b94e6d7fdd0fd6bb134695
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46197065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3078b3b99df7215ded8db96d35cbc2e557dd3614e75c79ced47a29399a239a9a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:14 GMT
ADD file:7fd90c097e2c4587dee91726d71abc02fa1aa6a3a3395c862206a4e14e0c299c in / 
# Tue, 09 Aug 2022 17:20:14 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:29:24 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 07 Oct 2022 04:29:24 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 07 Oct 2022 04:29:24 GMT
ARG MAKEFLAGS=
# Fri, 07 Oct 2022 04:29:24 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 07 Oct 2022 04:33:38 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 07 Oct 2022 04:33:39 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 07 Oct 2022 04:33:39 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 07 Oct 2022 04:33:39 GMT
VOLUME [/znc-data]
# Fri, 07 Oct 2022 04:33:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:72cfd02ff4d01b1f319eed108b53120dea0185b916d2abeb4e6121879cbf7a65`  
		Last Modified: Tue, 09 Aug 2022 17:21:16 GMT  
		Size: 2.8 MB (2827571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0f22044f90ae2a77eb095f28b9428f87de8918f228f9f85339e4cd8aad8850`  
		Last Modified: Fri, 07 Oct 2022 04:34:13 GMT  
		Size: 43.4 MB (43368543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bbd3936fe6a3a35579af2243d727780a9862256c761a2bf141b62fd6d9999e`  
		Last Modified: Fri, 07 Oct 2022 04:34:07 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071b7456cd68899b3f3ec4ab1b6e9e124fb1ea95840688aef6c72bade3d9a4f3`  
		Last Modified: Fri, 07 Oct 2022 04:34:07 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:4a5488f3b324e9fb1ea4f7071d95f6e2ba0529eb0a786148ac3b8eb871dd722c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44274813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2a6a47237e10d7d0775343e242337e4d51e4dfc9081445cc5f86deceb0edf1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Jul 2022 22:50:15 GMT
ADD file:19dc757ba128952e4f765f774da40913195379a34f272ac71f3b3a651adf2740 in / 
# Tue, 19 Jul 2022 22:50:16 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 06:33:55 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 20 Jul 2022 06:33:55 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 20 Jul 2022 06:33:56 GMT
ARG MAKEFLAGS=
# Wed, 20 Jul 2022 06:33:56 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 20 Jul 2022 06:45:34 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 20 Jul 2022 06:45:35 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 20 Jul 2022 06:45:36 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 20 Jul 2022 06:45:36 GMT
VOLUME [/znc-data]
# Wed, 20 Jul 2022 06:45:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:ecfe29996dc654c28c0e2c4726e34d251c79330ce39875ae8fbb5462d2695d5a`  
		Last Modified: Tue, 19 Jul 2022 22:51:54 GMT  
		Size: 2.6 MB (2625483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04365b0b3e572d8770a83c45266e92f3d8f34ac3c3494d983b7cbcd395cec702`  
		Last Modified: Wed, 20 Jul 2022 06:47:21 GMT  
		Size: 41.6 MB (41648378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08f00686afb3e6c39b2547417fa5b470494c04699317156a97d6950f24233f1`  
		Last Modified: Wed, 20 Jul 2022 06:46:54 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffcadac98083166f77f9a3cfdba4d87184f6bb9a22be883716beb55a21df2d9`  
		Last Modified: Wed, 20 Jul 2022 06:46:54 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:bb911f8bc2cf88790c9245fc843b2602733bcc3e8597c6ff20295e935b48ab1f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45937247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dabde43bca704526333938446de5eed40b465135b150023d7c2060705427f8d0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:59 GMT
ADD file:b501d234551d6b0f6f40b3533140338e5bc0d798a5699409f0fb5974318507d7 in / 
# Tue, 19 Jul 2022 22:40:00 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 03:53:27 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 20 Jul 2022 03:53:28 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 20 Jul 2022 03:53:29 GMT
ARG MAKEFLAGS=
# Wed, 20 Jul 2022 03:53:30 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 20 Jul 2022 03:58:21 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 20 Jul 2022 03:58:22 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 20 Jul 2022 03:58:23 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 20 Jul 2022 03:58:23 GMT
VOLUME [/znc-data]
# Wed, 20 Jul 2022 03:58:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e1e3bb43032bb6c47cf7fce8f9be50ba91100ca9d50c31130e9f56d3664daa23`  
		Last Modified: Tue, 19 Jul 2022 22:40:55 GMT  
		Size: 2.7 MB (2721189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd55e454e62000c5ad2b6c16e772f6d9bedbd9271e3e1c83aaff9ee275f6139`  
		Last Modified: Wed, 20 Jul 2022 03:59:17 GMT  
		Size: 43.2 MB (43215131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9ca440d915b17ccabc0859f57bda8c2d488e6c47d0147ac827e3ce5de9cbb8`  
		Last Modified: Wed, 20 Jul 2022 03:59:10 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4448385224f02cbf34a0c42453e03c59ce7c56730097846156e1604fcc41b86b`  
		Last Modified: Wed, 20 Jul 2022 03:59:10 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.8.2`

```console
$ docker pull znc@sha256:3392e08b1892be110fcf6164d6734135e4f3194ed259f96bcedd433f9ed0b62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8.2` - linux; amd64

```console
$ docker pull znc@sha256:35164b10f47970b0059f74dda1ab6e6dc828004ff11aa65bbdac249c7ce6fa0d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138548287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b1acee2da36b45e41bccf8ad06cfea9a255fda8532ffb3fa37160416b40220`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:14 GMT
ADD file:7fd90c097e2c4587dee91726d71abc02fa1aa6a3a3395c862206a4e14e0c299c in / 
# Tue, 09 Aug 2022 17:20:14 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:29:24 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 07 Oct 2022 04:29:24 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 07 Oct 2022 04:29:24 GMT
ARG MAKEFLAGS=
# Fri, 07 Oct 2022 04:29:24 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 07 Oct 2022 04:33:38 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 07 Oct 2022 04:33:39 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 07 Oct 2022 04:33:39 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 07 Oct 2022 04:33:39 GMT
VOLUME [/znc-data]
# Fri, 07 Oct 2022 04:33:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Oct 2022 04:33:53 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 07 Oct 2022 04:33:54 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:72cfd02ff4d01b1f319eed108b53120dea0185b916d2abeb4e6121879cbf7a65`  
		Last Modified: Tue, 09 Aug 2022 17:21:16 GMT  
		Size: 2.8 MB (2827571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0f22044f90ae2a77eb095f28b9428f87de8918f228f9f85339e4cd8aad8850`  
		Last Modified: Fri, 07 Oct 2022 04:34:13 GMT  
		Size: 43.4 MB (43368543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bbd3936fe6a3a35579af2243d727780a9862256c761a2bf141b62fd6d9999e`  
		Last Modified: Fri, 07 Oct 2022 04:34:07 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071b7456cd68899b3f3ec4ab1b6e9e124fb1ea95840688aef6c72bade3d9a4f3`  
		Last Modified: Fri, 07 Oct 2022 04:34:07 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7816457a4059b0065bf58cb940a11bdd7067e636b4976c855f9c8ce40c2134`  
		Last Modified: Fri, 07 Oct 2022 04:34:39 GMT  
		Size: 92.4 MB (92350891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5ad7123205b7247668526fa597cc4a8dabd73cd3ca1e8cc11ad96cca2549c3`  
		Last Modified: Fri, 07 Oct 2022 04:34:26 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2` - linux; arm variant v6

```console
$ docker pull znc@sha256:673942d17d238049782b6536ff5961763ce6a9b719fb98bc4973a7009ff31956
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122175320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285da3395747f306d610542f0fb342593dbdd1dbf5a9a8df85710e708020150f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Jul 2022 22:50:15 GMT
ADD file:19dc757ba128952e4f765f774da40913195379a34f272ac71f3b3a651adf2740 in / 
# Tue, 19 Jul 2022 22:50:16 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 06:33:55 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 20 Jul 2022 06:33:55 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 20 Jul 2022 06:33:56 GMT
ARG MAKEFLAGS=
# Wed, 20 Jul 2022 06:33:56 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 20 Jul 2022 06:45:34 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 20 Jul 2022 06:45:35 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 20 Jul 2022 06:45:36 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 20 Jul 2022 06:45:36 GMT
VOLUME [/znc-data]
# Wed, 20 Jul 2022 06:45:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Jul 2022 06:46:14 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Wed, 20 Jul 2022 06:46:15 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:ecfe29996dc654c28c0e2c4726e34d251c79330ce39875ae8fbb5462d2695d5a`  
		Last Modified: Tue, 19 Jul 2022 22:51:54 GMT  
		Size: 2.6 MB (2625483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04365b0b3e572d8770a83c45266e92f3d8f34ac3c3494d983b7cbcd395cec702`  
		Last Modified: Wed, 20 Jul 2022 06:47:21 GMT  
		Size: 41.6 MB (41648378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08f00686afb3e6c39b2547417fa5b470494c04699317156a97d6950f24233f1`  
		Last Modified: Wed, 20 Jul 2022 06:46:54 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffcadac98083166f77f9a3cfdba4d87184f6bb9a22be883716beb55a21df2d9`  
		Last Modified: Wed, 20 Jul 2022 06:46:54 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f679d213a928d7f35f9c46db04b199ee01565c7c77428f5d79fe539d1ae7b8aa`  
		Last Modified: Wed, 20 Jul 2022 06:48:27 GMT  
		Size: 77.9 MB (77900176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17d52cbfbfc887cba3435df82ddf6dddb7b6ecd490bced0ee19c00f209b4cde`  
		Last Modified: Wed, 20 Jul 2022 06:47:36 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:26076532660c7fd54ff20d515d2aa8171817f31cc8289d29e7f0a901b7943d5e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129838456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c2116f18426a17a35e712c6206dad65a9372b916b4d09af0a75ef7ae740c78`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:59 GMT
ADD file:b501d234551d6b0f6f40b3533140338e5bc0d798a5699409f0fb5974318507d7 in / 
# Tue, 19 Jul 2022 22:40:00 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 03:53:27 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 20 Jul 2022 03:53:28 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 20 Jul 2022 03:53:29 GMT
ARG MAKEFLAGS=
# Wed, 20 Jul 2022 03:53:30 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 20 Jul 2022 03:58:21 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 20 Jul 2022 03:58:22 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 20 Jul 2022 03:58:23 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 20 Jul 2022 03:58:23 GMT
VOLUME [/znc-data]
# Wed, 20 Jul 2022 03:58:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Jul 2022 03:58:48 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Wed, 20 Jul 2022 03:58:50 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:e1e3bb43032bb6c47cf7fce8f9be50ba91100ca9d50c31130e9f56d3664daa23`  
		Last Modified: Tue, 19 Jul 2022 22:40:55 GMT  
		Size: 2.7 MB (2721189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd55e454e62000c5ad2b6c16e772f6d9bedbd9271e3e1c83aaff9ee275f6139`  
		Last Modified: Wed, 20 Jul 2022 03:59:17 GMT  
		Size: 43.2 MB (43215131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9ca440d915b17ccabc0859f57bda8c2d488e6c47d0147ac827e3ce5de9cbb8`  
		Last Modified: Wed, 20 Jul 2022 03:59:10 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4448385224f02cbf34a0c42453e03c59ce7c56730097846156e1604fcc41b86b`  
		Last Modified: Wed, 20 Jul 2022 03:59:10 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1507601b8188cb311b770473dac611f08b9e9ddc7f3bb5f12e9794ac3a0f8a16`  
		Last Modified: Wed, 20 Jul 2022 03:59:44 GMT  
		Size: 83.9 MB (83900877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb93bba8c134f5dcbb73681521c2b9b2ef80b84dadb69b9fbed833e47cb4153`  
		Last Modified: Wed, 20 Jul 2022 03:59:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.8.2-slim`

```console
$ docker pull znc@sha256:c77f2b539a681fbdd5998c1c8724f62db34aa4178b63a6ee038330e9ce7bbcfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8.2-slim` - linux; amd64

```console
$ docker pull znc@sha256:1d629e8790c333896a94022e4a7b0fc3f804d135e6b94e6d7fdd0fd6bb134695
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46197065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3078b3b99df7215ded8db96d35cbc2e557dd3614e75c79ced47a29399a239a9a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:14 GMT
ADD file:7fd90c097e2c4587dee91726d71abc02fa1aa6a3a3395c862206a4e14e0c299c in / 
# Tue, 09 Aug 2022 17:20:14 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:29:24 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 07 Oct 2022 04:29:24 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 07 Oct 2022 04:29:24 GMT
ARG MAKEFLAGS=
# Fri, 07 Oct 2022 04:29:24 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 07 Oct 2022 04:33:38 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 07 Oct 2022 04:33:39 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 07 Oct 2022 04:33:39 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 07 Oct 2022 04:33:39 GMT
VOLUME [/znc-data]
# Fri, 07 Oct 2022 04:33:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:72cfd02ff4d01b1f319eed108b53120dea0185b916d2abeb4e6121879cbf7a65`  
		Last Modified: Tue, 09 Aug 2022 17:21:16 GMT  
		Size: 2.8 MB (2827571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0f22044f90ae2a77eb095f28b9428f87de8918f228f9f85339e4cd8aad8850`  
		Last Modified: Fri, 07 Oct 2022 04:34:13 GMT  
		Size: 43.4 MB (43368543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bbd3936fe6a3a35579af2243d727780a9862256c761a2bf141b62fd6d9999e`  
		Last Modified: Fri, 07 Oct 2022 04:34:07 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071b7456cd68899b3f3ec4ab1b6e9e124fb1ea95840688aef6c72bade3d9a4f3`  
		Last Modified: Fri, 07 Oct 2022 04:34:07 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:4a5488f3b324e9fb1ea4f7071d95f6e2ba0529eb0a786148ac3b8eb871dd722c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44274813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2a6a47237e10d7d0775343e242337e4d51e4dfc9081445cc5f86deceb0edf1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Jul 2022 22:50:15 GMT
ADD file:19dc757ba128952e4f765f774da40913195379a34f272ac71f3b3a651adf2740 in / 
# Tue, 19 Jul 2022 22:50:16 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 06:33:55 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 20 Jul 2022 06:33:55 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 20 Jul 2022 06:33:56 GMT
ARG MAKEFLAGS=
# Wed, 20 Jul 2022 06:33:56 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 20 Jul 2022 06:45:34 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 20 Jul 2022 06:45:35 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 20 Jul 2022 06:45:36 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 20 Jul 2022 06:45:36 GMT
VOLUME [/znc-data]
# Wed, 20 Jul 2022 06:45:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:ecfe29996dc654c28c0e2c4726e34d251c79330ce39875ae8fbb5462d2695d5a`  
		Last Modified: Tue, 19 Jul 2022 22:51:54 GMT  
		Size: 2.6 MB (2625483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04365b0b3e572d8770a83c45266e92f3d8f34ac3c3494d983b7cbcd395cec702`  
		Last Modified: Wed, 20 Jul 2022 06:47:21 GMT  
		Size: 41.6 MB (41648378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08f00686afb3e6c39b2547417fa5b470494c04699317156a97d6950f24233f1`  
		Last Modified: Wed, 20 Jul 2022 06:46:54 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffcadac98083166f77f9a3cfdba4d87184f6bb9a22be883716beb55a21df2d9`  
		Last Modified: Wed, 20 Jul 2022 06:46:54 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:bb911f8bc2cf88790c9245fc843b2602733bcc3e8597c6ff20295e935b48ab1f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45937247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dabde43bca704526333938446de5eed40b465135b150023d7c2060705427f8d0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:59 GMT
ADD file:b501d234551d6b0f6f40b3533140338e5bc0d798a5699409f0fb5974318507d7 in / 
# Tue, 19 Jul 2022 22:40:00 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 03:53:27 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 20 Jul 2022 03:53:28 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 20 Jul 2022 03:53:29 GMT
ARG MAKEFLAGS=
# Wed, 20 Jul 2022 03:53:30 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 20 Jul 2022 03:58:21 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 20 Jul 2022 03:58:22 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 20 Jul 2022 03:58:23 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 20 Jul 2022 03:58:23 GMT
VOLUME [/znc-data]
# Wed, 20 Jul 2022 03:58:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e1e3bb43032bb6c47cf7fce8f9be50ba91100ca9d50c31130e9f56d3664daa23`  
		Last Modified: Tue, 19 Jul 2022 22:40:55 GMT  
		Size: 2.7 MB (2721189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd55e454e62000c5ad2b6c16e772f6d9bedbd9271e3e1c83aaff9ee275f6139`  
		Last Modified: Wed, 20 Jul 2022 03:59:17 GMT  
		Size: 43.2 MB (43215131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9ca440d915b17ccabc0859f57bda8c2d488e6c47d0147ac827e3ce5de9cbb8`  
		Last Modified: Wed, 20 Jul 2022 03:59:10 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4448385224f02cbf34a0c42453e03c59ce7c56730097846156e1604fcc41b86b`  
		Last Modified: Wed, 20 Jul 2022 03:59:10 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:latest`

```console
$ docker pull znc@sha256:3392e08b1892be110fcf6164d6734135e4f3194ed259f96bcedd433f9ed0b62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:latest` - linux; amd64

```console
$ docker pull znc@sha256:35164b10f47970b0059f74dda1ab6e6dc828004ff11aa65bbdac249c7ce6fa0d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138548287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b1acee2da36b45e41bccf8ad06cfea9a255fda8532ffb3fa37160416b40220`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:14 GMT
ADD file:7fd90c097e2c4587dee91726d71abc02fa1aa6a3a3395c862206a4e14e0c299c in / 
# Tue, 09 Aug 2022 17:20:14 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:29:24 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 07 Oct 2022 04:29:24 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 07 Oct 2022 04:29:24 GMT
ARG MAKEFLAGS=
# Fri, 07 Oct 2022 04:29:24 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 07 Oct 2022 04:33:38 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 07 Oct 2022 04:33:39 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 07 Oct 2022 04:33:39 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 07 Oct 2022 04:33:39 GMT
VOLUME [/znc-data]
# Fri, 07 Oct 2022 04:33:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Oct 2022 04:33:53 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 07 Oct 2022 04:33:54 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:72cfd02ff4d01b1f319eed108b53120dea0185b916d2abeb4e6121879cbf7a65`  
		Last Modified: Tue, 09 Aug 2022 17:21:16 GMT  
		Size: 2.8 MB (2827571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0f22044f90ae2a77eb095f28b9428f87de8918f228f9f85339e4cd8aad8850`  
		Last Modified: Fri, 07 Oct 2022 04:34:13 GMT  
		Size: 43.4 MB (43368543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bbd3936fe6a3a35579af2243d727780a9862256c761a2bf141b62fd6d9999e`  
		Last Modified: Fri, 07 Oct 2022 04:34:07 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071b7456cd68899b3f3ec4ab1b6e9e124fb1ea95840688aef6c72bade3d9a4f3`  
		Last Modified: Fri, 07 Oct 2022 04:34:07 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7816457a4059b0065bf58cb940a11bdd7067e636b4976c855f9c8ce40c2134`  
		Last Modified: Fri, 07 Oct 2022 04:34:39 GMT  
		Size: 92.4 MB (92350891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5ad7123205b7247668526fa597cc4a8dabd73cd3ca1e8cc11ad96cca2549c3`  
		Last Modified: Fri, 07 Oct 2022 04:34:26 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:673942d17d238049782b6536ff5961763ce6a9b719fb98bc4973a7009ff31956
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122175320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285da3395747f306d610542f0fb342593dbdd1dbf5a9a8df85710e708020150f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Jul 2022 22:50:15 GMT
ADD file:19dc757ba128952e4f765f774da40913195379a34f272ac71f3b3a651adf2740 in / 
# Tue, 19 Jul 2022 22:50:16 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 06:33:55 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 20 Jul 2022 06:33:55 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 20 Jul 2022 06:33:56 GMT
ARG MAKEFLAGS=
# Wed, 20 Jul 2022 06:33:56 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 20 Jul 2022 06:45:34 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 20 Jul 2022 06:45:35 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 20 Jul 2022 06:45:36 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 20 Jul 2022 06:45:36 GMT
VOLUME [/znc-data]
# Wed, 20 Jul 2022 06:45:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Jul 2022 06:46:14 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Wed, 20 Jul 2022 06:46:15 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:ecfe29996dc654c28c0e2c4726e34d251c79330ce39875ae8fbb5462d2695d5a`  
		Last Modified: Tue, 19 Jul 2022 22:51:54 GMT  
		Size: 2.6 MB (2625483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04365b0b3e572d8770a83c45266e92f3d8f34ac3c3494d983b7cbcd395cec702`  
		Last Modified: Wed, 20 Jul 2022 06:47:21 GMT  
		Size: 41.6 MB (41648378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08f00686afb3e6c39b2547417fa5b470494c04699317156a97d6950f24233f1`  
		Last Modified: Wed, 20 Jul 2022 06:46:54 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffcadac98083166f77f9a3cfdba4d87184f6bb9a22be883716beb55a21df2d9`  
		Last Modified: Wed, 20 Jul 2022 06:46:54 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f679d213a928d7f35f9c46db04b199ee01565c7c77428f5d79fe539d1ae7b8aa`  
		Last Modified: Wed, 20 Jul 2022 06:48:27 GMT  
		Size: 77.9 MB (77900176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17d52cbfbfc887cba3435df82ddf6dddb7b6ecd490bced0ee19c00f209b4cde`  
		Last Modified: Wed, 20 Jul 2022 06:47:36 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:26076532660c7fd54ff20d515d2aa8171817f31cc8289d29e7f0a901b7943d5e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129838456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c2116f18426a17a35e712c6206dad65a9372b916b4d09af0a75ef7ae740c78`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:59 GMT
ADD file:b501d234551d6b0f6f40b3533140338e5bc0d798a5699409f0fb5974318507d7 in / 
# Tue, 19 Jul 2022 22:40:00 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 03:53:27 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 20 Jul 2022 03:53:28 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 20 Jul 2022 03:53:29 GMT
ARG MAKEFLAGS=
# Wed, 20 Jul 2022 03:53:30 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 20 Jul 2022 03:58:21 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 20 Jul 2022 03:58:22 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 20 Jul 2022 03:58:23 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 20 Jul 2022 03:58:23 GMT
VOLUME [/znc-data]
# Wed, 20 Jul 2022 03:58:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Jul 2022 03:58:48 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Wed, 20 Jul 2022 03:58:50 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:e1e3bb43032bb6c47cf7fce8f9be50ba91100ca9d50c31130e9f56d3664daa23`  
		Last Modified: Tue, 19 Jul 2022 22:40:55 GMT  
		Size: 2.7 MB (2721189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd55e454e62000c5ad2b6c16e772f6d9bedbd9271e3e1c83aaff9ee275f6139`  
		Last Modified: Wed, 20 Jul 2022 03:59:17 GMT  
		Size: 43.2 MB (43215131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9ca440d915b17ccabc0859f57bda8c2d488e6c47d0147ac827e3ce5de9cbb8`  
		Last Modified: Wed, 20 Jul 2022 03:59:10 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4448385224f02cbf34a0c42453e03c59ce7c56730097846156e1604fcc41b86b`  
		Last Modified: Wed, 20 Jul 2022 03:59:10 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1507601b8188cb311b770473dac611f08b9e9ddc7f3bb5f12e9794ac3a0f8a16`  
		Last Modified: Wed, 20 Jul 2022 03:59:44 GMT  
		Size: 83.9 MB (83900877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb93bba8c134f5dcbb73681521c2b9b2ef80b84dadb69b9fbed833e47cb4153`  
		Last Modified: Wed, 20 Jul 2022 03:59:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:slim`

```console
$ docker pull znc@sha256:c77f2b539a681fbdd5998c1c8724f62db34aa4178b63a6ee038330e9ce7bbcfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:slim` - linux; amd64

```console
$ docker pull znc@sha256:1d629e8790c333896a94022e4a7b0fc3f804d135e6b94e6d7fdd0fd6bb134695
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46197065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3078b3b99df7215ded8db96d35cbc2e557dd3614e75c79ced47a29399a239a9a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:14 GMT
ADD file:7fd90c097e2c4587dee91726d71abc02fa1aa6a3a3395c862206a4e14e0c299c in / 
# Tue, 09 Aug 2022 17:20:14 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:29:24 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 07 Oct 2022 04:29:24 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 07 Oct 2022 04:29:24 GMT
ARG MAKEFLAGS=
# Fri, 07 Oct 2022 04:29:24 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 07 Oct 2022 04:33:38 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 07 Oct 2022 04:33:39 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 07 Oct 2022 04:33:39 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 07 Oct 2022 04:33:39 GMT
VOLUME [/znc-data]
# Fri, 07 Oct 2022 04:33:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:72cfd02ff4d01b1f319eed108b53120dea0185b916d2abeb4e6121879cbf7a65`  
		Last Modified: Tue, 09 Aug 2022 17:21:16 GMT  
		Size: 2.8 MB (2827571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0f22044f90ae2a77eb095f28b9428f87de8918f228f9f85339e4cd8aad8850`  
		Last Modified: Fri, 07 Oct 2022 04:34:13 GMT  
		Size: 43.4 MB (43368543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bbd3936fe6a3a35579af2243d727780a9862256c761a2bf141b62fd6d9999e`  
		Last Modified: Fri, 07 Oct 2022 04:34:07 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071b7456cd68899b3f3ec4ab1b6e9e124fb1ea95840688aef6c72bade3d9a4f3`  
		Last Modified: Fri, 07 Oct 2022 04:34:07 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:4a5488f3b324e9fb1ea4f7071d95f6e2ba0529eb0a786148ac3b8eb871dd722c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44274813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2a6a47237e10d7d0775343e242337e4d51e4dfc9081445cc5f86deceb0edf1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Jul 2022 22:50:15 GMT
ADD file:19dc757ba128952e4f765f774da40913195379a34f272ac71f3b3a651adf2740 in / 
# Tue, 19 Jul 2022 22:50:16 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 06:33:55 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 20 Jul 2022 06:33:55 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 20 Jul 2022 06:33:56 GMT
ARG MAKEFLAGS=
# Wed, 20 Jul 2022 06:33:56 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 20 Jul 2022 06:45:34 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 20 Jul 2022 06:45:35 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 20 Jul 2022 06:45:36 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 20 Jul 2022 06:45:36 GMT
VOLUME [/znc-data]
# Wed, 20 Jul 2022 06:45:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:ecfe29996dc654c28c0e2c4726e34d251c79330ce39875ae8fbb5462d2695d5a`  
		Last Modified: Tue, 19 Jul 2022 22:51:54 GMT  
		Size: 2.6 MB (2625483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04365b0b3e572d8770a83c45266e92f3d8f34ac3c3494d983b7cbcd395cec702`  
		Last Modified: Wed, 20 Jul 2022 06:47:21 GMT  
		Size: 41.6 MB (41648378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08f00686afb3e6c39b2547417fa5b470494c04699317156a97d6950f24233f1`  
		Last Modified: Wed, 20 Jul 2022 06:46:54 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffcadac98083166f77f9a3cfdba4d87184f6bb9a22be883716beb55a21df2d9`  
		Last Modified: Wed, 20 Jul 2022 06:46:54 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:bb911f8bc2cf88790c9245fc843b2602733bcc3e8597c6ff20295e935b48ab1f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45937247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dabde43bca704526333938446de5eed40b465135b150023d7c2060705427f8d0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:59 GMT
ADD file:b501d234551d6b0f6f40b3533140338e5bc0d798a5699409f0fb5974318507d7 in / 
# Tue, 19 Jul 2022 22:40:00 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 03:53:27 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 20 Jul 2022 03:53:28 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 20 Jul 2022 03:53:29 GMT
ARG MAKEFLAGS=
# Wed, 20 Jul 2022 03:53:30 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 20 Jul 2022 03:58:21 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 20 Jul 2022 03:58:22 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 20 Jul 2022 03:58:23 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 20 Jul 2022 03:58:23 GMT
VOLUME [/znc-data]
# Wed, 20 Jul 2022 03:58:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e1e3bb43032bb6c47cf7fce8f9be50ba91100ca9d50c31130e9f56d3664daa23`  
		Last Modified: Tue, 19 Jul 2022 22:40:55 GMT  
		Size: 2.7 MB (2721189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd55e454e62000c5ad2b6c16e772f6d9bedbd9271e3e1c83aaff9ee275f6139`  
		Last Modified: Wed, 20 Jul 2022 03:59:17 GMT  
		Size: 43.2 MB (43215131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9ca440d915b17ccabc0859f57bda8c2d488e6c47d0147ac827e3ce5de9cbb8`  
		Last Modified: Wed, 20 Jul 2022 03:59:10 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4448385224f02cbf34a0c42453e03c59ce7c56730097846156e1604fcc41b86b`  
		Last Modified: Wed, 20 Jul 2022 03:59:10 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
