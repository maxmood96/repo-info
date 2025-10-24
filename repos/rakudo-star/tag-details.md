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
$ docker pull rakudo-star@sha256:0118a95804eb6ac356ba1c4ec4c464bfd04addbf56b1f8ea02ac46fcd4053942
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.10-bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:fa7cc20e218e01bf4efa87d82c1f6e9478c32fc1c3f6c738135c0366e746e234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179611469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dccfd7f238df624eddf3f521636d625481e22906b43441102e8f455899456e50`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
MAINTAINER Rob Hoelz
# Thu, 23 Oct 2025 03:12:19 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ARG rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
ENV rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 23 Oct 2025 03:12:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f279d33abc52c7384e0cbbb666ea22064ea29b50a968ec29ae3ad817f62e16e7`  
		Last Modified: Tue, 21 Oct 2025 04:46:37 GMT  
		Size: 24.0 MB (24028898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daa5a418829f3daa90a80438cd84706b5f7fa0c795eb7936874864ef1ab7b0c`  
		Last Modified: Tue, 21 Oct 2025 04:47:27 GMT  
		Size: 64.4 MB (64396405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b172132cc2f4256912ce276844a6f5f98cd39f62222a4593e32061d3a80d37cb`  
		Last Modified: Thu, 23 Oct 2025 23:46:15 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d9a86f1ae3a263ac5928cecc3a54136c6149d40282e5ba3db1837aee4d8f18`  
		Last Modified: Thu, 23 Oct 2025 23:46:19 GMT  
		Size: 42.7 MB (42702366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:9f2d50ca21fc05d3a382f5f3bdf833ca2785a1d3fc9f96dcff6af7dff4126162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d47a810159f6d123355a56ad8cc3d73ce17940777bdf07bf39580d469129c37`

```dockerfile
```

-	Layers:
	-	`sha256:a1dca53b9d97c3d5d7a3cfb0fda15cf3fde696b7055f3d87c3a5b8786df409cb`  
		Last Modified: Fri, 24 Oct 2025 01:33:27 GMT  
		Size: 8.0 MB (7967804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e6666b8379f3becee7043e296aa478ae31e8dbc7200a5801f275a7d3247b9e`  
		Last Modified: Fri, 24 Oct 2025 01:33:28 GMT  
		Size: 12.7 KB (12745 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:749f5d5b569f7d3934eca2c986480bb3d741db10854ec85dcd5989a7037b40ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177127550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d478cd1ec80932e8ed43ffffa1afde22fe56521063a22b5991b2d41517666a8`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
MAINTAINER Rob Hoelz
# Thu, 23 Oct 2025 03:12:19 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ARG rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
ENV rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 23 Oct 2025 03:12:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add7397bc0ae282f3ecd02217ad720d86eab3a3d325f0bfed57fc864c2281a58`  
		Last Modified: Tue, 21 Oct 2025 01:46:17 GMT  
		Size: 23.6 MB (23597991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd15270faa4e93fc4bcc62caecce8d2f5dfc1443d3c99572dfb689973b24c0a4`  
		Last Modified: Tue, 21 Oct 2025 02:35:23 GMT  
		Size: 64.4 MB (64370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fe3a92f044a9261ca742e556427ccec98be6fc6dc4cdd1cbf963eba90125f0`  
		Last Modified: Thu, 23 Oct 2025 22:05:50 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1aaaa75045291e039a37c4dcb42e4d439259a95f3cd40414d45558e76c210b`  
		Last Modified: Thu, 23 Oct 2025 22:05:59 GMT  
		Size: 40.8 MB (40796391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:c3b21a851f50e7197d884a66406d9cb545ae9321d878ba350cc2e0e10effcd77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ec337f92c9431f7ba1cdddf7dd6fa619616ee5bfbd9c5a2e259fdfa87fd568`

```dockerfile
```

-	Layers:
	-	`sha256:ff1eaf2f164f836cbda000790be218371bbbf55774ef617982d22af87bea6c8a`  
		Last Modified: Thu, 23 Oct 2025 22:33:20 GMT  
		Size: 8.0 MB (7974197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3ef17180b32c661dd4a79a4ed0c2ed3aa44d20d4ffa1c3434d8b168cd5dc017`  
		Last Modified: Thu, 23 Oct 2025 22:33:21 GMT  
		Size: 12.8 KB (12841 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2025.10-trixie`

```console
$ docker pull rakudo-star@sha256:f18987ecda7b990e85f84cc981b5fd990c4734ad9312aba4d35fb56991da9fca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.10-trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:c238c93fc010f2c661647546f1978fc72d04fae91bf6e85c11df37805b365cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185411700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9ae01988c2cc9743c92bea9140bcab1eba639c974e4af9b860c31b0e06c8e3`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
MAINTAINER AntonOks
# Thu, 23 Oct 2025 03:12:19 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ARG rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
ENV rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 23 Oct 2025 03:12:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d573bf42b377ce6a5a0451c15388849686fa4058efd68999f3b014daeb5b55`  
		Last Modified: Tue, 21 Oct 2025 01:42:47 GMT  
		Size: 25.6 MB (25615545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dfe2fac1c486e9aaf41d1028ed30be2c442aa84af44462bc7bac8c148ffb13`  
		Last Modified: Tue, 21 Oct 2025 04:47:38 GMT  
		Size: 67.8 MB (67784857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28e4c8432e07dfa537af083805a9c9f2e700e3bc33c42e205a59b3430544218`  
		Last Modified: Thu, 23 Oct 2025 23:47:58 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7c18d8c15a98323a619afa5e501fc1266640bfbfc63655070a78014019cbea`  
		Last Modified: Thu, 23 Oct 2025 23:48:01 GMT  
		Size: 42.7 MB (42723087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:5fd584928abe60a0b231db40dbdddea5741e723e5a97146e49dd78145bd28acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c1ccfbb50bc343309cbdfac05e86d17b34f93d7bb3f097a5b8c08b099d2584`

```dockerfile
```

-	Layers:
	-	`sha256:d092c865f9f864f0ce4c1cf64f60bdab4a52ead101902cdb87d291d725c6c070`  
		Last Modified: Fri, 24 Oct 2025 01:33:33 GMT  
		Size: 7.8 MB (7769451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48cd81fc0ecb8945f6e8db9673f63528b13f1c3d975851bfdc172eaf5ce0276e`  
		Last Modified: Fri, 24 Oct 2025 01:33:34 GMT  
		Size: 13.0 KB (13036 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.10-trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:efa3cb65a9f188e7e28792f6b94da590744fe7c26be4307062e24d7b591906c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183281823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c3ce4a8b57151b84165e0f644ac8dceef5955a8854175d9519141a27071dac`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
MAINTAINER AntonOks
# Thu, 23 Oct 2025 03:12:19 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ARG rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
ENV rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 23 Oct 2025 03:12:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510ac7d6fe76c0362c0162daee6964c5b93b20f5ddf65021b0bf3bcce16f306`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 25.0 MB (25017463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721433549fef8bfa398445abce4a12b5c7e64775b3de57bfc3ff37c8ed6fc0e4`  
		Last Modified: Tue, 21 Oct 2025 02:35:46 GMT  
		Size: 67.6 MB (67583109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd15d70036d0a5d6cd3395ca3453c84ec12b47f4ba2b57fae943a73ff1a29c55`  
		Last Modified: Thu, 23 Oct 2025 22:06:15 GMT  
		Size: 3.2 KB (3235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc65f543e3e31381d80d35a2dc8275cddd499c6a6dd12fba589131e02aa88298`  
		Last Modified: Thu, 23 Oct 2025 22:06:22 GMT  
		Size: 41.0 MB (41028273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3bafa09fe111721454bca973fd52f270ef011d2b460b72eba0311bb14a525443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44f043e1c2004533c24779c2f248ee1dd60ab8466ee8b48f2730c349ff48638`

```dockerfile
```

-	Layers:
	-	`sha256:cbb3e456afe899be9ea69b4073f387a2b9fa35a77933982a706c5e929ed6182a`  
		Last Modified: Thu, 23 Oct 2025 22:33:25 GMT  
		Size: 7.8 MB (7777126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9c7dc1b7755bc27925ebd6c792de5cf7f0e0993578d190fac1b1f7ae214e751`  
		Last Modified: Thu, 23 Oct 2025 22:33:26 GMT  
		Size: 13.1 KB (13143 bytes)  
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
$ docker pull rakudo-star@sha256:0118a95804eb6ac356ba1c4ec4c464bfd04addbf56b1f8ea02ac46fcd4053942
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:fa7cc20e218e01bf4efa87d82c1f6e9478c32fc1c3f6c738135c0366e746e234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179611469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dccfd7f238df624eddf3f521636d625481e22906b43441102e8f455899456e50`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
MAINTAINER Rob Hoelz
# Thu, 23 Oct 2025 03:12:19 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ARG rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
ENV rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 23 Oct 2025 03:12:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f279d33abc52c7384e0cbbb666ea22064ea29b50a968ec29ae3ad817f62e16e7`  
		Last Modified: Tue, 21 Oct 2025 04:46:37 GMT  
		Size: 24.0 MB (24028898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daa5a418829f3daa90a80438cd84706b5f7fa0c795eb7936874864ef1ab7b0c`  
		Last Modified: Tue, 21 Oct 2025 04:47:27 GMT  
		Size: 64.4 MB (64396405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b172132cc2f4256912ce276844a6f5f98cd39f62222a4593e32061d3a80d37cb`  
		Last Modified: Thu, 23 Oct 2025 23:46:15 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d9a86f1ae3a263ac5928cecc3a54136c6149d40282e5ba3db1837aee4d8f18`  
		Last Modified: Thu, 23 Oct 2025 23:46:19 GMT  
		Size: 42.7 MB (42702366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:9f2d50ca21fc05d3a382f5f3bdf833ca2785a1d3fc9f96dcff6af7dff4126162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d47a810159f6d123355a56ad8cc3d73ce17940777bdf07bf39580d469129c37`

```dockerfile
```

-	Layers:
	-	`sha256:a1dca53b9d97c3d5d7a3cfb0fda15cf3fde696b7055f3d87c3a5b8786df409cb`  
		Last Modified: Fri, 24 Oct 2025 01:33:27 GMT  
		Size: 8.0 MB (7967804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e6666b8379f3becee7043e296aa478ae31e8dbc7200a5801f275a7d3247b9e`  
		Last Modified: Fri, 24 Oct 2025 01:33:28 GMT  
		Size: 12.7 KB (12745 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:749f5d5b569f7d3934eca2c986480bb3d741db10854ec85dcd5989a7037b40ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177127550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d478cd1ec80932e8ed43ffffa1afde22fe56521063a22b5991b2d41517666a8`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
MAINTAINER Rob Hoelz
# Thu, 23 Oct 2025 03:12:19 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ARG rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
ENV rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 23 Oct 2025 03:12:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add7397bc0ae282f3ecd02217ad720d86eab3a3d325f0bfed57fc864c2281a58`  
		Last Modified: Tue, 21 Oct 2025 01:46:17 GMT  
		Size: 23.6 MB (23597991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd15270faa4e93fc4bcc62caecce8d2f5dfc1443d3c99572dfb689973b24c0a4`  
		Last Modified: Tue, 21 Oct 2025 02:35:23 GMT  
		Size: 64.4 MB (64370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fe3a92f044a9261ca742e556427ccec98be6fc6dc4cdd1cbf963eba90125f0`  
		Last Modified: Thu, 23 Oct 2025 22:05:50 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1aaaa75045291e039a37c4dcb42e4d439259a95f3cd40414d45558e76c210b`  
		Last Modified: Thu, 23 Oct 2025 22:05:59 GMT  
		Size: 40.8 MB (40796391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:c3b21a851f50e7197d884a66406d9cb545ae9321d878ba350cc2e0e10effcd77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ec337f92c9431f7ba1cdddf7dd6fa619616ee5bfbd9c5a2e259fdfa87fd568`

```dockerfile
```

-	Layers:
	-	`sha256:ff1eaf2f164f836cbda000790be218371bbbf55774ef617982d22af87bea6c8a`  
		Last Modified: Thu, 23 Oct 2025 22:33:20 GMT  
		Size: 8.0 MB (7974197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3ef17180b32c661dd4a79a4ed0c2ed3aa44d20d4ffa1c3434d8b168cd5dc017`  
		Last Modified: Thu, 23 Oct 2025 22:33:21 GMT  
		Size: 12.8 KB (12841 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:f18987ecda7b990e85f84cc981b5fd990c4734ad9312aba4d35fb56991da9fca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:c238c93fc010f2c661647546f1978fc72d04fae91bf6e85c11df37805b365cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185411700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9ae01988c2cc9743c92bea9140bcab1eba639c974e4af9b860c31b0e06c8e3`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
MAINTAINER AntonOks
# Thu, 23 Oct 2025 03:12:19 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ARG rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
ENV rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 23 Oct 2025 03:12:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d573bf42b377ce6a5a0451c15388849686fa4058efd68999f3b014daeb5b55`  
		Last Modified: Tue, 21 Oct 2025 01:42:47 GMT  
		Size: 25.6 MB (25615545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dfe2fac1c486e9aaf41d1028ed30be2c442aa84af44462bc7bac8c148ffb13`  
		Last Modified: Tue, 21 Oct 2025 04:47:38 GMT  
		Size: 67.8 MB (67784857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28e4c8432e07dfa537af083805a9c9f2e700e3bc33c42e205a59b3430544218`  
		Last Modified: Thu, 23 Oct 2025 23:47:58 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7c18d8c15a98323a619afa5e501fc1266640bfbfc63655070a78014019cbea`  
		Last Modified: Thu, 23 Oct 2025 23:48:01 GMT  
		Size: 42.7 MB (42723087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:5fd584928abe60a0b231db40dbdddea5741e723e5a97146e49dd78145bd28acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c1ccfbb50bc343309cbdfac05e86d17b34f93d7bb3f097a5b8c08b099d2584`

```dockerfile
```

-	Layers:
	-	`sha256:d092c865f9f864f0ce4c1cf64f60bdab4a52ead101902cdb87d291d725c6c070`  
		Last Modified: Fri, 24 Oct 2025 01:33:33 GMT  
		Size: 7.8 MB (7769451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48cd81fc0ecb8945f6e8db9673f63528b13f1c3d975851bfdc172eaf5ce0276e`  
		Last Modified: Fri, 24 Oct 2025 01:33:34 GMT  
		Size: 13.0 KB (13036 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:efa3cb65a9f188e7e28792f6b94da590744fe7c26be4307062e24d7b591906c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183281823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c3ce4a8b57151b84165e0f644ac8dceef5955a8854175d9519141a27071dac`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
MAINTAINER AntonOks
# Thu, 23 Oct 2025 03:12:19 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ARG rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
ENV rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 23 Oct 2025 03:12:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510ac7d6fe76c0362c0162daee6964c5b93b20f5ddf65021b0bf3bcce16f306`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 25.0 MB (25017463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721433549fef8bfa398445abce4a12b5c7e64775b3de57bfc3ff37c8ed6fc0e4`  
		Last Modified: Tue, 21 Oct 2025 02:35:46 GMT  
		Size: 67.6 MB (67583109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd15d70036d0a5d6cd3395ca3453c84ec12b47f4ba2b57fae943a73ff1a29c55`  
		Last Modified: Thu, 23 Oct 2025 22:06:15 GMT  
		Size: 3.2 KB (3235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc65f543e3e31381d80d35a2dc8275cddd499c6a6dd12fba589131e02aa88298`  
		Last Modified: Thu, 23 Oct 2025 22:06:22 GMT  
		Size: 41.0 MB (41028273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3bafa09fe111721454bca973fd52f270ef011d2b460b72eba0311bb14a525443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44f043e1c2004533c24779c2f248ee1dd60ab8466ee8b48f2730c349ff48638`

```dockerfile
```

-	Layers:
	-	`sha256:cbb3e456afe899be9ea69b4073f387a2b9fa35a77933982a706c5e929ed6182a`  
		Last Modified: Thu, 23 Oct 2025 22:33:25 GMT  
		Size: 7.8 MB (7777126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9c7dc1b7755bc27925ebd6c792de5cf7f0e0993578d190fac1b1f7ae214e751`  
		Last Modified: Thu, 23 Oct 2025 22:33:26 GMT  
		Size: 13.1 KB (13143 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:f18987ecda7b990e85f84cc981b5fd990c4734ad9312aba4d35fb56991da9fca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:c238c93fc010f2c661647546f1978fc72d04fae91bf6e85c11df37805b365cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185411700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9ae01988c2cc9743c92bea9140bcab1eba639c974e4af9b860c31b0e06c8e3`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
MAINTAINER AntonOks
# Thu, 23 Oct 2025 03:12:19 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ARG rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
ENV rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 23 Oct 2025 03:12:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d573bf42b377ce6a5a0451c15388849686fa4058efd68999f3b014daeb5b55`  
		Last Modified: Tue, 21 Oct 2025 01:42:47 GMT  
		Size: 25.6 MB (25615545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dfe2fac1c486e9aaf41d1028ed30be2c442aa84af44462bc7bac8c148ffb13`  
		Last Modified: Tue, 21 Oct 2025 04:47:38 GMT  
		Size: 67.8 MB (67784857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28e4c8432e07dfa537af083805a9c9f2e700e3bc33c42e205a59b3430544218`  
		Last Modified: Thu, 23 Oct 2025 23:47:58 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7c18d8c15a98323a619afa5e501fc1266640bfbfc63655070a78014019cbea`  
		Last Modified: Thu, 23 Oct 2025 23:48:01 GMT  
		Size: 42.7 MB (42723087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:5fd584928abe60a0b231db40dbdddea5741e723e5a97146e49dd78145bd28acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c1ccfbb50bc343309cbdfac05e86d17b34f93d7bb3f097a5b8c08b099d2584`

```dockerfile
```

-	Layers:
	-	`sha256:d092c865f9f864f0ce4c1cf64f60bdab4a52ead101902cdb87d291d725c6c070`  
		Last Modified: Fri, 24 Oct 2025 01:33:33 GMT  
		Size: 7.8 MB (7769451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48cd81fc0ecb8945f6e8db9673f63528b13f1c3d975851bfdc172eaf5ce0276e`  
		Last Modified: Fri, 24 Oct 2025 01:33:34 GMT  
		Size: 13.0 KB (13036 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:efa3cb65a9f188e7e28792f6b94da590744fe7c26be4307062e24d7b591906c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183281823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c3ce4a8b57151b84165e0f644ac8dceef5955a8854175d9519141a27071dac`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
MAINTAINER AntonOks
# Thu, 23 Oct 2025 03:12:19 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ARG rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
ENV rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 23 Oct 2025 03:12:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510ac7d6fe76c0362c0162daee6964c5b93b20f5ddf65021b0bf3bcce16f306`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 25.0 MB (25017463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721433549fef8bfa398445abce4a12b5c7e64775b3de57bfc3ff37c8ed6fc0e4`  
		Last Modified: Tue, 21 Oct 2025 02:35:46 GMT  
		Size: 67.6 MB (67583109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd15d70036d0a5d6cd3395ca3453c84ec12b47f4ba2b57fae943a73ff1a29c55`  
		Last Modified: Thu, 23 Oct 2025 22:06:15 GMT  
		Size: 3.2 KB (3235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc65f543e3e31381d80d35a2dc8275cddd499c6a6dd12fba589131e02aa88298`  
		Last Modified: Thu, 23 Oct 2025 22:06:22 GMT  
		Size: 41.0 MB (41028273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3bafa09fe111721454bca973fd52f270ef011d2b460b72eba0311bb14a525443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44f043e1c2004533c24779c2f248ee1dd60ab8466ee8b48f2730c349ff48638`

```dockerfile
```

-	Layers:
	-	`sha256:cbb3e456afe899be9ea69b4073f387a2b9fa35a77933982a706c5e929ed6182a`  
		Last Modified: Thu, 23 Oct 2025 22:33:25 GMT  
		Size: 7.8 MB (7777126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9c7dc1b7755bc27925ebd6c792de5cf7f0e0993578d190fac1b1f7ae214e751`  
		Last Modified: Thu, 23 Oct 2025 22:33:26 GMT  
		Size: 13.1 KB (13143 bytes)  
		MIME: application/vnd.in-toto+json
