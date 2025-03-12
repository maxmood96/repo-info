## `nats:latest`

```console
$ docker pull nats@sha256:736d575e60135ce1d50fc206675d48d0e57dcaa0704f696f0cb4b5f6dadd49d7
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
	-	windows version 10.0.17763.7009; amd64

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

### `nats:latest` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:e9950c9c6cc673857b7a7712a3d573db12e7e187006f6e08e3d25a56eaa009fc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112958008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633c1834299c01890b0d78202d9386be78f2a7b336a4f369cab1701e46058187`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 12 Mar 2025 19:23:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Mar 2025 19:23:18 GMT
RUN cmd /S /C #(nop) COPY file:1eb0b36109ac529ab5d5db4ea880cfd63ed514d1f542c8bd20a200d73207ed8e in C:\nats-server.exe 
# Wed, 12 Mar 2025 19:23:18 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 12 Mar 2025 19:23:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Mar 2025 19:23:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Mar 2025 19:23:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a900dc7d2f26761db67e60cfd79673a3fa72346347629a7e6a79c433d287154c`  
		Last Modified: Wed, 12 Mar 2025 19:23:23 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6920edc5818a3221b8e03e12ac0107cc942f4c1062b51fa335299c40c4ec3e72`  
		Last Modified: Wed, 12 Mar 2025 19:23:23 GMT  
		Size: 6.0 MB (6044474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06128ce0ff01d6dd016e7cdce3e67943afe9f9978eca85b3bdcc44578fe0282e`  
		Last Modified: Wed, 12 Mar 2025 19:23:22 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e933e2d7bff70e4e9f9936a27849b066a0d4e22cf2395793b721c07024c8de62`  
		Last Modified: Wed, 12 Mar 2025 19:23:22 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1406f3920ca5a6c47489049af44bfbe340f0c62aa5ee3d8b40bb9582f4b76fe`  
		Last Modified: Wed, 12 Mar 2025 19:23:22 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd2c18be1553a99b04e76719aa07a6d90045a584a02c7ef86402571d1d75935`  
		Last Modified: Wed, 12 Mar 2025 19:23:22 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
