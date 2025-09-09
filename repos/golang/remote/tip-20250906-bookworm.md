## `golang:tip-20250906-bookworm`

```console
$ docker pull golang@sha256:9c48511d00efe13d7599c5ab7e16387cf96dbd46ec832ff8d6b80373714eac94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; 386
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
		Last Modified: Mon, 08 Sep 2025 23:58:50 GMT  
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

### `golang:tip-20250906-bookworm` - linux; 386

```console
$ docker pull golang@sha256:666d64b900bb993cf5f91663558babc40a689ff4886cc5619f587da2456147a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312658274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4304a22571ba17f06155a9f2af5aa5d407c120d1fd7dee1100dbf3f6d5cdf21b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
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
	-	`sha256:5538e96bb7df1a7ef01bd7fcbf51f4cbc041246109c06cf661f7058c203851af`  
		Last Modified: Mon, 08 Sep 2025 21:12:26 GMT  
		Size: 49.5 MB (49466684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822d7073f1bfbc05d754234ff0c82bf81a44dcb6b19979f28688d3054a71fa6a`  
		Last Modified: Mon, 08 Sep 2025 22:07:56 GMT  
		Size: 24.9 MB (24860658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2248c0dfdaafb69ef95f2c3162eb9698e04d446b6646131ff2e543b79a6f79f`  
		Last Modified: Mon, 08 Sep 2025 22:39:17 GMT  
		Size: 66.2 MB (66233051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50acb439eee3e54ff7b408e815c7759ff6a3f373301ba7acf417dfa3ff1a3083`  
		Last Modified: Mon, 08 Sep 2025 23:16:18 GMT  
		Size: 89.8 MB (89807181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518dceeeab292a9ac96f797a930543374e02f8a442c539c30c018a2f30d27fff`  
		Last Modified: Mon, 08 Sep 2025 22:30:33 GMT  
		Size: 82.3 MB (82290543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a5ffac23f51bec07f6d54335e2b31951984ac49cfd3bd6378b5c78ba5a62ef`  
		Last Modified: Mon, 08 Sep 2025 23:50:18 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250906-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:66127c83e1c06cfb5cd8414b5390e22b690f8fb22acea3e06e7192cefd4897b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10502894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b66989091c2799ffb42a824b8bf8c4ad12b105ebe475f3e6e123ef7092bca5`

```dockerfile
```

-	Layers:
	-	`sha256:82b042dba56767013b656266c00383c0c8cdb8e93419d0e46690028d7a105027`  
		Last Modified: Tue, 09 Sep 2025 02:23:30 GMT  
		Size: 10.5 MB (10474499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b9a62982845f7aa1b583bbec19717b7d1e0af28aa6cb7f967dd25e26a96d98a`  
		Last Modified: Tue, 09 Sep 2025 02:23:31 GMT  
		Size: 28.4 KB (28395 bytes)  
		MIME: application/vnd.in-toto+json
