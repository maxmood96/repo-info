<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2024.09`](#rakudo-star202409)
-	[`rakudo-star:2024.09-alpine`](#rakudo-star202409-alpine)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:bookworm`](#rakudo-starbookworm)
-	[`rakudo-star:latest`](#rakudo-starlatest)

## `rakudo-star:2024.09`

```console
$ docker pull rakudo-star@sha256:f312ebab90df78dfbfc03d1443b041597ac0d22f9459ffa70625b7dbdc6ad313
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2024.09` - linux; amd64

```console
$ docker pull rakudo-star@sha256:a0499029020a37ecd36530dc57732d64c235d966e23c64d0982891b0435a4166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182739140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7319d52987c484286c586957367d9390935d68508066153b9be6e266c790b63f`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
MAINTAINER Rob Hoelz
# Thu, 03 Oct 2024 21:11:49 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ARG rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
ENV rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
# ARGS: rakudo_version=2024.09-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 03 Oct 2024 21:11:49 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aadc5092c3b7a865666b14bef3d4d038282b19b124542f1a158c98ea8c1ed1b`  
		Last Modified: Sat, 19 Oct 2024 02:06:37 GMT  
		Size: 64.4 MB (64389695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab749272c30099f03f8c49996f5e111419c05868719baeaca0720d340f78e225`  
		Last Modified: Sat, 19 Oct 2024 03:13:32 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc68be86620db6bcaa51e79be7b13c6a946914994c096097e33a6e50a2b64083`  
		Last Modified: Sat, 19 Oct 2024 03:13:34 GMT  
		Size: 44.7 MB (44739798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2024.09` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:f610d3006227721d677010de108d43de007d7467b1dd2c33fff93cb16712105b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef405b4a27a3d22d0323826b6428dcca8b28500af4e688a53dc33f61c761767`

```dockerfile
```

-	Layers:
	-	`sha256:810b3410586fcfd2739871a6c6b395b5be996aa8582525996a0c2cd2135fa3e0`  
		Last Modified: Sat, 19 Oct 2024 03:13:32 GMT  
		Size: 7.8 MB (7770513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de1a2618d6b97cceb6493c0437fcc0eda6bcfb82e808b357d15f84d152c3b29`  
		Last Modified: Sat, 19 Oct 2024 03:13:32 GMT  
		Size: 13.0 KB (13027 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2024.09` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f5cc119e6c91288b6041930c81effe8f5436d7427e335eaf57abae5d28e7e243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182116475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6dabde9d137b2806093f2b378f21def1dad79bed40778529cd0f081f4bcde9`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
MAINTAINER Rob Hoelz
# Thu, 03 Oct 2024 21:11:49 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ARG rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
ENV rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
# ARGS: rakudo_version=2024.09-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 03 Oct 2024 21:11:49 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7694546334bb4c693d08ef9a468c3569b60245a9d50961ffcade2048f23441af`  
		Last Modified: Sat, 19 Oct 2024 09:24:35 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6f351b8738c6bdcc02f7009e4cefbe4f7a789bfc75bfdf98c375986c809a25`  
		Last Modified: Sat, 19 Oct 2024 09:24:36 GMT  
		Size: 44.6 MB (44584382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2024.09` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:90a181e11d2cba5cd7be4002100867cf707d4b763686d29dca9d3f445c48faa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d095eb7c49b5006be9bd7d8aaddfe57b221b40c25e3c8fdf8e34901b368ac136`

```dockerfile
```

-	Layers:
	-	`sha256:8e6af9eeca6352ea4c09df64cc49c1d27443e1ae514d38a93c099b8024dc2452`  
		Last Modified: Sat, 19 Oct 2024 09:24:35 GMT  
		Size: 7.8 MB (7776924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f1736eedae85f7e16be88883cd25bd7ed57d1d27404b2ac10c023f43ae29bb5`  
		Last Modified: Sat, 19 Oct 2024 09:24:35 GMT  
		Size: 13.2 KB (13153 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2024.09-alpine`

```console
$ docker pull rakudo-star@sha256:b2bd6c9526b339eb3ca3103b098571447f70c6296be183c8e362578e7cf170f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2024.09-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:9eec117e33b1800f007692bc8e82e6a8560365b6feb63e53894df7a5f717f803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48585272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21194f4d0380cfdd55c7c207fe9ce897942316397d9a996551507920cd29585`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 03 Oct 2024 21:11:49 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ARG rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
ENV rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
# ARGS: rakudo_version=2024.09-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 03 Oct 2024 21:11:49 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3128327b77aec3fd403bb2f7463b2edff305d97c91d7a8b722ac38e2bb2990`  
		Last Modified: Sat, 19 Oct 2024 01:13:54 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cfbb22abb757d26c6d46bd02f4587ee31ea93cb42946664bd9de36e2e20dc9`  
		Last Modified: Sat, 19 Oct 2024 01:13:55 GMT  
		Size: 45.0 MB (44960503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2024.09-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b699f7f0514961b048225d2f5f429f9958de9c61e83094375f4b521324c9693c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 KB (127376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7669ad49f8babedbf2f0dcc5d85d5468f2d2923065aaa0426a801ad5559b4c49`

```dockerfile
```

-	Layers:
	-	`sha256:3ac922819e3554c14292089660b41ae1cf6ed5d204f27e5da1534e6bf5ef3fa8`  
		Last Modified: Sat, 19 Oct 2024 01:13:54 GMT  
		Size: 115.8 KB (115835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:993aef0341f574e539cddf05e52b0e84fedc56dd08f51ee201d5b9a21841def5`  
		Last Modified: Sat, 19 Oct 2024 01:13:54 GMT  
		Size: 11.5 KB (11541 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2024.09-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f47630391219dcaa6188720c8ba0b64333ea67eaabe19e9ad19b23cf4cb00f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48884392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83be2540b8ee30dfc0178ecc3024c6f6f9523638df179f13b953256a5c5a09e9`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 03 Oct 2024 21:11:49 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ARG rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
ENV rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
# ARGS: rakudo_version=2024.09-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 03 Oct 2024 21:11:49 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3710cd6f66dcae21a2ea1d0e6836d71d87df8a4f52edd5e66addc9ae38299c`  
		Last Modified: Sat, 19 Oct 2024 05:09:33 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b82e14b7459207e44e6f82f4747c60b602cc6969958df0c5d7b8b9e06f03932`  
		Last Modified: Sat, 19 Oct 2024 05:09:35 GMT  
		Size: 44.8 MB (44795785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2024.09-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3bea723533bb6ab131f927edba830709a263e52aceb3e548709f73b952908a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 KB (127498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88897c4e77d87e26c6e8afacfe40e3db590be58e91d2029e731b4a7a6c1f5211`

```dockerfile
```

-	Layers:
	-	`sha256:91267b83f9a7c879fcfa073e2f51a3fcd4ae88668c247bbd8b5e50b6a9ee886a`  
		Last Modified: Sat, 19 Oct 2024 05:09:33 GMT  
		Size: 115.9 KB (115867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:496f11f4d0db711be504c58de58df1afd117ce7fe9a63b11a55ea3bd9e3f09d1`  
		Last Modified: Sat, 19 Oct 2024 05:09:33 GMT  
		Size: 11.6 KB (11631 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:b2bd6c9526b339eb3ca3103b098571447f70c6296be183c8e362578e7cf170f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:9eec117e33b1800f007692bc8e82e6a8560365b6feb63e53894df7a5f717f803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48585272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21194f4d0380cfdd55c7c207fe9ce897942316397d9a996551507920cd29585`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 03 Oct 2024 21:11:49 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ARG rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
ENV rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
# ARGS: rakudo_version=2024.09-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 03 Oct 2024 21:11:49 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3128327b77aec3fd403bb2f7463b2edff305d97c91d7a8b722ac38e2bb2990`  
		Last Modified: Sat, 19 Oct 2024 01:13:54 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cfbb22abb757d26c6d46bd02f4587ee31ea93cb42946664bd9de36e2e20dc9`  
		Last Modified: Sat, 19 Oct 2024 01:13:55 GMT  
		Size: 45.0 MB (44960503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b699f7f0514961b048225d2f5f429f9958de9c61e83094375f4b521324c9693c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 KB (127376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7669ad49f8babedbf2f0dcc5d85d5468f2d2923065aaa0426a801ad5559b4c49`

```dockerfile
```

-	Layers:
	-	`sha256:3ac922819e3554c14292089660b41ae1cf6ed5d204f27e5da1534e6bf5ef3fa8`  
		Last Modified: Sat, 19 Oct 2024 01:13:54 GMT  
		Size: 115.8 KB (115835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:993aef0341f574e539cddf05e52b0e84fedc56dd08f51ee201d5b9a21841def5`  
		Last Modified: Sat, 19 Oct 2024 01:13:54 GMT  
		Size: 11.5 KB (11541 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f47630391219dcaa6188720c8ba0b64333ea67eaabe19e9ad19b23cf4cb00f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48884392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83be2540b8ee30dfc0178ecc3024c6f6f9523638df179f13b953256a5c5a09e9`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 03 Oct 2024 21:11:49 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ARG rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
ENV rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
# ARGS: rakudo_version=2024.09-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 03 Oct 2024 21:11:49 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3710cd6f66dcae21a2ea1d0e6836d71d87df8a4f52edd5e66addc9ae38299c`  
		Last Modified: Sat, 19 Oct 2024 05:09:33 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b82e14b7459207e44e6f82f4747c60b602cc6969958df0c5d7b8b9e06f03932`  
		Last Modified: Sat, 19 Oct 2024 05:09:35 GMT  
		Size: 44.8 MB (44795785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3bea723533bb6ab131f927edba830709a263e52aceb3e548709f73b952908a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 KB (127498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88897c4e77d87e26c6e8afacfe40e3db590be58e91d2029e731b4a7a6c1f5211`

```dockerfile
```

-	Layers:
	-	`sha256:91267b83f9a7c879fcfa073e2f51a3fcd4ae88668c247bbd8b5e50b6a9ee886a`  
		Last Modified: Sat, 19 Oct 2024 05:09:33 GMT  
		Size: 115.9 KB (115867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:496f11f4d0db711be504c58de58df1afd117ce7fe9a63b11a55ea3bd9e3f09d1`  
		Last Modified: Sat, 19 Oct 2024 05:09:33 GMT  
		Size: 11.6 KB (11631 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:f312ebab90df78dfbfc03d1443b041597ac0d22f9459ffa70625b7dbdc6ad313
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:a0499029020a37ecd36530dc57732d64c235d966e23c64d0982891b0435a4166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182739140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7319d52987c484286c586957367d9390935d68508066153b9be6e266c790b63f`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
MAINTAINER Rob Hoelz
# Thu, 03 Oct 2024 21:11:49 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ARG rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
ENV rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
# ARGS: rakudo_version=2024.09-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 03 Oct 2024 21:11:49 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aadc5092c3b7a865666b14bef3d4d038282b19b124542f1a158c98ea8c1ed1b`  
		Last Modified: Sat, 19 Oct 2024 02:06:37 GMT  
		Size: 64.4 MB (64389695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab749272c30099f03f8c49996f5e111419c05868719baeaca0720d340f78e225`  
		Last Modified: Sat, 19 Oct 2024 03:13:32 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc68be86620db6bcaa51e79be7b13c6a946914994c096097e33a6e50a2b64083`  
		Last Modified: Sat, 19 Oct 2024 03:13:34 GMT  
		Size: 44.7 MB (44739798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:f610d3006227721d677010de108d43de007d7467b1dd2c33fff93cb16712105b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef405b4a27a3d22d0323826b6428dcca8b28500af4e688a53dc33f61c761767`

```dockerfile
```

-	Layers:
	-	`sha256:810b3410586fcfd2739871a6c6b395b5be996aa8582525996a0c2cd2135fa3e0`  
		Last Modified: Sat, 19 Oct 2024 03:13:32 GMT  
		Size: 7.8 MB (7770513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de1a2618d6b97cceb6493c0437fcc0eda6bcfb82e808b357d15f84d152c3b29`  
		Last Modified: Sat, 19 Oct 2024 03:13:32 GMT  
		Size: 13.0 KB (13027 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f5cc119e6c91288b6041930c81effe8f5436d7427e335eaf57abae5d28e7e243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182116475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6dabde9d137b2806093f2b378f21def1dad79bed40778529cd0f081f4bcde9`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
MAINTAINER Rob Hoelz
# Thu, 03 Oct 2024 21:11:49 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ARG rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
ENV rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
# ARGS: rakudo_version=2024.09-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 03 Oct 2024 21:11:49 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7694546334bb4c693d08ef9a468c3569b60245a9d50961ffcade2048f23441af`  
		Last Modified: Sat, 19 Oct 2024 09:24:35 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6f351b8738c6bdcc02f7009e4cefbe4f7a789bfc75bfdf98c375986c809a25`  
		Last Modified: Sat, 19 Oct 2024 09:24:36 GMT  
		Size: 44.6 MB (44584382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:90a181e11d2cba5cd7be4002100867cf707d4b763686d29dca9d3f445c48faa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d095eb7c49b5006be9bd7d8aaddfe57b221b40c25e3c8fdf8e34901b368ac136`

```dockerfile
```

-	Layers:
	-	`sha256:8e6af9eeca6352ea4c09df64cc49c1d27443e1ae514d38a93c099b8024dc2452`  
		Last Modified: Sat, 19 Oct 2024 09:24:35 GMT  
		Size: 7.8 MB (7776924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f1736eedae85f7e16be88883cd25bd7ed57d1d27404b2ac10c023f43ae29bb5`  
		Last Modified: Sat, 19 Oct 2024 09:24:35 GMT  
		Size: 13.2 KB (13153 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:f312ebab90df78dfbfc03d1443b041597ac0d22f9459ffa70625b7dbdc6ad313
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:a0499029020a37ecd36530dc57732d64c235d966e23c64d0982891b0435a4166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182739140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7319d52987c484286c586957367d9390935d68508066153b9be6e266c790b63f`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
MAINTAINER Rob Hoelz
# Thu, 03 Oct 2024 21:11:49 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ARG rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
ENV rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
# ARGS: rakudo_version=2024.09-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 03 Oct 2024 21:11:49 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aadc5092c3b7a865666b14bef3d4d038282b19b124542f1a158c98ea8c1ed1b`  
		Last Modified: Sat, 19 Oct 2024 02:06:37 GMT  
		Size: 64.4 MB (64389695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab749272c30099f03f8c49996f5e111419c05868719baeaca0720d340f78e225`  
		Last Modified: Sat, 19 Oct 2024 03:13:32 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc68be86620db6bcaa51e79be7b13c6a946914994c096097e33a6e50a2b64083`  
		Last Modified: Sat, 19 Oct 2024 03:13:34 GMT  
		Size: 44.7 MB (44739798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:f610d3006227721d677010de108d43de007d7467b1dd2c33fff93cb16712105b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef405b4a27a3d22d0323826b6428dcca8b28500af4e688a53dc33f61c761767`

```dockerfile
```

-	Layers:
	-	`sha256:810b3410586fcfd2739871a6c6b395b5be996aa8582525996a0c2cd2135fa3e0`  
		Last Modified: Sat, 19 Oct 2024 03:13:32 GMT  
		Size: 7.8 MB (7770513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de1a2618d6b97cceb6493c0437fcc0eda6bcfb82e808b357d15f84d152c3b29`  
		Last Modified: Sat, 19 Oct 2024 03:13:32 GMT  
		Size: 13.0 KB (13027 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f5cc119e6c91288b6041930c81effe8f5436d7427e335eaf57abae5d28e7e243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182116475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6dabde9d137b2806093f2b378f21def1dad79bed40778529cd0f081f4bcde9`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
MAINTAINER Rob Hoelz
# Thu, 03 Oct 2024 21:11:49 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ARG rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
ENV rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
# ARGS: rakudo_version=2024.09-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 03 Oct 2024 21:11:49 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7694546334bb4c693d08ef9a468c3569b60245a9d50961ffcade2048f23441af`  
		Last Modified: Sat, 19 Oct 2024 09:24:35 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6f351b8738c6bdcc02f7009e4cefbe4f7a789bfc75bfdf98c375986c809a25`  
		Last Modified: Sat, 19 Oct 2024 09:24:36 GMT  
		Size: 44.6 MB (44584382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:90a181e11d2cba5cd7be4002100867cf707d4b763686d29dca9d3f445c48faa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d095eb7c49b5006be9bd7d8aaddfe57b221b40c25e3c8fdf8e34901b368ac136`

```dockerfile
```

-	Layers:
	-	`sha256:8e6af9eeca6352ea4c09df64cc49c1d27443e1ae514d38a93c099b8024dc2452`  
		Last Modified: Sat, 19 Oct 2024 09:24:35 GMT  
		Size: 7.8 MB (7776924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f1736eedae85f7e16be88883cd25bd7ed57d1d27404b2ac10c023f43ae29bb5`  
		Last Modified: Sat, 19 Oct 2024 09:24:35 GMT  
		Size: 13.2 KB (13153 bytes)  
		MIME: application/vnd.in-toto+json
