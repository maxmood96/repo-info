## `krakend:latest`

```console
$ docker pull krakend@sha256:a39da1ce9d3f29bf7851b30faa6f34ead3692880dbc5e313b18e491eb3f01b97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `krakend:latest` - linux; amd64

```console
$ docker pull krakend@sha256:41f5a3dbd5425371e35ebcc44e5ae369190f4416f90f9c4bca2dd3e5ea005990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52603525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cb3b54edda0f9eb7081a05cc5e44c093f40c8d895e5d26c4e67af088e21c94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 19 Jun 2025 18:43:53 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Thu, 19 Jun 2025 18:43:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Thu, 19 Jun 2025 18:43:53 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=10598c072ea895d99b4ad89b3d0d3cdd3b14298586a9a72f5800c5a5494b8cb387540c5f8297549891c049385f89e344fde71e73935b31a2d2b0c1219f15c888; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=9abe05143f0b3656ae9d337c84bfb9722c7280df37b7588a1f941df6c69386b19133b15ddd764fad298648244e14b627a8dcdbc88a35fe2607782d32449288e3; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakendio/krakend-ce/releases/download/v2.10.1/krakend_2.10.1_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakendio/krakend-ce/releases/download/v2.10.1/krakend_2.10.1_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Thu, 19 Jun 2025 18:43:53 GMT
WORKDIR /etc/krakend
# Thu, 19 Jun 2025 18:43:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Jun 2025 18:43:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Jun 2025 18:43:53 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Thu, 19 Jun 2025 18:43:53 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec19201e5ba5bc5efd9ac36a5c4b60f5e92c7855962064a0d60f255a1e68b79`  
		Last Modified: Fri, 20 Jun 2025 18:35:53 GMT  
		Size: 462.7 KB (462736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b950672061220c60cc85eb6aaea5ea81f0eeaa0d5a5dfb7cb8885b134c988cd`  
		Last Modified: Fri, 20 Jun 2025 18:35:56 GMT  
		Size: 48.5 MB (48497865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8e30503b04f7700bfc2e51c6aa7cac5555885d6010a444c90fdff8c3787836`  
		Last Modified: Fri, 20 Jun 2025 18:35:52 GMT  
		Size: 645.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:98c236ad02336e60f5320c0f77cca372b5f5ec89be0d58213dbfd7317bdf76f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 KB (15208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ac9edfe39c4b9aed26ddfc2b659b74730afa05a0196dd63e9b9a36d640789f`

```dockerfile
```

-	Layers:
	-	`sha256:ea91b63168c36e8d630da53a12e37a2f9f8e30f377ab64d4cee360030aa474ab`  
		Last Modified: Fri, 20 Jun 2025 20:12:26 GMT  
		Size: 15.2 KB (15208 bytes)  
		MIME: application/vnd.in-toto+json

### `krakend:latest` - linux; arm64 variant v8

```console
$ docker pull krakend@sha256:dec3f73e13dd296703e3d1271c056eb0bbbe54b4e2c8e5698775cbcbe77d807e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50622776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64bcc4f0a0857f16ae4f9bea1a02210c027045c470b20b25764a908e723b53f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 19 Jun 2025 18:43:53 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Thu, 19 Jun 2025 18:43:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Thu, 19 Jun 2025 18:43:53 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=10598c072ea895d99b4ad89b3d0d3cdd3b14298586a9a72f5800c5a5494b8cb387540c5f8297549891c049385f89e344fde71e73935b31a2d2b0c1219f15c888; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=9abe05143f0b3656ae9d337c84bfb9722c7280df37b7588a1f941df6c69386b19133b15ddd764fad298648244e14b627a8dcdbc88a35fe2607782d32449288e3; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakendio/krakend-ce/releases/download/v2.10.1/krakend_2.10.1_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakendio/krakend-ce/releases/download/v2.10.1/krakend_2.10.1_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Thu, 19 Jun 2025 18:43:53 GMT
WORKDIR /etc/krakend
# Thu, 19 Jun 2025 18:43:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Jun 2025 18:43:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Jun 2025 18:43:53 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Thu, 19 Jun 2025 18:43:53 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5fa319f0c31f7d1ea6e803a1852c2f71dd9beee550a90a11be369dffc09b59`  
		Last Modified: Fri, 20 Jun 2025 19:05:10 GMT  
		Size: 466.5 KB (466459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f2457573af802952ecb108fa23e87ba765f12a5e506ee82ab88ac31425139b`  
		Last Modified: Fri, 20 Jun 2025 20:12:47 GMT  
		Size: 46.2 MB (46162613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543c1bf6cc4c54abad75150c84ec649ec99eec6829e26ab338116a4a63137cb6`  
		Last Modified: Fri, 20 Jun 2025 19:05:57 GMT  
		Size: 643.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:9f44843f41b2d20f9ffd95be8e96d2284b2c26d1c42e0d3db65c1b7c7777ab7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 KB (15328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd36aa5bd834203b01db4f3668488bafc4d60f14490c94b239cd8e1848625acf`

```dockerfile
```

-	Layers:
	-	`sha256:050d12fbd0b9ec3b71a3ceab5cf382d5c1f6a29bb9e4d6e6883515d1d8d841e0`  
		Last Modified: Fri, 20 Jun 2025 20:12:34 GMT  
		Size: 15.3 KB (15328 bytes)  
		MIME: application/vnd.in-toto+json
