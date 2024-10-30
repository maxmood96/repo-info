## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:24c4d6c58ae053c4a58d600afb8a7eb1c12faeb05f7004cfc5f1ca3ae2b17fd3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:cec78db25e460e0821197b25f6f32ba534ee19b3a00a992be7bb8b62e0290cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48566212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d98ebf0912d2345ad228f3bb834ca4b10540b26cdfe487af9536d32fb0a7f0`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 03:18:11 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ARG rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
ENV rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
# ARGS: rakudo_version=2024.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 28 Oct 2024 03:18:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c454499e12d56d5d8d1f625de3a132a2950f95fb6b36b016dae77e4a185c54`  
		Last Modified: Wed, 30 Oct 2024 18:25:33 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a187625888c3f9f3dc823011cb7dbcca31e7b7c12a80c386bdb67d63d3f0ec`  
		Last Modified: Wed, 30 Oct 2024 18:25:34 GMT  
		Size: 44.9 MB (44941447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:7788cea9264c821703b970ee2bb8f2670fa4dc54c1c153c37aedb75748e19e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 KB (127377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5750ddd060701d0c13498390869dc21fb8d2c3ac330154c88ecd9b3fe76506`

```dockerfile
```

-	Layers:
	-	`sha256:65881754322061cd2cb8ded5bd6e6b5f83afe17ec1e605be2373231d17c18321`  
		Last Modified: Wed, 30 Oct 2024 18:25:33 GMT  
		Size: 115.8 KB (115835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24d84c3e744839e4ba7d9d173eb2c4b62113db0386eafdfc23731e30e84e1da8`  
		Last Modified: Wed, 30 Oct 2024 18:25:33 GMT  
		Size: 11.5 KB (11542 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:2ce2a44eb101b95ff1df31249ed21c6a6cd9ee35fbde278da71c6f7aa70499fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48875255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b2190c37e949c7ded7038016632dc4bd98580612be80a793c561943f9dc656`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 03:18:11 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ARG rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
ENV rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
# ARGS: rakudo_version=2024.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 28 Oct 2024 03:18:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adac99298427b0dcff4a83ee259bcfea75e29ecc63a015ed725b588f6dd3ea1c`  
		Last Modified: Wed, 30 Oct 2024 19:04:20 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d0ed0193eacf0c56621d51e2225ae6b9fb70621f2370246a25f3b4eed2adbd`  
		Last Modified: Wed, 30 Oct 2024 19:04:22 GMT  
		Size: 44.8 MB (44786649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:4bc1fe2aa12f31edb83a06715df0c5d524e7c9002be4cd3963ab9feb122c965f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 KB (127498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3745004811ad6e840cfdbe463f82e56f9044794e3809cf15f50bc4fd6cecc6d`

```dockerfile
```

-	Layers:
	-	`sha256:8d71de7144b10ebdb98efc6a5de00372b3a662b8b84dca73667b4378620d1460`  
		Last Modified: Wed, 30 Oct 2024 19:04:20 GMT  
		Size: 115.9 KB (115867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcb53bb46d85e71d6f05dc4406e4155cdea0ba5ca892f274636b238d018353bb`  
		Last Modified: Wed, 30 Oct 2024 19:04:20 GMT  
		Size: 11.6 KB (11631 bytes)  
		MIME: application/vnd.in-toto+json
