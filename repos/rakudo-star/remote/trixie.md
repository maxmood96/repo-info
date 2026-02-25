## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:4fad5613619d935065b5e98acf6872ddcf921c514421489170211e17487eae9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:e6a4a31f04a4a30ca26e525cb28f56ceb95ad350103ebc5f7316c2ede13a858c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183726082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb90e860d4128bcb9cc96754a5cac41376723f14af587e896cdfa9bc365ce142`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:41:31 GMT
MAINTAINER AntonOks
# Tue, 24 Feb 2026 20:41:31 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 24 Feb 2026 20:41:31 GMT
ARG rakudo_version=2026.01-01
# Tue, 24 Feb 2026 20:41:31 GMT
ENV rakudo_version=2026.01-01
# Tue, 24 Feb 2026 20:56:07 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 20:56:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 24 Feb 2026 20:56:07 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed881fbf1b07b42dd470cd5b56a8feb684d60879c6f8028a9e7a8715e0e72361`  
		Last Modified: Tue, 24 Feb 2026 19:20:17 GMT  
		Size: 25.6 MB (25614562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da421ddeb655bdfb3960e490b39373b0d1351e3eaba61d01978107920638392`  
		Last Modified: Tue, 24 Feb 2026 20:04:27 GMT  
		Size: 67.8 MB (67778971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a5dd9f1ea8eeda6f9bbd82467377582d49a9654af4f000c9452f6851504099`  
		Last Modified: Tue, 24 Feb 2026 20:56:21 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e72ac401f82f8ebc99b9237acc7131b59339b389a974030d14060fb949792c1`  
		Last Modified: Tue, 24 Feb 2026 20:56:22 GMT  
		Size: 41.0 MB (41036188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3f6fdb060d4c3279fe2fb00f9bee8e0d8b35f590eb2d0322f085cbf42a3f9c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7565c637d83d883d4bb069cc61ffebb979a8e4972b55109a648a5f9dce4547`

```dockerfile
```

-	Layers:
	-	`sha256:7b586f98a4197e1ff9985ff0e03eccc62abd4edd9bc804f5e6d6550351af7d03`  
		Last Modified: Tue, 24 Feb 2026 20:56:21 GMT  
		Size: 7.8 MB (7770538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecbcb2a4ea49e947417c5725eec704974988c54c550fef84fbc075ea561ee4cf`  
		Last Modified: Tue, 24 Feb 2026 20:56:21 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f494333ff3fb7184cdabd201443641a887715127d9e2ced89e33966600962b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181326480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec7c7c672d5408e03382427e842bef696f19c2131d248f65564b0794a76421e`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:33:10 GMT
MAINTAINER AntonOks
# Tue, 24 Feb 2026 21:33:10 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 24 Feb 2026 21:33:10 GMT
ARG rakudo_version=2026.01-01
# Tue, 24 Feb 2026 21:33:10 GMT
ENV rakudo_version=2026.01-01
# Tue, 24 Feb 2026 21:51:40 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 21:51:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 24 Feb 2026 21:51:40 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da832d1713c4ed161275cd40c4161680fbdd97c6faf23e71654d26bb2e58d6`  
		Last Modified: Tue, 24 Feb 2026 19:25:09 GMT  
		Size: 25.0 MB (25023493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c46eec5989abc098640d80ee9b97658d4487864f3268219dadc63c0a047866`  
		Last Modified: Tue, 24 Feb 2026 20:15:09 GMT  
		Size: 67.6 MB (67585551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d1ed4489cd9c9fa6ceafe2da92c08d884dd1f14669679f97a2489e8a94e640`  
		Last Modified: Tue, 24 Feb 2026 21:51:55 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695b3a266e3b8d592d861209abb74e8feb199943a86ae0d3c4a2d2ab3accf3ad`  
		Last Modified: Tue, 24 Feb 2026 21:51:56 GMT  
		Size: 39.1 MB (39062028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:f91f79b0317256dc72579c19319156ccccc18db64923451a147bcc459f3e8af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63547eb772f2cee140241f4029e61b630ae431b3dc0ee951b17a6b0db497c16`

```dockerfile
```

-	Layers:
	-	`sha256:84f660932f2c8c79a337000de11d5e923abb10813dbf2ad0a0d76ca684c31ab7`  
		Last Modified: Tue, 24 Feb 2026 21:51:56 GMT  
		Size: 7.8 MB (7778213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a08673963cb439ea169f0274c90b2d35dc7d0b6d028dd76007417eb1189c2906`  
		Last Modified: Tue, 24 Feb 2026 21:51:55 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json
