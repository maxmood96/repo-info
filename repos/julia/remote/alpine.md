## `julia:alpine`

```console
$ docker pull julia@sha256:0f20015a8db8fecc41942a842f1a2786238a2eb12451d850cfacd09d045fcf31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:alpine` - linux; amd64

```console
$ docker pull julia@sha256:13218a325a9c887ecef20ddb6c466771e848aeb988d1f643686c73eedd106afb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149941305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8f43b13a61779c303d00270995686a8379abbcf51516066c0600997427592f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 06 Oct 2022 22:47:30 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_VERSION=1.8.2
# Thu, 06 Oct 2022 22:47:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.2-musl-x86_64.tar.gz'; 			sha256='9a50f90f30254b588be74e1cb983f6408b0ed81f28f7cd7077a0eefc7f33e04a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 06 Oct 2022 22:47:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2882d2a8dfa789bca23e47bfb1771aeecb1a9a98fd41926bdfc49aa1771f659`  
		Last Modified: Thu, 06 Oct 2022 22:57:10 GMT  
		Size: 147.1 MB (147135251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
