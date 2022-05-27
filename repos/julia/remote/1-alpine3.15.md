## `julia:1-alpine3.15`

```console
$ docker pull julia@sha256:d6fa8fabdd487c6ccf2bf73eda6f540c362fd797268db2706e46c77d42354bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1-alpine3.15` - linux; amd64

```console
$ docker pull julia@sha256:b3810391745644514855447b2583e831219e00b39d9dd4cfbbd09809fda8d6a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134196865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03dc1372900070bcda61a31f4c83ff609cdd7eb4fa5869d44fbd2097424fed53`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:10:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 05 Apr 2022 07:10:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 07:10:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 27 May 2022 00:31:09 GMT
ENV JULIA_VERSION=1.7.3
# Fri, 27 May 2022 00:31:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.7/julia-1.7.3-musl-x86_64.tar.gz'; 			sha256='e8c7d8e94228c775661a3c5a5744c12b46b5cbda177c6ba0def9ed33705e6786'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Fri, 27 May 2022 00:31:30 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ac6cb5611dac84b97f20f2fc55aa730efed8dc16ecc92ebf36e651c7af896b`  
		Last Modified: Fri, 27 May 2022 00:34:48 GMT  
		Size: 131.4 MB (131382306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
