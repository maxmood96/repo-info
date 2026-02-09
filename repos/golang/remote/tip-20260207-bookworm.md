## `golang:tip-20260207-bookworm`

```console
$ docker pull golang@sha256:3884bbe6bfb4e22e8377a98d5b8e40e61dba9166666acc9647c0b0a17489517c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20260207-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:aeb61252abedb1c88460999038b58f893c7cdc92ef5b3e6c6fe3224a6f6b2bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.8 MB (322822882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d483ebd26e355889f199aad9ec4cf2078e9a138f36a9a5a951b6df40e92d08`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:01:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:03:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:03:23 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:03:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:03:23 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 20:03:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 20:03:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbceb003542957cee7df7b79249eaf0a71d21c5203d086969b565fb6dec85d86`  
		Last Modified: Tue, 03 Feb 2026 03:28:33 GMT  
		Size: 64.4 MB (64395971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5794ec0a150c0fc4e7463b8ad68754314f3c7c16b5909a3144a558ec10f1090b`  
		Last Modified: Mon, 09 Feb 2026 20:03:51 GMT  
		Size: 92.4 MB (92444806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72ac0d50002cbee1e950896b157d609a44688d9a2715460c4e3c92d9a126868`  
		Last Modified: Mon, 09 Feb 2026 20:03:44 GMT  
		Size: 93.5 MB (93462017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc47b64fcac1e250861d077103d5728c79f2d723f14506b5302121df363fb8db`  
		Last Modified: Mon, 09 Feb 2026 20:03:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:599345665c11ee0f8c495412180184aea0952c47079d38740df8d71ef2a2ff04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8605b54af44f519872e0de18eaac2af7e7d96d538d1de65e243e9fb860d412b9`

```dockerfile
```

-	Layers:
	-	`sha256:cd003e486b64b4ede5e8b5c87ab709eb38a6f8194dce597bd9bccfa3bb9d18e5`  
		Last Modified: Mon, 09 Feb 2026 20:03:49 GMT  
		Size: 10.5 MB (10497031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:361082a1069e680530f0695ed6eedb282efbe6813d8c2adeeb893973f0997f3b`  
		Last Modified: Mon, 09 Feb 2026 20:03:48 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:a27244845038c17069e9d63210f84427d58914c38a0c0f494f61bc45cf1695d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.7 MB (281687063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca6612960f06cf919f8a6c891c453dadf8afc86c51305e1f1ea058823fd48d2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:59:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:56:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:58:40 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 19:58:40 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 19:58:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:58:40 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 19:58:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 19:58:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:424cab4c9a6a41cd57ee6de8e95726c4d76fe3e913bd9c7731865fd244771971`  
		Last Modified: Tue, 03 Feb 2026 01:13:26 GMT  
		Size: 44.2 MB (44198733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7fc27aeb6b79b5764735a819c5fdf5feb13c904bdffa0dee2b4c1c5f3935e7`  
		Last Modified: Tue, 03 Feb 2026 03:30:05 GMT  
		Size: 21.9 MB (21942045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb0551578bad740c3a20b6a29166ce3ad8980e037c23d30c90a060f62da5338`  
		Last Modified: Tue, 03 Feb 2026 05:00:10 GMT  
		Size: 59.7 MB (59651962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811c1458275274d8a34773c4b1735215cc5a396855f5eebafd0b870d5c8a1b38`  
		Last Modified: Mon, 09 Feb 2026 19:59:07 GMT  
		Size: 66.3 MB (66310494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b60c394ecd04fc3ba572f8a2c09a22e7e8c913f51a7766b230d8afa0ed0ae01`  
		Last Modified: Mon, 09 Feb 2026 19:59:07 GMT  
		Size: 89.6 MB (89583671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5895a3b1addf75f160bffcf94951f60416b8b888b5227efa6caf6c6106b076d`  
		Last Modified: Mon, 09 Feb 2026 19:59:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:fde0ea7177b17515da57d67c3f884a9e24193e308c6cb5b174df7f202a3e7bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1233208fc4cb41152647e726bc05754c97502f75c91a1d2769c8d8b4735cb95c`

```dockerfile
```

-	Layers:
	-	`sha256:f6b75647abafcb6007ab2889bfe7387e06880e7230f1aca01a637f3b71891ad3`  
		Last Modified: Mon, 09 Feb 2026 19:59:05 GMT  
		Size: 10.3 MB (10303727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12ef3929764fde8b39d9de902fbe307afefe98b4aed1d12664c72224c0cf186`  
		Last Modified: Mon, 09 Feb 2026 19:59:04 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:89149d047c62d6112756dc526901fde6b7e5136718563d1e11deaa51d8784cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.4 MB (311449986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24cfe7f24ffd9f0e85bb1a81f1cb03f3c0c7d893aa011e40ceb2d6b9c1de426a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:01:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:03:12 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:03:12 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:03:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:03:12 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 20:03:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 20:03:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e9aa4982c2a67e202ea283fc3760e94d8d8b16966c616e01ad0238abbaac82`  
		Last Modified: Tue, 03 Feb 2026 03:46:50 GMT  
		Size: 64.5 MB (64479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f11ee8a2647f63bdf0ebf01ccd5ecdbc53eb4d332e7ad9093db64792f370fe3`  
		Last Modified: Mon, 09 Feb 2026 20:03:40 GMT  
		Size: 86.5 MB (86525222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700ae6b9569c22fdb680312e3253454dffff750989d3faaa4cebeb6c55de9593`  
		Last Modified: Mon, 09 Feb 2026 20:03:10 GMT  
		Size: 88.5 MB (88474120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123af99a3ec4b26a549e0cad33cc611ac382ac6de386b21185e7d07e277962b3`  
		Last Modified: Mon, 09 Feb 2026 20:03:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3ae61f25bb482056f83483e4d29867055958cbfc157b04004524d556080951d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456a5d6ddcd028d038715f346c22e709833877dce31aa113848942560169f568`

```dockerfile
```

-	Layers:
	-	`sha256:7b1c0b32d4d8813aa4771a4859d081e82d8a5b8836cf35ddc18791685e33e172`  
		Last Modified: Mon, 09 Feb 2026 20:03:39 GMT  
		Size: 10.5 MB (10524855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30751f22f541a83afed0577ca70e26b29fa6a9bf2fdfd59502be17ea8bfbfb59`  
		Last Modified: Mon, 09 Feb 2026 20:03:38 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-bookworm` - linux; 386

```console
$ docker pull golang@sha256:10d417c62a6488d0ad73f47f32d4622ddc3d7370703f3e630ec3a0ca554c096b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (321965958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8166a05ff3e338dc022852b8dc12060341131d352724fd0dc687c4810aa7283`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:24:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:58:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:00:16 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:00:16 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:00:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:00:16 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 20:00:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 20:00:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a7f977a794a5fd56ece19f51541cec3b8ba447f10234ab001213bf850f92f64d`  
		Last Modified: Tue, 03 Feb 2026 01:13:34 GMT  
		Size: 49.5 MB (49468454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50ea552b26a58c13b4166d933269500891fb4897db09bc72d932372276b158f`  
		Last Modified: Tue, 03 Feb 2026 02:49:31 GMT  
		Size: 24.9 MB (24872100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc15e0cd687cd62190081200fbe30ab5102ae840cc68b0386259c387aef2b9a`  
		Last Modified: Tue, 03 Feb 2026 03:25:00 GMT  
		Size: 66.2 MB (66234564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8150d8952b381ee5027c94d82c3f0ca4d1f763234bb3f53d2ab8e14e94275467`  
		Last Modified: Mon, 09 Feb 2026 20:00:47 GMT  
		Size: 89.9 MB (89871432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9eeab623b500684be7941586d4f5950cd5be2f0139f940b2104a8b3b5d40cc`  
		Last Modified: Mon, 09 Feb 2026 19:58:40 GMT  
		Size: 91.5 MB (91519249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e5556f1a1d8619ecf813db5aa9bc91748c7b4d61b3ef4f079ce4285ed938c9`  
		Last Modified: Mon, 09 Feb 2026 20:00:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4f201c2e7a1e00c502ee1856c9304baf9d867211b09ef5adf2475315ca437920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6084488163c072bf958a5d62343465a48c91d9d34893ac8e3d2e058bbf5651`

```dockerfile
```

-	Layers:
	-	`sha256:bb85f8c043d1b69a7ddf804f9dcc2a9745ef36e766dbbfa80295ffbed57b2090`  
		Last Modified: Mon, 09 Feb 2026 20:00:55 GMT  
		Size: 10.5 MB (10476611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a471aeb8f48a7a4843569847ad16499484afb8e837e86b577776f76e169dddd6`  
		Last Modified: Mon, 09 Feb 2026 20:00:45 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:f98c183d66f6c61e03f478cd8ea4205665b8ba726653a4d1df8118f26fb970d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.0 MB (292984683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9070f918e317c6ab1b0db26dbdd191dfff28c5602f59dbe369a52ef45460cf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 16:06:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 21:28:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 22:18:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:20:30 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:20:30 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:20:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:20:30 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 20:20:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 20:20:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:001d31ce76be3df3174382025b0b9e2985ddc96d785143497e14a46cdcdcf951`  
		Last Modified: Tue, 03 Feb 2026 01:12:32 GMT  
		Size: 48.8 MB (48763257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e910e12f1ba466db5d640f799037fd1161885165d6ef1a46de53b55b08cfb02`  
		Last Modified: Tue, 03 Feb 2026 16:07:24 GMT  
		Size: 23.6 MB (23615398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e0ad746711a3754afd4dc1df1be9308a858da3b48f46cc1d318cd1dbf2cb47`  
		Last Modified: Tue, 03 Feb 2026 21:29:58 GMT  
		Size: 63.3 MB (63310108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2164c80380b0dcd60ea92fbd5645d9478bdfb6a0b5dfaabf0daa2a974ecfb949`  
		Last Modified: Tue, 03 Feb 2026 22:20:18 GMT  
		Size: 70.0 MB (70021714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2941bc26ecd1a5504138788ecec8521b1cfe7a3f3f863ffffca2809c5df941`  
		Last Modified: Mon, 09 Feb 2026 20:22:42 GMT  
		Size: 87.3 MB (87274048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d861435e1d0a2c911db9037d5c879172be967a1e656857f44071e410e4e4690f`  
		Last Modified: Mon, 09 Feb 2026 20:22:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2aec4a8f43c759da8c6771111b28178fda52006e6bc97896df6b663d1229b245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c95090cf40fe4d8b1735dbfabf233fba33b2b11e6d5d6a941dd13a93876691`

```dockerfile
```

-	Layers:
	-	`sha256:5da9b7798c848694fca0bd77502bc225005492ff11be6d0a71c031e2b8cd8808`  
		Last Modified: Mon, 09 Feb 2026 20:22:32 GMT  
		Size: 28.2 KB (28239 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:76da6c8dd1b71b1dec056c6cbdd2d0fa935a4f032191416ed4b65e84762d4b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328402975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b9eb44869e3f3f7f9e2704caa11204a2dc3c37302f8984c1b041ee4bfb2cc1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:22:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 10:35:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:26:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:26:29 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:26:29 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:26:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:26:29 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 20:27:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 20:27:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1311f6670d65067c1adb8d518ab8836a9d3d42058afdd776824845f91935c9`  
		Last Modified: Tue, 03 Feb 2026 05:22:25 GMT  
		Size: 25.7 MB (25671343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3c21a9818f8ca2f73ccd29b595b5a2bc7818b3057c3895ec555bee901eb365`  
		Last Modified: Tue, 03 Feb 2026 10:36:21 GMT  
		Size: 69.8 MB (69846016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bf9d9076f39b8e2c0aced7f1f28dac543d58a8aafe215df11bf80a17810efe`  
		Last Modified: Mon, 09 Feb 2026 20:28:08 GMT  
		Size: 90.5 MB (90451427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f34b281626db46d13e5a751b54221f74b1d0be2bfad3701f6dc696782f8809`  
		Last Modified: Mon, 09 Feb 2026 20:28:07 GMT  
		Size: 90.1 MB (90106742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339cfadcf20d903a47d690dfd9f21897f8f86a35c7a28fbf8fd9c48103eaf27c`  
		Last Modified: Mon, 09 Feb 2026 20:28:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6522bc3c2d078ba3c7703b059762b29bb1982df055062cabb190a7b5dd502da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563abcf7bb80169c23f47293d4c483682d112d0c449e48424a445e3b08ac2230`

```dockerfile
```

-	Layers:
	-	`sha256:8b249963a210a1db618bcc5e9c733265cc2a096f2d680fd7b596a5d5a695ab57`  
		Last Modified: Mon, 09 Feb 2026 20:28:04 GMT  
		Size: 10.5 MB (10469516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22ff7c524d60b66e18d7f55f741499c485feab7aafa3f73de3ea190223825e88`  
		Last Modified: Mon, 09 Feb 2026 20:28:03 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:5d0a7da6bc8fbe94bd4c1b3733e41e727f5f1f2c761494eeceb7a59a7e3733a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296367507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f75bdb0d6fe63fc542f56ec353f8b7c7f719a8ae42cefba819b7ed766e859e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:28:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:00:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:00:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:00:01 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:00:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:00:01 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 20:00:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 20:00:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3072e3eb8c224dc593a4e18a3785b06d51467102b1cd9dd426d3d31d0e6831b8`  
		Last Modified: Tue, 03 Feb 2026 03:44:33 GMT  
		Size: 24.0 MB (24033633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61724404ca7e7ee67a943113b2e679af71546a07f66af094570e811bbc9fa743`  
		Last Modified: Tue, 03 Feb 2026 05:29:11 GMT  
		Size: 63.5 MB (63501320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be60f9687e53e1d931599c2c97d67403bb6a6a87fba5a8672d8f14c72b51e5e`  
		Last Modified: Mon, 09 Feb 2026 20:00:52 GMT  
		Size: 69.0 MB (69045163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b9ec9ce8a3837e5750bcd10b11df694113758518fac79cbd3aa70f831f2db7`  
		Last Modified: Mon, 09 Feb 2026 20:00:45 GMT  
		Size: 92.6 MB (92648889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79fc8e988c972d4fb98e4774410a8e4d457ae2f49d884af58cf3ec6766758c5`  
		Last Modified: Mon, 09 Feb 2026 20:00:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:d233c708816832fb1ca105f2ac23d62b5df5c5414e4448eb90287c9ba07657f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9675a98cb64312ef76cca49173a06c76eee7bd636ccc70ed0c22df39c4e3b8ff`

```dockerfile
```

-	Layers:
	-	`sha256:a01f73928ba67c7a9fb676501919e7c4accad9e9e4fa6ef96f99a9bd0a94abda`  
		Last Modified: Mon, 09 Feb 2026 20:00:56 GMT  
		Size: 10.3 MB (10328789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7249f0698428736ff1d4106e4b608d0e792eb6c2fb24c4494e3b96db9880beaf`  
		Last Modified: Mon, 09 Feb 2026 20:00:50 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json
