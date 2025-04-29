## `golang:tip-20250426-bookworm`

```console
$ docker pull golang@sha256:a784748a7384508d2aa51cf1bf88b21b6ebc9ca38f167c45f8c7401e1fc16a55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
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

### `golang:tip-20250426-bookworm` - linux; amd64

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

### `golang:tip-20250426-bookworm` - unknown; unknown

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

### `golang:tip-20250426-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:a8ecbe60636c5e4c5d8055b82036055199bc1034c46b10a875cf91b01e7933ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 MB (313626807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe0cefe3ea062b7a12af2423173c4cf4dc2e69c71037b59d87f22497130c0d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e40f48a2e6d38c2746e98a645887fe65e2b335f766dc7c61af172a1356726d5d`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 44.2 MB (44196771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d083faafd756a71980d33b1aeb908b0db85cdc7a159e3d49107170305f1bf41c`  
		Last Modified: Tue, 08 Apr 2025 07:37:54 GMT  
		Size: 21.9 MB (21918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5414268749270f000845caf5689fb7740534b9fe922712301ba571a6afca96`  
		Last Modified: Tue, 08 Apr 2025 17:29:39 GMT  
		Size: 59.6 MB (59639425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9a9e8df2c13231c1e0a205f7e3ac9fa85454d09e0c0e5c18afbd185b211ea`  
		Last Modified: Tue, 08 Apr 2025 20:42:26 GMT  
		Size: 66.2 MB (66197481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33618dace1ba528dcd7b40e80a4e895530a8d058bda71f5a87abf8312ed70c2`  
		Last Modified: Mon, 28 Apr 2025 18:46:15 GMT  
		Size: 121.7 MB (121674729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b8b647e08c98d52643dfd03d7e0037ee8d19bfe661857a0970dc0150b94ca7`  
		Last Modified: Mon, 28 Apr 2025 18:46:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250426-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:20d26d914467167819ddebb0acc5e7072dfbe4390995f9d477c9b421807df5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10107977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021de1d51662f90f2dc89603a91bb6c0f06d21faabc4484aa54cee89cfd02902`

```dockerfile
```

-	Layers:
	-	`sha256:bdd3a858d47bbfc6527d0d1520254d2e0b2e1b1ab231322fcbe26f182b02c9fc`  
		Last Modified: Mon, 28 Apr 2025 18:46:10 GMT  
		Size: 10.1 MB (10080190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eac80ae66bd2d1daf6d67d7d5bd6053184bf28b8d5e7dba618bccdf89410cd2`  
		Last Modified: Mon, 28 Apr 2025 18:46:09 GMT  
		Size: 27.8 KB (27787 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250426-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c1d4e06cc7898f8040c88fe112c405f48c5d187ff378f73b0c3c9386c318f8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.0 MB (342025258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ba2cbeb467db4037820c4258d6eb58285a42d35c54ef9b82c7d27b0ab7c7d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d81c64672754c46e5d99e385c8f3283bec2060a79ad7dacdb2f5ce904caa401`  
		Last Modified: Tue, 08 Apr 2025 06:03:14 GMT  
		Size: 23.5 MB (23544339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf144460616b42eb1462fd80a5e1909e578b1e1f7285b185e468ba2b01308b9`  
		Last Modified: Tue, 08 Apr 2025 12:18:06 GMT  
		Size: 64.4 MB (64355780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f72691c55039fb058e42d1e7433c859beeeeaa9e1b1856b791ba59bd1bc0586`  
		Last Modified: Mon, 14 Apr 2025 21:49:56 GMT  
		Size: 86.4 MB (86397123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280b2cbe9b185a145cd427125ccd35e0250a80679d21036014ab14fdf1e6e707`  
		Last Modified: Mon, 28 Apr 2025 18:48:43 GMT  
		Size: 119.4 MB (119400389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61890da2acea7a1af3ff7fcb8864fe6295d99fb5eb6499dc7a9c29e774df5153`  
		Last Modified: Mon, 28 Apr 2025 18:48:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250426-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:cb18a20ecf81dd5db5081c17e0826aa40de198b40aae1c2a3f42c20b86e53410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10327537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e5a8a3dfc8722949a14abd5ab72c65ce0aa638fcc11d88735a3b36352f2ec1`

```dockerfile
```

-	Layers:
	-	`sha256:895a5a82489741f968257bb9580f5b6d7455fd3e07242ea52e37967f8ffa7117`  
		Last Modified: Mon, 28 Apr 2025 18:48:39 GMT  
		Size: 10.3 MB (10299715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03e0f3c36e597797fa5b02efaaf5587478abb52c1912384eff405786bb3775e1`  
		Last Modified: Mon, 28 Apr 2025 18:48:39 GMT  
		Size: 27.8 KB (27822 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250426-bookworm` - linux; 386

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

### `golang:tip-20250426-bookworm` - unknown; unknown

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

### `golang:tip-20250426-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:206d51faafd8976ba755f1b2f8008c4a54f475d58bc02e360d2a0345d268e6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.7 MB (359735629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0cae848a451261c1f2e9e1bb0531e4bddc3137297fe42a8d1c8dc9e3d9fc30`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:96130533c16d0aeecdcc4c64baab4a3adfb31877715c21a61125a04fe062f893`  
		Last Modified: Tue, 08 Apr 2025 00:23:16 GMT  
		Size: 52.3 MB (52331646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54c9911bf701a3c84db58a7959c7ebb5f1e34a45bad705a2799f182bc4e0bf`  
		Last Modified: Tue, 08 Apr 2025 04:30:15 GMT  
		Size: 25.7 MB (25650176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02bafec621c70d63b6b8b80ca09a779f1c6500fb5feaa4c53d57a46c6a6ff7`  
		Last Modified: Tue, 08 Apr 2025 08:37:54 GMT  
		Size: 69.8 MB (69843923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ab73478cfc6c2c81f66fffabb6adb3536b4880f0b0cb959b34167c62eb4cc2`  
		Last Modified: Mon, 14 Apr 2025 21:52:04 GMT  
		Size: 90.4 MB (90350288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e2c76c2b3dfa96df067175069013952b6bbd2cd22cc810dd73e4d9fc005619`  
		Last Modified: Mon, 28 Apr 2025 19:13:46 GMT  
		Size: 121.6 MB (121559438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82dad12de472391dfc79a5abed8296380defc60817ea430d8401745d2f12b5f`  
		Last Modified: Mon, 28 Apr 2025 19:13:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250426-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:96d5a4884cf4d1f27d12810862c0f003015f961de590a20dcdd31a3397bb32bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10272282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868b203cb6803cd0a7db39ee250fc5419db7f78c0003ee9b8fcc62aa92f7925d`

```dockerfile
```

-	Layers:
	-	`sha256:8f026684fcb7039f366a19e41cea498d70e589826775e35e5fe907b34a4a8d2e`  
		Last Modified: Mon, 28 Apr 2025 19:13:40 GMT  
		Size: 10.2 MB (10244561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:527167ae84601cddf937d6ff3a519a44668627ba129eb62f8227c4f51b35a5fb`  
		Last Modified: Mon, 28 Apr 2025 19:13:39 GMT  
		Size: 27.7 KB (27721 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250426-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:d5b801e4f8116a9a537c219d508d485a67573c4c0cab1c54ace330161a35d044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.7 MB (327664954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4891b33cf27d65dc29c5ac9a74be5671e9935c53300c53d664b2a2e79b389ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:02fcba40f83e05adf85891b5c708b183d1028fd36fd80528f148e95bf593ab77`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 47.2 MB (47150996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a93e29489c173c9f7bae02e4e3f728f3e5b721748076de87502e6e9fd9108c`  
		Last Modified: Tue, 08 Apr 2025 03:44:19 GMT  
		Size: 24.0 MB (24008336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4fde99ce0eec506f038695c59ba0ff56bd0df358636c0b067f55c60d7d566c`  
		Last Modified: Tue, 08 Apr 2025 06:52:25 GMT  
		Size: 63.5 MB (63498375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbac9900eeeae74e6b991013801dd4b548da42e9a24a8a017f2f933bdd60bd62`  
		Last Modified: Mon, 14 Apr 2025 21:52:33 GMT  
		Size: 68.9 MB (68936844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad2d83862091acf5554bf81b44e1663cf8d039b94a8cf88149d288c587c3ad0`  
		Last Modified: Mon, 28 Apr 2025 18:30:52 GMT  
		Size: 124.1 MB (124070245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a995a09defb27b79980ad69f5777d427cc29603dd82b86ceb859e34faa4761b`  
		Last Modified: Mon, 28 Apr 2025 18:30:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250426-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:488ed180996864295cf6fb3900804b17b80929c518feed93f8cf192a03284603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10135511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb09d091b670d74fdfa768f89eb2c5e7afa028a34e0812bebaf116ec2c93793`

```dockerfile
```

-	Layers:
	-	`sha256:3c104d50ef2af0c18f2ed6dd28b354bd165507b8851af37e8af08b0a6d4a04fa`  
		Last Modified: Mon, 28 Apr 2025 18:30:49 GMT  
		Size: 10.1 MB (10107848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19b1f339dbdb30327f6420247a0f77e3465a8220d282a5a747e004fbe69e221e`  
		Last Modified: Mon, 28 Apr 2025 18:30:49 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json
