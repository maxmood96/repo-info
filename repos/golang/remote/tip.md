## `golang:tip`

```console
$ docker pull golang@sha256:0a97062d21d6392be9ae43141c608b832977cfd663b0e7c538edcdffdf7c3518
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

### `golang:tip` - linux; amd64

```console
$ docker pull golang@sha256:e893fca3b5461995d99b42209f46a9b890add024c64488946b5035e2dfe25318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.9 MB (355902901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895a791e48f69bf168e45b98ddfc94270bc664d837fa27ef8a88371e3150f2be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 28 Apr 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Mon, 28 Apr 2025 22:15:10 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dffcecd872244028b27adc31f32f5bfa758c2f04c36d93a08b4cf7bb357d8d7`  
		Last Modified: Tue, 29 Apr 2025 00:14:12 GMT  
		Size: 92.3 MB (92349590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65846c33088373b4d6ff39b83056f623dac3e1cb831137df32e4e70bf9d848be`  
		Last Modified: Mon, 28 Apr 2025 18:22:59 GMT  
		Size: 126.7 MB (126656346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a851cb9ba0dcc785189c8aa196549a4d8c17698c762e82762463341a2dec3b8`  
		Last Modified: Tue, 29 Apr 2025 00:14:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:1cdd7595065d59c418b7d436f1f02423300de609c5c24ac39d50be36b60629c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10299530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad5308d8b74a110ed8c98e5bd037fb6aeee698d2b23631ed32734b35942b783`

```dockerfile
```

-	Layers:
	-	`sha256:e182a5c8e1f8a8d35ec7e3459aeace6591f9323887734094a66133b757e8886d`  
		Last Modified: Tue, 29 Apr 2025 00:14:11 GMT  
		Size: 10.3 MB (10271868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf23d3612f35c9f410cd1d3ce66276b6d07874b74c70c6ac06874b3e9514e42f`  
		Last Modified: Tue, 29 Apr 2025 00:14:10 GMT  
		Size: 27.7 KB (27662 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:ad88a8edc19008227b5f90f5dd99763e3aa16a55af16265750e1ca06d3c3b751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313653027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13b85804bd15d153fce6a94c50ce1889d6ac5fd9dfbae96c02ee60fe49eaf3c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 28 Apr 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Mon, 28 Apr 2025 21:15:27 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Tue, 29 Apr 2025 03:37:10 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3553b1499305feec4f182c1e2562e06daaecb3dc337d83b89b8c909f46c0a1`  
		Last Modified: Tue, 29 Apr 2025 13:22:56 GMT  
		Size: 59.6 MB (59640211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6442f47db55887d087c4346d5fccc35d5cd8441653b35deaf402943d7978ae1`  
		Last Modified: Tue, 29 Apr 2025 16:59:19 GMT  
		Size: 66.2 MB (66222470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33618dace1ba528dcd7b40e80a4e895530a8d058bda71f5a87abf8312ed70c2`  
		Last Modified: Mon, 28 Apr 2025 18:46:15 GMT  
		Size: 121.7 MB (121674729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd529f3aac105c71f58deaf8291abb9b3843708e2a7e89a941a2d4c4592b3683`  
		Last Modified: Tue, 29 Apr 2025 20:33:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:eea724884bc3845e7d6929af6092e7d22e6e8b0999de32f3ae86938a659ade3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10107977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee43c5b21bf7f26e8bdf35cb61092ba3ea70e844801b4790082b404173f09962`

```dockerfile
```

-	Layers:
	-	`sha256:930066a38c2a3c33888c31c49f6f7e7c69448858f52812e2b30255caaa997dc6`  
		Last Modified: Tue, 29 Apr 2025 20:33:18 GMT  
		Size: 10.1 MB (10080190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5cb4e7035f681c11404cbc87cfb9731402f0405f9b289e75cb8418ecedafa4`  
		Last Modified: Tue, 29 Apr 2025 20:33:18 GMT  
		Size: 27.8 KB (27787 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c01ecb83875989a6f03818870e8bf5a1c2688db54f087fe7af5bdbefc0be4b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.0 MB (342043540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0d3e3727b9a403bd75ef408afeb955b6e6d14979c17222c4d2e9ccd5fe9e49`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 28 Apr 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2a14f59a002f5ef50911a0687d30beadf65bbe35bde8bd3823c3496cbd465`  
		Last Modified: Tue, 29 Apr 2025 18:37:11 GMT  
		Size: 64.4 MB (64355683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919170863bb5513bdfe1ce20b4f372538ef99b950b570408aa6aec57bfd91916`  
		Last Modified: Wed, 30 Apr 2025 02:34:40 GMT  
		Size: 86.4 MB (86415404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280b2cbe9b185a145cd427125ccd35e0250a80679d21036014ab14fdf1e6e707`  
		Last Modified: Mon, 28 Apr 2025 18:48:43 GMT  
		Size: 119.4 MB (119400389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b402c159bc8b0784200393b29ed0e0e3d646533dac339bf212acfc429c73b2f`  
		Last Modified: Wed, 30 Apr 2025 06:50:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:2a7ff694621d2333b673779faab65364f1fb2c124f68ce646989e488fe6bfb98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10327538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a65b8c07c913d34a96f807c4281d695e7a45bee62c89c75ca378e44465ff0b`

```dockerfile
```

-	Layers:
	-	`sha256:be532a671e25680f23ee107c223f1684d5674987804e3ed82a2c0319043b46f7`  
		Last Modified: Wed, 30 Apr 2025 06:50:22 GMT  
		Size: 10.3 MB (10299715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:146fe7db6ff253e150b87ac6e0de362d53857048df4795c6c7c9f998f6ecbf37`  
		Last Modified: Wed, 30 Apr 2025 06:50:21 GMT  
		Size: 27.8 KB (27823 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:dabeffde6604a3893d39570bffc5b56c8d795d0d4db030218a60cb42c2b3fdf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.4 MB (355374660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8278eb50a9c3014f7a24723795e287f740b16022ab81096f0f9d95956bd0d98`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 28 Apr 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Mon, 28 Apr 2025 21:08:03 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8121c387e441201e2e932ee9747762becb1f76490293a373bd9505310d1fe4e`  
		Last Modified: Mon, 28 Apr 2025 21:53:42 GMT  
		Size: 24.8 MB (24847147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce8929d56fab56325a8eea211cb4cd1021bc6ffc1e7a794d505ddbe638b23cd`  
		Last Modified: Mon, 28 Apr 2025 22:15:00 GMT  
		Size: 66.2 MB (66228922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5dce2d30d426acf5ebe0638cf433b6f53f6b91bf2e8fb1b96dc40e51050ea2`  
		Last Modified: Tue, 29 Apr 2025 00:14:51 GMT  
		Size: 89.8 MB (89777176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42eb229ffaec8bb2d4ae5f6af15344b1b77eb404d2dcc67eaa5dd80ff2f2957`  
		Last Modified: Mon, 28 Apr 2025 18:23:36 GMT  
		Size: 125.0 MB (125042685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23be7dd3f57f46264f2b9ded799d7c75d29a6f0a648dda6a27b66d6b2a37218f`  
		Last Modified: Tue, 29 Apr 2025 00:14:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:4bff4fc40049be8493c95dfc4c8a0c262ee9fa24819bd6c1ccb665a50d456abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10279562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f607cb372b517ac6ac098976286d6c4864fc1080599ee77bccecab2b1031c290`

```dockerfile
```

-	Layers:
	-	`sha256:8fa4d34c1a40b45722e0f35af7986108e348465a9e9a3430e4b15f4e43601ef2`  
		Last Modified: Tue, 29 Apr 2025 00:14:50 GMT  
		Size: 10.3 MB (10251942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2426535ebde8c3d1939a88f5e2bd1c155cd7160353e10d99a3c84866e13b8ce1`  
		Last Modified: Tue, 29 Apr 2025 00:14:48 GMT  
		Size: 27.6 KB (27620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; mips64le

```console
$ docker pull golang@sha256:cfbfd9d326b44f65c92d593138097059884f452c9ac160aac3c277e3b35652ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322012665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef5f2bdb4f9e2c61a34fc2d84e5d92c67457935cc9e420a90786eccf0263fc3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f5e7682657f9515783d77fb7efbdd12ea81bbe4c750080727193e5396dfa344f`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 48.8 MB (48774861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca83e3505dc809d18860248927308a5c27c298583b9da5817d702111bdd65622`  
		Last Modified: Tue, 08 Apr 2025 16:31:05 GMT  
		Size: 23.6 MB (23595612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89ecdcc124054ab515f88e8a0bc5260e578fb23450a3ca215363db6cf689231`  
		Last Modified: Wed, 09 Apr 2025 00:38:14 GMT  
		Size: 63.3 MB (63308311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67fb97ca2e19f9a62b9988d33fd9b65b01ccb5cc564c412de1d8c73ed7b28fc`  
		Last Modified: Wed, 09 Apr 2025 08:20:47 GMT  
		Size: 69.9 MB (69916439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c2812d70b5e59d5754f1df87fc74a0a34ccc712a63b78eefe2f011c6124a92`  
		Last Modified: Mon, 14 Apr 2025 23:38:14 GMT  
		Size: 116.4 MB (116417283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bdd0da5b4ee14fc37887e4cd57f7a66444abbfbced1bcfc65943dc6f1965b60`  
		Last Modified: Mon, 14 Apr 2025 23:38:03 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:4d636fb357318064dc08b53039cfd956dc7a1d5e9ea411b91b0bd4a32acc2ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef268210359f1fa797bc31c676dd1bea974acd38258d26aecfa7baa2d31ed07`

```dockerfile
```

-	Layers:
	-	`sha256:cf7139c6c7828d162ca45a756fa275fa592453607ddb683a901d92d0bb2ef624`  
		Last Modified: Mon, 14 Apr 2025 23:38:03 GMT  
		Size: 27.5 KB (27534 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:877176eeffe74ec5c7e27411cb33620d5370196cbef697e9efd103d55b8a8fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.7 MB (359732951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7203b9bf86e460a659733152d457a1f7532b8585eafb33002155c5c3f73dd043`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 28 Apr 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4617415431bf61f96c81d815cfb6cf010eef7bd0d8a8de24b02c1a7fe8407026`  
		Last Modified: Tue, 29 Apr 2025 07:46:58 GMT  
		Size: 25.7 MB (25650113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae70f40efc6df1466aa415707fbf58268a1633e6ab2dde78f23ec024d7c1e42`  
		Last Modified: Tue, 29 Apr 2025 08:29:00 GMT  
		Size: 69.8 MB (69840424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f4ea6f35d734e3ff8a820a7991e5169d5d24e7cc87410ff1b6ff4af4451028`  
		Last Modified: Tue, 29 Apr 2025 09:16:22 GMT  
		Size: 90.4 MB (90350689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e2c76c2b3dfa96df067175069013952b6bbd2cd22cc810dd73e4d9fc005619`  
		Last Modified: Mon, 28 Apr 2025 19:13:46 GMT  
		Size: 121.6 MB (121559438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a6d4f80e42672611c272baf4263451725001a6b57b5cba17b294d3ad5ab87b`  
		Last Modified: Tue, 29 Apr 2025 13:06:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:2e16244383d49414708bfc56c2b7e353cba0c310c3f68246024813323d494aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10272280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca97f96a07f5cfb21a763194cf2bc58e1b185f3aa4052b3aaabe644d2dc5470`

```dockerfile
```

-	Layers:
	-	`sha256:c270d084712f387ef5271c7084dbcf72952eff0744a1619399d321593c385adb`  
		Last Modified: Tue, 29 Apr 2025 13:06:58 GMT  
		Size: 10.2 MB (10244561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d30218b8265c41b21573c0021027edb0eeaf4ff6ea3d7b50395d75513d2ce2d1`  
		Last Modified: Tue, 29 Apr 2025 13:06:58 GMT  
		Size: 27.7 KB (27719 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:c4500e9d993c14067990c701a2f9dc2d2b02ea7da9412324b2fe9fcb27556344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.7 MB (327665435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9412e3d08ed5adb541444bb63e20064b3dc065fee8740fe85b0fb28ad4f9470`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 28 Apr 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c607354a47eba0ce7493f4dc26e0f40aaeea360944111a83eeeeb61083045`  
		Last Modified: Tue, 29 Apr 2025 00:01:21 GMT  
		Size: 24.0 MB (24008311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15250b46b7f7ffe8ad5ce0f3a2d64d0437e4fdf3d36b87579551846c0b2dd2bc`  
		Last Modified: Tue, 29 Apr 2025 02:58:48 GMT  
		Size: 63.5 MB (63496877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21538ac18bce01dcbc388d1060d1f4c02072e1607d7a15b2413b5a33918fc4c5`  
		Last Modified: Tue, 29 Apr 2025 05:38:51 GMT  
		Size: 68.9 MB (68938513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad2d83862091acf5554bf81b44e1663cf8d039b94a8cf88149d288c587c3ad0`  
		Last Modified: Mon, 28 Apr 2025 18:30:52 GMT  
		Size: 124.1 MB (124070245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8bc729bf830a11748ee45710d1c7878a1bee8721a23a600a512e143683b9a7`  
		Last Modified: Tue, 29 Apr 2025 09:29:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:6c90bad3e4b4c5e59375776837affc6e46d0a7ec9c6db4a8fe69622dcd854d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10135511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80654f07f3e0e15bbf68949885f820c30d3cff096b45cf65bc1f14ade9fd3955`

```dockerfile
```

-	Layers:
	-	`sha256:fb911c8c0dc139dcff5ca3c7975afcd09ff385ffd0213d2d43365c92c787f62f`  
		Last Modified: Tue, 29 Apr 2025 09:29:45 GMT  
		Size: 10.1 MB (10107848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:663bc7f6d6e85cc256a9d18be985f89b49c79b046eed116dbc5819b277c43f54`  
		Last Modified: Tue, 29 Apr 2025 09:29:45 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json
