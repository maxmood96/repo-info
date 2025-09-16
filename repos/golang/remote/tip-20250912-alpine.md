## `golang:tip-20250912-alpine`

```console
$ docker pull golang@sha256:255c9c70649330a9df85650d0eeb03350375a7c366bf4b5a3d06ac7f795526a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20250912-alpine` - linux; amd64

```console
$ docker pull golang@sha256:94f6cac365498736e4785285b4f2ee84f9d82033dbeec9bb879fdb81a595e9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87767466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a22e8cfcb7461af856402a26925cad0ca1af817f1f88858ec8c2d412cc88b598`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 15 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 15 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29199d42b6c7b094e9f97f689c9fc75c18abe6a015ab431641b0c450cb5f5e3`  
		Last Modified: Mon, 15 Sep 2025 21:12:36 GMT  
		Size: 282.4 KB (282449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8084ae79718311fedfafbc5a50335db8ff6184359260f7408a58117f5eecec`  
		Last Modified: Mon, 15 Sep 2025 21:12:40 GMT  
		Size: 83.7 MB (83685170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49a9a06c34b13d4a0aef368aed5f69b10bc4b01e7b4d2124aab1e598b4f861d`  
		Last Modified: Mon, 15 Sep 2025 21:12:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250912-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:cccae355c51d0b51859e49232be0394f93abdf007223727fb9ad0889b5455408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 KB (216665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a0c02f36eb68359d6a1205b4eb889659f0957331f01507ca6453699cd51e09`

```dockerfile
```

-	Layers:
	-	`sha256:6d1d861403ab20c62d51b487f158f1d70204d3dd77b111e2eceebbd0bf9cccb9`  
		Last Modified: Mon, 15 Sep 2025 23:23:58 GMT  
		Size: 191.5 KB (191527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d15d5701d13195e8115989a97b3ee542c8fa349c3661b27bda3eb84b05ff5354`  
		Last Modified: Mon, 15 Sep 2025 23:23:58 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250912-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:029d64d1c8b1a4e0334b9f397be9ad89a5f6bae7ca2dcc0816c49140dc432352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84746832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1840722c1ae93bae45ff0ed0cc37b626a86ff35a8c14325d05ccd787451c9d64`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 15 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 15 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2908e7f4eb6dac91fca6e7603888c684784c96b933344a09844a36e787d3852e`  
		Last Modified: Mon, 15 Sep 2025 21:11:45 GMT  
		Size: 283.3 KB (283333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b6aef09b857a662fce335473067e4c5ff59770662b877b890d536ab7f7b075`  
		Last Modified: Mon, 15 Sep 2025 21:11:56 GMT  
		Size: 81.0 MB (80962431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810eb968948b5fa48f1053ae86f22cd8acae872cca65e6f1609e22bb5661d077`  
		Last Modified: Mon, 15 Sep 2025 21:11:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250912-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:3acb5dab14671710dc05cc106f49219151a96b640d307e8d6c8763f382c0bcb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd5a9ca561b5e35911208fbcef6736b4a130f2ec31c12374e0944d1f840aafc`

```dockerfile
```

-	Layers:
	-	`sha256:9a71264077179a59009c7a0ec73c65becfd16dacafca4369c560bf54c8393cc5`  
		Last Modified: Mon, 15 Sep 2025 23:24:02 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250912-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:6aa9a7cbc65d11b2b340c342455f98d38d758257e920e9f7c20c778efa4c8c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84233443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3bcb2de4af9b9a54660ece3e3ca0c0728bca1916dfdb159d37e7f956ea7638`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 15 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 15 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23466287babe7680e5099b5607e8c030ee8e6274bd1f4ccee7e0e98eb4379590`  
		Last Modified: Mon, 15 Sep 2025 21:13:48 GMT  
		Size: 282.5 KB (282500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b987a50b9955c225cc2849c41b467e101fbe92c91e3dab2be8fb2645bad265`  
		Last Modified: Mon, 15 Sep 2025 21:13:14 GMT  
		Size: 80.7 MB (80731747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd66f1a5e327e145bf2b9dbe51eb826f4f89063597a63400acbeb7770a3f39a7`  
		Last Modified: Mon, 15 Sep 2025 21:13:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250912-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:fb6195d9ea12388afb15a2305be6884becbe714d409a3166d5d43f8a05b16f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f455d31e15287649253b3aa558e83a01b970cda0e1397fe9cd7732687dfe7755`

```dockerfile
```

-	Layers:
	-	`sha256:5f4dfc953cf2bdf9424f4c59bda4c887569e1d2ed7792c900a9f3d88287df79f`  
		Last Modified: Mon, 15 Sep 2025 23:24:05 GMT  
		Size: 191.5 KB (191549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb75c01a4e78b10aa73180bb850baabc54f87d2dcc1c2ffc00553aaf1025f2f7`  
		Last Modified: Mon, 15 Sep 2025 23:24:06 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250912-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:e09a34c0c86ed0a44abeaf089e223d232334f73160b5093385c78ef776d4ced8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84094361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9eeb92a53c6f501e6c3ed0d041373edd59e78f0ba152e6926911016e021d33b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 15 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 15 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5aca16c3e446f779a381c14508d0cdf509d760c746295e64ecd54044607c71a`  
		Last Modified: Mon, 15 Sep 2025 21:11:37 GMT  
		Size: 284.7 KB (284707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53a2c01c0918250210240d30defa285fe0edf22dfb1aaaf2291b5e92b61a74a`  
		Last Modified: Mon, 15 Sep 2025 21:11:43 GMT  
		Size: 79.7 MB (79678746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394fa75c9e1147a9926f0057f18a49ce7a97cc9b52f81e25fda8d1aeb85cbba0`  
		Last Modified: Mon, 15 Sep 2025 21:11:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250912-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:b013263f604e4422d24d50eb59c692211316307a9ed91235076768efc963ac67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 KB (216881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6e492d67605a6ecddc9cfd636b3f8866017d9645f1910007afec5d0d31271b`

```dockerfile
```

-	Layers:
	-	`sha256:b6ab5466df82b6f1090a20d89513a7ae90abe3234c8abeaa61c81cd6d4ce44b6`  
		Last Modified: Mon, 15 Sep 2025 23:24:09 GMT  
		Size: 191.6 KB (191583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c830d053c15c51159ba85c1f9f315c387499ea7029bdf2297903a3b7ead2c8a`  
		Last Modified: Mon, 15 Sep 2025 23:24:10 GMT  
		Size: 25.3 KB (25298 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250912-alpine` - linux; 386

```console
$ docker pull golang@sha256:fcdf78d0c7dd87bb456403a11f0db5c4180c2371ae65f9a37127d58f7b107020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86270483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ecfa0c331273daf2c35f031ace94384129ec6a33a58629a43a2c3923d95937`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 15 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 15 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014254cf66a34f1019262bf7a5b67c107165afa4b700a309547ced270cc292c1`  
		Last Modified: Mon, 15 Sep 2025 21:13:36 GMT  
		Size: 282.9 KB (282927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2aca1e976b6789d4066cf350d8d9b9afb301f494e0c2483f001f1e2c4a7034`  
		Last Modified: Mon, 15 Sep 2025 21:12:39 GMT  
		Size: 82.4 MB (82372393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9908455ba9492f2aa101b50607fb4dc47cbce1c85426b297f2271d5ef8e248c`  
		Last Modified: Mon, 15 Sep 2025 21:13:36 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250912-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:61e9f374008171809f86ed7ce4361f0829965850e33d8a746e6f50555389d710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 KB (216582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab12d2e5527a61eb37bee3e6f518707cbc81c32e53aa26cc053a54f3f786034`

```dockerfile
```

-	Layers:
	-	`sha256:db8feca8668a867281d00d4e3e2dc70816a9c54b7485fcacd0a0f055f1906cf2`  
		Last Modified: Mon, 15 Sep 2025 23:24:13 GMT  
		Size: 191.5 KB (191488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fefd5ff3efdc1d415a8644ec100dce8e195a5034476d3a94e3e2f459f8b765e`  
		Last Modified: Mon, 15 Sep 2025 23:24:14 GMT  
		Size: 25.1 KB (25094 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250912-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:1ce201bd9a69b33eb97993a25891d74e6aca9f97c7bf4441b3892faec0b54b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85050819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b681797e1c6837200761c071e59b1b5874477e9a29f626f1223c211ce24756b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 15 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 15 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8093a8784e85737b54c7bd288e58eb1c4d919cf932185be9835fe0acd194ad05`  
		Last Modified: Tue, 02 Sep 2025 17:37:11 GMT  
		Size: 285.1 KB (285121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0eb324782f5e8e3887f0d55cc6908c033fff6444770b36972445edcc39d815f`  
		Last Modified: Mon, 15 Sep 2025 21:15:44 GMT  
		Size: 81.0 MB (81038429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592f86ff8327f39dd92f46c918948763d9171cbd1d044b9021c835ff2e7792af`  
		Last Modified: Mon, 15 Sep 2025 21:22:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250912-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:d84833ab9d2172b202e9b7df99a4ddedae374d2d4ca6a901ad29353c5df3f68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604241d322554e4693054d5bdb87dfcd8d93f66295bfc88526a24168e99240a3`

```dockerfile
```

-	Layers:
	-	`sha256:a39462697621f0cc6084ae862ff13cc20c3848cfa31656883a0490d305d92006`  
		Last Modified: Mon, 15 Sep 2025 23:24:17 GMT  
		Size: 189.6 KB (189624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad05ff67c62d9af4260008bbba99f1ff5dfca662ae2f6488b007b577e770718b`  
		Last Modified: Mon, 15 Sep 2025 23:24:18 GMT  
		Size: 25.2 KB (25195 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250912-alpine` - linux; s390x

```console
$ docker pull golang@sha256:c0ff90e968d1e837785020d8e835acb9247c3176939938201a041ebaecb296b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86186687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6636fa735989898832a7318006321ebd00d930173286f8003fd36fd298a96a18`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 15 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 15 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82129bb6bf719d3efe5e37bbda9c61ccb03eefc8feac9fceac09035731c0c7d`  
		Last Modified: Wed, 03 Sep 2025 20:46:26 GMT  
		Size: 283.5 KB (283475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59bcd7ca863be9aebc61665811bb8814298aa2a6542f87325c4770560068944`  
		Last Modified: Mon, 15 Sep 2025 21:20:05 GMT  
		Size: 82.3 MB (82258083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3df22214f7726dc42eb5a8d4dd7a43a5253a064e2d42e1fee63ca4b294990f4`  
		Last Modified: Mon, 15 Sep 2025 21:31:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250912-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:06a7f161ac77ef5ff00d98ca24c437d1853b529e3c316af6a5591ac0a3fdd44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.7 KB (214714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9902389f4d95f2870209c2349c83d1a6eb35d441ee18f2910aa3e3a8d2c8e2d`

```dockerfile
```

-	Layers:
	-	`sha256:8a5c171bc7e770909d27198c39afda0a09b4426070191009c805c7d7895dd4b0`  
		Last Modified: Mon, 15 Sep 2025 23:24:21 GMT  
		Size: 189.6 KB (189576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3743d3f5189b6392a4855f02eaf6fe97cc6adc2ea706707795b711f314193293`  
		Last Modified: Mon, 15 Sep 2025 23:24:22 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json
