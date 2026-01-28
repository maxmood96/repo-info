## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:fb7009c46088b1c5a1c29c9482726656968ccb3948f7c20c92d7ec26f87e1f63
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
$ docker pull rakudo-star@sha256:f9425c53293b1c04b177f8d176ec190a099114d727f9a34a61c177eaa1569ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50282430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ea41bbff6270593d2f71a0bc560f380d42b047551e8a0a815488262bb9cac6`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Sun, 28 Dec 2025 05:53:14 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Sun, 28 Dec 2025 06:12:52 GMT
ARG rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:12:52 GMT
ENV rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:12:52 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Sun, 28 Dec 2025 06:12:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Sun, 28 Dec 2025 06:12:52 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bd0463e9cce2cf2e69d321d68c112c55ed5938ad6e0f7eadc43a0422d15dd9`  
		Last Modified: Sun, 28 Dec 2025 06:13:04 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3a9b3b72876e783969531d568fd8ba185daac1d1319d9dde5cd4a874f5164a`  
		Last Modified: Sun, 28 Dec 2025 06:13:06 GMT  
		Size: 46.1 MB (46085744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b5f6805a4e7f72b8f1b5ed0a029c869f93444b938cb54a6bb2d6747bfaf61666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 KB (198167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2097dbf45017e07c2140d46770b097116e7b1f327c83a1b833d6563291c428e`

```dockerfile
```

-	Layers:
	-	`sha256:9419e7a131a2ff381aeb74d53e3b0c551978012aa19c905ae79e781a4931a1e5`  
		Last Modified: Sun, 28 Dec 2025 06:13:04 GMT  
		Size: 186.4 KB (186355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c07e7c349f0d6d1151c4618b66c26b64dd91dc52cfb0cb17d816c0c09f4ce49d`  
		Last Modified: Sun, 28 Dec 2025 06:13:04 GMT  
		Size: 11.8 KB (11812 bytes)  
		MIME: application/vnd.in-toto+json
