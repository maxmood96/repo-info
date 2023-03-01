## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:e0c068fe39509bac5bbfb9474a5cfb9cb0a3e0ca12f9d68712d2041bc23a1501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:492309f2537f326af582de9301907b6155756f0045a8d04cf3aa7804d692a4fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50449323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e52e8b373b0af5e8e8a48f3c5c8c8fdaff7a31cc1aeb89d81ec29352339acd9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:33 GMT
ADD file:12083e75f80fb6bd621143c2eb98ab9ce4dfe1b28b3cde8a86dbc6bd8e4bc7bd in / 
# Wed, 01 Mar 2023 04:10:33 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:10:37 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:555942b702dc4f48a84a3d5d879bbeabc861fb4e7f24cdbd5384c4aea9dfe591`  
		Last Modified: Wed, 01 Mar 2023 04:15:23 GMT  
		Size: 50.4 MB (50449095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f306f771e7004b146336f5eaabe69cfc92544070412973d1c1532825f710dbf4`  
		Last Modified: Wed, 01 Mar 2023 04:15:33 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:34b7941b50ec36e2639b99b1de127c9a26ff694efc40e8e183c4a4e440b30699
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45916306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d52d5909bff9a48e8bfb27887fd4f0ca72a8930b61e64ba66dd6dfb99f84e9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:58:21 GMT
ADD file:ccafb0d4746567d93ef1a3ac27400488eb9d41acb93e3a18f1e77377ff97c8f1 in / 
# Wed, 01 Mar 2023 01:58:21 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:58:25 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:548799b11fde653a3d163dd7bb5426257f268b7c2b7133518be0cd64df798a73`  
		Last Modified: Wed, 01 Mar 2023 02:04:13 GMT  
		Size: 45.9 MB (45916081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10367b73896194527344a35e5c5fa3746f93197523f34ef9b1c66a6faba22c22`  
		Last Modified: Wed, 01 Mar 2023 02:04:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:e933844f3fedff1eb34d732d82c50b94af343fa3f594b9d67420861d8bed2849
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49240231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe2d4a15e43b3fe9aeb10949454b84ed03ee547f2470f5ce97d9fc2b72ad968`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:21:03 GMT
ADD file:d30c63a27172705fbf489d5393d7c5c2e1e89d8243e39b9eeef4ddb8ec9c7fba in / 
# Wed, 01 Mar 2023 02:21:04 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:21:07 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:eb7717bd039c193f3eef114c67fef1b76e73860d00d322acef59019c6c561a60`  
		Last Modified: Wed, 01 Mar 2023 02:25:13 GMT  
		Size: 49.2 MB (49240003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a92d766846ffbbab94fd3f24ac9bd4155c7be330057a44bd1434c44f01bd9fc`  
		Last Modified: Wed, 01 Mar 2023 02:25:22 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:5c84b108adc339d7d5a956e3967ebc6f03bf7fe6ba55d217eb9f4ac118ae75e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51207594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1056e4c655fa99d313bcad7fa44b70590c4202e03d56b7ec9e2756a5276dada`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:44 GMT
ADD file:ba1f3b4548523bc0d8aa4ed5bbe6fc6bb29fda65a8fcc8c60ef142590b253f83 in / 
# Wed, 01 Mar 2023 01:39:45 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:39:49 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2feb9b8f3b71378feaaaa0653ed32983eb258b997f8ac24d01093bc3d1a25c0a`  
		Last Modified: Wed, 01 Mar 2023 01:46:01 GMT  
		Size: 51.2 MB (51207370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846ed57e711eec887a1071d8aaddc50889c1b0994c486fbfc4443503eab225f1`  
		Last Modified: Wed, 01 Mar 2023 01:46:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
