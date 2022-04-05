## `julia:1-alpine3.15`

```console
$ docker pull julia@sha256:9ac3b3431bd54776cf889f71b08012ca7bb6cab4dc33ea7ce5fe324c6790fdc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1-alpine3.15` - linux; amd64

```console
$ docker pull julia@sha256:ef0b0602d581ae2181b2f956c8edf2fc5f394fbb477967c3b39e7651d2c85b33
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134581803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d2cae3d05e78023ce83c6ad5ec1305ebb91fe6fc01197f5f762631aec91bde`
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
# Tue, 05 Apr 2022 07:11:01 GMT
ENV JULIA_VERSION=1.7.2
# Tue, 05 Apr 2022 07:11:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.7/julia-1.7.2-musl-x86_64.tar.gz'; 			sha256='3bd653265f387450c796157629e6aa7aa4473d0169ef516a18e7b06b0301a7e1'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Tue, 05 Apr 2022 07:11:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fd9e782ff3c4a17bc140f9de2c1696d1c15aca1fbde3a9afdf8117c2a647b8`  
		Last Modified: Tue, 05 Apr 2022 07:14:33 GMT  
		Size: 131.8 MB (131767244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
