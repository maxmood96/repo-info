## `golang:tip-20260103-alpine`

```console
$ docker pull golang@sha256:99b6cd070f1ca4ad6382b4f2c45aec5695b50688effa5cfc9ddb2030bb40997b
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

### `golang:tip-20260103-alpine` - linux; amd64

```console
$ docker pull golang@sha256:a20379ec93eb3083db8b08db77f624cecd773b41a0939490745b26837ee8daba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99205060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3752ff38c8c3e041c7232592a26b34c100b69c1c9b11050e5afbf8251a841a42`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 05 Jan 2026 20:12:16 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 05 Jan 2026 20:14:16 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:14:16 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:14:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:14:16 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:14:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:14:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1152caf6ae49fb03a2d2365c0051751f5639bf3010cb9ee178f0fe4c00ce335`  
		Last Modified: Mon, 05 Jan 2026 20:14:40 GMT  
		Size: 296.1 KB (296091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff8d0c9ecfcf551b6bfe3152ed041603d59cea546df67e4bc43073bc9a2f5e7`  
		Last Modified: Mon, 05 Jan 2026 20:14:07 GMT  
		Size: 95.0 MB (95048707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d8cc8c52aaee990e783f4215d584406fee60310c88483b74aae0ab884fea1d`  
		Last Modified: Mon, 05 Jan 2026 20:14:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260103-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:40d5eacf62540a32b70000a31ed276e44e2bd79806f23ac00f9d127d86d22e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ffa63c8326b32a0e3e2e83fb4f668357ded670ee026b6b8d145c273bacd3e8`

```dockerfile
```

-	Layers:
	-	`sha256:8b71343d60d712aa580e4d90bddadae5dd61ca11b3ede82273641260bbb89a4f`  
		Last Modified: Mon, 05 Jan 2026 21:25:29 GMT  
		Size: 195.6 KB (195601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a37ccfdf0ed8c614f58179474e6e181ed3ac3fd46baf1d301474707621a8bf5`  
		Last Modified: Mon, 05 Jan 2026 21:25:30 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260103-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:f6fbfda154c80aa0cacd09ed208fb8a1e15cbb9b3004fc1e83307ae27f227aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95272434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413516f5d99a9f89d77a1fc99d0e9355585ac77ab82dd2185053402569a1519f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 05 Jan 2026 20:10:52 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 05 Jan 2026 20:13:28 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:13:28 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:13:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:13:28 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:13:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:13:30 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6dbfc10cf133ef7c306679e593d8f2c3eca2b4aa8f951e2509b0e2efc5fbdf7`  
		Last Modified: Mon, 05 Jan 2026 20:13:52 GMT  
		Size: 297.3 KB (297267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee32a5cb33f89634bd75c31557c25cc9e27ca00d368d41394d0e87b80ed48ac9`  
		Last Modified: Mon, 05 Jan 2026 20:14:02 GMT  
		Size: 91.4 MB (91406577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c205a8bb08758a87d3f961085b1bd7d62fc8d9d94c45425974cc5de36f26af3b`  
		Last Modified: Mon, 05 Jan 2026 20:13:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260103-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:3c345ba876f6adc15babd0de83be22888070067ec4b9a037e173facc00b858e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5a4d0c62cba3bf8f2d425f44f96d128129ab63b4d73156d829f5b2c62b965c`

```dockerfile
```

-	Layers:
	-	`sha256:094b1a8aeb8e22c27e4724dd8c34441c33cdd6301c2f161d5afbb27c4daf2f18`  
		Last Modified: Mon, 05 Jan 2026 21:25:33 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260103-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:d8ef02690c01919655ef4a95e893c5e4c6942c81cde75a736eed0db3ccc1a959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94702042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036bde6eb13d550d466c7776b8fa6a05a15f8d5968fea4d69a463ad1a8558aa4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 05 Jan 2026 20:14:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 05 Jan 2026 20:16:42 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:16:42 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:16:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:16:42 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:16:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:16:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f78981b0a4b9241cd9ccd41207ef6034075edd05ad4851997e10f6c2aa8812f`  
		Last Modified: Mon, 05 Jan 2026 20:17:06 GMT  
		Size: 296.2 KB (296203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e6b96a7f28bc62643bd07c2486d1581cdd92ecf9bab96beac98ff164054e9b`  
		Last Modified: Tue, 06 Jan 2026 02:36:10 GMT  
		Size: 91.1 MB (91126293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f39dd305ee79ba1e5e5a20898c82d2fd0233bd65c7c789436c0f062dc605c1`  
		Last Modified: Mon, 05 Jan 2026 20:17:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260103-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:6b5bb0ffe9ffe230f45b5c540496798ee35e45f6ed159772b84e2ff97da0ba5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb917ffdbca1e9c5fc770e183cd15d0fb0af79370e8bb51045549a26234c3107`

```dockerfile
```

-	Layers:
	-	`sha256:0dc7e3c01590fbb705650fd0966f5f8d77da6a84c7a3672d7a908fa4635479fe`  
		Last Modified: Mon, 05 Jan 2026 21:25:38 GMT  
		Size: 195.0 KB (194971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98c6c4f5451dff74b30c7d1ab06c0eee29afd3af639c61e6c7b390118668ab22`  
		Last Modified: Mon, 05 Jan 2026 21:25:39 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260103-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:1eeaa9d450ab0bcfdcbd7b53877db1c7bc3cb50a1861ae82d82e227a14d1af49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94629212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b562e9bc484bcdb3e4326d7a97929eba77d40319f41495a60ca7199b4139c56d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 05 Jan 2026 20:12:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 05 Jan 2026 20:13:41 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:13:41 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:13:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:13:41 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:13:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:13:44 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343c90774740cd0a8afe0dba95cc7aac089b7f316523581087ee59b087b17fce`  
		Last Modified: Mon, 05 Jan 2026 20:14:04 GMT  
		Size: 298.8 KB (298845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ea799c03d09b63583e3ebd313f2aacd577c4821e87f618e936a7b9c3c7ca14`  
		Last Modified: Mon, 05 Jan 2026 20:13:38 GMT  
		Size: 90.1 MB (90134470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7c86296f7bf6428621f43e4f7b012f701a0e93ba6377fe97ae01b90e237c14`  
		Last Modified: Mon, 05 Jan 2026 20:14:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260103-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:3cd5e8425da8beb05ceb4186271ec774bd4e2521726b96288787727b8513acc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12bc7301d6a011d6a8dae516dd943917c3cab1d0cbe1aa80016d693dcdfc7bc`

```dockerfile
```

-	Layers:
	-	`sha256:2c9d50fd782b9850c5017387d54af0ad271119d0dc1fcc48cb14853d7fea1d6d`  
		Last Modified: Mon, 05 Jan 2026 21:25:43 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b20c2310038c1a2d174e0da7f51e7281870edc16b411dcb11bffe5c8c06255bd`  
		Last Modified: Mon, 05 Jan 2026 21:25:43 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260103-alpine` - linux; 386

```console
$ docker pull golang@sha256:bd70d97cb707754404788a4f6d445275843c02b4379910afb0eddc395aeda76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96927740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246e8804d8e396e75a3f897ce9036542bedace31d932f4925a3439a58c4e6be0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Mon, 05 Jan 2026 20:13:56 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 05 Jan 2026 20:15:52 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:15:52 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:15:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:15:52 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:15:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:15:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111ea4680647ae2e898d6ba5aede0d95152de91387f4a51ed346a96f20430a0`  
		Last Modified: Mon, 05 Jan 2026 20:16:13 GMT  
		Size: 296.7 KB (296671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7adeeca0c05b570f562d36e2ca80fe92bff9d338efdfb31d2c7a616347bb0c`  
		Last Modified: Mon, 05 Jan 2026 20:15:35 GMT  
		Size: 92.9 MB (92944811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c3f6915a48de406cd095e8316197f3043370dc01f6cc595d21f3887d00e891`  
		Last Modified: Mon, 05 Jan 2026 20:16:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260103-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:b804e27283358fa86cdd0fa7e0cf8a73e82d91c48b549363de1c87e83ad9715c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246992fb2c29ffedb448dbdcb3531927a6bad5cf4f7dee4433b1e79d5a636720`

```dockerfile
```

-	Layers:
	-	`sha256:dc30d07ed7abd25b08eda6183c5e1ee86b86e31dafae8be06daed7bcc15981cd`  
		Last Modified: Mon, 05 Jan 2026 21:25:47 GMT  
		Size: 195.6 KB (195560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:531e7b00b3b7cf30d4b40c97286fbcc4383aadbdfc67bf820fdee9b4f195b5dd`  
		Last Modified: Mon, 05 Jan 2026 21:25:48 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260103-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:86861fc837763e526d26c4ec4f363c7f0ef5ce2b733a159c37c69635b363846d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95807812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf57b545f65ae38c195748514e70837a07d38d45df2035b371d4200835fa85a5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:36:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 05 Jan 2026 20:13:42 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:13:42 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:13:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:13:42 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:19:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:19:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c251744709998ea3415429d77aa83c1ba367b71bf12c4b11c84d3ff1d0c4b550`  
		Last Modified: Thu, 18 Dec 2025 01:37:40 GMT  
		Size: 299.3 KB (299257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd0091ff10375737167c3b5f9f5d9decb460a2e2aef6a9ae134067abb7cbf2b`  
		Last Modified: Mon, 05 Jan 2026 20:15:39 GMT  
		Size: 91.7 MB (91680642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fb74ace9a8976166d6d75144101663fcc3af67968f24ee4320a7b7c9eb792a`  
		Last Modified: Mon, 05 Jan 2026 20:19:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260103-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:781d3f01d5b6e520ac26311298b7ebe5ba172874feb27bfa7b19bcb09237466d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf57916edf0111220b092b3c60c32870814ef5f78c8be416cc55ff82d6ea32d0`

```dockerfile
```

-	Layers:
	-	`sha256:86ea51910b688a2efc34508cb966fb5cdb72514878457856eeed3fe317aa1a9c`  
		Last Modified: Mon, 05 Jan 2026 21:25:51 GMT  
		Size: 195.0 KB (195000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42f499858dedd43573bdca317969be7328b1c158eecc3e9bbc11df4aac60a1e2`  
		Last Modified: Mon, 05 Jan 2026 21:25:52 GMT  
		Size: 25.2 KB (25152 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260103-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:9c8757e81d94c4070ce3c4922369b84b24932eea1196f18ebe96471af1299412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96193498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9308d3b067491da819092efd6d7b1b388dfbac818069c641387fa609ce384d0c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:47:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Jan 2026 01:07:38 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Jan 2026 01:07:38 GMT
ENV GOPATH=/go
# Tue, 06 Jan 2026 01:07:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Jan 2026 01:07:38 GMT
COPY /target/ / # buildkit
# Tue, 06 Jan 2026 01:51:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Jan 2026 01:51:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c358a50d2f39217ca62c3bf8831f5ece762bf2d424204f727fa6a6f9f5124f1`  
		Last Modified: Fri, 19 Dec 2025 05:50:24 GMT  
		Size: 296.5 KB (296519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c89a20e33326bd3dc067a98c23f95a9f71a46db050c57b5d95bf4165852889`  
		Last Modified: Tue, 06 Jan 2026 01:15:07 GMT  
		Size: 92.3 MB (92312883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc19b76a833078be1fab221380801dac38212718ad3c929a4a9ff5ed5e74b28`  
		Last Modified: Tue, 06 Jan 2026 01:52:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260103-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a548cb1d878494627728db28d67cdfab9219fc8d18a84fca409761ee3712c5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65390fc199f442bdfa6d4fe4993db5fb8cd2df5698f3c0b71dc7b4071a8f2799`

```dockerfile
```

-	Layers:
	-	`sha256:5cd5ed6a1caa81fce1437fe2e21b93a4254677a83dcee745dc384d12a6944769`  
		Last Modified: Tue, 06 Jan 2026 03:23:55 GMT  
		Size: 195.0 KB (194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13ca42ee3f2143d5a5f5310ae49d441c2710b714e68fd09e37e7f4049d4518a3`  
		Last Modified: Tue, 06 Jan 2026 03:23:56 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260103-alpine` - linux; s390x

```console
$ docker pull golang@sha256:6e44be16b88a429e535556a85bb6c6c3a8a02ded94a2edaff62834008da086b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98246155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e0f922e1271c18d7e0491bc08cbba928b2e1b73326812714046f1a28c5f19d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:14:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 05 Jan 2026 20:14:09 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:14:09 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:14:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:14:09 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:14:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:14:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7224d7d29671ca737c9ec945a7373478caed2bbfb74b122f8685b8c92149198`  
		Last Modified: Thu, 18 Dec 2025 01:15:01 GMT  
		Size: 297.2 KB (297192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c1a057ff0ba348d0b96ad5fd481980beed6ee225e3440d5e3c814a12014a9d`  
		Last Modified: Mon, 05 Jan 2026 20:14:55 GMT  
		Size: 94.2 MB (94224494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1eaabdd361e43483fbd24635d6f26cd04691ece4a50ab90e49ac325ab1e1af`  
		Last Modified: Mon, 05 Jan 2026 20:14:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260103-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:fcb9fdec00aaad99bb92cc12467f329fab6dd8c251ee316a7a695f8eaba51d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 KB (219872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6587e3e42cfe083df464cae5c92da9ff3b6a23f308818f04493d5748a671eea`

```dockerfile
```

-	Layers:
	-	`sha256:4dfe6cf6de783c0ae24dac3e3cd22bc6ff1e71aece1b245ed26c2d6f3df91004`  
		Last Modified: Mon, 05 Jan 2026 21:25:56 GMT  
		Size: 194.9 KB (194950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90168f25d57bbf3237f1baa2b945d801db6448ab2029e6b61599d05361cd0e84`  
		Last Modified: Mon, 05 Jan 2026 21:25:57 GMT  
		Size: 24.9 KB (24922 bytes)  
		MIME: application/vnd.in-toto+json
