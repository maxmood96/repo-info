## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:60f630c763fe053a4fbb90a877964f17d8021043b8b31e36abe4e0ba9203e862
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:f608fe8aae34343c8a52fbc9ba0e3ab0aec156b3547db71d69dc2acee6ae4da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52898044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c394f4de6f740f7e91e05c6ef8a0e2c4949864c2d6b047ade93082e31715395`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 23 Oct 2025 03:12:19 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ARG rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
ENV rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 23 Oct 2025 03:12:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94ae187876b8dfd9796c6a5e83b3fd4df758dab43d6e470d4b3e2b0e8e699ef`  
		Last Modified: Thu, 23 Oct 2025 23:46:46 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479dd71f79409ea180e1088f9824b93c21d4c109f800a05baef9ffaf1b948035`  
		Last Modified: Thu, 23 Oct 2025 23:46:49 GMT  
		Size: 49.1 MB (49094643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:771edf5e119637bd6e29891909c6e22a41bf60b6cc4c956f170592d07fd7e1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 KB (197780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6e06b7417bc34fb3651e11bc883f341b3ac83727b269273649d67b1ce09942`

```dockerfile
```

-	Layers:
	-	`sha256:da1fe5c8cdce4abdd95d12d29185b6bd74c1cc4ee40fff1c14afe654a98db351`  
		Last Modified: Fri, 24 Oct 2025 01:33:20 GMT  
		Size: 186.0 KB (186020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:702e025402ada9b8eeba1897b6a64f0bdfa61551086096a3d5aea7ef06c12e7d`  
		Last Modified: Fri, 24 Oct 2025 01:33:21 GMT  
		Size: 11.8 KB (11760 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:a550cebb99664a9633d897c98c89899f51d8f9435ef5b614eb545fba93995bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52925677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1445c061ae404b4788a5178c6db3e7339ec2789e163e26d90c7fb4940e352b6`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 23 Oct 2025 03:12:19 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ARG rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
ENV rakudo_version=2025.10-01
# Thu, 23 Oct 2025 03:12:19 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 23 Oct 2025 03:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 23 Oct 2025 03:12:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f354594890fce8d86fccc0efd95519674214696b4d7be96e258f4608cd8935`  
		Last Modified: Thu, 23 Oct 2025 22:30:49 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea0230fc82455718c52d3c89e277ef1cf39d85f33ab447bccb2d125194cb203`  
		Last Modified: Thu, 23 Oct 2025 22:30:53 GMT  
		Size: 48.8 MB (48786660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:5321a6a3a5400198193ec57dd6da13c6ab29c95dcd6acaec789d0bbbf8573dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 KB (197907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0a76bc0ad9780a1dfd9b03748bb412e60acbd0726a1e8445c9e17dd01e5839`

```dockerfile
```

-	Layers:
	-	`sha256:a7d61e7b14327a9149659f2cc4dd38b50e46d7c5b2f272ec0a135c79719380a4`  
		Last Modified: Fri, 24 Oct 2025 01:33:24 GMT  
		Size: 186.1 KB (186052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:119a5fd04ebf8a2ee4f6476233145b8923f667a97a8c22c43bcf7bac0df4c3ca`  
		Last Modified: Fri, 24 Oct 2025 01:33:25 GMT  
		Size: 11.9 KB (11855 bytes)  
		MIME: application/vnd.in-toto+json
