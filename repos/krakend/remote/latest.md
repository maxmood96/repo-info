## `krakend:latest`

```console
$ docker pull krakend@sha256:eab4ddd440cffa844035e21b0db920aca539feb7ceb2b227a87c973f1a5fb1f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `krakend:latest` - linux; amd64

```console
$ docker pull krakend@sha256:ba11aaf9c6bbab8dad0a4c0bb4ab7162715e11e7c6a193ef1b6c053f50a78199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51583961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a936a471c893a06ffcab235d88ac0de411380e6113493b1d87023efb2bdee788`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
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
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d417e297e99303b9ef3c7340ab084f1a5a526d9fac0a2fb0e8bbf8de41954012`  
		Last Modified: Wed, 08 Oct 2025 22:39:15 GMT  
		Size: 459.5 KB (459484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f3449b19a5b01b50440ead505121950e1862b7a700b7c915395813a27256dd`  
		Last Modified: Wed, 08 Oct 2025 22:39:25 GMT  
		Size: 47.5 MB (47481235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b1b8bf952a2fa10e2ed3b6bbace670641c17b4c51b185c34cfbe38ea13f9b6`  
		Last Modified: Wed, 08 Oct 2025 22:39:15 GMT  
		Size: 641.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:2154fd9de82044048eb915560c8d3188b6566fe3e8770b3594e0e12e322924a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 KB (15206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383bf8546164c7dd8cdaa090ea06ac455c871896335779442e8a559fabe1095e`

```dockerfile
```

-	Layers:
	-	`sha256:60424883849f279e0419947b2ad08c657a726bd8d1ab08745ff9ce908101821c`  
		Last Modified: Thu, 09 Oct 2025 02:12:16 GMT  
		Size: 15.2 KB (15206 bytes)  
		MIME: application/vnd.in-toto+json

### `krakend:latest` - linux; arm64 variant v8

```console
$ docker pull krakend@sha256:a2b51c42d960933699fcafe223eb5ece51f9bb2b89b6908957573409b6802526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49191238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7598a7f5c60bffc882ab8e68415fb2c472c4e2731fe489520f4a7e32ddb92995`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
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
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcaaefb03766ea7f003739c50717a8b147950a148a90d45c837a7a6a416bff8`  
		Last Modified: Wed, 08 Oct 2025 21:28:33 GMT  
		Size: 463.1 KB (463100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fb9d73af0e98161aefe8cb25615c87190378a5d6aa9094cc9a905d49db3a3f`  
		Last Modified: Wed, 08 Oct 2025 21:28:35 GMT  
		Size: 44.7 MB (44735113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682d876f994d08b18295757d50723537cb72d6e62096eac0e9e200f896815c14`  
		Last Modified: Wed, 08 Oct 2025 21:28:33 GMT  
		Size: 640.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:7bb83f45f00e7f70b48870cf5ea2f608005a7160100edc07c2cfcd033a68f959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 KB (15328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b523cc5add3f77cf5f7822fac2462f4982ccd5b1ef619143d56d76b73c143f83`

```dockerfile
```

-	Layers:
	-	`sha256:8bd490ef59c1f695946e9808a7e4e3c84ad9eec10d0bb42a31db069d84ee4444`  
		Last Modified: Wed, 08 Oct 2025 23:12:19 GMT  
		Size: 15.3 KB (15328 bytes)  
		MIME: application/vnd.in-toto+json
