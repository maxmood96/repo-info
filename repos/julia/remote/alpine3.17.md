## `julia:alpine3.17`

```console
$ docker pull julia@sha256:9ba39e1931cdce7f671af6cc3647e1b9d04dfe7c860065727f34b695877b56d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:alpine3.17` - linux; amd64

```console
$ docker pull julia@sha256:7f199df42c03adbde5a4f98c7b6e424dcee166c3166185000fd458817638093a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154008698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3adb176cbb37f5601bc504a6943cf92b76d83ef2a5e35af0f1fb0791523293ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:04:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 29 Mar 2023 22:04:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Mar 2023 22:04:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 09 Jun 2023 06:31:45 GMT
ENV JULIA_VERSION=1.9.1
# Fri, 09 Jun 2023 06:32:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.9/julia-1.9.1-musl-x86_64.tar.gz'; 			sha256='9c33adcb1a1a7d3fca72cd4ac592d107ef2a70b1cb323e67a03b93a6e485fd0c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Fri, 09 Jun 2023 06:32:01 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Fri, 09 Jun 2023 06:32:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jun 2023 06:32:01 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f50003d7d6ce133628e1cf3e8580c1b5d3a79b248537eb5a4b7d5322bd81ce`  
		Last Modified: Fri, 09 Jun 2023 06:34:42 GMT  
		Size: 150.6 MB (150633766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2774065d74c23436bb8e36fb6e696e29cd2cb80fc1389d95184e0728a9b8607`  
		Last Modified: Fri, 09 Jun 2023 06:34:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
