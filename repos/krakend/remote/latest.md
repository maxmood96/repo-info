## `krakend:latest`

```console
$ docker pull krakend@sha256:7bfb05217733bdd654f56b4d0ff153bef9bea746fcc7517c2ec13e62815e010e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `krakend:latest` - linux; amd64

```console
$ docker pull krakend@sha256:4bbbc66146fd865620baca646329dad42b8e06fe85a53bb7c1d79405588fcab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51579111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2b93946d797828dc5f46500915dcb7244ef0a43f9e3a24746acd778582e21e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:20:31 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Wed, 08 Oct 2025 16:20:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Wed, 08 Oct 2025 16:20:31 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=c80858c5ee1e5d52f0e7aa9e5f0ed36b376e76f0341f51103ff5c1257070af8cd0803f91e811858246c013563dbb292328b18dd5feb4122cfa6ede7e8edca991; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=5a10fe6a588adfe28c1ce1b2f4b860260dfcc6a031853447a137182a611197c43f22f2e279e547287b7f447969148a3985065cf1c2b852bb7d357a4c48f83edc; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakendio/krakend-ce/releases/download/v2.11.1/krakend_2.11.1_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakendio/krakend-ce/releases/download/v2.11.1/krakend_2.11.1_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Wed, 08 Oct 2025 16:20:31 GMT
WORKDIR /etc/krakend
# Wed, 08 Oct 2025 16:20:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:20:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:20:31 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Wed, 08 Oct 2025 16:20:31 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6f9d6a4c9c190d8f354e7a2f90bad4256c4927c971bf881d9e7056091e6240`  
		Last Modified: Wed, 08 Oct 2025 18:08:07 GMT  
		Size: 459.5 KB (459536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887fd9f25b37eb598425945a5de0414d88ec397698c4e404bd036dce5b5f1e4e`  
		Last Modified: Wed, 08 Oct 2025 18:08:12 GMT  
		Size: 47.5 MB (47481330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac70813b70d060a25167cc60e4ea342f727cb802d56a1813c67b12c87adf924`  
		Last Modified: Wed, 08 Oct 2025 18:08:06 GMT  
		Size: 643.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:93d71d74c822a3e226d8d0fd5303b50884e667ee8f07a0b2d57b7d0c58babfb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 KB (15209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36892af222af9819576fcf4d9ad570a470c024b77237f40663692eb1d296073`

```dockerfile
```

-	Layers:
	-	`sha256:6a6408173c52598139397b2f6aeb177a9817331f62b48037dff2a629a1e006ab`  
		Last Modified: Wed, 08 Oct 2025 20:12:22 GMT  
		Size: 15.2 KB (15209 bytes)  
		MIME: application/vnd.in-toto+json

### `krakend:latest` - linux; arm64 variant v8

```console
$ docker pull krakend@sha256:fcc0a325c87d9519facb90ead3044106c71ccb4ac31bc1a2ebe169e676e90b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49186090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6f57c0d2973ef61b0cd9e5267bebde0ddc5d011a75f5d5fd2b0fccc3c7318a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 16:20:31 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Wed, 08 Oct 2025 16:20:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Wed, 08 Oct 2025 16:20:31 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=c80858c5ee1e5d52f0e7aa9e5f0ed36b376e76f0341f51103ff5c1257070af8cd0803f91e811858246c013563dbb292328b18dd5feb4122cfa6ede7e8edca991; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=5a10fe6a588adfe28c1ce1b2f4b860260dfcc6a031853447a137182a611197c43f22f2e279e547287b7f447969148a3985065cf1c2b852bb7d357a4c48f83edc; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakendio/krakend-ce/releases/download/v2.11.1/krakend_2.11.1_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakendio/krakend-ce/releases/download/v2.11.1/krakend_2.11.1_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Wed, 08 Oct 2025 16:20:31 GMT
WORKDIR /etc/krakend
# Wed, 08 Oct 2025 16:20:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 16:20:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 16:20:31 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Wed, 08 Oct 2025 16:20:31 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6a990d88595bcd9258c7ae339a53ec9297ef451f40421ab9bd12a801d83e1d`  
		Last Modified: Wed, 08 Oct 2025 18:08:30 GMT  
		Size: 463.1 KB (463146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b749a62d80a98133d46435037b69d1fb1634e089e240ab247945126d06a0987e`  
		Last Modified: Wed, 08 Oct 2025 18:08:40 GMT  
		Size: 44.7 MB (44735331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06591f25c72efd55f13e53486de943361d6722770f16c627e91600d65569657a`  
		Last Modified: Wed, 08 Oct 2025 18:08:31 GMT  
		Size: 644.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:3f2b23668e5b41cbf520d30f28ab566044c7f26e4bd1b1d61cb53344bbd6abeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 KB (15328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cdeaa0b9bdf0b7bf5428e631faa9cba1072e3ec8b27a9d3a706bec1d9674ab`

```dockerfile
```

-	Layers:
	-	`sha256:d8198db2c7700c3bf542696109ba8bd7c1ab689bd08ca65f52068a431d7eb151`  
		Last Modified: Wed, 08 Oct 2025 20:12:25 GMT  
		Size: 15.3 KB (15328 bytes)  
		MIME: application/vnd.in-toto+json
