## `znc:latest`

```console
$ docker pull znc@sha256:f2bcfee3dddf48341634dbc255ffab8fc0c7d2482a42b4aaebbfa075773a84a1
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
$ docker pull znc@sha256:9899a55976b35ae537ad182731519763bb03ca33d2a1c931899bccb374dac0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.3 MB (169326042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485a3780538cec9407ab2f3c5640e3480d9fc2aa1f4d938372fba3e0b9975e41`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 01 Jul 2025 21:26:43 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 01 Jul 2025 21:26:43 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Tue, 01 Jul 2025 21:26:43 GMT
ARG MAKEFLAGS=
# Tue, 01 Jul 2025 21:26:43 GMT
ENV ZNC_VERSION=1.10.1
# Tue, 01 Jul 2025 21:26:43 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
VOLUME [/znc-data]
# Tue, 01 Jul 2025 21:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63e3f0e4029030bd9f830942586bb0ca558e4468d53f436fc82c690a37142c9`  
		Last Modified: Tue, 15 Jul 2025 20:14:50 GMT  
		Size: 46.0 MB (45994220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3197994a98ed0bb04b6312326155f7147661fb91d563b72e90d3c3396ee149c`  
		Last Modified: Tue, 15 Jul 2025 20:14:46 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6104331ab47fae7a31feb99afced414094deb99e28c28fce2ae788ad0f9b86`  
		Last Modified: Tue, 15 Jul 2025 20:14:46 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46ffb394daa65aeb9537b6665a84078588c497c562a18b23ebc06b9c42c005e`  
		Last Modified: Tue, 15 Jul 2025 20:15:49 GMT  
		Size: 119.5 MB (119530882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098b1ab9fc7d89af010f78509e8c796807605ce7c0edeae3fb9b476bd2f7c4a2`  
		Last Modified: Tue, 15 Jul 2025 20:15:39 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:0a738603bc5d043e519d52abbabbf7cd0cf35b0a87ffcccc76e0c11f20ae083d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6868092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07fdd66fe7524fc67de744540369e4697123496e4a5bb0ae52cddbd726e6523a`

```dockerfile
```

-	Layers:
	-	`sha256:959d52bcc0ce3ab26a99619893327e35ca1b5cb49bba40e70895aaa95ed434e4`  
		Last Modified: Tue, 15 Jul 2025 21:35:19 GMT  
		Size: 6.9 MB (6858489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18922ba1ae66dcecd24dd80ce66652b5daab6d08f4d8ad17a430380ec7b236b6`  
		Last Modified: Tue, 15 Jul 2025 21:35:19 GMT  
		Size: 9.6 KB (9603 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:6930d5743b940f694136c32e32a0afd536e737f103400c851a6a964a9dd4b945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148638578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791ccadfc922ed39f85ed58f02f13ff635e369231410036260bfc92d91222214`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 01 Jul 2025 21:26:43 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 01 Jul 2025 21:26:43 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Tue, 01 Jul 2025 21:26:43 GMT
ARG MAKEFLAGS=
# Tue, 01 Jul 2025 21:26:43 GMT
ENV ZNC_VERSION=1.10.1
# Tue, 01 Jul 2025 21:26:43 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
VOLUME [/znc-data]
# Tue, 01 Jul 2025 21:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92a0ff41cb89bbb4e481182f94fc5637e4f7b9aaaf1ae7f5fe19a060178ff22`  
		Last Modified: Tue, 15 Jul 2025 22:55:18 GMT  
		Size: 44.6 MB (44597013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9dda5dfedcca72002ee45d157914364edcab2a4417e995e0a3aa38258db522`  
		Last Modified: Tue, 15 Jul 2025 22:55:14 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e015ad4dc1819407fb848af786072bb12c173e15854e7438faeba9567e3820c`  
		Last Modified: Tue, 15 Jul 2025 22:55:14 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc7bb2873927bb272838498fe433dcb593db4177055751b3a214bd68309d5b3`  
		Last Modified: Wed, 16 Jul 2025 06:35:47 GMT  
		Size: 100.5 MB (100539402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d564c4a0d46195e7297a641f325c27ada1abf9ff6ce088b2fea178c8a8a9e2c`  
		Last Modified: Wed, 16 Jul 2025 03:51:57 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:234987f48737358757c9c75f73e36b70d82e950c9db177a3fa558badae0536ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0318b06b7da43e8ebe079bd245b3ab8c456b2b7ae60a29abc6162d2b79b448`

```dockerfile
```

-	Layers:
	-	`sha256:447129b6c885939ea5f594be106e2fe1748fae479018d11bbe4f76b1ce6cd735`  
		Last Modified: Wed, 16 Jul 2025 06:35:21 GMT  
		Size: 9.5 KB (9456 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:70ec2f1d60b48ccb74255dfd01d325a264a9f35a5b8ac286f519ee0db714230b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163099542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fd10f3d09629bea675c6e332f2a129e6e8e6282ecfd22c05c81aa99351ad92`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 01 Jul 2025 21:26:43 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 01 Jul 2025 21:26:43 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Tue, 01 Jul 2025 21:26:43 GMT
ARG MAKEFLAGS=
# Tue, 01 Jul 2025 21:26:43 GMT
ENV ZNC_VERSION=1.10.1
# Tue, 01 Jul 2025 21:26:43 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
VOLUME [/znc-data]
# Tue, 01 Jul 2025 21:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393deeebc02c99eac9edf5ba13a48d19603413143e6b1679d51a19b5fc969b10`  
		Last Modified: Tue, 15 Jul 2025 23:18:03 GMT  
		Size: 45.8 MB (45806323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88496cd377a57b9b67751eeb20666ffc7868059eba9dce25a682210c0da9d45`  
		Last Modified: Tue, 15 Jul 2025 23:17:59 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b030d184dbe460634a56760f0f5f1c2c554b72677c6faf38c06ef0dd5686c5`  
		Last Modified: Tue, 15 Jul 2025 23:18:00 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be866556b13f6ff578da0ebda93e41c707b01f238ab6da814959d5f56f50ede`  
		Last Modified: Wed, 16 Jul 2025 06:17:29 GMT  
		Size: 113.2 MB (113161218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813ccf9ba913312b426d1f23112128202c8969cd21b8016776ea9843ad1ac4af`  
		Last Modified: Wed, 16 Jul 2025 06:17:22 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:26497482c352eb481a2b6437d756187ee389a35d139bdfa6a053692941c28037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6947608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27a0bb7dfd7f82c2584cee59157ad5eedf5fd4c44629145a760801e4f1be2a1`

```dockerfile
```

-	Layers:
	-	`sha256:04f74347e0e643dfb211c68462ef5e03ad4c72c17929a955cc35a03b9cfb0125`  
		Last Modified: Wed, 16 Jul 2025 09:35:23 GMT  
		Size: 6.9 MB (6937913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60b385ad5d7d805c3ccbebbd0d023aeaea0e247badbf7ccd4db184d799b535a4`  
		Last Modified: Wed, 16 Jul 2025 09:35:23 GMT  
		Size: 9.7 KB (9695 bytes)  
		MIME: application/vnd.in-toto+json
