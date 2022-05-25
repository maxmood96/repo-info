## `julia:rc-alpine`

```console
$ docker pull julia@sha256:4d3e2c751251f8c16a81e366779bb15b0b612131bd0a547544dc69f0639939ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:rc-alpine` - linux; amd64

```console
$ docker pull julia@sha256:9ff157819d333322641d584cc0cfa2e9044e437d75954498a774445a7c888ef1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145556826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91abb6879eb4fd99e79d2e7e0364786c6671c03fff6c55572cc70453ccb50909`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 23 May 2022 19:19:30 GMT
ADD file:8e81116368669ed3dd361bc898d61bff249f524139a239fdaf3ec46869a39921 in / 
# Mon, 23 May 2022 19:19:31 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 19:34:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 25 May 2022 19:34:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 May 2022 19:34:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 25 May 2022 19:34:36 GMT
ENV JULIA_VERSION=1.8.0-beta3
# Wed, 25 May 2022 19:34:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.0-beta3-musl-x86_64.tar.gz'; 			sha256='88fcc6b603e642d4884ba63c653a4885e74a715a982d0fda30e07f9f65e13540'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Wed, 25 May 2022 19:34:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2408cc74d12b6cd092bb8b516ba7d5e290f485d3eb9672efc00f0583730179e8`  
		Last Modified: Mon, 23 May 2022 19:09:38 GMT  
		Size: 2.8 MB (2798889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be4a8ecf7be8feca520206a99b070e14108189a9ba05580bb4f71c19bc45b04`  
		Last Modified: Wed, 25 May 2022 19:37:06 GMT  
		Size: 142.8 MB (142757937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
