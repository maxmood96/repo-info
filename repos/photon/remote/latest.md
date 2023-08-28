## `photon:latest`

```console
$ docker pull photon@sha256:b5ac63a7f4d5374b8321cc8d75b1bba93a21058676ca2cdc7ee4c417f4e0a87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:5fa5436238c66678d413aaca7da6d228100a2ec54727a4b7b1106691f61dd3a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15923202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9d826a161c96322d1496cef5290aba054eee5bdfa750fef1f85f6c62521b5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Aug 2023 21:51:10 GMT
ADD file:127afe00460514a4e7e201c524cb1a3a05dbbcd2dc5e81d694849aace54b337e in / 
# Mon, 28 Aug 2023 21:51:10 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20230826
# Mon, 28 Aug 2023 21:51:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f04330c343a66e1c3216903951fa736b9e0be0814c1bcaa274b9589d3cd5f489`  
		Last Modified: Mon, 28 Aug 2023 21:51:36 GMT  
		Size: 15.9 MB (15923202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:a51ab1e240df3a7a1390a225aa0c2f0aee422b96dc95bd1d60f2615850e63263
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14929499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece71ad42c3f7f2aa11531d8b0f7b36dc226ae2a927e10d75f66b471f4e8b170`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Aug 2023 20:27:14 GMT
ADD file:f2b6eb3fc1c93853dc60d29b62e2de6c76a0f71b28db68392a656b10d4ddcf17 in / 
# Mon, 28 Aug 2023 20:27:15 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20230826
# Mon, 28 Aug 2023 20:27:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0fbf17b4b6de782f8c9924a2b1a2b466db7e2b97f190563ec327f8cb3f2f1717`  
		Last Modified: Mon, 28 Aug 2023 20:27:35 GMT  
		Size: 14.9 MB (14929499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
