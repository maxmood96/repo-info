## `krakend:latest`

```console
$ docker pull krakend@sha256:ee484307cc986af2f8bf59fc9a4f7ddeb4ea6507afafe9a16bcde012337bf40d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `krakend:latest` - linux; amd64

```console
$ docker pull krakend@sha256:91e979d9fa6f3121dd00791724186717bc6dd08d8219b2d2bbd082a42ebf0b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52160299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301673f8f503947025bec62b83125398faf9c3340cff7654bd3c4f60c0fa5f8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Feb 2026 18:29:38 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Tue, 10 Feb 2026 18:29:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Tue, 10 Feb 2026 18:29:44 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=6ee7c2fda7c32b8398dfa5284de5145dedf80a28e187b649ed73bb4bc774f95e1a19da80c1b2155bc5b3bfd9dc2d01fc35d740e74578540740cc84e8e39f42fb; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=f0a169c7f082fd75d096867841b0713254f5a585b79e4adfdcec50cbb6d514cfe871131e48ce564ca8335453832b88c0f1ccf79c4daab0e6aaa0f61f0e34a6c6; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakendio/krakend-ce/releases/download/v2.13.0/krakend_2.13.0_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakendio/krakend-ce/releases/download/v2.13.0/krakend_2.13.0_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Tue, 10 Feb 2026 18:29:44 GMT
WORKDIR /etc/krakend
# Tue, 10 Feb 2026 18:29:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Feb 2026 18:29:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Feb 2026 18:29:44 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Tue, 10 Feb 2026 18:29:44 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c152c1750b0adcf476670f639902a7335619605b41b398f198476a7b8b51c1a`  
		Last Modified: Tue, 10 Feb 2026 18:29:51 GMT  
		Size: 463.4 KB (463433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a286d76c9f6924e719965758060c278e6ed386d8a076aa69edb842d735d6d98e`  
		Last Modified: Tue, 10 Feb 2026 18:29:53 GMT  
		Size: 47.8 MB (47834369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73001e729144c722d31abf9862750d1fdff64e5880e3d65d84d4bfa1f661f7d`  
		Last Modified: Tue, 10 Feb 2026 18:29:52 GMT  
		Size: 644.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:f46bd84ecf50a74e9e6fb3c3feb5392880ca1d416247958501b522d5b1508331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 KB (15154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4fa76084dc5367802893b185a76f0cf402a5505ebaccb1b8db56799be821bf9`

```dockerfile
```

-	Layers:
	-	`sha256:dbea3e752fd30b4b5d9f58d66517b47c399a7c1578f4075c19525deecbcfe1bd`  
		Last Modified: Tue, 10 Feb 2026 18:29:52 GMT  
		Size: 15.2 KB (15154 bytes)  
		MIME: application/vnd.in-toto+json

### `krakend:latest` - linux; arm64 variant v8

```console
$ docker pull krakend@sha256:db56bf6b72f04790fe81a3e95b936473348747787e4fa61b343d59a3bb4f261b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49740520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1236b36540d9a0f72f0cd3f2e387b50d92b8b26d3c63fd7306bdb490aa385dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 10 Feb 2026 18:29:32 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Tue, 10 Feb 2026 18:29:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Tue, 10 Feb 2026 18:29:38 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=6ee7c2fda7c32b8398dfa5284de5145dedf80a28e187b649ed73bb4bc774f95e1a19da80c1b2155bc5b3bfd9dc2d01fc35d740e74578540740cc84e8e39f42fb; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=f0a169c7f082fd75d096867841b0713254f5a585b79e4adfdcec50cbb6d514cfe871131e48ce564ca8335453832b88c0f1ccf79c4daab0e6aaa0f61f0e34a6c6; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakendio/krakend-ce/releases/download/v2.13.0/krakend_2.13.0_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakendio/krakend-ce/releases/download/v2.13.0/krakend_2.13.0_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Tue, 10 Feb 2026 18:29:38 GMT
WORKDIR /etc/krakend
# Tue, 10 Feb 2026 18:29:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Feb 2026 18:29:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Feb 2026 18:29:38 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Tue, 10 Feb 2026 18:29:38 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf2737b82ed92be1bc0306f86a8ae33f271b31f2f23cf470eca9cc6f60891e`  
		Last Modified: Tue, 10 Feb 2026 18:29:45 GMT  
		Size: 467.7 KB (467676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35bfdfe576ce90ccf5b9bab77b3d4ff78012c4efa2d26800304b7db6be583254`  
		Last Modified: Tue, 10 Feb 2026 18:29:47 GMT  
		Size: 45.1 MB (45075076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d776951f638ce5af3305eb3e5083fd636bdb44ff85c4087a51f275aa015025`  
		Last Modified: Tue, 10 Feb 2026 18:29:45 GMT  
		Size: 645.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:b0cc20c100b01658f6e1ed2e457e161ac5178e5c768e914f8d549ff9b7ac65ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 KB (15273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6707f3899ecd7ddf48656444d5081ae90edf226c53a3b060dcee8249aaedb95`

```dockerfile
```

-	Layers:
	-	`sha256:101523d6be345c898c91025295b9898b89144698c4b7b1b89bcc68c14cc97735`  
		Last Modified: Tue, 10 Feb 2026 18:29:45 GMT  
		Size: 15.3 KB (15273 bytes)  
		MIME: application/vnd.in-toto+json
