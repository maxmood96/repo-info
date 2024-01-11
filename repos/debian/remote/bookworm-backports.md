## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:ff24d73ad13ad52ebe2d6bdfb5152391fb5cc88385ed3a533c708c0940904205
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:23b817c96427bf1aaefcaee72a2cd9f56c62455dc710df25f35ed7d0bfba3f51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49561715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62dab75f458e7d67509370ac99278c6b4fc50eaa872d5f682896147dffa6863`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:37:46 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc8cf0b8b4be827b03744286865abe65d82668ea5d7a958fb1c157d06cbbe4`  
		Last Modified: Thu, 11 Jan 2024 02:42:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:f93f9977535bb2c7bad28ef8d7d23b60dcdc3a0c57d7047f0edc79a7d2137fa7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47319300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a77d46d391724b87d34afb68977c245040bd15de54a27320541da4236f7a6e9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:48:39 GMT
ADD file:a0f6aa0cd43d2f5d230b0fc0ff4408d84c08d1f2bb9c4a0b781f38a9be437f33 in / 
# Thu, 11 Jan 2024 01:48:40 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 01:48:47 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4aaad31c96d846308a92a43b3da192033e7d93114975064de59eead39852d764`  
		Last Modified: Thu, 11 Jan 2024 01:53:38 GMT  
		Size: 47.3 MB (47319075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5939551f93e19dddd6f24f05a568878b760774bb6f794ca85758b8975a4e4e7`  
		Last Modified: Thu, 11 Jan 2024 01:53:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b4517bd491e9054bb396888ce9c12bb4738750730f1c6a1a463baf3dc680a502
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45156899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b7f381403481c3d20ce2ab711103620f817c823d24b8136e3a23ec197ffb44`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:52 GMT
ADD file:781c48325e0a88993e9f749e0cd761de39d671e9a23223797cb25431ac40d39a in / 
# Thu, 11 Jan 2024 02:41:52 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:41:57 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1d306580a85c9098725ffcffdc42e708e47695a4be4626d1dc152e55ec7f04c2`  
		Last Modified: Thu, 11 Jan 2024 02:48:11 GMT  
		Size: 45.2 MB (45156672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1a36b93d46b9629ac6e23eccbd9c784d1145c6d333af259477c139381df80f`  
		Last Modified: Thu, 11 Jan 2024 02:48:26 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:74861ba5032c445e4aec1976fbf4000e91d6a92c0ede1304354e73d55e2ade7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49592471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7f39bfbae9224688d4c0ede0862e1506efbf081c4935504bece43af0d531b6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:40:39 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db9e02f6ac1ad8a4c6cc3f9e7a9a8d54593b35ea9c9c522567ec62fae87c14a`  
		Last Modified: Thu, 11 Jan 2024 02:43:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:b665e45c4e18b6186e3f1328d7886c0897400a0e03d92521374dd0a51af935eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50582204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0150ab1716741b5284c8a1a3e412f99bebecf8395764860bdd73e6f374eb98f0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:28 GMT
ADD file:c7cf48f483b7eba0a82956c5ef1a1c78e84c2b91d0b9cf17fdfde5b756fcba9f in / 
# Thu, 11 Jan 2024 02:38:28 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:38:32 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:348e22f3afa19ef4ed67af4c0a3dfafe2c1311e99bde0b9039be46cafd8069f8`  
		Last Modified: Thu, 11 Jan 2024 02:42:53 GMT  
		Size: 50.6 MB (50581977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ca9d201aa6b64c6a953cf6a41831e1e2f8b7bbb70d0efc18956dcdfa367cd2`  
		Last Modified: Thu, 11 Jan 2024 02:43:08 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:7eb4891f441fac85602429bb5db1942a8f2e255962c6b9aa34845e8f9d7ed01f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49548866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d865b3e8c026f45605b74e5ee81a23bb69fde6e81a72c76260d86f1577406aa2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:11:06 GMT
ADD file:e632734e8c2b1e7594b8a79fefe3b2790d6e662e647019a7daa2713f4b1aa7be in / 
# Thu, 11 Jan 2024 02:11:13 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:11:24 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:32de429a78b4633d08d4ddf9cb62b7ff44ee9ed79fafe52b6d33ec4e772c2beb`  
		Last Modified: Thu, 11 Jan 2024 02:21:59 GMT  
		Size: 49.5 MB (49548641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f98cbefb15b5c54676afa769d5295e47a3d70386a5c5840492044eadbc03eef`  
		Last Modified: Thu, 11 Jan 2024 02:22:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:5c7cc0850ae74ff925580d47924d6025d8cd4d7ee420910bcb37d852633fa843
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53557798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251bb92e556523b5f99b88eb38b76e318b5d6ca09ab85839521e772077b8b419`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:11 GMT
ADD file:181ff897280683d4e2f512551aa99c5bca9823305859ed4620c8ea3bd4d95cd5 in / 
# Thu, 11 Jan 2024 02:34:14 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:34:20 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:62296c33e75415de6ebf7e20132da876513ede04af94472801e60452c0a295dd`  
		Last Modified: Thu, 11 Jan 2024 02:38:58 GMT  
		Size: 53.6 MB (53557571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1b879af5cc4ab0c088ad19b934f186026016597dad39fa4a2002de68dd3ae6`  
		Last Modified: Thu, 11 Jan 2024 02:39:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:1200028d4954d731b037838f057ee575970e37a526115070538f7ed5f126daeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47918096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c5b30ce5b240cee888edd0b604bf9429daa48c7573948f900c38ef5b323c30`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:44:46 GMT
ADD file:b52927273f91d79b0b493ff5507714cde656c5d76433c6c5b3dafd358f4ed7cd in / 
# Thu, 11 Jan 2024 01:44:50 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 01:44:58 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d28727deb22d156e281ef621e3fd48900f453abc05f099f88bfed20e0f5861b3`  
		Last Modified: Thu, 11 Jan 2024 01:50:35 GMT  
		Size: 47.9 MB (47917872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8aa23f1c08b41f59c7a6be713458702abcc148f21c8b32f6d70cf7801ab91ec`  
		Last Modified: Thu, 11 Jan 2024 01:50:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
