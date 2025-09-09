<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `krakend`

-	[`krakend:2`](#krakend2)
-	[`krakend:2.11`](#krakend211)
-	[`krakend:2.11.0`](#krakend2110)
-	[`krakend:latest`](#krakendlatest)

## `krakend:2`

```console
$ docker pull krakend@sha256:639e285e3f6621a3a171c5c5bdf4fc3e2b5b8d016a0bf9c2da6f748e1973e020
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `krakend:2` - linux; amd64

```console
$ docker pull krakend@sha256:afce54a8bb15f49678ae72f1d9aeb23eb3cc99829e14d177f880e28f875cef27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52586455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:848dd60b8ce67df86f71fd0a55e9ea0c674c2a186041168223815f09444f6b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 22 Jul 2025 17:08:04 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Tue, 22 Jul 2025 17:08:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Tue, 22 Jul 2025 17:08:04 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=0c60cdf57f8ee7d5747d5792b0d4ddc5200b7e6c58948a3ecfdf4acdb9f7ddb4c2f3c168be85c9f2afc12532c9522d80d1c5e9c8ab0fb9320e7b107a059a6299; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=99b799263e05b4cad1b2067552028494e400d22d7a4b62d8c96df5e1b3077f483025726bf4ad332ab353dc7e8930fa5575e62751fc5bcf3e013492d431f50021; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakendio/krakend-ce/releases/download/v2.10.2/krakend_2.10.2_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakendio/krakend-ce/releases/download/v2.10.2/krakend_2.10.2_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Tue, 22 Jul 2025 17:08:04 GMT
WORKDIR /etc/krakend
# Tue, 22 Jul 2025 17:08:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 17:08:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 17:08:04 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Tue, 22 Jul 2025 17:08:04 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eae94c387d75e3e97c70fdc10a5a9076714d50c1dbc442f6657ec833ef0365b`  
		Last Modified: Tue, 22 Jul 2025 17:24:57 GMT  
		Size: 450.1 KB (450056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea206dc7856d95934e7cfb13f3da9535befd3dc59751e0eea1f17759c301474`  
		Last Modified: Tue, 22 Jul 2025 17:25:01 GMT  
		Size: 48.5 MB (48498155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2aa6f4e89734c7bb29aed1bde9fee8507d5911ad34bb0a7a0e5fad85b36f22`  
		Last Modified: Tue, 22 Jul 2025 17:24:57 GMT  
		Size: 642.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:2` - unknown; unknown

```console
$ docker pull krakend@sha256:bdee62c78a047449ae7c1f265c15a4ed66c4b12089f668a056229204c39ac035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 KB (15209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586452b72e8560fc4e4691a536445d38b93cd31bd2f719fefa0e464bcf0855bc`

```dockerfile
```

-	Layers:
	-	`sha256:e150a1ec2a3160bf6f4ea3acb14b8827382b948fe96c268101a06474ecf8e7c1`  
		Last Modified: Tue, 22 Jul 2025 20:12:18 GMT  
		Size: 15.2 KB (15209 bytes)  
		MIME: application/vnd.in-toto+json

### `krakend:2` - linux; arm64 variant v8

```console
$ docker pull krakend@sha256:789cde13d08689696df24f965f18f9cb4b5e314c556549b29413d038536d8e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50605702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277eaa159c0c98bbe8b791b6835f32a13f87957b41de20bf34231ffdd4292207`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 22 Jul 2025 17:08:04 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Tue, 22 Jul 2025 17:08:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Tue, 22 Jul 2025 17:08:04 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=0c60cdf57f8ee7d5747d5792b0d4ddc5200b7e6c58948a3ecfdf4acdb9f7ddb4c2f3c168be85c9f2afc12532c9522d80d1c5e9c8ab0fb9320e7b107a059a6299; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=99b799263e05b4cad1b2067552028494e400d22d7a4b62d8c96df5e1b3077f483025726bf4ad332ab353dc7e8930fa5575e62751fc5bcf3e013492d431f50021; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakendio/krakend-ce/releases/download/v2.10.2/krakend_2.10.2_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakendio/krakend-ce/releases/download/v2.10.2/krakend_2.10.2_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Tue, 22 Jul 2025 17:08:04 GMT
WORKDIR /etc/krakend
# Tue, 22 Jul 2025 17:08:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 17:08:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 17:08:04 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Tue, 22 Jul 2025 17:08:04 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10565e445dbdde4f630b6b91820343bf053438219630d56d27f04fe544a95718`  
		Last Modified: Wed, 23 Jul 2025 19:25:57 GMT  
		Size: 453.4 KB (453414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ecbb898c698017f656de8d8a1aa0aa11fa19549f8966bc6eac599f8daba3cf4`  
		Last Modified: Wed, 23 Jul 2025 19:26:00 GMT  
		Size: 46.2 MB (46164677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93a8fad8e4cdb7180d9027b6195c9c8c2f52c0796b1f204b25640e5de2d3526`  
		Last Modified: Wed, 23 Jul 2025 19:25:57 GMT  
		Size: 642.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:2` - unknown; unknown

```console
$ docker pull krakend@sha256:787cddaee97e87f54db3bcbb232f65535a233221e8a396b5f8bf260e6ce4a348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 KB (15328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b307a5573118141f815c54aa1a21fbb6f12c57a80461c9724322ff9797f4fd2`

```dockerfile
```

-	Layers:
	-	`sha256:e225a5930c805acccb0aab301726e174dce92cccbfce4a4b114a6610d9c4cfa4`  
		Last Modified: Wed, 23 Jul 2025 23:12:19 GMT  
		Size: 15.3 KB (15328 bytes)  
		MIME: application/vnd.in-toto+json

## `krakend:2.11`

**does not exist** (yet?)

## `krakend:2.11.0`

**does not exist** (yet?)

## `krakend:latest`

```console
$ docker pull krakend@sha256:639e285e3f6621a3a171c5c5bdf4fc3e2b5b8d016a0bf9c2da6f748e1973e020
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `krakend:latest` - linux; amd64

```console
$ docker pull krakend@sha256:afce54a8bb15f49678ae72f1d9aeb23eb3cc99829e14d177f880e28f875cef27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52586455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:848dd60b8ce67df86f71fd0a55e9ea0c674c2a186041168223815f09444f6b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 22 Jul 2025 17:08:04 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Tue, 22 Jul 2025 17:08:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Tue, 22 Jul 2025 17:08:04 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=0c60cdf57f8ee7d5747d5792b0d4ddc5200b7e6c58948a3ecfdf4acdb9f7ddb4c2f3c168be85c9f2afc12532c9522d80d1c5e9c8ab0fb9320e7b107a059a6299; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=99b799263e05b4cad1b2067552028494e400d22d7a4b62d8c96df5e1b3077f483025726bf4ad332ab353dc7e8930fa5575e62751fc5bcf3e013492d431f50021; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakendio/krakend-ce/releases/download/v2.10.2/krakend_2.10.2_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakendio/krakend-ce/releases/download/v2.10.2/krakend_2.10.2_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Tue, 22 Jul 2025 17:08:04 GMT
WORKDIR /etc/krakend
# Tue, 22 Jul 2025 17:08:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 17:08:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 17:08:04 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Tue, 22 Jul 2025 17:08:04 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eae94c387d75e3e97c70fdc10a5a9076714d50c1dbc442f6657ec833ef0365b`  
		Last Modified: Tue, 22 Jul 2025 17:24:57 GMT  
		Size: 450.1 KB (450056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea206dc7856d95934e7cfb13f3da9535befd3dc59751e0eea1f17759c301474`  
		Last Modified: Tue, 22 Jul 2025 17:25:01 GMT  
		Size: 48.5 MB (48498155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2aa6f4e89734c7bb29aed1bde9fee8507d5911ad34bb0a7a0e5fad85b36f22`  
		Last Modified: Tue, 22 Jul 2025 17:24:57 GMT  
		Size: 642.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:bdee62c78a047449ae7c1f265c15a4ed66c4b12089f668a056229204c39ac035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 KB (15209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586452b72e8560fc4e4691a536445d38b93cd31bd2f719fefa0e464bcf0855bc`

```dockerfile
```

-	Layers:
	-	`sha256:e150a1ec2a3160bf6f4ea3acb14b8827382b948fe96c268101a06474ecf8e7c1`  
		Last Modified: Tue, 22 Jul 2025 20:12:18 GMT  
		Size: 15.2 KB (15209 bytes)  
		MIME: application/vnd.in-toto+json

### `krakend:latest` - linux; arm64 variant v8

```console
$ docker pull krakend@sha256:789cde13d08689696df24f965f18f9cb4b5e314c556549b29413d038536d8e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50605702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277eaa159c0c98bbe8b791b6835f32a13f87957b41de20bf34231ffdd4292207`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 22 Jul 2025 17:08:04 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Tue, 22 Jul 2025 17:08:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Tue, 22 Jul 2025 17:08:04 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=0c60cdf57f8ee7d5747d5792b0d4ddc5200b7e6c58948a3ecfdf4acdb9f7ddb4c2f3c168be85c9f2afc12532c9522d80d1c5e9c8ab0fb9320e7b107a059a6299; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=99b799263e05b4cad1b2067552028494e400d22d7a4b62d8c96df5e1b3077f483025726bf4ad332ab353dc7e8930fa5575e62751fc5bcf3e013492d431f50021; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakendio/krakend-ce/releases/download/v2.10.2/krakend_2.10.2_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakendio/krakend-ce/releases/download/v2.10.2/krakend_2.10.2_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Tue, 22 Jul 2025 17:08:04 GMT
WORKDIR /etc/krakend
# Tue, 22 Jul 2025 17:08:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 17:08:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 17:08:04 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Tue, 22 Jul 2025 17:08:04 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10565e445dbdde4f630b6b91820343bf053438219630d56d27f04fe544a95718`  
		Last Modified: Wed, 23 Jul 2025 19:25:57 GMT  
		Size: 453.4 KB (453414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ecbb898c698017f656de8d8a1aa0aa11fa19549f8966bc6eac599f8daba3cf4`  
		Last Modified: Wed, 23 Jul 2025 19:26:00 GMT  
		Size: 46.2 MB (46164677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93a8fad8e4cdb7180d9027b6195c9c8c2f52c0796b1f204b25640e5de2d3526`  
		Last Modified: Wed, 23 Jul 2025 19:25:57 GMT  
		Size: 642.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:787cddaee97e87f54db3bcbb232f65535a233221e8a396b5f8bf260e6ce4a348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 KB (15328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b307a5573118141f815c54aa1a21fbb6f12c57a80461c9724322ff9797f4fd2`

```dockerfile
```

-	Layers:
	-	`sha256:e225a5930c805acccb0aab301726e174dce92cccbfce4a4b114a6610d9c4cfa4`  
		Last Modified: Wed, 23 Jul 2025 23:12:19 GMT  
		Size: 15.3 KB (15328 bytes)  
		MIME: application/vnd.in-toto+json
