## `julia:rc-alpine`

```console
$ docker pull julia@sha256:a7ee5bdecfc8eac615a41e29f575d0c49948c502a4c78c1fa726af31c7f78be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:rc-alpine` - linux; amd64

```console
$ docker pull julia@sha256:27eb79d6b5b35455ceca5129e92c7740f2079547bd0a88d551367e96c3b8e09d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (172960126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1222524efa305f3268e9dfb6de90781f5f681bc4b14eb1f49443f208e1c74c61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:14:09 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Jun 2023 00:14:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 00:14:10 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 03 Aug 2023 00:30:30 GMT
ENV JULIA_VERSION=1.10.0-beta1
# Thu, 03 Aug 2023 00:30:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.0-beta1-musl-x86_64.tar.gz'; 			sha256='dfe4eb34da27e6bc8f036473b1765aa3e90d954a226a2c6b16c95f9081d94531'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 03 Aug 2023 00:30:53 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Thu, 03 Aug 2023 00:30:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 00:30:53 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484c508c2b187208d145f02fa5ddf767b00cab97e16754547c16cd366737c897`  
		Last Modified: Thu, 03 Aug 2023 00:33:58 GMT  
		Size: 169.6 MB (169561874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a16d6613ede681fe732e3e5b01f39fe52f5202ce63ef8146c21ceb054e067a`  
		Last Modified: Thu, 03 Aug 2023 00:33:32 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
