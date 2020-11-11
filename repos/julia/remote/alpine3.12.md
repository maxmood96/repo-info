## `julia:alpine3.12`

```console
$ docker pull julia@sha256:07b22df615a7f0b7d31e2aa236f4756f7c9966c3e1389c78e0e740b9cc5340a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `julia:alpine3.12` - linux; amd64

```console
$ docker pull julia@sha256:bc82144c361781c3b65467965ce33fb461709a6236c8a5dc44613cef7e68e3fe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112506931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01dd80791cb4decdc2e9c578e70ce08394674a6415fc9c3334919f19b39f9cc6`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:36:22 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 22 Oct 2020 04:36:23 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Oct 2020 04:36:23 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 11 Nov 2020 01:34:44 GMT
ENV JULIA_VERSION=1.5.3
# Wed, 11 Nov 2020 01:34:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) tarArch='x86_64'; dirArch='x64'; sha256='2faf4ebe3b5fa1bbee853655ef7c292b457e80d3fca1af1c8d3f179286b27da6' ;; 		*) echo >&2 "error: current architecture ($apkArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	wget -O julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz.asc"; 	wget -O julia.tar.gz     "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Wed, 11 Nov 2020 01:34:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a76e24ea5a6b250dc311126c9e1a6a66304456bc71e88ed387deb66cb788897`  
		Last Modified: Wed, 11 Nov 2020 01:36:08 GMT  
		Size: 109.7 MB (109710071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
