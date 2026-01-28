## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:3478c900192d953c4daea962414fa1561b628519c852a85d02f9aa99ccbcd013
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:a5e46845f85f9d97a37529734562f9535dfce8ecbe217d73761ad74f70a5ef61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51507607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3310d06f6d5916955e54447d1c167423d910eeac7110d8502be77238768a6f`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:41:36 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Wed, 28 Jan 2026 03:56:35 GMT
ARG rakudo_version=2025.12-01
# Wed, 28 Jan 2026 03:56:35 GMT
ENV rakudo_version=2025.12-01
# Wed, 28 Jan 2026 03:56:35 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:56:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 28 Jan 2026 03:56:35 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7173023272275c47a98144e31caaf00c20e2c4c84752a2660fe4318ad5c3a5fc`  
		Last Modified: Wed, 28 Jan 2026 03:56:45 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b692d7ca77d32d4a320ec7630ebc5545eb24f322272eb9ff9bbd5262a6f566`  
		Last Modified: Wed, 28 Jan 2026 03:56:47 GMT  
		Size: 47.6 MB (47644840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:22fe7def47c09265029c912a0abf231e4bba51e8cf1260d75ff3e9c497955f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 KB (198691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463e8ce36fa34415336368ce0fbed0050a953984793827c7badb455a536445c3`

```dockerfile
```

-	Layers:
	-	`sha256:b16d66d90adc31c2357ca7c0f2c79a1d4b9754b4eb6af2ca98c78dc669e9013e`  
		Last Modified: Wed, 28 Jan 2026 03:56:45 GMT  
		Size: 187.0 KB (186973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc04d290013292d2ad10104d9608ac4b411eb75152ac3134a7a713b82a05d718`  
		Last Modified: Wed, 28 Jan 2026 03:56:45 GMT  
		Size: 11.7 KB (11718 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:7c72b48c05187a86e22f6593f062b1ab0f596bd0e1b379559a7cc4290bad2e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51560713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d589ceae623cb089ddc0e163c0424c9a49248598beed2f815937368350c7b376`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:47:52 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Wed, 28 Jan 2026 04:08:24 GMT
ARG rakudo_version=2025.12-01
# Wed, 28 Jan 2026 04:08:24 GMT
ENV rakudo_version=2025.12-01
# Wed, 28 Jan 2026 04:08:24 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 04:08:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 28 Jan 2026 04:08:24 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6fd5b94d560345f66076601fbe83e32491e54fb01a278d327170d584b9b17f`  
		Last Modified: Wed, 28 Jan 2026 04:08:36 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f1abf0f5ba7aaed079c297ff5a4bdb26c5a0e90e549d3c935b954bd458ff0b`  
		Last Modified: Wed, 28 Jan 2026 04:08:37 GMT  
		Size: 47.4 MB (47362675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:83b8b3744e9890bb6e9272fd63a976b97891edbc1dd33e67acc9a10e3c829b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 KB (198167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8c6fa5d8107ef94ed3f70ef553bbdb4547d9d73b9d14295b882a661fe415e1`

```dockerfile
```

-	Layers:
	-	`sha256:1e220de6430b407a29fa688406809986d2db209a99616e1b2625f96caa431fd1`  
		Last Modified: Wed, 28 Jan 2026 04:08:36 GMT  
		Size: 186.4 KB (186355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b087ee679f80357ff642d487acb43dd0faf002535aac6254eca50a39d965c0f4`  
		Last Modified: Wed, 28 Jan 2026 04:08:36 GMT  
		Size: 11.8 KB (11812 bytes)  
		MIME: application/vnd.in-toto+json
