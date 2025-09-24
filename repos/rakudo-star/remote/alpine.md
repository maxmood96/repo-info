## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:df255ffc1439245e8b1ac63e4a324ff3538f11403eda13605e654ea7938b8a32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:1bc512ea1640698b93202935f0296feac68e0f373b11541bdcee7f0e4d9f446b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46586336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3636b56e7047e491f39a70e879fb9cb42a76d0a88ac9db72e524c6b3df264ef4`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 06 Mar 2025 03:06:23 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
CMD ["/bin/sh"]
# Thu, 06 Mar 2025 03:06:23 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ARG rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
ENV rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
# ARGS: rakudo_version=2025.02-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 06 Mar 2025 03:06:23 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40846fd54c47d8a7bb154a2fbab5a0dd87087aa0f623fc203a5f7186dbf5ee3d`  
		Last Modified: Tue, 15 Jul 2025 19:48:43 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf4ae8ff5056d63922cca3b2c11a96b318ac846bae4d7dda8241c31022f29b5`  
		Last Modified: Tue, 15 Jul 2025 19:48:46 GMT  
		Size: 42.8 MB (42785702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:ad312f2a05bd3773725853b1d0b0e465cadea29f8b1e19ba7a8d05b2dc70fdc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 KB (132132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd98a13112ff73fc35af4f655615ec9647d878ce3260175a5cf2134dda56244`

```dockerfile
```

-	Layers:
	-	`sha256:234527b967730608cca382b34e2f62f5a3aea54766a598ba88e52458acfd74fb`  
		Last Modified: Tue, 15 Jul 2025 22:33:16 GMT  
		Size: 120.4 KB (120383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9acc71e602efdf0d69bd6f5bbaa8d5b31af3648bd5b46252c5b0e1bd2c96031`  
		Last Modified: Tue, 15 Jul 2025 22:33:17 GMT  
		Size: 11.7 KB (11749 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:0a9f51dde9679a0f880dbc4b322db523e324358faf7e2c193b642a9f5f0667eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52867285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aed50259288c8d8e91bc9eb06d67ab8868c80cc890acb1ca09493c186adf30e`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 23 Sep 2025 22:27:44 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ARG rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
ENV rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 23 Sep 2025 22:27:44 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfbdad542f1832bba5c94ef01c74d7be7bf3c61301ebbcf451e2da0dd184cf7`  
		Last Modified: Tue, 23 Sep 2025 23:43:49 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096970a951996d351b9326417b79a004409a7f7d181ce9696c2a6fcda8cbd039`  
		Last Modified: Tue, 23 Sep 2025 23:43:53 GMT  
		Size: 48.7 MB (48735587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:29d9c3a55ca997c5f3a628b56982cb4ab9110c346702363b280bbcd78dd7921d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 KB (197922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ecaa838c0222b8bfb4ea1e9f38566bd026f185a5a4796bb40ff0812e16e4267`

```dockerfile
```

-	Layers:
	-	`sha256:46dea7763507674cacdab410b5f3af80fa4a7b70bf84cb0e4737c2bb6c536265`  
		Last Modified: Wed, 24 Sep 2025 01:33:21 GMT  
		Size: 186.1 KB (186056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:659f7d3adfe9b6e9cf9da658336527238b2bdc2e62f9d2f4a918111c6c8de202`  
		Last Modified: Wed, 24 Sep 2025 01:33:22 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json
