## `julia:1-alpine3.19`

```console
$ docker pull julia@sha256:d87486d491c1a5d3567d01da25508c62798ca5eba3d5a278cbe64288c6352fa0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:b173e0fc6b927c55268f6b34ffeed624755a6c2abbca9ee54d1164f8d09f1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180483890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dec104b7b18b309590afc3ad2a4f0a951ea29c10faf13a93593fba453b82963`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Jun 2024 23:59:16 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Tue, 04 Jun 2024 23:59:16 GMT
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
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac9e56aea8a64f3cbe09ae5d0921c4033a441ddcd257664e4d43605b06df471`  
		Last Modified: Mon, 22 Jul 2024 23:06:13 GMT  
		Size: 177.1 MB (177064481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f30429bbccef6b6304122956127f98f8cb62d8dd9f39a93f70fcd2c816a538`  
		Last Modified: Mon, 22 Jul 2024 23:06:09 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:a08125953bbbf08305613692c44b2c413f861f326b55075bd15c551869541085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 KB (90602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6436df9f8fa91e38b5bd33695d454674c7f2720c3c75e9921208792dec674597`

```dockerfile
```

-	Layers:
	-	`sha256:77c131ade0415982c4fec8bbc576eb47ef8d258f076d873c096890cb86b98ffc`  
		Last Modified: Mon, 22 Jul 2024 23:06:09 GMT  
		Size: 78.3 KB (78265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9c60e27cec1d02bc82692abef41500c16ea7e70b25555a46161fe76689ef389`  
		Last Modified: Mon, 22 Jul 2024 23:06:08 GMT  
		Size: 12.3 KB (12337 bytes)  
		MIME: application/vnd.in-toto+json
