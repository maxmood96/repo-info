## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:e07888cf563040648f3276c9a1de410e77b013921c5df0c81ba5261943473e35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:6c92a86b586e15724d82bb65d07b554101290c746d453ff619a991752ab8c686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177941012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe42dadb31807624141cf42211a738d87c5e954a2d3555cd27178570f20bd3f`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:03:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:42:06 GMT
MAINTAINER Rob Hoelz
# Tue, 24 Feb 2026 20:42:06 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 24 Feb 2026 20:42:06 GMT
ARG rakudo_version=2026.01-01
# Tue, 24 Feb 2026 20:42:06 GMT
ENV rakudo_version=2026.01-01
# Tue, 24 Feb 2026 20:55:14 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 20:55:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 24 Feb 2026 20:55:14 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa27031269f0a970255d56a9e793fc2a9d6bb091463cd5e632af4ae274881601`  
		Last Modified: Tue, 24 Feb 2026 20:03:49 GMT  
		Size: 64.4 MB (64395853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0cb6749902567cac6d03be626f17a6413f5e4a380972a5af57ef2f0084cd56`  
		Last Modified: Tue, 24 Feb 2026 20:55:27 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611b5781bff0edfb56382588536700e10a2e0be0e4bb6352703c0a5a4120209a`  
		Last Modified: Tue, 24 Feb 2026 20:55:28 GMT  
		Size: 41.0 MB (41014694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:4d5dce5844e9fb9dd8cf25c9c0feb0d0a3863dc49ea30aa84286a09009ad17d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79df3b26b9465df992be43c7e6aac12f0d9c56fbca2dd8068448cbcf861ae64`

```dockerfile
```

-	Layers:
	-	`sha256:9fa361119b10e65b5b2a0d65e180d765f657b886fb3bc83ba150db41677bc193`  
		Last Modified: Tue, 24 Feb 2026 20:55:27 GMT  
		Size: 8.0 MB (7968447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:440f07b97eb32e236c20f29c7e29acb83eb032bbb3d60da95188a97e697f77a1`  
		Last Modified: Tue, 24 Feb 2026 20:55:27 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:0a99a97a658cc5e0235a5ae99c886548b60ae6c1e5a0a2c4ff0f994c94cd0ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175504671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7b1d948a8e5a45f57d6a3cfdf4f44788bab72e48d14dcce6781326ef937656`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:14:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:33:29 GMT
MAINTAINER Rob Hoelz
# Tue, 24 Feb 2026 21:33:29 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 24 Feb 2026 21:33:29 GMT
ARG rakudo_version=2026.01-01
# Tue, 24 Feb 2026 21:33:29 GMT
ENV rakudo_version=2026.01-01
# Tue, 24 Feb 2026 21:53:27 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 21:53:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 24 Feb 2026 21:53:27 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d27b842bb73f4af595ce58848c4c53ae713ca5c649636d25b483ca63bccc52`  
		Last Modified: Tue, 24 Feb 2026 20:14:46 GMT  
		Size: 64.5 MB (64479406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e88e002c8fe052dc7e362524df55a04dfef5b0e5625d1d9422ff6f37e857ff`  
		Last Modified: Tue, 24 Feb 2026 21:53:42 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026eb2954984506fff995ed957bd0c2e7dd0f0499d18c9c829cc9873212b0366`  
		Last Modified: Tue, 24 Feb 2026 21:53:44 GMT  
		Size: 39.0 MB (39044081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:0996c594e85e035208453b7574ffcc304a85ad31ce45efbd9aa09992250ba444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d19f0a3dc16af9a3fcff00be54699e9afd4eb8734dc9ff368c0fb9da5022c08`

```dockerfile
```

-	Layers:
	-	`sha256:b3f709b64cb707ca2f29dfe8a616b6274e447a59249c50f61d2ad3b0ccbbdc3b`  
		Last Modified: Tue, 24 Feb 2026 21:53:43 GMT  
		Size: 8.0 MB (7974840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f745f7daba9612e85227c91cfc8f7395094fc2081f6ede7f66cf6d00c6a70431`  
		Last Modified: Tue, 24 Feb 2026 21:53:42 GMT  
		Size: 12.8 KB (12797 bytes)  
		MIME: application/vnd.in-toto+json
