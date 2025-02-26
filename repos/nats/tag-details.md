<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.21`](#nats2-alpine321)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.21`](#nats210-alpine321)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-1809`](#nats210-nanoserver-1809)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-1809`](#nats210-windowsservercore-1809)
-	[`nats:2.10.26`](#nats21026)
-	[`nats:2.10.26-alpine`](#nats21026-alpine)
-	[`nats:2.10.26-alpine3.21`](#nats21026-alpine321)
-	[`nats:2.10.26-linux`](#nats21026-linux)
-	[`nats:2.10.26-nanoserver`](#nats21026-nanoserver)
-	[`nats:2.10.26-nanoserver-1809`](#nats21026-nanoserver-1809)
-	[`nats:2.10.26-scratch`](#nats21026-scratch)
-	[`nats:2.10.26-windowsservercore`](#nats21026-windowsservercore)
-	[`nats:2.10.26-windowsservercore-1809`](#nats21026-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.21`](#natsalpine321)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:b715753bac33754e4ed5c71b7445cc25d6b881fb22d022989ef2844196ce1c2e
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
	-	windows version 10.0.17763.6893; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:ab30601c4ae2e5de749e7e013dbf1bc8c5f948795d9ba14dfda2cc484f87b552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5923576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736726958d6b2f0e21680f7a56521500766540e90084a54a726a2672e345e95f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ea1d4d1eef4999bdc608bafb79b4807c2e0d126548d7f7d6e3a9b542c153bab`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.9 MB (5923068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8394405f954a1600ce69d033d4616992e140b23520ef911b5e8cb3c9fe0a0bab`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:f6eb9f0ff1ba7f1080413295e1bd058a3eb8eaa6346a04ce30d9b12633f178a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5fc4acfc4fca3421337954440d9551afa9681b105c24998d64a27f4f385456`

```dockerfile
```

-	Layers:
	-	`sha256:41f7e4d13b7d0cafe62fb08f772bde421af4e46d7c80aa8051eada0b71e2d6ad`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:a37f3705ca4f359f2cd688f2f2915c89396f3242ed0017031b1d1ac86b929f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5587283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa848ded2e7f822233d14d085a59458f091b55a5caad5800e30d9759389aeac0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7931d39fd2726f7116d27b851850cf4a1ff6e69fd3de1ed621bfe728eaf4c32`  
		Last Modified: Tue, 25 Feb 2025 19:16:31 GMT  
		Size: 5.6 MB (5586774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526621f9915e8bc26b6f41cb0b4ec86f849a2f797e44f1891bc4ec17549827f4`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:2fc0d021712bbbf87403b2efb33aa02fd447167450cd57cbd42e75ddc5fd29ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6710a8bb2aed7e8414816e8dedcb63a21a481320f77bf39efdf73bc7bb11668e`

```dockerfile
```

-	Layers:
	-	`sha256:92236e3a37db849c42f54749091d19b6ef1c03b5d1c5d1bf501fe9ed7360131e`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:da5d81783ddfc4e6e5ea9c7e9627dbae2052e148b0ca4c3a5adf3e8cdf5881a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5577156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c3470f5d2f8c4e3cdafea8433db44a91110f01e60967c2a3a8d978e31baaed`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0cf7641a4057a532da4f664f9cec79f7fe56c198bb9e71bcbc2c19bb907c58d5`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.6 MB (5576646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3463297bf29a5bbf37928948bb32bb57b1741d42493f2ae75ed53175a517af`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:8be21b20d1b6e3d2e901bce12f29bafce42afbbb1b762be62bfc195cb7e9b3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3610a7ae663a5ca8c8be4540df39767d306086365de3263700ddcce895420387`

```dockerfile
```

-	Layers:
	-	`sha256:234087f90831097305eb3b9065da97b803a126593235b546269cfbfa625f608c`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1ab5a26d1f1b792832dd7d52e60d8f57fdcb0ae690e943d796b2b3dea26599c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5471384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96361ef0a1d425f77a7d5bf22cccb8ab926a283d25551390017dcc936f8d6ddd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:34a7e29168d12cc49e3fd1454925bc4b2f10137b37fb10cc85f3b76f5e2959b9`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.5 MB (5470876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0851ead742e7b3af0d74476f1e7610234b00ab6bde066faf665277f50cd3c4c`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:4424673c4c02b57552cb838402189f34638ab966b9f85359bad2c59ee9ece0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68e730f04dffe04ac9fcc8af9491ae6be3a7b9be23078e4acc7d0f36fb24ca`

```dockerfile
```

-	Layers:
	-	`sha256:2f7c0d301103a7e55953e57ee1a1660e241006b0b659cffea67752432c2b5ab2`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:1bb4f59414ad9587da0bb4e32ff196ef02914c7e8225b5f3c1a3b79e521de195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5434760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ad4a1f1ab680fc057eaaf6c15371c9fda97d7ac3fa04092cefc46564cceb59`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3821b02a9a90c20826ffaffe25f12d7283677acc84047703af05ac61729fd3da`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.4 MB (5434252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a956e9b697668bf98cbe2a5ec65f9e9c0368945ed81d9e43faa5d064cf6cad4`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:e7bf236217d62b740ceeef3cf7150a2b66bf5c247d8d6ffbd991288ec58f799e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe4ef235be79096172af5671be15debaba38653149f5fe74fb76d2c59390183`

```dockerfile
```

-	Layers:
	-	`sha256:baa43bb7d01b88047f62ca6dc61952a118a1bc2c2a3222dbd65a322a26523d7d`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:84fbc6a0d4f3a6242710d3ea5b8ab4578403aa53d8a5302026bdd6ff20ced27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5777700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcaaa0f666e7b95fe6b20c8bbd70eadf8213e2790de894c72c9f7aa30939f4f0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46891594ec8b4d3680a1bbfe2877deba49c42d5db2b71635cc53e7a260da8759`  
		Last Modified: Tue, 25 Feb 2025 19:16:32 GMT  
		Size: 5.8 MB (5777190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642410c76d1bbecfc24938ff297ac86ca1a30d14e8ab6ef3e9beb0decbbb955`  
		Last Modified: Tue, 25 Feb 2025 23:28:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:192747a24178676ee22ac82db357523716ac68b38738fc729a9044432e7b8815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2f83f8a72ce10467cc585601118bc7a449b8d32a56af2df1c019124dfe4ecf`

```dockerfile
```

-	Layers:
	-	`sha256:841b5965931663c1f16aaccf610709337098323a7168962634fe4bed2d16175f`  
		Last Modified: Tue, 25 Feb 2025 23:28:06 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:6a4cc4d864f9bac7dc07b623679bf121113d41d21fc9b5e640e3c92fca1e5111
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112965803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0766c346c8b6c207312a07351709a6e4da8cd036fbaaa8c380d71c1d32ae393`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Tue, 25 Feb 2025 22:17:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:1eb0b36109ac529ab5d5db4ea880cfd63ed514d1f542c8bd20a200d73207ed8e in C:\nats-server.exe 
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 25 Feb 2025 22:17:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464c91c36773a1621c7277522f95c645dc9866e58b0867242b34277fc4145ada`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0903b195c823336fbd58a8a52901057cbde5d4f8e8a3fe8d643f7f0b1008ee5`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 6.0 MB (6044491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a624018395b9843449197873a8dfbfcd7cc07efd09eb9f5cb1fe8b5638255438`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbf5f27ca2dfe7fd5ede70769269354cf7852fe304a1af5d4b7bd17e201a74`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0a43a1bf148b020d83f3b26345be5a7f7cdc277350321ce4ad5a4e0fc73662`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3091f851d62e9660edca35a087ab74e6ce5c1ab16cd2dcc10c87c3b1e04be8`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:d69eb29526c1d98afdfb2e2434763bef77b5f3c83e2e24769c13a4d104be475e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:6e0cca2c6da79f0a3542ec5a3319dd10b1b05f5d8e8949afa8e9cdf6314bbf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10026010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e556ce07f949f5717c6dc8daabda0e17ded6419df74f43518c1f56c1e329c22b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1935954c94119c3706036d5d692853435b83d99c259f8ec51495e3e2efb18a6a`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 6.4 MB (6382794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06613330ae8540f47d41506b7d56df4c5bc71440bf813153c79399e3f5da3c5`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19394475462d5b1aea3c36ff72f30a11aeeb4f440112ebbb15b8a456f653ac55`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:58a608a3d90a3e203ff98c7e1e6bb1d98dcb587196fad9b5046c6a18e27c30e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0ae8cc81e579896c7a782ec0a7819a1abc513aac53c0053d0d8c8707a6100a`

```dockerfile
```

-	Layers:
	-	`sha256:55c1b3c18c84cf1aadd36f17ae37f6e463386696329d2f7845b2b7c772969160`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:888b3676fa9b74db3d6bc52a06a90ec37388f17f7a6c94fba1b0aab761c8d1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9412308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdbc5759068b8c3c7c0d9717f2fa31a8802843622ffa5bc1ee90ab2f97cc836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950d5a437e93fb02cf36f9a20e870f94dd8ac2842175b525de18d73671af6aa`  
		Last Modified: Tue, 25 Feb 2025 21:26:33 GMT  
		Size: 6.0 MB (6046604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d39378960e3fb615203a449ee86a6adc427a58bb348af84af623f9137eddb11`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1ce7e529762c20edc862cef19f51119c18e640a72162538b361811aac9cf6d`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d2f4a4f725f456222c0e0a232f481981a98db2a040b8e5e03a46ba5d19de93b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e467740581e449ded36748d517fc3d41e73c080a765637ab847143ff92b4c0c7`

```dockerfile
```

-	Layers:
	-	`sha256:64782c75142fcb4da7de03639949321d926dd843f9e85121ff5cc18d20715dac`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a1745de189516c48458486fde6b403abc48727f7e2dad55b951a85a77761e2bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9134853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e833dd9f4430c77bf7a6f708e9e6e002d936da7c311595bcdbb9d5979d2b8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2e5935cbee970cdf8caa27a6dafa7c7e944ca51b4d5b9a1c3b93ff3053eb4f`  
		Last Modified: Wed, 26 Feb 2025 02:51:22 GMT  
		Size: 6.0 MB (6035762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb14c94ff9b267a96d276f33d9182a887b066ea83d612971ecc3f07a5357233`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba509bbe23f7c8d23d12b140bf072518aebbb51dac6ac1a53d7dc7c21356dc`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4feb4a911e61e83936b9beb43d347f961ca2560f45191694f78f33d59d58755b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00883483bdc919a66a85b4f2f8521a2ebd1646c8f932d3437be0e289d01313a`

```dockerfile
```

-	Layers:
	-	`sha256:f5175fcbe6f613a2932126ce4d0da80ad1ab95ea38ae164d75b44f9eb774893e`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f9fb7d4a001bdeaf8efe662379474e453f8e63844b5c0913680367fe3124295a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9926441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6700a7a44644d35a74467c9dcbbe2492e70d661075b7755d96a3cbae0229ff7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8405433bc52db97fac8fbd2bd06458903c03f86a2d80d9d5de11d642868850f3`  
		Last Modified: Tue, 25 Feb 2025 23:33:53 GMT  
		Size: 5.9 MB (5932443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704f25bcef9e2d1d2333773f3c5b74abb44de6b6acf941f327d8672bd7ffe138`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5be759409abd41f18a0ac584e5d7d5a24910f005e7c64a45f84ebaf540f34c1`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b07c213de9995bce905bae01e3d3c91262c6ced69feb9739a94cc6e70b6c4941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98276d55b0f5cba673066fca22f6cae9b01c363da2f4f6a99dd3c9295bd32e82`

```dockerfile
```

-	Layers:
	-	`sha256:1b55454322f3ee2db01f280284055234c7a64d43c52c7cc0da084c9ccf4474fd`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:1e5c65a5b378164fbc055112722da9af33284202befb128e9716dfc8d8f998b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9472260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f9943fe40a1d887d0477acbedc42a3822bb2ae7f9ae3f8a2f3bc988aae0c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ad6d76a28889f354cf5c7376c4cd2238dc37a73bae19f1e12a713f6e666bf2`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 5.9 MB (5896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca8c83039c331226a414edca0991c08f1d9f07cdfab82595fbee7aed442ef69`  
		Last Modified: Tue, 25 Feb 2025 21:28:54 GMT  
		Size: 563.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad2d41ba212a6f1ff2dbe03563c50fd26cb7d51e46c4d08af2f4097c759e5c0`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cbfb602ab0fd542d76b033b69f65563107aadb7811c6215a22d44c215bfb9219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6596c1301cd69cdc9984c62cdabbd98209cacedd5cc4c6744c3badaf073080fd`

```dockerfile
```

-	Layers:
	-	`sha256:c5d5cfc84a3213cec6cbc7a0bff5c8f50266b3ffc1f0164f61a05ae22293b11e`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:3b8989b0fec1ee207ccdf0f52aa99b9ddd8d3902c1203c501e2d8272949de8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9707272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814240ee91751bb8caa1b427d6fe215c399953d2a8c1da768008d647eedba145`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a056f2f8e8ae073c4ef4c378c426dbf016cc4044eb5010d4c82049d61b8a47`  
		Last Modified: Tue, 25 Feb 2025 22:15:40 GMT  
		Size: 6.2 MB (6238736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccf3a43c9e162fc6fef2651da01103a02bca98d38462fe6395b9b4e6dc96a64`  
		Last Modified: Tue, 25 Feb 2025 22:15:39 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5067f57e0d418f66b609217b8ba7caa018ccab3ac38922d7c4797451579b7468`  
		Last Modified: Tue, 25 Feb 2025 22:15:39 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:66af7d583747898efea9f67c3ff93f8aa993f068528a5aaf50e18a5ffaae2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f226705d21a1826de8bd2c6ee20c35e3966881d96443741ee0b7ff81e103e4`

```dockerfile
```

-	Layers:
	-	`sha256:2db5025980dad4fcac824b97547a716063d145967c77ec341d5394357d3c0e90`  
		Last Modified: Tue, 25 Feb 2025 22:15:40 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.21`

```console
$ docker pull nats@sha256:d69eb29526c1d98afdfb2e2434763bef77b5f3c83e2e24769c13a4d104be475e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `nats:2-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:6e0cca2c6da79f0a3542ec5a3319dd10b1b05f5d8e8949afa8e9cdf6314bbf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10026010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e556ce07f949f5717c6dc8daabda0e17ded6419df74f43518c1f56c1e329c22b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1935954c94119c3706036d5d692853435b83d99c259f8ec51495e3e2efb18a6a`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 6.4 MB (6382794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06613330ae8540f47d41506b7d56df4c5bc71440bf813153c79399e3f5da3c5`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19394475462d5b1aea3c36ff72f30a11aeeb4f440112ebbb15b8a456f653ac55`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:58a608a3d90a3e203ff98c7e1e6bb1d98dcb587196fad9b5046c6a18e27c30e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0ae8cc81e579896c7a782ec0a7819a1abc513aac53c0053d0d8c8707a6100a`

```dockerfile
```

-	Layers:
	-	`sha256:55c1b3c18c84cf1aadd36f17ae37f6e463386696329d2f7845b2b7c772969160`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:888b3676fa9b74db3d6bc52a06a90ec37388f17f7a6c94fba1b0aab761c8d1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9412308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdbc5759068b8c3c7c0d9717f2fa31a8802843622ffa5bc1ee90ab2f97cc836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950d5a437e93fb02cf36f9a20e870f94dd8ac2842175b525de18d73671af6aa`  
		Last Modified: Tue, 25 Feb 2025 21:26:33 GMT  
		Size: 6.0 MB (6046604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d39378960e3fb615203a449ee86a6adc427a58bb348af84af623f9137eddb11`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1ce7e529762c20edc862cef19f51119c18e640a72162538b361811aac9cf6d`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:d2f4a4f725f456222c0e0a232f481981a98db2a040b8e5e03a46ba5d19de93b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e467740581e449ded36748d517fc3d41e73c080a765637ab847143ff92b4c0c7`

```dockerfile
```

-	Layers:
	-	`sha256:64782c75142fcb4da7de03639949321d926dd843f9e85121ff5cc18d20715dac`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:a1745de189516c48458486fde6b403abc48727f7e2dad55b951a85a77761e2bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9134853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e833dd9f4430c77bf7a6f708e9e6e002d936da7c311595bcdbb9d5979d2b8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2e5935cbee970cdf8caa27a6dafa7c7e944ca51b4d5b9a1c3b93ff3053eb4f`  
		Last Modified: Wed, 26 Feb 2025 02:51:22 GMT  
		Size: 6.0 MB (6035762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb14c94ff9b267a96d276f33d9182a887b066ea83d612971ecc3f07a5357233`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba509bbe23f7c8d23d12b140bf072518aebbb51dac6ac1a53d7dc7c21356dc`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:4feb4a911e61e83936b9beb43d347f961ca2560f45191694f78f33d59d58755b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00883483bdc919a66a85b4f2f8521a2ebd1646c8f932d3437be0e289d01313a`

```dockerfile
```

-	Layers:
	-	`sha256:f5175fcbe6f613a2932126ce4d0da80ad1ab95ea38ae164d75b44f9eb774893e`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f9fb7d4a001bdeaf8efe662379474e453f8e63844b5c0913680367fe3124295a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9926441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6700a7a44644d35a74467c9dcbbe2492e70d661075b7755d96a3cbae0229ff7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8405433bc52db97fac8fbd2bd06458903c03f86a2d80d9d5de11d642868850f3`  
		Last Modified: Tue, 25 Feb 2025 23:33:53 GMT  
		Size: 5.9 MB (5932443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704f25bcef9e2d1d2333773f3c5b74abb44de6b6acf941f327d8672bd7ffe138`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5be759409abd41f18a0ac584e5d7d5a24910f005e7c64a45f84ebaf540f34c1`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:b07c213de9995bce905bae01e3d3c91262c6ced69feb9739a94cc6e70b6c4941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98276d55b0f5cba673066fca22f6cae9b01c363da2f4f6a99dd3c9295bd32e82`

```dockerfile
```

-	Layers:
	-	`sha256:1b55454322f3ee2db01f280284055234c7a64d43c52c7cc0da084c9ccf4474fd`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:1e5c65a5b378164fbc055112722da9af33284202befb128e9716dfc8d8f998b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9472260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f9943fe40a1d887d0477acbedc42a3822bb2ae7f9ae3f8a2f3bc988aae0c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ad6d76a28889f354cf5c7376c4cd2238dc37a73bae19f1e12a713f6e666bf2`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 5.9 MB (5896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca8c83039c331226a414edca0991c08f1d9f07cdfab82595fbee7aed442ef69`  
		Last Modified: Tue, 25 Feb 2025 21:28:54 GMT  
		Size: 563.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad2d41ba212a6f1ff2dbe03563c50fd26cb7d51e46c4d08af2f4097c759e5c0`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cbfb602ab0fd542d76b033b69f65563107aadb7811c6215a22d44c215bfb9219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6596c1301cd69cdc9984c62cdabbd98209cacedd5cc4c6744c3badaf073080fd`

```dockerfile
```

-	Layers:
	-	`sha256:c5d5cfc84a3213cec6cbc7a0bff5c8f50266b3ffc1f0164f61a05ae22293b11e`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:3b8989b0fec1ee207ccdf0f52aa99b9ddd8d3902c1203c501e2d8272949de8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9707272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814240ee91751bb8caa1b427d6fe215c399953d2a8c1da768008d647eedba145`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a056f2f8e8ae073c4ef4c378c426dbf016cc4044eb5010d4c82049d61b8a47`  
		Last Modified: Tue, 25 Feb 2025 22:15:40 GMT  
		Size: 6.2 MB (6238736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccf3a43c9e162fc6fef2651da01103a02bca98d38462fe6395b9b4e6dc96a64`  
		Last Modified: Tue, 25 Feb 2025 22:15:39 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5067f57e0d418f66b609217b8ba7caa018ccab3ac38922d7c4797451579b7468`  
		Last Modified: Tue, 25 Feb 2025 22:15:39 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:66af7d583747898efea9f67c3ff93f8aa993f068528a5aaf50e18a5ffaae2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f226705d21a1826de8bd2c6ee20c35e3966881d96443741ee0b7ff81e103e4`

```dockerfile
```

-	Layers:
	-	`sha256:2db5025980dad4fcac824b97547a716063d145967c77ec341d5394357d3c0e90`  
		Last Modified: Tue, 25 Feb 2025 22:15:40 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:d86599f6811aae07be1c0b2b2955d47bb3df8dcf86c1d9fcdc080746829bfe9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:ab30601c4ae2e5de749e7e013dbf1bc8c5f948795d9ba14dfda2cc484f87b552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5923576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736726958d6b2f0e21680f7a56521500766540e90084a54a726a2672e345e95f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ea1d4d1eef4999bdc608bafb79b4807c2e0d126548d7f7d6e3a9b542c153bab`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.9 MB (5923068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8394405f954a1600ce69d033d4616992e140b23520ef911b5e8cb3c9fe0a0bab`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f6eb9f0ff1ba7f1080413295e1bd058a3eb8eaa6346a04ce30d9b12633f178a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5fc4acfc4fca3421337954440d9551afa9681b105c24998d64a27f4f385456`

```dockerfile
```

-	Layers:
	-	`sha256:41f7e4d13b7d0cafe62fb08f772bde421af4e46d7c80aa8051eada0b71e2d6ad`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:a37f3705ca4f359f2cd688f2f2915c89396f3242ed0017031b1d1ac86b929f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5587283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa848ded2e7f822233d14d085a59458f091b55a5caad5800e30d9759389aeac0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7931d39fd2726f7116d27b851850cf4a1ff6e69fd3de1ed621bfe728eaf4c32`  
		Last Modified: Tue, 25 Feb 2025 19:16:31 GMT  
		Size: 5.6 MB (5586774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526621f9915e8bc26b6f41cb0b4ec86f849a2f797e44f1891bc4ec17549827f4`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:2fc0d021712bbbf87403b2efb33aa02fd447167450cd57cbd42e75ddc5fd29ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6710a8bb2aed7e8414816e8dedcb63a21a481320f77bf39efdf73bc7bb11668e`

```dockerfile
```

-	Layers:
	-	`sha256:92236e3a37db849c42f54749091d19b6ef1c03b5d1c5d1bf501fe9ed7360131e`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:da5d81783ddfc4e6e5ea9c7e9627dbae2052e148b0ca4c3a5adf3e8cdf5881a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5577156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c3470f5d2f8c4e3cdafea8433db44a91110f01e60967c2a3a8d978e31baaed`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0cf7641a4057a532da4f664f9cec79f7fe56c198bb9e71bcbc2c19bb907c58d5`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.6 MB (5576646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3463297bf29a5bbf37928948bb32bb57b1741d42493f2ae75ed53175a517af`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8be21b20d1b6e3d2e901bce12f29bafce42afbbb1b762be62bfc195cb7e9b3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3610a7ae663a5ca8c8be4540df39767d306086365de3263700ddcce895420387`

```dockerfile
```

-	Layers:
	-	`sha256:234087f90831097305eb3b9065da97b803a126593235b546269cfbfa625f608c`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1ab5a26d1f1b792832dd7d52e60d8f57fdcb0ae690e943d796b2b3dea26599c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5471384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96361ef0a1d425f77a7d5bf22cccb8ab926a283d25551390017dcc936f8d6ddd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:34a7e29168d12cc49e3fd1454925bc4b2f10137b37fb10cc85f3b76f5e2959b9`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.5 MB (5470876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0851ead742e7b3af0d74476f1e7610234b00ab6bde066faf665277f50cd3c4c`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4424673c4c02b57552cb838402189f34638ab966b9f85359bad2c59ee9ece0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68e730f04dffe04ac9fcc8af9491ae6be3a7b9be23078e4acc7d0f36fb24ca`

```dockerfile
```

-	Layers:
	-	`sha256:2f7c0d301103a7e55953e57ee1a1660e241006b0b659cffea67752432c2b5ab2`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:1bb4f59414ad9587da0bb4e32ff196ef02914c7e8225b5f3c1a3b79e521de195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5434760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ad4a1f1ab680fc057eaaf6c15371c9fda97d7ac3fa04092cefc46564cceb59`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3821b02a9a90c20826ffaffe25f12d7283677acc84047703af05ac61729fd3da`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.4 MB (5434252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a956e9b697668bf98cbe2a5ec65f9e9c0368945ed81d9e43faa5d064cf6cad4`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:e7bf236217d62b740ceeef3cf7150a2b66bf5c247d8d6ffbd991288ec58f799e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe4ef235be79096172af5671be15debaba38653149f5fe74fb76d2c59390183`

```dockerfile
```

-	Layers:
	-	`sha256:baa43bb7d01b88047f62ca6dc61952a118a1bc2c2a3222dbd65a322a26523d7d`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:84fbc6a0d4f3a6242710d3ea5b8ab4578403aa53d8a5302026bdd6ff20ced27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5777700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcaaa0f666e7b95fe6b20c8bbd70eadf8213e2790de894c72c9f7aa30939f4f0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46891594ec8b4d3680a1bbfe2877deba49c42d5db2b71635cc53e7a260da8759`  
		Last Modified: Tue, 25 Feb 2025 19:16:32 GMT  
		Size: 5.8 MB (5777190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642410c76d1bbecfc24938ff297ac86ca1a30d14e8ab6ef3e9beb0decbbb955`  
		Last Modified: Tue, 25 Feb 2025 23:28:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:192747a24178676ee22ac82db357523716ac68b38738fc729a9044432e7b8815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2f83f8a72ce10467cc585601118bc7a449b8d32a56af2df1c019124dfe4ecf`

```dockerfile
```

-	Layers:
	-	`sha256:841b5965931663c1f16aaccf610709337098323a7168962634fe4bed2d16175f`  
		Last Modified: Tue, 25 Feb 2025 23:28:06 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:e37f384db2351a1bb09c1e1640b7571e012bece8e5579c2660ec07bf788b53ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:6a4cc4d864f9bac7dc07b623679bf121113d41d21fc9b5e640e3c92fca1e5111
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112965803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0766c346c8b6c207312a07351709a6e4da8cd036fbaaa8c380d71c1d32ae393`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Tue, 25 Feb 2025 22:17:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:1eb0b36109ac529ab5d5db4ea880cfd63ed514d1f542c8bd20a200d73207ed8e in C:\nats-server.exe 
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 25 Feb 2025 22:17:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464c91c36773a1621c7277522f95c645dc9866e58b0867242b34277fc4145ada`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0903b195c823336fbd58a8a52901057cbde5d4f8e8a3fe8d643f7f0b1008ee5`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 6.0 MB (6044491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a624018395b9843449197873a8dfbfcd7cc07efd09eb9f5cb1fe8b5638255438`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbf5f27ca2dfe7fd5ede70769269354cf7852fe304a1af5d4b7bd17e201a74`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0a43a1bf148b020d83f3b26345be5a7f7cdc277350321ce4ad5a4e0fc73662`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3091f851d62e9660edca35a087ab74e6ce5c1ab16cd2dcc10c87c3b1e04be8`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:e37f384db2351a1bb09c1e1640b7571e012bece8e5579c2660ec07bf788b53ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:6a4cc4d864f9bac7dc07b623679bf121113d41d21fc9b5e640e3c92fca1e5111
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112965803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0766c346c8b6c207312a07351709a6e4da8cd036fbaaa8c380d71c1d32ae393`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Tue, 25 Feb 2025 22:17:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:1eb0b36109ac529ab5d5db4ea880cfd63ed514d1f542c8bd20a200d73207ed8e in C:\nats-server.exe 
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 25 Feb 2025 22:17:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464c91c36773a1621c7277522f95c645dc9866e58b0867242b34277fc4145ada`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0903b195c823336fbd58a8a52901057cbde5d4f8e8a3fe8d643f7f0b1008ee5`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 6.0 MB (6044491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a624018395b9843449197873a8dfbfcd7cc07efd09eb9f5cb1fe8b5638255438`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbf5f27ca2dfe7fd5ede70769269354cf7852fe304a1af5d4b7bd17e201a74`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0a43a1bf148b020d83f3b26345be5a7f7cdc277350321ce4ad5a4e0fc73662`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3091f851d62e9660edca35a087ab74e6ce5c1ab16cd2dcc10c87c3b1e04be8`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:d86599f6811aae07be1c0b2b2955d47bb3df8dcf86c1d9fcdc080746829bfe9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:ab30601c4ae2e5de749e7e013dbf1bc8c5f948795d9ba14dfda2cc484f87b552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5923576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736726958d6b2f0e21680f7a56521500766540e90084a54a726a2672e345e95f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ea1d4d1eef4999bdc608bafb79b4807c2e0d126548d7f7d6e3a9b542c153bab`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.9 MB (5923068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8394405f954a1600ce69d033d4616992e140b23520ef911b5e8cb3c9fe0a0bab`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f6eb9f0ff1ba7f1080413295e1bd058a3eb8eaa6346a04ce30d9b12633f178a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5fc4acfc4fca3421337954440d9551afa9681b105c24998d64a27f4f385456`

```dockerfile
```

-	Layers:
	-	`sha256:41f7e4d13b7d0cafe62fb08f772bde421af4e46d7c80aa8051eada0b71e2d6ad`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:a37f3705ca4f359f2cd688f2f2915c89396f3242ed0017031b1d1ac86b929f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5587283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa848ded2e7f822233d14d085a59458f091b55a5caad5800e30d9759389aeac0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7931d39fd2726f7116d27b851850cf4a1ff6e69fd3de1ed621bfe728eaf4c32`  
		Last Modified: Tue, 25 Feb 2025 19:16:31 GMT  
		Size: 5.6 MB (5586774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526621f9915e8bc26b6f41cb0b4ec86f849a2f797e44f1891bc4ec17549827f4`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2fc0d021712bbbf87403b2efb33aa02fd447167450cd57cbd42e75ddc5fd29ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6710a8bb2aed7e8414816e8dedcb63a21a481320f77bf39efdf73bc7bb11668e`

```dockerfile
```

-	Layers:
	-	`sha256:92236e3a37db849c42f54749091d19b6ef1c03b5d1c5d1bf501fe9ed7360131e`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:da5d81783ddfc4e6e5ea9c7e9627dbae2052e148b0ca4c3a5adf3e8cdf5881a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5577156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c3470f5d2f8c4e3cdafea8433db44a91110f01e60967c2a3a8d978e31baaed`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0cf7641a4057a532da4f664f9cec79f7fe56c198bb9e71bcbc2c19bb907c58d5`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.6 MB (5576646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3463297bf29a5bbf37928948bb32bb57b1741d42493f2ae75ed53175a517af`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8be21b20d1b6e3d2e901bce12f29bafce42afbbb1b762be62bfc195cb7e9b3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3610a7ae663a5ca8c8be4540df39767d306086365de3263700ddcce895420387`

```dockerfile
```

-	Layers:
	-	`sha256:234087f90831097305eb3b9065da97b803a126593235b546269cfbfa625f608c`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1ab5a26d1f1b792832dd7d52e60d8f57fdcb0ae690e943d796b2b3dea26599c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5471384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96361ef0a1d425f77a7d5bf22cccb8ab926a283d25551390017dcc936f8d6ddd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:34a7e29168d12cc49e3fd1454925bc4b2f10137b37fb10cc85f3b76f5e2959b9`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.5 MB (5470876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0851ead742e7b3af0d74476f1e7610234b00ab6bde066faf665277f50cd3c4c`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4424673c4c02b57552cb838402189f34638ab966b9f85359bad2c59ee9ece0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68e730f04dffe04ac9fcc8af9491ae6be3a7b9be23078e4acc7d0f36fb24ca`

```dockerfile
```

-	Layers:
	-	`sha256:2f7c0d301103a7e55953e57ee1a1660e241006b0b659cffea67752432c2b5ab2`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:1bb4f59414ad9587da0bb4e32ff196ef02914c7e8225b5f3c1a3b79e521de195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5434760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ad4a1f1ab680fc057eaaf6c15371c9fda97d7ac3fa04092cefc46564cceb59`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3821b02a9a90c20826ffaffe25f12d7283677acc84047703af05ac61729fd3da`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.4 MB (5434252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a956e9b697668bf98cbe2a5ec65f9e9c0368945ed81d9e43faa5d064cf6cad4`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e7bf236217d62b740ceeef3cf7150a2b66bf5c247d8d6ffbd991288ec58f799e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe4ef235be79096172af5671be15debaba38653149f5fe74fb76d2c59390183`

```dockerfile
```

-	Layers:
	-	`sha256:baa43bb7d01b88047f62ca6dc61952a118a1bc2c2a3222dbd65a322a26523d7d`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:84fbc6a0d4f3a6242710d3ea5b8ab4578403aa53d8a5302026bdd6ff20ced27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5777700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcaaa0f666e7b95fe6b20c8bbd70eadf8213e2790de894c72c9f7aa30939f4f0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46891594ec8b4d3680a1bbfe2877deba49c42d5db2b71635cc53e7a260da8759`  
		Last Modified: Tue, 25 Feb 2025 19:16:32 GMT  
		Size: 5.8 MB (5777190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642410c76d1bbecfc24938ff297ac86ca1a30d14e8ab6ef3e9beb0decbbb955`  
		Last Modified: Tue, 25 Feb 2025 23:28:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:192747a24178676ee22ac82db357523716ac68b38738fc729a9044432e7b8815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2f83f8a72ce10467cc585601118bc7a449b8d32a56af2df1c019124dfe4ecf`

```dockerfile
```

-	Layers:
	-	`sha256:841b5965931663c1f16aaccf610709337098323a7168962634fe4bed2d16175f`  
		Last Modified: Tue, 25 Feb 2025 23:28:06 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:68de8391f116e75689a8894608af44359d970ed0f73f652cc4f64667a5974762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:f9baf586a7d5a24f77abdc3e1893d5742cbb2a8727aec3f00c4d2c65084ecfbf
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2143633528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4da431eb1469f157d1feecdb9b465288b0a748b57532bb21fca3548c57614c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 25 Feb 2025 21:36:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 25 Feb 2025 21:36:36 GMT
ENV NATS_DOCKERIZED=1
# Tue, 25 Feb 2025 21:36:37 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 21:36:37 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.26/nats-server-v2.10.26-windows-amd64.zip
# Tue, 25 Feb 2025 21:36:38 GMT
ENV NATS_SERVER_SHASUM=e1f9c4eee642bd521878dc493de8514b25c1468e3f2420312aa52f96f7bcbabf
# Tue, 25 Feb 2025 21:37:18 GMT
RUN Set-PSDebug -Trace 2
# Tue, 25 Feb 2025 21:37:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 25 Feb 2025 21:37:36 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 25 Feb 2025 21:37:36 GMT
EXPOSE 4222 6222 8222
# Tue, 25 Feb 2025 21:37:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 25 Feb 2025 21:37:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2962c26ced92b9e3c7f5d7aebd4559298828b0ae76a0527bf5464eb8c93c00`  
		Last Modified: Tue, 25 Feb 2025 21:37:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32fccbfd6adf85f404d7d84d70587914a6f99fa5e496abee390614035e0c64`  
		Last Modified: Tue, 25 Feb 2025 21:37:42 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990ef8a50ae119e863c3a1547280197e5983c7b6ddb20783b3dd54628b42f904`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afc88e2f571205bcf887d86513344166fa69e24de8659740f8ad26cd9154a06`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73a99f6d11801b46659a585416d0f1f7fca41472d4acbb2d75b754d570f102d`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14def5a308e7ba00beab57e8d0a555e41835d6a7e1fbe73f8cd629e61bbc8412`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 326.1 KB (326129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a913fc4a516e6de7ee8ad909be1db22fc51317f9f677a7b0ec983264959dacc`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 6.4 MB (6386222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4701a610edc58e425cad5c3761df38b0f91e54ade7cffbc439cd6a221370ad`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1170eed527f5197ddf382cc34947fc054416200276965d19eb7f138c222ac3a8`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5f193df96420bf97804f7057740950b173da86fd7c1f79a5f50160154ce512`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db71a5d16206f50e02aa99cc42ce61d770468b7173c5b885ee1d5516f74682d`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:68de8391f116e75689a8894608af44359d970ed0f73f652cc4f64667a5974762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:f9baf586a7d5a24f77abdc3e1893d5742cbb2a8727aec3f00c4d2c65084ecfbf
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2143633528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4da431eb1469f157d1feecdb9b465288b0a748b57532bb21fca3548c57614c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 25 Feb 2025 21:36:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 25 Feb 2025 21:36:36 GMT
ENV NATS_DOCKERIZED=1
# Tue, 25 Feb 2025 21:36:37 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 21:36:37 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.26/nats-server-v2.10.26-windows-amd64.zip
# Tue, 25 Feb 2025 21:36:38 GMT
ENV NATS_SERVER_SHASUM=e1f9c4eee642bd521878dc493de8514b25c1468e3f2420312aa52f96f7bcbabf
# Tue, 25 Feb 2025 21:37:18 GMT
RUN Set-PSDebug -Trace 2
# Tue, 25 Feb 2025 21:37:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 25 Feb 2025 21:37:36 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 25 Feb 2025 21:37:36 GMT
EXPOSE 4222 6222 8222
# Tue, 25 Feb 2025 21:37:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 25 Feb 2025 21:37:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2962c26ced92b9e3c7f5d7aebd4559298828b0ae76a0527bf5464eb8c93c00`  
		Last Modified: Tue, 25 Feb 2025 21:37:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32fccbfd6adf85f404d7d84d70587914a6f99fa5e496abee390614035e0c64`  
		Last Modified: Tue, 25 Feb 2025 21:37:42 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990ef8a50ae119e863c3a1547280197e5983c7b6ddb20783b3dd54628b42f904`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afc88e2f571205bcf887d86513344166fa69e24de8659740f8ad26cd9154a06`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73a99f6d11801b46659a585416d0f1f7fca41472d4acbb2d75b754d570f102d`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14def5a308e7ba00beab57e8d0a555e41835d6a7e1fbe73f8cd629e61bbc8412`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 326.1 KB (326129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a913fc4a516e6de7ee8ad909be1db22fc51317f9f677a7b0ec983264959dacc`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 6.4 MB (6386222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4701a610edc58e425cad5c3761df38b0f91e54ade7cffbc439cd6a221370ad`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1170eed527f5197ddf382cc34947fc054416200276965d19eb7f138c222ac3a8`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5f193df96420bf97804f7057740950b173da86fd7c1f79a5f50160154ce512`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db71a5d16206f50e02aa99cc42ce61d770468b7173c5b885ee1d5516f74682d`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:b715753bac33754e4ed5c71b7445cc25d6b881fb22d022989ef2844196ce1c2e
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
	-	windows version 10.0.17763.6893; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:ab30601c4ae2e5de749e7e013dbf1bc8c5f948795d9ba14dfda2cc484f87b552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5923576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736726958d6b2f0e21680f7a56521500766540e90084a54a726a2672e345e95f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ea1d4d1eef4999bdc608bafb79b4807c2e0d126548d7f7d6e3a9b542c153bab`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.9 MB (5923068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8394405f954a1600ce69d033d4616992e140b23520ef911b5e8cb3c9fe0a0bab`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:f6eb9f0ff1ba7f1080413295e1bd058a3eb8eaa6346a04ce30d9b12633f178a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5fc4acfc4fca3421337954440d9551afa9681b105c24998d64a27f4f385456`

```dockerfile
```

-	Layers:
	-	`sha256:41f7e4d13b7d0cafe62fb08f772bde421af4e46d7c80aa8051eada0b71e2d6ad`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:a37f3705ca4f359f2cd688f2f2915c89396f3242ed0017031b1d1ac86b929f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5587283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa848ded2e7f822233d14d085a59458f091b55a5caad5800e30d9759389aeac0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7931d39fd2726f7116d27b851850cf4a1ff6e69fd3de1ed621bfe728eaf4c32`  
		Last Modified: Tue, 25 Feb 2025 19:16:31 GMT  
		Size: 5.6 MB (5586774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526621f9915e8bc26b6f41cb0b4ec86f849a2f797e44f1891bc4ec17549827f4`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:2fc0d021712bbbf87403b2efb33aa02fd447167450cd57cbd42e75ddc5fd29ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6710a8bb2aed7e8414816e8dedcb63a21a481320f77bf39efdf73bc7bb11668e`

```dockerfile
```

-	Layers:
	-	`sha256:92236e3a37db849c42f54749091d19b6ef1c03b5d1c5d1bf501fe9ed7360131e`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:da5d81783ddfc4e6e5ea9c7e9627dbae2052e148b0ca4c3a5adf3e8cdf5881a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5577156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c3470f5d2f8c4e3cdafea8433db44a91110f01e60967c2a3a8d978e31baaed`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0cf7641a4057a532da4f664f9cec79f7fe56c198bb9e71bcbc2c19bb907c58d5`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.6 MB (5576646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3463297bf29a5bbf37928948bb32bb57b1741d42493f2ae75ed53175a517af`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:8be21b20d1b6e3d2e901bce12f29bafce42afbbb1b762be62bfc195cb7e9b3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3610a7ae663a5ca8c8be4540df39767d306086365de3263700ddcce895420387`

```dockerfile
```

-	Layers:
	-	`sha256:234087f90831097305eb3b9065da97b803a126593235b546269cfbfa625f608c`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1ab5a26d1f1b792832dd7d52e60d8f57fdcb0ae690e943d796b2b3dea26599c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5471384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96361ef0a1d425f77a7d5bf22cccb8ab926a283d25551390017dcc936f8d6ddd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:34a7e29168d12cc49e3fd1454925bc4b2f10137b37fb10cc85f3b76f5e2959b9`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.5 MB (5470876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0851ead742e7b3af0d74476f1e7610234b00ab6bde066faf665277f50cd3c4c`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:4424673c4c02b57552cb838402189f34638ab966b9f85359bad2c59ee9ece0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68e730f04dffe04ac9fcc8af9491ae6be3a7b9be23078e4acc7d0f36fb24ca`

```dockerfile
```

-	Layers:
	-	`sha256:2f7c0d301103a7e55953e57ee1a1660e241006b0b659cffea67752432c2b5ab2`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:1bb4f59414ad9587da0bb4e32ff196ef02914c7e8225b5f3c1a3b79e521de195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5434760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ad4a1f1ab680fc057eaaf6c15371c9fda97d7ac3fa04092cefc46564cceb59`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3821b02a9a90c20826ffaffe25f12d7283677acc84047703af05ac61729fd3da`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.4 MB (5434252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a956e9b697668bf98cbe2a5ec65f9e9c0368945ed81d9e43faa5d064cf6cad4`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:e7bf236217d62b740ceeef3cf7150a2b66bf5c247d8d6ffbd991288ec58f799e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe4ef235be79096172af5671be15debaba38653149f5fe74fb76d2c59390183`

```dockerfile
```

-	Layers:
	-	`sha256:baa43bb7d01b88047f62ca6dc61952a118a1bc2c2a3222dbd65a322a26523d7d`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:84fbc6a0d4f3a6242710d3ea5b8ab4578403aa53d8a5302026bdd6ff20ced27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5777700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcaaa0f666e7b95fe6b20c8bbd70eadf8213e2790de894c72c9f7aa30939f4f0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46891594ec8b4d3680a1bbfe2877deba49c42d5db2b71635cc53e7a260da8759`  
		Last Modified: Tue, 25 Feb 2025 19:16:32 GMT  
		Size: 5.8 MB (5777190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642410c76d1bbecfc24938ff297ac86ca1a30d14e8ab6ef3e9beb0decbbb955`  
		Last Modified: Tue, 25 Feb 2025 23:28:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:192747a24178676ee22ac82db357523716ac68b38738fc729a9044432e7b8815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2f83f8a72ce10467cc585601118bc7a449b8d32a56af2df1c019124dfe4ecf`

```dockerfile
```

-	Layers:
	-	`sha256:841b5965931663c1f16aaccf610709337098323a7168962634fe4bed2d16175f`  
		Last Modified: Tue, 25 Feb 2025 23:28:06 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:6a4cc4d864f9bac7dc07b623679bf121113d41d21fc9b5e640e3c92fca1e5111
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112965803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0766c346c8b6c207312a07351709a6e4da8cd036fbaaa8c380d71c1d32ae393`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Tue, 25 Feb 2025 22:17:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:1eb0b36109ac529ab5d5db4ea880cfd63ed514d1f542c8bd20a200d73207ed8e in C:\nats-server.exe 
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 25 Feb 2025 22:17:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464c91c36773a1621c7277522f95c645dc9866e58b0867242b34277fc4145ada`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0903b195c823336fbd58a8a52901057cbde5d4f8e8a3fe8d643f7f0b1008ee5`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 6.0 MB (6044491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a624018395b9843449197873a8dfbfcd7cc07efd09eb9f5cb1fe8b5638255438`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbf5f27ca2dfe7fd5ede70769269354cf7852fe304a1af5d4b7bd17e201a74`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0a43a1bf148b020d83f3b26345be5a7f7cdc277350321ce4ad5a4e0fc73662`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3091f851d62e9660edca35a087ab74e6ce5c1ab16cd2dcc10c87c3b1e04be8`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:d69eb29526c1d98afdfb2e2434763bef77b5f3c83e2e24769c13a4d104be475e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:6e0cca2c6da79f0a3542ec5a3319dd10b1b05f5d8e8949afa8e9cdf6314bbf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10026010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e556ce07f949f5717c6dc8daabda0e17ded6419df74f43518c1f56c1e329c22b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1935954c94119c3706036d5d692853435b83d99c259f8ec51495e3e2efb18a6a`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 6.4 MB (6382794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06613330ae8540f47d41506b7d56df4c5bc71440bf813153c79399e3f5da3c5`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19394475462d5b1aea3c36ff72f30a11aeeb4f440112ebbb15b8a456f653ac55`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:58a608a3d90a3e203ff98c7e1e6bb1d98dcb587196fad9b5046c6a18e27c30e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0ae8cc81e579896c7a782ec0a7819a1abc513aac53c0053d0d8c8707a6100a`

```dockerfile
```

-	Layers:
	-	`sha256:55c1b3c18c84cf1aadd36f17ae37f6e463386696329d2f7845b2b7c772969160`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:888b3676fa9b74db3d6bc52a06a90ec37388f17f7a6c94fba1b0aab761c8d1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9412308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdbc5759068b8c3c7c0d9717f2fa31a8802843622ffa5bc1ee90ab2f97cc836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950d5a437e93fb02cf36f9a20e870f94dd8ac2842175b525de18d73671af6aa`  
		Last Modified: Tue, 25 Feb 2025 21:26:33 GMT  
		Size: 6.0 MB (6046604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d39378960e3fb615203a449ee86a6adc427a58bb348af84af623f9137eddb11`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1ce7e529762c20edc862cef19f51119c18e640a72162538b361811aac9cf6d`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d2f4a4f725f456222c0e0a232f481981a98db2a040b8e5e03a46ba5d19de93b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e467740581e449ded36748d517fc3d41e73c080a765637ab847143ff92b4c0c7`

```dockerfile
```

-	Layers:
	-	`sha256:64782c75142fcb4da7de03639949321d926dd843f9e85121ff5cc18d20715dac`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a1745de189516c48458486fde6b403abc48727f7e2dad55b951a85a77761e2bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9134853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e833dd9f4430c77bf7a6f708e9e6e002d936da7c311595bcdbb9d5979d2b8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2e5935cbee970cdf8caa27a6dafa7c7e944ca51b4d5b9a1c3b93ff3053eb4f`  
		Last Modified: Wed, 26 Feb 2025 02:51:22 GMT  
		Size: 6.0 MB (6035762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb14c94ff9b267a96d276f33d9182a887b066ea83d612971ecc3f07a5357233`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba509bbe23f7c8d23d12b140bf072518aebbb51dac6ac1a53d7dc7c21356dc`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4feb4a911e61e83936b9beb43d347f961ca2560f45191694f78f33d59d58755b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00883483bdc919a66a85b4f2f8521a2ebd1646c8f932d3437be0e289d01313a`

```dockerfile
```

-	Layers:
	-	`sha256:f5175fcbe6f613a2932126ce4d0da80ad1ab95ea38ae164d75b44f9eb774893e`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f9fb7d4a001bdeaf8efe662379474e453f8e63844b5c0913680367fe3124295a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9926441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6700a7a44644d35a74467c9dcbbe2492e70d661075b7755d96a3cbae0229ff7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8405433bc52db97fac8fbd2bd06458903c03f86a2d80d9d5de11d642868850f3`  
		Last Modified: Tue, 25 Feb 2025 23:33:53 GMT  
		Size: 5.9 MB (5932443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704f25bcef9e2d1d2333773f3c5b74abb44de6b6acf941f327d8672bd7ffe138`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5be759409abd41f18a0ac584e5d7d5a24910f005e7c64a45f84ebaf540f34c1`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b07c213de9995bce905bae01e3d3c91262c6ced69feb9739a94cc6e70b6c4941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98276d55b0f5cba673066fca22f6cae9b01c363da2f4f6a99dd3c9295bd32e82`

```dockerfile
```

-	Layers:
	-	`sha256:1b55454322f3ee2db01f280284055234c7a64d43c52c7cc0da084c9ccf4474fd`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:1e5c65a5b378164fbc055112722da9af33284202befb128e9716dfc8d8f998b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9472260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f9943fe40a1d887d0477acbedc42a3822bb2ae7f9ae3f8a2f3bc988aae0c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ad6d76a28889f354cf5c7376c4cd2238dc37a73bae19f1e12a713f6e666bf2`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 5.9 MB (5896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca8c83039c331226a414edca0991c08f1d9f07cdfab82595fbee7aed442ef69`  
		Last Modified: Tue, 25 Feb 2025 21:28:54 GMT  
		Size: 563.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad2d41ba212a6f1ff2dbe03563c50fd26cb7d51e46c4d08af2f4097c759e5c0`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cbfb602ab0fd542d76b033b69f65563107aadb7811c6215a22d44c215bfb9219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6596c1301cd69cdc9984c62cdabbd98209cacedd5cc4c6744c3badaf073080fd`

```dockerfile
```

-	Layers:
	-	`sha256:c5d5cfc84a3213cec6cbc7a0bff5c8f50266b3ffc1f0164f61a05ae22293b11e`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:3b8989b0fec1ee207ccdf0f52aa99b9ddd8d3902c1203c501e2d8272949de8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9707272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814240ee91751bb8caa1b427d6fe215c399953d2a8c1da768008d647eedba145`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a056f2f8e8ae073c4ef4c378c426dbf016cc4044eb5010d4c82049d61b8a47`  
		Last Modified: Tue, 25 Feb 2025 22:15:40 GMT  
		Size: 6.2 MB (6238736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccf3a43c9e162fc6fef2651da01103a02bca98d38462fe6395b9b4e6dc96a64`  
		Last Modified: Tue, 25 Feb 2025 22:15:39 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5067f57e0d418f66b609217b8ba7caa018ccab3ac38922d7c4797451579b7468`  
		Last Modified: Tue, 25 Feb 2025 22:15:39 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:66af7d583747898efea9f67c3ff93f8aa993f068528a5aaf50e18a5ffaae2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f226705d21a1826de8bd2c6ee20c35e3966881d96443741ee0b7ff81e103e4`

```dockerfile
```

-	Layers:
	-	`sha256:2db5025980dad4fcac824b97547a716063d145967c77ec341d5394357d3c0e90`  
		Last Modified: Tue, 25 Feb 2025 22:15:40 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-alpine3.21`

```console
$ docker pull nats@sha256:d69eb29526c1d98afdfb2e2434763bef77b5f3c83e2e24769c13a4d104be475e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `nats:2.10-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:6e0cca2c6da79f0a3542ec5a3319dd10b1b05f5d8e8949afa8e9cdf6314bbf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10026010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e556ce07f949f5717c6dc8daabda0e17ded6419df74f43518c1f56c1e329c22b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1935954c94119c3706036d5d692853435b83d99c259f8ec51495e3e2efb18a6a`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 6.4 MB (6382794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06613330ae8540f47d41506b7d56df4c5bc71440bf813153c79399e3f5da3c5`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19394475462d5b1aea3c36ff72f30a11aeeb4f440112ebbb15b8a456f653ac55`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:58a608a3d90a3e203ff98c7e1e6bb1d98dcb587196fad9b5046c6a18e27c30e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0ae8cc81e579896c7a782ec0a7819a1abc513aac53c0053d0d8c8707a6100a`

```dockerfile
```

-	Layers:
	-	`sha256:55c1b3c18c84cf1aadd36f17ae37f6e463386696329d2f7845b2b7c772969160`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:888b3676fa9b74db3d6bc52a06a90ec37388f17f7a6c94fba1b0aab761c8d1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9412308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdbc5759068b8c3c7c0d9717f2fa31a8802843622ffa5bc1ee90ab2f97cc836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950d5a437e93fb02cf36f9a20e870f94dd8ac2842175b525de18d73671af6aa`  
		Last Modified: Tue, 25 Feb 2025 21:26:33 GMT  
		Size: 6.0 MB (6046604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d39378960e3fb615203a449ee86a6adc427a58bb348af84af623f9137eddb11`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1ce7e529762c20edc862cef19f51119c18e640a72162538b361811aac9cf6d`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:d2f4a4f725f456222c0e0a232f481981a98db2a040b8e5e03a46ba5d19de93b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e467740581e449ded36748d517fc3d41e73c080a765637ab847143ff92b4c0c7`

```dockerfile
```

-	Layers:
	-	`sha256:64782c75142fcb4da7de03639949321d926dd843f9e85121ff5cc18d20715dac`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:a1745de189516c48458486fde6b403abc48727f7e2dad55b951a85a77761e2bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9134853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e833dd9f4430c77bf7a6f708e9e6e002d936da7c311595bcdbb9d5979d2b8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2e5935cbee970cdf8caa27a6dafa7c7e944ca51b4d5b9a1c3b93ff3053eb4f`  
		Last Modified: Wed, 26 Feb 2025 02:51:22 GMT  
		Size: 6.0 MB (6035762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb14c94ff9b267a96d276f33d9182a887b066ea83d612971ecc3f07a5357233`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba509bbe23f7c8d23d12b140bf072518aebbb51dac6ac1a53d7dc7c21356dc`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:4feb4a911e61e83936b9beb43d347f961ca2560f45191694f78f33d59d58755b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00883483bdc919a66a85b4f2f8521a2ebd1646c8f932d3437be0e289d01313a`

```dockerfile
```

-	Layers:
	-	`sha256:f5175fcbe6f613a2932126ce4d0da80ad1ab95ea38ae164d75b44f9eb774893e`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f9fb7d4a001bdeaf8efe662379474e453f8e63844b5c0913680367fe3124295a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9926441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6700a7a44644d35a74467c9dcbbe2492e70d661075b7755d96a3cbae0229ff7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8405433bc52db97fac8fbd2bd06458903c03f86a2d80d9d5de11d642868850f3`  
		Last Modified: Tue, 25 Feb 2025 23:33:53 GMT  
		Size: 5.9 MB (5932443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704f25bcef9e2d1d2333773f3c5b74abb44de6b6acf941f327d8672bd7ffe138`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5be759409abd41f18a0ac584e5d7d5a24910f005e7c64a45f84ebaf540f34c1`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:b07c213de9995bce905bae01e3d3c91262c6ced69feb9739a94cc6e70b6c4941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98276d55b0f5cba673066fca22f6cae9b01c363da2f4f6a99dd3c9295bd32e82`

```dockerfile
```

-	Layers:
	-	`sha256:1b55454322f3ee2db01f280284055234c7a64d43c52c7cc0da084c9ccf4474fd`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:1e5c65a5b378164fbc055112722da9af33284202befb128e9716dfc8d8f998b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9472260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f9943fe40a1d887d0477acbedc42a3822bb2ae7f9ae3f8a2f3bc988aae0c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ad6d76a28889f354cf5c7376c4cd2238dc37a73bae19f1e12a713f6e666bf2`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 5.9 MB (5896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca8c83039c331226a414edca0991c08f1d9f07cdfab82595fbee7aed442ef69`  
		Last Modified: Tue, 25 Feb 2025 21:28:54 GMT  
		Size: 563.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad2d41ba212a6f1ff2dbe03563c50fd26cb7d51e46c4d08af2f4097c759e5c0`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cbfb602ab0fd542d76b033b69f65563107aadb7811c6215a22d44c215bfb9219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6596c1301cd69cdc9984c62cdabbd98209cacedd5cc4c6744c3badaf073080fd`

```dockerfile
```

-	Layers:
	-	`sha256:c5d5cfc84a3213cec6cbc7a0bff5c8f50266b3ffc1f0164f61a05ae22293b11e`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:3b8989b0fec1ee207ccdf0f52aa99b9ddd8d3902c1203c501e2d8272949de8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9707272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814240ee91751bb8caa1b427d6fe215c399953d2a8c1da768008d647eedba145`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a056f2f8e8ae073c4ef4c378c426dbf016cc4044eb5010d4c82049d61b8a47`  
		Last Modified: Tue, 25 Feb 2025 22:15:40 GMT  
		Size: 6.2 MB (6238736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccf3a43c9e162fc6fef2651da01103a02bca98d38462fe6395b9b4e6dc96a64`  
		Last Modified: Tue, 25 Feb 2025 22:15:39 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5067f57e0d418f66b609217b8ba7caa018ccab3ac38922d7c4797451579b7468`  
		Last Modified: Tue, 25 Feb 2025 22:15:39 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:66af7d583747898efea9f67c3ff93f8aa993f068528a5aaf50e18a5ffaae2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f226705d21a1826de8bd2c6ee20c35e3966881d96443741ee0b7ff81e103e4`

```dockerfile
```

-	Layers:
	-	`sha256:2db5025980dad4fcac824b97547a716063d145967c77ec341d5394357d3c0e90`  
		Last Modified: Tue, 25 Feb 2025 22:15:40 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:d86599f6811aae07be1c0b2b2955d47bb3df8dcf86c1d9fcdc080746829bfe9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:ab30601c4ae2e5de749e7e013dbf1bc8c5f948795d9ba14dfda2cc484f87b552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5923576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736726958d6b2f0e21680f7a56521500766540e90084a54a726a2672e345e95f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ea1d4d1eef4999bdc608bafb79b4807c2e0d126548d7f7d6e3a9b542c153bab`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.9 MB (5923068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8394405f954a1600ce69d033d4616992e140b23520ef911b5e8cb3c9fe0a0bab`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f6eb9f0ff1ba7f1080413295e1bd058a3eb8eaa6346a04ce30d9b12633f178a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5fc4acfc4fca3421337954440d9551afa9681b105c24998d64a27f4f385456`

```dockerfile
```

-	Layers:
	-	`sha256:41f7e4d13b7d0cafe62fb08f772bde421af4e46d7c80aa8051eada0b71e2d6ad`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:a37f3705ca4f359f2cd688f2f2915c89396f3242ed0017031b1d1ac86b929f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5587283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa848ded2e7f822233d14d085a59458f091b55a5caad5800e30d9759389aeac0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7931d39fd2726f7116d27b851850cf4a1ff6e69fd3de1ed621bfe728eaf4c32`  
		Last Modified: Tue, 25 Feb 2025 19:16:31 GMT  
		Size: 5.6 MB (5586774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526621f9915e8bc26b6f41cb0b4ec86f849a2f797e44f1891bc4ec17549827f4`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:2fc0d021712bbbf87403b2efb33aa02fd447167450cd57cbd42e75ddc5fd29ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6710a8bb2aed7e8414816e8dedcb63a21a481320f77bf39efdf73bc7bb11668e`

```dockerfile
```

-	Layers:
	-	`sha256:92236e3a37db849c42f54749091d19b6ef1c03b5d1c5d1bf501fe9ed7360131e`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:da5d81783ddfc4e6e5ea9c7e9627dbae2052e148b0ca4c3a5adf3e8cdf5881a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5577156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c3470f5d2f8c4e3cdafea8433db44a91110f01e60967c2a3a8d978e31baaed`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0cf7641a4057a532da4f664f9cec79f7fe56c198bb9e71bcbc2c19bb907c58d5`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.6 MB (5576646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3463297bf29a5bbf37928948bb32bb57b1741d42493f2ae75ed53175a517af`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8be21b20d1b6e3d2e901bce12f29bafce42afbbb1b762be62bfc195cb7e9b3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3610a7ae663a5ca8c8be4540df39767d306086365de3263700ddcce895420387`

```dockerfile
```

-	Layers:
	-	`sha256:234087f90831097305eb3b9065da97b803a126593235b546269cfbfa625f608c`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1ab5a26d1f1b792832dd7d52e60d8f57fdcb0ae690e943d796b2b3dea26599c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5471384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96361ef0a1d425f77a7d5bf22cccb8ab926a283d25551390017dcc936f8d6ddd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:34a7e29168d12cc49e3fd1454925bc4b2f10137b37fb10cc85f3b76f5e2959b9`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.5 MB (5470876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0851ead742e7b3af0d74476f1e7610234b00ab6bde066faf665277f50cd3c4c`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4424673c4c02b57552cb838402189f34638ab966b9f85359bad2c59ee9ece0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68e730f04dffe04ac9fcc8af9491ae6be3a7b9be23078e4acc7d0f36fb24ca`

```dockerfile
```

-	Layers:
	-	`sha256:2f7c0d301103a7e55953e57ee1a1660e241006b0b659cffea67752432c2b5ab2`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:1bb4f59414ad9587da0bb4e32ff196ef02914c7e8225b5f3c1a3b79e521de195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5434760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ad4a1f1ab680fc057eaaf6c15371c9fda97d7ac3fa04092cefc46564cceb59`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3821b02a9a90c20826ffaffe25f12d7283677acc84047703af05ac61729fd3da`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.4 MB (5434252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a956e9b697668bf98cbe2a5ec65f9e9c0368945ed81d9e43faa5d064cf6cad4`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:e7bf236217d62b740ceeef3cf7150a2b66bf5c247d8d6ffbd991288ec58f799e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe4ef235be79096172af5671be15debaba38653149f5fe74fb76d2c59390183`

```dockerfile
```

-	Layers:
	-	`sha256:baa43bb7d01b88047f62ca6dc61952a118a1bc2c2a3222dbd65a322a26523d7d`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:84fbc6a0d4f3a6242710d3ea5b8ab4578403aa53d8a5302026bdd6ff20ced27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5777700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcaaa0f666e7b95fe6b20c8bbd70eadf8213e2790de894c72c9f7aa30939f4f0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46891594ec8b4d3680a1bbfe2877deba49c42d5db2b71635cc53e7a260da8759`  
		Last Modified: Tue, 25 Feb 2025 19:16:32 GMT  
		Size: 5.8 MB (5777190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642410c76d1bbecfc24938ff297ac86ca1a30d14e8ab6ef3e9beb0decbbb955`  
		Last Modified: Tue, 25 Feb 2025 23:28:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:192747a24178676ee22ac82db357523716ac68b38738fc729a9044432e7b8815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2f83f8a72ce10467cc585601118bc7a449b8d32a56af2df1c019124dfe4ecf`

```dockerfile
```

-	Layers:
	-	`sha256:841b5965931663c1f16aaccf610709337098323a7168962634fe4bed2d16175f`  
		Last Modified: Tue, 25 Feb 2025 23:28:06 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:e37f384db2351a1bb09c1e1640b7571e012bece8e5579c2660ec07bf788b53ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:6a4cc4d864f9bac7dc07b623679bf121113d41d21fc9b5e640e3c92fca1e5111
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112965803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0766c346c8b6c207312a07351709a6e4da8cd036fbaaa8c380d71c1d32ae393`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Tue, 25 Feb 2025 22:17:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:1eb0b36109ac529ab5d5db4ea880cfd63ed514d1f542c8bd20a200d73207ed8e in C:\nats-server.exe 
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 25 Feb 2025 22:17:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464c91c36773a1621c7277522f95c645dc9866e58b0867242b34277fc4145ada`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0903b195c823336fbd58a8a52901057cbde5d4f8e8a3fe8d643f7f0b1008ee5`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 6.0 MB (6044491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a624018395b9843449197873a8dfbfcd7cc07efd09eb9f5cb1fe8b5638255438`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbf5f27ca2dfe7fd5ede70769269354cf7852fe304a1af5d4b7bd17e201a74`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0a43a1bf148b020d83f3b26345be5a7f7cdc277350321ce4ad5a4e0fc73662`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3091f851d62e9660edca35a087ab74e6ce5c1ab16cd2dcc10c87c3b1e04be8`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:e37f384db2351a1bb09c1e1640b7571e012bece8e5579c2660ec07bf788b53ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:6a4cc4d864f9bac7dc07b623679bf121113d41d21fc9b5e640e3c92fca1e5111
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112965803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0766c346c8b6c207312a07351709a6e4da8cd036fbaaa8c380d71c1d32ae393`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Tue, 25 Feb 2025 22:17:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:1eb0b36109ac529ab5d5db4ea880cfd63ed514d1f542c8bd20a200d73207ed8e in C:\nats-server.exe 
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 25 Feb 2025 22:17:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464c91c36773a1621c7277522f95c645dc9866e58b0867242b34277fc4145ada`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0903b195c823336fbd58a8a52901057cbde5d4f8e8a3fe8d643f7f0b1008ee5`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 6.0 MB (6044491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a624018395b9843449197873a8dfbfcd7cc07efd09eb9f5cb1fe8b5638255438`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbf5f27ca2dfe7fd5ede70769269354cf7852fe304a1af5d4b7bd17e201a74`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0a43a1bf148b020d83f3b26345be5a7f7cdc277350321ce4ad5a4e0fc73662`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3091f851d62e9660edca35a087ab74e6ce5c1ab16cd2dcc10c87c3b1e04be8`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:d86599f6811aae07be1c0b2b2955d47bb3df8dcf86c1d9fcdc080746829bfe9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:ab30601c4ae2e5de749e7e013dbf1bc8c5f948795d9ba14dfda2cc484f87b552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5923576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736726958d6b2f0e21680f7a56521500766540e90084a54a726a2672e345e95f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ea1d4d1eef4999bdc608bafb79b4807c2e0d126548d7f7d6e3a9b542c153bab`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.9 MB (5923068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8394405f954a1600ce69d033d4616992e140b23520ef911b5e8cb3c9fe0a0bab`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f6eb9f0ff1ba7f1080413295e1bd058a3eb8eaa6346a04ce30d9b12633f178a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5fc4acfc4fca3421337954440d9551afa9681b105c24998d64a27f4f385456`

```dockerfile
```

-	Layers:
	-	`sha256:41f7e4d13b7d0cafe62fb08f772bde421af4e46d7c80aa8051eada0b71e2d6ad`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:a37f3705ca4f359f2cd688f2f2915c89396f3242ed0017031b1d1ac86b929f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5587283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa848ded2e7f822233d14d085a59458f091b55a5caad5800e30d9759389aeac0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7931d39fd2726f7116d27b851850cf4a1ff6e69fd3de1ed621bfe728eaf4c32`  
		Last Modified: Tue, 25 Feb 2025 19:16:31 GMT  
		Size: 5.6 MB (5586774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526621f9915e8bc26b6f41cb0b4ec86f849a2f797e44f1891bc4ec17549827f4`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2fc0d021712bbbf87403b2efb33aa02fd447167450cd57cbd42e75ddc5fd29ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6710a8bb2aed7e8414816e8dedcb63a21a481320f77bf39efdf73bc7bb11668e`

```dockerfile
```

-	Layers:
	-	`sha256:92236e3a37db849c42f54749091d19b6ef1c03b5d1c5d1bf501fe9ed7360131e`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:da5d81783ddfc4e6e5ea9c7e9627dbae2052e148b0ca4c3a5adf3e8cdf5881a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5577156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c3470f5d2f8c4e3cdafea8433db44a91110f01e60967c2a3a8d978e31baaed`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0cf7641a4057a532da4f664f9cec79f7fe56c198bb9e71bcbc2c19bb907c58d5`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.6 MB (5576646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3463297bf29a5bbf37928948bb32bb57b1741d42493f2ae75ed53175a517af`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8be21b20d1b6e3d2e901bce12f29bafce42afbbb1b762be62bfc195cb7e9b3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3610a7ae663a5ca8c8be4540df39767d306086365de3263700ddcce895420387`

```dockerfile
```

-	Layers:
	-	`sha256:234087f90831097305eb3b9065da97b803a126593235b546269cfbfa625f608c`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1ab5a26d1f1b792832dd7d52e60d8f57fdcb0ae690e943d796b2b3dea26599c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5471384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96361ef0a1d425f77a7d5bf22cccb8ab926a283d25551390017dcc936f8d6ddd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:34a7e29168d12cc49e3fd1454925bc4b2f10137b37fb10cc85f3b76f5e2959b9`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.5 MB (5470876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0851ead742e7b3af0d74476f1e7610234b00ab6bde066faf665277f50cd3c4c`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4424673c4c02b57552cb838402189f34638ab966b9f85359bad2c59ee9ece0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68e730f04dffe04ac9fcc8af9491ae6be3a7b9be23078e4acc7d0f36fb24ca`

```dockerfile
```

-	Layers:
	-	`sha256:2f7c0d301103a7e55953e57ee1a1660e241006b0b659cffea67752432c2b5ab2`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:1bb4f59414ad9587da0bb4e32ff196ef02914c7e8225b5f3c1a3b79e521de195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5434760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ad4a1f1ab680fc057eaaf6c15371c9fda97d7ac3fa04092cefc46564cceb59`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3821b02a9a90c20826ffaffe25f12d7283677acc84047703af05ac61729fd3da`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.4 MB (5434252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a956e9b697668bf98cbe2a5ec65f9e9c0368945ed81d9e43faa5d064cf6cad4`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e7bf236217d62b740ceeef3cf7150a2b66bf5c247d8d6ffbd991288ec58f799e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe4ef235be79096172af5671be15debaba38653149f5fe74fb76d2c59390183`

```dockerfile
```

-	Layers:
	-	`sha256:baa43bb7d01b88047f62ca6dc61952a118a1bc2c2a3222dbd65a322a26523d7d`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:84fbc6a0d4f3a6242710d3ea5b8ab4578403aa53d8a5302026bdd6ff20ced27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5777700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcaaa0f666e7b95fe6b20c8bbd70eadf8213e2790de894c72c9f7aa30939f4f0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46891594ec8b4d3680a1bbfe2877deba49c42d5db2b71635cc53e7a260da8759`  
		Last Modified: Tue, 25 Feb 2025 19:16:32 GMT  
		Size: 5.8 MB (5777190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642410c76d1bbecfc24938ff297ac86ca1a30d14e8ab6ef3e9beb0decbbb955`  
		Last Modified: Tue, 25 Feb 2025 23:28:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:192747a24178676ee22ac82db357523716ac68b38738fc729a9044432e7b8815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2f83f8a72ce10467cc585601118bc7a449b8d32a56af2df1c019124dfe4ecf`

```dockerfile
```

-	Layers:
	-	`sha256:841b5965931663c1f16aaccf610709337098323a7168962634fe4bed2d16175f`  
		Last Modified: Tue, 25 Feb 2025 23:28:06 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:68de8391f116e75689a8894608af44359d970ed0f73f652cc4f64667a5974762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:f9baf586a7d5a24f77abdc3e1893d5742cbb2a8727aec3f00c4d2c65084ecfbf
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2143633528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4da431eb1469f157d1feecdb9b465288b0a748b57532bb21fca3548c57614c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 25 Feb 2025 21:36:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 25 Feb 2025 21:36:36 GMT
ENV NATS_DOCKERIZED=1
# Tue, 25 Feb 2025 21:36:37 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 21:36:37 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.26/nats-server-v2.10.26-windows-amd64.zip
# Tue, 25 Feb 2025 21:36:38 GMT
ENV NATS_SERVER_SHASUM=e1f9c4eee642bd521878dc493de8514b25c1468e3f2420312aa52f96f7bcbabf
# Tue, 25 Feb 2025 21:37:18 GMT
RUN Set-PSDebug -Trace 2
# Tue, 25 Feb 2025 21:37:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 25 Feb 2025 21:37:36 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 25 Feb 2025 21:37:36 GMT
EXPOSE 4222 6222 8222
# Tue, 25 Feb 2025 21:37:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 25 Feb 2025 21:37:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2962c26ced92b9e3c7f5d7aebd4559298828b0ae76a0527bf5464eb8c93c00`  
		Last Modified: Tue, 25 Feb 2025 21:37:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32fccbfd6adf85f404d7d84d70587914a6f99fa5e496abee390614035e0c64`  
		Last Modified: Tue, 25 Feb 2025 21:37:42 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990ef8a50ae119e863c3a1547280197e5983c7b6ddb20783b3dd54628b42f904`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afc88e2f571205bcf887d86513344166fa69e24de8659740f8ad26cd9154a06`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73a99f6d11801b46659a585416d0f1f7fca41472d4acbb2d75b754d570f102d`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14def5a308e7ba00beab57e8d0a555e41835d6a7e1fbe73f8cd629e61bbc8412`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 326.1 KB (326129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a913fc4a516e6de7ee8ad909be1db22fc51317f9f677a7b0ec983264959dacc`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 6.4 MB (6386222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4701a610edc58e425cad5c3761df38b0f91e54ade7cffbc439cd6a221370ad`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1170eed527f5197ddf382cc34947fc054416200276965d19eb7f138c222ac3a8`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5f193df96420bf97804f7057740950b173da86fd7c1f79a5f50160154ce512`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db71a5d16206f50e02aa99cc42ce61d770468b7173c5b885ee1d5516f74682d`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:68de8391f116e75689a8894608af44359d970ed0f73f652cc4f64667a5974762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:f9baf586a7d5a24f77abdc3e1893d5742cbb2a8727aec3f00c4d2c65084ecfbf
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2143633528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4da431eb1469f157d1feecdb9b465288b0a748b57532bb21fca3548c57614c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 25 Feb 2025 21:36:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 25 Feb 2025 21:36:36 GMT
ENV NATS_DOCKERIZED=1
# Tue, 25 Feb 2025 21:36:37 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 21:36:37 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.26/nats-server-v2.10.26-windows-amd64.zip
# Tue, 25 Feb 2025 21:36:38 GMT
ENV NATS_SERVER_SHASUM=e1f9c4eee642bd521878dc493de8514b25c1468e3f2420312aa52f96f7bcbabf
# Tue, 25 Feb 2025 21:37:18 GMT
RUN Set-PSDebug -Trace 2
# Tue, 25 Feb 2025 21:37:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 25 Feb 2025 21:37:36 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 25 Feb 2025 21:37:36 GMT
EXPOSE 4222 6222 8222
# Tue, 25 Feb 2025 21:37:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 25 Feb 2025 21:37:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2962c26ced92b9e3c7f5d7aebd4559298828b0ae76a0527bf5464eb8c93c00`  
		Last Modified: Tue, 25 Feb 2025 21:37:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32fccbfd6adf85f404d7d84d70587914a6f99fa5e496abee390614035e0c64`  
		Last Modified: Tue, 25 Feb 2025 21:37:42 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990ef8a50ae119e863c3a1547280197e5983c7b6ddb20783b3dd54628b42f904`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afc88e2f571205bcf887d86513344166fa69e24de8659740f8ad26cd9154a06`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73a99f6d11801b46659a585416d0f1f7fca41472d4acbb2d75b754d570f102d`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14def5a308e7ba00beab57e8d0a555e41835d6a7e1fbe73f8cd629e61bbc8412`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 326.1 KB (326129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a913fc4a516e6de7ee8ad909be1db22fc51317f9f677a7b0ec983264959dacc`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 6.4 MB (6386222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4701a610edc58e425cad5c3761df38b0f91e54ade7cffbc439cd6a221370ad`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1170eed527f5197ddf382cc34947fc054416200276965d19eb7f138c222ac3a8`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5f193df96420bf97804f7057740950b173da86fd7c1f79a5f50160154ce512`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db71a5d16206f50e02aa99cc42ce61d770468b7173c5b885ee1d5516f74682d`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.26`

```console
$ docker pull nats@sha256:b715753bac33754e4ed5c71b7445cc25d6b881fb22d022989ef2844196ce1c2e
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
	-	windows version 10.0.17763.6893; amd64

### `nats:2.10.26` - linux; amd64

```console
$ docker pull nats@sha256:ab30601c4ae2e5de749e7e013dbf1bc8c5f948795d9ba14dfda2cc484f87b552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5923576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736726958d6b2f0e21680f7a56521500766540e90084a54a726a2672e345e95f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ea1d4d1eef4999bdc608bafb79b4807c2e0d126548d7f7d6e3a9b542c153bab`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.9 MB (5923068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8394405f954a1600ce69d033d4616992e140b23520ef911b5e8cb3c9fe0a0bab`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26` - unknown; unknown

```console
$ docker pull nats@sha256:f6eb9f0ff1ba7f1080413295e1bd058a3eb8eaa6346a04ce30d9b12633f178a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5fc4acfc4fca3421337954440d9551afa9681b105c24998d64a27f4f385456`

```dockerfile
```

-	Layers:
	-	`sha256:41f7e4d13b7d0cafe62fb08f772bde421af4e46d7c80aa8051eada0b71e2d6ad`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26` - linux; arm variant v6

```console
$ docker pull nats@sha256:a37f3705ca4f359f2cd688f2f2915c89396f3242ed0017031b1d1ac86b929f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5587283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa848ded2e7f822233d14d085a59458f091b55a5caad5800e30d9759389aeac0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7931d39fd2726f7116d27b851850cf4a1ff6e69fd3de1ed621bfe728eaf4c32`  
		Last Modified: Tue, 25 Feb 2025 19:16:31 GMT  
		Size: 5.6 MB (5586774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526621f9915e8bc26b6f41cb0b4ec86f849a2f797e44f1891bc4ec17549827f4`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26` - unknown; unknown

```console
$ docker pull nats@sha256:2fc0d021712bbbf87403b2efb33aa02fd447167450cd57cbd42e75ddc5fd29ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6710a8bb2aed7e8414816e8dedcb63a21a481320f77bf39efdf73bc7bb11668e`

```dockerfile
```

-	Layers:
	-	`sha256:92236e3a37db849c42f54749091d19b6ef1c03b5d1c5d1bf501fe9ed7360131e`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26` - linux; arm variant v7

```console
$ docker pull nats@sha256:da5d81783ddfc4e6e5ea9c7e9627dbae2052e148b0ca4c3a5adf3e8cdf5881a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5577156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c3470f5d2f8c4e3cdafea8433db44a91110f01e60967c2a3a8d978e31baaed`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0cf7641a4057a532da4f664f9cec79f7fe56c198bb9e71bcbc2c19bb907c58d5`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.6 MB (5576646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3463297bf29a5bbf37928948bb32bb57b1741d42493f2ae75ed53175a517af`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26` - unknown; unknown

```console
$ docker pull nats@sha256:8be21b20d1b6e3d2e901bce12f29bafce42afbbb1b762be62bfc195cb7e9b3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3610a7ae663a5ca8c8be4540df39767d306086365de3263700ddcce895420387`

```dockerfile
```

-	Layers:
	-	`sha256:234087f90831097305eb3b9065da97b803a126593235b546269cfbfa625f608c`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1ab5a26d1f1b792832dd7d52e60d8f57fdcb0ae690e943d796b2b3dea26599c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5471384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96361ef0a1d425f77a7d5bf22cccb8ab926a283d25551390017dcc936f8d6ddd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:34a7e29168d12cc49e3fd1454925bc4b2f10137b37fb10cc85f3b76f5e2959b9`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.5 MB (5470876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0851ead742e7b3af0d74476f1e7610234b00ab6bde066faf665277f50cd3c4c`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26` - unknown; unknown

```console
$ docker pull nats@sha256:4424673c4c02b57552cb838402189f34638ab966b9f85359bad2c59ee9ece0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68e730f04dffe04ac9fcc8af9491ae6be3a7b9be23078e4acc7d0f36fb24ca`

```dockerfile
```

-	Layers:
	-	`sha256:2f7c0d301103a7e55953e57ee1a1660e241006b0b659cffea67752432c2b5ab2`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26` - linux; ppc64le

```console
$ docker pull nats@sha256:1bb4f59414ad9587da0bb4e32ff196ef02914c7e8225b5f3c1a3b79e521de195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5434760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ad4a1f1ab680fc057eaaf6c15371c9fda97d7ac3fa04092cefc46564cceb59`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3821b02a9a90c20826ffaffe25f12d7283677acc84047703af05ac61729fd3da`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.4 MB (5434252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a956e9b697668bf98cbe2a5ec65f9e9c0368945ed81d9e43faa5d064cf6cad4`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26` - unknown; unknown

```console
$ docker pull nats@sha256:e7bf236217d62b740ceeef3cf7150a2b66bf5c247d8d6ffbd991288ec58f799e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe4ef235be79096172af5671be15debaba38653149f5fe74fb76d2c59390183`

```dockerfile
```

-	Layers:
	-	`sha256:baa43bb7d01b88047f62ca6dc61952a118a1bc2c2a3222dbd65a322a26523d7d`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26` - linux; s390x

```console
$ docker pull nats@sha256:84fbc6a0d4f3a6242710d3ea5b8ab4578403aa53d8a5302026bdd6ff20ced27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5777700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcaaa0f666e7b95fe6b20c8bbd70eadf8213e2790de894c72c9f7aa30939f4f0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46891594ec8b4d3680a1bbfe2877deba49c42d5db2b71635cc53e7a260da8759`  
		Last Modified: Tue, 25 Feb 2025 19:16:32 GMT  
		Size: 5.8 MB (5777190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642410c76d1bbecfc24938ff297ac86ca1a30d14e8ab6ef3e9beb0decbbb955`  
		Last Modified: Tue, 25 Feb 2025 23:28:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26` - unknown; unknown

```console
$ docker pull nats@sha256:192747a24178676ee22ac82db357523716ac68b38738fc729a9044432e7b8815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2f83f8a72ce10467cc585601118bc7a449b8d32a56af2df1c019124dfe4ecf`

```dockerfile
```

-	Layers:
	-	`sha256:841b5965931663c1f16aaccf610709337098323a7168962634fe4bed2d16175f`  
		Last Modified: Tue, 25 Feb 2025 23:28:06 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:6a4cc4d864f9bac7dc07b623679bf121113d41d21fc9b5e640e3c92fca1e5111
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112965803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0766c346c8b6c207312a07351709a6e4da8cd036fbaaa8c380d71c1d32ae393`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Tue, 25 Feb 2025 22:17:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:1eb0b36109ac529ab5d5db4ea880cfd63ed514d1f542c8bd20a200d73207ed8e in C:\nats-server.exe 
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 25 Feb 2025 22:17:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464c91c36773a1621c7277522f95c645dc9866e58b0867242b34277fc4145ada`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0903b195c823336fbd58a8a52901057cbde5d4f8e8a3fe8d643f7f0b1008ee5`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 6.0 MB (6044491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a624018395b9843449197873a8dfbfcd7cc07efd09eb9f5cb1fe8b5638255438`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbf5f27ca2dfe7fd5ede70769269354cf7852fe304a1af5d4b7bd17e201a74`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0a43a1bf148b020d83f3b26345be5a7f7cdc277350321ce4ad5a4e0fc73662`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3091f851d62e9660edca35a087ab74e6ce5c1ab16cd2dcc10c87c3b1e04be8`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.26-alpine`

```console
$ docker pull nats@sha256:d69eb29526c1d98afdfb2e2434763bef77b5f3c83e2e24769c13a4d104be475e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `nats:2.10.26-alpine` - linux; amd64

```console
$ docker pull nats@sha256:6e0cca2c6da79f0a3542ec5a3319dd10b1b05f5d8e8949afa8e9cdf6314bbf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10026010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e556ce07f949f5717c6dc8daabda0e17ded6419df74f43518c1f56c1e329c22b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1935954c94119c3706036d5d692853435b83d99c259f8ec51495e3e2efb18a6a`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 6.4 MB (6382794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06613330ae8540f47d41506b7d56df4c5bc71440bf813153c79399e3f5da3c5`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19394475462d5b1aea3c36ff72f30a11aeeb4f440112ebbb15b8a456f653ac55`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:58a608a3d90a3e203ff98c7e1e6bb1d98dcb587196fad9b5046c6a18e27c30e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0ae8cc81e579896c7a782ec0a7819a1abc513aac53c0053d0d8c8707a6100a`

```dockerfile
```

-	Layers:
	-	`sha256:55c1b3c18c84cf1aadd36f17ae37f6e463386696329d2f7845b2b7c772969160`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:888b3676fa9b74db3d6bc52a06a90ec37388f17f7a6c94fba1b0aab761c8d1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9412308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdbc5759068b8c3c7c0d9717f2fa31a8802843622ffa5bc1ee90ab2f97cc836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950d5a437e93fb02cf36f9a20e870f94dd8ac2842175b525de18d73671af6aa`  
		Last Modified: Tue, 25 Feb 2025 21:26:33 GMT  
		Size: 6.0 MB (6046604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d39378960e3fb615203a449ee86a6adc427a58bb348af84af623f9137eddb11`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1ce7e529762c20edc862cef19f51119c18e640a72162538b361811aac9cf6d`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d2f4a4f725f456222c0e0a232f481981a98db2a040b8e5e03a46ba5d19de93b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e467740581e449ded36748d517fc3d41e73c080a765637ab847143ff92b4c0c7`

```dockerfile
```

-	Layers:
	-	`sha256:64782c75142fcb4da7de03639949321d926dd843f9e85121ff5cc18d20715dac`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a1745de189516c48458486fde6b403abc48727f7e2dad55b951a85a77761e2bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9134853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e833dd9f4430c77bf7a6f708e9e6e002d936da7c311595bcdbb9d5979d2b8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2e5935cbee970cdf8caa27a6dafa7c7e944ca51b4d5b9a1c3b93ff3053eb4f`  
		Last Modified: Wed, 26 Feb 2025 02:51:22 GMT  
		Size: 6.0 MB (6035762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb14c94ff9b267a96d276f33d9182a887b066ea83d612971ecc3f07a5357233`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba509bbe23f7c8d23d12b140bf072518aebbb51dac6ac1a53d7dc7c21356dc`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4feb4a911e61e83936b9beb43d347f961ca2560f45191694f78f33d59d58755b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00883483bdc919a66a85b4f2f8521a2ebd1646c8f932d3437be0e289d01313a`

```dockerfile
```

-	Layers:
	-	`sha256:f5175fcbe6f613a2932126ce4d0da80ad1ab95ea38ae164d75b44f9eb774893e`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f9fb7d4a001bdeaf8efe662379474e453f8e63844b5c0913680367fe3124295a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9926441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6700a7a44644d35a74467c9dcbbe2492e70d661075b7755d96a3cbae0229ff7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8405433bc52db97fac8fbd2bd06458903c03f86a2d80d9d5de11d642868850f3`  
		Last Modified: Tue, 25 Feb 2025 23:33:53 GMT  
		Size: 5.9 MB (5932443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704f25bcef9e2d1d2333773f3c5b74abb44de6b6acf941f327d8672bd7ffe138`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5be759409abd41f18a0ac584e5d7d5a24910f005e7c64a45f84ebaf540f34c1`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b07c213de9995bce905bae01e3d3c91262c6ced69feb9739a94cc6e70b6c4941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98276d55b0f5cba673066fca22f6cae9b01c363da2f4f6a99dd3c9295bd32e82`

```dockerfile
```

-	Layers:
	-	`sha256:1b55454322f3ee2db01f280284055234c7a64d43c52c7cc0da084c9ccf4474fd`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:1e5c65a5b378164fbc055112722da9af33284202befb128e9716dfc8d8f998b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9472260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f9943fe40a1d887d0477acbedc42a3822bb2ae7f9ae3f8a2f3bc988aae0c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ad6d76a28889f354cf5c7376c4cd2238dc37a73bae19f1e12a713f6e666bf2`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 5.9 MB (5896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca8c83039c331226a414edca0991c08f1d9f07cdfab82595fbee7aed442ef69`  
		Last Modified: Tue, 25 Feb 2025 21:28:54 GMT  
		Size: 563.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad2d41ba212a6f1ff2dbe03563c50fd26cb7d51e46c4d08af2f4097c759e5c0`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cbfb602ab0fd542d76b033b69f65563107aadb7811c6215a22d44c215bfb9219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6596c1301cd69cdc9984c62cdabbd98209cacedd5cc4c6744c3badaf073080fd`

```dockerfile
```

-	Layers:
	-	`sha256:c5d5cfc84a3213cec6cbc7a0bff5c8f50266b3ffc1f0164f61a05ae22293b11e`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26-alpine` - linux; s390x

```console
$ docker pull nats@sha256:3b8989b0fec1ee207ccdf0f52aa99b9ddd8d3902c1203c501e2d8272949de8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9707272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814240ee91751bb8caa1b427d6fe215c399953d2a8c1da768008d647eedba145`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a056f2f8e8ae073c4ef4c378c426dbf016cc4044eb5010d4c82049d61b8a47`  
		Last Modified: Tue, 25 Feb 2025 22:15:40 GMT  
		Size: 6.2 MB (6238736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccf3a43c9e162fc6fef2651da01103a02bca98d38462fe6395b9b4e6dc96a64`  
		Last Modified: Tue, 25 Feb 2025 22:15:39 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5067f57e0d418f66b609217b8ba7caa018ccab3ac38922d7c4797451579b7468`  
		Last Modified: Tue, 25 Feb 2025 22:15:39 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:66af7d583747898efea9f67c3ff93f8aa993f068528a5aaf50e18a5ffaae2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f226705d21a1826de8bd2c6ee20c35e3966881d96443741ee0b7ff81e103e4`

```dockerfile
```

-	Layers:
	-	`sha256:2db5025980dad4fcac824b97547a716063d145967c77ec341d5394357d3c0e90`  
		Last Modified: Tue, 25 Feb 2025 22:15:40 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.26-alpine3.21`

```console
$ docker pull nats@sha256:d69eb29526c1d98afdfb2e2434763bef77b5f3c83e2e24769c13a4d104be475e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `nats:2.10.26-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:6e0cca2c6da79f0a3542ec5a3319dd10b1b05f5d8e8949afa8e9cdf6314bbf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10026010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e556ce07f949f5717c6dc8daabda0e17ded6419df74f43518c1f56c1e329c22b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1935954c94119c3706036d5d692853435b83d99c259f8ec51495e3e2efb18a6a`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 6.4 MB (6382794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06613330ae8540f47d41506b7d56df4c5bc71440bf813153c79399e3f5da3c5`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19394475462d5b1aea3c36ff72f30a11aeeb4f440112ebbb15b8a456f653ac55`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:58a608a3d90a3e203ff98c7e1e6bb1d98dcb587196fad9b5046c6a18e27c30e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0ae8cc81e579896c7a782ec0a7819a1abc513aac53c0053d0d8c8707a6100a`

```dockerfile
```

-	Layers:
	-	`sha256:55c1b3c18c84cf1aadd36f17ae37f6e463386696329d2f7845b2b7c772969160`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:888b3676fa9b74db3d6bc52a06a90ec37388f17f7a6c94fba1b0aab761c8d1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9412308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdbc5759068b8c3c7c0d9717f2fa31a8802843622ffa5bc1ee90ab2f97cc836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950d5a437e93fb02cf36f9a20e870f94dd8ac2842175b525de18d73671af6aa`  
		Last Modified: Tue, 25 Feb 2025 21:26:33 GMT  
		Size: 6.0 MB (6046604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d39378960e3fb615203a449ee86a6adc427a58bb348af84af623f9137eddb11`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1ce7e529762c20edc862cef19f51119c18e640a72162538b361811aac9cf6d`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:d2f4a4f725f456222c0e0a232f481981a98db2a040b8e5e03a46ba5d19de93b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e467740581e449ded36748d517fc3d41e73c080a765637ab847143ff92b4c0c7`

```dockerfile
```

-	Layers:
	-	`sha256:64782c75142fcb4da7de03639949321d926dd843f9e85121ff5cc18d20715dac`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:a1745de189516c48458486fde6b403abc48727f7e2dad55b951a85a77761e2bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9134853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e833dd9f4430c77bf7a6f708e9e6e002d936da7c311595bcdbb9d5979d2b8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2e5935cbee970cdf8caa27a6dafa7c7e944ca51b4d5b9a1c3b93ff3053eb4f`  
		Last Modified: Wed, 26 Feb 2025 02:51:22 GMT  
		Size: 6.0 MB (6035762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb14c94ff9b267a96d276f33d9182a887b066ea83d612971ecc3f07a5357233`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba509bbe23f7c8d23d12b140bf072518aebbb51dac6ac1a53d7dc7c21356dc`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:4feb4a911e61e83936b9beb43d347f961ca2560f45191694f78f33d59d58755b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00883483bdc919a66a85b4f2f8521a2ebd1646c8f932d3437be0e289d01313a`

```dockerfile
```

-	Layers:
	-	`sha256:f5175fcbe6f613a2932126ce4d0da80ad1ab95ea38ae164d75b44f9eb774893e`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f9fb7d4a001bdeaf8efe662379474e453f8e63844b5c0913680367fe3124295a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9926441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6700a7a44644d35a74467c9dcbbe2492e70d661075b7755d96a3cbae0229ff7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8405433bc52db97fac8fbd2bd06458903c03f86a2d80d9d5de11d642868850f3`  
		Last Modified: Tue, 25 Feb 2025 23:33:53 GMT  
		Size: 5.9 MB (5932443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704f25bcef9e2d1d2333773f3c5b74abb44de6b6acf941f327d8672bd7ffe138`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5be759409abd41f18a0ac584e5d7d5a24910f005e7c64a45f84ebaf540f34c1`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:b07c213de9995bce905bae01e3d3c91262c6ced69feb9739a94cc6e70b6c4941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98276d55b0f5cba673066fca22f6cae9b01c363da2f4f6a99dd3c9295bd32e82`

```dockerfile
```

-	Layers:
	-	`sha256:1b55454322f3ee2db01f280284055234c7a64d43c52c7cc0da084c9ccf4474fd`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:1e5c65a5b378164fbc055112722da9af33284202befb128e9716dfc8d8f998b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9472260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f9943fe40a1d887d0477acbedc42a3822bb2ae7f9ae3f8a2f3bc988aae0c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ad6d76a28889f354cf5c7376c4cd2238dc37a73bae19f1e12a713f6e666bf2`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 5.9 MB (5896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca8c83039c331226a414edca0991c08f1d9f07cdfab82595fbee7aed442ef69`  
		Last Modified: Tue, 25 Feb 2025 21:28:54 GMT  
		Size: 563.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad2d41ba212a6f1ff2dbe03563c50fd26cb7d51e46c4d08af2f4097c759e5c0`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cbfb602ab0fd542d76b033b69f65563107aadb7811c6215a22d44c215bfb9219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6596c1301cd69cdc9984c62cdabbd98209cacedd5cc4c6744c3badaf073080fd`

```dockerfile
```

-	Layers:
	-	`sha256:c5d5cfc84a3213cec6cbc7a0bff5c8f50266b3ffc1f0164f61a05ae22293b11e`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:3b8989b0fec1ee207ccdf0f52aa99b9ddd8d3902c1203c501e2d8272949de8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9707272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814240ee91751bb8caa1b427d6fe215c399953d2a8c1da768008d647eedba145`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a056f2f8e8ae073c4ef4c378c426dbf016cc4044eb5010d4c82049d61b8a47`  
		Last Modified: Tue, 25 Feb 2025 22:15:40 GMT  
		Size: 6.2 MB (6238736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccf3a43c9e162fc6fef2651da01103a02bca98d38462fe6395b9b4e6dc96a64`  
		Last Modified: Tue, 25 Feb 2025 22:15:39 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5067f57e0d418f66b609217b8ba7caa018ccab3ac38922d7c4797451579b7468`  
		Last Modified: Tue, 25 Feb 2025 22:15:39 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:66af7d583747898efea9f67c3ff93f8aa993f068528a5aaf50e18a5ffaae2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f226705d21a1826de8bd2c6ee20c35e3966881d96443741ee0b7ff81e103e4`

```dockerfile
```

-	Layers:
	-	`sha256:2db5025980dad4fcac824b97547a716063d145967c77ec341d5394357d3c0e90`  
		Last Modified: Tue, 25 Feb 2025 22:15:40 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.26-linux`

```console
$ docker pull nats@sha256:d86599f6811aae07be1c0b2b2955d47bb3df8dcf86c1d9fcdc080746829bfe9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `nats:2.10.26-linux` - linux; amd64

```console
$ docker pull nats@sha256:ab30601c4ae2e5de749e7e013dbf1bc8c5f948795d9ba14dfda2cc484f87b552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5923576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736726958d6b2f0e21680f7a56521500766540e90084a54a726a2672e345e95f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ea1d4d1eef4999bdc608bafb79b4807c2e0d126548d7f7d6e3a9b542c153bab`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.9 MB (5923068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8394405f954a1600ce69d033d4616992e140b23520ef911b5e8cb3c9fe0a0bab`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f6eb9f0ff1ba7f1080413295e1bd058a3eb8eaa6346a04ce30d9b12633f178a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5fc4acfc4fca3421337954440d9551afa9681b105c24998d64a27f4f385456`

```dockerfile
```

-	Layers:
	-	`sha256:41f7e4d13b7d0cafe62fb08f772bde421af4e46d7c80aa8051eada0b71e2d6ad`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:a37f3705ca4f359f2cd688f2f2915c89396f3242ed0017031b1d1ac86b929f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5587283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa848ded2e7f822233d14d085a59458f091b55a5caad5800e30d9759389aeac0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7931d39fd2726f7116d27b851850cf4a1ff6e69fd3de1ed621bfe728eaf4c32`  
		Last Modified: Tue, 25 Feb 2025 19:16:31 GMT  
		Size: 5.6 MB (5586774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526621f9915e8bc26b6f41cb0b4ec86f849a2f797e44f1891bc4ec17549827f4`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-linux` - unknown; unknown

```console
$ docker pull nats@sha256:2fc0d021712bbbf87403b2efb33aa02fd447167450cd57cbd42e75ddc5fd29ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6710a8bb2aed7e8414816e8dedcb63a21a481320f77bf39efdf73bc7bb11668e`

```dockerfile
```

-	Layers:
	-	`sha256:92236e3a37db849c42f54749091d19b6ef1c03b5d1c5d1bf501fe9ed7360131e`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:da5d81783ddfc4e6e5ea9c7e9627dbae2052e148b0ca4c3a5adf3e8cdf5881a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5577156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c3470f5d2f8c4e3cdafea8433db44a91110f01e60967c2a3a8d978e31baaed`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0cf7641a4057a532da4f664f9cec79f7fe56c198bb9e71bcbc2c19bb907c58d5`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.6 MB (5576646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3463297bf29a5bbf37928948bb32bb57b1741d42493f2ae75ed53175a517af`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8be21b20d1b6e3d2e901bce12f29bafce42afbbb1b762be62bfc195cb7e9b3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3610a7ae663a5ca8c8be4540df39767d306086365de3263700ddcce895420387`

```dockerfile
```

-	Layers:
	-	`sha256:234087f90831097305eb3b9065da97b803a126593235b546269cfbfa625f608c`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1ab5a26d1f1b792832dd7d52e60d8f57fdcb0ae690e943d796b2b3dea26599c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5471384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96361ef0a1d425f77a7d5bf22cccb8ab926a283d25551390017dcc936f8d6ddd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:34a7e29168d12cc49e3fd1454925bc4b2f10137b37fb10cc85f3b76f5e2959b9`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.5 MB (5470876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0851ead742e7b3af0d74476f1e7610234b00ab6bde066faf665277f50cd3c4c`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4424673c4c02b57552cb838402189f34638ab966b9f85359bad2c59ee9ece0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68e730f04dffe04ac9fcc8af9491ae6be3a7b9be23078e4acc7d0f36fb24ca`

```dockerfile
```

-	Layers:
	-	`sha256:2f7c0d301103a7e55953e57ee1a1660e241006b0b659cffea67752432c2b5ab2`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:1bb4f59414ad9587da0bb4e32ff196ef02914c7e8225b5f3c1a3b79e521de195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5434760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ad4a1f1ab680fc057eaaf6c15371c9fda97d7ac3fa04092cefc46564cceb59`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3821b02a9a90c20826ffaffe25f12d7283677acc84047703af05ac61729fd3da`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.4 MB (5434252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a956e9b697668bf98cbe2a5ec65f9e9c0368945ed81d9e43faa5d064cf6cad4`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-linux` - unknown; unknown

```console
$ docker pull nats@sha256:e7bf236217d62b740ceeef3cf7150a2b66bf5c247d8d6ffbd991288ec58f799e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe4ef235be79096172af5671be15debaba38653149f5fe74fb76d2c59390183`

```dockerfile
```

-	Layers:
	-	`sha256:baa43bb7d01b88047f62ca6dc61952a118a1bc2c2a3222dbd65a322a26523d7d`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26-linux` - linux; s390x

```console
$ docker pull nats@sha256:84fbc6a0d4f3a6242710d3ea5b8ab4578403aa53d8a5302026bdd6ff20ced27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5777700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcaaa0f666e7b95fe6b20c8bbd70eadf8213e2790de894c72c9f7aa30939f4f0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46891594ec8b4d3680a1bbfe2877deba49c42d5db2b71635cc53e7a260da8759`  
		Last Modified: Tue, 25 Feb 2025 19:16:32 GMT  
		Size: 5.8 MB (5777190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642410c76d1bbecfc24938ff297ac86ca1a30d14e8ab6ef3e9beb0decbbb955`  
		Last Modified: Tue, 25 Feb 2025 23:28:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-linux` - unknown; unknown

```console
$ docker pull nats@sha256:192747a24178676ee22ac82db357523716ac68b38738fc729a9044432e7b8815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2f83f8a72ce10467cc585601118bc7a449b8d32a56af2df1c019124dfe4ecf`

```dockerfile
```

-	Layers:
	-	`sha256:841b5965931663c1f16aaccf610709337098323a7168962634fe4bed2d16175f`  
		Last Modified: Tue, 25 Feb 2025 23:28:06 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.26-nanoserver`

```console
$ docker pull nats@sha256:e37f384db2351a1bb09c1e1640b7571e012bece8e5579c2660ec07bf788b53ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2.10.26-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:6a4cc4d864f9bac7dc07b623679bf121113d41d21fc9b5e640e3c92fca1e5111
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112965803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0766c346c8b6c207312a07351709a6e4da8cd036fbaaa8c380d71c1d32ae393`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Tue, 25 Feb 2025 22:17:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:1eb0b36109ac529ab5d5db4ea880cfd63ed514d1f542c8bd20a200d73207ed8e in C:\nats-server.exe 
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 25 Feb 2025 22:17:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464c91c36773a1621c7277522f95c645dc9866e58b0867242b34277fc4145ada`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0903b195c823336fbd58a8a52901057cbde5d4f8e8a3fe8d643f7f0b1008ee5`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 6.0 MB (6044491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a624018395b9843449197873a8dfbfcd7cc07efd09eb9f5cb1fe8b5638255438`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbf5f27ca2dfe7fd5ede70769269354cf7852fe304a1af5d4b7bd17e201a74`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0a43a1bf148b020d83f3b26345be5a7f7cdc277350321ce4ad5a4e0fc73662`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3091f851d62e9660edca35a087ab74e6ce5c1ab16cd2dcc10c87c3b1e04be8`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.26-nanoserver-1809`

```console
$ docker pull nats@sha256:e37f384db2351a1bb09c1e1640b7571e012bece8e5579c2660ec07bf788b53ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2.10.26-nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:6a4cc4d864f9bac7dc07b623679bf121113d41d21fc9b5e640e3c92fca1e5111
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112965803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0766c346c8b6c207312a07351709a6e4da8cd036fbaaa8c380d71c1d32ae393`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Tue, 25 Feb 2025 22:17:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:1eb0b36109ac529ab5d5db4ea880cfd63ed514d1f542c8bd20a200d73207ed8e in C:\nats-server.exe 
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 25 Feb 2025 22:17:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464c91c36773a1621c7277522f95c645dc9866e58b0867242b34277fc4145ada`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0903b195c823336fbd58a8a52901057cbde5d4f8e8a3fe8d643f7f0b1008ee5`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 6.0 MB (6044491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a624018395b9843449197873a8dfbfcd7cc07efd09eb9f5cb1fe8b5638255438`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbf5f27ca2dfe7fd5ede70769269354cf7852fe304a1af5d4b7bd17e201a74`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0a43a1bf148b020d83f3b26345be5a7f7cdc277350321ce4ad5a4e0fc73662`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3091f851d62e9660edca35a087ab74e6ce5c1ab16cd2dcc10c87c3b1e04be8`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.26-scratch`

```console
$ docker pull nats@sha256:d86599f6811aae07be1c0b2b2955d47bb3df8dcf86c1d9fcdc080746829bfe9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `nats:2.10.26-scratch` - linux; amd64

```console
$ docker pull nats@sha256:ab30601c4ae2e5de749e7e013dbf1bc8c5f948795d9ba14dfda2cc484f87b552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5923576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736726958d6b2f0e21680f7a56521500766540e90084a54a726a2672e345e95f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ea1d4d1eef4999bdc608bafb79b4807c2e0d126548d7f7d6e3a9b542c153bab`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.9 MB (5923068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8394405f954a1600ce69d033d4616992e140b23520ef911b5e8cb3c9fe0a0bab`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f6eb9f0ff1ba7f1080413295e1bd058a3eb8eaa6346a04ce30d9b12633f178a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5fc4acfc4fca3421337954440d9551afa9681b105c24998d64a27f4f385456`

```dockerfile
```

-	Layers:
	-	`sha256:41f7e4d13b7d0cafe62fb08f772bde421af4e46d7c80aa8051eada0b71e2d6ad`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:a37f3705ca4f359f2cd688f2f2915c89396f3242ed0017031b1d1ac86b929f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5587283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa848ded2e7f822233d14d085a59458f091b55a5caad5800e30d9759389aeac0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7931d39fd2726f7116d27b851850cf4a1ff6e69fd3de1ed621bfe728eaf4c32`  
		Last Modified: Tue, 25 Feb 2025 19:16:31 GMT  
		Size: 5.6 MB (5586774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526621f9915e8bc26b6f41cb0b4ec86f849a2f797e44f1891bc4ec17549827f4`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2fc0d021712bbbf87403b2efb33aa02fd447167450cd57cbd42e75ddc5fd29ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6710a8bb2aed7e8414816e8dedcb63a21a481320f77bf39efdf73bc7bb11668e`

```dockerfile
```

-	Layers:
	-	`sha256:92236e3a37db849c42f54749091d19b6ef1c03b5d1c5d1bf501fe9ed7360131e`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:da5d81783ddfc4e6e5ea9c7e9627dbae2052e148b0ca4c3a5adf3e8cdf5881a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5577156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c3470f5d2f8c4e3cdafea8433db44a91110f01e60967c2a3a8d978e31baaed`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0cf7641a4057a532da4f664f9cec79f7fe56c198bb9e71bcbc2c19bb907c58d5`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.6 MB (5576646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3463297bf29a5bbf37928948bb32bb57b1741d42493f2ae75ed53175a517af`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8be21b20d1b6e3d2e901bce12f29bafce42afbbb1b762be62bfc195cb7e9b3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3610a7ae663a5ca8c8be4540df39767d306086365de3263700ddcce895420387`

```dockerfile
```

-	Layers:
	-	`sha256:234087f90831097305eb3b9065da97b803a126593235b546269cfbfa625f608c`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1ab5a26d1f1b792832dd7d52e60d8f57fdcb0ae690e943d796b2b3dea26599c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5471384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96361ef0a1d425f77a7d5bf22cccb8ab926a283d25551390017dcc936f8d6ddd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:34a7e29168d12cc49e3fd1454925bc4b2f10137b37fb10cc85f3b76f5e2959b9`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.5 MB (5470876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0851ead742e7b3af0d74476f1e7610234b00ab6bde066faf665277f50cd3c4c`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4424673c4c02b57552cb838402189f34638ab966b9f85359bad2c59ee9ece0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68e730f04dffe04ac9fcc8af9491ae6be3a7b9be23078e4acc7d0f36fb24ca`

```dockerfile
```

-	Layers:
	-	`sha256:2f7c0d301103a7e55953e57ee1a1660e241006b0b659cffea67752432c2b5ab2`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:1bb4f59414ad9587da0bb4e32ff196ef02914c7e8225b5f3c1a3b79e521de195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5434760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ad4a1f1ab680fc057eaaf6c15371c9fda97d7ac3fa04092cefc46564cceb59`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3821b02a9a90c20826ffaffe25f12d7283677acc84047703af05ac61729fd3da`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.4 MB (5434252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a956e9b697668bf98cbe2a5ec65f9e9c0368945ed81d9e43faa5d064cf6cad4`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e7bf236217d62b740ceeef3cf7150a2b66bf5c247d8d6ffbd991288ec58f799e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe4ef235be79096172af5671be15debaba38653149f5fe74fb76d2c59390183`

```dockerfile
```

-	Layers:
	-	`sha256:baa43bb7d01b88047f62ca6dc61952a118a1bc2c2a3222dbd65a322a26523d7d`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.26-scratch` - linux; s390x

```console
$ docker pull nats@sha256:84fbc6a0d4f3a6242710d3ea5b8ab4578403aa53d8a5302026bdd6ff20ced27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5777700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcaaa0f666e7b95fe6b20c8bbd70eadf8213e2790de894c72c9f7aa30939f4f0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46891594ec8b4d3680a1bbfe2877deba49c42d5db2b71635cc53e7a260da8759`  
		Last Modified: Tue, 25 Feb 2025 19:16:32 GMT  
		Size: 5.8 MB (5777190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642410c76d1bbecfc24938ff297ac86ca1a30d14e8ab6ef3e9beb0decbbb955`  
		Last Modified: Tue, 25 Feb 2025 23:28:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.26-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:192747a24178676ee22ac82db357523716ac68b38738fc729a9044432e7b8815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2f83f8a72ce10467cc585601118bc7a449b8d32a56af2df1c019124dfe4ecf`

```dockerfile
```

-	Layers:
	-	`sha256:841b5965931663c1f16aaccf610709337098323a7168962634fe4bed2d16175f`  
		Last Modified: Tue, 25 Feb 2025 23:28:06 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.26-windowsservercore`

```console
$ docker pull nats@sha256:68de8391f116e75689a8894608af44359d970ed0f73f652cc4f64667a5974762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2.10.26-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:f9baf586a7d5a24f77abdc3e1893d5742cbb2a8727aec3f00c4d2c65084ecfbf
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2143633528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4da431eb1469f157d1feecdb9b465288b0a748b57532bb21fca3548c57614c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 25 Feb 2025 21:36:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 25 Feb 2025 21:36:36 GMT
ENV NATS_DOCKERIZED=1
# Tue, 25 Feb 2025 21:36:37 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 21:36:37 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.26/nats-server-v2.10.26-windows-amd64.zip
# Tue, 25 Feb 2025 21:36:38 GMT
ENV NATS_SERVER_SHASUM=e1f9c4eee642bd521878dc493de8514b25c1468e3f2420312aa52f96f7bcbabf
# Tue, 25 Feb 2025 21:37:18 GMT
RUN Set-PSDebug -Trace 2
# Tue, 25 Feb 2025 21:37:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 25 Feb 2025 21:37:36 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 25 Feb 2025 21:37:36 GMT
EXPOSE 4222 6222 8222
# Tue, 25 Feb 2025 21:37:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 25 Feb 2025 21:37:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2962c26ced92b9e3c7f5d7aebd4559298828b0ae76a0527bf5464eb8c93c00`  
		Last Modified: Tue, 25 Feb 2025 21:37:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32fccbfd6adf85f404d7d84d70587914a6f99fa5e496abee390614035e0c64`  
		Last Modified: Tue, 25 Feb 2025 21:37:42 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990ef8a50ae119e863c3a1547280197e5983c7b6ddb20783b3dd54628b42f904`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afc88e2f571205bcf887d86513344166fa69e24de8659740f8ad26cd9154a06`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73a99f6d11801b46659a585416d0f1f7fca41472d4acbb2d75b754d570f102d`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14def5a308e7ba00beab57e8d0a555e41835d6a7e1fbe73f8cd629e61bbc8412`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 326.1 KB (326129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a913fc4a516e6de7ee8ad909be1db22fc51317f9f677a7b0ec983264959dacc`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 6.4 MB (6386222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4701a610edc58e425cad5c3761df38b0f91e54ade7cffbc439cd6a221370ad`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1170eed527f5197ddf382cc34947fc054416200276965d19eb7f138c222ac3a8`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5f193df96420bf97804f7057740950b173da86fd7c1f79a5f50160154ce512`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db71a5d16206f50e02aa99cc42ce61d770468b7173c5b885ee1d5516f74682d`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.26-windowsservercore-1809`

```console
$ docker pull nats@sha256:68de8391f116e75689a8894608af44359d970ed0f73f652cc4f64667a5974762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2.10.26-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:f9baf586a7d5a24f77abdc3e1893d5742cbb2a8727aec3f00c4d2c65084ecfbf
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2143633528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4da431eb1469f157d1feecdb9b465288b0a748b57532bb21fca3548c57614c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 25 Feb 2025 21:36:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 25 Feb 2025 21:36:36 GMT
ENV NATS_DOCKERIZED=1
# Tue, 25 Feb 2025 21:36:37 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 21:36:37 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.26/nats-server-v2.10.26-windows-amd64.zip
# Tue, 25 Feb 2025 21:36:38 GMT
ENV NATS_SERVER_SHASUM=e1f9c4eee642bd521878dc493de8514b25c1468e3f2420312aa52f96f7bcbabf
# Tue, 25 Feb 2025 21:37:18 GMT
RUN Set-PSDebug -Trace 2
# Tue, 25 Feb 2025 21:37:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 25 Feb 2025 21:37:36 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 25 Feb 2025 21:37:36 GMT
EXPOSE 4222 6222 8222
# Tue, 25 Feb 2025 21:37:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 25 Feb 2025 21:37:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2962c26ced92b9e3c7f5d7aebd4559298828b0ae76a0527bf5464eb8c93c00`  
		Last Modified: Tue, 25 Feb 2025 21:37:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32fccbfd6adf85f404d7d84d70587914a6f99fa5e496abee390614035e0c64`  
		Last Modified: Tue, 25 Feb 2025 21:37:42 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990ef8a50ae119e863c3a1547280197e5983c7b6ddb20783b3dd54628b42f904`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afc88e2f571205bcf887d86513344166fa69e24de8659740f8ad26cd9154a06`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73a99f6d11801b46659a585416d0f1f7fca41472d4acbb2d75b754d570f102d`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14def5a308e7ba00beab57e8d0a555e41835d6a7e1fbe73f8cd629e61bbc8412`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 326.1 KB (326129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a913fc4a516e6de7ee8ad909be1db22fc51317f9f677a7b0ec983264959dacc`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 6.4 MB (6386222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4701a610edc58e425cad5c3761df38b0f91e54ade7cffbc439cd6a221370ad`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1170eed527f5197ddf382cc34947fc054416200276965d19eb7f138c222ac3a8`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5f193df96420bf97804f7057740950b173da86fd7c1f79a5f50160154ce512`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db71a5d16206f50e02aa99cc42ce61d770468b7173c5b885ee1d5516f74682d`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:d69eb29526c1d98afdfb2e2434763bef77b5f3c83e2e24769c13a4d104be475e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:6e0cca2c6da79f0a3542ec5a3319dd10b1b05f5d8e8949afa8e9cdf6314bbf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10026010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e556ce07f949f5717c6dc8daabda0e17ded6419df74f43518c1f56c1e329c22b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1935954c94119c3706036d5d692853435b83d99c259f8ec51495e3e2efb18a6a`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 6.4 MB (6382794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06613330ae8540f47d41506b7d56df4c5bc71440bf813153c79399e3f5da3c5`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19394475462d5b1aea3c36ff72f30a11aeeb4f440112ebbb15b8a456f653ac55`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:58a608a3d90a3e203ff98c7e1e6bb1d98dcb587196fad9b5046c6a18e27c30e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0ae8cc81e579896c7a782ec0a7819a1abc513aac53c0053d0d8c8707a6100a`

```dockerfile
```

-	Layers:
	-	`sha256:55c1b3c18c84cf1aadd36f17ae37f6e463386696329d2f7845b2b7c772969160`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:888b3676fa9b74db3d6bc52a06a90ec37388f17f7a6c94fba1b0aab761c8d1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9412308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdbc5759068b8c3c7c0d9717f2fa31a8802843622ffa5bc1ee90ab2f97cc836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950d5a437e93fb02cf36f9a20e870f94dd8ac2842175b525de18d73671af6aa`  
		Last Modified: Tue, 25 Feb 2025 21:26:33 GMT  
		Size: 6.0 MB (6046604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d39378960e3fb615203a449ee86a6adc427a58bb348af84af623f9137eddb11`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1ce7e529762c20edc862cef19f51119c18e640a72162538b361811aac9cf6d`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d2f4a4f725f456222c0e0a232f481981a98db2a040b8e5e03a46ba5d19de93b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e467740581e449ded36748d517fc3d41e73c080a765637ab847143ff92b4c0c7`

```dockerfile
```

-	Layers:
	-	`sha256:64782c75142fcb4da7de03639949321d926dd843f9e85121ff5cc18d20715dac`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a1745de189516c48458486fde6b403abc48727f7e2dad55b951a85a77761e2bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9134853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e833dd9f4430c77bf7a6f708e9e6e002d936da7c311595bcdbb9d5979d2b8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2e5935cbee970cdf8caa27a6dafa7c7e944ca51b4d5b9a1c3b93ff3053eb4f`  
		Last Modified: Wed, 26 Feb 2025 02:51:22 GMT  
		Size: 6.0 MB (6035762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb14c94ff9b267a96d276f33d9182a887b066ea83d612971ecc3f07a5357233`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba509bbe23f7c8d23d12b140bf072518aebbb51dac6ac1a53d7dc7c21356dc`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4feb4a911e61e83936b9beb43d347f961ca2560f45191694f78f33d59d58755b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00883483bdc919a66a85b4f2f8521a2ebd1646c8f932d3437be0e289d01313a`

```dockerfile
```

-	Layers:
	-	`sha256:f5175fcbe6f613a2932126ce4d0da80ad1ab95ea38ae164d75b44f9eb774893e`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f9fb7d4a001bdeaf8efe662379474e453f8e63844b5c0913680367fe3124295a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9926441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6700a7a44644d35a74467c9dcbbe2492e70d661075b7755d96a3cbae0229ff7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8405433bc52db97fac8fbd2bd06458903c03f86a2d80d9d5de11d642868850f3`  
		Last Modified: Tue, 25 Feb 2025 23:33:53 GMT  
		Size: 5.9 MB (5932443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704f25bcef9e2d1d2333773f3c5b74abb44de6b6acf941f327d8672bd7ffe138`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5be759409abd41f18a0ac584e5d7d5a24910f005e7c64a45f84ebaf540f34c1`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b07c213de9995bce905bae01e3d3c91262c6ced69feb9739a94cc6e70b6c4941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98276d55b0f5cba673066fca22f6cae9b01c363da2f4f6a99dd3c9295bd32e82`

```dockerfile
```

-	Layers:
	-	`sha256:1b55454322f3ee2db01f280284055234c7a64d43c52c7cc0da084c9ccf4474fd`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:1e5c65a5b378164fbc055112722da9af33284202befb128e9716dfc8d8f998b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9472260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f9943fe40a1d887d0477acbedc42a3822bb2ae7f9ae3f8a2f3bc988aae0c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ad6d76a28889f354cf5c7376c4cd2238dc37a73bae19f1e12a713f6e666bf2`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 5.9 MB (5896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca8c83039c331226a414edca0991c08f1d9f07cdfab82595fbee7aed442ef69`  
		Last Modified: Tue, 25 Feb 2025 21:28:54 GMT  
		Size: 563.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad2d41ba212a6f1ff2dbe03563c50fd26cb7d51e46c4d08af2f4097c759e5c0`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cbfb602ab0fd542d76b033b69f65563107aadb7811c6215a22d44c215bfb9219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6596c1301cd69cdc9984c62cdabbd98209cacedd5cc4c6744c3badaf073080fd`

```dockerfile
```

-	Layers:
	-	`sha256:c5d5cfc84a3213cec6cbc7a0bff5c8f50266b3ffc1f0164f61a05ae22293b11e`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:3b8989b0fec1ee207ccdf0f52aa99b9ddd8d3902c1203c501e2d8272949de8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9707272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814240ee91751bb8caa1b427d6fe215c399953d2a8c1da768008d647eedba145`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a056f2f8e8ae073c4ef4c378c426dbf016cc4044eb5010d4c82049d61b8a47`  
		Last Modified: Tue, 25 Feb 2025 22:15:40 GMT  
		Size: 6.2 MB (6238736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccf3a43c9e162fc6fef2651da01103a02bca98d38462fe6395b9b4e6dc96a64`  
		Last Modified: Tue, 25 Feb 2025 22:15:39 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5067f57e0d418f66b609217b8ba7caa018ccab3ac38922d7c4797451579b7468`  
		Last Modified: Tue, 25 Feb 2025 22:15:39 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:66af7d583747898efea9f67c3ff93f8aa993f068528a5aaf50e18a5ffaae2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f226705d21a1826de8bd2c6ee20c35e3966881d96443741ee0b7ff81e103e4`

```dockerfile
```

-	Layers:
	-	`sha256:2db5025980dad4fcac824b97547a716063d145967c77ec341d5394357d3c0e90`  
		Last Modified: Tue, 25 Feb 2025 22:15:40 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.21`

```console
$ docker pull nats@sha256:d69eb29526c1d98afdfb2e2434763bef77b5f3c83e2e24769c13a4d104be475e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `nats:alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:6e0cca2c6da79f0a3542ec5a3319dd10b1b05f5d8e8949afa8e9cdf6314bbf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10026010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e556ce07f949f5717c6dc8daabda0e17ded6419df74f43518c1f56c1e329c22b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1935954c94119c3706036d5d692853435b83d99c259f8ec51495e3e2efb18a6a`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 6.4 MB (6382794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06613330ae8540f47d41506b7d56df4c5bc71440bf813153c79399e3f5da3c5`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19394475462d5b1aea3c36ff72f30a11aeeb4f440112ebbb15b8a456f653ac55`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:58a608a3d90a3e203ff98c7e1e6bb1d98dcb587196fad9b5046c6a18e27c30e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0ae8cc81e579896c7a782ec0a7819a1abc513aac53c0053d0d8c8707a6100a`

```dockerfile
```

-	Layers:
	-	`sha256:55c1b3c18c84cf1aadd36f17ae37f6e463386696329d2f7845b2b7c772969160`  
		Last Modified: Tue, 25 Feb 2025 21:26:56 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:888b3676fa9b74db3d6bc52a06a90ec37388f17f7a6c94fba1b0aab761c8d1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9412308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdbc5759068b8c3c7c0d9717f2fa31a8802843622ffa5bc1ee90ab2f97cc836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950d5a437e93fb02cf36f9a20e870f94dd8ac2842175b525de18d73671af6aa`  
		Last Modified: Tue, 25 Feb 2025 21:26:33 GMT  
		Size: 6.0 MB (6046604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d39378960e3fb615203a449ee86a6adc427a58bb348af84af623f9137eddb11`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1ce7e529762c20edc862cef19f51119c18e640a72162538b361811aac9cf6d`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:d2f4a4f725f456222c0e0a232f481981a98db2a040b8e5e03a46ba5d19de93b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e467740581e449ded36748d517fc3d41e73c080a765637ab847143ff92b4c0c7`

```dockerfile
```

-	Layers:
	-	`sha256:64782c75142fcb4da7de03639949321d926dd843f9e85121ff5cc18d20715dac`  
		Last Modified: Tue, 25 Feb 2025 21:26:32 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:a1745de189516c48458486fde6b403abc48727f7e2dad55b951a85a77761e2bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9134853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e833dd9f4430c77bf7a6f708e9e6e002d936da7c311595bcdbb9d5979d2b8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2e5935cbee970cdf8caa27a6dafa7c7e944ca51b4d5b9a1c3b93ff3053eb4f`  
		Last Modified: Wed, 26 Feb 2025 02:51:22 GMT  
		Size: 6.0 MB (6035762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb14c94ff9b267a96d276f33d9182a887b066ea83d612971ecc3f07a5357233`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba509bbe23f7c8d23d12b140bf072518aebbb51dac6ac1a53d7dc7c21356dc`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:4feb4a911e61e83936b9beb43d347f961ca2560f45191694f78f33d59d58755b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00883483bdc919a66a85b4f2f8521a2ebd1646c8f932d3437be0e289d01313a`

```dockerfile
```

-	Layers:
	-	`sha256:f5175fcbe6f613a2932126ce4d0da80ad1ab95ea38ae164d75b44f9eb774893e`  
		Last Modified: Wed, 26 Feb 2025 02:51:21 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f9fb7d4a001bdeaf8efe662379474e453f8e63844b5c0913680367fe3124295a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9926441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6700a7a44644d35a74467c9dcbbe2492e70d661075b7755d96a3cbae0229ff7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8405433bc52db97fac8fbd2bd06458903c03f86a2d80d9d5de11d642868850f3`  
		Last Modified: Tue, 25 Feb 2025 23:33:53 GMT  
		Size: 5.9 MB (5932443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704f25bcef9e2d1d2333773f3c5b74abb44de6b6acf941f327d8672bd7ffe138`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5be759409abd41f18a0ac584e5d7d5a24910f005e7c64a45f84ebaf540f34c1`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:b07c213de9995bce905bae01e3d3c91262c6ced69feb9739a94cc6e70b6c4941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98276d55b0f5cba673066fca22f6cae9b01c363da2f4f6a99dd3c9295bd32e82`

```dockerfile
```

-	Layers:
	-	`sha256:1b55454322f3ee2db01f280284055234c7a64d43c52c7cc0da084c9ccf4474fd`  
		Last Modified: Tue, 25 Feb 2025 23:33:52 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:1e5c65a5b378164fbc055112722da9af33284202befb128e9716dfc8d8f998b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9472260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f9943fe40a1d887d0477acbedc42a3822bb2ae7f9ae3f8a2f3bc988aae0c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ad6d76a28889f354cf5c7376c4cd2238dc37a73bae19f1e12a713f6e666bf2`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 5.9 MB (5896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca8c83039c331226a414edca0991c08f1d9f07cdfab82595fbee7aed442ef69`  
		Last Modified: Tue, 25 Feb 2025 21:28:54 GMT  
		Size: 563.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad2d41ba212a6f1ff2dbe03563c50fd26cb7d51e46c4d08af2f4097c759e5c0`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cbfb602ab0fd542d76b033b69f65563107aadb7811c6215a22d44c215bfb9219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6596c1301cd69cdc9984c62cdabbd98209cacedd5cc4c6744c3badaf073080fd`

```dockerfile
```

-	Layers:
	-	`sha256:c5d5cfc84a3213cec6cbc7a0bff5c8f50266b3ffc1f0164f61a05ae22293b11e`  
		Last Modified: Tue, 25 Feb 2025 21:28:55 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:3b8989b0fec1ee207ccdf0f52aa99b9ddd8d3902c1203c501e2d8272949de8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9707272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814240ee91751bb8caa1b427d6fe215c399953d2a8c1da768008d647eedba145`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 19:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='aba1b169f18d4441b4b5d760805c562dccc57b425a7a213a82753a2269a27235' ;; 		armhf) natsArch='arm6'; sha256='65a7003e8bfad9e8ba2d34efe8cc33299e754da2134d30b9cffb37561379f9b2' ;; 		armv7) natsArch='arm7'; sha256='85bfefdd849528df836da8820b46a088c20bbb7cf2ef90dfaa5211a789ac92be' ;; 		x86_64) natsArch='amd64'; sha256='6cbac67107e69c9e5a352d6f1555027f9da6a6b3fa81cceafefa9598b4451512' ;; 		x86) natsArch='386'; sha256='fc536de9e39ffe69f3f593e10c34d39a68c1ac98cfd88eff28f8c87dd09ec804' ;; 		s390x) natsArch='s390x'; sha256='c6f857d0dec8ea44f78efa3b4a7580fb51b7419e32b168bb1cb476527db04971' ;; 		ppc64le) natsArch='ppc64le'; sha256='d416e0c151959ec896152ded12746e75ff549b9643dbec1e0087b0262c5b959a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a056f2f8e8ae073c4ef4c378c426dbf016cc4044eb5010d4c82049d61b8a47`  
		Last Modified: Tue, 25 Feb 2025 22:15:40 GMT  
		Size: 6.2 MB (6238736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccf3a43c9e162fc6fef2651da01103a02bca98d38462fe6395b9b4e6dc96a64`  
		Last Modified: Tue, 25 Feb 2025 22:15:39 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5067f57e0d418f66b609217b8ba7caa018ccab3ac38922d7c4797451579b7468`  
		Last Modified: Tue, 25 Feb 2025 22:15:39 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:66af7d583747898efea9f67c3ff93f8aa993f068528a5aaf50e18a5ffaae2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f226705d21a1826de8bd2c6ee20c35e3966881d96443741ee0b7ff81e103e4`

```dockerfile
```

-	Layers:
	-	`sha256:2db5025980dad4fcac824b97547a716063d145967c77ec341d5394357d3c0e90`  
		Last Modified: Tue, 25 Feb 2025 22:15:40 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:b715753bac33754e4ed5c71b7445cc25d6b881fb22d022989ef2844196ce1c2e
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
	-	windows version 10.0.17763.6893; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:ab30601c4ae2e5de749e7e013dbf1bc8c5f948795d9ba14dfda2cc484f87b552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5923576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736726958d6b2f0e21680f7a56521500766540e90084a54a726a2672e345e95f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ea1d4d1eef4999bdc608bafb79b4807c2e0d126548d7f7d6e3a9b542c153bab`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.9 MB (5923068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8394405f954a1600ce69d033d4616992e140b23520ef911b5e8cb3c9fe0a0bab`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:f6eb9f0ff1ba7f1080413295e1bd058a3eb8eaa6346a04ce30d9b12633f178a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5fc4acfc4fca3421337954440d9551afa9681b105c24998d64a27f4f385456`

```dockerfile
```

-	Layers:
	-	`sha256:41f7e4d13b7d0cafe62fb08f772bde421af4e46d7c80aa8051eada0b71e2d6ad`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:a37f3705ca4f359f2cd688f2f2915c89396f3242ed0017031b1d1ac86b929f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5587283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa848ded2e7f822233d14d085a59458f091b55a5caad5800e30d9759389aeac0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7931d39fd2726f7116d27b851850cf4a1ff6e69fd3de1ed621bfe728eaf4c32`  
		Last Modified: Tue, 25 Feb 2025 19:16:31 GMT  
		Size: 5.6 MB (5586774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526621f9915e8bc26b6f41cb0b4ec86f849a2f797e44f1891bc4ec17549827f4`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:2fc0d021712bbbf87403b2efb33aa02fd447167450cd57cbd42e75ddc5fd29ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6710a8bb2aed7e8414816e8dedcb63a21a481320f77bf39efdf73bc7bb11668e`

```dockerfile
```

-	Layers:
	-	`sha256:92236e3a37db849c42f54749091d19b6ef1c03b5d1c5d1bf501fe9ed7360131e`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:da5d81783ddfc4e6e5ea9c7e9627dbae2052e148b0ca4c3a5adf3e8cdf5881a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5577156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c3470f5d2f8c4e3cdafea8433db44a91110f01e60967c2a3a8d978e31baaed`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0cf7641a4057a532da4f664f9cec79f7fe56c198bb9e71bcbc2c19bb907c58d5`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.6 MB (5576646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3463297bf29a5bbf37928948bb32bb57b1741d42493f2ae75ed53175a517af`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:8be21b20d1b6e3d2e901bce12f29bafce42afbbb1b762be62bfc195cb7e9b3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3610a7ae663a5ca8c8be4540df39767d306086365de3263700ddcce895420387`

```dockerfile
```

-	Layers:
	-	`sha256:234087f90831097305eb3b9065da97b803a126593235b546269cfbfa625f608c`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1ab5a26d1f1b792832dd7d52e60d8f57fdcb0ae690e943d796b2b3dea26599c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5471384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96361ef0a1d425f77a7d5bf22cccb8ab926a283d25551390017dcc936f8d6ddd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:34a7e29168d12cc49e3fd1454925bc4b2f10137b37fb10cc85f3b76f5e2959b9`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.5 MB (5470876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0851ead742e7b3af0d74476f1e7610234b00ab6bde066faf665277f50cd3c4c`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:4424673c4c02b57552cb838402189f34638ab966b9f85359bad2c59ee9ece0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68e730f04dffe04ac9fcc8af9491ae6be3a7b9be23078e4acc7d0f36fb24ca`

```dockerfile
```

-	Layers:
	-	`sha256:2f7c0d301103a7e55953e57ee1a1660e241006b0b659cffea67752432c2b5ab2`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:1bb4f59414ad9587da0bb4e32ff196ef02914c7e8225b5f3c1a3b79e521de195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5434760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ad4a1f1ab680fc057eaaf6c15371c9fda97d7ac3fa04092cefc46564cceb59`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3821b02a9a90c20826ffaffe25f12d7283677acc84047703af05ac61729fd3da`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.4 MB (5434252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a956e9b697668bf98cbe2a5ec65f9e9c0368945ed81d9e43faa5d064cf6cad4`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:e7bf236217d62b740ceeef3cf7150a2b66bf5c247d8d6ffbd991288ec58f799e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe4ef235be79096172af5671be15debaba38653149f5fe74fb76d2c59390183`

```dockerfile
```

-	Layers:
	-	`sha256:baa43bb7d01b88047f62ca6dc61952a118a1bc2c2a3222dbd65a322a26523d7d`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:84fbc6a0d4f3a6242710d3ea5b8ab4578403aa53d8a5302026bdd6ff20ced27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5777700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcaaa0f666e7b95fe6b20c8bbd70eadf8213e2790de894c72c9f7aa30939f4f0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46891594ec8b4d3680a1bbfe2877deba49c42d5db2b71635cc53e7a260da8759`  
		Last Modified: Tue, 25 Feb 2025 19:16:32 GMT  
		Size: 5.8 MB (5777190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642410c76d1bbecfc24938ff297ac86ca1a30d14e8ab6ef3e9beb0decbbb955`  
		Last Modified: Tue, 25 Feb 2025 23:28:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:192747a24178676ee22ac82db357523716ac68b38738fc729a9044432e7b8815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2f83f8a72ce10467cc585601118bc7a449b8d32a56af2df1c019124dfe4ecf`

```dockerfile
```

-	Layers:
	-	`sha256:841b5965931663c1f16aaccf610709337098323a7168962634fe4bed2d16175f`  
		Last Modified: Tue, 25 Feb 2025 23:28:06 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:6a4cc4d864f9bac7dc07b623679bf121113d41d21fc9b5e640e3c92fca1e5111
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112965803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0766c346c8b6c207312a07351709a6e4da8cd036fbaaa8c380d71c1d32ae393`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Tue, 25 Feb 2025 22:17:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:1eb0b36109ac529ab5d5db4ea880cfd63ed514d1f542c8bd20a200d73207ed8e in C:\nats-server.exe 
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 25 Feb 2025 22:17:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464c91c36773a1621c7277522f95c645dc9866e58b0867242b34277fc4145ada`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0903b195c823336fbd58a8a52901057cbde5d4f8e8a3fe8d643f7f0b1008ee5`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 6.0 MB (6044491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a624018395b9843449197873a8dfbfcd7cc07efd09eb9f5cb1fe8b5638255438`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbf5f27ca2dfe7fd5ede70769269354cf7852fe304a1af5d4b7bd17e201a74`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0a43a1bf148b020d83f3b26345be5a7f7cdc277350321ce4ad5a4e0fc73662`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3091f851d62e9660edca35a087ab74e6ce5c1ab16cd2dcc10c87c3b1e04be8`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:d86599f6811aae07be1c0b2b2955d47bb3df8dcf86c1d9fcdc080746829bfe9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:ab30601c4ae2e5de749e7e013dbf1bc8c5f948795d9ba14dfda2cc484f87b552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5923576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736726958d6b2f0e21680f7a56521500766540e90084a54a726a2672e345e95f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ea1d4d1eef4999bdc608bafb79b4807c2e0d126548d7f7d6e3a9b542c153bab`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.9 MB (5923068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8394405f954a1600ce69d033d4616992e140b23520ef911b5e8cb3c9fe0a0bab`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:f6eb9f0ff1ba7f1080413295e1bd058a3eb8eaa6346a04ce30d9b12633f178a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5fc4acfc4fca3421337954440d9551afa9681b105c24998d64a27f4f385456`

```dockerfile
```

-	Layers:
	-	`sha256:41f7e4d13b7d0cafe62fb08f772bde421af4e46d7c80aa8051eada0b71e2d6ad`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:a37f3705ca4f359f2cd688f2f2915c89396f3242ed0017031b1d1ac86b929f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5587283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa848ded2e7f822233d14d085a59458f091b55a5caad5800e30d9759389aeac0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7931d39fd2726f7116d27b851850cf4a1ff6e69fd3de1ed621bfe728eaf4c32`  
		Last Modified: Tue, 25 Feb 2025 19:16:31 GMT  
		Size: 5.6 MB (5586774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526621f9915e8bc26b6f41cb0b4ec86f849a2f797e44f1891bc4ec17549827f4`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:2fc0d021712bbbf87403b2efb33aa02fd447167450cd57cbd42e75ddc5fd29ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6710a8bb2aed7e8414816e8dedcb63a21a481320f77bf39efdf73bc7bb11668e`

```dockerfile
```

-	Layers:
	-	`sha256:92236e3a37db849c42f54749091d19b6ef1c03b5d1c5d1bf501fe9ed7360131e`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:da5d81783ddfc4e6e5ea9c7e9627dbae2052e148b0ca4c3a5adf3e8cdf5881a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5577156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c3470f5d2f8c4e3cdafea8433db44a91110f01e60967c2a3a8d978e31baaed`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0cf7641a4057a532da4f664f9cec79f7fe56c198bb9e71bcbc2c19bb907c58d5`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.6 MB (5576646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3463297bf29a5bbf37928948bb32bb57b1741d42493f2ae75ed53175a517af`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:8be21b20d1b6e3d2e901bce12f29bafce42afbbb1b762be62bfc195cb7e9b3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3610a7ae663a5ca8c8be4540df39767d306086365de3263700ddcce895420387`

```dockerfile
```

-	Layers:
	-	`sha256:234087f90831097305eb3b9065da97b803a126593235b546269cfbfa625f608c`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1ab5a26d1f1b792832dd7d52e60d8f57fdcb0ae690e943d796b2b3dea26599c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5471384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96361ef0a1d425f77a7d5bf22cccb8ab926a283d25551390017dcc936f8d6ddd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:34a7e29168d12cc49e3fd1454925bc4b2f10137b37fb10cc85f3b76f5e2959b9`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.5 MB (5470876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0851ead742e7b3af0d74476f1e7610234b00ab6bde066faf665277f50cd3c4c`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:4424673c4c02b57552cb838402189f34638ab966b9f85359bad2c59ee9ece0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68e730f04dffe04ac9fcc8af9491ae6be3a7b9be23078e4acc7d0f36fb24ca`

```dockerfile
```

-	Layers:
	-	`sha256:2f7c0d301103a7e55953e57ee1a1660e241006b0b659cffea67752432c2b5ab2`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:1bb4f59414ad9587da0bb4e32ff196ef02914c7e8225b5f3c1a3b79e521de195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5434760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ad4a1f1ab680fc057eaaf6c15371c9fda97d7ac3fa04092cefc46564cceb59`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3821b02a9a90c20826ffaffe25f12d7283677acc84047703af05ac61729fd3da`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.4 MB (5434252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a956e9b697668bf98cbe2a5ec65f9e9c0368945ed81d9e43faa5d064cf6cad4`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:e7bf236217d62b740ceeef3cf7150a2b66bf5c247d8d6ffbd991288ec58f799e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe4ef235be79096172af5671be15debaba38653149f5fe74fb76d2c59390183`

```dockerfile
```

-	Layers:
	-	`sha256:baa43bb7d01b88047f62ca6dc61952a118a1bc2c2a3222dbd65a322a26523d7d`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:84fbc6a0d4f3a6242710d3ea5b8ab4578403aa53d8a5302026bdd6ff20ced27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5777700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcaaa0f666e7b95fe6b20c8bbd70eadf8213e2790de894c72c9f7aa30939f4f0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46891594ec8b4d3680a1bbfe2877deba49c42d5db2b71635cc53e7a260da8759`  
		Last Modified: Tue, 25 Feb 2025 19:16:32 GMT  
		Size: 5.8 MB (5777190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642410c76d1bbecfc24938ff297ac86ca1a30d14e8ab6ef3e9beb0decbbb955`  
		Last Modified: Tue, 25 Feb 2025 23:28:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:192747a24178676ee22ac82db357523716ac68b38738fc729a9044432e7b8815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2f83f8a72ce10467cc585601118bc7a449b8d32a56af2df1c019124dfe4ecf`

```dockerfile
```

-	Layers:
	-	`sha256:841b5965931663c1f16aaccf610709337098323a7168962634fe4bed2d16175f`  
		Last Modified: Tue, 25 Feb 2025 23:28:06 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:e37f384db2351a1bb09c1e1640b7571e012bece8e5579c2660ec07bf788b53ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:6a4cc4d864f9bac7dc07b623679bf121113d41d21fc9b5e640e3c92fca1e5111
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112965803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0766c346c8b6c207312a07351709a6e4da8cd036fbaaa8c380d71c1d32ae393`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Tue, 25 Feb 2025 22:17:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:1eb0b36109ac529ab5d5db4ea880cfd63ed514d1f542c8bd20a200d73207ed8e in C:\nats-server.exe 
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 25 Feb 2025 22:17:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464c91c36773a1621c7277522f95c645dc9866e58b0867242b34277fc4145ada`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0903b195c823336fbd58a8a52901057cbde5d4f8e8a3fe8d643f7f0b1008ee5`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 6.0 MB (6044491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a624018395b9843449197873a8dfbfcd7cc07efd09eb9f5cb1fe8b5638255438`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbf5f27ca2dfe7fd5ede70769269354cf7852fe304a1af5d4b7bd17e201a74`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0a43a1bf148b020d83f3b26345be5a7f7cdc277350321ce4ad5a4e0fc73662`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3091f851d62e9660edca35a087ab74e6ce5c1ab16cd2dcc10c87c3b1e04be8`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:e37f384db2351a1bb09c1e1640b7571e012bece8e5579c2660ec07bf788b53ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:6a4cc4d864f9bac7dc07b623679bf121113d41d21fc9b5e640e3c92fca1e5111
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112965803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0766c346c8b6c207312a07351709a6e4da8cd036fbaaa8c380d71c1d32ae393`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Tue, 25 Feb 2025 22:17:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:1eb0b36109ac529ab5d5db4ea880cfd63ed514d1f542c8bd20a200d73207ed8e in C:\nats-server.exe 
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 25 Feb 2025 22:17:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464c91c36773a1621c7277522f95c645dc9866e58b0867242b34277fc4145ada`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0903b195c823336fbd58a8a52901057cbde5d4f8e8a3fe8d643f7f0b1008ee5`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 6.0 MB (6044491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a624018395b9843449197873a8dfbfcd7cc07efd09eb9f5cb1fe8b5638255438`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbf5f27ca2dfe7fd5ede70769269354cf7852fe304a1af5d4b7bd17e201a74`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0a43a1bf148b020d83f3b26345be5a7f7cdc277350321ce4ad5a4e0fc73662`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3091f851d62e9660edca35a087ab74e6ce5c1ab16cd2dcc10c87c3b1e04be8`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:d86599f6811aae07be1c0b2b2955d47bb3df8dcf86c1d9fcdc080746829bfe9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:ab30601c4ae2e5de749e7e013dbf1bc8c5f948795d9ba14dfda2cc484f87b552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5923576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736726958d6b2f0e21680f7a56521500766540e90084a54a726a2672e345e95f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ea1d4d1eef4999bdc608bafb79b4807c2e0d126548d7f7d6e3a9b542c153bab`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.9 MB (5923068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8394405f954a1600ce69d033d4616992e140b23520ef911b5e8cb3c9fe0a0bab`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f6eb9f0ff1ba7f1080413295e1bd058a3eb8eaa6346a04ce30d9b12633f178a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5fc4acfc4fca3421337954440d9551afa9681b105c24998d64a27f4f385456`

```dockerfile
```

-	Layers:
	-	`sha256:41f7e4d13b7d0cafe62fb08f772bde421af4e46d7c80aa8051eada0b71e2d6ad`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:a37f3705ca4f359f2cd688f2f2915c89396f3242ed0017031b1d1ac86b929f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5587283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa848ded2e7f822233d14d085a59458f091b55a5caad5800e30d9759389aeac0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7931d39fd2726f7116d27b851850cf4a1ff6e69fd3de1ed621bfe728eaf4c32`  
		Last Modified: Tue, 25 Feb 2025 19:16:31 GMT  
		Size: 5.6 MB (5586774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526621f9915e8bc26b6f41cb0b4ec86f849a2f797e44f1891bc4ec17549827f4`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2fc0d021712bbbf87403b2efb33aa02fd447167450cd57cbd42e75ddc5fd29ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6710a8bb2aed7e8414816e8dedcb63a21a481320f77bf39efdf73bc7bb11668e`

```dockerfile
```

-	Layers:
	-	`sha256:92236e3a37db849c42f54749091d19b6ef1c03b5d1c5d1bf501fe9ed7360131e`  
		Last Modified: Tue, 25 Feb 2025 22:07:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:da5d81783ddfc4e6e5ea9c7e9627dbae2052e148b0ca4c3a5adf3e8cdf5881a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5577156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c3470f5d2f8c4e3cdafea8433db44a91110f01e60967c2a3a8d978e31baaed`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0cf7641a4057a532da4f664f9cec79f7fe56c198bb9e71bcbc2c19bb907c58d5`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.6 MB (5576646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3463297bf29a5bbf37928948bb32bb57b1741d42493f2ae75ed53175a517af`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8be21b20d1b6e3d2e901bce12f29bafce42afbbb1b762be62bfc195cb7e9b3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3610a7ae663a5ca8c8be4540df39767d306086365de3263700ddcce895420387`

```dockerfile
```

-	Layers:
	-	`sha256:234087f90831097305eb3b9065da97b803a126593235b546269cfbfa625f608c`  
		Last Modified: Wed, 26 Feb 2025 04:31:23 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1ab5a26d1f1b792832dd7d52e60d8f57fdcb0ae690e943d796b2b3dea26599c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5471384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96361ef0a1d425f77a7d5bf22cccb8ab926a283d25551390017dcc936f8d6ddd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:34a7e29168d12cc49e3fd1454925bc4b2f10137b37fb10cc85f3b76f5e2959b9`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.5 MB (5470876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0851ead742e7b3af0d74476f1e7610234b00ab6bde066faf665277f50cd3c4c`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4424673c4c02b57552cb838402189f34638ab966b9f85359bad2c59ee9ece0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68e730f04dffe04ac9fcc8af9491ae6be3a7b9be23078e4acc7d0f36fb24ca`

```dockerfile
```

-	Layers:
	-	`sha256:2f7c0d301103a7e55953e57ee1a1660e241006b0b659cffea67752432c2b5ab2`  
		Last Modified: Wed, 26 Feb 2025 00:54:54 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:1bb4f59414ad9587da0bb4e32ff196ef02914c7e8225b5f3c1a3b79e521de195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5434760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ad4a1f1ab680fc057eaaf6c15371c9fda97d7ac3fa04092cefc46564cceb59`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3821b02a9a90c20826ffaffe25f12d7283677acc84047703af05ac61729fd3da`  
		Last Modified: Tue, 25 Feb 2025 19:16:34 GMT  
		Size: 5.4 MB (5434252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a956e9b697668bf98cbe2a5ec65f9e9c0368945ed81d9e43faa5d064cf6cad4`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e7bf236217d62b740ceeef3cf7150a2b66bf5c247d8d6ffbd991288ec58f799e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe4ef235be79096172af5671be15debaba38653149f5fe74fb76d2c59390183`

```dockerfile
```

-	Layers:
	-	`sha256:baa43bb7d01b88047f62ca6dc61952a118a1bc2c2a3222dbd65a322a26523d7d`  
		Last Modified: Tue, 25 Feb 2025 22:07:43 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:84fbc6a0d4f3a6242710d3ea5b8ab4578403aa53d8a5302026bdd6ff20ced27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5777700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcaaa0f666e7b95fe6b20c8bbd70eadf8213e2790de894c72c9f7aa30939f4f0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 Feb 2025 19:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 25 Feb 2025 19:15:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 25 Feb 2025 19:15:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 25 Feb 2025 19:15:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 Feb 2025 19:15:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46891594ec8b4d3680a1bbfe2877deba49c42d5db2b71635cc53e7a260da8759`  
		Last Modified: Tue, 25 Feb 2025 19:16:32 GMT  
		Size: 5.8 MB (5777190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642410c76d1bbecfc24938ff297ac86ca1a30d14e8ab6ef3e9beb0decbbb955`  
		Last Modified: Tue, 25 Feb 2025 23:28:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:192747a24178676ee22ac82db357523716ac68b38738fc729a9044432e7b8815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2f83f8a72ce10467cc585601118bc7a449b8d32a56af2df1c019124dfe4ecf`

```dockerfile
```

-	Layers:
	-	`sha256:841b5965931663c1f16aaccf610709337098323a7168962634fe4bed2d16175f`  
		Last Modified: Tue, 25 Feb 2025 23:28:06 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:68de8391f116e75689a8894608af44359d970ed0f73f652cc4f64667a5974762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:f9baf586a7d5a24f77abdc3e1893d5742cbb2a8727aec3f00c4d2c65084ecfbf
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2143633528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4da431eb1469f157d1feecdb9b465288b0a748b57532bb21fca3548c57614c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 25 Feb 2025 21:36:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 25 Feb 2025 21:36:36 GMT
ENV NATS_DOCKERIZED=1
# Tue, 25 Feb 2025 21:36:37 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 21:36:37 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.26/nats-server-v2.10.26-windows-amd64.zip
# Tue, 25 Feb 2025 21:36:38 GMT
ENV NATS_SERVER_SHASUM=e1f9c4eee642bd521878dc493de8514b25c1468e3f2420312aa52f96f7bcbabf
# Tue, 25 Feb 2025 21:37:18 GMT
RUN Set-PSDebug -Trace 2
# Tue, 25 Feb 2025 21:37:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 25 Feb 2025 21:37:36 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 25 Feb 2025 21:37:36 GMT
EXPOSE 4222 6222 8222
# Tue, 25 Feb 2025 21:37:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 25 Feb 2025 21:37:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2962c26ced92b9e3c7f5d7aebd4559298828b0ae76a0527bf5464eb8c93c00`  
		Last Modified: Tue, 25 Feb 2025 21:37:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32fccbfd6adf85f404d7d84d70587914a6f99fa5e496abee390614035e0c64`  
		Last Modified: Tue, 25 Feb 2025 21:37:42 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990ef8a50ae119e863c3a1547280197e5983c7b6ddb20783b3dd54628b42f904`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afc88e2f571205bcf887d86513344166fa69e24de8659740f8ad26cd9154a06`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73a99f6d11801b46659a585416d0f1f7fca41472d4acbb2d75b754d570f102d`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14def5a308e7ba00beab57e8d0a555e41835d6a7e1fbe73f8cd629e61bbc8412`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 326.1 KB (326129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a913fc4a516e6de7ee8ad909be1db22fc51317f9f677a7b0ec983264959dacc`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 6.4 MB (6386222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4701a610edc58e425cad5c3761df38b0f91e54ade7cffbc439cd6a221370ad`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1170eed527f5197ddf382cc34947fc054416200276965d19eb7f138c222ac3a8`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5f193df96420bf97804f7057740950b173da86fd7c1f79a5f50160154ce512`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db71a5d16206f50e02aa99cc42ce61d770468b7173c5b885ee1d5516f74682d`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:68de8391f116e75689a8894608af44359d970ed0f73f652cc4f64667a5974762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:f9baf586a7d5a24f77abdc3e1893d5742cbb2a8727aec3f00c4d2c65084ecfbf
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2143633528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4da431eb1469f157d1feecdb9b465288b0a748b57532bb21fca3548c57614c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 25 Feb 2025 21:36:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 25 Feb 2025 21:36:36 GMT
ENV NATS_DOCKERIZED=1
# Tue, 25 Feb 2025 21:36:37 GMT
ENV NATS_SERVER=2.10.26
# Tue, 25 Feb 2025 21:36:37 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.26/nats-server-v2.10.26-windows-amd64.zip
# Tue, 25 Feb 2025 21:36:38 GMT
ENV NATS_SERVER_SHASUM=e1f9c4eee642bd521878dc493de8514b25c1468e3f2420312aa52f96f7bcbabf
# Tue, 25 Feb 2025 21:37:18 GMT
RUN Set-PSDebug -Trace 2
# Tue, 25 Feb 2025 21:37:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 25 Feb 2025 21:37:36 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 25 Feb 2025 21:37:36 GMT
EXPOSE 4222 6222 8222
# Tue, 25 Feb 2025 21:37:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 25 Feb 2025 21:37:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2962c26ced92b9e3c7f5d7aebd4559298828b0ae76a0527bf5464eb8c93c00`  
		Last Modified: Tue, 25 Feb 2025 21:37:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32fccbfd6adf85f404d7d84d70587914a6f99fa5e496abee390614035e0c64`  
		Last Modified: Tue, 25 Feb 2025 21:37:42 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990ef8a50ae119e863c3a1547280197e5983c7b6ddb20783b3dd54628b42f904`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afc88e2f571205bcf887d86513344166fa69e24de8659740f8ad26cd9154a06`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73a99f6d11801b46659a585416d0f1f7fca41472d4acbb2d75b754d570f102d`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14def5a308e7ba00beab57e8d0a555e41835d6a7e1fbe73f8cd629e61bbc8412`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 326.1 KB (326129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a913fc4a516e6de7ee8ad909be1db22fc51317f9f677a7b0ec983264959dacc`  
		Last Modified: Tue, 25 Feb 2025 21:37:41 GMT  
		Size: 6.4 MB (6386222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4701a610edc58e425cad5c3761df38b0f91e54ade7cffbc439cd6a221370ad`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1170eed527f5197ddf382cc34947fc054416200276965d19eb7f138c222ac3a8`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5f193df96420bf97804f7057740950b173da86fd7c1f79a5f50160154ce512`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db71a5d16206f50e02aa99cc42ce61d770468b7173c5b885ee1d5516f74682d`  
		Last Modified: Tue, 25 Feb 2025 21:37:40 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
