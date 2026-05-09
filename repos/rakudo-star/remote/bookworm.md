## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:811bf42f560bf09a28500665556724e5f6cafdbd779295e939346d718b34c8c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:50c806a10afa0a7d5ef153aad5c8eb1d1bb3c28fea7b630e65e52c1edf869bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179174934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fe25ed908da98ea95700a9236bee422b35ea1afc098ee0d7c4b4b0cad0b6ac`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:19:52 GMT
MAINTAINER Rob Hoelz
# Fri, 08 May 2026 21:19:52 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 08 May 2026 21:19:52 GMT
ARG rakudo_version=2026.03-01
# Fri, 08 May 2026 21:19:52 GMT
ENV rakudo_version=2026.03-01
# Fri, 08 May 2026 21:36:08 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 21:36:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 08 May 2026 21:36:08 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0869e5c4dac5849d3555a38db741288a16528478145da8dcb95b8dba2464d55d`  
		Last Modified: Fri, 08 May 2026 20:26:25 GMT  
		Size: 64.4 MB (64397036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f954b518f588312517f28e20327abec13582880777509e3a82d6b0bc2f4d94`  
		Last Modified: Fri, 08 May 2026 21:36:22 GMT  
		Size: 3.2 KB (3244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915f308a59b3d70acbec66c84c3bca1b2b0cd345dceebe5ea5018cc9daf3cbb2`  
		Last Modified: Fri, 08 May 2026 21:36:24 GMT  
		Size: 42.2 MB (42243798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:e0fffc5c01c7a279d7d56446ec73bd4d891c1e3e65359014829b48f40ebe7a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a8ea5c07249ff83cb25b20fb419783a3c21b07f81b2492ebd8adcc0097b61d`

```dockerfile
```

-	Layers:
	-	`sha256:db12d36070da5315141ac60c902c7da121e18dda05bd8be7abb962196060d3f0`  
		Last Modified: Fri, 08 May 2026 21:36:23 GMT  
		Size: 8.0 MB (7968447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fbb171494a541a1221e5a85bfe47b5de90dea011ac7aa0da05ddb61fd59abc0`  
		Last Modified: Fri, 08 May 2026 21:36:22 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:8126b1128cff1d8f9abfd34f968b113d65a50a84f8671f37af4a7d5cbfd2b881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176718072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8560ac6c4092839aad5173a1ccc5031877df19bb41841d55b6813f42f069a610`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:31:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:20:32 GMT
MAINTAINER Rob Hoelz
# Fri, 08 May 2026 21:20:32 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 08 May 2026 21:20:32 GMT
ARG rakudo_version=2026.03-01
# Fri, 08 May 2026 21:20:32 GMT
ENV rakudo_version=2026.03-01
# Fri, 08 May 2026 21:40:22 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 21:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 08 May 2026 21:40:22 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5c3bf1fab727b805a2f735f33789c10938680bdeb2f8922a44aa2738df91f`  
		Last Modified: Fri, 08 May 2026 20:32:11 GMT  
		Size: 64.5 MB (64479741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4b96e5b48c46c2cf2dc3cca656850c57ea041540d0b02915ab752c4a4869b4`  
		Last Modified: Fri, 08 May 2026 21:40:37 GMT  
		Size: 3.2 KB (3243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b725c68988ab7b550c2e796c0f8c258d168d612dd57d6f23c3c299eaa866`  
		Last Modified: Fri, 08 May 2026 21:40:39 GMT  
		Size: 40.3 MB (40252581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:18d0c25748ccab282fdeeaa68cfccb03d753e36accb61b32fe5c2ce9b5be8b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70eab49d26402bffe796fdc6a77bf3b8956a234801cafdc3a6a77523e2fd7d65`

```dockerfile
```

-	Layers:
	-	`sha256:a028daf4443ff62384fdcb0f47bea9b2e56b84bb401a8fc0e4b235460549f894`  
		Last Modified: Fri, 08 May 2026 21:40:38 GMT  
		Size: 8.0 MB (7974840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36fc0888faf084e8c38943b57273357ca085b8f272c97699c2e464528b11c9b7`  
		Last Modified: Fri, 08 May 2026 21:40:37 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json
