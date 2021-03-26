## `znc:latest`

```console
$ docker pull znc@sha256:63b4279c5cc6d277d36909b6ce8c631bfb3274ada95220f038dc5e8c2ed15bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:latest` - linux; amd64

```console
$ docker pull znc@sha256:06f36fd86b43a8e7734f8170934e9d4fa5bbc6a94ce90f965882edf9f6f0f20d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150968904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c803978ff1716d522e2dbb48cf667a2933030683dec6170898f8ea135ffb72e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:49:36 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 26 Mar 2021 02:49:37 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 26 Mar 2021 02:49:37 GMT
ARG MAKEFLAGS=
# Fri, 26 Mar 2021 02:49:37 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 26 Mar 2021 02:55:28 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 26 Mar 2021 02:55:28 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 26 Mar 2021 02:55:28 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Fri, 26 Mar 2021 02:55:29 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Fri, 26 Mar 2021 02:55:29 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Fri, 26 Mar 2021 02:55:29 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Fri, 26 Mar 2021 02:55:29 GMT
VOLUME [/znc-data]
# Fri, 26 Mar 2021 02:55:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 02:55:39 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Fri, 26 Mar 2021 02:55:39 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef753c00beaf06a3ee7647f2da37af968d3c33b9655927a8d6aca2d1d995e28c`  
		Last Modified: Fri, 26 Mar 2021 02:56:04 GMT  
		Size: 44.8 MB (44790585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9739f8a41ed5c01a8660fa107743ba3fb79709cdf9fd584ea4298252afa54a14`  
		Last Modified: Fri, 26 Mar 2021 02:55:52 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f021d06d531c1dbf7b87991e227094bb17ed380b2aeac36c819c64fad6cf9cc`  
		Last Modified: Fri, 26 Mar 2021 02:55:53 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db01e30df5558a3c24faf6d409e32758133a06c2e2145417d83e1cbeb3e4aee`  
		Last Modified: Fri, 26 Mar 2021 02:55:52 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afac7b001b7aa8a0b0dbd7c72ca4b057cf50099234a4751ab06b4e33b5a17f10`  
		Last Modified: Fri, 26 Mar 2021 02:55:52 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee18e3181ce87afeaaadc596532013194e9cc8132f0c58f8d235f7f9295e734`  
		Last Modified: Fri, 26 Mar 2021 02:55:52 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7585d98d7ae0ca7844e2d481de40ee8bfee40e04d9afa6d3c57a664165d40cc0`  
		Last Modified: Fri, 26 Mar 2021 02:56:35 GMT  
		Size: 103.4 MB (103376800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3bd687d2611b904fa018ddbec55747e33a4ef0747e568c2976c11c595859cc`  
		Last Modified: Fri, 26 Mar 2021 02:56:17 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:6a449eb5765171573b6e4b91369372bc641cd3a113a58de9ceee26a5588cb22d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132673605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747dc9a064a095004554fec21a0d018426b1b01e3ebb2d43b2a5424fb9466362`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:50:43 GMT
ADD file:65a3462a527f49c8c625927be6b8b57b4257c8cc37d685055a1f183d76c68920 in / 
# Thu, 25 Mar 2021 22:50:47 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 10:12:50 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 26 Mar 2021 10:12:52 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 26 Mar 2021 10:12:53 GMT
ARG MAKEFLAGS=
# Fri, 26 Mar 2021 10:12:54 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 26 Mar 2021 10:21:17 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 26 Mar 2021 10:21:19 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 26 Mar 2021 10:21:20 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Fri, 26 Mar 2021 10:21:21 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Fri, 26 Mar 2021 10:21:23 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Fri, 26 Mar 2021 10:21:24 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Fri, 26 Mar 2021 10:21:25 GMT
VOLUME [/znc-data]
# Fri, 26 Mar 2021 10:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 10:21:59 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Fri, 26 Mar 2021 10:22:02 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:181a1446f0acaaa0871cec07aba4f733041f2d80ffbe01b19df43fe005df29f3`  
		Last Modified: Thu, 25 Mar 2021 22:55:06 GMT  
		Size: 2.6 MB (2604815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0982423e7ae754c069956d580e1acaca3e66a55226c9278186c5e968762152`  
		Last Modified: Fri, 26 Mar 2021 10:22:37 GMT  
		Size: 43.0 MB (43047470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a6dab70842fd7ecb0941421cfdc83583257388d0b9e2c4fe37a2e274528a1a`  
		Last Modified: Fri, 26 Mar 2021 10:22:20 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac8ece3256d78ffb62f9faba6d74c742a1a3108e9dd08a08cac15d6f3fdba99`  
		Last Modified: Fri, 26 Mar 2021 10:22:20 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0b52ec48c1b6e16295fdd380f99ab5dcd22d4958e551ef4c420b233975f2a6`  
		Last Modified: Fri, 26 Mar 2021 10:22:21 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5a2f289f7c171815ae10f6d69cba36b438cc64d018f82007389981c11a00e0`  
		Last Modified: Fri, 26 Mar 2021 10:22:20 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1350b1a43ad95790dc342884c6ab68d3b55066fa3a8c6cd86bddd7187d73f81e`  
		Last Modified: Fri, 26 Mar 2021 10:22:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68793b9aa6bb49993044686abc70313f5c5f508ea5fa70339d6d4cfd1aa0bff9`  
		Last Modified: Fri, 26 Mar 2021 10:23:17 GMT  
		Size: 87.0 MB (87019565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a43393af528896993bec84436872fe1e484022cfba3ad14eb8d2f78e4a2935a`  
		Last Modified: Fri, 26 Mar 2021 10:22:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:867d8008e3c661f2f36ae5de43c0d8761c09394f6efa432fb9755f41388ad2de
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138119258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9dbdb0d56d42b79e772164b24015a6b6eb5f3df3a9d7c74e803e51ce2f1f2e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:00 GMT
ADD file:97aac29a9ffbba2c76441891035010395614dc3115c4710d58932205b604308f in / 
# Thu, 25 Mar 2021 22:41:10 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:50:00 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 26 Mar 2021 08:50:01 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 26 Mar 2021 08:50:01 GMT
ARG MAKEFLAGS=
# Fri, 26 Mar 2021 08:50:02 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 26 Mar 2021 08:58:39 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 26 Mar 2021 08:58:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 26 Mar 2021 08:58:41 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Fri, 26 Mar 2021 08:58:43 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Fri, 26 Mar 2021 08:58:44 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Fri, 26 Mar 2021 08:58:45 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Fri, 26 Mar 2021 08:58:46 GMT
VOLUME [/znc-data]
# Fri, 26 Mar 2021 08:58:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 08:59:09 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Fri, 26 Mar 2021 08:59:12 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:95dec6db372224fc1909f0d0c0a9a9d5767ec6b78d066ff6a7d5723160037828`  
		Last Modified: Thu, 25 Mar 2021 22:45:23 GMT  
		Size: 2.7 MB (2709692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261b1493d1cb2458295caac1ef25dd52633a9918efc444ba17cc51219d26a8d9`  
		Last Modified: Fri, 26 Mar 2021 08:59:40 GMT  
		Size: 44.6 MB (44634463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2281c6206ad9e01aeba3f087c93c093edf03b65b013c1e5f30f1c1cc74e9d4d`  
		Last Modified: Fri, 26 Mar 2021 08:59:27 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6757db4ee2933909c092344b92ea6da1ae5f0cb9dc22909417c149a6c7230e6`  
		Last Modified: Fri, 26 Mar 2021 08:59:27 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1812d97bc4f8773fb4157ee1040400c92ba44a0f4cb42ee1d3968738f711d30`  
		Last Modified: Fri, 26 Mar 2021 08:59:26 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ed828033ac4f4536b200687724afd662cadc3cadab7be191836076e23b0a8`  
		Last Modified: Fri, 26 Mar 2021 08:59:26 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351579885da0be0c3e00c76b547db0e55bdeeba9d93a2a5bc221e79e44d1cdb`  
		Last Modified: Fri, 26 Mar 2021 08:59:26 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2c89f681197b95d37c9eca50392af5784da5bba01a0b5b061626be357271a1`  
		Last Modified: Fri, 26 Mar 2021 09:00:18 GMT  
		Size: 90.8 MB (90773349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6446c82cbc42091f0d17d84181f2a84c5a3c8a6fbba3169b39554bb92d3241`  
		Last Modified: Fri, 26 Mar 2021 08:59:52 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
