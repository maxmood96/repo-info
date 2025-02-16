## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:33189b08c28f938f828ccd80bf18c2ca072ad39df3ec215e0e46eba40c31c717
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:23aba77146bc8518c7b882a04d72749bd661b2e15f8e7bc64ec9b7143f25c00b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45643641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f165d0f253935f04b5df1a8895c9ba661d597d9fcd432f01798f090c328da2d`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Dec 2024 03:29:03 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86564e6fe6ca585100328a41da0634754a68eb70c2bb2651af6fbf3c1e476c53`  
		Last Modified: Sat, 15 Feb 2025 05:02:07 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb98552c75fa02b9c86ca7980afddf4c289744ec8e900b52c14d978ef1ecc0a`  
		Last Modified: Sat, 15 Feb 2025 05:02:09 GMT  
		Size: 42.0 MB (42000448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:585611c8c5765b7e6a84c3530fdbd447823b8307477459a4265d8d7d19e8859b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 KB (132467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0ae7369b89ac49eb5fa521d9ed93363fed9a60a74e56a6a1b67fca59e1b055`

```dockerfile
```

-	Layers:
	-	`sha256:55793d27d7b434e2fe29bc1b8e7098ca4ee42b21e9ae9bcddf3f810a1fe4d8a5`  
		Last Modified: Fri, 14 Feb 2025 23:33:15 GMT  
		Size: 120.7 KB (120726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afafa4aabe01f776e18ecc64c0f92be2b5fb24a745a2279314dae3c4d9b4df56`  
		Last Modified: Fri, 14 Feb 2025 23:33:16 GMT  
		Size: 11.7 KB (11741 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:eb621de4a27241ce8d2a963f8920b73a96a24eb0d079d42ce09bb417d918cc29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45823142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34d9200680157653dddba47cb58cf52ea537e8cd2cd32a6ca2285e6cf879ad6`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Dec 2024 03:29:03 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10efd9326b07c9d4d79c7e7c20dcac84b1d972ce22cf1ced33b07e577fe0541`  
		Last Modified: Sun, 16 Feb 2025 12:32:29 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fea430330fa04b042f359fbbc134928c01c73be3d903b79064353de58f8351`  
		Last Modified: Sun, 16 Feb 2025 12:32:32 GMT  
		Size: 41.8 MB (41829166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:72e1c8596f4be9c41ecddfd4642138a1afbc70b509a88bd4c8dffc99b873c267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9dce6fc2372be759cbba73cd3b03630e107d707a1d42000e7692497f294db69`

```dockerfile
```

-	Layers:
	-	`sha256:c9729986a8a071d10777b5eb9f4023d64a91fe5b08ac06aa8ce871b3188ed218`  
		Last Modified: Sat, 15 Feb 2025 08:33:17 GMT  
		Size: 120.8 KB (120758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d51f204534c6591f11fe31ed44dd8c672bf50627d764ef2351e6acea7e06a59`  
		Last Modified: Sat, 15 Feb 2025 08:33:17 GMT  
		Size: 11.8 KB (11836 bytes)  
		MIME: application/vnd.in-toto+json
