## `golang:tip-bullseye`

```console
$ docker pull golang@sha256:fb7aee4b240b71ae8a9658ea23b86bce6139916cfafa52149ec57f9544e964f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `golang:tip-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:ff3dc79903d27c231836e26703eac3cdfa3fa26da6a8af12d5a6159be2d852a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 MB (293384871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70a3f353d1716c4b949b8bef48c2a7858d79f9e989407310b68c275d9097a1b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06408a499c9b569e198473b636afa8c383e459ee6fe76ba4159b758c84e68f10`  
		Last Modified: Tue, 01 Jul 2025 02:25:30 GMT  
		Size: 15.8 MB (15765336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06772a4eff3df697497bb68b4dcdeb97fdb9338b5e7dde7d1a53579c3203c9ba`  
		Last Modified: Tue, 01 Jul 2025 03:20:06 GMT  
		Size: 54.8 MB (54757481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff65fddaabf9d1ab419a7611f4352d6a200e90398c81625e97d7c84c582ff29`  
		Last Modified: Tue, 01 Jul 2025 05:15:15 GMT  
		Size: 86.0 MB (86022019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d8f8c49f445d30fa7cd4c028a18d5365e5bdfe97436ef61eb7709425c99cad`  
		Last Modified: Mon, 30 Jun 2025 17:30:36 GMT  
		Size: 83.1 MB (83085055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fd6e5625907470d516bf6869aa8d91c8843d66f479600cdbd06dc61292dd8e`  
		Last Modified: Tue, 01 Jul 2025 05:15:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:2ff1f12235d1ebb43bae29394d1073667012393f95cb25547d777e3742c36e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10509221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beef52f5132fa95e835ce57e27317b1c7754daa05b10674b8c8661f1830b7b14`

```dockerfile
```

-	Layers:
	-	`sha256:00c619bc9c56e49fcfd8af275004e70d2a6b3ade863e5d496977726a52072edc`  
		Last Modified: Tue, 01 Jul 2025 08:23:57 GMT  
		Size: 10.5 MB (10482164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91c40bbfca6acdbec1353afe30682eb0931a03efe0c47db31cc2777d245ca5df`  
		Last Modified: Tue, 01 Jul 2025 08:23:57 GMT  
		Size: 27.1 KB (27057 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:3886292f77800645d840009c376da1ae48b08ed8d9b01cb4ba3c73522fea9fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259661368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0a966b5d92dfbd678a81e68e70d0197ab920ffa9f80cc479b971c636d550fb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c43258def9bd93af20e1c5bd4e42a71d9db281a9fc468bbb5eb78d7a51c6472a`  
		Last Modified: Tue, 10 Jun 2025 22:47:56 GMT  
		Size: 49.0 MB (49043954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319bc9ba38020b34f4e3f562e110c9ab25e658493eaf95bfc783a633f2d4b036`  
		Last Modified: Wed, 11 Jun 2025 20:11:47 GMT  
		Size: 14.9 MB (14880672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc07acb5bb3458d1880be716fdb2bcc90e78327b21f1c1531b5e4bd0941213a8`  
		Last Modified: Wed, 11 Jun 2025 13:12:55 GMT  
		Size: 50.6 MB (50630824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f7feeb0b6a1c7b2f8058fc4bcf8523950540bd39c01231df0b01c7791add68`  
		Last Modified: Wed, 11 Jun 2025 18:28:34 GMT  
		Size: 64.9 MB (64942390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6586f6a3b72edca5355ba2231baded357cf799f55b8944edc8ae75b0c7b67acf`  
		Last Modified: Mon, 30 Jun 2025 17:31:46 GMT  
		Size: 80.2 MB (80163369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be63f93a75831bb3cbe2364b60cedca7d06c643c073ecaf72e637e23a317eec9`  
		Last Modified: Mon, 30 Jun 2025 17:35:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:f58ccc8703c8ae6e5e95c2999e95c73493210ff37d19c59ce9e6fe27f06f6f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10316329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef442bdbfd4bdb2cc383499fa57e9863bffdfd80c19514a2dbc21f6e1645c6a`

```dockerfile
```

-	Layers:
	-	`sha256:e297eccf639db4cfe39e2f3ebbb2c9d4f81ef0e000327d514a087fbeb190a3db`  
		Last Modified: Mon, 30 Jun 2025 20:25:17 GMT  
		Size: 10.3 MB (10289165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0c8a5c321facf3ffff7ccd044500c0bf3ace88d0fba226c69340ddde4c7e554`  
		Last Modified: Mon, 30 Jun 2025 20:25:18 GMT  
		Size: 27.2 KB (27164 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:92598b39367549813637f4b3344f102883bcca8684962e912b205f32d44ea0e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.3 MB (283345781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a3ac2f410d9dcd124a32d51993fdea78de9ac89bb5bff1dc71e2077f4c3e44`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6f3b6fbce84c42871ea80f05b2c61e622e08647f7164e9a95a391926c1f714`  
		Last Modified: Wed, 11 Jun 2025 02:56:50 GMT  
		Size: 15.8 MB (15750566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7850095446c84fa9107622e378378aa7daf4b928caeecbc1149118900d32f7`  
		Last Modified: Wed, 11 Jun 2025 10:33:17 GMT  
		Size: 54.9 MB (54853082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de44d5956aed85d3d6d2c696b8489053af4a6a4d168314e425819189773cd2fb`  
		Last Modified: Wed, 11 Jun 2025 23:10:33 GMT  
		Size: 81.4 MB (81431904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f0e5c856fb20135c901f955406b40129ab946b3615cd5e0d5839e969930423`  
		Last Modified: Mon, 30 Jun 2025 17:34:31 GMT  
		Size: 79.1 MB (79057770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22dc9b5a9728d8f4ad9b9d089d8c95beb611c03e6c20459aa655d686913b3f2f`  
		Last Modified: Mon, 30 Jun 2025 17:36:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:5115d479328cbcbc5c38c36121898b50dab295f2b973110b01ea7fa12effa80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10510640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e42f92d0daaf72475c8f678cb124f438ef4eca00dd72f4251a9194cc9df87db`

```dockerfile
```

-	Layers:
	-	`sha256:087e937579aa430df1087aaa5834342106cbeb729855ff4f0bdab50ff5a338c6`  
		Last Modified: Mon, 30 Jun 2025 20:25:26 GMT  
		Size: 10.5 MB (10483447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50da57d1ec156dfaa94169446f0015045869cfeb18919ceae9ab2d0b2c7e9ed6`  
		Last Modified: Mon, 30 Jun 2025 20:25:26 GMT  
		Size: 27.2 KB (27193 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; 386

```console
$ docker pull golang@sha256:3ad8057ad2478d964b22cdacad9f99771a0d000684d14a95394ec15276acd6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296267176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03987f68f49b93dd9d7e230b8df34508f09059561312d1bf9afad6b388c1544a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7813ab6958459e0b769c4eaa51def1096dfab337ff7338a6ea28a8bdd9011dfb`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 54.7 MB (54689934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113be81052ec8e8323c4db158dc9c99295355934e950a6367e5c27038fd1e04c`  
		Last Modified: Tue, 01 Jul 2025 02:24:43 GMT  
		Size: 16.3 MB (16268907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05b439f6df174e28bd21dc59eead603def3bcbd47ec6462f86b7758c4db6ef`  
		Last Modified: Tue, 01 Jul 2025 03:19:57 GMT  
		Size: 56.0 MB (56049937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95b49fca8027ab7ff6fcdd95e09620be08d40cae5cdb0982de9e99ff60677de`  
		Last Modified: Tue, 01 Jul 2025 05:15:25 GMT  
		Size: 87.4 MB (87448098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb2781a7c01ceed520d1e8478386c7e0683cbeab9ca6a32207c24229a367897`  
		Last Modified: Mon, 30 Jun 2025 17:31:11 GMT  
		Size: 81.8 MB (81810142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f3d143b1a70367f9c9c4c3edc03d3cf2f999f88ea5ff1b3f05c3208a656385`  
		Last Modified: Tue, 01 Jul 2025 05:15:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:1b7121e99bd45901279da58dd64fda8c600f86230ab4f6e049ec05c9c72c5b9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10498525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584e1ed686d3291a29fd4c33cd2721fcc201c4c2f53cb6e99256961f3e906c7f`

```dockerfile
```

-	Layers:
	-	`sha256:02d2f4b2eef50b5971326528c1845cf5eaa7c65f2720bfde53f4031e9dfb8099`  
		Last Modified: Tue, 01 Jul 2025 08:24:18 GMT  
		Size: 10.5 MB (10471501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9a07a4887aa66e15ba9832ce6f9d049d373710043808e963aa98a3670dd7ebb`  
		Last Modified: Tue, 01 Jul 2025 08:24:19 GMT  
		Size: 27.0 KB (27024 bytes)  
		MIME: application/vnd.in-toto+json
