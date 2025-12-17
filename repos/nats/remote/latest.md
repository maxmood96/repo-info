## `nats:latest`

```console
$ docker pull nats@sha256:4966783b7b37ed3fd8af03ea9e88e37fda0bc80cf7d9bb447b83f6af23aa4b78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.4529; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:409d49daf0939f5e7d8cde71d214d33af5f082a3f413399223dd0b08d2fc50aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6591138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2aa68383287bc4011abbb0cda6516a3a4c06e62dd9d51014d5f83e7efff7e80`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Dec 2025 20:01:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Dec 2025 20:01:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 17 Dec 2025 20:01:26 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 17 Dec 2025 20:01:26 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 17 Dec 2025 20:01:26 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Dec 2025 20:01:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4acd967ddc02590a1f9db5c0ab104a521c3b01c4fc3ca5ced9eeff9ee3ba3c59`  
		Last Modified: Wed, 17 Dec 2025 13:44:10 GMT  
		Size: 6.6 MB (6590629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0103929f5e0e3db1b12e36e1aeff3c923eddff5d1968e3d0f22b3f7aa30ebba`  
		Last Modified: Wed, 17 Dec 2025 20:01:35 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:a226abede1d8384071e63eb0257452b99108eaaea6501acd919580c2ec3e3232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a153786df027a7d066c8f5784f26e41ed9689710d05d147a66218be1b4dd1fd8`

```dockerfile
```

-	Layers:
	-	`sha256:89af6a462dd1e2f4e92326ee7e0ef9f89f947b5a380af7de2ddcacc09f645306`  
		Last Modified: Wed, 17 Dec 2025 21:56:32 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:3853bb8507245773d5a8ce05deea7cfd9f4da723b2c363480580cc012ca53270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93286d48902d584731e848087c653ac0a6d01e8425909fc66515ffaefe8acc14`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Dec 2025 20:00:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Dec 2025 20:00:39 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 17 Dec 2025 20:00:39 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 17 Dec 2025 20:00:39 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 17 Dec 2025 20:00:39 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Dec 2025 20:00:39 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8c692c13a40e92100ded6771cbbc3a0d5bf2526f18f3fb0a48f15be60c2df82b`  
		Last Modified: Wed, 17 Dec 2025 13:44:11 GMT  
		Size: 6.3 MB (6313188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631effd298b53473939d3adcebf4dec825a0b3d91fa6fc10553e7ddad15928d5`  
		Last Modified: Wed, 17 Dec 2025 20:00:53 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:a12d6f521214dc21cc2bcdc941aa35f4ec314380c729cdfdc42c3aa6d6bfc542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaab9a175ebb399933d1c8ea3f50398dd348dcdf598f5424f2921569526e82d2`

```dockerfile
```

-	Layers:
	-	`sha256:43b1dc7d6b077ab1f2267d99aa3a71b675795ee1f57b76f8a7ecd3d05fcdd480`  
		Last Modified: Wed, 17 Dec 2025 21:56:35 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:e94a35025c028537959412b3781acd5c082d9d6128056903a36fd72303137cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6303727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f76d4a21e40bc97da539f87250554131486a6b9c78c7f1cb563c0d439eca6ab`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Dec 2025 20:01:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Dec 2025 20:01:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 17 Dec 2025 20:01:23 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 17 Dec 2025 20:01:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 17 Dec 2025 20:01:23 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Dec 2025 20:01:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:01896e41e5c875829be6c7302849d50cafb36c60f2d5c87a51de5fabf2685566`  
		Last Modified: Wed, 17 Dec 2025 13:44:10 GMT  
		Size: 6.3 MB (6303218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab6380a921e8bfb9374117891c2d4b44f70dbff897277d49684e71993aeeed6`  
		Last Modified: Wed, 17 Dec 2025 20:01:37 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:bdeeb64af43ebd422511c43d18c5a021b9479759aa01ecee8697b08b7fb4643e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:effc5987cb319c0e4e830fe710b565d3b22924a14ccc2cf7c699563cf61c77cb`

```dockerfile
```

-	Layers:
	-	`sha256:7b416a76ffa2ed1d1fa53988ed093bff6a8848e20a45bb7a0a886694eb1e40d8`  
		Last Modified: Wed, 17 Dec 2025 21:56:38 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:84d27658916274fc90839c8b5bf429b19e31cbb1b75c0f0a3a182f9279cde8eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6003867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f75f93cbc9093743fb6bf5ee34eb5be475b654219900b550d3165c0581cde4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Dec 2025 20:01:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Dec 2025 20:01:20 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 17 Dec 2025 20:01:20 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 17 Dec 2025 20:01:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 17 Dec 2025 20:01:20 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Dec 2025 20:01:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f4415656319a68dcb618baeb6a60d650defd1f514a481e6f6330af14c4fceaf5`  
		Last Modified: Wed, 17 Dec 2025 13:44:10 GMT  
		Size: 6.0 MB (6003360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4accf7902539648ceff59ea4a622f93d63233a3be68792f88eea5f1cc22b62c8`  
		Last Modified: Wed, 17 Dec 2025 20:01:31 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:0686bfde4b19aeb60c7a324a5b424e778381949910a579bcd02b4278b37178cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9a1a0cf88ef6c816b9693ea6fcb3cb96324947044e828f401611a57feb07ed`

```dockerfile
```

-	Layers:
	-	`sha256:69f25a8aa435a51636bb06e19bfeb02c5b239c55ba93c340ddef2ae067172c61`  
		Last Modified: Wed, 17 Dec 2025 21:56:41 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:c2b63aa758462e86058c91fe8401191b41043d2163a78fdec57519d4f0b49998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6053571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c2636ef42b619db39e1975f9b631869bc3c3b24489f7866a08171ddcc5033c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Dec 2025 20:01:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Dec 2025 20:01:33 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 17 Dec 2025 20:01:34 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 17 Dec 2025 20:01:34 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 17 Dec 2025 20:01:34 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Dec 2025 20:01:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fff90457358766f5b735feb2d49e853cf695210b8abe6ba57edc0abce8282fd8`  
		Last Modified: Wed, 17 Dec 2025 13:44:10 GMT  
		Size: 6.1 MB (6053063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589282b0ff2ad41789a44317f1ea281a1922d78ec8dbf8a031acc22733f31036`  
		Last Modified: Wed, 17 Dec 2025 20:01:51 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:d7d1570fb25ef2bda69d3d006ba8f47a5bd2a378411613cb7f881e8ab5078488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed570c2ba4ccaf310e9bacf729785e05e597e250ef1e4f162cd4184a0794cf04`

```dockerfile
```

-	Layers:
	-	`sha256:f91f2c07ab8052b7c97b473ee388d713a2cb3c94fbc741e2892b0a738632be01`  
		Last Modified: Wed, 17 Dec 2025 21:56:44 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:28f34bed0a682b4aa4eedefde127516cf11d48fe189b5012061d4ceead86a883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6432293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34db5d9b7c6ad05b3a0206e1c4bc40e08f029d7a4ceb4f9a193d6fef9f3705c9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 17 Dec 2025 20:01:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 17 Dec 2025 20:01:39 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 17 Dec 2025 20:01:39 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 17 Dec 2025 20:01:39 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 17 Dec 2025 20:01:39 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 17 Dec 2025 20:01:39 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f8e43cf01609735e89620aa1f85d5675eccdd17850b8f0944070d6fca83f5f31`  
		Last Modified: Wed, 17 Dec 2025 13:44:11 GMT  
		Size: 6.4 MB (6431785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efe491c24bd21151ceadabf60f82f7288e106c5c5b2e1cf0a0e303fd951a962`  
		Last Modified: Wed, 17 Dec 2025 20:01:55 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:64a2cb9ff1e0f5b75e2e53f9f9ccbb96c66e914c524763620814e9606fef2057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e6c0882b54633cd5fdbda1ba2a5bcf53fc177361102c5052cb69a80692dbab2`

```dockerfile
```

-	Layers:
	-	`sha256:62f918a7cdeb02a6e02929e5b0c8f5dbe6366961c236880f3d712024736b37d8`  
		Last Modified: Wed, 17 Dec 2025 21:56:47 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.20348.4529; amd64

```console
$ docker pull nats@sha256:5ade3b8097e2c50045d7cc5b9916a1321e3f818b0f69cc7a634875e82710b5d9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133135109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683da254fb63f0c8cc5b83a6a6886eb0b42cb4d1d93a9428bb4501e1916755e9`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Wed, 17 Dec 2025 20:08:30 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 17 Dec 2025 20:08:32 GMT
RUN cmd /S /C #(nop) COPY file:ec94fa0a8d5bdb04f4e8f7e8ecc10a64d72990dc4ba8ddff1a8c14d23473ba63 in C:\nats-server.exe 
# Wed, 17 Dec 2025 20:08:33 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 17 Dec 2025 20:08:34 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 17 Dec 2025 20:08:35 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Dec 2025 20:08:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4379c3ab1892caff9ef2f09d2151fe9c94acf23b255c7d428856217a4471cc26`  
		Last Modified: Wed, 17 Dec 2025 20:08:50 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed88622b97e1e8bc58e7e06c582dabc0960f88c7867718f137df1317df14a43`  
		Last Modified: Wed, 17 Dec 2025 20:08:51 GMT  
		Size: 6.8 MB (6770883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7f74d617f9673094225d8b877378420e0abe0f0d053a55b42227c4e0372eb6`  
		Last Modified: Wed, 17 Dec 2025 20:08:50 GMT  
		Size: 1.7 KB (1700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f18ccfaa70090ed55b2ff35289f33e2afda0692a803f7d03dcb5feb802997c9`  
		Last Modified: Wed, 17 Dec 2025 20:08:51 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1199736a2361291ce2d46dd331a637415989e45930d7911bd7e1938535b12ada`  
		Last Modified: Wed, 17 Dec 2025 20:08:50 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed3a3fa4f1b13762dd50df7e973f336fd8d84b4d13104f77f04454e3e7615b4`  
		Last Modified: Wed, 17 Dec 2025 20:08:50 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
