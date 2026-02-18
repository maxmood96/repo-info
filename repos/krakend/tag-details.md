<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `krakend`

-	[`krakend:2`](#krakend2)
-	[`krakend:2.13`](#krakend213)
-	[`krakend:2.13.1`](#krakend2131)
-	[`krakend:latest`](#krakendlatest)

## `krakend:2`

```console
$ docker pull krakend@sha256:4846fb545f8434b4a884091e45738d14bb3fb66a2d4c4bfc3b77a84a16ca94d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `krakend:2` - linux; amd64

```console
$ docker pull krakend@sha256:29e257cf1f261dd2dbb013625f8ae3ff471630fbf995a6adbee8685c306d45f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52174819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5146b8a5c1295d85b80f7a8b715a101150eff34a100301d626f40cd4de8e81f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 18:36:11 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Wed, 18 Feb 2026 18:36:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Wed, 18 Feb 2026 18:36:16 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=fdef1657bc99e0a8082d508cce6c411089e6cbacc4ac069b75ef35dea37bf701a9b5d7fbdc31a06dedba0a9d4560d5f6b06fa0a45feb1feaa71f716f97c7c290; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=ab15cad55ff915751a57d6fd9d5d862eb785226f23a4c0dd4e60d736a588d71525b3c1d494c478e94761f53318838ff55f66550a26c4a23150675840929b96f2; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakend/krakend-ce/releases/download/v2.13.1/krakend_2.13.1_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakend/krakend-ce/releases/download/v2.13.1/krakend_2.13.1_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Wed, 18 Feb 2026 18:36:16 GMT
WORKDIR /etc/krakend
# Wed, 18 Feb 2026 18:36:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 18:36:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 18:36:16 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Wed, 18 Feb 2026 18:36:16 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363f5dac1003908fc3facdf3c2e24cf60e39e4b0ef1c7eb6d65466767d67b11b`  
		Last Modified: Wed, 18 Feb 2026 18:36:23 GMT  
		Size: 463.4 KB (463433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbcb7815902e5dd1b72909e76e0d203f80caecefc6ff301988b9d91a4ac043c`  
		Last Modified: Wed, 18 Feb 2026 18:36:25 GMT  
		Size: 47.8 MB (47848889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12874f71aaab449b09d639f052b8b922e2fdb154a823f311b57c93bc02a00c27`  
		Last Modified: Wed, 18 Feb 2026 18:36:23 GMT  
		Size: 644.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:2` - unknown; unknown

```console
$ docker pull krakend@sha256:3223c84f6794066991674bb04d4d677b2902a6e17944ffd5f755e0ff0bb80955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 KB (15142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761c72a004fc74609a0255eafa89ddcb1a85e7dc10b77fc0e43de5b8d38606ba`

```dockerfile
```

-	Layers:
	-	`sha256:c19e7acba48a57b2a43e885f1a00594e84e964f1a8a448b3120bba8dbebad591`  
		Last Modified: Wed, 18 Feb 2026 18:36:23 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `krakend:2` - linux; arm64 variant v8

```console
$ docker pull krakend@sha256:6fc852bf25802730a6392778b60c41cc7a9d7ec556af3685f805f894e5bf63d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49758845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8acf2b1cdc96b2886c5576a817334f3cb30e2fe0a5897a4ca87834cf07302915`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 18:36:06 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Wed, 18 Feb 2026 18:36:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Wed, 18 Feb 2026 18:36:11 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=fdef1657bc99e0a8082d508cce6c411089e6cbacc4ac069b75ef35dea37bf701a9b5d7fbdc31a06dedba0a9d4560d5f6b06fa0a45feb1feaa71f716f97c7c290; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=ab15cad55ff915751a57d6fd9d5d862eb785226f23a4c0dd4e60d736a588d71525b3c1d494c478e94761f53318838ff55f66550a26c4a23150675840929b96f2; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakend/krakend-ce/releases/download/v2.13.1/krakend_2.13.1_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakend/krakend-ce/releases/download/v2.13.1/krakend_2.13.1_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Wed, 18 Feb 2026 18:36:11 GMT
WORKDIR /etc/krakend
# Wed, 18 Feb 2026 18:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 18:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 18:36:11 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Wed, 18 Feb 2026 18:36:11 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5137884a5ef37f05bf7ae774ac218e0390cc993c437ee80f77b0b7d3feffc5a9`  
		Last Modified: Wed, 18 Feb 2026 18:36:19 GMT  
		Size: 467.7 KB (467674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c62fd4ba6c4f560ac05d8adf9c8ca5af5670b76c1e0ac41ed6ec31a1c31ca6d`  
		Last Modified: Wed, 18 Feb 2026 18:36:20 GMT  
		Size: 45.1 MB (45093404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de5d2ee8ed62a58a78483a2b8ca8392df8b6015b4577b2d52558b54be140650`  
		Last Modified: Wed, 18 Feb 2026 18:36:19 GMT  
		Size: 644.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:2` - unknown; unknown

```console
$ docker pull krakend@sha256:fcb58bc84303ec4fd956f351d7f2ecd6ab660b174b19a9b8cb46c385ec28785e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 KB (15261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee50167d0ddca6923810e00a7ecacbc4916f5e17286917ee5cc4a0a219f10a2`

```dockerfile
```

-	Layers:
	-	`sha256:c5ae125897b5fb4ee00ae212b5353f76df5a4a3430aa2edc85316e80fab172e2`  
		Last Modified: Wed, 18 Feb 2026 18:36:18 GMT  
		Size: 15.3 KB (15261 bytes)  
		MIME: application/vnd.in-toto+json

## `krakend:2.13`

```console
$ docker pull krakend@sha256:4846fb545f8434b4a884091e45738d14bb3fb66a2d4c4bfc3b77a84a16ca94d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `krakend:2.13` - linux; amd64

```console
$ docker pull krakend@sha256:29e257cf1f261dd2dbb013625f8ae3ff471630fbf995a6adbee8685c306d45f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52174819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5146b8a5c1295d85b80f7a8b715a101150eff34a100301d626f40cd4de8e81f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 18:36:11 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Wed, 18 Feb 2026 18:36:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Wed, 18 Feb 2026 18:36:16 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=fdef1657bc99e0a8082d508cce6c411089e6cbacc4ac069b75ef35dea37bf701a9b5d7fbdc31a06dedba0a9d4560d5f6b06fa0a45feb1feaa71f716f97c7c290; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=ab15cad55ff915751a57d6fd9d5d862eb785226f23a4c0dd4e60d736a588d71525b3c1d494c478e94761f53318838ff55f66550a26c4a23150675840929b96f2; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakend/krakend-ce/releases/download/v2.13.1/krakend_2.13.1_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakend/krakend-ce/releases/download/v2.13.1/krakend_2.13.1_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Wed, 18 Feb 2026 18:36:16 GMT
WORKDIR /etc/krakend
# Wed, 18 Feb 2026 18:36:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 18:36:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 18:36:16 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Wed, 18 Feb 2026 18:36:16 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363f5dac1003908fc3facdf3c2e24cf60e39e4b0ef1c7eb6d65466767d67b11b`  
		Last Modified: Wed, 18 Feb 2026 18:36:23 GMT  
		Size: 463.4 KB (463433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbcb7815902e5dd1b72909e76e0d203f80caecefc6ff301988b9d91a4ac043c`  
		Last Modified: Wed, 18 Feb 2026 18:36:25 GMT  
		Size: 47.8 MB (47848889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12874f71aaab449b09d639f052b8b922e2fdb154a823f311b57c93bc02a00c27`  
		Last Modified: Wed, 18 Feb 2026 18:36:23 GMT  
		Size: 644.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:2.13` - unknown; unknown

```console
$ docker pull krakend@sha256:3223c84f6794066991674bb04d4d677b2902a6e17944ffd5f755e0ff0bb80955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 KB (15142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761c72a004fc74609a0255eafa89ddcb1a85e7dc10b77fc0e43de5b8d38606ba`

```dockerfile
```

-	Layers:
	-	`sha256:c19e7acba48a57b2a43e885f1a00594e84e964f1a8a448b3120bba8dbebad591`  
		Last Modified: Wed, 18 Feb 2026 18:36:23 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `krakend:2.13` - linux; arm64 variant v8

```console
$ docker pull krakend@sha256:6fc852bf25802730a6392778b60c41cc7a9d7ec556af3685f805f894e5bf63d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49758845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8acf2b1cdc96b2886c5576a817334f3cb30e2fe0a5897a4ca87834cf07302915`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 18:36:06 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Wed, 18 Feb 2026 18:36:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Wed, 18 Feb 2026 18:36:11 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=fdef1657bc99e0a8082d508cce6c411089e6cbacc4ac069b75ef35dea37bf701a9b5d7fbdc31a06dedba0a9d4560d5f6b06fa0a45feb1feaa71f716f97c7c290; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=ab15cad55ff915751a57d6fd9d5d862eb785226f23a4c0dd4e60d736a588d71525b3c1d494c478e94761f53318838ff55f66550a26c4a23150675840929b96f2; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakend/krakend-ce/releases/download/v2.13.1/krakend_2.13.1_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakend/krakend-ce/releases/download/v2.13.1/krakend_2.13.1_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Wed, 18 Feb 2026 18:36:11 GMT
WORKDIR /etc/krakend
# Wed, 18 Feb 2026 18:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 18:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 18:36:11 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Wed, 18 Feb 2026 18:36:11 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5137884a5ef37f05bf7ae774ac218e0390cc993c437ee80f77b0b7d3feffc5a9`  
		Last Modified: Wed, 18 Feb 2026 18:36:19 GMT  
		Size: 467.7 KB (467674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c62fd4ba6c4f560ac05d8adf9c8ca5af5670b76c1e0ac41ed6ec31a1c31ca6d`  
		Last Modified: Wed, 18 Feb 2026 18:36:20 GMT  
		Size: 45.1 MB (45093404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de5d2ee8ed62a58a78483a2b8ca8392df8b6015b4577b2d52558b54be140650`  
		Last Modified: Wed, 18 Feb 2026 18:36:19 GMT  
		Size: 644.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:2.13` - unknown; unknown

```console
$ docker pull krakend@sha256:fcb58bc84303ec4fd956f351d7f2ecd6ab660b174b19a9b8cb46c385ec28785e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 KB (15261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee50167d0ddca6923810e00a7ecacbc4916f5e17286917ee5cc4a0a219f10a2`

```dockerfile
```

-	Layers:
	-	`sha256:c5ae125897b5fb4ee00ae212b5353f76df5a4a3430aa2edc85316e80fab172e2`  
		Last Modified: Wed, 18 Feb 2026 18:36:18 GMT  
		Size: 15.3 KB (15261 bytes)  
		MIME: application/vnd.in-toto+json

## `krakend:2.13.1`

```console
$ docker pull krakend@sha256:4846fb545f8434b4a884091e45738d14bb3fb66a2d4c4bfc3b77a84a16ca94d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `krakend:2.13.1` - linux; amd64

```console
$ docker pull krakend@sha256:29e257cf1f261dd2dbb013625f8ae3ff471630fbf995a6adbee8685c306d45f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52174819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5146b8a5c1295d85b80f7a8b715a101150eff34a100301d626f40cd4de8e81f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 18:36:11 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Wed, 18 Feb 2026 18:36:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Wed, 18 Feb 2026 18:36:16 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=fdef1657bc99e0a8082d508cce6c411089e6cbacc4ac069b75ef35dea37bf701a9b5d7fbdc31a06dedba0a9d4560d5f6b06fa0a45feb1feaa71f716f97c7c290; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=ab15cad55ff915751a57d6fd9d5d862eb785226f23a4c0dd4e60d736a588d71525b3c1d494c478e94761f53318838ff55f66550a26c4a23150675840929b96f2; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakend/krakend-ce/releases/download/v2.13.1/krakend_2.13.1_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakend/krakend-ce/releases/download/v2.13.1/krakend_2.13.1_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Wed, 18 Feb 2026 18:36:16 GMT
WORKDIR /etc/krakend
# Wed, 18 Feb 2026 18:36:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 18:36:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 18:36:16 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Wed, 18 Feb 2026 18:36:16 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363f5dac1003908fc3facdf3c2e24cf60e39e4b0ef1c7eb6d65466767d67b11b`  
		Last Modified: Wed, 18 Feb 2026 18:36:23 GMT  
		Size: 463.4 KB (463433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbcb7815902e5dd1b72909e76e0d203f80caecefc6ff301988b9d91a4ac043c`  
		Last Modified: Wed, 18 Feb 2026 18:36:25 GMT  
		Size: 47.8 MB (47848889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12874f71aaab449b09d639f052b8b922e2fdb154a823f311b57c93bc02a00c27`  
		Last Modified: Wed, 18 Feb 2026 18:36:23 GMT  
		Size: 644.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:2.13.1` - unknown; unknown

```console
$ docker pull krakend@sha256:3223c84f6794066991674bb04d4d677b2902a6e17944ffd5f755e0ff0bb80955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 KB (15142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761c72a004fc74609a0255eafa89ddcb1a85e7dc10b77fc0e43de5b8d38606ba`

```dockerfile
```

-	Layers:
	-	`sha256:c19e7acba48a57b2a43e885f1a00594e84e964f1a8a448b3120bba8dbebad591`  
		Last Modified: Wed, 18 Feb 2026 18:36:23 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `krakend:2.13.1` - linux; arm64 variant v8

```console
$ docker pull krakend@sha256:6fc852bf25802730a6392778b60c41cc7a9d7ec556af3685f805f894e5bf63d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49758845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8acf2b1cdc96b2886c5576a817334f3cb30e2fe0a5897a4ca87834cf07302915`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 18:36:06 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Wed, 18 Feb 2026 18:36:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Wed, 18 Feb 2026 18:36:11 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=fdef1657bc99e0a8082d508cce6c411089e6cbacc4ac069b75ef35dea37bf701a9b5d7fbdc31a06dedba0a9d4560d5f6b06fa0a45feb1feaa71f716f97c7c290; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=ab15cad55ff915751a57d6fd9d5d862eb785226f23a4c0dd4e60d736a588d71525b3c1d494c478e94761f53318838ff55f66550a26c4a23150675840929b96f2; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakend/krakend-ce/releases/download/v2.13.1/krakend_2.13.1_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakend/krakend-ce/releases/download/v2.13.1/krakend_2.13.1_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Wed, 18 Feb 2026 18:36:11 GMT
WORKDIR /etc/krakend
# Wed, 18 Feb 2026 18:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 18:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 18:36:11 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Wed, 18 Feb 2026 18:36:11 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5137884a5ef37f05bf7ae774ac218e0390cc993c437ee80f77b0b7d3feffc5a9`  
		Last Modified: Wed, 18 Feb 2026 18:36:19 GMT  
		Size: 467.7 KB (467674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c62fd4ba6c4f560ac05d8adf9c8ca5af5670b76c1e0ac41ed6ec31a1c31ca6d`  
		Last Modified: Wed, 18 Feb 2026 18:36:20 GMT  
		Size: 45.1 MB (45093404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de5d2ee8ed62a58a78483a2b8ca8392df8b6015b4577b2d52558b54be140650`  
		Last Modified: Wed, 18 Feb 2026 18:36:19 GMT  
		Size: 644.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:2.13.1` - unknown; unknown

```console
$ docker pull krakend@sha256:fcb58bc84303ec4fd956f351d7f2ecd6ab660b174b19a9b8cb46c385ec28785e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 KB (15261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee50167d0ddca6923810e00a7ecacbc4916f5e17286917ee5cc4a0a219f10a2`

```dockerfile
```

-	Layers:
	-	`sha256:c5ae125897b5fb4ee00ae212b5353f76df5a4a3430aa2edc85316e80fab172e2`  
		Last Modified: Wed, 18 Feb 2026 18:36:18 GMT  
		Size: 15.3 KB (15261 bytes)  
		MIME: application/vnd.in-toto+json

## `krakend:latest`

```console
$ docker pull krakend@sha256:4846fb545f8434b4a884091e45738d14bb3fb66a2d4c4bfc3b77a84a16ca94d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `krakend:latest` - linux; amd64

```console
$ docker pull krakend@sha256:29e257cf1f261dd2dbb013625f8ae3ff471630fbf995a6adbee8685c306d45f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52174819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5146b8a5c1295d85b80f7a8b715a101150eff34a100301d626f40cd4de8e81f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 18:36:11 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Wed, 18 Feb 2026 18:36:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Wed, 18 Feb 2026 18:36:16 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=fdef1657bc99e0a8082d508cce6c411089e6cbacc4ac069b75ef35dea37bf701a9b5d7fbdc31a06dedba0a9d4560d5f6b06fa0a45feb1feaa71f716f97c7c290; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=ab15cad55ff915751a57d6fd9d5d862eb785226f23a4c0dd4e60d736a588d71525b3c1d494c478e94761f53318838ff55f66550a26c4a23150675840929b96f2; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakend/krakend-ce/releases/download/v2.13.1/krakend_2.13.1_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakend/krakend-ce/releases/download/v2.13.1/krakend_2.13.1_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Wed, 18 Feb 2026 18:36:16 GMT
WORKDIR /etc/krakend
# Wed, 18 Feb 2026 18:36:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 18:36:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 18:36:16 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Wed, 18 Feb 2026 18:36:16 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363f5dac1003908fc3facdf3c2e24cf60e39e4b0ef1c7eb6d65466767d67b11b`  
		Last Modified: Wed, 18 Feb 2026 18:36:23 GMT  
		Size: 463.4 KB (463433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbcb7815902e5dd1b72909e76e0d203f80caecefc6ff301988b9d91a4ac043c`  
		Last Modified: Wed, 18 Feb 2026 18:36:25 GMT  
		Size: 47.8 MB (47848889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12874f71aaab449b09d639f052b8b922e2fdb154a823f311b57c93bc02a00c27`  
		Last Modified: Wed, 18 Feb 2026 18:36:23 GMT  
		Size: 644.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:3223c84f6794066991674bb04d4d677b2902a6e17944ffd5f755e0ff0bb80955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 KB (15142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761c72a004fc74609a0255eafa89ddcb1a85e7dc10b77fc0e43de5b8d38606ba`

```dockerfile
```

-	Layers:
	-	`sha256:c19e7acba48a57b2a43e885f1a00594e84e964f1a8a448b3120bba8dbebad591`  
		Last Modified: Wed, 18 Feb 2026 18:36:23 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `krakend:latest` - linux; arm64 variant v8

```console
$ docker pull krakend@sha256:6fc852bf25802730a6392778b60c41cc7a9d7ec556af3685f805f894e5bf63d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49758845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8acf2b1cdc96b2886c5576a817334f3cb30e2fe0a5897a4ca87834cf07302915`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 18:36:06 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Wed, 18 Feb 2026 18:36:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Wed, 18 Feb 2026 18:36:11 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=fdef1657bc99e0a8082d508cce6c411089e6cbacc4ac069b75ef35dea37bf701a9b5d7fbdc31a06dedba0a9d4560d5f6b06fa0a45feb1feaa71f716f97c7c290; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=ab15cad55ff915751a57d6fd9d5d862eb785226f23a4c0dd4e60d736a588d71525b3c1d494c478e94761f53318838ff55f66550a26c4a23150675840929b96f2; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakend/krakend-ce/releases/download/v2.13.1/krakend_2.13.1_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakend/krakend-ce/releases/download/v2.13.1/krakend_2.13.1_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Wed, 18 Feb 2026 18:36:11 GMT
WORKDIR /etc/krakend
# Wed, 18 Feb 2026 18:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 18:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 18:36:11 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Wed, 18 Feb 2026 18:36:11 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5137884a5ef37f05bf7ae774ac218e0390cc993c437ee80f77b0b7d3feffc5a9`  
		Last Modified: Wed, 18 Feb 2026 18:36:19 GMT  
		Size: 467.7 KB (467674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c62fd4ba6c4f560ac05d8adf9c8ca5af5670b76c1e0ac41ed6ec31a1c31ca6d`  
		Last Modified: Wed, 18 Feb 2026 18:36:20 GMT  
		Size: 45.1 MB (45093404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de5d2ee8ed62a58a78483a2b8ca8392df8b6015b4577b2d52558b54be140650`  
		Last Modified: Wed, 18 Feb 2026 18:36:19 GMT  
		Size: 644.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:fcb58bc84303ec4fd956f351d7f2ecd6ab660b174b19a9b8cb46c385ec28785e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 KB (15261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee50167d0ddca6923810e00a7ecacbc4916f5e17286917ee5cc4a0a219f10a2`

```dockerfile
```

-	Layers:
	-	`sha256:c5ae125897b5fb4ee00ae212b5353f76df5a4a3430aa2edc85316e80fab172e2`  
		Last Modified: Wed, 18 Feb 2026 18:36:18 GMT  
		Size: 15.3 KB (15261 bytes)  
		MIME: application/vnd.in-toto+json
