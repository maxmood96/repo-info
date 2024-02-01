## `debian:testing-backports`

```console
$ docker pull debian@sha256:143824ed7ac50b96347719e8069d75eb4b8d4cdcf4da305fb0f844953f3079ad
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:e230d6dde941442d59bc24a2c1e1ca25c5ded78aa9157714a31a5430558dee0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52283415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06aeeca315752d12d9e2c3ba543a245be6237a5be03ea6a8805cf0ed116a0028`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:37:36 GMT
ADD file:603237810768dd1380a911bc8974893a077b7a5906fa11d5bd7013e62e2aa352 in / 
# Wed, 31 Jan 2024 22:37:37 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:37:41 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:10c69e045d41e730cfa46d159956d856795f06d2d429a76925ed787b9cb1b442`  
		Last Modified: Wed, 31 Jan 2024 22:44:03 GMT  
		Size: 52.3 MB (52283193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5531566d64a552ce65eef50dedf0a7c28f7c9bf99dfa06819af8536eeecf593`  
		Last Modified: Wed, 31 Jan 2024 22:44:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:0dc57c58a56d16d9f0d934f53cf235691a966abd1214e5b0cb23e3c8efe77886
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49401000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfbf922730889c43c07edc22837c3f41b3d37af14f62ce48cfb7c6688931abe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:48 GMT
ADD file:90a3531052ff4387c0d5e35eaadd762a14bc0518f413bdd8a0452a10ed55b6ba in / 
# Wed, 31 Jan 2024 22:45:49 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:45:51 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4372d9a33f73b854e7d6eda35c1d09c526aaba889914364e5d54d0995c62ba21`  
		Last Modified: Wed, 31 Jan 2024 22:50:52 GMT  
		Size: 49.4 MB (49400778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7450e6d7d7fa0161c46cae4a54eb6f9561ce85f99d17eaa4961a01b1ca2d31`  
		Last Modified: Wed, 31 Jan 2024 22:51:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:dc5f130e4f08a54fed97da3f2d6a1d3746301460e5761cb9706eb7d402a3ad1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46892778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7e3e2a48d87bd0f8d015bb6ad131e0014cbfb0ca740d3617031170807c6120`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:43 GMT
ADD file:4abc811ec07a2b9e79f32ae2883f53afbfe2781cc7486917b191b5ca0979c3a5 in / 
# Wed, 31 Jan 2024 22:46:43 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:46:46 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:554f87df2e7ab2cc89f0233ccd233c6bc99b1eef9563f57b480b942939b32662`  
		Last Modified: Wed, 31 Jan 2024 22:52:49 GMT  
		Size: 46.9 MB (46892553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c96d62d2660da572743baf4984d898957adf223ec696f4838393fe74b476ba0`  
		Last Modified: Wed, 31 Jan 2024 22:52:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8ab12be946545ebe36db27ee7b79f1be4afc55085e497d27f9c79feedd5e8907
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52161602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbc6612c08e76f187b58d1695cd9993146fa1a19838a4cc015e53d137ccc079`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:03 GMT
ADD file:7ee3c0539d396e0792ed68269fa710165c0457a7534e01b5c22cabc84cdafcfb in / 
# Wed, 31 Jan 2024 22:46:04 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:46:07 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:76832b4a5d197ea5c080862484bac9955c3fb1c4bab0098cf33a245ed7bfd72e`  
		Last Modified: Wed, 31 Jan 2024 22:51:59 GMT  
		Size: 52.2 MB (52161380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73240f2f3cd0607d90e9f30bddc869f48bf51199fe337abab5c3cd5dfa3adc0`  
		Last Modified: Wed, 31 Jan 2024 22:52:08 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:0e9d8554738581f1d6ad6b5f32ac1c911cca6c317ff17a72478f5028b14398b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53140269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7323a961b0f78e955f715281ab5536e66069b5bf5dbc29e81079d4da48fb67e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:41:21 GMT
ADD file:4980e795e30b2f59ab068fbc04ec5998d59fa21986e1ffa344e1127c407b4b17 in / 
# Wed, 31 Jan 2024 22:41:22 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:41:25 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ee9510c6acc00b1bd0ac3202e11ddcb9b4ea9cd7f655026c4a2a81d4a02ecdb5`  
		Last Modified: Wed, 31 Jan 2024 22:48:29 GMT  
		Size: 53.1 MB (53140046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7171cab4388fbcb14e203380d62ae6c2acb715bf263dea46c157718aa69ada8`  
		Last Modified: Wed, 31 Jan 2024 22:48:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:7870e2989c6c66368db19964ae0976628c737b0c4b45aebea051e78244306d56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51373976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb256628bba1322e3ac36342a83f48703c6906001931c079d6b62d234d4ef96`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:32:44 GMT
ADD file:7af8d4e36ebf06b41ab9afcd5dcc2ab5c14d0342fc0c919c2d4e281a9cd435c7 in / 
# Wed, 31 Jan 2024 22:32:51 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:33:04 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:912a6e52ac2e7eedcba0446cfc3253750323ce0ce193eb3a3f83d4975425f630`  
		Last Modified: Wed, 31 Jan 2024 22:44:12 GMT  
		Size: 51.4 MB (51373754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9db569d463a1d62614087f7c797773942569b6d277b7dba3ea6c7f15fe1f80`  
		Last Modified: Wed, 31 Jan 2024 22:44:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:238e5c021e0f0be435a0b1bb2897fe7ced45457d11e9a6ec3900021a892f0b92
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56199069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9af5833c68586e0074d74b50a0dd6fbb82534b0d191872758e133e71af6f64`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:31:45 GMT
ADD file:250d605af8ffae8b389f7325ab9d0e69d953ea56c80a4aff820652c5a4fe0ada in / 
# Wed, 31 Jan 2024 22:31:49 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:31:53 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e31582b2e6d39845d4311bbd81ac584a8bcc2c9e6e745892afb34a275a20d4b2`  
		Last Modified: Wed, 31 Jan 2024 22:37:37 GMT  
		Size: 56.2 MB (56198847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7feedf06fed3e56d2bce0567ee9fb5ad463d1cd4e68c5277fba6b9bde317d12`  
		Last Modified: Wed, 31 Jan 2024 22:37:46 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:af741c3387748c4607522923a74b00a47ba03981e424823bacaeb90ca24951c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51697985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d8c208e5c324701f2e70a9ba53d83d44bb2774981045a3c2e104d912df024f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:14:33 GMT
ADD file:bc42aa20ca8fb3dffb3153578505c3bfe2a0932acb648b236a60d80efd6cab2d in / 
# Wed, 31 Jan 2024 23:14:36 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:15:46 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:33220e6bab847d2bdb1e35e8cfa9c770914024121a7b0c8ee790d490925e8b6e`  
		Last Modified: Wed, 31 Jan 2024 23:31:13 GMT  
		Size: 51.7 MB (51697763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b5fb787c3cfe0d74621dacd1f50ac5c81d689f3dc266c08107dba3ddd096b3`  
		Last Modified: Wed, 31 Jan 2024 23:31:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
