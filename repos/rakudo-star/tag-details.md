<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2025.10-alpine`](#rakudo-star202510-alpine)
-	[`rakudo-star:2025.10-bookworm`](#rakudo-star202510-bookworm)
-	[`rakudo-star:2025.10-trixie`](#rakudo-star202510-trixie)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:bookworm`](#rakudo-starbookworm)
-	[`rakudo-star:latest`](#rakudo-starlatest)
-	[`rakudo-star:trixie`](#rakudo-startrixie)

## `rakudo-star:2025.10-alpine`

```console
$ docker pull rakudo-star@sha256:60f630c763fe053a4fbb90a877964f17d8021043b8b31e36abe4e0ba9203e862
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.10-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:f608fe8aae34343c8a52fbc9ba0e3ab0aec156b3547db71d69dc2acee6ae4da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52898044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c394f4de6f740f7e91e05c6ef8a0e2c4949864c2d6b047ade93082e31715395`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 23 Oct 2025 03:12:19 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ARG rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
ENV rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 23 Oct 2025 03:12:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94ae187876b8dfd9796c6a5e83b3fd4df758dab43d6e470d4b3e2b0e8e699ef`  
		Last Modified: Thu, 23 Oct 2025 23:46:46 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479dd71f79409ea180e1088f9824b93c21d4c109f800a05baef9ffaf1b948035`  
		Last Modified: Thu, 23 Oct 2025 23:46:49 GMT  
		Size: 49.1 MB (49094643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:771edf5e119637bd6e29891909c6e22a41bf60b6cc4c956f170592d07fd7e1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 KB (197780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6e06b7417bc34fb3651e11bc883f341b3ac83727b269273649d67b1ce09942`

```dockerfile
```

-	Layers:
	-	`sha256:da1fe5c8cdce4abdd95d12d29185b6bd74c1cc4ee40fff1c14afe654a98db351`  
		Last Modified: Fri, 24 Oct 2025 01:33:20 GMT  
		Size: 186.0 KB (186020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:702e025402ada9b8eeba1897b6a64f0bdfa61551086096a3d5aea7ef06c12e7d`  
		Last Modified: Fri, 24 Oct 2025 01:33:21 GMT  
		Size: 11.8 KB (11760 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.10-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:a550cebb99664a9633d897c98c89899f51d8f9435ef5b614eb545fba93995bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52925677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1445c061ae404b4788a5178c6db3e7339ec2789e163e26d90c7fb4940e352b6`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 23 Oct 2025 03:12:19 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ARG rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
ENV rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 23 Oct 2025 03:12:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f354594890fce8d86fccc0efd95519674214696b4d7be96e258f4608cd8935`  
		Last Modified: Thu, 23 Oct 2025 22:30:49 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea0230fc82455718c52d3c89e277ef1cf39d85f33ab447bccb2d125194cb203`  
		Last Modified: Thu, 23 Oct 2025 22:30:53 GMT  
		Size: 48.8 MB (48786660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:5321a6a3a5400198193ec57dd6da13c6ab29c95dcd6acaec789d0bbbf8573dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 KB (197907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0a76bc0ad9780a1dfd9b03748bb412e60acbd0726a1e8445c9e17dd01e5839`

```dockerfile
```

-	Layers:
	-	`sha256:a7d61e7b14327a9149659f2cc4dd38b50e46d7c5b2f272ec0a135c79719380a4`  
		Last Modified: Fri, 24 Oct 2025 01:33:24 GMT  
		Size: 186.1 KB (186052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:119a5fd04ebf8a2ee4f6476233145b8923f667a97a8c22c43bcf7bac0df4c3ca`  
		Last Modified: Fri, 24 Oct 2025 01:33:25 GMT  
		Size: 11.9 KB (11855 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2025.10-bookworm`

```console
$ docker pull rakudo-star@sha256:09fa24dd191fd7d10f1ab5e55ee24e70186dda655d331071724547150520b26d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.10-bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:3c62798d9ade7bb0752bf0ebe859448dd01cea55cb5282c3365f6daf606c9efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179609194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70bb6676cb8c9a0ed29aff6f7d3f916b8b4ca7be8b1f8e9a88ade89d561864a`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 07:54:11 GMT
MAINTAINER Rob Hoelz
# Tue, 04 Nov 2025 07:54:11 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 04 Nov 2025 07:54:11 GMT
ARG rakudo_version=2025.10-01
# Tue, 04 Nov 2025 07:54:11 GMT
ENV rakudo_version=2025.10-01
# Tue, 04 Nov 2025 08:07:41 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 08:07:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 04 Nov 2025 08:07:41 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb445e472b1bad54f5a28edd51b11aec79eca8513394866a261891be9da6a343`  
		Last Modified: Tue, 04 Nov 2025 00:28:00 GMT  
		Size: 24.0 MB (24029301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2123190679e81d983648da92f1bb9ddc74383512edb00ad64f93d24d00d8807a`  
		Last Modified: Tue, 04 Nov 2025 04:14:49 GMT  
		Size: 64.4 MB (64396145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633ac49056b7e7c2f64edced1ade8a636680f9bf6791553ff98e4d880d3f4e38`  
		Last Modified: Tue, 04 Nov 2025 08:54:06 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb7d7339212c95d87768b3f020e3e2a4cdc95a79cf73e40a0e279f480958d45`  
		Last Modified: Tue, 04 Nov 2025 08:54:20 GMT  
		Size: 42.7 MB (42699451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:42f57bd9717fe38a745397f956c5e7e88bd6674637065b8105b125bdec0450ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b297f186483aa478e4a201fc65eef874fafb2b11d8e7902382c42624bc564eac`

```dockerfile
```

-	Layers:
	-	`sha256:cb95eaf12a4e70fa6293c6e6cc66b3c76db2bac5e69d31a8f6e3b04f137596a3`  
		Last Modified: Tue, 04 Nov 2025 11:33:21 GMT  
		Size: 8.0 MB (7967804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96286a82ebaa1e4ba9580f5ad9a8442e5da01e87c7284c86d10077489a4cfdce`  
		Last Modified: Tue, 04 Nov 2025 11:33:21 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:2a61b910303225f3064bc18c7a17a27dfe04e5f9c17aacbf1e6e3d6f0470481d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177094097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac904f2c5def4a31a6f61eb5e4e0b3d90add82b1552e08ff43d40ac78f7aada`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:29:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:33:38 GMT
MAINTAINER Rob Hoelz
# Tue, 04 Nov 2025 02:33:38 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 04 Nov 2025 02:33:38 GMT
ARG rakudo_version=2025.10-01
# Tue, 04 Nov 2025 02:33:38 GMT
ENV rakudo_version=2025.10-01
# Tue, 04 Nov 2025 02:52:06 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 02:52:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 04 Nov 2025 02:52:06 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463896571d3ff5317461a64229e9e4cb27d6d877114079419cf8b4fc96b0c02`  
		Last Modified: Tue, 04 Nov 2025 00:30:33 GMT  
		Size: 23.6 MB (23598514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020f0f7f102dcd1ca7603a86d7398adbe5369a820cc6f32954c0b3b5e2ac7403`  
		Last Modified: Tue, 04 Nov 2025 01:30:05 GMT  
		Size: 64.4 MB (64371335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f54836e448885f2f4db146794f3b923a57237811bcaa8e804da471d9b0f5ba`  
		Last Modified: Tue, 04 Nov 2025 02:52:37 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaf1f2ddf6a9cfd9dbf571c7063995b649c2f7c6d8e94e9aefef41dbc665012`  
		Last Modified: Tue, 04 Nov 2025 02:52:43 GMT  
		Size: 40.8 MB (40761533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:098090b1ddaec33ab798033b77aa66bcc14dd47bbfdd4aa34d59a8c1ac9c1a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a1df382b01c308a96b9a7d24875fd6763acaf013e1c59c8dee752bdea6257a`

```dockerfile
```

-	Layers:
	-	`sha256:b167a316173c64af749917f0de4c9835e291de4a4c9a0fb5569a089b02862467`  
		Last Modified: Tue, 04 Nov 2025 11:33:28 GMT  
		Size: 8.0 MB (7974197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08742e7b975b9c0e7f7b679d6ecec4245cd71f8679d214afb14d172fc83c48e`  
		Last Modified: Tue, 04 Nov 2025 11:33:28 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2025.10-trixie`

```console
$ docker pull rakudo-star@sha256:0ca0c4402045a0fe331671e0f62bd6861e8cdc5c920dae47f062053c9932789c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.10-trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:cf86957b35679695d7a352ab4d89ec498d93b3d136c74369ed2bbc20e6a740a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184825431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae044e46e5d07efb52cdcfa92a73f9852ee3b9a8a30e5711e63df247649ade5d`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 07:42:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 11:17:00 GMT
MAINTAINER AntonOks
# Tue, 04 Nov 2025 11:17:00 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 04 Nov 2025 11:17:00 GMT
ARG rakudo_version=2025.10-01
# Tue, 04 Nov 2025 11:17:00 GMT
ENV rakudo_version=2025.10-01
# Tue, 04 Nov 2025 11:33:45 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 11:33:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 04 Nov 2025 11:33:45 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3143549f2b8b3ad8d79efdc47824641c6771796b3770f3c637a38aabd2b3462`  
		Last Modified: Tue, 04 Nov 2025 04:14:53 GMT  
		Size: 25.6 MB (25615393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e8e93b0d018b135d833207c6feaba205653ac52e0a80d214477ec0de239dee`  
		Last Modified: Tue, 04 Nov 2025 07:43:02 GMT  
		Size: 67.8 MB (67776858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78db28b0b23217f4f7e9b0dd25ad6daf33ac267840f3d806cf1a1989a00b7ea2`  
		Last Modified: Tue, 04 Nov 2025 11:34:07 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c44c7e54d667d73c03f35c013712ecb39086403f65fb817f50da55a970e7f36`  
		Last Modified: Tue, 04 Nov 2025 11:34:13 GMT  
		Size: 42.1 MB (42144313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:90176f2764cd6354380e7a9d7b2c8055083e8a00b516d8ff17ff9d8422116cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ef6909df47dac6d0570add6a8eb0629222d01bf4334888d0e214d53ed8e203`

```dockerfile
```

-	Layers:
	-	`sha256:35452f6bfc9f81583f224ebdde4be6622bfc14bbf0abddda9618ba709e8fb3c3`  
		Last Modified: Tue, 04 Nov 2025 14:33:21 GMT  
		Size: 7.8 MB (7769451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:652e71426534d396a8b2b896c041a36126b96d312cd74d2df18e392dfb44eb6e`  
		Last Modified: Tue, 04 Nov 2025 14:33:21 GMT  
		Size: 13.0 KB (12992 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.10-trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:10cf88e7568d31fe8a044d887e5a6c8b3a9284f339fd5d730437b7de6a2868d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (183036871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2b10b6968f21ef4c853528185f2f37b6d3e802a0cf7b02e81da8f514bca00a`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:20:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:30:57 GMT
MAINTAINER AntonOks
# Tue, 04 Nov 2025 03:30:57 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 04 Nov 2025 03:30:57 GMT
ARG rakudo_version=2025.10-01
# Tue, 04 Nov 2025 03:30:57 GMT
ENV rakudo_version=2025.10-01
# Tue, 04 Nov 2025 03:49:26 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 03:49:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 04 Nov 2025 03:49:26 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f766ef2ec48737a0f300405019c312acd667d14467b50c402750d1454e3591`  
		Last Modified: Tue, 04 Nov 2025 01:30:11 GMT  
		Size: 25.0 MB (25017577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186d0d0b2411f880d1a385216013fead1acb2dee0584aac75da87dfdeb1202db`  
		Last Modified: Tue, 04 Nov 2025 02:21:20 GMT  
		Size: 67.6 MB (67583874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05b9da4e0e176636bb48a7c9235bd155818dff94ba349815aa97e9e224c7dd3`  
		Last Modified: Tue, 04 Nov 2025 03:49:47 GMT  
		Size: 3.2 KB (3243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535e1825c308d54722e04831f1c621c8c95733439975df1b3a22b8bdef1160f3`  
		Last Modified: Tue, 04 Nov 2025 03:49:49 GMT  
		Size: 40.8 MB (40781747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3bedf9cd88476cc2ed75fc4e5c0643b52d75737885eac3dd81b202edeb1d9b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27fcb103193e5349298658c95ef0e1c9be7acba78ef76ee584ea711c3c216211`

```dockerfile
```

-	Layers:
	-	`sha256:0fd1dcb1baa2b9f9f3685f106e113c71357f3e7bb323b86214c3053280af1317`  
		Last Modified: Tue, 04 Nov 2025 11:33:32 GMT  
		Size: 7.8 MB (7777126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2c467e605ba7ccbe64606b2c732f6567a51eaf1828c91d300b2606bd8cf08be`  
		Last Modified: Tue, 04 Nov 2025 11:33:33 GMT  
		Size: 13.1 KB (13099 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:60f630c763fe053a4fbb90a877964f17d8021043b8b31e36abe4e0ba9203e862
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:f608fe8aae34343c8a52fbc9ba0e3ab0aec156b3547db71d69dc2acee6ae4da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52898044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c394f4de6f740f7e91e05c6ef8a0e2c4949864c2d6b047ade93082e31715395`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 23 Oct 2025 03:12:19 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ARG rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
ENV rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 23 Oct 2025 03:12:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94ae187876b8dfd9796c6a5e83b3fd4df758dab43d6e470d4b3e2b0e8e699ef`  
		Last Modified: Thu, 23 Oct 2025 23:46:46 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479dd71f79409ea180e1088f9824b93c21d4c109f800a05baef9ffaf1b948035`  
		Last Modified: Thu, 23 Oct 2025 23:46:49 GMT  
		Size: 49.1 MB (49094643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:771edf5e119637bd6e29891909c6e22a41bf60b6cc4c956f170592d07fd7e1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 KB (197780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6e06b7417bc34fb3651e11bc883f341b3ac83727b269273649d67b1ce09942`

```dockerfile
```

-	Layers:
	-	`sha256:da1fe5c8cdce4abdd95d12d29185b6bd74c1cc4ee40fff1c14afe654a98db351`  
		Last Modified: Fri, 24 Oct 2025 01:33:20 GMT  
		Size: 186.0 KB (186020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:702e025402ada9b8eeba1897b6a64f0bdfa61551086096a3d5aea7ef06c12e7d`  
		Last Modified: Fri, 24 Oct 2025 01:33:21 GMT  
		Size: 11.8 KB (11760 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:a550cebb99664a9633d897c98c89899f51d8f9435ef5b614eb545fba93995bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52925677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1445c061ae404b4788a5178c6db3e7339ec2789e163e26d90c7fb4940e352b6`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 23 Oct 2025 03:12:19 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ARG rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
ENV rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 23 Oct 2025 03:12:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f354594890fce8d86fccc0efd95519674214696b4d7be96e258f4608cd8935`  
		Last Modified: Thu, 23 Oct 2025 22:30:49 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea0230fc82455718c52d3c89e277ef1cf39d85f33ab447bccb2d125194cb203`  
		Last Modified: Thu, 23 Oct 2025 22:30:53 GMT  
		Size: 48.8 MB (48786660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:5321a6a3a5400198193ec57dd6da13c6ab29c95dcd6acaec789d0bbbf8573dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 KB (197907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0a76bc0ad9780a1dfd9b03748bb412e60acbd0726a1e8445c9e17dd01e5839`

```dockerfile
```

-	Layers:
	-	`sha256:a7d61e7b14327a9149659f2cc4dd38b50e46d7c5b2f272ec0a135c79719380a4`  
		Last Modified: Fri, 24 Oct 2025 01:33:24 GMT  
		Size: 186.1 KB (186052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:119a5fd04ebf8a2ee4f6476233145b8923f667a97a8c22c43bcf7bac0df4c3ca`  
		Last Modified: Fri, 24 Oct 2025 01:33:25 GMT  
		Size: 11.9 KB (11855 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:09fa24dd191fd7d10f1ab5e55ee24e70186dda655d331071724547150520b26d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:3c62798d9ade7bb0752bf0ebe859448dd01cea55cb5282c3365f6daf606c9efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179609194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70bb6676cb8c9a0ed29aff6f7d3f916b8b4ca7be8b1f8e9a88ade89d561864a`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 07:54:11 GMT
MAINTAINER Rob Hoelz
# Tue, 04 Nov 2025 07:54:11 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 04 Nov 2025 07:54:11 GMT
ARG rakudo_version=2025.10-01
# Tue, 04 Nov 2025 07:54:11 GMT
ENV rakudo_version=2025.10-01
# Tue, 04 Nov 2025 08:07:41 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 08:07:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 04 Nov 2025 08:07:41 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb445e472b1bad54f5a28edd51b11aec79eca8513394866a261891be9da6a343`  
		Last Modified: Tue, 04 Nov 2025 00:28:00 GMT  
		Size: 24.0 MB (24029301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2123190679e81d983648da92f1bb9ddc74383512edb00ad64f93d24d00d8807a`  
		Last Modified: Tue, 04 Nov 2025 04:14:49 GMT  
		Size: 64.4 MB (64396145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633ac49056b7e7c2f64edced1ade8a636680f9bf6791553ff98e4d880d3f4e38`  
		Last Modified: Tue, 04 Nov 2025 08:54:06 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb7d7339212c95d87768b3f020e3e2a4cdc95a79cf73e40a0e279f480958d45`  
		Last Modified: Tue, 04 Nov 2025 08:54:20 GMT  
		Size: 42.7 MB (42699451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:42f57bd9717fe38a745397f956c5e7e88bd6674637065b8105b125bdec0450ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b297f186483aa478e4a201fc65eef874fafb2b11d8e7902382c42624bc564eac`

```dockerfile
```

-	Layers:
	-	`sha256:cb95eaf12a4e70fa6293c6e6cc66b3c76db2bac5e69d31a8f6e3b04f137596a3`  
		Last Modified: Tue, 04 Nov 2025 11:33:21 GMT  
		Size: 8.0 MB (7967804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96286a82ebaa1e4ba9580f5ad9a8442e5da01e87c7284c86d10077489a4cfdce`  
		Last Modified: Tue, 04 Nov 2025 11:33:21 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:2a61b910303225f3064bc18c7a17a27dfe04e5f9c17aacbf1e6e3d6f0470481d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177094097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac904f2c5def4a31a6f61eb5e4e0b3d90add82b1552e08ff43d40ac78f7aada`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:29:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:33:38 GMT
MAINTAINER Rob Hoelz
# Tue, 04 Nov 2025 02:33:38 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 04 Nov 2025 02:33:38 GMT
ARG rakudo_version=2025.10-01
# Tue, 04 Nov 2025 02:33:38 GMT
ENV rakudo_version=2025.10-01
# Tue, 04 Nov 2025 02:52:06 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 02:52:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 04 Nov 2025 02:52:06 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463896571d3ff5317461a64229e9e4cb27d6d877114079419cf8b4fc96b0c02`  
		Last Modified: Tue, 04 Nov 2025 00:30:33 GMT  
		Size: 23.6 MB (23598514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020f0f7f102dcd1ca7603a86d7398adbe5369a820cc6f32954c0b3b5e2ac7403`  
		Last Modified: Tue, 04 Nov 2025 01:30:05 GMT  
		Size: 64.4 MB (64371335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f54836e448885f2f4db146794f3b923a57237811bcaa8e804da471d9b0f5ba`  
		Last Modified: Tue, 04 Nov 2025 02:52:37 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaf1f2ddf6a9cfd9dbf571c7063995b649c2f7c6d8e94e9aefef41dbc665012`  
		Last Modified: Tue, 04 Nov 2025 02:52:43 GMT  
		Size: 40.8 MB (40761533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:098090b1ddaec33ab798033b77aa66bcc14dd47bbfdd4aa34d59a8c1ac9c1a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a1df382b01c308a96b9a7d24875fd6763acaf013e1c59c8dee752bdea6257a`

```dockerfile
```

-	Layers:
	-	`sha256:b167a316173c64af749917f0de4c9835e291de4a4c9a0fb5569a089b02862467`  
		Last Modified: Tue, 04 Nov 2025 11:33:28 GMT  
		Size: 8.0 MB (7974197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08742e7b975b9c0e7f7b679d6ecec4245cd71f8679d214afb14d172fc83c48e`  
		Last Modified: Tue, 04 Nov 2025 11:33:28 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:0ca0c4402045a0fe331671e0f62bd6861e8cdc5c920dae47f062053c9932789c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:cf86957b35679695d7a352ab4d89ec498d93b3d136c74369ed2bbc20e6a740a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184825431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae044e46e5d07efb52cdcfa92a73f9852ee3b9a8a30e5711e63df247649ade5d`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 07:42:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 11:17:00 GMT
MAINTAINER AntonOks
# Tue, 04 Nov 2025 11:17:00 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 04 Nov 2025 11:17:00 GMT
ARG rakudo_version=2025.10-01
# Tue, 04 Nov 2025 11:17:00 GMT
ENV rakudo_version=2025.10-01
# Tue, 04 Nov 2025 11:33:45 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 11:33:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 04 Nov 2025 11:33:45 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3143549f2b8b3ad8d79efdc47824641c6771796b3770f3c637a38aabd2b3462`  
		Last Modified: Tue, 04 Nov 2025 04:14:53 GMT  
		Size: 25.6 MB (25615393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e8e93b0d018b135d833207c6feaba205653ac52e0a80d214477ec0de239dee`  
		Last Modified: Tue, 04 Nov 2025 07:43:02 GMT  
		Size: 67.8 MB (67776858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78db28b0b23217f4f7e9b0dd25ad6daf33ac267840f3d806cf1a1989a00b7ea2`  
		Last Modified: Tue, 04 Nov 2025 11:34:07 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c44c7e54d667d73c03f35c013712ecb39086403f65fb817f50da55a970e7f36`  
		Last Modified: Tue, 04 Nov 2025 11:34:13 GMT  
		Size: 42.1 MB (42144313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:90176f2764cd6354380e7a9d7b2c8055083e8a00b516d8ff17ff9d8422116cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ef6909df47dac6d0570add6a8eb0629222d01bf4334888d0e214d53ed8e203`

```dockerfile
```

-	Layers:
	-	`sha256:35452f6bfc9f81583f224ebdde4be6622bfc14bbf0abddda9618ba709e8fb3c3`  
		Last Modified: Tue, 04 Nov 2025 14:33:21 GMT  
		Size: 7.8 MB (7769451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:652e71426534d396a8b2b896c041a36126b96d312cd74d2df18e392dfb44eb6e`  
		Last Modified: Tue, 04 Nov 2025 14:33:21 GMT  
		Size: 13.0 KB (12992 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:10cf88e7568d31fe8a044d887e5a6c8b3a9284f339fd5d730437b7de6a2868d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (183036871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2b10b6968f21ef4c853528185f2f37b6d3e802a0cf7b02e81da8f514bca00a`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:20:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:30:57 GMT
MAINTAINER AntonOks
# Tue, 04 Nov 2025 03:30:57 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 04 Nov 2025 03:30:57 GMT
ARG rakudo_version=2025.10-01
# Tue, 04 Nov 2025 03:30:57 GMT
ENV rakudo_version=2025.10-01
# Tue, 04 Nov 2025 03:49:26 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 03:49:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 04 Nov 2025 03:49:26 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f766ef2ec48737a0f300405019c312acd667d14467b50c402750d1454e3591`  
		Last Modified: Tue, 04 Nov 2025 01:30:11 GMT  
		Size: 25.0 MB (25017577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186d0d0b2411f880d1a385216013fead1acb2dee0584aac75da87dfdeb1202db`  
		Last Modified: Tue, 04 Nov 2025 02:21:20 GMT  
		Size: 67.6 MB (67583874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05b9da4e0e176636bb48a7c9235bd155818dff94ba349815aa97e9e224c7dd3`  
		Last Modified: Tue, 04 Nov 2025 03:49:47 GMT  
		Size: 3.2 KB (3243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535e1825c308d54722e04831f1c621c8c95733439975df1b3a22b8bdef1160f3`  
		Last Modified: Tue, 04 Nov 2025 03:49:49 GMT  
		Size: 40.8 MB (40781747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3bedf9cd88476cc2ed75fc4e5c0643b52d75737885eac3dd81b202edeb1d9b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27fcb103193e5349298658c95ef0e1c9be7acba78ef76ee584ea711c3c216211`

```dockerfile
```

-	Layers:
	-	`sha256:0fd1dcb1baa2b9f9f3685f106e113c71357f3e7bb323b86214c3053280af1317`  
		Last Modified: Tue, 04 Nov 2025 11:33:32 GMT  
		Size: 7.8 MB (7777126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2c467e605ba7ccbe64606b2c732f6567a51eaf1828c91d300b2606bd8cf08be`  
		Last Modified: Tue, 04 Nov 2025 11:33:33 GMT  
		Size: 13.1 KB (13099 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:0ca0c4402045a0fe331671e0f62bd6861e8cdc5c920dae47f062053c9932789c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:cf86957b35679695d7a352ab4d89ec498d93b3d136c74369ed2bbc20e6a740a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184825431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae044e46e5d07efb52cdcfa92a73f9852ee3b9a8a30e5711e63df247649ade5d`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 07:42:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 11:17:00 GMT
MAINTAINER AntonOks
# Tue, 04 Nov 2025 11:17:00 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 04 Nov 2025 11:17:00 GMT
ARG rakudo_version=2025.10-01
# Tue, 04 Nov 2025 11:17:00 GMT
ENV rakudo_version=2025.10-01
# Tue, 04 Nov 2025 11:33:45 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 11:33:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 04 Nov 2025 11:33:45 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3143549f2b8b3ad8d79efdc47824641c6771796b3770f3c637a38aabd2b3462`  
		Last Modified: Tue, 04 Nov 2025 04:14:53 GMT  
		Size: 25.6 MB (25615393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e8e93b0d018b135d833207c6feaba205653ac52e0a80d214477ec0de239dee`  
		Last Modified: Tue, 04 Nov 2025 07:43:02 GMT  
		Size: 67.8 MB (67776858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78db28b0b23217f4f7e9b0dd25ad6daf33ac267840f3d806cf1a1989a00b7ea2`  
		Last Modified: Tue, 04 Nov 2025 11:34:07 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c44c7e54d667d73c03f35c013712ecb39086403f65fb817f50da55a970e7f36`  
		Last Modified: Tue, 04 Nov 2025 11:34:13 GMT  
		Size: 42.1 MB (42144313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:90176f2764cd6354380e7a9d7b2c8055083e8a00b516d8ff17ff9d8422116cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ef6909df47dac6d0570add6a8eb0629222d01bf4334888d0e214d53ed8e203`

```dockerfile
```

-	Layers:
	-	`sha256:35452f6bfc9f81583f224ebdde4be6622bfc14bbf0abddda9618ba709e8fb3c3`  
		Last Modified: Tue, 04 Nov 2025 14:33:21 GMT  
		Size: 7.8 MB (7769451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:652e71426534d396a8b2b896c041a36126b96d312cd74d2df18e392dfb44eb6e`  
		Last Modified: Tue, 04 Nov 2025 14:33:21 GMT  
		Size: 13.0 KB (12992 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:10cf88e7568d31fe8a044d887e5a6c8b3a9284f339fd5d730437b7de6a2868d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (183036871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2b10b6968f21ef4c853528185f2f37b6d3e802a0cf7b02e81da8f514bca00a`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:20:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:30:57 GMT
MAINTAINER AntonOks
# Tue, 04 Nov 2025 03:30:57 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 04 Nov 2025 03:30:57 GMT
ARG rakudo_version=2025.10-01
# Tue, 04 Nov 2025 03:30:57 GMT
ENV rakudo_version=2025.10-01
# Tue, 04 Nov 2025 03:49:26 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 03:49:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 04 Nov 2025 03:49:26 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f766ef2ec48737a0f300405019c312acd667d14467b50c402750d1454e3591`  
		Last Modified: Tue, 04 Nov 2025 01:30:11 GMT  
		Size: 25.0 MB (25017577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186d0d0b2411f880d1a385216013fead1acb2dee0584aac75da87dfdeb1202db`  
		Last Modified: Tue, 04 Nov 2025 02:21:20 GMT  
		Size: 67.6 MB (67583874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05b9da4e0e176636bb48a7c9235bd155818dff94ba349815aa97e9e224c7dd3`  
		Last Modified: Tue, 04 Nov 2025 03:49:47 GMT  
		Size: 3.2 KB (3243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535e1825c308d54722e04831f1c621c8c95733439975df1b3a22b8bdef1160f3`  
		Last Modified: Tue, 04 Nov 2025 03:49:49 GMT  
		Size: 40.8 MB (40781747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3bedf9cd88476cc2ed75fc4e5c0643b52d75737885eac3dd81b202edeb1d9b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27fcb103193e5349298658c95ef0e1c9be7acba78ef76ee584ea711c3c216211`

```dockerfile
```

-	Layers:
	-	`sha256:0fd1dcb1baa2b9f9f3685f106e113c71357f3e7bb323b86214c3053280af1317`  
		Last Modified: Tue, 04 Nov 2025 11:33:32 GMT  
		Size: 7.8 MB (7777126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2c467e605ba7ccbe64606b2c732f6567a51eaf1828c91d300b2606bd8cf08be`  
		Last Modified: Tue, 04 Nov 2025 11:33:33 GMT  
		Size: 13.1 KB (13099 bytes)  
		MIME: application/vnd.in-toto+json
