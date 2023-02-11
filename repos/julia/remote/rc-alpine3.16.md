## `julia:rc-alpine3.16`

```console
$ docker pull julia@sha256:47b89116bc659f5398a8b999629eb08cbbbef905e9b5fd274b1c71acbdb74d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:rc-alpine3.16` - linux; amd64

```console
$ docker pull julia@sha256:0ae5776070e1489bfafef358155bda2452290491662052256ce350884d5de310
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.8 MB (152843814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5eecdf703f7b493990930fb15a0c61f1d83a6ef55866fdb76a0845f78823e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 09:51:23 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 11 Feb 2023 09:51:23 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Feb 2023 09:51:23 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 11 Feb 2023 09:51:24 GMT
ENV JULIA_VERSION=1.9.0-beta4
# Sat, 11 Feb 2023 09:51:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.9/julia-1.9.0-beta4-musl-x86_64.tar.gz'; 			sha256='fcf4fc9f076526591bd73c9b55eb7a6db3d45484bd4874d0160a265a068eecc4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Sat, 11 Feb 2023 09:51:39 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Sat, 11 Feb 2023 09:51:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 11 Feb 2023 09:51:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893e28b3225a8f49181126a80bd683537d1f207d2b07f58f34e0b0afc4ed795f`  
		Last Modified: Sat, 11 Feb 2023 09:54:51 GMT  
		Size: 150.0 MB (150035682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3ec6077f2e468da011f35520681503011eda7c499d437c4a97568917ed93d7`  
		Last Modified: Sat, 11 Feb 2023 09:54:27 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
