## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:a544b2f161b37ae2783f967ddd990522d45e73b75aabe83b850fcb3ad254accf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:e7b45f3cd7ab812ae3637c17232519bb39dee4ed8f80eb2aec2f44a371d8f70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185426245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e147f329e22e06183c45cb4d918a05979096277b0571eb09d5db0d5ac8771bc`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:51:28 GMT
MAINTAINER AntonOks
# Tue, 09 Dec 2025 00:51:28 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 09 Dec 2025 00:51:28 GMT
ARG rakudo_version=2025.10-01
# Tue, 09 Dec 2025 00:51:28 GMT
ENV rakudo_version=2025.10-01
# Tue, 09 Dec 2025 01:07:15 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 01:07:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 09 Dec 2025 01:07:15 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22766554d6bfa95c7325b00ee002f2705a7b8605908c3eb43dbe729c412422c`  
		Last Modified: Mon, 08 Dec 2025 23:07:43 GMT  
		Size: 25.6 MB (25613863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f2d358b447d091790c5ef0943550bbcf57bac46c4b8bfcfc3e6dacf4cb7969`  
		Last Modified: Tue, 09 Dec 2025 00:06:46 GMT  
		Size: 67.8 MB (67778647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1e2fa53da7fb32f2efff992e980c1df2af29150be96ca181e72e7b6914493d`  
		Last Modified: Tue, 09 Dec 2025 01:07:37 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78a86b01210135bc5548f563542a13ad1fe8a73b4d29a59ef46a77f09fa465f`  
		Last Modified: Tue, 09 Dec 2025 01:07:44 GMT  
		Size: 42.7 MB (42740978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:1bf6859dc52a3ba7f34cb8b9303f9990462845609c1889c223798eb4b81237cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0ac35cb7daefab1768a4e3cfe41587e4d84361689533b0e6d59e0e7828d1fa`

```dockerfile
```

-	Layers:
	-	`sha256:16978ee8723517d7dcc22296d0704b77f3d299d615b98360b69a797eaa06dc13`  
		Last Modified: Tue, 09 Dec 2025 02:33:55 GMT  
		Size: 7.8 MB (7769499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922a732d1a0bfcefb16fcafe9cb57ca1673dd2b74e2ef38ddb9b96ad514dab87`  
		Last Modified: Tue, 09 Dec 2025 02:33:56 GMT  
		Size: 13.0 KB (12991 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:e3b3fef13d1f29b09acf0c555dea91b6e0699d443cd312030926ae3e46b8ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183056558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63fc0b355649f63ed18d485a3fe60b488f4f1bd57c6ec0e40f846b6579400d80`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:22:13 GMT
MAINTAINER AntonOks
# Tue, 09 Dec 2025 01:22:13 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 09 Dec 2025 01:22:13 GMT
ARG rakudo_version=2025.10-01
# Tue, 09 Dec 2025 01:22:13 GMT
ENV rakudo_version=2025.10-01
# Tue, 09 Dec 2025 01:42:16 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 01:42:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 09 Dec 2025 01:42:16 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097d536d3c26abbb49039062f8d8e471b0c97bdfcc2ecfcfcf56545161524fb`  
		Last Modified: Mon, 08 Dec 2025 23:11:17 GMT  
		Size: 25.0 MB (25020941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb13e64d383cee6a152ac57ad29b9b1116554b1c9daab0e94464d674f3804db`  
		Last Modified: Tue, 09 Dec 2025 00:12:25 GMT  
		Size: 67.6 MB (67585014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b70bb4683a0e3c06330cd1201aef1a2871d8cdcfbc68246766951a3cb9ab93c`  
		Last Modified: Tue, 09 Dec 2025 01:42:44 GMT  
		Size: 3.2 KB (3236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c755f7599d208bcabfaefa4aa0d9af367e28a569e38fb23d1423699abd8982`  
		Last Modified: Tue, 09 Dec 2025 01:42:47 GMT  
		Size: 40.8 MB (40797141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:79a53978fd34e34bbe25a0a225125cd21f655b393511c5101ae8303619f0db3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe5055dc7329e70b90a1d8d528df86fbf0f5009a1b11a304e7270348ea5cf50`

```dockerfile
```

-	Layers:
	-	`sha256:e2f0e9561ba045229e9252dedfcd6ec04acee7311af65e7d35ab8552f8ee1b75`  
		Last Modified: Tue, 09 Dec 2025 05:33:37 GMT  
		Size: 7.8 MB (7777174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e98075ab4ace7c2f9d9ce885d2fdc0801b0bd95eb3d37b4ef053f0fb947a8e1`  
		Last Modified: Tue, 09 Dec 2025 05:33:38 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json
