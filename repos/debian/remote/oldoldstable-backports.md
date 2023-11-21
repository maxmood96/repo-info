## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:718f362577f413d33cf3d25e34b71a71b009d7d323135f270ff4659f4efb568d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldoldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:2ed79a0e266b5eae0f93818bd670a9acc8304b4f7043ea168769f242903abc9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50499680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a51cf31f0317b6802db0155c40541ea06eebec68ad3b1ff21e021435a64d1e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:29 GMT
ADD file:a60837c9bce3302172a84bc8ea4ae85b4cac32d384c4d87df499438a506bf23e in / 
# Tue, 21 Nov 2023 05:22:29 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 05:22:34 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:68d0235a7d22f3ed1874fd990f3ffb1117c3891e6b6e4d8639414f711b8e5739`  
		Last Modified: Tue, 21 Nov 2023 05:27:39 GMT  
		Size: 50.5 MB (50499454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b100c4ca10dd379bdd19912bada46348da8576094954dccfd3ad9d6d5fe6ce`  
		Last Modified: Tue, 21 Nov 2023 05:27:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:2458f72456ef1a85117966f6688dbd470cfd39fb94a72fca638a619d755c4211
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45966557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e513140ded15c3bfc97b34daca60da4f68bd05f8769a73f4e66b032db947139c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:58:30 GMT
ADD file:16e24782831afb010e862a2ac0a2ceed2617535dff06e6cd8a091df2c0bbe452 in / 
# Tue, 21 Nov 2023 03:58:31 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 03:58:34 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c18d73f59fce2adf5960353a3a44ed26b5e9c631e434a3979db569ffbde89ca1`  
		Last Modified: Tue, 21 Nov 2023 04:03:41 GMT  
		Size: 46.0 MB (45966330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcab596109d56b969ccb5eb44cf0d2c6b29bf3e608d8fadb21ee147bca050a5d`  
		Last Modified: Tue, 21 Nov 2023 04:03:50 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5cf86b4540423ca769d5980f16964ec4082db82088dc4d70463c2ba5da9958b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49291365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60669c6b7d788fb7852c58b0a6adb5cbf0a4db8080b708100577aa2bcf5604a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:41 GMT
ADD file:364316cc8652a355ab4fefa71b24592bc98d699a652a28afe21661129fd21f13 in / 
# Tue, 21 Nov 2023 06:27:42 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:27:44 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e0245ae6c5766a6cfacf793077439ce09c0bb3eafd1af926871de9ef74045fa1`  
		Last Modified: Tue, 21 Nov 2023 06:32:02 GMT  
		Size: 49.3 MB (49291140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:763b87ffbad2fc34258e76650e9a375c83136241778f2a77a15f99f84a34bad8`  
		Last Modified: Tue, 21 Nov 2023 06:32:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:1baf7f4642a907081c1282ea13dbe4449e579fa0d5b04db3ce7b4ca0da25bfb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51256373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c562a5214e90164e925b9baef094d04cf8805405d34a43d990b965f681c470`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:40:48 GMT
ADD file:31e793a57f0790996fe5a2214acd41429941a3b362aff70d5fd504eada62085d in / 
# Tue, 21 Nov 2023 04:40:48 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:40:52 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:04418c23f29bd4990c6b8fa1256b0c7d50b97b5dac1f1b40d0856bd4ab82ba8d`  
		Last Modified: Tue, 21 Nov 2023 04:46:33 GMT  
		Size: 51.3 MB (51256146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0685d979af90eb07d1103976ccd7db171aa412d6156181eb60d44c49580958`  
		Last Modified: Tue, 21 Nov 2023 04:46:43 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
