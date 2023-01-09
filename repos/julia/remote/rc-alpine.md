## `julia:rc-alpine`

```console
$ docker pull julia@sha256:539a50180b59b0b39cd99682476370255d91106581a0495753aa8661559e6d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:rc-alpine` - linux; amd64

```console
$ docker pull julia@sha256:2f34a384dcedcf6c5117784c78dc4a1c85d96384841ae2434f4ad3f7063f55ec
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151968844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def9f70072dbd65a032e935fc13b77d3437805b5fa7b2ae9f13c806d9cf5e153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:20 GMT
ADD file:e4d600fc4c9c293efe360be7b30ee96579925d1b4634c94332e2ec73f7d8eca1 in / 
# Mon, 09 Jan 2023 17:05:20 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:28:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 09 Jan 2023 18:28:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jan 2023 18:28:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 09 Jan 2023 18:28:29 GMT
ENV JULIA_VERSION=1.9.0-beta2
# Mon, 09 Jan 2023 18:28:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.9/julia-1.9.0-beta2-musl-x86_64.tar.gz'; 			sha256='a2171d91f97ab7cb95f5aa4618878a8224e2eb046f5e71999952e7a1d2176e27'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Mon, 09 Jan 2023 18:28:49 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:28:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:28:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8921db27df2831fa6eaa85321205a2470c669b855f3ec95d5a3c2b46de0442c9`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.4 MB (3370628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc41df757538a7c90e74209dddad9183d6df7511f06ff1a9bebad695374d7de9`  
		Last Modified: Mon, 09 Jan 2023 18:31:06 GMT  
		Size: 148.6 MB (148597844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee18fc652b3c9c29572fa10542cde4c22500b872ad74366b4a1d627ea1ef387`  
		Last Modified: Mon, 09 Jan 2023 18:30:41 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
