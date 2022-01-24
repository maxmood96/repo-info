## `photon:latest`

```console
$ docker pull photon@sha256:d2615d7b294f776388993384bb3ad2b1a2286273bc4a412bd5d0bd6ae8268fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:1fbd2e67398230f49fd92bdb4d925a0acddc22b276d90287e46dea76a08362f4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17533167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d7cd763b3ddd1bd57b33395ecf0d7f657ff0a0f89476155fc56354cd3a993b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Jan 2022 02:20:04 GMT
ADD file:69cced27e5a291913a99f654496c11ee1005c65d26b23bd8aa360ded21cf658e in / 
# Sat, 15 Jan 2022 02:20:04 GMT
LABEL name=Photon OS x86_64/4.0 Base Image vendor=VMware build-date=20220114
# Sat, 15 Jan 2022 02:20:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:db3bd88ae7a547d9d850f257ecadb732b90b36dbb6241a8b32e7b0fe080414af`  
		Last Modified: Sat, 15 Jan 2022 02:20:35 GMT  
		Size: 17.5 MB (17533167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:dd217cdb8709f985b0ade02363237733c333e9e0c9c765b411a381c3daa469a5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16537626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c93ba2240cce732aded2b61b8cd540907382b68bf51af4dcf2eb6d9b9619e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 24 Jan 2022 18:40:40 GMT
ADD file:309a260f9d5ff3f86a96c283afd15bebb58b1c8ab3a7eafec9ffeafa42f13a9f in / 
# Mon, 24 Jan 2022 18:40:40 GMT
LABEL name=Photon OS aarch64/4.0 Base Image vendor=VMware build-date=20220123
# Mon, 24 Jan 2022 18:40:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3bb90232ab06e103c030543fea1bf8a1033f4a9ece70c5097313e9011a2cc816`  
		Last Modified: Mon, 24 Jan 2022 18:41:11 GMT  
		Size: 16.5 MB (16537626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
