<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `krakend`

-	[`krakend:2`](#krakend2)
-	[`krakend:2.12`](#krakend212)
-	[`krakend:2.12.0`](#krakend2120)
-	[`krakend:latest`](#krakendlatest)

## `krakend:2`

```console
$ docker pull krakend@sha256:9ba8567cfb5da2aba081ab8198eb582d3715ec3fbe66d37483c61ebe7a0bc957
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `krakend:2` - linux; amd64

```console
$ docker pull krakend@sha256:8452d5c54661e3c769749aee05bfe2b6799f41adbf9bdc0db6df932a2005eabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51586427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65d7659610d5bd9d7fb55fde781796c7d0d33370dae2373bd867aee7b0ae07b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 13:59:06 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Thu, 16 Oct 2025 13:59:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Thu, 16 Oct 2025 13:59:06 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=5fb522a3d4b3713c2ae3073f8d9f13fa9e6018163de4706783edc646164e7770a6942920703f04f9c92e3b92485e08be6df820615f1f0cf72f9804832ed20c57; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=22cd1058fffe5bd71587600357b66542bbbf47cc99ca595e80e9832193cdb79fa10b2f57718d45eb6961c79706f665b7bbd4c5e7bfae87a7ba62f8bf782e4917; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakendio/krakend-ce/releases/download/v2.11.2/krakend_2.11.2_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakendio/krakend-ce/releases/download/v2.11.2/krakend_2.11.2_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Thu, 16 Oct 2025 13:59:06 GMT
WORKDIR /etc/krakend
# Thu, 16 Oct 2025 13:59:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 13:59:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 13:59:06 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Thu, 16 Oct 2025 13:59:06 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540ab03ff467739bcc4541104435e1801530f9cf6ab9ccf2fa782d0bb2be0594`  
		Last Modified: Thu, 16 Oct 2025 18:33:29 GMT  
		Size: 459.5 KB (459482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98141a9cf60301fe91201c805cad29bc429a49e5903339822051aac3bcf70e4`  
		Last Modified: Thu, 16 Oct 2025 18:33:38 GMT  
		Size: 47.5 MB (47483700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24271a1c67bfa6bc8189a72b44d04ccd4b792c0af1086c1f08bcf8db3fa347df`  
		Last Modified: Thu, 16 Oct 2025 18:33:29 GMT  
		Size: 644.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:2` - unknown; unknown

```console
$ docker pull krakend@sha256:609af39da915510ee3f4d9b7cf05d22268ee3c87263ead041a3dec5dfd44d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 KB (15197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffae8264f2f584e684005978f652a76e9d3ed8eb23b1f4bc9cf85bd91ad6b61`

```dockerfile
```

-	Layers:
	-	`sha256:8cbde111efb71aa8a42012586fc688175b3a0a79f48181c3e50b44bb79f695c2`  
		Last Modified: Thu, 16 Oct 2025 20:12:19 GMT  
		Size: 15.2 KB (15197 bytes)  
		MIME: application/vnd.in-toto+json

### `krakend:2` - linux; arm64 variant v8

```console
$ docker pull krakend@sha256:8ca5f835949d368f0b9f3179a99cdc9bebc64f79ce733e9c637fa9669b7b1761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49193573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73598d732b67b95cf593232ee769391118caf4f7a14cf563610cda3f965e7d41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 13:59:06 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Thu, 16 Oct 2025 13:59:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Thu, 16 Oct 2025 13:59:06 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=5fb522a3d4b3713c2ae3073f8d9f13fa9e6018163de4706783edc646164e7770a6942920703f04f9c92e3b92485e08be6df820615f1f0cf72f9804832ed20c57; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=22cd1058fffe5bd71587600357b66542bbbf47cc99ca595e80e9832193cdb79fa10b2f57718d45eb6961c79706f665b7bbd4c5e7bfae87a7ba62f8bf782e4917; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakendio/krakend-ce/releases/download/v2.11.2/krakend_2.11.2_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakendio/krakend-ce/releases/download/v2.11.2/krakend_2.11.2_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Thu, 16 Oct 2025 13:59:06 GMT
WORKDIR /etc/krakend
# Thu, 16 Oct 2025 13:59:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 13:59:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 13:59:06 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Thu, 16 Oct 2025 13:59:06 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cee614d599aa222bb2b53280142da611df8da8434d6bb93d9b06b6700ae9c5`  
		Last Modified: Thu, 16 Oct 2025 18:11:25 GMT  
		Size: 463.1 KB (463106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e935ae3e3b5cba554daa2a7ddb2a85664e623b36a4c2ef4159b723fa6454a6dc`  
		Last Modified: Thu, 16 Oct 2025 18:11:29 GMT  
		Size: 44.7 MB (44737441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497ebdabca9321f82efcbfb3e4da9a2f8361a6c34240f4145ce235a49d39772b`  
		Last Modified: Thu, 16 Oct 2025 18:11:25 GMT  
		Size: 641.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:2` - unknown; unknown

```console
$ docker pull krakend@sha256:df449e010b7e636e14461a7965cfacf9aefcd71bba0830fa6b84d0947fc739fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 KB (15316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc13a430a08e9eaae4a2be96fd26b78bbcbf469437420284855ad170fc21c436`

```dockerfile
```

-	Layers:
	-	`sha256:2d28122f340d550e717cf954f2e9a6cfc12290433b286ba42c56fcc367e1e762`  
		Last Modified: Thu, 16 Oct 2025 20:12:22 GMT  
		Size: 15.3 KB (15316 bytes)  
		MIME: application/vnd.in-toto+json

## `krakend:2.12`

**does not exist** (yet?)

## `krakend:2.12.0`

**does not exist** (yet?)

## `krakend:latest`

```console
$ docker pull krakend@sha256:9ba8567cfb5da2aba081ab8198eb582d3715ec3fbe66d37483c61ebe7a0bc957
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `krakend:latest` - linux; amd64

```console
$ docker pull krakend@sha256:8452d5c54661e3c769749aee05bfe2b6799f41adbf9bdc0db6df932a2005eabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51586427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65d7659610d5bd9d7fb55fde781796c7d0d33370dae2373bd867aee7b0ae07b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 13:59:06 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Thu, 16 Oct 2025 13:59:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Thu, 16 Oct 2025 13:59:06 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=5fb522a3d4b3713c2ae3073f8d9f13fa9e6018163de4706783edc646164e7770a6942920703f04f9c92e3b92485e08be6df820615f1f0cf72f9804832ed20c57; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=22cd1058fffe5bd71587600357b66542bbbf47cc99ca595e80e9832193cdb79fa10b2f57718d45eb6961c79706f665b7bbd4c5e7bfae87a7ba62f8bf782e4917; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakendio/krakend-ce/releases/download/v2.11.2/krakend_2.11.2_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakendio/krakend-ce/releases/download/v2.11.2/krakend_2.11.2_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Thu, 16 Oct 2025 13:59:06 GMT
WORKDIR /etc/krakend
# Thu, 16 Oct 2025 13:59:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 13:59:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 13:59:06 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Thu, 16 Oct 2025 13:59:06 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540ab03ff467739bcc4541104435e1801530f9cf6ab9ccf2fa782d0bb2be0594`  
		Last Modified: Thu, 16 Oct 2025 18:33:29 GMT  
		Size: 459.5 KB (459482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98141a9cf60301fe91201c805cad29bc429a49e5903339822051aac3bcf70e4`  
		Last Modified: Thu, 16 Oct 2025 18:33:38 GMT  
		Size: 47.5 MB (47483700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24271a1c67bfa6bc8189a72b44d04ccd4b792c0af1086c1f08bcf8db3fa347df`  
		Last Modified: Thu, 16 Oct 2025 18:33:29 GMT  
		Size: 644.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:609af39da915510ee3f4d9b7cf05d22268ee3c87263ead041a3dec5dfd44d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 KB (15197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffae8264f2f584e684005978f652a76e9d3ed8eb23b1f4bc9cf85bd91ad6b61`

```dockerfile
```

-	Layers:
	-	`sha256:8cbde111efb71aa8a42012586fc688175b3a0a79f48181c3e50b44bb79f695c2`  
		Last Modified: Thu, 16 Oct 2025 20:12:19 GMT  
		Size: 15.2 KB (15197 bytes)  
		MIME: application/vnd.in-toto+json

### `krakend:latest` - linux; arm64 variant v8

```console
$ docker pull krakend@sha256:8ca5f835949d368f0b9f3179a99cdc9bebc64f79ce733e9c637fa9669b7b1761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49193573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73598d732b67b95cf593232ee769391118caf4f7a14cf563610cda3f965e7d41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 13:59:06 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Thu, 16 Oct 2025 13:59:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Thu, 16 Oct 2025 13:59:06 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=5fb522a3d4b3713c2ae3073f8d9f13fa9e6018163de4706783edc646164e7770a6942920703f04f9c92e3b92485e08be6df820615f1f0cf72f9804832ed20c57; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=22cd1058fffe5bd71587600357b66542bbbf47cc99ca595e80e9832193cdb79fa10b2f57718d45eb6961c79706f665b7bbd4c5e7bfae87a7ba62f8bf782e4917; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakendio/krakend-ce/releases/download/v2.11.2/krakend_2.11.2_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakendio/krakend-ce/releases/download/v2.11.2/krakend_2.11.2_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Thu, 16 Oct 2025 13:59:06 GMT
WORKDIR /etc/krakend
# Thu, 16 Oct 2025 13:59:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 13:59:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 13:59:06 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Thu, 16 Oct 2025 13:59:06 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cee614d599aa222bb2b53280142da611df8da8434d6bb93d9b06b6700ae9c5`  
		Last Modified: Thu, 16 Oct 2025 18:11:25 GMT  
		Size: 463.1 KB (463106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e935ae3e3b5cba554daa2a7ddb2a85664e623b36a4c2ef4159b723fa6454a6dc`  
		Last Modified: Thu, 16 Oct 2025 18:11:29 GMT  
		Size: 44.7 MB (44737441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497ebdabca9321f82efcbfb3e4da9a2f8361a6c34240f4145ce235a49d39772b`  
		Last Modified: Thu, 16 Oct 2025 18:11:25 GMT  
		Size: 641.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:df449e010b7e636e14461a7965cfacf9aefcd71bba0830fa6b84d0947fc739fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 KB (15316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc13a430a08e9eaae4a2be96fd26b78bbcbf469437420284855ad170fc21c436`

```dockerfile
```

-	Layers:
	-	`sha256:2d28122f340d550e717cf954f2e9a6cfc12290433b286ba42c56fcc367e1e762`  
		Last Modified: Thu, 16 Oct 2025 20:12:22 GMT  
		Size: 15.3 KB (15316 bytes)  
		MIME: application/vnd.in-toto+json
