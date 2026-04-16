## `golang:tip-alpine`

```console
$ docker pull golang@sha256:f3e5f209dabbe26dc4ecbb0277a8e6de2ff80888d84c14ac990291bf35cf69fd
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

### `golang:tip-alpine` - linux; amd64

```console
$ docker pull golang@sha256:c38af0add8828cd12410848ec6d56ca094ba0580971cc2a5cc8653175507bc35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.7 MB (98736535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d80668a7f5c30361dd3ac91640edc66d5acb518aa4960cc9ccff1f153aa6aa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:21:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 21:31:11 GMT
ENV GOTOOLCHAIN=local
# Wed, 15 Apr 2026 21:31:11 GMT
ENV GOPATH=/go
# Wed, 15 Apr 2026 21:31:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:31:11 GMT
COPY /target/ / # buildkit
# Wed, 15 Apr 2026 21:31:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 15 Apr 2026 21:31:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb496381bf96a08576a8320f7ff7202e580d0da89ae78f7abc411f7c21974eb`  
		Last Modified: Wed, 15 Apr 2026 20:22:06 GMT  
		Size: 290.2 KB (290244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab04cb4a8e454fc7559b5ebb652cf17e60070b889bacf79f9339f14ac23b48e`  
		Last Modified: Tue, 14 Apr 2026 00:01:54 GMT  
		Size: 94.6 MB (94581946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0147c304824bb4f87a0dbbe8f6f3286a9dfc9e0d5693c47e0318ab0644dcd0bb`  
		Last Modified: Wed, 15 Apr 2026 21:31:29 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:44b3cadea2615d8efab08f02b8e8cffef7213cbcbb2836185cb92347d14383aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54c0c15bd0fbeb34485a2eae8f6d55d4c2962dfc801eed7ad61de60cd947289`

```dockerfile
```

-	Layers:
	-	`sha256:0c087269e8063ca7f6d91f39f382da71091900af3e2cd47e680e765a4dc26a20`  
		Last Modified: Wed, 15 Apr 2026 21:31:29 GMT  
		Size: 193.6 KB (193648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2116804d07f052b47cae556e9683dc6a5388b0502d898431214c4800dd0b80a8`  
		Last Modified: Wed, 15 Apr 2026 21:31:29 GMT  
		Size: 25.1 KB (25093 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:fc3cbeeb16e893dd1ec2f2845aa83fa0638624be03986a23a0ffadac9838feee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95049895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c34346c3bf36d1e64d4cb0bef2f33f5fb3ff245d07f115fc6d5fada7fc1b9f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:22:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 21:25:20 GMT
ENV GOTOOLCHAIN=local
# Wed, 15 Apr 2026 21:25:20 GMT
ENV GOPATH=/go
# Wed, 15 Apr 2026 21:25:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:25:20 GMT
COPY /target/ / # buildkit
# Wed, 15 Apr 2026 21:25:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 15 Apr 2026 21:25:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e242a58dfe3d5201571258c75219855bdb953d7e9ff8da9876953a853a5428be`  
		Last Modified: Wed, 15 Apr 2026 21:25:34 GMT  
		Size: 291.0 KB (291016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b805d56aa0bb12df6840037301a097e9d8c991b01763b634df28890710475e8`  
		Last Modified: Tue, 14 Apr 2026 00:07:36 GMT  
		Size: 91.2 MB (91186859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca140d3b52b0ee36e4cd6c2555a1fcd55563497bdfaa50c9ff294ac869e135d`  
		Last Modified: Wed, 15 Apr 2026 21:25:34 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:0a497fa80157b37f8250ac292f0f9d305661c89eeacb173cb74ebdbc18c28857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe119ac39ea3b86d80771b481e242309321eb9ab2c026903b4402590ed68400d`

```dockerfile
```

-	Layers:
	-	`sha256:ba4d69b4b0440bc256aa32226d99e817edfbb2394d33547690f25356eaf7ae5e`  
		Last Modified: Wed, 15 Apr 2026 21:25:34 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:7827c5cb124e573af3d8ddf42e359b14c62cb398662b4c87d325f71762fa3224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94465916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a292f267ef3c9a865f0bc9ae889a617132af5d3c6d4ba9dbfd7cb29431974e4b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:32:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 21:35:32 GMT
ENV GOTOOLCHAIN=local
# Wed, 15 Apr 2026 21:35:32 GMT
ENV GOPATH=/go
# Wed, 15 Apr 2026 21:35:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:35:32 GMT
COPY /target/ / # buildkit
# Wed, 15 Apr 2026 21:35:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 15 Apr 2026 21:35:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7d0f4184e95c7741caefde17b722c67a5e2f80446f00c3126fc30e33e32736`  
		Last Modified: Wed, 15 Apr 2026 21:35:50 GMT  
		Size: 290.2 KB (290165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5edd4ff2dbd145648193fafaa3d5f04805713affd95a7e7d9d0029f6ec1270`  
		Last Modified: Tue, 14 Apr 2026 00:02:12 GMT  
		Size: 90.9 MB (90892470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a011c424aad812e9f6b6ede593eb9a7d459b37b387839887ef8491ba6b612c64`  
		Last Modified: Wed, 15 Apr 2026 21:35:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:ecacb6816202bf15f8fe4ee88de3e15d1d1920343f9aa6081008364a58bf35e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949d1d8ea6988536bdff2258e7c54bde238e59eb9bf2e9e76cc36afeccf82ead`

```dockerfile
```

-	Layers:
	-	`sha256:00d13a3ed1b6d8f1d4202aa35f018d3ed8423a0037b6cc22df3c1426e98ea336`  
		Last Modified: Wed, 15 Apr 2026 21:35:50 GMT  
		Size: 193.0 KB (193018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30d3e4a8d9e3877ab4fa532a6c8fdb094471d87afad873209489b3e5c39451d4`  
		Last Modified: Wed, 15 Apr 2026 21:35:50 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:dcffccd129935d64e6a11eb8b83c1ae19a97c4c6ee64b4548aff02f890aec337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94193782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f6abe6ae2ac03cb6925881137c59ffce276088cdfe54ac99af7c30a0e66939`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:42:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 21:44:03 GMT
ENV GOTOOLCHAIN=local
# Wed, 15 Apr 2026 21:44:03 GMT
ENV GOPATH=/go
# Wed, 15 Apr 2026 21:44:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:44:03 GMT
COPY /target/ / # buildkit
# Wed, 15 Apr 2026 21:44:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 15 Apr 2026 21:44:06 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43356b12db75088b260ca33aae20519a73d8aeb3b3797b26e87106812759ec6`  
		Last Modified: Wed, 15 Apr 2026 21:44:20 GMT  
		Size: 292.9 KB (292862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca293ee12e748379dfc7e49600a21d46479ed1f62dbf74c0006b5ec77222dadb`  
		Last Modified: Tue, 14 Apr 2026 00:03:08 GMT  
		Size: 89.7 MB (89700892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5483721b557dfd6f02b5df6bd7ffa99fb5b3663ca77e24ffd2fb5da195ca50`  
		Last Modified: Wed, 15 Apr 2026 21:44:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:04b7a799ec64b7ffb531bf26fb862b2db35907a69cffeac4508b4ad5347ba27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 KB (218308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d27cf17c22a1d42fa33fca9272cdf0f46064ab9165c25fe302b4c5cbbce78e`

```dockerfile
```

-	Layers:
	-	`sha256:bb4eba6a6eed71eb9362660af5b4fdf488a7149b1ebe5d1fe3faa5eeba1df70e`  
		Last Modified: Wed, 15 Apr 2026 21:44:20 GMT  
		Size: 193.1 KB (193054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aaa50e4963e502010fad104df00b0380a563bd0f738be42b69c0af57b40e0fd`  
		Last Modified: Wed, 15 Apr 2026 21:44:20 GMT  
		Size: 25.3 KB (25254 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:61593d1dbf2fd1d468f51b8ef6d7e53da02c675b84826bb5bc41d1c251af9924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96602490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7941a896331cd8679d0f7e813936b67f58d02429526ca6e6c8519604838aded6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:17:11 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 23:19:29 GMT
ENV GOTOOLCHAIN=local
# Wed, 15 Apr 2026 23:19:29 GMT
ENV GOPATH=/go
# Wed, 15 Apr 2026 23:19:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 23:19:29 GMT
COPY /target/ / # buildkit
# Wed, 15 Apr 2026 23:19:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 15 Apr 2026 23:19:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fe6e8dfaad08024752a284da87ed137a95626202a8e1daa8ed81948391254c`  
		Last Modified: Wed, 15 Apr 2026 23:19:46 GMT  
		Size: 290.6 KB (290629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa5425bebab36322e26303eb33424df1802209b7a6b3dc6b986570aca912bfd`  
		Last Modified: Tue, 14 Apr 2026 00:29:28 GMT  
		Size: 92.6 MB (92621258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734ae46362d0814cfe00e0d4469fdf172a578cbe14c6b2fb78516f9eb284b460`  
		Last Modified: Wed, 15 Apr 2026 23:19:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:4cb37adb1c7fd2d670fe7bf0517c328fc9bb3f06def4e7990daac152e88500f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2df9ef9653642e2e3f5209c7f20abb73709802d7f10e2f1fd14c06748fa325`

```dockerfile
```

-	Layers:
	-	`sha256:f2f2bae96ed6b7eab1ae0e2e3ebbfb1416f5d19179363d298816dff5244e03da`  
		Last Modified: Wed, 15 Apr 2026 23:19:46 GMT  
		Size: 193.6 KB (193607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36774b4c617bb968a2c97a5ebef4ed42cab9e4f98f509fdc1298ffd32ddd664b`  
		Last Modified: Wed, 15 Apr 2026 23:19:46 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:03d7970ceed7d62bab1be62fb5a92f48463fd094b8d455b60e8e3fcde18e6473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95469674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066d97817b8b0baccf2cf2c36b26cddaecac1285280109ba47bdfc36c6cc6f9b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:07:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 14 Apr 2026 00:06:08 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 00:06:08 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 00:06:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:06:08 GMT
COPY /target/ / # buildkit
# Thu, 16 Apr 2026 00:22:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 16 Apr 2026 00:22:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7ccd49384e7556733dfe66ba3c21432bf16a2524fd3822010b69719728c426`  
		Last Modified: Wed, 15 Apr 2026 21:07:48 GMT  
		Size: 293.4 KB (293365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0175a2939aed372a8574a3f30ca86be23817fbc044f643da506137d0f0ef397`  
		Last Modified: Tue, 14 Apr 2026 00:07:09 GMT  
		Size: 91.3 MB (91345222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db74de8ed3636d2debab23dfadb13a2d6221004aae8344739a3491e120f840f`  
		Last Modified: Thu, 16 Apr 2026 00:22:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:dc6feeab1f11502456d13eaf26b61c18309970d8ddcea362379fc9d3e022e35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec21cdfda4dbb5bb4695eae4d1806c44a8a0a5beccf4eeb69b4766e2abc1aa0a`

```dockerfile
```

-	Layers:
	-	`sha256:0ccaec101d07704f728925e0ad339292fc0019ce6354195e1a3f21ad386288db`  
		Last Modified: Thu, 16 Apr 2026 00:22:53 GMT  
		Size: 193.0 KB (193047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d28e5631bba24adcd9aff5800617d3ca6e0db4d1f4bac5a8c155b2a8e9456b01`  
		Last Modified: Thu, 16 Apr 2026 00:22:53 GMT  
		Size: 25.2 KB (25151 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:6c2968e2d480c17c4672c5141f738a09c3c2f498375bfe1f81d5efbb5d7c2002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95740951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7eadd83478bb2f0291d8f1773a739906a44c01907bf294d4bce72aa80e633d1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 08:51:29 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 14 Apr 2026 10:51:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 10:51:28 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 10:51:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 10:51:28 GMT
COPY /target/ / # buildkit
# Tue, 14 Apr 2026 11:38:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 14 Apr 2026 11:38:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653a48053074547bb1f8e43c4e508d8a803d45b52e98210c3539d09ceb870090`  
		Last Modified: Tue, 24 Mar 2026 08:53:11 GMT  
		Size: 296.5 KB (296514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbae07da1d6f03b6754026e98e9959804791bb758eb0115a888df646b9fb60ce`  
		Last Modified: Tue, 14 Apr 2026 10:58:28 GMT  
		Size: 91.9 MB (91858991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a163a5346fb71eb2c3c2e585aa64096b4927b04726a1363083d60e7827dd0b`  
		Last Modified: Tue, 14 Apr 2026 11:39:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e5df4eb19900cd106b9b26535438f087100720e153e52ae7ae7891b0743753b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618b3d8d94d4882ed10eeb1178b7cba39b1a65e7ac4403b83bda9e9a0a22da06`

```dockerfile
```

-	Layers:
	-	`sha256:8e9f631ea9e828c33f2b48c538bb81b8878186e528b3cb0321a012ca317884d5`  
		Last Modified: Tue, 14 Apr 2026 11:39:26 GMT  
		Size: 195.0 KB (194998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ad168a09b1ad231c9722ad618ea6108c9133b9c8f6da801a45e4aa78f5a1774`  
		Last Modified: Tue, 14 Apr 2026 11:39:26 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:ffff6c5fe29b53f2c41906988b42ed63db93d2881ab59bbd93a485f2cf78a555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97796027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad3aec7c8ca490399f1fb2d5c9ffa951dd66be8d5a2de6422274855c8e2e0ae`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:41:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 14 Apr 2026 00:26:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 00:26:50 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 00:26:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:26:50 GMT
COPY /target/ / # buildkit
# Wed, 15 Apr 2026 23:56:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 15 Apr 2026 23:56:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107efaa291b5f83372c13d97ab11aebdd260da2222cd795a4f56930ce905e525`  
		Last Modified: Wed, 15 Apr 2026 20:41:28 GMT  
		Size: 291.1 KB (291147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5aaa70187b5fa60b40f4f6aa959f778263834bd8f55472a34e3a940460eef6`  
		Last Modified: Tue, 14 Apr 2026 00:26:59 GMT  
		Size: 93.8 MB (93778190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed454565d70a685562a80c5fca8f597e565224a1af5155a1a9c7817950707802`  
		Last Modified: Wed, 15 Apr 2026 23:56:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c237a97acb302a1c36c8af68a21e1f56e09524ff99dc54a9fe7463afe0efc578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 KB (218091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17078ebc2a2ebca41a10975e03e9cabfd8b91573e08fc3430495f007ae270431`

```dockerfile
```

-	Layers:
	-	`sha256:4f3f1aed0e88cb9df007815ca5916c635d66bf92e584a313d99104b74b76cd96`  
		Last Modified: Wed, 15 Apr 2026 23:56:47 GMT  
		Size: 193.0 KB (192997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75ab92c73597d8c57e6a91be1df5e536594793ac6fd73bb5f339e60814dba1ec`  
		Last Modified: Wed, 15 Apr 2026 23:56:47 GMT  
		Size: 25.1 KB (25094 bytes)  
		MIME: application/vnd.in-toto+json
