## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:e46c003e9e4b6b303d44de2f24e8b1424bae5736a2718f7d12725ea012a9d318
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:97050756419eb501f0be4e40610b65665e1db33ad92fd05d618db8bbe44cd4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181879688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea021b0279cf6e523e5799a7deab6609fc30b45aa5c48a0e39a80ff894b894d6`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
MAINTAINER Rob Hoelz
# Mon, 28 Oct 2024 03:18:11 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ARG rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
ENV rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
# ARGS: rakudo_version=2024.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 28 Oct 2024 03:18:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551df7f94f9c131f2fec0e8063142411365f0a1c88b935b9fac22be91af227e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 64.4 MB (64391508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b7079f71d2b9cb5b091d83e9743431393b2abcfcbb89f5aa251a9ad02cd4bd`  
		Last Modified: Tue, 03 Dec 2024 04:48:54 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08483f85f5abf5717bc3d3203b05882e1bad247b6ab3a95279dadded989a55db`  
		Last Modified: Tue, 03 Dec 2024 04:48:54 GMT  
		Size: 45.1 MB (45121854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:e6f636544c1f7e72b4ccd47c09d4505ca8279b7937e8e79df1499d409096c00f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1950dba3e69b8b8b773229f84e29085de90306dcb29468144b79ca4ce28677`

```dockerfile
```

-	Layers:
	-	`sha256:2aed4ec6b62b5755769876e51398dfd03e57c4b1b93506b0eb502ff9ce7018f3`  
		Last Modified: Tue, 03 Dec 2024 04:48:54 GMT  
		Size: 7.8 MB (7769337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2af4c5db9fdde8b4032f0c0fafdae471f1989e0af2ec068df503c8f87fb7fda9`  
		Last Modified: Tue, 03 Dec 2024 04:48:54 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:79de1e3c86710784950ebbe8deaa4bfc9656db6437c4ee81c2e2ac005a063e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181016567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118d5229a8bd0a2994e193f3b93ef1df6a9964fea2dba9ca7102139f977ca446`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
MAINTAINER Rob Hoelz
# Mon, 28 Oct 2024 03:18:11 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ARG rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
ENV rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
# ARGS: rakudo_version=2024.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 28 Oct 2024 03:18:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261351ed796deb9fdad22dc734919eaf6726dd79a8dea99327d9e1376ecdcbce`  
		Last Modified: Tue, 03 Dec 2024 11:50:22 GMT  
		Size: 64.3 MB (64347852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e6ed1698d5490e992e98bc298614886a1b500596a7e299d59d8fc33c71c4d8`  
		Last Modified: Tue, 03 Dec 2024 17:19:28 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d86e49ce1ddb7a5b79f0b7153d705ba6bb72641ea7b99bd4f16320dbcf58965`  
		Last Modified: Tue, 03 Dec 2024 17:19:30 GMT  
		Size: 44.9 MB (44933981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:d89247381731341b1e8d68bdbe924c5a36331da254a415143a4d23938d50a6c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7788882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2011e4c1aafe01531b971737de9db4a51ea70920280b48e077b4c3b8f225eae7`

```dockerfile
```

-	Layers:
	-	`sha256:a9c8f917bb102f3afd2ec55d51cef2ec6e7442d60c8323067be70721fd8238e3`  
		Last Modified: Tue, 03 Dec 2024 17:19:29 GMT  
		Size: 7.8 MB (7775748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a900b4a88b60299d1ab9e0d79eeb8cf26d5b12c9c4249d74fd2c04b5fdee7616`  
		Last Modified: Tue, 03 Dec 2024 17:19:28 GMT  
		Size: 13.1 KB (13134 bytes)  
		MIME: application/vnd.in-toto+json
