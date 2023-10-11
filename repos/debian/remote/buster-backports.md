## `debian:buster-backports`

```console
$ docker pull debian@sha256:bd9a9b50a0fbe2b28fb7a9346b84eda250e024008e6a0e0021a878f285c703ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:f3a511b47f2c0a7d41a53d1360680e4f5881d4112329c00c817100961c48c602
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50499622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bba45ebc5dcfa4ce50a12bdc6e6474acc7cf72105103f6633919c2f278143d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:23 GMT
ADD file:1efe9845e057e7029a1c2c26c148e6dc1bd9c65d0cbbb23cb49c86295d1f1f48 in / 
# Wed, 11 Oct 2023 18:35:23 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:35:28 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:99db33be616a9a2a0b0b1bc913b548317bab7bd11cb6968d357457e201c44077`  
		Last Modified: Wed, 11 Oct 2023 18:40:37 GMT  
		Size: 50.5 MB (50499400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580d82265e7310a04e2257cba87f28ca59c40ecd98024e979d71d6f04860db71`  
		Last Modified: Wed, 11 Oct 2023 18:40:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:ece761e4b3a61126a8c7bab94f5b3298cccbc96a8f2c1c2fc0552568d819560e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45966576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d6ecd9faeb11c3ac91544267acf48e4e03c813a6c78c36981096febee2631a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:37 GMT
ADD file:90492dd68d097af40a6208353165e1b7e2bc04a31cd2270232e085416f6e940e in / 
# Wed, 11 Oct 2023 17:42:38 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:42:41 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2ecd2705b9dde659b853da74fbe8d7227d02acd96f1d34766d44193b82468b37`  
		Last Modified: Wed, 11 Oct 2023 17:47:27 GMT  
		Size: 46.0 MB (45966353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c7277fd2e2c97e576f9c891f54b79826e08a712630034fa8d7814866b73d07`  
		Last Modified: Wed, 11 Oct 2023 17:47:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:cbe3586a5022b84609d6eeab5502c72405200fa5c6e31529e5ab1b9ab870e799
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49291311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b7a444fd2596797d2454aaa67b9d6044016b821cd1a5587fe15fc332baaf10`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:12 GMT
ADD file:d97d8c89883987c89b2150923abea982086030e71970f5473a534e95252b4972 in / 
# Wed, 11 Oct 2023 18:25:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:25:16 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6a7acee270b8289bdc6bb8836f1a4899f794d60337a0cdc46b58a717bd27ba89`  
		Last Modified: Wed, 11 Oct 2023 18:29:25 GMT  
		Size: 49.3 MB (49291086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bf9a13532a291366328749119063db5816e6cf7b46dc382f56ad94d819e0a2`  
		Last Modified: Wed, 11 Oct 2023 18:29:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:e427385be52fbcd45a1ec54cf7c504a08ce12ff411d8dd24817a2fd1d04feb26
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51256296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bb61c0041b6e5420ffd7d27640fc6bc4c4cd2ca6e3b91b9f127a0897b6483c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:41:14 GMT
ADD file:47cece2eff96bf7383dd2a9c5632f0ad7bb31b3a459677530f77a78e22658e98 in / 
# Wed, 11 Oct 2023 17:41:14 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:41:18 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:62bc68699d611f4c048328a0468ebc10de528260c7823c8938796da30db31a17`  
		Last Modified: Wed, 11 Oct 2023 17:46:45 GMT  
		Size: 51.3 MB (51256071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f86b1e43f0734ffa16e319109f07e32b13b868c1bff5f71a082c31c12d925a2`  
		Last Modified: Wed, 11 Oct 2023 17:47:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
