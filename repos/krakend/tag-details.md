<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `krakend`

-	[`krakend:2`](#krakend2)
-	[`krakend:2.13`](#krakend213)
-	[`krakend:2.13.2`](#krakend2132)
-	[`krakend:latest`](#krakendlatest)

## `krakend:2`

```console
$ docker pull krakend@sha256:7165217c5ee5f3fe02aa2a765ca9356035064cb20e62d5e38d6780558e11c033
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `krakend:2` - linux; amd64

```console
$ docker pull krakend@sha256:8979c9fe91437ded27df5b76d49f79ad57f1e3aaf85dc131ac7bca08e6e213b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59396520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1605babadc400b5e064f824f69cba6907694f3bbda43349ba71524f5fbf465ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:35:21 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Mon, 09 Mar 2026 18:35:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Mon, 09 Mar 2026 18:35:26 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=de4bd800546e13a749e5c1254d45a9dc4d1bd37e76647995cc7e62d1b0e025a0be00685c8a7a80c1b412ffbf9d33ec32a1298162ed368d436f77cfe1b17a69c0; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=50dedb294d047fc351b37de66349ba086896aa5e899f60804cb52c1a91c83a4fa43b08477d62bcb4da8650f74204bff79a9bc42655103e20f9c9f82bd26bdff6; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakend/krakend-ce/releases/download/v2.13.2/krakend_2.13.2_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakend/krakend-ce/releases/download/v2.13.2/krakend_2.13.2_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Mon, 09 Mar 2026 18:35:26 GMT
WORKDIR /etc/krakend
# Mon, 09 Mar 2026 18:35:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 18:35:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:35:27 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Mon, 09 Mar 2026 18:35:27 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a8b1e176527ad5d76e2f073d84e7cfbe0db32a1e1b1b300ad6ddca8eb7e491`  
		Last Modified: Mon, 09 Mar 2026 18:35:34 GMT  
		Size: 463.2 KB (463249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5b3516e1496f6574a9d6ac86dac6228155798967617f7845b34bd812955821`  
		Last Modified: Mon, 09 Mar 2026 18:35:36 GMT  
		Size: 55.1 MB (55070772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd22d43a8e1a9ac9d6cd8971d4880022bfdd02c060e9362ea1f4129177b060ad`  
		Last Modified: Mon, 09 Mar 2026 18:35:34 GMT  
		Size: 646.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:2` - unknown; unknown

```console
$ docker pull krakend@sha256:af50018bbf9f9a5a93cd555d68f7b17b2ee7b5a6413eb25a6016cd1a02027ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 KB (15142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0c22e58d12006b9ddb4ac59d554171ad41b9b457b297ac5b9f2c7e8063faad`

```dockerfile
```

-	Layers:
	-	`sha256:de32c00fb3f9020008f3cbfaff95d1a1067a51149f217a3df4b37acd116e6e51`  
		Last Modified: Mon, 09 Mar 2026 18:35:34 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `krakend:2` - linux; arm64 variant v8

```console
$ docker pull krakend@sha256:f98656362ce6138f89f79a7e9bd503d5ae5bce74c1eac310444274b296453a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56396756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ca5e16fc88f89da68f18aa41118d444a307368707efa67224ca7230a8d3e4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:03:27 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Mon, 09 Mar 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Mon, 09 Mar 2026 18:03:33 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=de4bd800546e13a749e5c1254d45a9dc4d1bd37e76647995cc7e62d1b0e025a0be00685c8a7a80c1b412ffbf9d33ec32a1298162ed368d436f77cfe1b17a69c0; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=50dedb294d047fc351b37de66349ba086896aa5e899f60804cb52c1a91c83a4fa43b08477d62bcb4da8650f74204bff79a9bc42655103e20f9c9f82bd26bdff6; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakend/krakend-ce/releases/download/v2.13.2/krakend_2.13.2_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakend/krakend-ce/releases/download/v2.13.2/krakend_2.13.2_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Mon, 09 Mar 2026 18:03:33 GMT
WORKDIR /etc/krakend
# Mon, 09 Mar 2026 18:03:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 18:03:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:03:33 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Mon, 09 Mar 2026 18:03:33 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8d52811a974a2d0fcb72df27f5467a1a6487a25c85e826eaf2cbbcb6c03ab8`  
		Last Modified: Mon, 09 Mar 2026 18:03:41 GMT  
		Size: 467.4 KB (467430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4c012d76b5187c9c13c34d0a41a07cf3266f2e3d230ce75f578ad1eaf41a70`  
		Last Modified: Mon, 09 Mar 2026 18:03:42 GMT  
		Size: 51.7 MB (51731561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4754d457341846e0b67039ca87f859d68f1df61050a736ef59de1075880f207`  
		Last Modified: Mon, 09 Mar 2026 18:03:41 GMT  
		Size: 642.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:2` - unknown; unknown

```console
$ docker pull krakend@sha256:c3869458a194f581c993cdef8c721316ad172ad9d2a6484b66a26147770de730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 KB (15261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d6e88a0698c8b3cf4d37b003575475cbd6ead1649dd67209dcef47500f41cf`

```dockerfile
```

-	Layers:
	-	`sha256:d6deb23c6e8a51834578d29ab6aa5ed313a513da449cc5652652d44385aaae4f`  
		Last Modified: Mon, 09 Mar 2026 18:03:41 GMT  
		Size: 15.3 KB (15261 bytes)  
		MIME: application/vnd.in-toto+json

## `krakend:2.13`

```console
$ docker pull krakend@sha256:7165217c5ee5f3fe02aa2a765ca9356035064cb20e62d5e38d6780558e11c033
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `krakend:2.13` - linux; amd64

```console
$ docker pull krakend@sha256:8979c9fe91437ded27df5b76d49f79ad57f1e3aaf85dc131ac7bca08e6e213b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59396520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1605babadc400b5e064f824f69cba6907694f3bbda43349ba71524f5fbf465ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:35:21 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Mon, 09 Mar 2026 18:35:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Mon, 09 Mar 2026 18:35:26 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=de4bd800546e13a749e5c1254d45a9dc4d1bd37e76647995cc7e62d1b0e025a0be00685c8a7a80c1b412ffbf9d33ec32a1298162ed368d436f77cfe1b17a69c0; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=50dedb294d047fc351b37de66349ba086896aa5e899f60804cb52c1a91c83a4fa43b08477d62bcb4da8650f74204bff79a9bc42655103e20f9c9f82bd26bdff6; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakend/krakend-ce/releases/download/v2.13.2/krakend_2.13.2_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakend/krakend-ce/releases/download/v2.13.2/krakend_2.13.2_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Mon, 09 Mar 2026 18:35:26 GMT
WORKDIR /etc/krakend
# Mon, 09 Mar 2026 18:35:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 18:35:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:35:27 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Mon, 09 Mar 2026 18:35:27 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a8b1e176527ad5d76e2f073d84e7cfbe0db32a1e1b1b300ad6ddca8eb7e491`  
		Last Modified: Mon, 09 Mar 2026 18:35:34 GMT  
		Size: 463.2 KB (463249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5b3516e1496f6574a9d6ac86dac6228155798967617f7845b34bd812955821`  
		Last Modified: Mon, 09 Mar 2026 18:35:36 GMT  
		Size: 55.1 MB (55070772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd22d43a8e1a9ac9d6cd8971d4880022bfdd02c060e9362ea1f4129177b060ad`  
		Last Modified: Mon, 09 Mar 2026 18:35:34 GMT  
		Size: 646.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:2.13` - unknown; unknown

```console
$ docker pull krakend@sha256:af50018bbf9f9a5a93cd555d68f7b17b2ee7b5a6413eb25a6016cd1a02027ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 KB (15142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0c22e58d12006b9ddb4ac59d554171ad41b9b457b297ac5b9f2c7e8063faad`

```dockerfile
```

-	Layers:
	-	`sha256:de32c00fb3f9020008f3cbfaff95d1a1067a51149f217a3df4b37acd116e6e51`  
		Last Modified: Mon, 09 Mar 2026 18:35:34 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `krakend:2.13` - linux; arm64 variant v8

```console
$ docker pull krakend@sha256:f98656362ce6138f89f79a7e9bd503d5ae5bce74c1eac310444274b296453a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56396756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ca5e16fc88f89da68f18aa41118d444a307368707efa67224ca7230a8d3e4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:03:27 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Mon, 09 Mar 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Mon, 09 Mar 2026 18:03:33 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=de4bd800546e13a749e5c1254d45a9dc4d1bd37e76647995cc7e62d1b0e025a0be00685c8a7a80c1b412ffbf9d33ec32a1298162ed368d436f77cfe1b17a69c0; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=50dedb294d047fc351b37de66349ba086896aa5e899f60804cb52c1a91c83a4fa43b08477d62bcb4da8650f74204bff79a9bc42655103e20f9c9f82bd26bdff6; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakend/krakend-ce/releases/download/v2.13.2/krakend_2.13.2_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakend/krakend-ce/releases/download/v2.13.2/krakend_2.13.2_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Mon, 09 Mar 2026 18:03:33 GMT
WORKDIR /etc/krakend
# Mon, 09 Mar 2026 18:03:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 18:03:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:03:33 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Mon, 09 Mar 2026 18:03:33 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8d52811a974a2d0fcb72df27f5467a1a6487a25c85e826eaf2cbbcb6c03ab8`  
		Last Modified: Mon, 09 Mar 2026 18:03:41 GMT  
		Size: 467.4 KB (467430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4c012d76b5187c9c13c34d0a41a07cf3266f2e3d230ce75f578ad1eaf41a70`  
		Last Modified: Mon, 09 Mar 2026 18:03:42 GMT  
		Size: 51.7 MB (51731561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4754d457341846e0b67039ca87f859d68f1df61050a736ef59de1075880f207`  
		Last Modified: Mon, 09 Mar 2026 18:03:41 GMT  
		Size: 642.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:2.13` - unknown; unknown

```console
$ docker pull krakend@sha256:c3869458a194f581c993cdef8c721316ad172ad9d2a6484b66a26147770de730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 KB (15261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d6e88a0698c8b3cf4d37b003575475cbd6ead1649dd67209dcef47500f41cf`

```dockerfile
```

-	Layers:
	-	`sha256:d6deb23c6e8a51834578d29ab6aa5ed313a513da449cc5652652d44385aaae4f`  
		Last Modified: Mon, 09 Mar 2026 18:03:41 GMT  
		Size: 15.3 KB (15261 bytes)  
		MIME: application/vnd.in-toto+json

## `krakend:2.13.2`

```console
$ docker pull krakend@sha256:7165217c5ee5f3fe02aa2a765ca9356035064cb20e62d5e38d6780558e11c033
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `krakend:2.13.2` - linux; amd64

```console
$ docker pull krakend@sha256:8979c9fe91437ded27df5b76d49f79ad57f1e3aaf85dc131ac7bca08e6e213b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59396520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1605babadc400b5e064f824f69cba6907694f3bbda43349ba71524f5fbf465ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:35:21 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Mon, 09 Mar 2026 18:35:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Mon, 09 Mar 2026 18:35:26 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=de4bd800546e13a749e5c1254d45a9dc4d1bd37e76647995cc7e62d1b0e025a0be00685c8a7a80c1b412ffbf9d33ec32a1298162ed368d436f77cfe1b17a69c0; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=50dedb294d047fc351b37de66349ba086896aa5e899f60804cb52c1a91c83a4fa43b08477d62bcb4da8650f74204bff79a9bc42655103e20f9c9f82bd26bdff6; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakend/krakend-ce/releases/download/v2.13.2/krakend_2.13.2_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakend/krakend-ce/releases/download/v2.13.2/krakend_2.13.2_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Mon, 09 Mar 2026 18:35:26 GMT
WORKDIR /etc/krakend
# Mon, 09 Mar 2026 18:35:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 18:35:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:35:27 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Mon, 09 Mar 2026 18:35:27 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a8b1e176527ad5d76e2f073d84e7cfbe0db32a1e1b1b300ad6ddca8eb7e491`  
		Last Modified: Mon, 09 Mar 2026 18:35:34 GMT  
		Size: 463.2 KB (463249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5b3516e1496f6574a9d6ac86dac6228155798967617f7845b34bd812955821`  
		Last Modified: Mon, 09 Mar 2026 18:35:36 GMT  
		Size: 55.1 MB (55070772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd22d43a8e1a9ac9d6cd8971d4880022bfdd02c060e9362ea1f4129177b060ad`  
		Last Modified: Mon, 09 Mar 2026 18:35:34 GMT  
		Size: 646.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:2.13.2` - unknown; unknown

```console
$ docker pull krakend@sha256:af50018bbf9f9a5a93cd555d68f7b17b2ee7b5a6413eb25a6016cd1a02027ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 KB (15142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0c22e58d12006b9ddb4ac59d554171ad41b9b457b297ac5b9f2c7e8063faad`

```dockerfile
```

-	Layers:
	-	`sha256:de32c00fb3f9020008f3cbfaff95d1a1067a51149f217a3df4b37acd116e6e51`  
		Last Modified: Mon, 09 Mar 2026 18:35:34 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `krakend:2.13.2` - linux; arm64 variant v8

```console
$ docker pull krakend@sha256:f98656362ce6138f89f79a7e9bd503d5ae5bce74c1eac310444274b296453a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56396756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ca5e16fc88f89da68f18aa41118d444a307368707efa67224ca7230a8d3e4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:03:27 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Mon, 09 Mar 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Mon, 09 Mar 2026 18:03:33 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=de4bd800546e13a749e5c1254d45a9dc4d1bd37e76647995cc7e62d1b0e025a0be00685c8a7a80c1b412ffbf9d33ec32a1298162ed368d436f77cfe1b17a69c0; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=50dedb294d047fc351b37de66349ba086896aa5e899f60804cb52c1a91c83a4fa43b08477d62bcb4da8650f74204bff79a9bc42655103e20f9c9f82bd26bdff6; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakend/krakend-ce/releases/download/v2.13.2/krakend_2.13.2_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakend/krakend-ce/releases/download/v2.13.2/krakend_2.13.2_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Mon, 09 Mar 2026 18:03:33 GMT
WORKDIR /etc/krakend
# Mon, 09 Mar 2026 18:03:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 18:03:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:03:33 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Mon, 09 Mar 2026 18:03:33 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8d52811a974a2d0fcb72df27f5467a1a6487a25c85e826eaf2cbbcb6c03ab8`  
		Last Modified: Mon, 09 Mar 2026 18:03:41 GMT  
		Size: 467.4 KB (467430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4c012d76b5187c9c13c34d0a41a07cf3266f2e3d230ce75f578ad1eaf41a70`  
		Last Modified: Mon, 09 Mar 2026 18:03:42 GMT  
		Size: 51.7 MB (51731561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4754d457341846e0b67039ca87f859d68f1df61050a736ef59de1075880f207`  
		Last Modified: Mon, 09 Mar 2026 18:03:41 GMT  
		Size: 642.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:2.13.2` - unknown; unknown

```console
$ docker pull krakend@sha256:c3869458a194f581c993cdef8c721316ad172ad9d2a6484b66a26147770de730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 KB (15261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d6e88a0698c8b3cf4d37b003575475cbd6ead1649dd67209dcef47500f41cf`

```dockerfile
```

-	Layers:
	-	`sha256:d6deb23c6e8a51834578d29ab6aa5ed313a513da449cc5652652d44385aaae4f`  
		Last Modified: Mon, 09 Mar 2026 18:03:41 GMT  
		Size: 15.3 KB (15261 bytes)  
		MIME: application/vnd.in-toto+json

## `krakend:latest`

```console
$ docker pull krakend@sha256:7165217c5ee5f3fe02aa2a765ca9356035064cb20e62d5e38d6780558e11c033
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `krakend:latest` - linux; amd64

```console
$ docker pull krakend@sha256:8979c9fe91437ded27df5b76d49f79ad57f1e3aaf85dc131ac7bca08e6e213b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59396520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1605babadc400b5e064f824f69cba6907694f3bbda43349ba71524f5fbf465ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:35:21 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Mon, 09 Mar 2026 18:35:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Mon, 09 Mar 2026 18:35:26 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=de4bd800546e13a749e5c1254d45a9dc4d1bd37e76647995cc7e62d1b0e025a0be00685c8a7a80c1b412ffbf9d33ec32a1298162ed368d436f77cfe1b17a69c0; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=50dedb294d047fc351b37de66349ba086896aa5e899f60804cb52c1a91c83a4fa43b08477d62bcb4da8650f74204bff79a9bc42655103e20f9c9f82bd26bdff6; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakend/krakend-ce/releases/download/v2.13.2/krakend_2.13.2_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakend/krakend-ce/releases/download/v2.13.2/krakend_2.13.2_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Mon, 09 Mar 2026 18:35:26 GMT
WORKDIR /etc/krakend
# Mon, 09 Mar 2026 18:35:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 18:35:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:35:27 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Mon, 09 Mar 2026 18:35:27 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a8b1e176527ad5d76e2f073d84e7cfbe0db32a1e1b1b300ad6ddca8eb7e491`  
		Last Modified: Mon, 09 Mar 2026 18:35:34 GMT  
		Size: 463.2 KB (463249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5b3516e1496f6574a9d6ac86dac6228155798967617f7845b34bd812955821`  
		Last Modified: Mon, 09 Mar 2026 18:35:36 GMT  
		Size: 55.1 MB (55070772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd22d43a8e1a9ac9d6cd8971d4880022bfdd02c060e9362ea1f4129177b060ad`  
		Last Modified: Mon, 09 Mar 2026 18:35:34 GMT  
		Size: 646.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:af50018bbf9f9a5a93cd555d68f7b17b2ee7b5a6413eb25a6016cd1a02027ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 KB (15142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0c22e58d12006b9ddb4ac59d554171ad41b9b457b297ac5b9f2c7e8063faad`

```dockerfile
```

-	Layers:
	-	`sha256:de32c00fb3f9020008f3cbfaff95d1a1067a51149f217a3df4b37acd116e6e51`  
		Last Modified: Mon, 09 Mar 2026 18:35:34 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `krakend:latest` - linux; arm64 variant v8

```console
$ docker pull krakend@sha256:f98656362ce6138f89f79a7e9bd503d5ae5bce74c1eac310444274b296453a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56396756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ca5e16fc88f89da68f18aa41118d444a307368707efa67224ca7230a8d3e4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:03:27 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Mon, 09 Mar 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Mon, 09 Mar 2026 18:03:33 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=de4bd800546e13a749e5c1254d45a9dc4d1bd37e76647995cc7e62d1b0e025a0be00685c8a7a80c1b412ffbf9d33ec32a1298162ed368d436f77cfe1b17a69c0; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=50dedb294d047fc351b37de66349ba086896aa5e899f60804cb52c1a91c83a4fa43b08477d62bcb4da8650f74204bff79a9bc42655103e20f9c9f82bd26bdff6; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakend/krakend-ce/releases/download/v2.13.2/krakend_2.13.2_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakend/krakend-ce/releases/download/v2.13.2/krakend_2.13.2_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Mon, 09 Mar 2026 18:03:33 GMT
WORKDIR /etc/krakend
# Mon, 09 Mar 2026 18:03:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 18:03:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:03:33 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Mon, 09 Mar 2026 18:03:33 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8d52811a974a2d0fcb72df27f5467a1a6487a25c85e826eaf2cbbcb6c03ab8`  
		Last Modified: Mon, 09 Mar 2026 18:03:41 GMT  
		Size: 467.4 KB (467430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4c012d76b5187c9c13c34d0a41a07cf3266f2e3d230ce75f578ad1eaf41a70`  
		Last Modified: Mon, 09 Mar 2026 18:03:42 GMT  
		Size: 51.7 MB (51731561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4754d457341846e0b67039ca87f859d68f1df61050a736ef59de1075880f207`  
		Last Modified: Mon, 09 Mar 2026 18:03:41 GMT  
		Size: 642.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:c3869458a194f581c993cdef8c721316ad172ad9d2a6484b66a26147770de730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 KB (15261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d6e88a0698c8b3cf4d37b003575475cbd6ead1649dd67209dcef47500f41cf`

```dockerfile
```

-	Layers:
	-	`sha256:d6deb23c6e8a51834578d29ab6aa5ed313a513da449cc5652652d44385aaae4f`  
		Last Modified: Mon, 09 Mar 2026 18:03:41 GMT  
		Size: 15.3 KB (15261 bytes)  
		MIME: application/vnd.in-toto+json
