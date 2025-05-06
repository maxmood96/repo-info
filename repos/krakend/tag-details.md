<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `krakend`

-	[`krakend:2`](#krakend2)
-	[`krakend:2.10`](#krakend210)
-	[`krakend:2.10.0`](#krakend2100)
-	[`krakend:latest`](#krakendlatest)

## `krakend:2`

```console
$ docker pull krakend@sha256:3ebd35a9d8c5b517bded0cd4535cbad70f870682cd17bd69ca596c43e1d4d0e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `krakend:2` - linux; amd64

```console
$ docker pull krakend@sha256:d06fb33c26ccea30df537171957e6246802e1e823e3dc2d2bf741d33bd06929e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52552312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b30b16b35e28fb1e2c296bb5d707aad948f3a90f684e78d0a5351cd45ab3ae9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 14:44:31 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Thu, 10 Apr 2025 14:44:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Thu, 10 Apr 2025 14:44:31 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=3ac93a341c88337dd57613d0dbc116f84636b8346185d88fecb0967775e36e923f7696cac5a6ab1be08b530d9b272c737f28b71ae004a29c12cd4ca1c9a950be; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=d4e5b0bccd25694be2fcb77a53d513a7f26536e346dec3efad7badc3d7d6c9eb8209f31e2679959dc806b1605c22169005d4554ac9ca3c2fe24543e79d8a10da; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakendio/krakend-ce/releases/download/v2.9.4/krakend_2.9.4_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakendio/krakend-ce/releases/download/v2.9.4/krakend_2.9.4_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Thu, 10 Apr 2025 14:44:31 GMT
WORKDIR /etc/krakend
# Thu, 10 Apr 2025 14:44:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 14:44:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 14:44:31 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Thu, 10 Apr 2025 14:44:31 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3929b54929a029f195d5732d3a0088758208e37b6c14773ebf49f53292c3d939`  
		Last Modified: Thu, 10 Apr 2025 17:23:12 GMT  
		Size: 462.7 KB (462719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fe095bd83b87926727a3d339efafaa5214c6ba095b049bbb4521252829ec94`  
		Last Modified: Thu, 10 Apr 2025 17:23:13 GMT  
		Size: 48.4 MB (48446672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ef7207237fb78385b45da0fc8779ad856693aaad251e795c6fe553b83a4701`  
		Last Modified: Thu, 10 Apr 2025 17:23:12 GMT  
		Size: 642.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:2` - unknown; unknown

```console
$ docker pull krakend@sha256:ecea3d1ff6713df38b46225ef3ddac8f0614964b9d11c2b9d83eecae427bd891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 KB (15190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6a720a0bbd54645f7d6033420e75577f26f378d2554d0ed368f1306a6696a1`

```dockerfile
```

-	Layers:
	-	`sha256:618915c95b2a0674fee8f76e80271a82d75c2677eaa423165200ac198b80b170`  
		Last Modified: Thu, 10 Apr 2025 17:23:12 GMT  
		Size: 15.2 KB (15190 bytes)  
		MIME: application/vnd.in-toto+json

### `krakend:2` - linux; arm64 variant v8

```console
$ docker pull krakend@sha256:e05c32e7fe71dea7bd6b727b6b0924fabba3ae77a1ba4e9ebb307dc5683339ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50593113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506c92b2fef4c47d0f4d6dbeea5c0fb6370b1f44dfaf12d7654442fece571fbc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 14:44:31 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Thu, 10 Apr 2025 14:44:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Thu, 10 Apr 2025 14:44:31 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=3ac93a341c88337dd57613d0dbc116f84636b8346185d88fecb0967775e36e923f7696cac5a6ab1be08b530d9b272c737f28b71ae004a29c12cd4ca1c9a950be; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=d4e5b0bccd25694be2fcb77a53d513a7f26536e346dec3efad7badc3d7d6c9eb8209f31e2679959dc806b1605c22169005d4554ac9ca3c2fe24543e79d8a10da; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakendio/krakend-ce/releases/download/v2.9.4/krakend_2.9.4_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakendio/krakend-ce/releases/download/v2.9.4/krakend_2.9.4_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Thu, 10 Apr 2025 14:44:31 GMT
WORKDIR /etc/krakend
# Thu, 10 Apr 2025 14:44:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 14:44:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 14:44:31 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Thu, 10 Apr 2025 14:44:31 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4258cd50eab32d7143d502cb1f16a36969069234680b8a863475a5fcc2eb0097`  
		Last Modified: Thu, 10 Apr 2025 17:22:59 GMT  
		Size: 466.5 KB (466451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9d51069d432701eb02a573186e3910fe749e7545dca06d77ab3b4b44d2853f`  
		Last Modified: Thu, 10 Apr 2025 17:23:01 GMT  
		Size: 46.1 MB (46132957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e419e5d77109f34da02d6c15b44989a905d442d6fb22170da3bc026266e2dec8`  
		Last Modified: Thu, 10 Apr 2025 17:22:59 GMT  
		Size: 644.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:2` - unknown; unknown

```console
$ docker pull krakend@sha256:8e17f8a1fb87302b643c657f905c85f0f54e1b57ac1d3e12442e2073e8f99137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 KB (15309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092eeffbda420edab30d16534cd55abab37932a9f276c4463881583bc1c27b6e`

```dockerfile
```

-	Layers:
	-	`sha256:d4ad8cae0cf119bd30c737fc612d1c50e6a0030b4d9b06e99aeac5424ee07b29`  
		Last Modified: Thu, 10 Apr 2025 17:22:59 GMT  
		Size: 15.3 KB (15309 bytes)  
		MIME: application/vnd.in-toto+json

## `krakend:2.10`

**does not exist** (yet?)

## `krakend:2.10.0`

**does not exist** (yet?)

## `krakend:latest`

```console
$ docker pull krakend@sha256:3ebd35a9d8c5b517bded0cd4535cbad70f870682cd17bd69ca596c43e1d4d0e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `krakend:latest` - linux; amd64

```console
$ docker pull krakend@sha256:d06fb33c26ccea30df537171957e6246802e1e823e3dc2d2bf741d33bd06929e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52552312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b30b16b35e28fb1e2c296bb5d707aad948f3a90f684e78d0a5351cd45ab3ae9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 14:44:31 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Thu, 10 Apr 2025 14:44:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Thu, 10 Apr 2025 14:44:31 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=3ac93a341c88337dd57613d0dbc116f84636b8346185d88fecb0967775e36e923f7696cac5a6ab1be08b530d9b272c737f28b71ae004a29c12cd4ca1c9a950be; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=d4e5b0bccd25694be2fcb77a53d513a7f26536e346dec3efad7badc3d7d6c9eb8209f31e2679959dc806b1605c22169005d4554ac9ca3c2fe24543e79d8a10da; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakendio/krakend-ce/releases/download/v2.9.4/krakend_2.9.4_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakendio/krakend-ce/releases/download/v2.9.4/krakend_2.9.4_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Thu, 10 Apr 2025 14:44:31 GMT
WORKDIR /etc/krakend
# Thu, 10 Apr 2025 14:44:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 14:44:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 14:44:31 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Thu, 10 Apr 2025 14:44:31 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3929b54929a029f195d5732d3a0088758208e37b6c14773ebf49f53292c3d939`  
		Last Modified: Thu, 10 Apr 2025 17:23:12 GMT  
		Size: 462.7 KB (462719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fe095bd83b87926727a3d339efafaa5214c6ba095b049bbb4521252829ec94`  
		Last Modified: Thu, 10 Apr 2025 17:23:13 GMT  
		Size: 48.4 MB (48446672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ef7207237fb78385b45da0fc8779ad856693aaad251e795c6fe553b83a4701`  
		Last Modified: Thu, 10 Apr 2025 17:23:12 GMT  
		Size: 642.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:ecea3d1ff6713df38b46225ef3ddac8f0614964b9d11c2b9d83eecae427bd891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 KB (15190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6a720a0bbd54645f7d6033420e75577f26f378d2554d0ed368f1306a6696a1`

```dockerfile
```

-	Layers:
	-	`sha256:618915c95b2a0674fee8f76e80271a82d75c2677eaa423165200ac198b80b170`  
		Last Modified: Thu, 10 Apr 2025 17:23:12 GMT  
		Size: 15.2 KB (15190 bytes)  
		MIME: application/vnd.in-toto+json

### `krakend:latest` - linux; arm64 variant v8

```console
$ docker pull krakend@sha256:e05c32e7fe71dea7bd6b727b6b0924fabba3ae77a1ba4e9ebb307dc5683339ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50593113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506c92b2fef4c47d0f4d6dbeea5c0fb6370b1f44dfaf12d7654442fece571fbc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 14:44:31 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Thu, 10 Apr 2025 14:44:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Thu, 10 Apr 2025 14:44:31 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=3ac93a341c88337dd57613d0dbc116f84636b8346185d88fecb0967775e36e923f7696cac5a6ab1be08b530d9b272c737f28b71ae004a29c12cd4ca1c9a950be; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=d4e5b0bccd25694be2fcb77a53d513a7f26536e346dec3efad7badc3d7d6c9eb8209f31e2679959dc806b1605c22169005d4554ac9ca3c2fe24543e79d8a10da; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakendio/krakend-ce/releases/download/v2.9.4/krakend_2.9.4_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakendio/krakend-ce/releases/download/v2.9.4/krakend_2.9.4_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Thu, 10 Apr 2025 14:44:31 GMT
WORKDIR /etc/krakend
# Thu, 10 Apr 2025 14:44:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 14:44:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 14:44:31 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Thu, 10 Apr 2025 14:44:31 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4258cd50eab32d7143d502cb1f16a36969069234680b8a863475a5fcc2eb0097`  
		Last Modified: Thu, 10 Apr 2025 17:22:59 GMT  
		Size: 466.5 KB (466451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9d51069d432701eb02a573186e3910fe749e7545dca06d77ab3b4b44d2853f`  
		Last Modified: Thu, 10 Apr 2025 17:23:01 GMT  
		Size: 46.1 MB (46132957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e419e5d77109f34da02d6c15b44989a905d442d6fb22170da3bc026266e2dec8`  
		Last Modified: Thu, 10 Apr 2025 17:22:59 GMT  
		Size: 644.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:8e17f8a1fb87302b643c657f905c85f0f54e1b57ac1d3e12442e2073e8f99137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 KB (15309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092eeffbda420edab30d16534cd55abab37932a9f276c4463881583bc1c27b6e`

```dockerfile
```

-	Layers:
	-	`sha256:d4ad8cae0cf119bd30c737fc612d1c50e6a0030b4d9b06e99aeac5424ee07b29`  
		Last Modified: Thu, 10 Apr 2025 17:22:59 GMT  
		Size: 15.3 KB (15309 bytes)  
		MIME: application/vnd.in-toto+json
