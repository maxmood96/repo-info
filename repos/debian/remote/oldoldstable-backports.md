## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:990e6a0a250304ffb6114c08afafbc56e115d6890b437384e723590b2f6dd219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldoldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:6cf5892664f1b722a0bc8e19c47fd96a4ab159d624de66a22bd863bf2efea5d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50448771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8e98baf0782e7e760aae73443874a861434bdd3c6c8c09c3a3cc0a9e3d8271`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:44 GMT
ADD file:88ea278ee6d3a91699abcaa45e03a772a8680792810318c411122debafb13ad9 in / 
# Mon, 12 Jun 2023 23:21:45 GMT
CMD ["bash"]
# Mon, 12 Jun 2023 23:21:49 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6d3a2bf6b853b9d5e48e2c40bf6dc4ac611e4431b6181940624ce4f2408aaa2d`  
		Last Modified: Mon, 12 Jun 2023 23:27:26 GMT  
		Size: 50.4 MB (50448544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ff5df54e0998b1db51bd8e50f9b394c271b28aa89a1d02ad0d7919058afe5c`  
		Last Modified: Mon, 12 Jun 2023 23:27:34 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:480b9d3fda3fc5b1c8adf5d4d99fea535a86d81b5e87ad406fb269dfe56b82c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45916311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed4a746927c0da82291832f83eae79b4131e96db9b7110925b3587193a8b939`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:59:34 GMT
ADD file:79e23e8b1992d0ec28699da9cc7669215f5a1e6a0049a313674c95889c1c68b5 in / 
# Mon, 12 Jun 2023 23:59:35 GMT
CMD ["bash"]
# Mon, 12 Jun 2023 23:59:40 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0bdceec0a5f15568de21cad120e580d2f3987d491d15eb0c4e0cc76f7c0b046c`  
		Last Modified: Tue, 13 Jun 2023 00:05:24 GMT  
		Size: 45.9 MB (45916087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3aaad7fd0cf2eef159974a86318ecaf444776fc30c73049a700a6d60f8e4b1b`  
		Last Modified: Tue, 13 Jun 2023 00:05:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:92a6846b9f5dc4f8c39e012db9ccc6b6f0fd9e98fcb8421ad3e115c5868a302a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49238650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9f32baf70ffc449e8f2195a0f3c38e00f1ceb962685497d34a0452badf836c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:41:01 GMT
ADD file:e2942c977c101539f35f37f69e020802ef763ca33d8ef4ffd4bfca8f5cb496d0 in / 
# Mon, 12 Jun 2023 23:41:01 GMT
CMD ["bash"]
# Mon, 12 Jun 2023 23:41:03 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:023125a50c120c98a11d445d8dc0121fa2823e4f053e7c98b2d61b97b9a2012d`  
		Last Modified: Mon, 12 Jun 2023 23:45:37 GMT  
		Size: 49.2 MB (49238427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5275cb97965ee9ad2241db6b71fc491c7754588916460fc848f53ac95197c3fd`  
		Last Modified: Mon, 12 Jun 2023 23:45:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:982a1dc77be9aabf0ead3de931492413d41282f4f57108027f8e36dba1caf723
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51206223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9774975734b7bfb1d346176bbd6cf912fed5d2405058fdc0d39beea2040c2d7c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:54 GMT
ADD file:c1185fe141b862f97bde1607c0ac6b9f6243d5d7a763296a82c72466de9e9c28 in / 
# Mon, 12 Jun 2023 23:40:55 GMT
CMD ["bash"]
# Mon, 12 Jun 2023 23:41:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cb5c8a7aa1b433e8ef99af81a22f654ee247118cfc32f82f86af969632128bc5`  
		Last Modified: Mon, 12 Jun 2023 23:48:11 GMT  
		Size: 51.2 MB (51205998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90d68062b587693fa848f406f83c7e8a8501c7899b6e99518b6b6bcc8e6b38f`  
		Last Modified: Mon, 12 Jun 2023 23:48:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
