## `julia:1-alpine3.21`

```console
$ docker pull julia@sha256:fce56b355c9ba531382fc3fd163ebff5c31310ecba5eb7f1830dd827dae375da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:c1ff3e885f354a03999f14b1db932dd0da4d31e1929756fbaf9492c3b215b781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295126458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53eac3c99ea88c4f449b6ef4381d0a6f8e6e14023735c900909163b0d7a05480`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 10 Jul 2025 17:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_VERSION=1.11.6
# Thu, 10 Jul 2025 17:59:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.6-musl-x86_64.tar.gz'; 			sha256='ca024f199e30af9d5dc002fdb238ff6b5f0729cdda3f9a4521e360288f12031f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Jul 2025 17:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15501648b2fc5bd253b3b383afcd53bd0084df7df632b8ea5a8e97eb3e53c53a`  
		Last Modified: Sat, 12 Jul 2025 05:19:21 GMT  
		Size: 291.5 MB (291483847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a568e41f478d45b9a2fd2bd3d899da7398d6317a7d624000d0f9a9db251faf`  
		Last Modified: Fri, 11 Jul 2025 23:37:29 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:6c8feb2022161643f93b14b028691e1acf5ef7ce8c42fa9f31fa28cf80764f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 KB (92821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e5a520f982d00287d27f94d3e19828fdccd4ac6260801fb07719f4dd980376`

```dockerfile
```

-	Layers:
	-	`sha256:3640822151899a0cab803e930893594ae1b1757ce490888ec115e39baea35f8f`  
		Last Modified: Sat, 12 Jul 2025 02:02:39 GMT  
		Size: 80.2 KB (80245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56b7bf6e3be3e0cdcd5e83e96ae11d852b25404fd3453fc5ac7acd06b18fdc9d`  
		Last Modified: Sat, 12 Jul 2025 02:02:40 GMT  
		Size: 12.6 KB (12576 bytes)  
		MIME: application/vnd.in-toto+json
