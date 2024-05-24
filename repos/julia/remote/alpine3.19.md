## `julia:alpine3.19`

```console
$ docker pull julia@sha256:31e29724ba1d1ac03a845dffc54f2da3cc840a1669907d9bc8148c43b312b3e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:29806286bc090934d9f4f75512a591c7678e4977376dd728e8695a2703bcf348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181477953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fbd97ebeb6535572e38fe958d9d1d88c381d091f39f5f2ed22948d89b56916f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 May 2024 13:40:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_VERSION=1.10.3
# Thu, 23 May 2024 13:40:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.3-musl-x86_64.tar.gz'; 			sha256='2bb735b3fdef62a4370a79b91239c47d8e8b923d5263466e63a2abc80faee9e5'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Thu, 23 May 2024 13:40:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 13:40:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 13:40:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88afc171df39ee2a0e032a548b78c4c01aace0e253e73364664cc6e8bbe9344f`  
		Last Modified: Fri, 24 May 2024 14:53:42 GMT  
		Size: 178.1 MB (178068855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae78ac58a29f7814f11c1d1ec0885e628d3e4a3396983845a231da64b66e1a1f`  
		Last Modified: Fri, 24 May 2024 14:53:39 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:d4f72333e9d2c2ae6197333f8b3cd1790c6544bd728d8032e4c7e2da38a66313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 KB (87631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33e90ea22efbd7206f5509a044a220a55aa2418d7e8189eee981af41139319c`

```dockerfile
```

-	Layers:
	-	`sha256:b300fc66733c47ee9e4ea2f581c808858d97f4cefff1bee8899cf3f082958ead`  
		Last Modified: Fri, 24 May 2024 14:53:39 GMT  
		Size: 75.2 KB (75177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75ae0ef531f5df3f4c09d95d01b19283a46792b3eba38b89b048e30f8b686988`  
		Last Modified: Fri, 24 May 2024 14:53:39 GMT  
		Size: 12.5 KB (12454 bytes)  
		MIME: application/vnd.in-toto+json
