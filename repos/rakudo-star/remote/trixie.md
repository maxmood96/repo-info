## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:d61f9353a8091955fbeb493d728f48a00c02fbe6322058e5438731ec7a4cd61a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:23101a16105f652d19844b48b6c43174ab0be3d6e259e0b5ec48de4e80a9caae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183669958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6212dab6d87fb18387d387f1cc742eb0dba25c59745fc3f050a2d012d699fc9`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:43:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:26:38 GMT
MAINTAINER AntonOks
# Tue, 07 Apr 2026 03:26:38 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 07 Apr 2026 03:26:38 GMT
ARG rakudo_version=2026.02-01
# Tue, 07 Apr 2026 03:26:38 GMT
ENV rakudo_version=2026.02-01
# Tue, 07 Apr 2026 03:41:31 GMT
# ARGS: rakudo_version=2026.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 03:41:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 07 Apr 2026 03:41:31 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33970743aee750df25f6c661132b7401c8fefe930e5f4803f4c8b6f567a6b55`  
		Last Modified: Tue, 07 Apr 2026 01:47:22 GMT  
		Size: 25.6 MB (25621678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5397da1d1537c4d725f3090c5688a582e14eeaf7743d75d9b38bad1649554987`  
		Last Modified: Tue, 07 Apr 2026 02:43:39 GMT  
		Size: 67.8 MB (67780708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57257cc462fa158485ef8936cd001a9943d468b402767efa82318d2028e6c91`  
		Last Modified: Tue, 07 Apr 2026 03:41:54 GMT  
		Size: 3.2 KB (3244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2492036ef8b49a1d58934bcbdc738b245ebd52a46460367bfef2f1f8100e5188`  
		Last Modified: Tue, 07 Apr 2026 03:41:56 GMT  
		Size: 41.0 MB (40966495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:591e75b5f0b6537d2180e7d1a582affa1ed347a659fe586e37b8a7a8120c42f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab85bfa57736b9c3245d1338d86f6bb4778d5e0de329e6a94ae01fb207f45ab`

```dockerfile
```

-	Layers:
	-	`sha256:20706ef706724d170da8fc89fb063e896e8f0d302d627ee96484a3a075aa4efe`  
		Last Modified: Tue, 07 Apr 2026 03:41:55 GMT  
		Size: 7.8 MB (7770304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a012bcbfd00716b658df4d3f2f0efa995c4681589b7955519694c5ed5b02ce06`  
		Last Modified: Tue, 07 Apr 2026 03:41:55 GMT  
		Size: 12.7 KB (12685 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:8c08e943da1e75067e48d29eb62016d4767a67c36f79c895b2ec0d8fd3a48c89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181299328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c354eeb17bec78712e460b0772e2e20a36dbe5047479e15d149ec24d9599da`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:50:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:53:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:38:41 GMT
MAINTAINER AntonOks
# Tue, 07 Apr 2026 03:38:41 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 07 Apr 2026 03:38:41 GMT
ARG rakudo_version=2026.02-01
# Tue, 07 Apr 2026 03:38:41 GMT
ENV rakudo_version=2026.02-01
# Tue, 07 Apr 2026 03:59:16 GMT
# ARGS: rakudo_version=2026.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 03:59:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 07 Apr 2026 03:59:16 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ee5883c1f173b0485b465221ddea5443b64c95935146f0bb3655baee3647d`  
		Last Modified: Tue, 07 Apr 2026 01:50:26 GMT  
		Size: 25.0 MB (25023654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6084ed286765ee022e8f8d9df76b9a2bd97a3224c379e905079f3bb11e1e48ca`  
		Last Modified: Tue, 07 Apr 2026 02:54:15 GMT  
		Size: 67.6 MB (67591915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46650357223e61e94f7bb3c68d8e9cf2287be7baa477bb9440b1f7189998d40`  
		Last Modified: Tue, 07 Apr 2026 03:59:32 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb9a4a6428e8db5658a620e9299ee1221deb67b6dde6db6e8e0c3f993ab19f2`  
		Last Modified: Tue, 07 Apr 2026 03:59:33 GMT  
		Size: 39.0 MB (39015262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:745f8649a74da9b0ce4dae5db94a181fa1db09ff8a8ec7ef1a568c7ab2f99e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7027998df555dcf27f3e6c4529e901263ace61d3b9dc1e221844e22e12b25ae`

```dockerfile
```

-	Layers:
	-	`sha256:41479ffb9744a5ff5c316b85d3746447f03b4a3cd485dc89e35d35def4793b87`  
		Last Modified: Tue, 07 Apr 2026 03:59:32 GMT  
		Size: 7.8 MB (7777967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b88e25a2da8d045158cbbfd4ad652329cba4140ef9f5133c07780565cb37df68`  
		Last Modified: Tue, 07 Apr 2026 03:59:32 GMT  
		Size: 12.8 KB (12780 bytes)  
		MIME: application/vnd.in-toto+json
