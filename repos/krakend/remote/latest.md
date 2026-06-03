## `krakend:latest`

```console
$ docker pull krakend@sha256:c52603d669b4f8930ea82f9158b3d83e69d0cdd2a355dcd629eec459785b230c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `krakend:latest` - linux; amd64

```console
$ docker pull krakend@sha256:91c346c02e706bc63036c0fc73c67f13c3b60cd5672d4219d05887fc0abe4d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59538112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c615ce1d3d7c7891653ec7a91bdcbd02326505304657c035f2747113d8aa98d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 03 Jun 2026 18:03:20 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Wed, 03 Jun 2026 18:03:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Wed, 03 Jun 2026 18:03:25 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=7fad4a25772a51bb7935fcf2d5b440b65686e2653db6c963853564d63379bab832e26f8527c0b4f78defb2b4566e37ab14da85b3008d6cc562c5396c2b580e28; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=038efd98782fcc9b2103bb2fc9931fd781af4bb153b76c15fb9abb5784c7e5a915b3d009f138af95eff7157bd6a4e66b64a4e204d3a451bc1835c409d2a3b28a; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakend/krakend-ce/releases/download/v2.13.7/krakend_2.13.7_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakend/krakend-ce/releases/download/v2.13.7/krakend_2.13.7_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Wed, 03 Jun 2026 18:03:25 GMT
WORKDIR /etc/krakend
# Wed, 03 Jun 2026 18:03:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Jun 2026 18:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Jun 2026 18:03:25 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Wed, 03 Jun 2026 18:03:25 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6801ce53967c275613ed2351ef5fca9fd0df89cfbdda8025750a13c76c520a`  
		Last Modified: Wed, 03 Jun 2026 18:03:32 GMT  
		Size: 458.4 KB (458354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ceb6dad4d0640a109b8d64023ca45b000144aa23f2ce092b34cbfcf4475af94`  
		Last Modified: Wed, 03 Jun 2026 18:03:34 GMT  
		Size: 55.2 MB (55214891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbebdcc52da4065764dbd30aa9839919058321c44e1542dbbe2073ba7193892`  
		Last Modified: Wed, 03 Jun 2026 18:03:33 GMT  
		Size: 646.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:d53672c26c1104414cb15315382c666a979725b03a706522ebc688e81445508b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 KB (15142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c477c982e1dced432655fee07462fe48a3cf8704b1ab77265f42670e2739bec9`

```dockerfile
```

-	Layers:
	-	`sha256:133ba3fa3dfc4e2ad4e4b96ea23dfb28f90c414e3eb5843a46e5c3d94b45f487`  
		Last Modified: Wed, 03 Jun 2026 18:03:32 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `krakend:latest` - linux; arm64 variant v8

```console
$ docker pull krakend@sha256:9e8d5a6f182587fdbdc06bd75a0ab7aeede13d328f0ee5e13618777077845a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56516201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a1434dd96e7db5310c7bdd69f76ea6d163ebe65bd5de7ac09350cd6fe9ffc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 03 Jun 2026 18:04:22 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Wed, 03 Jun 2026 18:04:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Wed, 03 Jun 2026 18:04:27 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=7fad4a25772a51bb7935fcf2d5b440b65686e2653db6c963853564d63379bab832e26f8527c0b4f78defb2b4566e37ab14da85b3008d6cc562c5396c2b580e28; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=038efd98782fcc9b2103bb2fc9931fd781af4bb153b76c15fb9abb5784c7e5a915b3d009f138af95eff7157bd6a4e66b64a4e204d3a451bc1835c409d2a3b28a; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakend/krakend-ce/releases/download/v2.13.7/krakend_2.13.7_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakend/krakend-ce/releases/download/v2.13.7/krakend_2.13.7_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Wed, 03 Jun 2026 18:04:27 GMT
WORKDIR /etc/krakend
# Wed, 03 Jun 2026 18:04:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Jun 2026 18:04:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Jun 2026 18:04:27 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Wed, 03 Jun 2026 18:04:27 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5832ce44851bc40317e8983b40bdcab093ee3ed8b318e8a299a49d422f3f15a`  
		Last Modified: Wed, 03 Jun 2026 18:04:35 GMT  
		Size: 461.7 KB (461723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8de288b32621aaf4503a91e58ce2a9a2684d4ed0753f92141857319d06446a`  
		Last Modified: Wed, 03 Jun 2026 18:04:37 GMT  
		Size: 51.9 MB (51853935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e61a040ba8b15f6bc30d5dbce4a238d2a6abd30c4ef19ddea4f5fe148a335a`  
		Last Modified: Wed, 03 Jun 2026 18:04:35 GMT  
		Size: 641.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:be2f8c81302b7f3d80fb31ece3a325378960e87f70213635956baa63207e9f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 KB (15260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3eef69d355c576b2b185c4edb156ddcd33bd65a609c4a4e9bd62701e40a8a69`

```dockerfile
```

-	Layers:
	-	`sha256:f093dfac04762e6d6fa091bf7e5183067d60d564d8a987dc4c8f64e86860bb47`  
		Last Modified: Wed, 03 Jun 2026 18:04:35 GMT  
		Size: 15.3 KB (15260 bytes)  
		MIME: application/vnd.in-toto+json
