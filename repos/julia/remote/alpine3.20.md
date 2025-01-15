## `julia:alpine3.20`

```console
$ docker pull julia@sha256:36bdd2cff17d005def5ced39df2fce1f06f3797e6c789d07fe5cd93eb234bf72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:alpine3.20` - linux; amd64

```console
$ docker pull julia@sha256:e764199815d9453aceae6459f4a5235ada084c9ecf6ac65c6718726bf60be959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294460117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da63cdeddf7a4b78d42adce868b0130a8cd28ecba1448b8eeb878cd7baffbbc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7896bc82c7ec6c59f0af6e7dfeb6b1d6668aeb7a36f4958a8d79a670e4f2c809`  
		Last Modified: Wed, 08 Jan 2025 18:00:28 GMT  
		Size: 290.8 MB (290833491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75cdd7c23ebe1c1c15f2284c5bd6f67b6ab00e769bf6d6b3f11927b6ce8080e`  
		Last Modified: Wed, 08 Jan 2025 18:00:24 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:alpine3.20` - unknown; unknown

```console
$ docker pull julia@sha256:9ecd79dd21d9b8e165c8c341265de3b0f308fe50dc63996cfd29411eae5f1c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 KB (85502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8132bfe87e02db14d7973f745bb4e474c438005dca92ffa9351f2dc5227e509f`

```dockerfile
```

-	Layers:
	-	`sha256:cf1f94b43ab787e3bbdcf9f8b40787d331e15968f3aa284c4c086c21ca392488`  
		Last Modified: Wed, 08 Jan 2025 18:00:24 GMT  
		Size: 72.9 KB (72926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c7e7d5a18dc1105acbf200e1eafc5480eb5b0a00aad3bee06b108acb75ff7f6`  
		Last Modified: Wed, 08 Jan 2025 18:00:24 GMT  
		Size: 12.6 KB (12576 bytes)  
		MIME: application/vnd.in-toto+json
