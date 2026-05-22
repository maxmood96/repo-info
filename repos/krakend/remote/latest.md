## `krakend:latest`

```console
$ docker pull krakend@sha256:d6ec060f5edffb6d6c659f5465c07c5113eb431b5347e6f02ea1bef8c25c9b8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `krakend:latest` - linux; amd64

```console
$ docker pull krakend@sha256:581498806f38a4433217191ce118eca73f05f86179f06a9f8cec6bdc515d1cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59536684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0694306b3359fb7f7c87fb3d2f35491315d3f2159a59d1c8134b62be11a49d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 22 May 2026 18:30:17 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Fri, 22 May 2026 18:30:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Fri, 22 May 2026 18:30:21 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=c1d39556716091f038d676294156d658dba1c72bd0a3761c63e220b93f1ef9e4c7b27ec58d37cbe307528bde815a22936a73002b1c8048f89863258b85ea1fd4; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=dc149f1b4e805bd22d5c916eb0e6d942e451c707d99070fd7c9dd47bf95c44dcd957d9c81f3d68de0bddce2214aa1f5e3f5e66b34fafb27be9d8d4a00eb564e8; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakend/krakend-ce/releases/download/v2.13.6/krakend_2.13.6_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakend/krakend-ce/releases/download/v2.13.6/krakend_2.13.6_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Fri, 22 May 2026 18:30:22 GMT
WORKDIR /etc/krakend
# Fri, 22 May 2026 18:30:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 May 2026 18:30:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 May 2026 18:30:22 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Fri, 22 May 2026 18:30:22 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712c939572199ee5fc776791b9050327ce0286fbeb56d5f12fc8dc05a499f0eb`  
		Last Modified: Fri, 22 May 2026 18:30:30 GMT  
		Size: 458.3 KB (458336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c583f49f2c37f709c04ae17feeea3db59aebbaf78d9fc848403999e254bd926`  
		Last Modified: Fri, 22 May 2026 18:30:31 GMT  
		Size: 55.2 MB (55213484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916ef2bd196781726572ad757a76a6534484c4125cb718efef47f7399c367e3d`  
		Last Modified: Fri, 22 May 2026 18:30:29 GMT  
		Size: 643.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:2e77cbfef2fe6fb39cd017dc6bbd50fe4b575a53de894e9d1517e74f657a8aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 KB (15142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f36cb07f2d6db59060cdf1ea6537b9e53624f64176ff15bfe402442b8d5b113`

```dockerfile
```

-	Layers:
	-	`sha256:781d898bab665d07bd0a5c81f1bdf41e8ce1545ef80a17470d6ef639d472a4de`  
		Last Modified: Fri, 22 May 2026 18:30:29 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `krakend:latest` - linux; arm64 variant v8

```console
$ docker pull krakend@sha256:ceb5bd94fd0144437024f49ed06f5ceac685f7b40b163894896e27ae584a195d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56519013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499766ba2abe6781621a2270e789720b72e9197d17cf14647d6daf02339cc81d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["krakend","run","-c","krakend.json"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 22 May 2026 18:30:15 GMT
LABEL org.opencontainers.image.authors=community@krakend.io
# Fri, 22 May 2026 18:30:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .run-deps ca-certificates su-exec tzdata; 	adduser -u 1000 -S -D -H krakend; # buildkit
# Fri, 22 May 2026 18:30:20 GMT
RUN set -eux;     apk add --no-cache --virtual .build-deps gnupg;     arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=c1d39556716091f038d676294156d658dba1c72bd0a3761c63e220b93f1ef9e4c7b27ec58d37cbe307528bde815a22936a73002b1c8048f89863258b85ea1fd4; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			export KRAKEND_DOWNLOAD_SHA512=dc149f1b4e805bd22d5c916eb0e6d942e451c707d99070fd7c9dd47bf95c44dcd957d9c81f3d68de0bddce2214aa1f5e3f5e66b34fafb27be9d8d4a00eb564e8; 			;; 		*) echo >&2 "error: unsupported architecture '$TARGETARCH' (likely packaging update needed)"; exit 1 ;; 	esac;     wget -O krakend.tar.gz "https://github.com/krakend/krakend-ce/releases/download/v2.13.6/krakend_2.13.6_${GOARCH}_alpine.tar.gz";     wget -O krakend.tar.gz.asc "https://github.com/krakend/krakend-ce/releases/download/v2.13.6/krakend_2.13.6_${GOARCH}_alpine.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 5B270F2E01E375FD9D5635E25DE6FD698AD6FDD2;     gpg --batch --verify krakend.tar.gz.asc krakend.tar.gz;     gpgconf --kill all;     rm -rf "$GNUPGHOME";     echo "$KRAKEND_DOWNLOAD_SHA512 *krakend.tar.gz" | sha512sum -c;     tar -xzf krakend.tar.gz -C / --strip-components 1;     rm -f krakend.tar.gz krakend.tar.gz.asc;     apk del --no-network .build-deps;     echo '{ "version": 3 }' > /etc/krakend/krakend.json # buildkit
# Fri, 22 May 2026 18:30:20 GMT
WORKDIR /etc/krakend
# Fri, 22 May 2026 18:30:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 May 2026 18:30:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 May 2026 18:30:20 GMT
EXPOSE map[8080/tcp:{} 8090/tcp:{}]
# Fri, 22 May 2026 18:30:20 GMT
CMD ["krakend" "run" "-c" "krakend.json"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41946f7759bf34d168020f00bedcc1c380385a535dec122007d80085f9b4cf5f`  
		Last Modified: Fri, 22 May 2026 18:30:28 GMT  
		Size: 461.7 KB (461726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c94ec2473d1ec5d3322d232f3d0336c57041b8832f1a7f197d1b9d71ca4ade9`  
		Last Modified: Fri, 22 May 2026 18:30:29 GMT  
		Size: 51.9 MB (51856742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6465232043a8506257729afbc79e308efc67b3edfcf1e66eca6c6069a7c526fe`  
		Last Modified: Fri, 22 May 2026 18:30:28 GMT  
		Size: 643.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `krakend:latest` - unknown; unknown

```console
$ docker pull krakend@sha256:f89e50bca3f9c27ca9511daf3b19ded6357707442ee4fa98cdc8858f453c74c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 KB (15260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4957835f50784e48467349c81e0a833a40bfc18a203bdfdd814d8dc9a6133734`

```dockerfile
```

-	Layers:
	-	`sha256:75bf43d401c583597a1cc3586b666e64382e0ef44a73f1df3ffd0870ac7da1dc`  
		Last Modified: Fri, 22 May 2026 18:30:28 GMT  
		Size: 15.3 KB (15260 bytes)  
		MIME: application/vnd.in-toto+json
