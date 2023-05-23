## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:9ad22cabceb35168308de0fb5ae32d1a2abb4bfee9989db6ec991619390ebf89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:85e201cd4b5e9a0661268899fb766cfbc905a3060c5f30c70b108837778aea88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50448926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b210fbc496ec238bad459f5d6616edd65acfa1e1c37941f64c01276471bc252`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:25 GMT
ADD file:4cb930e9734087a901749e455f5244654b460a84b00eed90eb1d9c2291bc164f in / 
# Tue, 02 May 2023 23:47:25 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:47:28 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2e82f76fc41ab7d9e1f846f491035ff27c2662e3d9df1310f7a469aa044f641d`  
		Last Modified: Tue, 02 May 2023 23:51:18 GMT  
		Size: 50.4 MB (50448700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be48503b426423d15697b120a1cea6fb2a6e9fb9359b3d777c0b409c158ef390`  
		Last Modified: Tue, 02 May 2023 23:51:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:1179c1e78e5bf235b4d68d7aa1a3776a08b6e1c05c234b3f8f45ed52b58c37d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45916741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c418eceed6b6b67322929efdb000a509c0444ac744937de11a48a6a41f2e47fb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:58:28 GMT
ADD file:c01c1e55a32cf16d6866f2777cdab993547c9d3146a52e544ca51a9ccc509943 in / 
# Tue, 23 May 2023 00:58:29 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:58:32 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3d19d8a6bda91ea2f74badb378612f4de79d44843359fa77b6729117c91e2909`  
		Last Modified: Tue, 23 May 2023 01:02:41 GMT  
		Size: 45.9 MB (45916514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c978153a76e0579feffa366aeefa92aece7ce510744bb38c66577f6d75b1cde`  
		Last Modified: Tue, 23 May 2023 01:02:50 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4e0ca308da5db1e24a4049423965b0199fc0781d988a1ca792257f5d140ca7eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49238531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5771dd59823d24df83de6b00702d43f8cfeff9ffbad9e55a49ab06e347e5414b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:34 GMT
ADD file:2b432f06d80368a0aa70a57bcd07324e818b6b65b1336463e006b3cceeec5b02 in / 
# Tue, 23 May 2023 00:43:35 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:43:37 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:44d886d3df364a0fe6793fd29d8ba173862fda98799b137e777715ec187529dd`  
		Last Modified: Tue, 23 May 2023 00:47:00 GMT  
		Size: 49.2 MB (49238306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a9318c0b6e4f22781a456e41571949f5555b86d27b09b516fe6fe7cb942e74`  
		Last Modified: Tue, 23 May 2023 00:47:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:18dcc41fec8ade13c438d785b2cec1944fac2a2e95d255507d721f59181c6e90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51205887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60a63feab02634dec995df892b89aa5224d36e77449a361c3acf47a355abad1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:40:16 GMT
ADD file:f325a21337c4f12d2e4d33e79575f5def109973d55be6718dd79cd88d2f1fe90 in / 
# Tue, 23 May 2023 00:40:17 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:40:21 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:61be7484f153c0c17d8706c487d19cc83c629ffd8202911ed497d1b6b6bc7d3d`  
		Last Modified: Tue, 23 May 2023 00:45:33 GMT  
		Size: 51.2 MB (51205663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6378eb9d571d3a8b41ef3fa3e8d27649853fa60b5cf98dea48472a80ec586b61`  
		Last Modified: Tue, 23 May 2023 00:45:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
