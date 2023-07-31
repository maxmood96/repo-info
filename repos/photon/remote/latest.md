## `photon:latest`

```console
$ docker pull photon@sha256:4e2a6b2197b95607f8caae778a39d01c5ad4db35c1f16ff8cc54427716f4cf63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:1b0d90353bd99cc16c24662a89a1a5bd4d31309dc0d8393f974fbaa15613beba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15922845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176b9b7c816e414648afb18af610b1af85c10f49c50f4a14b7b74d481b554bfe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 21:20:28 GMT
ADD file:fadc402f84e1d5c814507059567da6b0e6754e6b0e0bbd041b19f2f869605a0f in / 
# Mon, 31 Jul 2023 21:20:28 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20230729
# Mon, 31 Jul 2023 21:20:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:549f5d667deb3c7c555273adf34aef5a27841ed11ddbfbe27bff182b711ba404`  
		Last Modified: Mon, 31 Jul 2023 21:20:55 GMT  
		Size: 15.9 MB (15922845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:b8dcd7c9081161a68a42635fe5620f054510e13f44145aab2644f4268b1feb44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14925945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6024ffa0db80a80bc651e22c6470818085c5c1c18ddf24bfac6bf911b6493b3c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 24 Jul 2023 22:07:32 GMT
ADD file:0a19e9073876672f760a6c11e34a17e34cd43fdaefdd0b9299275831a5c6ed46 in / 
# Mon, 24 Jul 2023 22:07:32 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20230722
# Mon, 24 Jul 2023 22:07:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dc75f982711b298db2c6a030ab58914ea755738657486225e12620524fc936ee`  
		Last Modified: Mon, 24 Jul 2023 22:07:53 GMT  
		Size: 14.9 MB (14925945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
