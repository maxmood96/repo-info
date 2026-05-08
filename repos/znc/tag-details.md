<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `znc`

-	[`znc:1.10`](#znc110)
-	[`znc:1.10-slim`](#znc110-slim)
-	[`znc:1.10.2`](#znc1102)
-	[`znc:1.10.2-slim`](#znc1102-slim)
-	[`znc:latest`](#znclatest)
-	[`znc:slim`](#zncslim)

## `znc:1.10`

```console
$ docker pull znc@sha256:c731c6a9b8b63f283aecbcdbee236574c6b05995766574213422c365db429147
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `znc:1.10` - linux; amd64

```console
$ docker pull znc@sha256:e37f0a533d35fe23e0a37b14f27c6a94de5e41ab7699fc6068c2bbdb242a4478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169364545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf50b4b7cb015939d2bd51213202b072973a606c379b71af0982e3a6ec0aac5d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:25:12 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 17 Apr 2026 00:25:12 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 17 Apr 2026 00:25:12 GMT
ARG MAKEFLAGS=
# Fri, 17 Apr 2026 00:25:12 GMT
ENV ZNC_VERSION=1.10.1
# Fri, 17 Apr 2026 00:25:12 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Fri, 17 Apr 2026 00:25:12 GMT
COPY entrypoint.sh / # buildkit
# Fri, 17 Apr 2026 00:25:12 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Fri, 17 Apr 2026 00:25:12 GMT
VOLUME [/znc-data]
# Fri, 17 Apr 2026 00:25:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 01:13:19 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Fri, 17 Apr 2026 01:13:19 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab87e5c08dbaa94f2abe60a96c74f3d65dcedb1f7235faf6090204fc191e4544`  
		Last Modified: Fri, 17 Apr 2026 00:25:24 GMT  
		Size: 46.0 MB (46023713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2182e80f9ad42f6496030d84016d16b92e151e06b4e016cd308c0fac0b4a8a42`  
		Last Modified: Fri, 17 Apr 2026 00:25:22 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35aa1571b1b2f924731940bf8358cda86cf72a8b2a20d2346918dfac1af56c0`  
		Last Modified: Fri, 17 Apr 2026 00:25:22 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c139231a03fbbf6fe759b85db4425833b4fd87e657002f0dea00e5fe85e5b418`  
		Last Modified: Fri, 17 Apr 2026 01:13:42 GMT  
		Size: 119.5 MB (119531388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c13837f80dbf618f1b43bac44de79e819083b359f857f0a82a662a6f13dc9b0`  
		Last Modified: Fri, 17 Apr 2026 01:13:39 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10` - unknown; unknown

```console
$ docker pull znc@sha256:808537df43bf21a94bb31ecca0a1872eca5920e458a5e7a2606c3a483509adae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6869975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cda17cb8b73bcdd9024e5b93d1a648d517d49cd5817dda890f545056539ec5f`

```dockerfile
```

-	Layers:
	-	`sha256:aef6e0ee47e4e01d1f2779171f6d3b1fb2e3eed807b7d9248e05dc2ca068e7d7`  
		Last Modified: Fri, 17 Apr 2026 01:13:39 GMT  
		Size: 6.9 MB (6860415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b1c335c30bc24e240ac92e9c1c372fda79c9591b407b733547bffeb2aeaa20f`  
		Last Modified: Fri, 17 Apr 2026 01:13:39 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10` - linux; arm variant v6

```console
$ docker pull znc@sha256:3aa535594ba7579fd38b8c6827f0f05953be6ead3599cb2faeb9a8ba4ec41f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148658031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42bbf9efb0eb17e16887d4c45d9d243d49b521d17fe8b1cdd5c2716e372e69a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:39 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 17 Apr 2026 00:32:39 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 17 Apr 2026 00:32:39 GMT
ARG MAKEFLAGS=
# Fri, 17 Apr 2026 00:32:39 GMT
ENV ZNC_VERSION=1.10.1
# Fri, 17 Apr 2026 00:32:39 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Fri, 17 Apr 2026 00:32:39 GMT
COPY entrypoint.sh / # buildkit
# Fri, 17 Apr 2026 00:32:39 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Fri, 17 Apr 2026 00:32:39 GMT
VOLUME [/znc-data]
# Fri, 17 Apr 2026 00:32:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 01:12:37 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Fri, 17 Apr 2026 01:12:37 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966ee517e4aa87f280941db01d122485043381c8d9af87cb4de293fb92c16ef1`  
		Last Modified: Fri, 17 Apr 2026 00:32:48 GMT  
		Size: 44.6 MB (44608529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b94e4faa7c02667627fa6948e955f05851c0207a9bb17dbc81090eeb3e5bbcd`  
		Last Modified: Fri, 17 Apr 2026 00:32:47 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bd26bb3234b7a6756fb2372a754b64d573f4b32e1fd5d705ac7d8679bfe7bd`  
		Last Modified: Fri, 17 Apr 2026 00:32:47 GMT  
		Size: 751.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb263554f52dbaa15d11a1ca4dd63d63c1a6e5c6792b0ecb827810a3dd7bb13d`  
		Last Modified: Fri, 17 Apr 2026 01:12:54 GMT  
		Size: 100.5 MB (100540865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b516220b86528d08d38772121d958b316017231f425a341d65b16088e1d095`  
		Last Modified: Fri, 17 Apr 2026 01:12:51 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10` - unknown; unknown

```console
$ docker pull znc@sha256:28844ae9b0d30e5246be2a9125184b386f00ca2aa02f48ace568f3381af4227f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b882c6152b6a077f3636516f7ae08303024b3e369f1382deb6545d4e965331`

```dockerfile
```

-	Layers:
	-	`sha256:c5ceb5a7c6f10bf877b76624dbaa69b7eff517393c227dfde0e0f48d6138223b`  
		Last Modified: Fri, 17 Apr 2026 01:12:51 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:27f44b5cda925b501ec43222c037adbf6fb969c6acd7c72a68343e8259babec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163127873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d847cfc8d2c616240c6e59892a03151df10c952582731bd8a0232fff5c8b07`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:27:38 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 17 Apr 2026 00:27:38 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 17 Apr 2026 00:27:38 GMT
ARG MAKEFLAGS=
# Fri, 17 Apr 2026 00:27:38 GMT
ENV ZNC_VERSION=1.10.1
# Fri, 17 Apr 2026 00:27:38 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Fri, 17 Apr 2026 00:27:38 GMT
COPY entrypoint.sh / # buildkit
# Fri, 17 Apr 2026 00:27:38 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Fri, 17 Apr 2026 00:27:38 GMT
VOLUME [/znc-data]
# Fri, 17 Apr 2026 00:27:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 01:34:36 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Fri, 17 Apr 2026 01:34:36 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10c085ab11c93dc230c7b70da849b0449e854ed31522b9758b4214b47506da5`  
		Last Modified: Fri, 17 Apr 2026 00:27:49 GMT  
		Size: 45.8 MB (45821426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3755031d12e56fe753125278f020485273ff494877fa4b598747df17985261ef`  
		Last Modified: Fri, 17 Apr 2026 00:27:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c2bd649a20601af73ae1bfd32fa4bc5ea011a3a38d7ba80fcf8b868acdf488`  
		Last Modified: Fri, 17 Apr 2026 00:27:48 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f07692eb313edf8bfb5c38af72bc0376841e3f33c6afdbb2482c7d02c56d03`  
		Last Modified: Fri, 17 Apr 2026 01:34:59 GMT  
		Size: 113.2 MB (113163302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49bdd732e07fcb6267a35c9b6a76253b5e218253a838db2ae6cb6dd610a6f26`  
		Last Modified: Fri, 17 Apr 2026 01:34:56 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10` - unknown; unknown

```console
$ docker pull znc@sha256:229e390099a6041c554dc3ee3aff9929826edd00d66c081ef53bebeaaa06ca34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6949491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c050a4379214458e94157f7c20e7936db2853c9d1cc6b89f0b256380d1202f67`

```dockerfile
```

-	Layers:
	-	`sha256:f054058310935024ec64ff515dcf3ab715483359f53515628e240b14df2086e5`  
		Last Modified: Fri, 17 Apr 2026 01:34:56 GMT  
		Size: 6.9 MB (6939839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf325017a9a249cbfc71c8a1c1cf6505304cef767c1d5077fb099c060d3bcf53`  
		Last Modified: Fri, 17 Apr 2026 01:34:55 GMT  
		Size: 9.7 KB (9652 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.10-slim`

```console
$ docker pull znc@sha256:f9e8b560438735ef045f419054e96b54fc3ef23d10a5c48a0323b1e675ae9a42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `znc:1.10-slim` - linux; amd64

```console
$ docker pull znc@sha256:e228716553b8b3030b3f258f663561fcd5efeac1038451ade040d31705b90d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49832826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8daa794f654e88fafa0dc001362b980f1f6b6b7fb19536a66c7b3a3020cadf70`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:25:12 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 17 Apr 2026 00:25:12 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 17 Apr 2026 00:25:12 GMT
ARG MAKEFLAGS=
# Fri, 17 Apr 2026 00:25:12 GMT
ENV ZNC_VERSION=1.10.1
# Fri, 17 Apr 2026 00:25:12 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Fri, 17 Apr 2026 00:25:12 GMT
COPY entrypoint.sh / # buildkit
# Fri, 17 Apr 2026 00:25:12 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Fri, 17 Apr 2026 00:25:12 GMT
VOLUME [/znc-data]
# Fri, 17 Apr 2026 00:25:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab87e5c08dbaa94f2abe60a96c74f3d65dcedb1f7235faf6090204fc191e4544`  
		Last Modified: Fri, 17 Apr 2026 00:25:24 GMT  
		Size: 46.0 MB (46023713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2182e80f9ad42f6496030d84016d16b92e151e06b4e016cd308c0fac0b4a8a42`  
		Last Modified: Fri, 17 Apr 2026 00:25:22 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35aa1571b1b2f924731940bf8358cda86cf72a8b2a20d2346918dfac1af56c0`  
		Last Modified: Fri, 17 Apr 2026 00:25:22 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10-slim` - unknown; unknown

```console
$ docker pull znc@sha256:7f19e0320df791909a275ff253ec950a0710fa4b21191952d320b0dde0752a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1766071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfbb9557eeb3c1680ea4906530982212814d8167cf417703d6253882f70c61e`

```dockerfile
```

-	Layers:
	-	`sha256:007cc217b1a227cce5274f22d0f419680978b5a190c6e6cb1c350f65a1ab03ba`  
		Last Modified: Fri, 17 Apr 2026 00:25:23 GMT  
		Size: 1.8 MB (1752083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c1b84cd96d7f30ca91e49b8ebe345c764078c15e7f6272d9f0b8cb00dcaf420`  
		Last Modified: Fri, 17 Apr 2026 00:25:22 GMT  
		Size: 14.0 KB (13988 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:2d24b27e3840077c2b021b2914099aff46ee59fbceba4bd10e3c67eb1587f28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48116835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0d0190b68cfb15dacf3fd50af2a27480036cb8a93d3bf2b5d4e62291dd11b2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:39 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 17 Apr 2026 00:32:39 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 17 Apr 2026 00:32:39 GMT
ARG MAKEFLAGS=
# Fri, 17 Apr 2026 00:32:39 GMT
ENV ZNC_VERSION=1.10.1
# Fri, 17 Apr 2026 00:32:39 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Fri, 17 Apr 2026 00:32:39 GMT
COPY entrypoint.sh / # buildkit
# Fri, 17 Apr 2026 00:32:39 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Fri, 17 Apr 2026 00:32:39 GMT
VOLUME [/znc-data]
# Fri, 17 Apr 2026 00:32:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966ee517e4aa87f280941db01d122485043381c8d9af87cb4de293fb92c16ef1`  
		Last Modified: Fri, 17 Apr 2026 00:32:48 GMT  
		Size: 44.6 MB (44608529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b94e4faa7c02667627fa6948e955f05851c0207a9bb17dbc81090eeb3e5bbcd`  
		Last Modified: Fri, 17 Apr 2026 00:32:47 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bd26bb3234b7a6756fb2372a754b64d573f4b32e1fd5d705ac7d8679bfe7bd`  
		Last Modified: Fri, 17 Apr 2026 00:32:47 GMT  
		Size: 751.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10-slim` - unknown; unknown

```console
$ docker pull znc@sha256:fb76cb5d097a8c88d00c6accc72887d18a23d4fe971cb2d8005a54334159b234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c82710f8dbb8d3b78374e312af2543140e8d03cda80b04b79158fc266a85acb1`

```dockerfile
```

-	Layers:
	-	`sha256:60a02431cc967c044ca09506bdbeea031d04804bcddf1da30525fef8acbfb574`  
		Last Modified: Fri, 17 Apr 2026 00:32:47 GMT  
		Size: 13.8 KB (13845 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:f944fbd5020e43f90a0bc9e83edff2bc32fd54cc532c652c07063f3bfaa41308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49964240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2824ddc7639b3f2d37467a03903453f251d8bfb381d0d2473752115ee953833e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:27:38 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 17 Apr 2026 00:27:38 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 17 Apr 2026 00:27:38 GMT
ARG MAKEFLAGS=
# Fri, 17 Apr 2026 00:27:38 GMT
ENV ZNC_VERSION=1.10.1
# Fri, 17 Apr 2026 00:27:38 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Fri, 17 Apr 2026 00:27:38 GMT
COPY entrypoint.sh / # buildkit
# Fri, 17 Apr 2026 00:27:38 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Fri, 17 Apr 2026 00:27:38 GMT
VOLUME [/znc-data]
# Fri, 17 Apr 2026 00:27:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10c085ab11c93dc230c7b70da849b0449e854ed31522b9758b4214b47506da5`  
		Last Modified: Fri, 17 Apr 2026 00:27:49 GMT  
		Size: 45.8 MB (45821426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3755031d12e56fe753125278f020485273ff494877fa4b598747df17985261ef`  
		Last Modified: Fri, 17 Apr 2026 00:27:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c2bd649a20601af73ae1bfd32fa4bc5ea011a3a38d7ba80fcf8b868acdf488`  
		Last Modified: Fri, 17 Apr 2026 00:27:48 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10-slim` - unknown; unknown

```console
$ docker pull znc@sha256:8b6dad1a2124da6c415d4b7ceaf611d054ec966409b484a0d8f90b299b17b943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1766293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34933bc6372061aebaa8e7a9ad28eb28b5a3bd0db07bef9e8dd6006f1180f8eb`

```dockerfile
```

-	Layers:
	-	`sha256:911a96ed676bcf7574e8c46b28b88e9d371739b9f7da7edc85dddb2074d806ad`  
		Last Modified: Fri, 17 Apr 2026 00:27:48 GMT  
		Size: 1.8 MB (1752213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:634350886123612ef7dbe4f8b52c013ff7be1e10edbc21f591ac8c35fb0c315e`  
		Last Modified: Fri, 17 Apr 2026 00:27:48 GMT  
		Size: 14.1 KB (14080 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.10.2`

**does not exist** (yet?)

## `znc:1.10.2-slim`

**does not exist** (yet?)

## `znc:latest`

```console
$ docker pull znc@sha256:c731c6a9b8b63f283aecbcdbee236574c6b05995766574213422c365db429147
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `znc:latest` - linux; amd64

```console
$ docker pull znc@sha256:e37f0a533d35fe23e0a37b14f27c6a94de5e41ab7699fc6068c2bbdb242a4478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169364545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf50b4b7cb015939d2bd51213202b072973a606c379b71af0982e3a6ec0aac5d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:25:12 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 17 Apr 2026 00:25:12 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 17 Apr 2026 00:25:12 GMT
ARG MAKEFLAGS=
# Fri, 17 Apr 2026 00:25:12 GMT
ENV ZNC_VERSION=1.10.1
# Fri, 17 Apr 2026 00:25:12 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Fri, 17 Apr 2026 00:25:12 GMT
COPY entrypoint.sh / # buildkit
# Fri, 17 Apr 2026 00:25:12 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Fri, 17 Apr 2026 00:25:12 GMT
VOLUME [/znc-data]
# Fri, 17 Apr 2026 00:25:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 01:13:19 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Fri, 17 Apr 2026 01:13:19 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab87e5c08dbaa94f2abe60a96c74f3d65dcedb1f7235faf6090204fc191e4544`  
		Last Modified: Fri, 17 Apr 2026 00:25:24 GMT  
		Size: 46.0 MB (46023713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2182e80f9ad42f6496030d84016d16b92e151e06b4e016cd308c0fac0b4a8a42`  
		Last Modified: Fri, 17 Apr 2026 00:25:22 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35aa1571b1b2f924731940bf8358cda86cf72a8b2a20d2346918dfac1af56c0`  
		Last Modified: Fri, 17 Apr 2026 00:25:22 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c139231a03fbbf6fe759b85db4425833b4fd87e657002f0dea00e5fe85e5b418`  
		Last Modified: Fri, 17 Apr 2026 01:13:42 GMT  
		Size: 119.5 MB (119531388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c13837f80dbf618f1b43bac44de79e819083b359f857f0a82a662a6f13dc9b0`  
		Last Modified: Fri, 17 Apr 2026 01:13:39 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:808537df43bf21a94bb31ecca0a1872eca5920e458a5e7a2606c3a483509adae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6869975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cda17cb8b73bcdd9024e5b93d1a648d517d49cd5817dda890f545056539ec5f`

```dockerfile
```

-	Layers:
	-	`sha256:aef6e0ee47e4e01d1f2779171f6d3b1fb2e3eed807b7d9248e05dc2ca068e7d7`  
		Last Modified: Fri, 17 Apr 2026 01:13:39 GMT  
		Size: 6.9 MB (6860415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b1c335c30bc24e240ac92e9c1c372fda79c9591b407b733547bffeb2aeaa20f`  
		Last Modified: Fri, 17 Apr 2026 01:13:39 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:3aa535594ba7579fd38b8c6827f0f05953be6ead3599cb2faeb9a8ba4ec41f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148658031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42bbf9efb0eb17e16887d4c45d9d243d49b521d17fe8b1cdd5c2716e372e69a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:39 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 17 Apr 2026 00:32:39 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 17 Apr 2026 00:32:39 GMT
ARG MAKEFLAGS=
# Fri, 17 Apr 2026 00:32:39 GMT
ENV ZNC_VERSION=1.10.1
# Fri, 17 Apr 2026 00:32:39 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Fri, 17 Apr 2026 00:32:39 GMT
COPY entrypoint.sh / # buildkit
# Fri, 17 Apr 2026 00:32:39 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Fri, 17 Apr 2026 00:32:39 GMT
VOLUME [/znc-data]
# Fri, 17 Apr 2026 00:32:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 01:12:37 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Fri, 17 Apr 2026 01:12:37 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966ee517e4aa87f280941db01d122485043381c8d9af87cb4de293fb92c16ef1`  
		Last Modified: Fri, 17 Apr 2026 00:32:48 GMT  
		Size: 44.6 MB (44608529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b94e4faa7c02667627fa6948e955f05851c0207a9bb17dbc81090eeb3e5bbcd`  
		Last Modified: Fri, 17 Apr 2026 00:32:47 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bd26bb3234b7a6756fb2372a754b64d573f4b32e1fd5d705ac7d8679bfe7bd`  
		Last Modified: Fri, 17 Apr 2026 00:32:47 GMT  
		Size: 751.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb263554f52dbaa15d11a1ca4dd63d63c1a6e5c6792b0ecb827810a3dd7bb13d`  
		Last Modified: Fri, 17 Apr 2026 01:12:54 GMT  
		Size: 100.5 MB (100540865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b516220b86528d08d38772121d958b316017231f425a341d65b16088e1d095`  
		Last Modified: Fri, 17 Apr 2026 01:12:51 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:28844ae9b0d30e5246be2a9125184b386f00ca2aa02f48ace568f3381af4227f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b882c6152b6a077f3636516f7ae08303024b3e369f1382deb6545d4e965331`

```dockerfile
```

-	Layers:
	-	`sha256:c5ceb5a7c6f10bf877b76624dbaa69b7eff517393c227dfde0e0f48d6138223b`  
		Last Modified: Fri, 17 Apr 2026 01:12:51 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:27f44b5cda925b501ec43222c037adbf6fb969c6acd7c72a68343e8259babec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163127873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d847cfc8d2c616240c6e59892a03151df10c952582731bd8a0232fff5c8b07`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:27:38 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 17 Apr 2026 00:27:38 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 17 Apr 2026 00:27:38 GMT
ARG MAKEFLAGS=
# Fri, 17 Apr 2026 00:27:38 GMT
ENV ZNC_VERSION=1.10.1
# Fri, 17 Apr 2026 00:27:38 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Fri, 17 Apr 2026 00:27:38 GMT
COPY entrypoint.sh / # buildkit
# Fri, 17 Apr 2026 00:27:38 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Fri, 17 Apr 2026 00:27:38 GMT
VOLUME [/znc-data]
# Fri, 17 Apr 2026 00:27:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 01:34:36 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Fri, 17 Apr 2026 01:34:36 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10c085ab11c93dc230c7b70da849b0449e854ed31522b9758b4214b47506da5`  
		Last Modified: Fri, 17 Apr 2026 00:27:49 GMT  
		Size: 45.8 MB (45821426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3755031d12e56fe753125278f020485273ff494877fa4b598747df17985261ef`  
		Last Modified: Fri, 17 Apr 2026 00:27:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c2bd649a20601af73ae1bfd32fa4bc5ea011a3a38d7ba80fcf8b868acdf488`  
		Last Modified: Fri, 17 Apr 2026 00:27:48 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f07692eb313edf8bfb5c38af72bc0376841e3f33c6afdbb2482c7d02c56d03`  
		Last Modified: Fri, 17 Apr 2026 01:34:59 GMT  
		Size: 113.2 MB (113163302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49bdd732e07fcb6267a35c9b6a76253b5e218253a838db2ae6cb6dd610a6f26`  
		Last Modified: Fri, 17 Apr 2026 01:34:56 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:229e390099a6041c554dc3ee3aff9929826edd00d66c081ef53bebeaaa06ca34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6949491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c050a4379214458e94157f7c20e7936db2853c9d1cc6b89f0b256380d1202f67`

```dockerfile
```

-	Layers:
	-	`sha256:f054058310935024ec64ff515dcf3ab715483359f53515628e240b14df2086e5`  
		Last Modified: Fri, 17 Apr 2026 01:34:56 GMT  
		Size: 6.9 MB (6939839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf325017a9a249cbfc71c8a1c1cf6505304cef767c1d5077fb099c060d3bcf53`  
		Last Modified: Fri, 17 Apr 2026 01:34:55 GMT  
		Size: 9.7 KB (9652 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:slim`

```console
$ docker pull znc@sha256:f9e8b560438735ef045f419054e96b54fc3ef23d10a5c48a0323b1e675ae9a42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `znc:slim` - linux; amd64

```console
$ docker pull znc@sha256:e228716553b8b3030b3f258f663561fcd5efeac1038451ade040d31705b90d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49832826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8daa794f654e88fafa0dc001362b980f1f6b6b7fb19536a66c7b3a3020cadf70`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:25:12 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 17 Apr 2026 00:25:12 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 17 Apr 2026 00:25:12 GMT
ARG MAKEFLAGS=
# Fri, 17 Apr 2026 00:25:12 GMT
ENV ZNC_VERSION=1.10.1
# Fri, 17 Apr 2026 00:25:12 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Fri, 17 Apr 2026 00:25:12 GMT
COPY entrypoint.sh / # buildkit
# Fri, 17 Apr 2026 00:25:12 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Fri, 17 Apr 2026 00:25:12 GMT
VOLUME [/znc-data]
# Fri, 17 Apr 2026 00:25:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab87e5c08dbaa94f2abe60a96c74f3d65dcedb1f7235faf6090204fc191e4544`  
		Last Modified: Fri, 17 Apr 2026 00:25:24 GMT  
		Size: 46.0 MB (46023713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2182e80f9ad42f6496030d84016d16b92e151e06b4e016cd308c0fac0b4a8a42`  
		Last Modified: Fri, 17 Apr 2026 00:25:22 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35aa1571b1b2f924731940bf8358cda86cf72a8b2a20d2346918dfac1af56c0`  
		Last Modified: Fri, 17 Apr 2026 00:25:22 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:7f19e0320df791909a275ff253ec950a0710fa4b21191952d320b0dde0752a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1766071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfbb9557eeb3c1680ea4906530982212814d8167cf417703d6253882f70c61e`

```dockerfile
```

-	Layers:
	-	`sha256:007cc217b1a227cce5274f22d0f419680978b5a190c6e6cb1c350f65a1ab03ba`  
		Last Modified: Fri, 17 Apr 2026 00:25:23 GMT  
		Size: 1.8 MB (1752083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c1b84cd96d7f30ca91e49b8ebe345c764078c15e7f6272d9f0b8cb00dcaf420`  
		Last Modified: Fri, 17 Apr 2026 00:25:22 GMT  
		Size: 14.0 KB (13988 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:2d24b27e3840077c2b021b2914099aff46ee59fbceba4bd10e3c67eb1587f28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48116835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0d0190b68cfb15dacf3fd50af2a27480036cb8a93d3bf2b5d4e62291dd11b2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:39 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 17 Apr 2026 00:32:39 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 17 Apr 2026 00:32:39 GMT
ARG MAKEFLAGS=
# Fri, 17 Apr 2026 00:32:39 GMT
ENV ZNC_VERSION=1.10.1
# Fri, 17 Apr 2026 00:32:39 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Fri, 17 Apr 2026 00:32:39 GMT
COPY entrypoint.sh / # buildkit
# Fri, 17 Apr 2026 00:32:39 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Fri, 17 Apr 2026 00:32:39 GMT
VOLUME [/znc-data]
# Fri, 17 Apr 2026 00:32:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966ee517e4aa87f280941db01d122485043381c8d9af87cb4de293fb92c16ef1`  
		Last Modified: Fri, 17 Apr 2026 00:32:48 GMT  
		Size: 44.6 MB (44608529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b94e4faa7c02667627fa6948e955f05851c0207a9bb17dbc81090eeb3e5bbcd`  
		Last Modified: Fri, 17 Apr 2026 00:32:47 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bd26bb3234b7a6756fb2372a754b64d573f4b32e1fd5d705ac7d8679bfe7bd`  
		Last Modified: Fri, 17 Apr 2026 00:32:47 GMT  
		Size: 751.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:fb76cb5d097a8c88d00c6accc72887d18a23d4fe971cb2d8005a54334159b234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c82710f8dbb8d3b78374e312af2543140e8d03cda80b04b79158fc266a85acb1`

```dockerfile
```

-	Layers:
	-	`sha256:60a02431cc967c044ca09506bdbeea031d04804bcddf1da30525fef8acbfb574`  
		Last Modified: Fri, 17 Apr 2026 00:32:47 GMT  
		Size: 13.8 KB (13845 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:f944fbd5020e43f90a0bc9e83edff2bc32fd54cc532c652c07063f3bfaa41308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49964240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2824ddc7639b3f2d37467a03903453f251d8bfb381d0d2473752115ee953833e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:27:38 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 17 Apr 2026 00:27:38 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 17 Apr 2026 00:27:38 GMT
ARG MAKEFLAGS=
# Fri, 17 Apr 2026 00:27:38 GMT
ENV ZNC_VERSION=1.10.1
# Fri, 17 Apr 2026 00:27:38 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Fri, 17 Apr 2026 00:27:38 GMT
COPY entrypoint.sh / # buildkit
# Fri, 17 Apr 2026 00:27:38 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Fri, 17 Apr 2026 00:27:38 GMT
VOLUME [/znc-data]
# Fri, 17 Apr 2026 00:27:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10c085ab11c93dc230c7b70da849b0449e854ed31522b9758b4214b47506da5`  
		Last Modified: Fri, 17 Apr 2026 00:27:49 GMT  
		Size: 45.8 MB (45821426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3755031d12e56fe753125278f020485273ff494877fa4b598747df17985261ef`  
		Last Modified: Fri, 17 Apr 2026 00:27:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c2bd649a20601af73ae1bfd32fa4bc5ea011a3a38d7ba80fcf8b868acdf488`  
		Last Modified: Fri, 17 Apr 2026 00:27:48 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:8b6dad1a2124da6c415d4b7ceaf611d054ec966409b484a0d8f90b299b17b943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1766293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34933bc6372061aebaa8e7a9ad28eb28b5a3bd0db07bef9e8dd6006f1180f8eb`

```dockerfile
```

-	Layers:
	-	`sha256:911a96ed676bcf7574e8c46b28b88e9d371739b9f7da7edc85dddb2074d806ad`  
		Last Modified: Fri, 17 Apr 2026 00:27:48 GMT  
		Size: 1.8 MB (1752213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:634350886123612ef7dbe4f8b52c013ff7be1e10edbc21f591ac8c35fb0c315e`  
		Last Modified: Fri, 17 Apr 2026 00:27:48 GMT  
		Size: 14.1 KB (14080 bytes)  
		MIME: application/vnd.in-toto+json
