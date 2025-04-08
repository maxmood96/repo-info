## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:944b0a29f1a3df2e2b3e79f2bb13dfdfb3a2b5b7e99b6987d316594946f07aa9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:0e88efedb05bcc7aaabacf6394a17660e11367c0767a64f3c1db2cc61d7197bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.6 MB (178637819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b2930ec1013188ebb6c13e4e2c510b8be77b0d31df46cf374185d7707be51b`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
MAINTAINER Rob Hoelz
# Thu, 06 Mar 2025 03:06:23 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ARG rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
ENV rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
# ARGS: rakudo_version=2025.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 06 Mar 2025 03:06:23 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1b5af933d2dfc3d0dd509d6e20534825e4a537f7b006a6cb5b8e5a1f20905`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 24.0 MB (24011090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb98adba0eb44a2e4facf9ca3626a4a66feedd0dd56d159cca90a35205744e7`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 64.4 MB (64396468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658453baa222297e44ad439ac8d327171f4fbe033497ffa8e0e660a6107d16fd`  
		Last Modified: Tue, 08 Apr 2025 03:35:06 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fde98860aa91372d1565b08fcb781798ea873a30d648bc9df749f82f4808cf3`  
		Last Modified: Tue, 08 Apr 2025 03:35:07 GMT  
		Size: 41.7 MB (41736481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:962d5df0b96909a741c47237f15064000303987883fb0c8db1087eedddf2f169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7769717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6339d9bfe76e514acfd2739109f46f2284aa4068ef043e66fa9e1e5ac97717`

```dockerfile
```

-	Layers:
	-	`sha256:8431dae4abc467001570a94ab98929de075ebec526cab7d64358937269e7ddf7`  
		Last Modified: Tue, 08 Apr 2025 03:35:07 GMT  
		Size: 7.8 MB (7756681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e30b9d461abb953c63c9f4fe3161b222b4b5d80375cb28ffbad512f440234d2`  
		Last Modified: Tue, 08 Apr 2025 03:35:06 GMT  
		Size: 13.0 KB (13036 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:56424347cbdb58d545dd024aa74e36812bb5cd504429d962fc9cfa18a3710121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176142842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cd4355d4bfa12a5dbcd64e7aed3fb84e957e29101a8e98c45de8d713c03ca0`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
MAINTAINER Rob Hoelz
# Thu, 06 Mar 2025 03:06:23 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ARG rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
ENV rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
# ARGS: rakudo_version=2025.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 06 Mar 2025 03:06:23 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378a6c11dea5043896b9425853a850807e5845b0018fe01ddee56c16245fc3c`  
		Last Modified: Tue, 18 Mar 2025 05:00:37 GMT  
		Size: 23.5 MB (23544349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d15be2fea6dcd21c20cadae2601a118c08a938168718b2612ad6aca91f74a`  
		Last Modified: Tue, 18 Mar 2025 13:13:07 GMT  
		Size: 64.4 MB (64355791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47adee9c6c100b72968c4214c8212a437fd4133a55e025becbfcf80201321f3`  
		Last Modified: Tue, 18 Mar 2025 14:35:10 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4f6ef112049b8b6a8d542134e78cbde095354fa59ffe018f391a219f755315`  
		Last Modified: Tue, 18 Mar 2025 14:35:12 GMT  
		Size: 39.9 MB (39934610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3a0374e87a7fa8842cf91c55fafac0a8399735033a634dc04745e4105d694e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720cb8db8cc384888c52a6866e0c3f8b701aaa5695e86d06a748bdf50e972c09`

```dockerfile
```

-	Layers:
	-	`sha256:e598025b798fa61da776de6416222a57b31bec0d9f5b7c68e594e2e955ee30b9`  
		Last Modified: Tue, 18 Mar 2025 14:35:11 GMT  
		Size: 7.8 MB (7761702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:034ca069e9f372350214d5597a510d089b132965ace7419cb1f6415ce17cbec8`  
		Last Modified: Tue, 18 Mar 2025 14:35:10 GMT  
		Size: 13.1 KB (13143 bytes)  
		MIME: application/vnd.in-toto+json
