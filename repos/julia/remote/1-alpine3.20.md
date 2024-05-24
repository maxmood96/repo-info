## `julia:1-alpine3.20`

```console
$ docker pull julia@sha256:729c03a7672d50b7c97e86973e3d7c2d3e2b49a2f1b63131eb1e95330d64b3be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine3.20` - linux; amd64

```console
$ docker pull julia@sha256:284152c59dbbb78046656422cfc003ce6cbaebaeb4996c3985a14ca4a2667b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.7 MB (181688995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821b7875166ee19fc39813b71a00a31a9187b7f7487b722a4e9f50f09ca21c6a`
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
ENV JULIA_VERSION=1.10.3
# Thu, 23 May 2024 13:40:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.3-musl-x86_64.tar.gz'; 			sha256='2bb735b3fdef62a4370a79b91239c47d8e8b923d5263466e63a2abc80faee9e5'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
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
	-	`sha256:a052d105e45167a802f06e2401858b5f924b659453f2152d97fa5fca320ff05d`  
		Last Modified: Fri, 24 May 2024 14:53:58 GMT  
		Size: 178.1 MB (178066536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906e956a18d8b6719b5f959bb9dfa006f1c71a6fa108eb20c3bb7f8c3937ab43`  
		Last Modified: Fri, 24 May 2024 14:53:54 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine3.20` - unknown; unknown

```console
$ docker pull julia@sha256:b6dabee607cf27abf47cefeb37e39443f762c69818b17f60f53e8f418b0be475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 KB (86106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d58e9ce29e41d12bb80b575cb7a8a7437a38f22dcf0c902081ae90732c6d89`

```dockerfile
```

-	Layers:
	-	`sha256:f726d6f298b368404a4d6a9bb3ae6f5b5a752bc02bca7026bdcd9b87a5ca25d7`  
		Last Modified: Fri, 24 May 2024 14:53:53 GMT  
		Size: 72.4 KB (72440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc8ff8753685fbf1075c09a024d3e7edd790cd828f74bdf7da59af0d037061d`  
		Last Modified: Fri, 24 May 2024 14:53:53 GMT  
		Size: 13.7 KB (13666 bytes)  
		MIME: application/vnd.in-toto+json
