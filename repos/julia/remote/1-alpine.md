## `julia:1-alpine`

```console
$ docker pull julia@sha256:135e15f017347ae4a1f07e506fa389bfe5cf98cd34019162f9e23f75e6e542a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1-alpine` - linux; amd64

```console
$ docker pull julia@sha256:a4ccea96659a0418914abfeb46e834b8d77cb01c6f2ff3bdc096235521eed59c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134565832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0afb8e9089caa6a380447e128cc386ace395d818445178ae13f4f3cc50d806bb`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 23 May 2022 19:19:30 GMT
ADD file:8e81116368669ed3dd361bc898d61bff249f524139a239fdaf3ec46869a39921 in / 
# Mon, 23 May 2022 19:19:31 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 19:34:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 25 May 2022 19:34:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 May 2022 19:34:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 25 May 2022 19:35:02 GMT
ENV JULIA_VERSION=1.7.2
# Wed, 25 May 2022 19:35:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.7/julia-1.7.2-musl-x86_64.tar.gz'; 			sha256='3bd653265f387450c796157629e6aa7aa4473d0169ef516a18e7b06b0301a7e1'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Wed, 25 May 2022 19:35:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2408cc74d12b6cd092bb8b516ba7d5e290f485d3eb9672efc00f0583730179e8`  
		Last Modified: Mon, 23 May 2022 19:09:38 GMT  
		Size: 2.8 MB (2798889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38074b0f5006dba232528bb483d4dacce34cfb6c651549dae9695b6d622a52c7`  
		Last Modified: Wed, 25 May 2022 19:37:51 GMT  
		Size: 131.8 MB (131766943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
