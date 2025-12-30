## `golang:tip-20251227-bookworm`

```console
$ docker pull golang@sha256:ed127a0939e11f2f3b468dcf2e0ef23182d27472f61cc09fa9898c0b61e07941
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; 386
	-	unknown; unknown

### `golang:tip-20251227-bookworm` - linux; 386

```console
$ docker pull golang@sha256:90b6300a978db20b518692780b8c46945238398eb7fb3e0e45bd314943a203ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.3 MB (323343427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e5c5b19d4b7a3246ef21e4a4c1b1b0ad409c72f8f863008b6f943b406b8743`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:47:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:32:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:19:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:21:29 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Dec 2025 02:21:29 GMT
ENV GOPATH=/go
# Tue, 30 Dec 2025 02:21:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:21:29 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 02:21:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 02:21:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d27cc9ffb7903d292157edf3b1fb57175a2a59b66ae4855d328a6a97d9b4a6e9`  
		Last Modified: Mon, 29 Dec 2025 22:24:49 GMT  
		Size: 49.5 MB (49466879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63bb42155eb2fe3cb6496304c20382db95885b672da0e34a3fffa188861a6ec`  
		Last Modified: Mon, 29 Dec 2025 23:47:31 GMT  
		Size: 24.9 MB (24864466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10eedb7d741cb151d52259302acf62c6c98590a9a4168d4370619e890f15715`  
		Last Modified: Tue, 30 Dec 2025 00:32:36 GMT  
		Size: 66.2 MB (66233282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e295f8252ca90e89f51c1363170a6376ce4095e7645eaba61a98042c65f425ae`  
		Last Modified: Tue, 30 Dec 2025 02:22:14 GMT  
		Size: 89.8 MB (89839937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b6f0074455116012c1ba771d20edb2ec10d2462257d60366f8ccb9b9224a99`  
		Last Modified: Mon, 29 Dec 2025 22:17:35 GMT  
		Size: 92.9 MB (92938705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575dbe2fb45e9468db32a096a5c32074522972f62ce95c55407ebe75f1465a51`  
		Last Modified: Tue, 30 Dec 2025 02:22:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251227-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c543ca285f12d47013a6e570d44c6c1bbe57eb915eaa09084c67b57d0c4fee8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1393781d7623e4fcf8ab599d8591e32ede8f54ff2476af17600821c1310acc0`

```dockerfile
```

-	Layers:
	-	`sha256:4418ac70f1828e832a87b372b6c622992d41da35cee387eba1e6315d909595d4`  
		Last Modified: Tue, 30 Dec 2025 03:26:00 GMT  
		Size: 10.5 MB (10475969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c83effd6df77e320910a28d105e949a1b9f1de1679ae8284bf2831492a73cc4`  
		Last Modified: Tue, 30 Dec 2025 03:26:01 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json
