## `znc:latest`

```console
$ docker pull znc@sha256:6b1bec9f8da3866919f49ffcb1e850c050f0f65192170ef820de8104b7dc0a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:latest` - linux; amd64

```console
$ docker pull znc@sha256:792086307563b65168174df9db9fc1248ca342439a1f2c2e558d3cddc7793d59
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141035369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9846126f9a1644eac75ca66a376fceb1ed1cd2907da04d5b026fd27a62f8df2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2020 06:03:41 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 24 Jan 2020 06:03:42 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 24 Jan 2020 06:03:42 GMT
ARG MAKEFLAGS=
# Fri, 24 Jan 2020 06:03:42 GMT
ENV ZNC_VERSION=1.7.5
# Fri, 24 Jan 2020 06:09:40 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 24 Jan 2020 06:09:41 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 24 Jan 2020 06:09:41 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Fri, 24 Jan 2020 06:09:41 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Fri, 24 Jan 2020 06:09:41 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Fri, 24 Jan 2020 06:09:41 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Fri, 24 Jan 2020 06:09:42 GMT
VOLUME [/znc-data]
# Fri, 24 Jan 2020 06:09:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2020 06:10:09 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Fri, 24 Jan 2020 06:10:09 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d431a7a850a5f025178c3f777f5088d9b146ee379cb5d825a5c8a9f60fa33f3`  
		Last Modified: Fri, 24 Jan 2020 06:10:58 GMT  
		Size: 57.2 MB (57150897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeac081eeec39f38f5555ba19b6e37545ee73d545b5c130b85958178481d75e3`  
		Last Modified: Fri, 24 Jan 2020 06:10:20 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ce8bd72a7bafeeb0c4f3d839bd97e139d9dae2d46aa7457128c81ad9ee8f5c`  
		Last Modified: Fri, 24 Jan 2020 06:10:20 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77728f03247ad0f4eda096aafd7cebfbf697a71fbb345f46f2023acdf6b3b885`  
		Last Modified: Fri, 24 Jan 2020 06:10:20 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3946d71a165cf02480f9040255c376da9a9f1df968ca958886bd6f57edb318`  
		Last Modified: Fri, 24 Jan 2020 06:10:20 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21228b04c92627db7b8d28dfc3932db82bddb24cdf469656de9412d4383012c`  
		Last Modified: Fri, 24 Jan 2020 06:10:20 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f3fbaa1b2909e9c3f05cd072414687b6fa6fe3b00cc8eacc2b75d702519ade`  
		Last Modified: Fri, 24 Jan 2020 06:11:27 GMT  
		Size: 81.1 MB (81095782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1c012f32f3cc925b0da06af80edb5df381684225b31882305cb5807e608b80`  
		Last Modified: Fri, 24 Jan 2020 06:11:04 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:5f14d3ecd12d3145974f3b147148bced0c8723013344b3848be5c6a34125ae5f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126815571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bd94a7e565e5a0c8a62eb79310f0ec76b3150f4cbed425f77dfc7e0975f399`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:2aa80d52585a6b34b2cc5811d46965a084e50cfb8cd183f1a88b2b1bc6556e1f in / 
# Thu, 23 Jan 2020 16:53:28 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 20:56:37 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Thu, 23 Jan 2020 20:56:37 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Thu, 23 Jan 2020 20:56:38 GMT
ARG MAKEFLAGS=
# Thu, 23 Jan 2020 20:56:39 GMT
ENV ZNC_VERSION=1.7.5
# Thu, 23 Jan 2020 21:05:00 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Thu, 23 Jan 2020 21:05:03 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Thu, 23 Jan 2020 21:05:03 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Thu, 23 Jan 2020 21:05:04 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Thu, 23 Jan 2020 21:05:04 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Thu, 23 Jan 2020 21:05:05 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Thu, 23 Jan 2020 21:05:05 GMT
VOLUME [/znc-data]
# Thu, 23 Jan 2020 21:05:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 21:05:35 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Thu, 23 Jan 2020 21:05:37 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:896868b7b9168cabb308702db96dc9769d10c23e20fc66f5f4abedf4c75d7642`  
		Last Modified: Thu, 23 Jan 2020 16:54:07 GMT  
		Size: 2.6 MB (2571407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f646e7e71ebccab4b1fd906d140b5fab547701a88ad78b01404e4f64977e8f5a`  
		Last Modified: Thu, 23 Jan 2020 21:06:13 GMT  
		Size: 54.9 MB (54929733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6240c69e595f7aa407cbda1c18b7334fd3835a6c564db6170ddd0c5b0aee8970`  
		Last Modified: Thu, 23 Jan 2020 21:05:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cfe3a21b36b65f88bfcc48c0afd53d160972793ac5990241f04a4ecd98ebe7`  
		Last Modified: Thu, 23 Jan 2020 21:05:48 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921b737ffe2a02023dd047793c179ab6b66372804e516816e56841337f6ac031`  
		Last Modified: Thu, 23 Jan 2020 21:05:51 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719ed2abaeabf3bae538c081751ae24e1f7aa3e1e6ffd2daa69fbab5795a7bab`  
		Last Modified: Thu, 23 Jan 2020 21:05:48 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47ff4b7222d42a58a483b5fadaf8cc3faaeadedcc439b7e8221e5a75e07abb1`  
		Last Modified: Thu, 23 Jan 2020 21:05:48 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:504e2e49c2adf71db912ee04ff14d2c7be03954e091b10239c8580411dfc8ecb`  
		Last Modified: Thu, 23 Jan 2020 21:06:50 GMT  
		Size: 69.3 MB (69312676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02038cf0452afb3264dc3102497b32eb459d6e6211e3aef90430f805beb747f`  
		Last Modified: Thu, 23 Jan 2020 21:06:21 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:8497a8aeeda6b0730266cdbcfc425424353908d3d0ce163e402d647c8fd6b6b7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133123411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcdc8b15ffcba76c2fe2f09927b76a88c106b03ce2b3807982f8ad61379190f7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:39 GMT
ADD file:bdfbd4b0dfb53eecc80bac65894d1e2fcfafb27dcf24ab019176e2c9f60b9a39 in / 
# Thu, 23 Jan 2020 16:54:40 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 23:29:58 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Thu, 23 Jan 2020 23:29:59 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Thu, 23 Jan 2020 23:30:00 GMT
ARG MAKEFLAGS=
# Thu, 23 Jan 2020 23:30:01 GMT
ENV ZNC_VERSION=1.7.5
# Thu, 23 Jan 2020 23:39:17 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Thu, 23 Jan 2020 23:39:20 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Thu, 23 Jan 2020 23:39:21 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Thu, 23 Jan 2020 23:39:21 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Thu, 23 Jan 2020 23:39:22 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Thu, 23 Jan 2020 23:39:22 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Thu, 23 Jan 2020 23:39:23 GMT
VOLUME [/znc-data]
# Thu, 23 Jan 2020 23:39:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 23:39:48 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Thu, 23 Jan 2020 23:39:50 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:f07e4bcf42b862c240f4c00f2f7ed362d7d93ca15151de547beda593f3b669e5`  
		Last Modified: Thu, 23 Jan 2020 16:55:24 GMT  
		Size: 2.7 MB (2717732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3b47418bf3a6e5d2778b748061c50a7518c6554c0d3ec81d6d608530d78679`  
		Last Modified: Thu, 23 Jan 2020 23:40:25 GMT  
		Size: 57.1 MB (57144077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f98e527749796085630187d3f964dd3718db09ff97587fdc5195f68795e9b92`  
		Last Modified: Thu, 23 Jan 2020 23:40:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d580c323b6dee1733c0c7210d8e203b178782bf67bea74d779ce609e775b6d6a`  
		Last Modified: Thu, 23 Jan 2020 23:40:01 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8d290025141c446610989abd8ac637f56cf93cba54a50b4b2b2d37c7588afc`  
		Last Modified: Thu, 23 Jan 2020 23:40:01 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bb431ea14ba15dbea9a83c016a06a3c001c14bd48b3fd4c90e1cbbb5d81706`  
		Last Modified: Thu, 23 Jan 2020 23:40:01 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd070f6b75d343824eaf1daec8e97b268c4b16280c69285af0b51915186d4c0c`  
		Last Modified: Thu, 23 Jan 2020 23:40:01 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ae45375592048973050782ae12ab1805b934022f9a7fb0724f538120da267c`  
		Last Modified: Thu, 23 Jan 2020 23:40:58 GMT  
		Size: 73.3 MB (73259842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e84c297ba8f182bce571f9b95d0bf3f39844cee063d6f2f5b0ae82703005a1`  
		Last Modified: Thu, 23 Jan 2020 23:40:33 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
