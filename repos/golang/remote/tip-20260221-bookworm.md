## `golang:tip-20260221-bookworm`

```console
$ docker pull golang@sha256:f9fff4536ddf066f36b80c1add32270d41d0497df319f12722b01bde7914a004
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `golang:tip-20260221-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:6786b4557aaf478221023340773d9cf02ac62e0f015d57cf2a9619606ba5810e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.9 MB (322932031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4215c750573053537fed8f5ca830de2238fbb326f394c033a05089cd6070be9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:03:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:17:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:19:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 21:19:32 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 21:19:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:19:32 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 21:19:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 21:19:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa27031269f0a970255d56a9e793fc2a9d6bb091463cd5e632af4ae274881601`  
		Last Modified: Tue, 24 Feb 2026 20:03:49 GMT  
		Size: 64.4 MB (64395853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22ead324cc053655a27bd7c2c7a2d0d0c15da81263d5bfd174f722c02f783c6`  
		Last Modified: Tue, 24 Feb 2026 21:20:00 GMT  
		Size: 92.4 MB (92444836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d495feeee1b60c984a8277e0860f99ef7f9650e71ef87f6e01f020f04c712c1e`  
		Last Modified: Tue, 24 Feb 2026 19:01:11 GMT  
		Size: 93.6 MB (93563958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582b0cd87b6c91f70e99b8337370a36fad0f8c86cb84cacebbc5418e97e7f394`  
		Last Modified: Tue, 24 Feb 2026 21:19:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260221-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2eb1cf9a4fe183c6d541e4435839be12d67ca47edc087019c65976ae2f708e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b79cb356ee6d0d23230a5050040403e5dd836a7d1ac5efe737d26135bc44e6`

```dockerfile
```

-	Layers:
	-	`sha256:71faed9daae169079b6b5b908a4d43f6f1b764fa3a70a1e09c704bf00f32d8e1`  
		Last Modified: Tue, 24 Feb 2026 21:19:59 GMT  
		Size: 10.5 MB (10497031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b958c1d486f88dbe3e8ca73b5ca7b0ca02e198ec0ebd4299d7779dc17e5ce23`  
		Last Modified: Tue, 24 Feb 2026 21:19:58 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260221-bookworm` - linux; 386

```console
$ docker pull golang@sha256:9aeb668af244f03d37e0f9d62e58dcca03e2a7596ea42a6b1ac5b89da0d2c573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.9 MB (321910301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91370cdfd7095a325613ac71e9f0345e503258593b8a117b2bf02595e896df8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:56:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:15:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 21:15:31 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 21:15:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:15:31 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 21:15:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 21:15:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:443394a7d911f581670ce4df7959c82f7e8f0be02b5a7ba3c71bc5958012963d`  
		Last Modified: Tue, 24 Feb 2026 18:41:48 GMT  
		Size: 49.5 MB (49477853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31e1fab6283d72f6ce2de137bc123a8ab89a85f0baa0b6c11c2c6d28c359a32`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 24.9 MB (24872106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383bd8d2ca9c40d67394c0121b8fdb7d7c8f44082342e21f4188fc611c88e9a6`  
		Last Modified: Tue, 24 Feb 2026 19:56:53 GMT  
		Size: 66.2 MB (66234334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0eef27a00b9b7db3948f213e46e37a1218941e612ff12da04f2f04381e2cf5`  
		Last Modified: Tue, 24 Feb 2026 21:15:57 GMT  
		Size: 89.9 MB (89871402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70dcda3c127f8506d59d712159bc64c0b0ee6293dc7af8e7cd42a7bdd642799`  
		Last Modified: Tue, 24 Feb 2026 19:27:40 GMT  
		Size: 91.5 MB (91454447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7595e9a9c0b3b2239280a002f6a76f48d259931ed03e5fb84c1382bcacf8f77f`  
		Last Modified: Tue, 24 Feb 2026 21:15:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260221-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:31528947ad120b6ec105c2ed26fe93e17277b7e7fb5beba673548ac1d8c9bf59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda8383e5a34e2f325bbcdc2d4e42aea01385d7a9a2f134db7486bc5d32274c6`

```dockerfile
```

-	Layers:
	-	`sha256:2c80b7e1ed51984d177257fa901e04d5a066fd43a70726a8f45fb4020d0b1da2`  
		Last Modified: Tue, 24 Feb 2026 21:15:55 GMT  
		Size: 10.5 MB (10476611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47c7f4aa57315a97e711f9f26e1f4ebf399778123b8b523188eee2fb5218b94b`  
		Last Modified: Tue, 24 Feb 2026 21:15:54 GMT  
		Size: 28.4 KB (28352 bytes)  
		MIME: application/vnd.in-toto+json
