## `julia:1-alpine3.21`

```console
$ docker pull julia@sha256:f2922eb1db894483efe2b4267dd8ae0d68923669b5e830ee1949ca022b23d689
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:138dfba624506fbdd113d360fca3850cd434a2b53fe9fd2eb0b0c49acebcd7c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295121625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a78dc9388a8b95db36f26c5f4e956f0f26ae3c94ea517c1eb28eebf593230ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 10 Jul 2025 17:59:19 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
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
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8234f603dd35c6a974d0ed46e1b148d364b85d8f572ae68c65dc5f905b0ccf7c`  
		Last Modified: Wed, 16 Jul 2025 01:39:09 GMT  
		Size: 291.5 MB (291483685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5a359321d77a8464c0f3457901edba1fd4b7e80683b8bc411f6a00a7d82214`  
		Last Modified: Tue, 15 Jul 2025 19:13:49 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:20e11d8774f03ca11f094dc7ad06c9b65afd1a20729c73378222e4b36622f032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 KB (92821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2993a38d24cb94d7e74cad17f4df7ed236f3cf609d67a5d295ae7d2544fa8582`

```dockerfile
```

-	Layers:
	-	`sha256:35a037201ba29402074d50427acccabbaf163a9db86eeab62bbc762a71fbe481`  
		Last Modified: Tue, 15 Jul 2025 23:02:21 GMT  
		Size: 80.2 KB (80245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a8816b06d57ed34860e4c7db5fc828c92868d8bc49be4df87369dbde4148049`  
		Last Modified: Tue, 15 Jul 2025 23:02:22 GMT  
		Size: 12.6 KB (12576 bytes)  
		MIME: application/vnd.in-toto+json
