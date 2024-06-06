## `julia:1-alpine`

```console
$ docker pull julia@sha256:3e99c5859695a46d83d3516224e0d4f082bf20b5ccc7f9005106e0bfbf17961c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine` - linux; amd64

```console
$ docker pull julia@sha256:42b6ebb735a3fc3f066610629c757971b94bb265e3e90cad05404d4cf9b162ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.7 MB (180688186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080961ef7ca661f0d256317fbd1c86322594af347fc621ae4ce82071c7d5fd1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a314380c005f5b9a4cb31d9ea64abb63942ed1dacbd66f0e46fa020b4a88bb`  
		Last Modified: Thu, 06 Jun 2024 00:57:06 GMT  
		Size: 177.1 MB (177065720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38b1809cc5a8679fae3025a3a2890efe92a1319442d5b0e53ab81076d57bcfd`  
		Last Modified: Thu, 06 Jun 2024 00:57:01 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:a49a3e14854983349708d6c006e154dcb2f1e9bfcf1e776401d04bd755c4564e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 KB (85987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae6f61b2c81d2eb246cca14304ec7b3e848ed9c2137e8f26fcd6e18c1ed6eb8`

```dockerfile
```

-	Layers:
	-	`sha256:2cee0aba04e5440be2f358bbfe1bceb77da89f7a9e1042d38877360acaabe7af`  
		Last Modified: Thu, 06 Jun 2024 00:57:01 GMT  
		Size: 72.4 KB (72439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69e35e60864f62b135f1daec5f07f2cd8ef89a9084d0fc145997458e81518b66`  
		Last Modified: Thu, 06 Jun 2024 00:57:01 GMT  
		Size: 13.5 KB (13548 bytes)  
		MIME: application/vnd.in-toto+json
