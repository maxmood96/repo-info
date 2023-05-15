## `julia:alpine`

```console
$ docker pull julia@sha256:9df2dbe2638111d1133a5d401f981c46e7c98ae2c8fd2d21961a5e5ee13156f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:alpine` - linux; amd64

```console
$ docker pull julia@sha256:9ed027843d8b3172d329dc5c1d2c6a6e587e748c42148cef8760a8fccbb83b85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153983502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82888c0d329cf435c73c43c4d89b154f6c0aaeb5468851cdf4364ae43472fec1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Mon, 15 May 2023 22:24:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 15 May 2023 22:24:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 May 2023 22:24:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 15 May 2023 22:24:11 GMT
ENV JULIA_VERSION=1.9.0
# Mon, 15 May 2023 22:24:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.9/julia-1.9.0-musl-x86_64.tar.gz'; 			sha256='2594ff9a69d86415faae2e2e218ec3a5abbeb41ab3590b646b75824221adcb5b'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Mon, 15 May 2023 22:24:28 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Mon, 15 May 2023 22:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 22:24:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c3362ee69b9e183770605ef4b78cc162da6ed0150fa898768ebcb885a75ad3`  
		Last Modified: Mon, 15 May 2023 22:25:39 GMT  
		Size: 150.6 MB (150585641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ee82d7382bfddf890d4621823ade41cd9210f9d81b1e38b44b6696272338b8`  
		Last Modified: Mon, 15 May 2023 22:25:17 GMT  
		Size: 371.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
