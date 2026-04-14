## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:ffcecd0daa42e80c3029f7217880738f4672e367994eb783757dd212682f511e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:5e1e118e6a35dbdabc871e830c8c01f1d7d66b22facc826194ec56e73cfe7e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184922881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37db924fe4a2130930163b00a4f5d8d16673d68ff4938ea6eec977ab2e0ebcb2`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:43:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Apr 2026 21:46:44 GMT
MAINTAINER AntonOks
# Mon, 13 Apr 2026 21:46:44 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 13 Apr 2026 21:46:44 GMT
ARG rakudo_version=2026.03-01
# Mon, 13 Apr 2026 21:46:44 GMT
ENV rakudo_version=2026.03-01
# Mon, 13 Apr 2026 22:03:24 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 13 Apr 2026 22:03:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 13 Apr 2026 22:03:24 GMT
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
	-	`sha256:36a228dbe2677612d82ede2d95e3fd39f0eeaaf48d21f520e05acd9678284e07`  
		Last Modified: Mon, 13 Apr 2026 22:03:40 GMT  
		Size: 3.2 KB (3242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f78573956e12245067b2f4a1cf234374971d2b49e255ffd367d72a732a7c496`  
		Last Modified: Mon, 13 Apr 2026 22:03:41 GMT  
		Size: 42.2 MB (42219420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:a24706ca16d7bd9aac21a6bf15356d9b789dad7ea588c309e9009814dac2ed2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d214e5e5102dab9979168e0140ebe0f76732a8f7fd91391914214e97f11ff88`

```dockerfile
```

-	Layers:
	-	`sha256:40fb6bb1ec03c39ed29aa412af130c06e4a62971c674bcc264009bdb8aace792`  
		Last Modified: Mon, 13 Apr 2026 22:03:40 GMT  
		Size: 7.8 MB (7770612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a5aed902d99f75c9361979fede6894f8e119ba2dd3d5b928aa2280eebb8d29`  
		Last Modified: Mon, 13 Apr 2026 22:03:40 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:6e59b113072012af6ab89a8150083cda2cdf9a4e7e990fc1bc309f08a00247dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182509485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e55c610f5f82eddcca8e92f3d1443646f0b633aad85ae7b40b7b5a8556f4e81`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:50:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:53:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Apr 2026 21:51:48 GMT
MAINTAINER AntonOks
# Mon, 13 Apr 2026 21:51:48 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 13 Apr 2026 21:51:48 GMT
ARG rakudo_version=2026.03-01
# Mon, 13 Apr 2026 21:51:48 GMT
ENV rakudo_version=2026.03-01
# Mon, 13 Apr 2026 22:12:28 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 13 Apr 2026 22:12:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 13 Apr 2026 22:12:28 GMT
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
	-	`sha256:d29e6a5f08d5483c8a75ce08d32a0353f4459e4e076c4b2136103d1060959b8a`  
		Last Modified: Mon, 13 Apr 2026 22:12:45 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b3e3bc1e45ec09da0459321b6873dd20351709947976bbd53e7ebcc8102a95`  
		Last Modified: Mon, 13 Apr 2026 22:12:46 GMT  
		Size: 40.2 MB (40225419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3106a4b9e0fc67399c1acaa57821a81b8716c8f2d09116e1da80cfdbb12865d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419598772e5c8659634129aee7a7444fbb0b6a326c6f6a48cf2dd1235dd2be24`

```dockerfile
```

-	Layers:
	-	`sha256:8cb1fce8f5cc1838f24848952a5b4deed994260f446534db023686a40f76d944`  
		Last Modified: Mon, 13 Apr 2026 22:12:45 GMT  
		Size: 7.8 MB (7778287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10c762ea4900845eeb8385a9105369f7ce11d7b9ed78cc2d2820cf647d32e469`  
		Last Modified: Mon, 13 Apr 2026 22:12:45 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json
