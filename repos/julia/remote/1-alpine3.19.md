## `julia:1-alpine3.19`

```console
$ docker pull julia@sha256:57ef99e72fc86548c4538bcac207cb90c5ddd6a9264d0a218a0ff3b48d04a7d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:f0ed31f0f5408f89ebab2c32d35380e769ee1a85a5e970711eeb2b16a1792f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180473700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22b4a3daffb688d629b1de81ebe39961a8864cde4b34c09de2119726d1f7eb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Jun 2024 23:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_VERSION=1.10.4
# Tue, 04 Jun 2024 23:59:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.4-musl-x86_64.tar.gz'; 			sha256='c7506a1aad431ff1d902a3f4eb9373cfe25440492b45148268a5aca48ece04c2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 23:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d08fe266ed4e029f8af33b2981b111b6f1a3304009eb7d6f6669b6bb52a18f9`  
		Last Modified: Thu, 06 Jun 2024 00:57:24 GMT  
		Size: 177.1 MB (177064602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfe37eee830fb348af54590182c08e0789dc5bde6c98fe08669ed33b245e04e`  
		Last Modified: Thu, 06 Jun 2024 00:57:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:17213d372ae6fbc065624dde93023dcf7a239a9e84bb93f09955ee386a00c390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 KB (87513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0018f4e93bf81bc126be9cabeee2a8ca375eb2fb82195f39c762107f4928f795`

```dockerfile
```

-	Layers:
	-	`sha256:06cb320500684e15714e97e245acf514bcc48ad4f1f433e18af1de4995c4a40d`  
		Last Modified: Thu, 06 Jun 2024 00:57:20 GMT  
		Size: 75.2 KB (75176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9b386b0f1387c7c5507291e3e1868d9ea8e020a863b1d9d9ba0828a1a03a701`  
		Last Modified: Thu, 06 Jun 2024 00:57:20 GMT  
		Size: 12.3 KB (12337 bytes)  
		MIME: application/vnd.in-toto+json
