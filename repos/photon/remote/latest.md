## `photon:latest`

```console
$ docker pull photon@sha256:722c5fabeecd2dde9b674adfc3e2d9030d2abfe423f832c7db6863fc6c64cd69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:e069b45d18067e10b09b2a2ed35937591c4b907c3d1b8792f45ce394bf7b57b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15987469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:158e07912150ddafc8dfffaa5dfe9694acec0848d1169ad47508e4f3910cb4d8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 01:06:36 GMT
ADD file:9ac5b81d6fd8562e629d86774fb5f82b0cb4ef320e93e28ec8d9e4d2bc31fea8 in / 
# Fri, 12 Apr 2024 01:06:36 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20240411
# Fri, 12 Apr 2024 01:06:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5c70ea440659879175df459899240174f44dc78d22e7ee5724f551ea864b7231`  
		Last Modified: Fri, 12 Apr 2024 01:07:01 GMT  
		Size: 16.0 MB (15987469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:96543e03810f31f98a459d130931e2a0fc78ca77cf78e659defb2601a363df22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14974158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487edc50ebd83b7d10b15b70fbf0b3cfe0441d86814c8417e8c3a1e6e13522d9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 25 Mar 2024 18:48:57 GMT
ADD file:b34565002143d0bfaad2bbc79a55ae57531469e383a03357cc96943c08d55665 in / 
# Mon, 01 Apr 2024 18:12:02 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20240331
# Mon, 01 Apr 2024 18:12:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cb1133252202ea1b0e62801cb5fef81dfe23bd52d6f5708504d01b39cf774890`  
		Last Modified: Mon, 25 Mar 2024 18:49:17 GMT  
		Size: 15.0 MB (14974158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
