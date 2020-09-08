<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `znc`

-	[`znc:1.8`](#znc18)
-	[`znc:1.8.2`](#znc182)
-	[`znc:1.8.2-slim`](#znc182-slim)
-	[`znc:1.8-slim`](#znc18-slim)
-	[`znc:latest`](#znclatest)
-	[`znc:slim`](#zncslim)

## `znc:1.8`

```console
$ docker pull znc@sha256:e093797ff6a40ddd5ee55cc57d33ec0ab8780fe61fed1263e13171eab153df70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8` - linux; amd64

```console
$ docker pull znc@sha256:f05fa99cf91c247467afad3c0ad3fd262a6f8f27fccc36a8446837db52f3e6c0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145467376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c6bf2e7b733563835673ce63565322b6186e1049e6634d8dbc0f3f8df1f86`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2020 19:22:11 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Mon, 04 May 2020 19:22:11 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Mon, 04 May 2020 19:22:11 GMT
ARG MAKEFLAGS=
# Mon, 08 Jun 2020 18:25:56 GMT
ENV ZNC_VERSION=1.8.1
# Mon, 08 Jun 2020 18:30:18 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Mon, 08 Jun 2020 18:30:18 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Mon, 08 Jun 2020 18:30:18 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:30:19 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:30:19 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Mon, 08 Jun 2020 18:30:19 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:30:19 GMT
VOLUME [/znc-data]
# Mon, 08 Jun 2020 18:30:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2020 18:30:35 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Mon, 08 Jun 2020 18:30:35 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5a1332069b5686f2953370c761c60ad203b22a4b5d907cddabd5e3766aa49b`  
		Last Modified: Mon, 08 Jun 2020 18:30:56 GMT  
		Size: 57.4 MB (57402945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a3efef78d5bed01124912e52f0e3a0779a6345f5b42c17788d65c978ea7bb7`  
		Last Modified: Mon, 08 Jun 2020 18:30:43 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c3f10758cc9042e43fb6abf244903f8ba5a9dc2a669a9a30b95dc589d21087`  
		Last Modified: Mon, 08 Jun 2020 18:30:43 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83dd650d49b861285b5f22ebeb69e7cf2ef5c693e0648c22b4b78d960a91a9dc`  
		Last Modified: Mon, 08 Jun 2020 18:30:43 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee9947bd59b5d71c18d40c71849c7ed7540188da416129ac186d78cd18b0714`  
		Last Modified: Mon, 08 Jun 2020 18:30:43 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ec4d8b8066c8edda8b14884cea78384b3245fc8ff088524fee89c3409d3389`  
		Last Modified: Mon, 08 Jun 2020 18:30:43 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7115798da545f00a3b605b09ecee681bab84bb9f2a5aa910306504c5fcdf758c`  
		Last Modified: Mon, 08 Jun 2020 18:31:16 GMT  
		Size: 85.2 MB (85249387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82542bfc7155c7556a2ef1fc164c34f30eaf31d36613e32107c0fd122756a45c`  
		Last Modified: Mon, 08 Jun 2020 18:31:01 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8` - linux; arm variant v6

```console
$ docker pull znc@sha256:47740b4e5a6c020aada41ac19c1931c360b7d129267b271ce5f06d67b426e831
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132809194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed893f3b3eb5611fc653b2c70c796c00e2190e482db23d758ce36325b39c39f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Tue, 08 Sep 2020 22:04:03 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 08 Sep 2020 22:04:10 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Tue, 08 Sep 2020 22:04:19 GMT
ARG MAKEFLAGS=
# Tue, 08 Sep 2020 22:04:27 GMT
ENV ZNC_VERSION=1.8.2
# Tue, 08 Sep 2020 22:13:28 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Tue, 08 Sep 2020 22:13:41 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Tue, 08 Sep 2020 22:13:57 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:11 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:25 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:40 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:51 GMT
VOLUME [/znc-data]
# Tue, 08 Sep 2020 22:15:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Sep 2020 22:16:05 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Tue, 08 Sep 2020 22:16:20 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82217ea964091f8c190214bd997420f9132e906b89fed351d36269f6152d586e`  
		Last Modified: Tue, 08 Sep 2020 22:16:54 GMT  
		Size: 43.2 MB (43184125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8954ac8421360fdd845e73456cca768d6e6063c0a97b158edecdd95f999965b7`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523acf9284a5c22a3148b30bdca3b5c4f5fe55e1ae8586a8e282235cc56a4f7c`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aba0fda97135a4280a08db5555814f2b04ae0ffc032f48d47b47a98d6783c15`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd444df6d3a77099159e06342ba5bca06b8dca6d054d79165cabbfa044b5c7f`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766280c07d141fab7909b7e07cbd0a3373166a404354be8fdb200285c9a813d4`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275a81cb106f91a9cc396b3ff0d4d472115391735da996d949d4e960100219c8`  
		Last Modified: Tue, 08 Sep 2020 22:17:34 GMT  
		Size: 87.0 MB (87020019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f02b101b1cfe888ef641b0875361f3640ac62ce395366cb86645a78c69e6a7`  
		Last Modified: Tue, 08 Sep 2020 22:17:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:9b1369022519d39413ce456ee0368eaa3a8b6720ba32d9beee434c0bb8ac5c4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135289590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036305fce5a5341a326034ee6b3a8938105ea4cde69ada975d1206a5660a4158`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2020 19:40:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Mon, 04 May 2020 19:40:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Mon, 04 May 2020 19:40:24 GMT
ARG MAKEFLAGS=
# Mon, 08 Jun 2020 18:44:15 GMT
ENV ZNC_VERSION=1.8.1
# Mon, 08 Jun 2020 18:52:37 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Mon, 08 Jun 2020 18:52:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Mon, 08 Jun 2020 18:52:41 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:52:42 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:52:42 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Mon, 08 Jun 2020 18:52:43 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:52:43 GMT
VOLUME [/znc-data]
# Mon, 08 Jun 2020 18:52:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2020 18:53:06 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Mon, 08 Jun 2020 18:53:09 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3887515d24b1515c28be3aeca64919edc9acbcff3321a497ba03a160633368`  
		Last Modified: Mon, 08 Jun 2020 18:53:38 GMT  
		Size: 57.3 MB (57312408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79050300cb2ffb98537cb2cfa0f82a803c51cc89a4d952679aed84418b9efdc2`  
		Last Modified: Mon, 08 Jun 2020 18:53:20 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4a6462efa842040fc02cfab1ac30d09819cf8a70034bda884df08f50ff60e6`  
		Last Modified: Mon, 08 Jun 2020 18:53:20 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdbcc0a36123d143db9ab73ea2025356b52af8c3f872e1e2778fba03fb46ff6`  
		Last Modified: Mon, 08 Jun 2020 18:53:20 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deeec6fca5fad8f785f3307d8fbc2886d7c9f565801eded4da2da998260812e2`  
		Last Modified: Mon, 08 Jun 2020 18:53:20 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7add17715b9f9b7f4adf7b91582039d04239311f783b7b1c8be8e52c60a97a41`  
		Last Modified: Mon, 08 Jun 2020 18:53:20 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db4a3dd149ce5b911704202d9dfa809d57303fd48fc45762642eb9d121bfc64`  
		Last Modified: Mon, 08 Jun 2020 18:54:32 GMT  
		Size: 75.3 MB (75251002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdd51f2fb833202202ffebf7fc1a469502a05c393d501702c9ea804ef2aa456`  
		Last Modified: Mon, 08 Jun 2020 18:53:47 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.8.2`

```console
$ docker pull znc@sha256:7339ba943c41da19ae8c2aa917c4c70f9d1df620c6f28ca0578bc0b62d41a343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v6

### `znc:1.8.2` - linux; arm variant v6

```console
$ docker pull znc@sha256:47740b4e5a6c020aada41ac19c1931c360b7d129267b271ce5f06d67b426e831
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132809194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed893f3b3eb5611fc653b2c70c796c00e2190e482db23d758ce36325b39c39f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Tue, 08 Sep 2020 22:04:03 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 08 Sep 2020 22:04:10 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Tue, 08 Sep 2020 22:04:19 GMT
ARG MAKEFLAGS=
# Tue, 08 Sep 2020 22:04:27 GMT
ENV ZNC_VERSION=1.8.2
# Tue, 08 Sep 2020 22:13:28 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Tue, 08 Sep 2020 22:13:41 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Tue, 08 Sep 2020 22:13:57 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:11 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:25 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:40 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:51 GMT
VOLUME [/znc-data]
# Tue, 08 Sep 2020 22:15:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Sep 2020 22:16:05 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Tue, 08 Sep 2020 22:16:20 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82217ea964091f8c190214bd997420f9132e906b89fed351d36269f6152d586e`  
		Last Modified: Tue, 08 Sep 2020 22:16:54 GMT  
		Size: 43.2 MB (43184125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8954ac8421360fdd845e73456cca768d6e6063c0a97b158edecdd95f999965b7`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523acf9284a5c22a3148b30bdca3b5c4f5fe55e1ae8586a8e282235cc56a4f7c`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aba0fda97135a4280a08db5555814f2b04ae0ffc032f48d47b47a98d6783c15`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd444df6d3a77099159e06342ba5bca06b8dca6d054d79165cabbfa044b5c7f`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766280c07d141fab7909b7e07cbd0a3373166a404354be8fdb200285c9a813d4`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275a81cb106f91a9cc396b3ff0d4d472115391735da996d949d4e960100219c8`  
		Last Modified: Tue, 08 Sep 2020 22:17:34 GMT  
		Size: 87.0 MB (87020019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f02b101b1cfe888ef641b0875361f3640ac62ce395366cb86645a78c69e6a7`  
		Last Modified: Tue, 08 Sep 2020 22:17:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.8.2-slim`

```console
$ docker pull znc@sha256:bd20b978fa8d59980bc3ca32f9bd09ba723811d1b422b76c845c778e981bf964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v6

### `znc:1.8.2-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:2d2fe3d7467f682f7b1962b6e47f29dfeda723a7d7641847db975a99591d15dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45788843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7541c0de651479df78d735885ce26e781c56acc7f9da6835593137563454a3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Tue, 08 Sep 2020 22:04:03 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 08 Sep 2020 22:04:10 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Tue, 08 Sep 2020 22:04:19 GMT
ARG MAKEFLAGS=
# Tue, 08 Sep 2020 22:04:27 GMT
ENV ZNC_VERSION=1.8.2
# Tue, 08 Sep 2020 22:13:28 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Tue, 08 Sep 2020 22:13:41 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Tue, 08 Sep 2020 22:13:57 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:11 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:25 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:40 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:51 GMT
VOLUME [/znc-data]
# Tue, 08 Sep 2020 22:15:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82217ea964091f8c190214bd997420f9132e906b89fed351d36269f6152d586e`  
		Last Modified: Tue, 08 Sep 2020 22:16:54 GMT  
		Size: 43.2 MB (43184125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8954ac8421360fdd845e73456cca768d6e6063c0a97b158edecdd95f999965b7`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523acf9284a5c22a3148b30bdca3b5c4f5fe55e1ae8586a8e282235cc56a4f7c`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aba0fda97135a4280a08db5555814f2b04ae0ffc032f48d47b47a98d6783c15`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd444df6d3a77099159e06342ba5bca06b8dca6d054d79165cabbfa044b5c7f`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766280c07d141fab7909b7e07cbd0a3373166a404354be8fdb200285c9a813d4`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.8-slim`

```console
$ docker pull znc@sha256:f07bb8f669a8d2d9ec4b4a0fc333ccc70cd8f15a32af796c4fb4654f8c53eac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8-slim` - linux; amd64

```console
$ docker pull znc@sha256:befd9ba6f2781b5a6afcc0360dbc8ddaee995cbafa48e642b85e111f235425c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60217659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ad09677c3e952082f8efcdf8f65d8136caefe9e75a481efefe6d5d81de6e21`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2020 19:22:11 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Mon, 04 May 2020 19:22:11 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Mon, 04 May 2020 19:22:11 GMT
ARG MAKEFLAGS=
# Mon, 08 Jun 2020 18:25:56 GMT
ENV ZNC_VERSION=1.8.1
# Mon, 08 Jun 2020 18:30:18 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Mon, 08 Jun 2020 18:30:18 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Mon, 08 Jun 2020 18:30:18 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:30:19 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:30:19 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Mon, 08 Jun 2020 18:30:19 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:30:19 GMT
VOLUME [/znc-data]
# Mon, 08 Jun 2020 18:30:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5a1332069b5686f2953370c761c60ad203b22a4b5d907cddabd5e3766aa49b`  
		Last Modified: Mon, 08 Jun 2020 18:30:56 GMT  
		Size: 57.4 MB (57402945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a3efef78d5bed01124912e52f0e3a0779a6345f5b42c17788d65c978ea7bb7`  
		Last Modified: Mon, 08 Jun 2020 18:30:43 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c3f10758cc9042e43fb6abf244903f8ba5a9dc2a669a9a30b95dc589d21087`  
		Last Modified: Mon, 08 Jun 2020 18:30:43 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83dd650d49b861285b5f22ebeb69e7cf2ef5c693e0648c22b4b78d960a91a9dc`  
		Last Modified: Mon, 08 Jun 2020 18:30:43 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee9947bd59b5d71c18d40c71849c7ed7540188da416129ac186d78cd18b0714`  
		Last Modified: Mon, 08 Jun 2020 18:30:43 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ec4d8b8066c8edda8b14884cea78384b3245fc8ff088524fee89c3409d3389`  
		Last Modified: Mon, 08 Jun 2020 18:30:43 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:2d2fe3d7467f682f7b1962b6e47f29dfeda723a7d7641847db975a99591d15dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45788843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7541c0de651479df78d735885ce26e781c56acc7f9da6835593137563454a3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Tue, 08 Sep 2020 22:04:03 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 08 Sep 2020 22:04:10 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Tue, 08 Sep 2020 22:04:19 GMT
ARG MAKEFLAGS=
# Tue, 08 Sep 2020 22:04:27 GMT
ENV ZNC_VERSION=1.8.2
# Tue, 08 Sep 2020 22:13:28 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Tue, 08 Sep 2020 22:13:41 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Tue, 08 Sep 2020 22:13:57 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:11 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:25 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:40 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:51 GMT
VOLUME [/znc-data]
# Tue, 08 Sep 2020 22:15:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82217ea964091f8c190214bd997420f9132e906b89fed351d36269f6152d586e`  
		Last Modified: Tue, 08 Sep 2020 22:16:54 GMT  
		Size: 43.2 MB (43184125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8954ac8421360fdd845e73456cca768d6e6063c0a97b158edecdd95f999965b7`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523acf9284a5c22a3148b30bdca3b5c4f5fe55e1ae8586a8e282235cc56a4f7c`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aba0fda97135a4280a08db5555814f2b04ae0ffc032f48d47b47a98d6783c15`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd444df6d3a77099159e06342ba5bca06b8dca6d054d79165cabbfa044b5c7f`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766280c07d141fab7909b7e07cbd0a3373166a404354be8fdb200285c9a813d4`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:45db8a930c474ec1b471d330f0d7837817781f442781660d54b83c957d3913d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60038258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6493addde7db3714dc117a9bd647ff1ba622a8bdb5dbceb68954dc4d43a562d7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2020 19:40:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Mon, 04 May 2020 19:40:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Mon, 04 May 2020 19:40:24 GMT
ARG MAKEFLAGS=
# Mon, 08 Jun 2020 18:44:15 GMT
ENV ZNC_VERSION=1.8.1
# Mon, 08 Jun 2020 18:52:37 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Mon, 08 Jun 2020 18:52:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Mon, 08 Jun 2020 18:52:41 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:52:42 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:52:42 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Mon, 08 Jun 2020 18:52:43 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:52:43 GMT
VOLUME [/znc-data]
# Mon, 08 Jun 2020 18:52:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3887515d24b1515c28be3aeca64919edc9acbcff3321a497ba03a160633368`  
		Last Modified: Mon, 08 Jun 2020 18:53:38 GMT  
		Size: 57.3 MB (57312408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79050300cb2ffb98537cb2cfa0f82a803c51cc89a4d952679aed84418b9efdc2`  
		Last Modified: Mon, 08 Jun 2020 18:53:20 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4a6462efa842040fc02cfab1ac30d09819cf8a70034bda884df08f50ff60e6`  
		Last Modified: Mon, 08 Jun 2020 18:53:20 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdbcc0a36123d143db9ab73ea2025356b52af8c3f872e1e2778fba03fb46ff6`  
		Last Modified: Mon, 08 Jun 2020 18:53:20 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deeec6fca5fad8f785f3307d8fbc2886d7c9f565801eded4da2da998260812e2`  
		Last Modified: Mon, 08 Jun 2020 18:53:20 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7add17715b9f9b7f4adf7b91582039d04239311f783b7b1c8be8e52c60a97a41`  
		Last Modified: Mon, 08 Jun 2020 18:53:20 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:latest`

```console
$ docker pull znc@sha256:e093797ff6a40ddd5ee55cc57d33ec0ab8780fe61fed1263e13171eab153df70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:latest` - linux; amd64

```console
$ docker pull znc@sha256:f05fa99cf91c247467afad3c0ad3fd262a6f8f27fccc36a8446837db52f3e6c0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145467376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c6bf2e7b733563835673ce63565322b6186e1049e6634d8dbc0f3f8df1f86`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2020 19:22:11 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Mon, 04 May 2020 19:22:11 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Mon, 04 May 2020 19:22:11 GMT
ARG MAKEFLAGS=
# Mon, 08 Jun 2020 18:25:56 GMT
ENV ZNC_VERSION=1.8.1
# Mon, 08 Jun 2020 18:30:18 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Mon, 08 Jun 2020 18:30:18 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Mon, 08 Jun 2020 18:30:18 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:30:19 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:30:19 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Mon, 08 Jun 2020 18:30:19 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:30:19 GMT
VOLUME [/znc-data]
# Mon, 08 Jun 2020 18:30:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2020 18:30:35 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Mon, 08 Jun 2020 18:30:35 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5a1332069b5686f2953370c761c60ad203b22a4b5d907cddabd5e3766aa49b`  
		Last Modified: Mon, 08 Jun 2020 18:30:56 GMT  
		Size: 57.4 MB (57402945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a3efef78d5bed01124912e52f0e3a0779a6345f5b42c17788d65c978ea7bb7`  
		Last Modified: Mon, 08 Jun 2020 18:30:43 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c3f10758cc9042e43fb6abf244903f8ba5a9dc2a669a9a30b95dc589d21087`  
		Last Modified: Mon, 08 Jun 2020 18:30:43 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83dd650d49b861285b5f22ebeb69e7cf2ef5c693e0648c22b4b78d960a91a9dc`  
		Last Modified: Mon, 08 Jun 2020 18:30:43 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee9947bd59b5d71c18d40c71849c7ed7540188da416129ac186d78cd18b0714`  
		Last Modified: Mon, 08 Jun 2020 18:30:43 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ec4d8b8066c8edda8b14884cea78384b3245fc8ff088524fee89c3409d3389`  
		Last Modified: Mon, 08 Jun 2020 18:30:43 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7115798da545f00a3b605b09ecee681bab84bb9f2a5aa910306504c5fcdf758c`  
		Last Modified: Mon, 08 Jun 2020 18:31:16 GMT  
		Size: 85.2 MB (85249387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82542bfc7155c7556a2ef1fc164c34f30eaf31d36613e32107c0fd122756a45c`  
		Last Modified: Mon, 08 Jun 2020 18:31:01 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:47740b4e5a6c020aada41ac19c1931c360b7d129267b271ce5f06d67b426e831
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132809194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed893f3b3eb5611fc653b2c70c796c00e2190e482db23d758ce36325b39c39f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Tue, 08 Sep 2020 22:04:03 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 08 Sep 2020 22:04:10 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Tue, 08 Sep 2020 22:04:19 GMT
ARG MAKEFLAGS=
# Tue, 08 Sep 2020 22:04:27 GMT
ENV ZNC_VERSION=1.8.2
# Tue, 08 Sep 2020 22:13:28 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Tue, 08 Sep 2020 22:13:41 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Tue, 08 Sep 2020 22:13:57 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:11 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:25 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:40 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:51 GMT
VOLUME [/znc-data]
# Tue, 08 Sep 2020 22:15:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Sep 2020 22:16:05 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Tue, 08 Sep 2020 22:16:20 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82217ea964091f8c190214bd997420f9132e906b89fed351d36269f6152d586e`  
		Last Modified: Tue, 08 Sep 2020 22:16:54 GMT  
		Size: 43.2 MB (43184125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8954ac8421360fdd845e73456cca768d6e6063c0a97b158edecdd95f999965b7`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523acf9284a5c22a3148b30bdca3b5c4f5fe55e1ae8586a8e282235cc56a4f7c`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aba0fda97135a4280a08db5555814f2b04ae0ffc032f48d47b47a98d6783c15`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd444df6d3a77099159e06342ba5bca06b8dca6d054d79165cabbfa044b5c7f`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766280c07d141fab7909b7e07cbd0a3373166a404354be8fdb200285c9a813d4`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275a81cb106f91a9cc396b3ff0d4d472115391735da996d949d4e960100219c8`  
		Last Modified: Tue, 08 Sep 2020 22:17:34 GMT  
		Size: 87.0 MB (87020019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f02b101b1cfe888ef641b0875361f3640ac62ce395366cb86645a78c69e6a7`  
		Last Modified: Tue, 08 Sep 2020 22:17:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:9b1369022519d39413ce456ee0368eaa3a8b6720ba32d9beee434c0bb8ac5c4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135289590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036305fce5a5341a326034ee6b3a8938105ea4cde69ada975d1206a5660a4158`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2020 19:40:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Mon, 04 May 2020 19:40:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Mon, 04 May 2020 19:40:24 GMT
ARG MAKEFLAGS=
# Mon, 08 Jun 2020 18:44:15 GMT
ENV ZNC_VERSION=1.8.1
# Mon, 08 Jun 2020 18:52:37 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Mon, 08 Jun 2020 18:52:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Mon, 08 Jun 2020 18:52:41 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:52:42 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:52:42 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Mon, 08 Jun 2020 18:52:43 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:52:43 GMT
VOLUME [/znc-data]
# Mon, 08 Jun 2020 18:52:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2020 18:53:06 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Mon, 08 Jun 2020 18:53:09 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3887515d24b1515c28be3aeca64919edc9acbcff3321a497ba03a160633368`  
		Last Modified: Mon, 08 Jun 2020 18:53:38 GMT  
		Size: 57.3 MB (57312408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79050300cb2ffb98537cb2cfa0f82a803c51cc89a4d952679aed84418b9efdc2`  
		Last Modified: Mon, 08 Jun 2020 18:53:20 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4a6462efa842040fc02cfab1ac30d09819cf8a70034bda884df08f50ff60e6`  
		Last Modified: Mon, 08 Jun 2020 18:53:20 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdbcc0a36123d143db9ab73ea2025356b52af8c3f872e1e2778fba03fb46ff6`  
		Last Modified: Mon, 08 Jun 2020 18:53:20 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deeec6fca5fad8f785f3307d8fbc2886d7c9f565801eded4da2da998260812e2`  
		Last Modified: Mon, 08 Jun 2020 18:53:20 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7add17715b9f9b7f4adf7b91582039d04239311f783b7b1c8be8e52c60a97a41`  
		Last Modified: Mon, 08 Jun 2020 18:53:20 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db4a3dd149ce5b911704202d9dfa809d57303fd48fc45762642eb9d121bfc64`  
		Last Modified: Mon, 08 Jun 2020 18:54:32 GMT  
		Size: 75.3 MB (75251002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdd51f2fb833202202ffebf7fc1a469502a05c393d501702c9ea804ef2aa456`  
		Last Modified: Mon, 08 Jun 2020 18:53:47 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:slim`

```console
$ docker pull znc@sha256:f07bb8f669a8d2d9ec4b4a0fc333ccc70cd8f15a32af796c4fb4654f8c53eac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:slim` - linux; amd64

```console
$ docker pull znc@sha256:befd9ba6f2781b5a6afcc0360dbc8ddaee995cbafa48e642b85e111f235425c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60217659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ad09677c3e952082f8efcdf8f65d8136caefe9e75a481efefe6d5d81de6e21`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2020 19:22:11 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Mon, 04 May 2020 19:22:11 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Mon, 04 May 2020 19:22:11 GMT
ARG MAKEFLAGS=
# Mon, 08 Jun 2020 18:25:56 GMT
ENV ZNC_VERSION=1.8.1
# Mon, 08 Jun 2020 18:30:18 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Mon, 08 Jun 2020 18:30:18 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Mon, 08 Jun 2020 18:30:18 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:30:19 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:30:19 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Mon, 08 Jun 2020 18:30:19 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:30:19 GMT
VOLUME [/znc-data]
# Mon, 08 Jun 2020 18:30:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5a1332069b5686f2953370c761c60ad203b22a4b5d907cddabd5e3766aa49b`  
		Last Modified: Mon, 08 Jun 2020 18:30:56 GMT  
		Size: 57.4 MB (57402945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a3efef78d5bed01124912e52f0e3a0779a6345f5b42c17788d65c978ea7bb7`  
		Last Modified: Mon, 08 Jun 2020 18:30:43 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c3f10758cc9042e43fb6abf244903f8ba5a9dc2a669a9a30b95dc589d21087`  
		Last Modified: Mon, 08 Jun 2020 18:30:43 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83dd650d49b861285b5f22ebeb69e7cf2ef5c693e0648c22b4b78d960a91a9dc`  
		Last Modified: Mon, 08 Jun 2020 18:30:43 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee9947bd59b5d71c18d40c71849c7ed7540188da416129ac186d78cd18b0714`  
		Last Modified: Mon, 08 Jun 2020 18:30:43 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ec4d8b8066c8edda8b14884cea78384b3245fc8ff088524fee89c3409d3389`  
		Last Modified: Mon, 08 Jun 2020 18:30:43 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:2d2fe3d7467f682f7b1962b6e47f29dfeda723a7d7641847db975a99591d15dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45788843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7541c0de651479df78d735885ce26e781c56acc7f9da6835593137563454a3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Tue, 08 Sep 2020 22:04:03 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 08 Sep 2020 22:04:10 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Tue, 08 Sep 2020 22:04:19 GMT
ARG MAKEFLAGS=
# Tue, 08 Sep 2020 22:04:27 GMT
ENV ZNC_VERSION=1.8.2
# Tue, 08 Sep 2020 22:13:28 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Tue, 08 Sep 2020 22:13:41 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Tue, 08 Sep 2020 22:13:57 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:11 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:25 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:40 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Tue, 08 Sep 2020 22:14:51 GMT
VOLUME [/znc-data]
# Tue, 08 Sep 2020 22:15:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82217ea964091f8c190214bd997420f9132e906b89fed351d36269f6152d586e`  
		Last Modified: Tue, 08 Sep 2020 22:16:54 GMT  
		Size: 43.2 MB (43184125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8954ac8421360fdd845e73456cca768d6e6063c0a97b158edecdd95f999965b7`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523acf9284a5c22a3148b30bdca3b5c4f5fe55e1ae8586a8e282235cc56a4f7c`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aba0fda97135a4280a08db5555814f2b04ae0ffc032f48d47b47a98d6783c15`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd444df6d3a77099159e06342ba5bca06b8dca6d054d79165cabbfa044b5c7f`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766280c07d141fab7909b7e07cbd0a3373166a404354be8fdb200285c9a813d4`  
		Last Modified: Tue, 08 Sep 2020 22:16:39 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:45db8a930c474ec1b471d330f0d7837817781f442781660d54b83c957d3913d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60038258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6493addde7db3714dc117a9bd647ff1ba622a8bdb5dbceb68954dc4d43a562d7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2020 19:40:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Mon, 04 May 2020 19:40:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Mon, 04 May 2020 19:40:24 GMT
ARG MAKEFLAGS=
# Mon, 08 Jun 2020 18:44:15 GMT
ENV ZNC_VERSION=1.8.1
# Mon, 08 Jun 2020 18:52:37 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Mon, 08 Jun 2020 18:52:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Mon, 08 Jun 2020 18:52:41 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:52:42 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:52:42 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Mon, 08 Jun 2020 18:52:43 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Mon, 08 Jun 2020 18:52:43 GMT
VOLUME [/znc-data]
# Mon, 08 Jun 2020 18:52:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3887515d24b1515c28be3aeca64919edc9acbcff3321a497ba03a160633368`  
		Last Modified: Mon, 08 Jun 2020 18:53:38 GMT  
		Size: 57.3 MB (57312408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79050300cb2ffb98537cb2cfa0f82a803c51cc89a4d952679aed84418b9efdc2`  
		Last Modified: Mon, 08 Jun 2020 18:53:20 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4a6462efa842040fc02cfab1ac30d09819cf8a70034bda884df08f50ff60e6`  
		Last Modified: Mon, 08 Jun 2020 18:53:20 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdbcc0a36123d143db9ab73ea2025356b52af8c3f872e1e2778fba03fb46ff6`  
		Last Modified: Mon, 08 Jun 2020 18:53:20 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deeec6fca5fad8f785f3307d8fbc2886d7c9f565801eded4da2da998260812e2`  
		Last Modified: Mon, 08 Jun 2020 18:53:20 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7add17715b9f9b7f4adf7b91582039d04239311f783b7b1c8be8e52c60a97a41`  
		Last Modified: Mon, 08 Jun 2020 18:53:20 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
