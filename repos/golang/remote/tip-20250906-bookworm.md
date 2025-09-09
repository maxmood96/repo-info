## `golang:tip-20250906-bookworm`

```console
$ docker pull golang@sha256:4869140da4b2b3c65173a751d7060d5932c523195afa6605aef228a0e58272c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `golang:tip-20250906-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:11b571368290f91aeb0e6fc180c482dd61c523ffa3bae838027e511d83ac9a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.9 MB (312916261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe6eea6736909aa6682acb9f2f727a227d04a4ec280cfe94d3f054a9a7fb37f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 08 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5073558d5a5274440fddfe987f56645dc90b8b84481e9e3dc858ac3311e33e`  
		Last Modified: Mon, 08 Sep 2025 22:13:51 GMT  
		Size: 64.4 MB (64396915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c418ef4a1a0e3743573d619edd949a839a9bc4036c7ba90b1fd367157b4ab68b`  
		Last Modified: Mon, 08 Sep 2025 22:42:33 GMT  
		Size: 92.4 MB (92385940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981ded06cd7fc4272134c8fd8dd6fe01e98f582c7adaa60ab9166ea8bfd71723`  
		Last Modified: Mon, 08 Sep 2025 22:39:32 GMT  
		Size: 83.6 MB (83626642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996ee3455ba7adb88c17ae922fe81fe99fa16555013fe37dca072c6e01a98ca7`  
		Last Modified: Mon, 08 Sep 2025 23:36:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250906-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:7bffa2886359d91c1d83226c9f20b49f8f0f1dccc9cb167069aef31231621716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10523344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c28a9f882525732dc4893868ea701a84a16f2c169a0bd561fec950ecba1df5`

```dockerfile
```

-	Layers:
	-	`sha256:b508da0c46c3fda625e18f206c8934bd527e32241ac4417cb1091495ce25129f`  
		Last Modified: Mon, 08 Sep 2025 23:24:42 GMT  
		Size: 10.5 MB (10494916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eeaef9d01b6596c7148adf050e08bdc7915c02996776704e620a384a2ae250e`  
		Last Modified: Mon, 08 Sep 2025 23:24:43 GMT  
		Size: 28.4 KB (28428 bytes)  
		MIME: application/vnd.in-toto+json
