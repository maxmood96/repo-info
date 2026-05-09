## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:8fa52e07957af55cd0dc7df314bdc24bf1dcb5a66045554ae7821c8684c01aae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:becc95dff92662eab5470178f38f4e68c66ad33985c2867797af5f976c084e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (184976515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752c06859dabaaef9d2dd62ea7b20f2a21b61f0d61e59f97addfac3333617cd1`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:26:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:19:36 GMT
MAINTAINER AntonOks
# Fri, 08 May 2026 21:19:36 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 08 May 2026 21:19:36 GMT
ARG rakudo_version=2026.03-01
# Fri, 08 May 2026 21:19:36 GMT
ENV rakudo_version=2026.03-01
# Fri, 08 May 2026 21:35:27 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 21:35:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 08 May 2026 21:35:27 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf6c0a95e34418907d5abfe604d08c5cc6bf9d689943856fcd842eb2be82c6c`  
		Last Modified: Fri, 08 May 2026 19:40:57 GMT  
		Size: 25.6 MB (25623106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a92b93bf7181c9d6b4525236a1a2fec85dc591d4deee481e828e707853f42c`  
		Last Modified: Fri, 08 May 2026 20:27:02 GMT  
		Size: 67.8 MB (67789206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46240e81cf02e288be339f64f94dcf8bf7ddc00ea0b0624bc56db109113d2e6`  
		Last Modified: Fri, 08 May 2026 21:35:41 GMT  
		Size: 3.2 KB (3243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d69b8e298bfac72d48946b3adf1fd8c3ba2d9aaf42c301c0e18e9bdc4c6a256`  
		Last Modified: Fri, 08 May 2026 21:35:42 GMT  
		Size: 42.3 MB (42258640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:5bd74c7bb6d99ee3e42787c4624b0a90afe8e158249d4840cf2a9a956a87e3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451fdc2f83a32e2f764bfaf3305a84f55103c914e5d59960fafa2431a4d8b430`

```dockerfile
```

-	Layers:
	-	`sha256:56cd30df74aabaf94c2aa85e77474cf89457156fe9bfc6f8f2fba50a58e015e9`  
		Last Modified: Fri, 08 May 2026 21:35:41 GMT  
		Size: 7.8 MB (7770666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a30ef50d81c9784fb53290e22ce97f39df612fec9a1c00e38b6289d842d9587a`  
		Last Modified: Fri, 08 May 2026 21:35:41 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:dee7fb4ecab2e1d9334fe442680c58607dc92ea0b0a54a1386fcf66cd98b86a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182557585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3def38ef5c552e78674daa05109c10bc7b4b9f77b6fe6a7732c3010cd65c9c7`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:19:38 GMT
MAINTAINER AntonOks
# Fri, 08 May 2026 21:19:38 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 08 May 2026 21:19:38 GMT
ARG rakudo_version=2026.03-01
# Fri, 08 May 2026 21:19:38 GMT
ENV rakudo_version=2026.03-01
# Fri, 08 May 2026 21:39:53 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 21:39:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 08 May 2026 21:39:53 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6968d8edb06bcdaf22846e8626a2500d70d68bae3413bca896fefe955e2a6ef0`  
		Last Modified: Fri, 08 May 2026 19:42:46 GMT  
		Size: 25.0 MB (25023476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc880ef5fbb726989fb57630c05c39cfe57a36a9f03c5b86a2d51c9c86ed66f2`  
		Last Modified: Fri, 08 May 2026 20:32:42 GMT  
		Size: 67.6 MB (67592055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d944f36e8d4737c299105fd017ba91ba09672d464f7eef4eb9cba7ba964b84a5`  
		Last Modified: Fri, 08 May 2026 21:40:08 GMT  
		Size: 3.2 KB (3243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6eeede9eacb1facb6d0661f8c30fba4020b7f3418c486bd58018b93f84c009`  
		Last Modified: Fri, 08 May 2026 21:40:10 GMT  
		Size: 40.3 MB (40269366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:32ccb461388015d98105e4686b54f68f3f43dd239085cf48fdbbf5f3c98cdd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c058b821f308233406eb7a0f952f31df392d7c5d0afcbd300853d1269c64ac9b`

```dockerfile
```

-	Layers:
	-	`sha256:c64fb2df571d20d6f12cfdf8883932c5bd26aedafab5008a5b3ff5a1ec8f521f`  
		Last Modified: Fri, 08 May 2026 21:40:09 GMT  
		Size: 7.8 MB (7778341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de358beba4bf91db65e0d7dcb26181b827fe6146187d6fae4bedb81eb141b70`  
		Last Modified: Fri, 08 May 2026 21:40:08 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json
