## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:818eb76f68a30f1fbd7d5a660bbbe8a6eeeed4cd37d0b9d7d78cdb9598112097
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

### `golang:tip-alpine3.22` - linux; amd64

```console
$ docker pull golang@sha256:610744a9e0ef6c3c213a4f4a0c6f8afadb74240a6c3f8a25ae773df2f247a8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106099957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68186e7332ca907e4727c3db55233392632369cde9ab52b9e6567ccd090d5bb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:41:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 16:40:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:40:54 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:40:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:40:54 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:43:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:43:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d89acf571ad584eadb72ef0de45cf58c8e49f18192230d03642d23851fed913`  
		Last Modified: Tue, 02 Jun 2026 16:43:31 GMT  
		Size: 289.4 KB (289448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23f29da6194068cf9bcb9d5261ce3db2ba9613e69bf068059cae42650df5c10`  
		Last Modified: Tue, 02 Jun 2026 16:41:24 GMT  
		Size: 102.0 MB (102002162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9963e838d66d77e6a17968a457e3e6fc4d1a2d148442a3cb40e6f78051d332d9`  
		Last Modified: Tue, 02 Jun 2026 16:43:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:117ed8378d67b5d68940a46a297e02ea5cdda412b20c255e79d3ddd4a2d7bff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27857c6321e6cce1517d853dd1a137c9d82bf7f34926c60c9466c632cd24a68b`

```dockerfile
```

-	Layers:
	-	`sha256:281707aa31c572f19c6e3703cff8e403b5da8fe96a3dba312e840387fe008e8a`  
		Last Modified: Tue, 02 Jun 2026 16:43:31 GMT  
		Size: 194.3 KB (194297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca00e01e89a78d94a53c40d25ab8f4c752a6935d69d23e22f1dce4f6f34d381b`  
		Last Modified: Tue, 02 Jun 2026 16:43:31 GMT  
		Size: 24.5 KB (24469 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:cbfcd6d03ee2038b9e4cc9399beba4fc5d4e7cabba68d55e4d6ac8f0e464148e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101815756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f6a9b17e6c6b9eb9b9c0b45975c0db94c934a8fee8312e0f37cd752b6a99cc7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:39:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 16:42:53 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:42:53 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:42:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:42:53 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:42:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:42:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0af90783d3605f7526b384294e637f40a4117c53fad656f82aeeda9704afa62`  
		Last Modified: Tue, 02 Jun 2026 16:43:08 GMT  
		Size: 290.3 KB (290336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e28476efd8da64969ee963c59bc7bbb65ceb1b7045e417b1e645826aca392a`  
		Last Modified: Tue, 02 Jun 2026 16:42:09 GMT  
		Size: 98.0 MB (98017879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dde158146936076044ed3207d4f16e1c01bbffbc8181b01a1df41513acd458`  
		Last Modified: Tue, 02 Jun 2026 16:43:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:e1f34739393538172c10ef378f98058ad7877d72d5ec47e2bb01f318cd467620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:564491917ddb90ccc8a4d9335877cde770c383fdd395615905f06f671ef5cceb`

```dockerfile
```

-	Layers:
	-	`sha256:657ce8e4ce11549a68ac180fc3d9dfb7b8effb90dfec4111f88e1f1609f521bc`  
		Last Modified: Tue, 02 Jun 2026 16:43:08 GMT  
		Size: 24.4 KB (24361 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:e511f9a456d782c4b2b3a60cf8287723b2d63650325e25ea0acd339bb6e305e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101230563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0dd32993a560c49e9b518af5027ea71d4c2ea4e30c851040dd96665c892bf17`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:41:22 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 16:44:24 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:44:24 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:44:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:44:24 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:44:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:44:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1077695f5c2d7bcf2df05250252a087ac766914b15ba4bf312667ccb472a3fad`  
		Last Modified: Tue, 02 Jun 2026 16:44:43 GMT  
		Size: 289.5 KB (289519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c820ebe5b5536b95e87912c5dc1f2663a3e9f184b88c7a174fffa610cef8238c`  
		Last Modified: Tue, 02 Jun 2026 16:42:07 GMT  
		Size: 97.7 MB (97715056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8710662ffb6ca68e98ef5b0fa49b6bdd0bc29ee1d874c59f3a20ee35dfd8bcea`  
		Last Modified: Tue, 02 Jun 2026 16:44:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:45682158bfc8b6efcc25389bf2e0ce9071a145c842b66b6c57413cfcc6b1b258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6c951537123ec539bf495a5279ab3654551d3026b348eb15d5fa49a3825a99`

```dockerfile
```

-	Layers:
	-	`sha256:7bde7e98cabb5022f8667ec99a925d08fbffebe1e91d398695c6daea6214235a`  
		Last Modified: Tue, 02 Jun 2026 16:44:43 GMT  
		Size: 194.3 KB (194301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91fb1c2e6cedddbde529a7fcdd1aeb6a6c4e739eef1de05a349978d58b0900c7`  
		Last Modified: Tue, 02 Jun 2026 16:44:43 GMT  
		Size: 24.6 KB (24576 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c7e69645e128fd16d5ab85ed325ac2f3f23851e7fa9e5e371d8735adf43700c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100868533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fab282158261fff5b58d03de7d46cf283a078ae980f075bff9fca719775400`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:41:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 16:40:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:40:58 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:40:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:40:58 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:43:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:43:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7666b90847d1454372db440e5fd1f74c2143f86acc108b4c3fd901d2818c94`  
		Last Modified: Tue, 02 Jun 2026 16:43:45 GMT  
		Size: 291.9 KB (291900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ffb09d61853e3fb3628a4cb3b2d395b59e27aec015f8f1626a8b2ce9bb2f2`  
		Last Modified: Tue, 02 Jun 2026 16:41:30 GMT  
		Size: 96.4 MB (96434582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5711afbb6dfe0093c9ee0b830b81fe6b6ac3bf83316d2e7d39d5d0ed1cc8c536`  
		Last Modified: Tue, 02 Jun 2026 16:43:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:6b0b1d847cf7e2eeee7b199505d24d70ef82bf960f6ab3a5722286b7c3aa6a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54de292178a578bdab2f11808968a7891d3bab2fd39bea4d175b468959ac94b3`

```dockerfile
```

-	Layers:
	-	`sha256:a1460c336df6cfc9c1f4f6a5c5e0d649fe8c13f4faf26a78f32f0874610f2e78`  
		Last Modified: Tue, 02 Jun 2026 16:43:45 GMT  
		Size: 194.3 KB (194329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb9677ddd8b2b0357317c3d2b9a82c0d02fa35647eb4ceec05f0813a9fc03a39`  
		Last Modified: Tue, 02 Jun 2026 16:43:45 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:c52455806362bf8278fe62a82fcb99069e8193e958f847f2d368008d894b2c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103684346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64eef279bbce2b0c9fc6a32c82c9123699e1fb00001f9b92c2e843f52371e6c2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:40:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 16:43:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:43:32 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:43:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:43:32 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:43:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:43:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8763d3b4e43839d8d2d052e2899bb9a6983ced8612468f99fd1eaee73e2a015c`  
		Last Modified: Tue, 02 Jun 2026 16:43:50 GMT  
		Size: 289.9 KB (289937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f630b89f59dc6a4b85d53c6ab2696f0b52ea5d937a0bd9344e6c06fc5883a6`  
		Last Modified: Tue, 02 Jun 2026 16:42:33 GMT  
		Size: 99.8 MB (99769529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0023d8f0197f4fc0a75947bf216d172c02d7a6f717e339c0a22ace33439e4a2c`  
		Last Modified: Tue, 02 Jun 2026 16:43:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:e7747b968cfdd4e86c1c904946b147075ee43502fb8b70d1e978e9f6996e9b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34a2fe308fa70841cd7c797686d9263db163ec81309a7dd07336373b5567272`

```dockerfile
```

-	Layers:
	-	`sha256:83e9d8294747e7d1bec51bfff7f8dfe2e6bf6373ffc21f25fe91db673f652a62`  
		Last Modified: Tue, 02 Jun 2026 16:43:50 GMT  
		Size: 194.3 KB (194266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed521f90db353a277b8dba8926a0c9eec8b3bac7a52291be471a72aeb74cdb95`  
		Last Modified: Tue, 02 Jun 2026 16:43:50 GMT  
		Size: 24.4 KB (24431 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:127d0a1ca041e4f562504df6bf8294412676f87d2f2d417927112626d8702cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102416343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f0eb51c55bb4c00abcbbfb046dcac51f98eb23e0e75928921f31a6cb073ba9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:47:38 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 16:41:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:41:50 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:41:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:41:50 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:47:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:47:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc19e70a619da2cc79678570dca39a29588122c6fe070ad72dcbd9b097fe32a5`  
		Last Modified: Tue, 02 Jun 2026 16:47:54 GMT  
		Size: 292.4 KB (292437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a76d2265265ac98a5752cfbf5ed880207c013050351547f0c225cf8c995ca0`  
		Last Modified: Tue, 02 Jun 2026 16:43:17 GMT  
		Size: 98.4 MB (98387092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f485423abbc19164208b67f0dc6250779ff7d97a652ca17a5c1b252ce75eca07`  
		Last Modified: Tue, 02 Jun 2026 16:47:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:17a475e1ac7627aaf88c88b13514f5c1ac1de02b7b8d3680fdcebab56b3ce009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 KB (216894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349ac85db072c3244a63bb411459ddebeedc96efa6e8f129009f09e908d0c055`

```dockerfile
```

-	Layers:
	-	`sha256:84259cc3fe660b5f1acd96277d55775f2d8d98445df5503e7d2de0b4268cf858`  
		Last Modified: Tue, 02 Jun 2026 16:47:54 GMT  
		Size: 192.4 KB (192384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b3f449b1f1b26287bcb50464b86ee69371176307cd1fb880cda1c25a1f00aa4`  
		Last Modified: Tue, 02 Jun 2026 16:47:54 GMT  
		Size: 24.5 KB (24510 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:054ccdac2ddee9a8c07955ac47d1cd87e8a5060fd2320706aefd591ae2384005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102973269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3118c7e8ba3950e4049f63397ebfcc68f040a7afc4a335b922cdacb3d67756`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 01:45:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 28 May 2026 11:35:46 GMT
ENV GOTOOLCHAIN=local
# Thu, 28 May 2026 11:35:46 GMT
ENV GOPATH=/go
# Thu, 28 May 2026 11:35:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 11:35:46 GMT
COPY /target/ / # buildkit
# Thu, 28 May 2026 11:36:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 28 May 2026 11:36:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e48325e06ab8f03302d19014bd8681498f11993eba6b2fa96b633d7c283c8e`  
		Last Modified: Tue, 28 Apr 2026 02:26:34 GMT  
		Size: 289.8 KB (289807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ba57acf5ba3d18b7eb9e4286139141d4a6480c2e9b8f4fd881334e86e5e1a9`  
		Last Modified: Thu, 28 May 2026 11:39:26 GMT  
		Size: 99.2 MB (99162424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795892d6f12a429d3b0e36731748a7b9154d470881b4072746a1e0e22e70609f`  
		Last Modified: Thu, 28 May 2026 11:39:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:57e8f5d08ecb8e1c745325027457a2d2b68e48d9217631f6c0b323518a487917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 KB (216891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a75cae907bdc842cb9ed613cc9f1c3c573ddd90a6a0e934ffc33e05d132dba`

```dockerfile
```

-	Layers:
	-	`sha256:3f384adbfcaf495b09ebf99a354d833dc74820ede5be05b08115c6370367eacd`  
		Last Modified: Thu, 28 May 2026 11:39:11 GMT  
		Size: 192.4 KB (192380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05f83fdb52e76bc370fac045ed71dc939532bac1b737a5a0242ce0672effc851`  
		Last Modified: Thu, 28 May 2026 11:39:11 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:71dc360321973241163ad5b927afe21eb8661de6f2070776e540ce5b5370172c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104398154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44af92c1c3e47c47767bf5d90561337404ca483cd4bde2509b05fff34bbdd804`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:42:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 16:42:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:42:00 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:42:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:42:00 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:42:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:42:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825e7a7c51c19d9988c7f5f1d66c52125dd9844775837a1e0b2a0c0ddcf7da3c`  
		Last Modified: Tue, 02 Jun 2026 16:42:26 GMT  
		Size: 290.5 KB (290472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca767cc33ca0e2036ed1bd1b9a5ecdd963a3598306969640db0e92025a10887`  
		Last Modified: Tue, 02 Jun 2026 16:42:28 GMT  
		Size: 100.5 MB (100453651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9996a94274c781c9e75ca2d7270662316e2e1c26ee0a2fe9f209e6ba6255d217`  
		Last Modified: Tue, 02 Jun 2026 16:42:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:ea2c4b5b74d4dd72483414ad7fe2cfe280598fa84e5addf62c21359901dcec13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e65958f91a914307da364d7918b82b65b583b6bd8e6063615e938c95af8cc85e`

```dockerfile
```

-	Layers:
	-	`sha256:cb79cd014b7814aef5c5ab466252685ed424a208cee4d3c6dcd7844746fc9ea0`  
		Last Modified: Tue, 02 Jun 2026 16:42:26 GMT  
		Size: 193.1 KB (193094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a2a37a67bbb782bd3e54e72fc412cc2fe4c81d54f9bb9168f2e271cf5b0baaf`  
		Last Modified: Tue, 02 Jun 2026 16:42:26 GMT  
		Size: 24.5 KB (24469 bytes)  
		MIME: application/vnd.in-toto+json
