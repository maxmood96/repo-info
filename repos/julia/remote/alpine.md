## `julia:alpine`

```console
$ docker pull julia@sha256:63f1b87c37354ada080b8ff19f960720e3cb3f5e40805e1b4f8880ce19188088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:alpine` - linux; amd64

```console
$ docker pull julia@sha256:67b9cca0941fd91943778c5af44fe15dd3b7a1313e3cc5466c9dc505fc2a6128
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137910584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d3107ed5f53156153c666df752f29f03c25965c82b0f3ae2ec6caa94e493f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Thu, 01 Dec 2022 20:56:47 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 01 Dec 2022 20:56:48 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Dec 2022 20:56:48 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 27 Dec 2022 18:37:04 GMT
ENV JULIA_VERSION=1.8.4
# Tue, 27 Dec 2022 18:37:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.4-musl-x86_64.tar.gz'; 			sha256='e24290c742cd8b3526330b72f2475f4bd9ea548bf3827d493e7df3da0583c130'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Tue, 27 Dec 2022 18:37:18 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Tue, 27 Dec 2022 18:37:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Dec 2022 18:37:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a158d742744e7cd706b421386e9dc0f2ba314a7355b367d1c428dca3e04b05d8`  
		Last Modified: Tue, 27 Dec 2022 18:40:12 GMT  
		Size: 134.5 MB (134539506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a59902c96e258ece25098bb1e601ed6e49238e1ae6479305e0080a922b2677`  
		Last Modified: Tue, 27 Dec 2022 18:39:49 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
