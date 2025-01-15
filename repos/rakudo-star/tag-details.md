<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2024.12`](#rakudo-star202412)
-	[`rakudo-star:2024.12-alpine`](#rakudo-star202412-alpine)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:bookworm`](#rakudo-starbookworm)
-	[`rakudo-star:latest`](#rakudo-starlatest)

## `rakudo-star:2024.12`

```console
$ docker pull rakudo-star@sha256:f11c6f6b62e62f6df4652282a03cc8636fcfa7b6465de1a61d37860f00d3da6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2024.12` - linux; amd64

```console
$ docker pull rakudo-star@sha256:58348c3380dd9e0b952ab18676f21266224a17caa3a4abc20849259de3934f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179519864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e029f8cf39569506140eae175d2efb474a65848c4e17e6eb1ef0c8715aa855e`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
MAINTAINER Rob Hoelz
# Mon, 16 Dec 2024 03:29:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 20:33:03 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684a51896c8291a1769034cf6e10971c82a82c43b6b4588d1c71d215953eaa61`  
		Last Modified: Tue, 14 Jan 2025 03:18:17 GMT  
		Size: 64.4 MB (64398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04f8dc5e92d4d608c833db2b4d87e31bf2ebf236efb0e445f3b9821fb6957b3`  
		Last Modified: Wed, 15 Jan 2025 00:03:53 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4e1a4420b2ef8e89628a9bbfb50a0882d416aca81571acc359169bccdb4a0b`  
		Last Modified: Tue, 14 Jan 2025 04:34:40 GMT  
		Size: 42.6 MB (42579340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2024.12` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:0d627df729c70483bb24888dd953e513bc0415832378823ee43f5da57edb6926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2fd6e78ac59ca15d52171f81c3dd2c283c309cabdfe83ea42c32c2f472e9ce6`

```dockerfile
```

-	Layers:
	-	`sha256:a518a365a2b7eea556a0ddd8a750c35898a6de842971acbd4209fe6850d4cc13`  
		Last Modified: Tue, 14 Jan 2025 04:34:39 GMT  
		Size: 7.8 MB (7758969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:367f025a9b064ad2b51eeb9ba2b2d32cfcf76c6abc5b407b9e94c0dc6f0cd9f8`  
		Last Modified: Tue, 14 Jan 2025 20:33:24 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2024.12` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f714227ecac99c76a364553e4f320ff161a508709dcec1e2c4dbaffa50f12873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177105126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10352e09764ae48efccfd154154a16a2af2ad5def16ebe09aaea201e7644ec31`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
MAINTAINER Rob Hoelz
# Mon, 16 Dec 2024 03:29:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 20:33:16 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5668aa1d66870e70ed95649b861be58d77e1808e472ce4be592ddcceb18df20`  
		Last Modified: Tue, 14 Jan 2025 22:08:43 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7eff42d4908ee892ddb83f4455ab011af3d6feae864235486f412300160b3d6`  
		Last Modified: Tue, 14 Jan 2025 22:08:57 GMT  
		Size: 40.8 MB (40840335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2024.12` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:9a3e2ac11db1530bca214d70b5dd477965e126ccb83deb79ac4ab6809e9a3995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09a493b160a90054b7491f289bc0e070846717d21383d219066ec70d698ba89`

```dockerfile
```

-	Layers:
	-	`sha256:1bfd91fd84e33faf6b79127433331e3f7f957820abd7ff652efccd43bed681b9`  
		Last Modified: Tue, 14 Jan 2025 18:14:31 GMT  
		Size: 7.8 MB (7765374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:926a2d81c90ac35974693a4f6b1ad49b908cb1e5ddbe12292c3d8dd640a47098`  
		Last Modified: Tue, 14 Jan 2025 18:14:30 GMT  
		Size: 13.1 KB (13135 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2024.12-alpine`

```console
$ docker pull rakudo-star@sha256:fb70065f1fbdaef6ff07ab22ba1b16027c538908881a24dea7a48b1202a8eb07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2024.12-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:384a583f64eb556a2b0ca05aac576f9e1cbb137bca1b8e838812a4e54ee2ab73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46340961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81764192a8cbf2f12b137442ab5ba1203b2a39131ea4f3e223f7ed387b102256`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Dec 2024 03:29:03 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 03:29:03 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf8b73e0ff864fb76f8769c64826f2a7c0864a28804843a01e12e0de8caf452`  
		Last Modified: Wed, 08 Jan 2025 18:36:32 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74bf2c3c3b4039559c6e7861911050f4ffa8156ac38552a5139b21b41e95c4e`  
		Last Modified: Wed, 08 Jan 2025 18:36:34 GMT  
		Size: 42.7 MB (42698289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2024.12-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:cb1a00894224576971c40cda63e03ce9047f63a627be546cb6608eacdbd07e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 KB (132460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3163c8d3b62a05ab5629a6e12b7ca895d5bdc8d21a2373682ac586c2a529d007`

```dockerfile
```

-	Layers:
	-	`sha256:9ecdb9f8a20f47bb5a40dfac19dc1309b5703d558ce361c7b8a2af617b86fc54`  
		Last Modified: Wed, 08 Jan 2025 18:36:32 GMT  
		Size: 120.7 KB (120720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dd9eefe60febc916d82649b7fe21ae3ca2be0a31938c57300d952edbf8afe44`  
		Last Modified: Wed, 08 Jan 2025 18:36:32 GMT  
		Size: 11.7 KB (11740 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2024.12-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:622a48f5c6f2f624089d829f8f0be7210b374c7581c7f9a458b10aa7adea71db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46532725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9eb6dc302a7500dbf738e889b531af4ce324c83fd0470ca1750f100088e411b`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Dec 2024 03:29:03 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 03:29:03 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59a85858ab78fc027ff09d8a5376e12d1c253c404713d7efe7405d9485c0658`  
		Last Modified: Thu, 09 Jan 2025 05:36:34 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bc37222c9c2729eb1560eab770571b8489e1b2a41d6798313691fa0d2bdce2`  
		Last Modified: Thu, 09 Jan 2025 05:36:36 GMT  
		Size: 42.5 MB (42539409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2024.12-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:32b4351b519969f0c07291760aa7923e07c04e43ba7d76032284154f54c3ef12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ed771a17bc112b5eac37f476c31631d522c7fa10f84498efa3c8e98e02a3f0`

```dockerfile
```

-	Layers:
	-	`sha256:53a7bbdb39dd309755f0b861de59689e4c3d7ac365f1250395d2919a76fb13bc`  
		Last Modified: Thu, 09 Jan 2025 05:36:34 GMT  
		Size: 120.8 KB (120752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f29f769a60dffdc0a10299cbe78eceef4ea168da59c2a6d6d4d2f8f00091385`  
		Last Modified: Thu, 09 Jan 2025 05:36:34 GMT  
		Size: 11.8 KB (11836 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:fb70065f1fbdaef6ff07ab22ba1b16027c538908881a24dea7a48b1202a8eb07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:384a583f64eb556a2b0ca05aac576f9e1cbb137bca1b8e838812a4e54ee2ab73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46340961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81764192a8cbf2f12b137442ab5ba1203b2a39131ea4f3e223f7ed387b102256`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Dec 2024 03:29:03 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 03:29:03 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf8b73e0ff864fb76f8769c64826f2a7c0864a28804843a01e12e0de8caf452`  
		Last Modified: Wed, 08 Jan 2025 18:36:32 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74bf2c3c3b4039559c6e7861911050f4ffa8156ac38552a5139b21b41e95c4e`  
		Last Modified: Wed, 08 Jan 2025 18:36:34 GMT  
		Size: 42.7 MB (42698289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:cb1a00894224576971c40cda63e03ce9047f63a627be546cb6608eacdbd07e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 KB (132460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3163c8d3b62a05ab5629a6e12b7ca895d5bdc8d21a2373682ac586c2a529d007`

```dockerfile
```

-	Layers:
	-	`sha256:9ecdb9f8a20f47bb5a40dfac19dc1309b5703d558ce361c7b8a2af617b86fc54`  
		Last Modified: Wed, 08 Jan 2025 18:36:32 GMT  
		Size: 120.7 KB (120720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dd9eefe60febc916d82649b7fe21ae3ca2be0a31938c57300d952edbf8afe44`  
		Last Modified: Wed, 08 Jan 2025 18:36:32 GMT  
		Size: 11.7 KB (11740 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:622a48f5c6f2f624089d829f8f0be7210b374c7581c7f9a458b10aa7adea71db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46532725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9eb6dc302a7500dbf738e889b531af4ce324c83fd0470ca1750f100088e411b`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Dec 2024 03:29:03 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 03:29:03 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59a85858ab78fc027ff09d8a5376e12d1c253c404713d7efe7405d9485c0658`  
		Last Modified: Thu, 09 Jan 2025 05:36:34 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bc37222c9c2729eb1560eab770571b8489e1b2a41d6798313691fa0d2bdce2`  
		Last Modified: Thu, 09 Jan 2025 05:36:36 GMT  
		Size: 42.5 MB (42539409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:32b4351b519969f0c07291760aa7923e07c04e43ba7d76032284154f54c3ef12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ed771a17bc112b5eac37f476c31631d522c7fa10f84498efa3c8e98e02a3f0`

```dockerfile
```

-	Layers:
	-	`sha256:53a7bbdb39dd309755f0b861de59689e4c3d7ac365f1250395d2919a76fb13bc`  
		Last Modified: Thu, 09 Jan 2025 05:36:34 GMT  
		Size: 120.8 KB (120752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f29f769a60dffdc0a10299cbe78eceef4ea168da59c2a6d6d4d2f8f00091385`  
		Last Modified: Thu, 09 Jan 2025 05:36:34 GMT  
		Size: 11.8 KB (11836 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:f11c6f6b62e62f6df4652282a03cc8636fcfa7b6465de1a61d37860f00d3da6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:58348c3380dd9e0b952ab18676f21266224a17caa3a4abc20849259de3934f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179519864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e029f8cf39569506140eae175d2efb474a65848c4e17e6eb1ef0c8715aa855e`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
MAINTAINER Rob Hoelz
# Mon, 16 Dec 2024 03:29:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 20:33:03 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684a51896c8291a1769034cf6e10971c82a82c43b6b4588d1c71d215953eaa61`  
		Last Modified: Tue, 14 Jan 2025 03:18:17 GMT  
		Size: 64.4 MB (64398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04f8dc5e92d4d608c833db2b4d87e31bf2ebf236efb0e445f3b9821fb6957b3`  
		Last Modified: Wed, 15 Jan 2025 00:03:53 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4e1a4420b2ef8e89628a9bbfb50a0882d416aca81571acc359169bccdb4a0b`  
		Last Modified: Tue, 14 Jan 2025 04:34:40 GMT  
		Size: 42.6 MB (42579340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:0d627df729c70483bb24888dd953e513bc0415832378823ee43f5da57edb6926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2fd6e78ac59ca15d52171f81c3dd2c283c309cabdfe83ea42c32c2f472e9ce6`

```dockerfile
```

-	Layers:
	-	`sha256:a518a365a2b7eea556a0ddd8a750c35898a6de842971acbd4209fe6850d4cc13`  
		Last Modified: Tue, 14 Jan 2025 04:34:39 GMT  
		Size: 7.8 MB (7758969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:367f025a9b064ad2b51eeb9ba2b2d32cfcf76c6abc5b407b9e94c0dc6f0cd9f8`  
		Last Modified: Tue, 14 Jan 2025 20:33:24 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f714227ecac99c76a364553e4f320ff161a508709dcec1e2c4dbaffa50f12873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177105126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10352e09764ae48efccfd154154a16a2af2ad5def16ebe09aaea201e7644ec31`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
MAINTAINER Rob Hoelz
# Mon, 16 Dec 2024 03:29:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 20:33:16 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5668aa1d66870e70ed95649b861be58d77e1808e472ce4be592ddcceb18df20`  
		Last Modified: Tue, 14 Jan 2025 22:08:43 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7eff42d4908ee892ddb83f4455ab011af3d6feae864235486f412300160b3d6`  
		Last Modified: Tue, 14 Jan 2025 22:08:57 GMT  
		Size: 40.8 MB (40840335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:9a3e2ac11db1530bca214d70b5dd477965e126ccb83deb79ac4ab6809e9a3995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09a493b160a90054b7491f289bc0e070846717d21383d219066ec70d698ba89`

```dockerfile
```

-	Layers:
	-	`sha256:1bfd91fd84e33faf6b79127433331e3f7f957820abd7ff652efccd43bed681b9`  
		Last Modified: Tue, 14 Jan 2025 18:14:31 GMT  
		Size: 7.8 MB (7765374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:926a2d81c90ac35974693a4f6b1ad49b908cb1e5ddbe12292c3d8dd640a47098`  
		Last Modified: Tue, 14 Jan 2025 18:14:30 GMT  
		Size: 13.1 KB (13135 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:f11c6f6b62e62f6df4652282a03cc8636fcfa7b6465de1a61d37860f00d3da6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:58348c3380dd9e0b952ab18676f21266224a17caa3a4abc20849259de3934f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179519864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e029f8cf39569506140eae175d2efb474a65848c4e17e6eb1ef0c8715aa855e`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
MAINTAINER Rob Hoelz
# Mon, 16 Dec 2024 03:29:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 20:33:03 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684a51896c8291a1769034cf6e10971c82a82c43b6b4588d1c71d215953eaa61`  
		Last Modified: Tue, 14 Jan 2025 03:18:17 GMT  
		Size: 64.4 MB (64398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04f8dc5e92d4d608c833db2b4d87e31bf2ebf236efb0e445f3b9821fb6957b3`  
		Last Modified: Wed, 15 Jan 2025 00:03:53 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4e1a4420b2ef8e89628a9bbfb50a0882d416aca81571acc359169bccdb4a0b`  
		Last Modified: Tue, 14 Jan 2025 04:34:40 GMT  
		Size: 42.6 MB (42579340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:0d627df729c70483bb24888dd953e513bc0415832378823ee43f5da57edb6926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2fd6e78ac59ca15d52171f81c3dd2c283c309cabdfe83ea42c32c2f472e9ce6`

```dockerfile
```

-	Layers:
	-	`sha256:a518a365a2b7eea556a0ddd8a750c35898a6de842971acbd4209fe6850d4cc13`  
		Last Modified: Tue, 14 Jan 2025 04:34:39 GMT  
		Size: 7.8 MB (7758969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:367f025a9b064ad2b51eeb9ba2b2d32cfcf76c6abc5b407b9e94c0dc6f0cd9f8`  
		Last Modified: Tue, 14 Jan 2025 20:33:24 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f714227ecac99c76a364553e4f320ff161a508709dcec1e2c4dbaffa50f12873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177105126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10352e09764ae48efccfd154154a16a2af2ad5def16ebe09aaea201e7644ec31`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
MAINTAINER Rob Hoelz
# Mon, 16 Dec 2024 03:29:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 20:33:16 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5668aa1d66870e70ed95649b861be58d77e1808e472ce4be592ddcceb18df20`  
		Last Modified: Tue, 14 Jan 2025 22:08:43 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7eff42d4908ee892ddb83f4455ab011af3d6feae864235486f412300160b3d6`  
		Last Modified: Tue, 14 Jan 2025 22:08:57 GMT  
		Size: 40.8 MB (40840335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:9a3e2ac11db1530bca214d70b5dd477965e126ccb83deb79ac4ab6809e9a3995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09a493b160a90054b7491f289bc0e070846717d21383d219066ec70d698ba89`

```dockerfile
```

-	Layers:
	-	`sha256:1bfd91fd84e33faf6b79127433331e3f7f957820abd7ff652efccd43bed681b9`  
		Last Modified: Tue, 14 Jan 2025 18:14:31 GMT  
		Size: 7.8 MB (7765374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:926a2d81c90ac35974693a4f6b1ad49b908cb1e5ddbe12292c3d8dd640a47098`  
		Last Modified: Tue, 14 Jan 2025 18:14:30 GMT  
		Size: 13.1 KB (13135 bytes)  
		MIME: application/vnd.in-toto+json
