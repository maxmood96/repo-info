## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:146bbcc1beb84f509d169d2777ed873c519364b542873553d1cea96a009a90c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:b86610468fc307c09289dee6e0e42b1c1a0757e394d12dd6809429a960bd3cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183674684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427b75a5d505332a08c4dc8b60c5bfdeada105e02b930d9c39472103caaa44ad`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:25:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 03 Apr 2026 16:48:02 GMT
MAINTAINER AntonOks
# Fri, 03 Apr 2026 16:48:02 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 03 Apr 2026 16:48:02 GMT
ARG rakudo_version=2026.02-01
# Fri, 03 Apr 2026 16:48:02 GMT
ENV rakudo_version=2026.02-01
# Fri, 03 Apr 2026 17:02:30 GMT
# ARGS: rakudo_version=2026.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 03 Apr 2026 17:02:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 03 Apr 2026 17:02:30 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b012eb15dff0bce418c03ec940325aee6aa4300d771c325728855697e620c63a`  
		Last Modified: Mon, 16 Mar 2026 22:38:25 GMT  
		Size: 25.6 MB (25621715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3a0e7d77f0c84203cab438fcf345647c8121bbd80506a3c692f8608a14c4f4`  
		Last Modified: Mon, 16 Mar 2026 23:25:57 GMT  
		Size: 67.8 MB (67780758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057dd72c0508b5b843429b514063317ec0b8a34fab30981bfd832f1ab2dc6181`  
		Last Modified: Fri, 03 Apr 2026 17:02:45 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b94f60fda7cf700b36b1853419cfcbee307e31f6fc498d664e144baefe2658`  
		Last Modified: Fri, 03 Apr 2026 17:02:46 GMT  
		Size: 41.0 MB (40971441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:033421dbd2b87777bdde49c7349381cf9bb9fb3f4f139bcc2dc0807e151b6fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980f56dad88ff63bf2e02fd15a5782f228bad7bfae6feb532b1bf47f9706498d`

```dockerfile
```

-	Layers:
	-	`sha256:eade7d07912a683a27aa9d6d7d8beafe0ba9520f3677fff4d7de425983c6600a`  
		Last Modified: Fri, 03 Apr 2026 17:02:46 GMT  
		Size: 7.8 MB (7770304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea1ec642db9331e451ee1b64782b127d8423a8b68241f990bca189ffd7ea000`  
		Last Modified: Fri, 03 Apr 2026 17:02:45 GMT  
		Size: 12.7 KB (12685 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:d5c6f9514810d4916a72a56e49d69bba768d320d64ab86c56b771911808ae586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181282614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269d0a7b7269d31d277589719549d4fd39de05bca1e7ed5788fc28186d875dba`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:30:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 03 Apr 2026 16:48:42 GMT
MAINTAINER AntonOks
# Fri, 03 Apr 2026 16:48:42 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 03 Apr 2026 16:48:42 GMT
ARG rakudo_version=2026.02-01
# Fri, 03 Apr 2026 16:48:42 GMT
ENV rakudo_version=2026.02-01
# Fri, 03 Apr 2026 17:08:19 GMT
# ARGS: rakudo_version=2026.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 03 Apr 2026 17:08:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 03 Apr 2026 17:08:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6778b62bd97b31237948877e89abc29ad2b2c003f3b965027457c8c90d4f44e0`  
		Last Modified: Mon, 16 Mar 2026 22:40:45 GMT  
		Size: 25.0 MB (25023728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16813bdedcf0a1acbd78336c5bed6fbfaee2674574408140ba7e896cd49cb95`  
		Last Modified: Mon, 16 Mar 2026 23:31:00 GMT  
		Size: 67.6 MB (67584568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1131783f546848fafb465101404a0fd847156698c68062ed85837e8acb8574`  
		Last Modified: Fri, 03 Apr 2026 17:08:35 GMT  
		Size: 3.2 KB (3245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c93828b0f63386d7951699cac0832c05942eb6cbd094f16addf2500c1a485d0`  
		Last Modified: Fri, 03 Apr 2026 17:08:37 GMT  
		Size: 39.0 MB (39006120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:cd9cd59d881f3b7abf9f5a8d7e6e4429673c2b0ddd202851b8de32e2357bd6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd775206cac4f8ca587e23038a30f8645127ff4ea6d0af1b4c633ddcc20105f`

```dockerfile
```

-	Layers:
	-	`sha256:7f2fbe656fc8d72c70f64b12aadff23310fe61889b435af7fd672f9f2d9779ae`  
		Last Modified: Fri, 03 Apr 2026 17:08:36 GMT  
		Size: 7.8 MB (7777967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70be210d8025c56fd62595311f6219d71c6ce24a6119d15e12c8b498c481ec4`  
		Last Modified: Fri, 03 Apr 2026 17:08:35 GMT  
		Size: 12.8 KB (12779 bytes)  
		MIME: application/vnd.in-toto+json
