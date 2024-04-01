## `photon:latest`

```console
$ docker pull photon@sha256:c99317b045c3bfaac279aae93e8c9e1d86ea3f964559cc92f40b37d0c074aa25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:9715c4839181ed92ddb8308fe785748ed5c20ef15bc949a2fe73a51893988bed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15986391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4764967061f10c47a52c5912b8888c9e8c586df1b5152cbec2c3b2569499f0ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 01 Apr 2024 17:57:03 GMT
ADD file:15bd4261b8c6621c37e4236a300fdf484160ae263249b1c516b79af6e45657e5 in / 
# Mon, 01 Apr 2024 17:57:04 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20240331
# Mon, 01 Apr 2024 17:57:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1c947763c863d93d79007c5f3a46b2ecd9cf224e2812cd61083fa2e821b315a1`  
		Last Modified: Mon, 01 Apr 2024 17:57:21 GMT  
		Size: 16.0 MB (15986391 bytes)  
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
