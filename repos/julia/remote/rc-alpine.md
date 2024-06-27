## `julia:rc-alpine`

```console
$ docker pull julia@sha256:19aac423a4bf24d126e7c4d7a21a0586f56dd59cbc2765bc83e7e2ade0b47f35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:rc-alpine` - linux; amd64

```console
$ docker pull julia@sha256:a7b154c49bda92d159eb29a15456f3fc1d357a66fd8bda07238bd25dd04a2c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261335972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01da07dc1533957a232c06df3fd3e54c11593a0663303e4f4bb1691ad0fb315f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 May 2024 13:40:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_VERSION=1.11.0-beta1
# Thu, 23 May 2024 13:40:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.0-beta1-musl-x86_64.tar.gz'; 			sha256='eee8f77c947b88334306ee4a9fce3633851a5d3954746138dc69e8be99b68b57'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Thu, 23 May 2024 13:40:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 13:40:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 13:40:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fc59a008043360328808a292f7c36858c26f5e41e5d25b894f630531a4614c`  
		Last Modified: Fri, 24 May 2024 14:53:51 GMT  
		Size: 257.7 MB (257713512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da83669e7381d5f172527503a04b443c06a072ac7f9fb181f6e7d19f8fa00552`  
		Last Modified: Fri, 24 May 2024 14:53:48 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:965abb440f3d0f2cddff0cf939a13e0c7f524c2d9eee161fb414585118ad6c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 KB (84058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91a4373247788ac5f9d7280e9771f18fcaaf3d68e3505a07d4659e7cac766b0`

```dockerfile
```

-	Layers:
	-	`sha256:b3bc7a81f2d72767afd4467d0eb5161a4f5ecf69aaa29c3ca05de4f2f1dee489`  
		Last Modified: Fri, 24 May 2024 14:53:48 GMT  
		Size: 70.9 KB (70907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:165b81f35896593a39b6e0129349190fd01c3d4a922660f4184510181d77f501`  
		Last Modified: Fri, 24 May 2024 14:53:48 GMT  
		Size: 13.2 KB (13151 bytes)  
		MIME: application/vnd.in-toto+json
