## `debian:stable-backports`

```console
$ docker pull debian@sha256:54df9b9938d85e1308c74f1666238783fdcf926a1233103c4110fe1b9a6aa832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:0a65ebc8abebfbd4fbae3e27eddef4f6c5a5490d89b14ae60146dce2179278f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55038852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f001b6e3e386bcc3774997609f4737d6d88ca2fd9c88f6ab14c13f8e3b24512`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 04:06:00 GMT
ADD file:c4fbd3ab46680998a74e7b05106e844b092e14d03bd08140394fb19f7c0be3d4 in / 
# Tue, 15 Nov 2022 04:06:01 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 04:06:04 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f1ddc4dbfb7e4f9007800195fc0e219b7a85f4ce9f36f6d82c4061b5903baed2`  
		Last Modified: Tue, 15 Nov 2022 04:10:43 GMT  
		Size: 55.0 MB (55038630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd1cbfba7769f68f105c6884ab821153a309bdea9d89a36ab87df49fcf80cc8b`  
		Last Modified: Tue, 15 Nov 2022 04:10:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:00947d85650d27d8daebbee3fb187f10b7540fbd2594837c5ef92bcd1de3d337
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52542495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8bc7257961e1190e0549d7ad01f61d2fefbd84d9da8828eb05d90e5bfc70cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:49:54 GMT
ADD file:c56a16ebd120c9d2448913e557242a550b39af10b1dff83cdf69b36f72c1e6b8 in / 
# Tue, 15 Nov 2022 01:49:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:50:03 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9eb727b769b056f5d53ee8bc52c01d2580cf7c5d7ae2a28c5dfd887b410bd983`  
		Last Modified: Tue, 15 Nov 2022 01:55:26 GMT  
		Size: 52.5 MB (52542271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c3c27bfc8ae6c0f567407066592467ff01a51f366b18518492baac5922d7b6`  
		Last Modified: Tue, 15 Nov 2022 01:55:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:80c11e999bbf1051788cea905b9f8c18307e7a0f484f237f934edf4854ef2b58
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50206587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea25b4733f6ee8123be4640ede973626a5101fac8ef2ae84ee39d1a249ec0f3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 03:45:06 GMT
ADD file:1dd559f159b86594b9a6d7c63096d122d817868b9e8a5d27675c3fc631a960ab in / 
# Tue, 15 Nov 2022 03:45:07 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 03:45:14 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a016636191734b76a599d70b2848e0a21a713eec24912dd841c8e08ffa0d07e1`  
		Last Modified: Tue, 15 Nov 2022 03:52:36 GMT  
		Size: 50.2 MB (50206362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc7cd067ce395608b9725ee849df1ad01ab91bdda1ff5670d024eadfb0394d2`  
		Last Modified: Tue, 15 Nov 2022 03:52:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:3303300abfa32958f7b0492cafe07c9458a05b2deb165ec78220a80f4bca67cd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53700099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8aa7a2f2576752924da0fb2008c43a615d460e593d8feaf29ed86caedd9f2f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:06 GMT
ADD file:cb0f17b5c0cbf03c82acb98a92225ba47d72e4cf6d1039b6760009c2eb430c0a in / 
# Tue, 15 Nov 2022 01:42:06 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:42:09 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fd378029bda450e62dec19ae0ce9ebd20616424f3c6c6d281e8c411594558b4b`  
		Last Modified: Tue, 15 Nov 2022 01:46:24 GMT  
		Size: 53.7 MB (53699878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f0ec656aeeba343138e525e7e8bf229179c2ba2c716e78b1cb9f7230b0122b`  
		Last Modified: Tue, 15 Nov 2022 01:46:32 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:2ef215e5656ed4e6ee6dd2e8721796419bd26c8ad870e9a2f03a43c7efe37bc6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56020913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d964dbdc1eed7fca8dbd7c1bf2bc79e8921d0bb7909f45c28d85cc15c7b0e7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:eb06ac11e2a7b5584c9bb251789605586d29c9f4a4ea0f8415459ce24644c591 in / 
# Tue, 15 Nov 2022 01:42:52 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:42:57 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:58464fc4cc4947d2a30f51c0e0715925e75926341a83c62e773b844642d75886`  
		Last Modified: Tue, 15 Nov 2022 01:49:18 GMT  
		Size: 56.0 MB (56020692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d1b480146465f0f072e0d6fa2138cbacbaa67f1ad1e400d9f2ae92dc8e988f`  
		Last Modified: Tue, 15 Nov 2022 01:49:28 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:cb2b5f5554f05f22d3ebc521613517acdf2442f46cc0120df2b84c61b98b878d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53260629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70ef1731cb946bf5d57d78272487c5833d855b389334411854f1758f6bf81a3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 04:15:13 GMT
ADD file:b8936d98f61b1463e16da2d128d92f3dd34067582b54e6f8e755c45460a07ac0 in / 
# Tue, 15 Nov 2022 04:15:18 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 04:15:27 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a334d86ba4e6a79b4017be1faf7c12199e1850972b859344f2a0ae78618c057e`  
		Last Modified: Tue, 15 Nov 2022 04:23:05 GMT  
		Size: 53.3 MB (53260404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59909d4e0a68277653faf616128e9f3f16c0b9234161081e5ae74b35611cdd32`  
		Last Modified: Tue, 15 Nov 2022 04:23:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:6be808351a56610f85c311092dd23e4e2c5ac6e5f1e63e0c1d810b683dbe366f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58910951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b731f44916ed45c6a6bbed9d1335bb21435880ee462343d63cba40b77d48341`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 05:19:35 GMT
ADD file:77c6279e0e37af898732624971eb4f88b482b32941fe62f7f7eec444e74679a8 in / 
# Tue, 15 Nov 2022 05:19:38 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:19:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1ee232b47de3da422a9d4d3f738701072078686c3c45e51109296ebacd9c98ed`  
		Last Modified: Tue, 15 Nov 2022 05:25:32 GMT  
		Size: 58.9 MB (58910729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0550832745a9a9ea26cff31d94344985d2f52f7f43a4a164098dda0f4f3b6bbd`  
		Last Modified: Tue, 15 Nov 2022 05:25:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:bbabe850809bad5a5ecfe10aab79b2030562b75231e7d3294fc5408ffb7f2bc1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53271844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8740d90b5b3dc12c9491178eabd93f77e533bb0b607f4e62e3af6ae10b41bb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:43:38 GMT
ADD file:090f7ef0a67db6d185481df06803e1bc2ae6f8e0f6c47c49ecff6babfb423160 in / 
# Tue, 15 Nov 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:43:49 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:06734e3d172b32fd981d96e3a709fad21580728f847d74f9406cfa3231177d2c`  
		Last Modified: Tue, 15 Nov 2022 01:48:14 GMT  
		Size: 53.3 MB (53271622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c8013459fcdb3eecbab58141227533d44b3d5548c9472230488492684fbac7`  
		Last Modified: Tue, 15 Nov 2022 01:48:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
