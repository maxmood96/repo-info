## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:8d0b70737fb8add6abf7e4ac002a3198e58dc787ada3871a2ab4dcc8d20cd5c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:960713616609e64506bf9b35c394f5409dced16cc7965d7f7dc03930f360fd57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185416555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c831535d9f3ca6839a7bdea0e8847bea222d0580d714d8a65e32295bc9481db8`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
MAINTAINER AntonOks
# Thu, 25 Sep 2025 18:16:25 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ARG rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
ENV rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 25 Sep 2025 18:16:25 GMT
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
	-	`sha256:405a2df5c6591a4d7296a608188ebbc0ef07f786b9a850efae7f647785d1dccf`  
		Last Modified: Tue, 21 Oct 2025 08:25:36 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb6e1d7b2d12ac2139a6bc375338d956fd85774a291128c1847c00ec2556210`  
		Last Modified: Tue, 21 Oct 2025 08:25:38 GMT  
		Size: 42.7 MB (42727944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:bcfe1a97ed5166dd1f6491ee2f968568f4c00e9daf36c6df0a21ce8f37a40664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5aab141df1ff7e92a4ece91a7c4d9e106d905b76aa15ec0bf9695311effaf85`

```dockerfile
```

-	Layers:
	-	`sha256:0d449a6138569ed209da47475f197adb6836ef113dea1dc95e8c31ed46fa26c6`  
		Last Modified: Tue, 21 Oct 2025 10:33:29 GMT  
		Size: 7.8 MB (7769455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54d27c0b2bd995f61454d87d0ddee41d2b4f14956693137adb59757ed4ecc15d`  
		Last Modified: Tue, 21 Oct 2025 10:33:30 GMT  
		Size: 13.1 KB (13050 bytes)  
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
