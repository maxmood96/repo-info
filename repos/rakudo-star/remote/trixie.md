## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:588eeb71c889832b0753c41f5488d2cc4dfed9eb3097b6044fa4fe4b9780ebc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:c327678130dc4cc21016b4797e7db4acc8eb0006237579dba5261f22be1cfdc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182454535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa5465b728c615b686b632c67aa901e486ee8f5dd58d3b0366cb362f072128c`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 28 Dec 2025 05:51:01 GMT
MAINTAINER AntonOks
# Sun, 28 Dec 2025 05:51:01 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Sun, 28 Dec 2025 05:51:01 GMT
ARG rakudo_version=2025.12-01
# Sun, 28 Dec 2025 05:51:01 GMT
ENV rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:04:58 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 28 Dec 2025 06:04:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Sun, 28 Dec 2025 06:04:58 GMT
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
	-	`sha256:95217a361e37efeac6ad41b978aeb38f999c166ef3a0bbb6b0ab96ec7039350e`  
		Last Modified: Sun, 28 Dec 2025 06:05:20 GMT  
		Size: 3.2 KB (3244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34137921a2e46afb191b17ceaf28bb332e63dfd262869b8a6df6095e8b07d88`  
		Last Modified: Sun, 28 Dec 2025 06:05:25 GMT  
		Size: 39.8 MB (39769261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:7ff558f7a81805375ec83bcbaec2db641d9102d0d2ddd22403c44878f3c72fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c9158dd4c950625b697fda25a60fa8fcc74176e78d462a30e65fa1aa0ddc17`

```dockerfile
```

-	Layers:
	-	`sha256:0991552a10ff7383368da1ed1ac2635b9bb9353bf4f84dc105a5df0fe63a6dd3`  
		Last Modified: Sun, 28 Dec 2025 08:33:35 GMT  
		Size: 7.8 MB (7769499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44cba456c68ea28728fa377a36e3a33ef283f7ddc75966f61b04398cdd96a3f5`  
		Last Modified: Sun, 28 Dec 2025 08:33:36 GMT  
		Size: 13.0 KB (12992 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:133dceefe28117eaa25f7a676d1c698fd00d18fa172796f1f2a39fae3069b4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.1 MB (180073593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31e3b95f4f14b9f733a219207da8235471e91dded23d37fc28a8f9262518030`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 28 Dec 2025 05:52:12 GMT
MAINTAINER AntonOks
# Sun, 28 Dec 2025 05:52:12 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Sun, 28 Dec 2025 05:52:12 GMT
ARG rakudo_version=2025.12-01
# Sun, 28 Dec 2025 05:52:12 GMT
ENV rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:12:07 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 28 Dec 2025 06:12:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Sun, 28 Dec 2025 06:12:07 GMT
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
	-	`sha256:7d8eec79c9a4e5bc4dd20acecdde355a57d33906fdf19b4ea9a45d404d180499`  
		Last Modified: Sun, 28 Dec 2025 06:12:30 GMT  
		Size: 3.2 KB (3244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7405a3fd297caf3404b3b4e80425f58185229292e66edc966cce2ae56b383137`  
		Last Modified: Sun, 28 Dec 2025 06:12:33 GMT  
		Size: 37.8 MB (37814168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b97dac5e2c1dfde6e85254a359111f71863a91f26ae517bc3431174a58b38593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b672b2980dc22eb95f9fca365a146ae75dc544a7afc8d9b79bdb9b06ff1d97`

```dockerfile
```

-	Layers:
	-	`sha256:3308fa553a2c791b08292e5777d2770bf27e2fa52106da0576049497294855d5`  
		Last Modified: Sun, 28 Dec 2025 08:33:42 GMT  
		Size: 7.8 MB (7777174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b97b1945a3b482a96aa0fa587c119d53041f70a1d62fbcdfdd3ba8ae6c77b7fb`  
		Last Modified: Sun, 28 Dec 2025 08:33:42 GMT  
		Size: 13.1 KB (13099 bytes)  
		MIME: application/vnd.in-toto+json
