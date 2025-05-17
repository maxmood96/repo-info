## `julia:1-alpine3.20`

```console
$ docker pull julia@sha256:f6b74bf3d424578183b6048a2084a095b46a6d52e0cfff350a8084bf3ae18484
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine3.20` - linux; amd64

```console
$ docker pull julia@sha256:b287122c1e1f6d86a9e4ca1d9899267077fcbdec4b4a8470813555a692a94a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.4 MB (294438413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47089a3bf6068d2486c201175501756f2263a17362481c502344d7f3a26fee7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 14 Apr 2025 23:59:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_VERSION=1.11.5
# Mon, 14 Apr 2025 23:59:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.5-musl-x86_64.tar.gz'; 			sha256='1a5ff1dabf9c712502d17ea38bc9aa5507ae3e6f6add438fa34b77a3df8e466c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 23:59:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e733d5807997c2d8d4b673fece6b6d759289f7ec2ffabff3d2465c24f7a7b9`  
		Last Modified: Sat, 17 May 2025 01:38:58 GMT  
		Size: 290.8 MB (290811148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1722991b3207e2d0e9265f6bd677625ec76aaba1f827db67a9d3fc73d83ba6`  
		Last Modified: Sat, 17 May 2025 01:38:34 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine3.20` - unknown; unknown

```console
$ docker pull julia@sha256:911058561585b9d3675ec0fee8e5c3a7ecd102600034b18945e961f37a12e400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 KB (85502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba1402cb5ded6d7539429de8c0fcce5773e4fe79e38925cce4909c882e571938`

```dockerfile
```

-	Layers:
	-	`sha256:448742caa7033778bd15d8b2879b341da707350377e894e813f86ad8efdb6e9c`  
		Last Modified: Tue, 15 Apr 2025 21:52:43 GMT  
		Size: 72.9 KB (72926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca3ce3b289fc0c5f36d5c785d0234690bb1e5a3544541076117646fa60a0b56`  
		Last Modified: Tue, 15 Apr 2025 21:52:43 GMT  
		Size: 12.6 KB (12576 bytes)  
		MIME: application/vnd.in-toto+json
