## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:00710e26ef40afb4c0f9285867a685dd30daee4bc6c1d745add940d2081bfad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:b33bdb0b6da2a15498a7b63082e6cb713d4263bb9b76427efabfeb015688d1b0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181496405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70631dfc0b2e02d4fd9ba34c0b1b563b8ddfa3ecf039568cba71cb18c9a91ee2`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:03 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Tue, 23 Jul 2024 05:24:03 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:06:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 10:23:41 GMT
MAINTAINER Rob Hoelz
# Tue, 23 Jul 2024 10:23:42 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku
# Tue, 23 Jul 2024 10:23:42 GMT
ARG rakudo_version=2024.05-01
# Tue, 23 Jul 2024 10:23:42 GMT
ENV rakudo_version=2024.05-01
# Tue, 23 Jul 2024 10:43:46 GMT
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 10:43:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 23 Jul 2024 10:43:46 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d643a5fa823cd013a108b2076f4d2edf1b2a921f863b533e83ea5ed8d09bd4`  
		Last Modified: Tue, 23 Jul 2024 06:13:33 GMT  
		Size: 64.1 MB (64143199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea35765819a2e5efae4c69e77e0fa72494cb552dc231c1c85a7e8d114ae3aeff`  
		Last Modified: Tue, 23 Jul 2024 10:43:59 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76889c6fc3333b91d0766bcfacc49e0690df49f98e39cf52ec712d99b0bda0c0`  
		Last Modified: Tue, 23 Jul 2024 10:44:07 GMT  
		Size: 43.7 MB (43745069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:affee09deb348e5bd58ebdbb3aab3a2d567e3d3fa765461f9f7b0c792fa2596e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180794114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b3ca8671cb1e451bb6c56666b005ee950e7900632f002bb5bf20550290ca2ac`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:42 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Tue, 13 Aug 2024 00:39:43 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:02:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 04:12:17 GMT
MAINTAINER Rob Hoelz
# Tue, 13 Aug 2024 04:12:18 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku
# Tue, 13 Aug 2024 04:12:18 GMT
ARG rakudo_version=2024.05-01
# Tue, 13 Aug 2024 04:12:18 GMT
ENV rakudo_version=2024.05-01
# Tue, 13 Aug 2024 04:30:50 GMT
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Aug 2024 04:30:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 13 Aug 2024 04:30:51 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1593650c75729f64218ae272e8ffff9da7bbba9599bd1815877da99a2651fd9b`  
		Last Modified: Tue, 13 Aug 2024 01:09:17 GMT  
		Size: 23.6 MB (23592427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275677961327bd0cf394699228e29d7caf27f171c627899a20ebc9eeb550e209`  
		Last Modified: Tue, 13 Aug 2024 01:09:34 GMT  
		Size: 64.0 MB (63994880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617ddac7c3aa7acce3c88c46b906b300930fdf3d5777f517736840890e0558e8`  
		Last Modified: Tue, 13 Aug 2024 04:31:04 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866ee59cf13594b65df391220c650ac996bfaf221888516a69119fabe7c25f22`  
		Last Modified: Tue, 13 Aug 2024 04:31:12 GMT  
		Size: 43.6 MB (43614954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
