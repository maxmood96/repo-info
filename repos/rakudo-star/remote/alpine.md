## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:a2f6e7033e1e57ae5951ec0fc8a395c4e9fcfc1f8583005fbaf8db92f746f7f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:c8c976ca3fc139d061d848201f107b3b9c72d8a5022a71090ae196846165dc8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53201174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d45ee45f329ed7a83b2cdaa7e446367b0a345d03da8b1533f7c8061fcc8085`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 20:03:16 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Wed, 03 Dec 2025 20:19:47 GMT
ARG rakudo_version=2025.10-01
# Wed, 03 Dec 2025 20:19:47 GMT
ENV rakudo_version=2025.10-01
# Wed, 03 Dec 2025 20:19:47 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Wed, 03 Dec 2025 20:19:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 03 Dec 2025 20:19:47 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea966dcb91608765a4b518e719c4b74c2fa933682229f548b6952421f033d9e`  
		Last Modified: Wed, 03 Dec 2025 20:20:12 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67c87c769308d01dd4494173151acd529862506a291feb41229eb3f0b8ef37d`  
		Last Modified: Wed, 03 Dec 2025 20:20:15 GMT  
		Size: 49.3 MB (49340915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:087a8b78029e8a16023aa2e8c6d5b5b100dbb00a3a49d378d47d218ed27eaac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 KB (198691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfa296b0f199a17f3a46901d18750d69929f7190f46e9606cb1b956ec0ef3fe`

```dockerfile
```

-	Layers:
	-	`sha256:c57e1b14a07da6455345eb2c43f7807ee74ec4291de17eed32e9fa4f489459ac`  
		Last Modified: Wed, 03 Dec 2025 23:33:50 GMT  
		Size: 187.0 KB (186973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb4f9f7c2166835f05a85e7a8704f8ade738381ce9655da6a96f0f3805fc2a98`  
		Last Modified: Wed, 03 Dec 2025 23:33:51 GMT  
		Size: 11.7 KB (11718 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:c2fc729067afec561672c23fb3aae61e71b287f76a0b521787a91fa82abbd7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53260811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f416b4aac7673c941ca50990f89b25a7c71d1dede8d0d564cd2f5105f1b8b2f4`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 20:02:44 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Wed, 03 Dec 2025 20:23:50 GMT
ARG rakudo_version=2025.10-01
# Wed, 03 Dec 2025 20:23:50 GMT
ENV rakudo_version=2025.10-01
# Wed, 03 Dec 2025 20:23:50 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Wed, 03 Dec 2025 20:23:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 03 Dec 2025 20:23:50 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6746cc9aada545857a96583e349746c29ac6a577f1b0cd17c0f98f56a770941c`  
		Last Modified: Wed, 03 Dec 2025 20:24:19 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e038c16be749f056d0c640d52d6dc8af117865f2d7a96b4599ab257abd1283f`  
		Last Modified: Wed, 03 Dec 2025 20:24:25 GMT  
		Size: 49.1 MB (49064665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:5c3c99acb4d4bec7013352ab55061309ca9b4f68e316e872d8c13a5d977810b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 KB (198168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f7981983392dfb5d8c28ed760600dbc4823be84e9df1cf242ed69688b816a6`

```dockerfile
```

-	Layers:
	-	`sha256:84621f879b0599da41a08ac876eaf36de8f6a432d0a0af329c2e3a8e54ac08c3`  
		Last Modified: Wed, 03 Dec 2025 23:33:54 GMT  
		Size: 186.4 KB (186355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a69e042e15077c32fa7beb783e769edd275673015610276c6fafc8443bd53a7f`  
		Last Modified: Wed, 03 Dec 2025 23:33:55 GMT  
		Size: 11.8 KB (11813 bytes)  
		MIME: application/vnd.in-toto+json
