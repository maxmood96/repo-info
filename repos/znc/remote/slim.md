## `znc:slim`

```console
$ docker pull znc@sha256:5c24c6f06735a81010ff3c480a64dcee7b5a4038549b6ef72a4f51238f553df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:slim` - linux; amd64

```console
$ docker pull znc@sha256:63a2de96ee16efca8e0f36216d6653d0ee34646e25d620d3bfd4745af1018c93
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47359439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67a97f125e909d872072d2586cf2cb9e4e71b0b8ca84e1c1a6079f986f46ece`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:58:41 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 11 Dec 2020 02:58:41 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 11 Dec 2020 02:58:41 GMT
ARG MAKEFLAGS=
# Fri, 11 Dec 2020 02:58:41 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 11 Dec 2020 03:04:58 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 11 Dec 2020 03:04:59 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 11 Dec 2020 03:04:59 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Fri, 11 Dec 2020 03:05:00 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Fri, 11 Dec 2020 03:05:00 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Fri, 11 Dec 2020 03:05:00 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Fri, 11 Dec 2020 03:05:00 GMT
VOLUME [/znc-data]
# Fri, 11 Dec 2020 03:05:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57e0a0d721075aff41f2227ea83044ddda0b4afaaa8dd922e0b12d10c85f5ca`  
		Last Modified: Fri, 11 Dec 2020 03:05:55 GMT  
		Size: 44.6 MB (44561100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2073b962af9cd96c54f17d308f1c4a67b8ccb872a8a033b7d1e9b4ae748e6f30`  
		Last Modified: Fri, 11 Dec 2020 03:05:43 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3b9973333fd68f4e0e03509daef45327575a0ecf60989b47b0fda013bcb87`  
		Last Modified: Fri, 11 Dec 2020 03:05:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993dfe378ea75a077d968f140037ac8fb081756951374e81f9f80f44905644ef`  
		Last Modified: Fri, 11 Dec 2020 03:05:42 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ab289eda1213c4054cef7dda7c63a605d2f1d2241f6def781bfd203ddd522b`  
		Last Modified: Fri, 11 Dec 2020 03:05:42 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c0ab7ef77192afe5ae14e997d6c64551a7a94251c93cb8c8c015f22cf8bfe4`  
		Last Modified: Fri, 11 Dec 2020 03:05:43 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:24eeaf0d0606e4ccb855a64428e2917a294cbcdd3cfa8562f5c04f711f3f0788
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45412960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd7b4ab4046c4df5d3143d3b982eba8b7d62c470a53654de2ffed4f95f82720`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:34:27 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 11 Dec 2020 02:34:28 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 11 Dec 2020 02:34:28 GMT
ARG MAKEFLAGS=
# Fri, 11 Dec 2020 02:34:29 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 11 Dec 2020 02:42:54 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 11 Dec 2020 02:42:58 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 11 Dec 2020 02:43:00 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Fri, 11 Dec 2020 02:43:01 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Fri, 11 Dec 2020 02:43:02 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Fri, 11 Dec 2020 02:43:03 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Fri, 11 Dec 2020 02:43:04 GMT
VOLUME [/znc-data]
# Fri, 11 Dec 2020 02:43:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043b4c6bc8cfa950eb03e926e1130e4825d522bf66267e02e9c9036e8629cc99`  
		Last Modified: Fri, 11 Dec 2020 02:44:20 GMT  
		Size: 42.8 MB (42809541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0845ae291286fa4622fac61300800cbef3c9853de74e3bf9c9546f1a02172840`  
		Last Modified: Fri, 11 Dec 2020 02:44:02 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f183aec44f89308458daa4e7cff8ff2dd9b5dd8bd65b3b57c137dfd7cb7d519`  
		Last Modified: Fri, 11 Dec 2020 02:44:02 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8cb45344b405a2764aa750d8337e1db7a395489e8af2116fa7f585e19b032c`  
		Last Modified: Fri, 11 Dec 2020 02:44:02 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280d32b89b6c626c2ed5a5fe058e004d3841bb6738fda663e203496a08d6fa03`  
		Last Modified: Fri, 11 Dec 2020 02:44:03 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fafcc5c3dd3e14c609ae721b2e43cbdef55c49b54e658c3edf2c5351d21b6b40`  
		Last Modified: Fri, 11 Dec 2020 02:44:03 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:be3c031c422e9dc4116dfd74c0f2cc651016f2bc46af80e8d6e1925e2973d138
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46991596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccd6fc946d85d81bc6874201425f7e3ba05449ae7f0e8df2334df9be85efa12`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 09:01:42 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Thu, 22 Oct 2020 09:01:45 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Thu, 22 Oct 2020 09:01:48 GMT
ARG MAKEFLAGS=
# Thu, 22 Oct 2020 09:01:50 GMT
ENV ZNC_VERSION=1.8.2
# Thu, 22 Oct 2020 09:10:37 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Thu, 22 Oct 2020 09:10:42 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Thu, 22 Oct 2020 09:10:44 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Thu, 22 Oct 2020 09:10:46 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Thu, 22 Oct 2020 09:10:47 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Thu, 22 Oct 2020 09:10:48 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Thu, 22 Oct 2020 09:10:49 GMT
VOLUME [/znc-data]
# Thu, 22 Oct 2020 09:10:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e69975ef2f071f47e6a8159018b0000af3316f435fb29b5e12f80bf23b0865`  
		Last Modified: Thu, 22 Oct 2020 09:11:48 GMT  
		Size: 44.3 MB (44283612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bfd76a6014b83f46b976d0c98dafebcf9e6a91e832788475c5ff60794ae02b`  
		Last Modified: Thu, 22 Oct 2020 09:11:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d791235545f3c8e17af33e674365b13808cc6348a52c0dc3ec48723eee0e61`  
		Last Modified: Thu, 22 Oct 2020 09:11:35 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7e28d6f56306765f31465d151ca375f40116b5f37d3e5e5a09b02f164bf94e`  
		Last Modified: Thu, 22 Oct 2020 09:11:35 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8c670d0a39679602a9fa0b0a413c87efddceeedd82dc9127eb44c77a4b10df`  
		Last Modified: Thu, 22 Oct 2020 09:11:36 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7fefce2f133a082ab2963d6a2ef3843f0bbec30c94ce4379cfcaff169dda03c`  
		Last Modified: Thu, 22 Oct 2020 09:11:35 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
