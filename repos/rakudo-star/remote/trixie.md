## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:d0ded55394c33c5c981eab3d316f9125553fee4a0f7e8744e82b7f2d5e78b399
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:a5db8c5546a9bf772884c217d6f58ff2655dd7dddcce853bd0afc089024a0c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185001475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e235f8172f1db249661eb65b983ee7b804f0a605d3bf83884691bb61ec3dfdff`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:17:38 GMT
MAINTAINER AntonOks
# Wed, 20 May 2026 01:17:38 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:17:38 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:17:38 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:34:12 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:34:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:34:12 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7504cd2818ce40ac76c17886a03dff25ef0aa06ff6125bf0f0c7302cdc6471`  
		Last Modified: Tue, 19 May 2026 23:23:34 GMT  
		Size: 25.6 MB (25633915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53089dca50590292ecc77bf803152a5799650e734717e4b706cb812a02073ba`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 67.8 MB (67777732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80607773a759902698ec0cf0e10e9da74c8fec8600e897dd0d797640a8d43289`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a545e4e9cef0f98ea91a02d9353066d60795f5c7148a00c456565202f9d39f1`  
		Last Modified: Wed, 20 May 2026 01:34:28 GMT  
		Size: 42.3 MB (42275965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b8d9720544b8579958f2d506853810431859b3015ba612506e4fdd2c98bbbdad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be136192959832f739f7038ee624e566f1e5fc55145602eff71e677a0bad0e2f`

```dockerfile
```

-	Layers:
	-	`sha256:45681b8ec93bdda21c74edc2fcf9abaea31dd877f07579176d589bf86d203bd3`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 7.8 MB (7770816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4742c2a063641ea363ab07e0d07d0471a7144c88f8de15d64633f7b638b8638e`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:ccd3cde3b3b0ab86674ce234601a09f0497ee19cd2db420af00a4822c39fa0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182575813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4c935a370b4c3e919d83b00af34b9f1b21ebb20c32afc63c545279dc9655ce`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:17:57 GMT
MAINTAINER AntonOks
# Wed, 20 May 2026 01:17:57 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:17:57 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:17:57 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:37:35 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:37:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:37:35 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28313c8eaf165ac06f26bda4877768677cf5e44e5c61ec169a81b436b2e985b`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 25.0 MB (25025606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39feea71264a587b284d92fded7754becc4682529629dd95c8bc3dd25a948a27`  
		Last Modified: Wed, 20 May 2026 00:27:52 GMT  
		Size: 67.6 MB (67592849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3069e913afb301820f3287b1aaeb6333296bfb8d622c88f851dcf6c38ed9480`  
		Last Modified: Wed, 20 May 2026 01:37:50 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0266231e82e884294c5a8205e13d1880ff188f73f6167cadd931cbd3e0523b`  
		Last Modified: Wed, 20 May 2026 01:37:52 GMT  
		Size: 40.3 MB (40281898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:6466072a9135ac916eac9efb849ed2427893887f31b3a5424447e7e421100e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3537f7f6df5ce7c38ecf4d28c44f1442099095cf51a65fa2dd6c7b3eab4c7d`

```dockerfile
```

-	Layers:
	-	`sha256:ac7e39d6c3ac29c1b181bd3b0de881a3901d99c74c9ddcd10c9fcb6b25f5ab65`  
		Last Modified: Wed, 20 May 2026 01:37:51 GMT  
		Size: 7.8 MB (7777854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcbb83e93fe5d19fb6c866ed79b54e169dbc586a17bdefaf9386062d5b5204a1`  
		Last Modified: Wed, 20 May 2026 01:37:50 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json
