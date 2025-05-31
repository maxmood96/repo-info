## `golang:tip-20250524-alpine`

```console
$ docker pull golang@sha256:1cb3371d2034a8c8defd23cdeefa2c3bfe158da961bb4b566dd2ee449fef9a80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20250524-alpine` - linux; amd64

```console
$ docker pull golang@sha256:b3315b942d803814ea4dda543a57236572562ac08ee8da25e9450859c4e8baf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130332833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d1b049d6fd3b438d24cf667539ee8dd84c6cb6a0c82632c8fbe7f835fa4561`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:49:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 30 May 2025 20:49:27 GMT
ENV GOTOOLCHAIN=local
# Fri, 30 May 2025 20:49:27 GMT
ENV GOPATH=/go
# Fri, 30 May 2025 20:49:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:49:27 GMT
COPY /target/ / # buildkit
# Fri, 30 May 2025 20:49:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 30 May 2025 20:49:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Fri, 30 May 2025 18:04:24 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbaabb46005d1e53df800f7fd9845b4a509e29973e2e56abf81a261126321d3`  
		Last Modified: Sat, 31 May 2025 00:10:57 GMT  
		Size: 294.9 KB (294912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37739a11166de3eef493c06e2f945d1e527fcbc7b45049a9bf54b5049c44176`  
		Last Modified: Tue, 27 May 2025 19:04:56 GMT  
		Size: 126.2 MB (126240918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a311201e70388492edc9c9be4d112ef8c8f7024a119164177fadb02347d45eda`  
		Last Modified: Sat, 31 May 2025 00:10:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250524-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f7319748a00e71cc2a6f2fef6d6538e058c1342b43e3a1ed8e6e491287c2e161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.3 KB (239343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788bd4f51b637a96bd6c518ff33d21c197195ca2475781d86a5874c16c35d1af`

```dockerfile
```

-	Layers:
	-	`sha256:86ac8c0dd40068863720083e24e44d6c44e0fbe225dbc4ef235d8325aa3099a5`  
		Last Modified: Sat, 31 May 2025 00:10:57 GMT  
		Size: 214.2 KB (214201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b94632353d1d148cb560c1270e8da215c56f1fb9ed9fcc0f3da290b01b915b0e`  
		Last Modified: Sat, 31 May 2025 00:10:57 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250524-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:b72b0dd1aa2328de752c7d30c6c7604cf20a59755ec4a9e89f76d0e130034b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125245849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4314538ad4072bfcc7a1e17c3ec10efd5d773c03bf81ae266b8fd67df957684`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:49:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 30 May 2025 20:49:27 GMT
ENV GOTOOLCHAIN=local
# Fri, 30 May 2025 20:49:27 GMT
ENV GOPATH=/go
# Fri, 30 May 2025 20:49:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:49:27 GMT
COPY /target/ / # buildkit
# Fri, 30 May 2025 20:49:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 30 May 2025 20:49:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Fri, 30 May 2025 18:04:31 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade1a66512d0d840a56a8c3fcd61678c4f71bc9949c18f7ee679feb7494b20e0`  
		Last Modified: Sat, 31 May 2025 00:11:16 GMT  
		Size: 296.3 KB (296292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd0559c7de6f506244fa457bd5bb8e69593e5e2f5b69b52b74b698afed88582`  
		Last Modified: Tue, 27 May 2025 19:05:14 GMT  
		Size: 121.4 MB (121448470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3937f9b932a3f81d165cc64a093b0f3fe4f1f4c070930d03fd83d2625f2f49ea`  
		Last Modified: Sat, 31 May 2025 05:04:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250524-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:fc00c01073a5546c3545e13e3c73df36e8e2a685694b838c66c12f401e7df4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fcfd58582ffb45c2f598bf3b35c184f52d862f8eac030b13758938e8d6c7392`

```dockerfile
```

-	Layers:
	-	`sha256:736de009333231d9e7bf6b2e66fa73a54f15db1f28b13bccf12e633c745ce0a1`  
		Last Modified: Sat, 31 May 2025 05:04:09 GMT  
		Size: 25.1 KB (25050 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250524-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:404b2e107652d03ad6aec199f9effefb4b2b0152a0d44e227344f8f7e38ce27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124623488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f069a581a519ca13aacd9fd1216d20faed94d79b559c09e647f353ad97a1bad3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:49:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 30 May 2025 20:49:27 GMT
ENV GOTOOLCHAIN=local
# Fri, 30 May 2025 20:49:27 GMT
ENV GOPATH=/go
# Fri, 30 May 2025 20:49:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:49:27 GMT
COPY /target/ / # buildkit
# Fri, 30 May 2025 20:49:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 30 May 2025 20:49:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Fri, 30 May 2025 18:14:23 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6c9cae412d8d42471b3ec2789f87569712940a14bb5b06595436c95f2904f8`  
		Last Modified: Sat, 31 May 2025 04:58:03 GMT  
		Size: 295.2 KB (295232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d0fe5e7d3d09e12944b416a2054aa6712ade9bdcb8b3878cad2dddeefd549a`  
		Last Modified: Tue, 27 May 2025 19:07:16 GMT  
		Size: 121.1 MB (121108917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173dfb6844fcbe1643fcc08507339bf43b7aea1476440d0ca2436c6498df6dcf`  
		Last Modified: Sat, 31 May 2025 05:09:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250524-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:9e4129d4726a5b9ba0d123a2fd2e192cd89d98506e13d740dbec6a501db20a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 KB (239463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d100a4934dd8fe570453faab23a265c5a5b1bf69c6485a45acdbe6e60c46368`

```dockerfile
```

-	Layers:
	-	`sha256:91819424adf842e7934b5b4a114c89b43111851347cd45f3ab590810dfbf6c6b`  
		Last Modified: Sat, 31 May 2025 05:09:56 GMT  
		Size: 214.2 KB (214197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a8497f4122ba85bc07bcfbac92578f2bbf6979d470d6e843542c542615e8413`  
		Last Modified: Sat, 31 May 2025 05:09:55 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250524-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5e9d20b9f0f9a3143388d3a31ab61d4fba6236c41a04575edc77f9e429d75408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123488258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f522ea8ce4327ac99af771783cdff883e3283d7d6a2412f9507819057a570b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:49:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 30 May 2025 20:49:27 GMT
ENV GOTOOLCHAIN=local
# Fri, 30 May 2025 20:49:27 GMT
ENV GOPATH=/go
# Fri, 30 May 2025 20:49:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:49:27 GMT
COPY /target/ / # buildkit
# Fri, 30 May 2025 20:49:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 30 May 2025 20:49:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Fri, 30 May 2025 18:15:21 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373964117ef6ddcc9d2295f836a878c54d49d139d1981ffedc92cef7282b2a9c`  
		Last Modified: Sat, 31 May 2025 03:56:24 GMT  
		Size: 297.9 KB (297885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea33ecb4b895f73f5e4d5736d5a0a4109e5ac27823a9c5ca57f0642e5a3d9a8b`  
		Last Modified: Tue, 27 May 2025 19:23:28 GMT  
		Size: 119.1 MB (119054274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df770bfa3d437e99e7f9db463a69954517043cf561294d4f044e50ea133cc9c6`  
		Last Modified: Sat, 31 May 2025 04:09:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250524-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:4f7378d5287a7f7c7e3e3fa4b96f610152f104077b77809ff8269542832d0249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.6 KB (239559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca7a987f9a755993285acaad9b648a207bf200421756fff6a4a4bae46d7833c`

```dockerfile
```

-	Layers:
	-	`sha256:09cc3491744e39a6888f8b38b79d5dafb8ab361818c3551d44bad83f25eed1ba`  
		Last Modified: Sat, 31 May 2025 04:09:05 GMT  
		Size: 214.3 KB (214257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:686b4395038319e2570978ec8cef5115c37b493ac914a4902339a478e2f8a892`  
		Last Modified: Sat, 31 May 2025 04:09:05 GMT  
		Size: 25.3 KB (25302 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250524-alpine` - linux; 386

```console
$ docker pull golang@sha256:414def27bf9d66d032e2dd20dea4e9b7a57a2bbc41f06e0487f7d874b17beeb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128118975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4e4aafe02cc85ad26a3b033313e181949580805281dde46f94474ce9f85073`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:49:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 30 May 2025 20:49:27 GMT
ENV GOTOOLCHAIN=local
# Fri, 30 May 2025 20:49:27 GMT
ENV GOPATH=/go
# Fri, 30 May 2025 20:49:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:49:27 GMT
COPY /target/ / # buildkit
# Fri, 30 May 2025 20:49:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 30 May 2025 20:49:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Fri, 30 May 2025 18:04:26 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5066e61a61ee71172507385d91129514820687af1e081f651b09749694e3b87`  
		Last Modified: Sat, 31 May 2025 00:11:34 GMT  
		Size: 295.6 KB (295611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb63d3af1099d61647a313155e9eaa0aeecda078cbf5fcab7fb7996b234e196d`  
		Last Modified: Tue, 27 May 2025 19:05:30 GMT  
		Size: 124.2 MB (124207178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965ddcd44bfbc81eef6786b5537fc742e3ab87d77fcca18083be4bdf55be540d`  
		Last Modified: Sat, 31 May 2025 00:11:34 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250524-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:9e0b1605a22689727ff658baf16c93e242060a2e7927be42297d8cfb5e51ee14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 KB (239235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3676c633f537a3d2b8c43cb0a29144b71818db62e7b4052e588f8feabd6495f9`

```dockerfile
```

-	Layers:
	-	`sha256:990000b80e3701dcd6e4c26fb4e3002318cefeaeac154c33de6926637c4823f9`  
		Last Modified: Sat, 31 May 2025 00:11:34 GMT  
		Size: 214.1 KB (214136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3706f75c3fe954b3161c61cb45d3d89c5ee1717cce3fc2afacf79b63b9ceffdd`  
		Last Modified: Sat, 31 May 2025 00:11:34 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250524-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:18db8fdfca22961a29321119148d51e447acf031683257e0525dec8a952c3756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125194084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426817440316fe041f6b86abc4aa7d35039175499f72d5a9978fe836f6ac5e4e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:49:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 30 May 2025 20:49:27 GMT
ENV GOTOOLCHAIN=local
# Fri, 30 May 2025 20:49:27 GMT
ENV GOPATH=/go
# Fri, 30 May 2025 20:49:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:49:27 GMT
COPY /target/ / # buildkit
# Fri, 30 May 2025 20:49:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 30 May 2025 20:49:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Fri, 30 May 2025 18:14:22 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a187c79905be9977c8b81d03082bbff0333d20fe9ac9a7740864c66f7e0e5c7a`  
		Last Modified: Sat, 31 May 2025 00:09:46 GMT  
		Size: 298.3 KB (298320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4275b8143ff44473029dc987922dbd1dd91e814dab86dd3c175ed73d2ef81d1c`  
		Last Modified: Tue, 27 May 2025 19:06:55 GMT  
		Size: 121.2 MB (121165419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c94da76c1832c69de9c52bde28e8940fab6ad3399a3ab7c64bc96690d07497`  
		Last Modified: Sat, 31 May 2025 01:14:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250524-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:0d5007954367d53881cfbeda777b8d4fd6a1aa86119706261b76df9d9aa285ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 KB (237524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f66de3c6237e8c110fa9a4c4d775a17fa2e49d1373cf48275ad3c15acedb4b5`

```dockerfile
```

-	Layers:
	-	`sha256:2a812ea8fafb4606b4b1136184b9160a5c1169439a161b09c35855a0da0f4164`  
		Last Modified: Sat, 31 May 2025 01:14:36 GMT  
		Size: 212.3 KB (212324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37b08b0c3bd98cbf23b4698d2f56058786946841c98620b517084e38c874d1ff`  
		Last Modified: Sat, 31 May 2025 01:14:36 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250524-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:5b3e702fa335d596ea045f6e6c6fd780e04f9bd896a26bfe604ca6790325537a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125203140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9324e0f6c1fd87c2129a249e5eb4788853dac4b087a02d87e52efef0555c0178`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:49:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 30 May 2025 20:49:27 GMT
ENV GOTOOLCHAIN=local
# Fri, 30 May 2025 20:49:27 GMT
ENV GOPATH=/go
# Fri, 30 May 2025 20:49:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:49:27 GMT
COPY /target/ / # buildkit
# Fri, 30 May 2025 20:49:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 30 May 2025 20:49:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Fri, 30 May 2025 18:54:40 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850bf8006499bec04d28fe13dec3efd4cf9075748d5dcf5b6dc1415aa6aeb8f0`  
		Last Modified: Sat, 31 May 2025 03:27:47 GMT  
		Size: 295.4 KB (295390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf501e8ac8e034ccf3f3064d2d56237fc55dc6b377839b153c3f162a1fadf302`  
		Last Modified: Tue, 27 May 2025 20:07:53 GMT  
		Size: 121.4 MB (121393782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4ffe88e75a9bf6641394bd699c19a6852fd1260e8246048f9113a3f35391f2`  
		Last Modified: Sat, 31 May 2025 14:14:49 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250524-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:686ae9250b048277587c2ebd065aead2079e223dfb099877540bdb01d8bc13e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 KB (237520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4cee7c445a06f336c54f65de2c349d0826c30b18f9be4f5773c72b7879d334`

```dockerfile
```

-	Layers:
	-	`sha256:7cf3dd315217b44ff5a43d4196898495b675c7555d7e89920a8568379d312e52`  
		Last Modified: Sat, 31 May 2025 14:14:49 GMT  
		Size: 212.3 KB (212320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f482b53928edfe53dbd61faf4af28a1e91caa36635ab8e03f8e35469e0e03c1c`  
		Last Modified: Sat, 31 May 2025 14:14:49 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250524-alpine` - linux; s390x

```console
$ docker pull golang@sha256:3e9cbfc81426a42e11d98789b3b62271ffa5fc07245e4ca0f67083cd3cc7244d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127406444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff629f73fb920ad1660efd845dce554dc9e50232918b10eec38643dad9cc5b3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:49:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 30 May 2025 20:49:27 GMT
ENV GOTOOLCHAIN=local
# Fri, 30 May 2025 20:49:27 GMT
ENV GOPATH=/go
# Fri, 30 May 2025 20:49:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:49:27 GMT
COPY /target/ / # buildkit
# Fri, 30 May 2025 20:49:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 30 May 2025 20:49:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Fri, 30 May 2025 18:13:14 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02725f6addf0718099c43b5965203aa513fc71aa710978afc18cf384dfb4798`  
		Last Modified: Sat, 31 May 2025 00:11:27 GMT  
		Size: 296.2 KB (296215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a53d6c9d36291056f30ae15703f561e0a8333bad5f15ea579763f74d2b6616b`  
		Last Modified: Tue, 27 May 2025 19:05:45 GMT  
		Size: 123.5 MB (123462542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4d93ef3ab9e0e99d0ac3782fb5de2815fbf745a370c515e4cb5730434d15d9`  
		Last Modified: Sat, 31 May 2025 04:50:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250524-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:1507758b943faf11586e3089d219bbd6655e510c869ec660714f3bc285ae1268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 KB (237391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804d30b972930806e83ef0cd7f6421379b6d3e367b012cc06048da0da54c18b3`

```dockerfile
```

-	Layers:
	-	`sha256:06b23e6efc3a04817b2805561a1d05cb49b245056314a6c7c5c18ff74f608881`  
		Last Modified: Sat, 31 May 2025 04:50:54 GMT  
		Size: 212.2 KB (212250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec4cdef61ed39f4cbbadb34351de49ee716e99f60ffb2f2c3dc944d900f7eb1f`  
		Last Modified: Sat, 31 May 2025 04:50:54 GMT  
		Size: 25.1 KB (25141 bytes)  
		MIME: application/vnd.in-toto+json
