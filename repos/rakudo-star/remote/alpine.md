## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:20b4f2da16dcaec43872f73740c8ffb09d15844e970990e791087e6456c99729
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:7ba68152715de27831884af0929ad67fc5470c165da6b61f080ba28df758ae2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52786197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4293cea04569f8cba4ea278e22e92c2a645a4555b2e49b5b59b000dde53acbd`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 25 Sep 2025 18:16:25 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 18:16:25 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ARG rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
ENV rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 25 Sep 2025 18:16:25 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb568ddd1c171fa25eaf659e843ae544a16f6a01eeb1e49e2024de09d2859802`  
		Last Modified: Wed, 08 Oct 2025 23:32:04 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7abdd7824a25e48b2cb7b3b9601d90324022ce1dc44cccee3103958cb9b8bc`  
		Last Modified: Wed, 08 Oct 2025 23:32:06 GMT  
		Size: 49.0 MB (48982798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:802766c89ee57467889670b301f1181f4f9c7fb9e3d24ba21b1e63f2a6382266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 KB (197795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6093dbbd728edc0b4134ae851df675c55fb021ea696a066df63154b31d0fef`

```dockerfile
```

-	Layers:
	-	`sha256:cb14286aeb12efd3f73436a2d70d10dddcaef91fce106c2e570cfb6beeec1ef5`  
		Last Modified: Thu, 09 Oct 2025 01:33:20 GMT  
		Size: 186.0 KB (186024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78db66a19edca11888a6169ff5c8c4c411ced7b184935bec11adc74372e922a2`  
		Last Modified: Thu, 09 Oct 2025 01:33:21 GMT  
		Size: 11.8 KB (11771 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:ab2c76d88bf5eb48e0825125345838d323cbf22ca901acd2e6bf3a32c9685b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52894513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc524f2968a5856e4cd97223a684ab54252d95580d6360f30b0215ed2dc9221`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 25 Sep 2025 18:16:25 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 18:16:25 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ARG rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
ENV rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 25 Sep 2025 18:16:25 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b0d4bdb013522c8d0a0c94c80a2a4cf283e73f867aedd96e01f680dca84c9e`  
		Last Modified: Wed, 08 Oct 2025 22:22:04 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c738eb1065ed95605035bbec26e02e04090572ec08614269277b6ac389a7a891`  
		Last Modified: Wed, 08 Oct 2025 22:22:08 GMT  
		Size: 48.8 MB (48755496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:c87aff0017a83a37e45c37b8e4ad86ccc00f0b01234c9558b431cd8c9c51669e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 KB (197922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f266b2b5b18e42e51ccf7d210d6d02cd49fc7258a1c4274776f4ebfb671d614c`

```dockerfile
```

-	Layers:
	-	`sha256:695c5dc7135f76aac74050069cb34a1dcbcd61067e4d0bdeca4dff2fae1d8517`  
		Last Modified: Thu, 09 Oct 2025 01:33:24 GMT  
		Size: 186.1 KB (186056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a0177a3f02ba22841c9b3fb3c9898bfee297d5c9b13210c2af0f1d441b764b5`  
		Last Modified: Thu, 09 Oct 2025 01:33:25 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json
