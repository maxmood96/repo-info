## `debian:rc-buggy`

```console
$ docker pull debian@sha256:2a800d1fb35c1c7b6fcac7b8326aa303328adbe4795943c50b669a28c0635998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:ae1f5f00b779415202b106320385752632d2b9f1c6543277a30c05068ac11326
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51500518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d57d6416697df27589b0cf98c6e2efe22b8a52190fe0a589127a98e649f50e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:15 GMT
ADD file:5df7677e65add6d6a9ff681d686094447da195b4999a1f7cff2192740e38e1af in / 
# Sat, 30 Mar 2024 20:52:15 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 20:53:42 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:9fbbc539fc86b3c511f2260d35b9cf5ffb90638ed287142abafd6e1e4bdffbf8`  
		Last Modified: Sat, 30 Mar 2024 20:54:42 GMT  
		Size: 51.5 MB (51500293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd262245893028f02e0762e4b97fbecc144d20896be79287f0961006feec5541`  
		Last Modified: Sat, 30 Mar 2024 20:56:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:26f2d2ad1ad17a98182eca3ac3f472c27a97f22e905dca04b4a9f9540943e910
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48683830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7429ba30a39c8c08cfce42f10501b25792574d37aec8ebff4a0e81879804d262`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:51:36 GMT
ADD file:cd2edb4c012f30c27d706f9d77429a6159628b9f9825990e5ed53fadf0dd1f2a in / 
# Sat, 30 Mar 2024 20:51:36 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 20:52:42 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:803f1fb1440883aa3e0e25bfaee63bd45d691a63416fe58ffa21737aa458dded`  
		Last Modified: Sat, 30 Mar 2024 20:53:32 GMT  
		Size: 48.7 MB (48683606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b33b959d72723bf0cab887539d933fbc655e86063ebab87cd5017588ea2db6`  
		Last Modified: Sat, 30 Mar 2024 20:55:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:d3c3d34ecc37965fae11979842461ac4befc564db387ec51a6c5b28fe2b54a0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46295598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63436c25998b6e3dd2cb6521d16bd6edc193635a37db554b239ac7d153d48207`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:42 GMT
ADD file:0ac8f97579d9f7611b866966dd5fc34fcfa2144355ba39b31883284475bb2585 in / 
# Sat, 30 Mar 2024 20:52:42 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 20:53:55 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0e8b88d91442c01c97d07c620eba463296206c34b7c84ca5b992728b1cf4bd11`  
		Last Modified: Sat, 30 Mar 2024 20:54:52 GMT  
		Size: 46.3 MB (46295373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7caf909f8871d41bbd8ce0b588eec49da6959adcc3e9501d2ca46afb31af70fb`  
		Last Modified: Sat, 30 Mar 2024 20:56:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:399e7842cf3ca96426cdeab73805888b66064a012ef992539e8be750b02c9580
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51377437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43c2762f21c85ca29545a9fe072fba54ab1eea183456f6f8f69a7b698c69b82`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:01 GMT
ADD file:0431bf12596e1a5c3a0d8d282912373bfc2669375b5302333bbd39ecebd1e167 in / 
# Sat, 30 Mar 2024 20:55:01 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 20:56:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:7a4a3e98356da458ec5973da971b31825c760cc233f97a317c13cc7d3cf704a6`  
		Last Modified: Sat, 30 Mar 2024 20:56:59 GMT  
		Size: 51.4 MB (51377212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204b20e25ce229dabc71e82356417f649bb7a09aa3b97d38734221d401f3ddb3`  
		Last Modified: Sat, 30 Mar 2024 20:59:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:9f31d43cb2deaf39a472da01d6cd5744ab80ce06113feecd011a00dc1d201c4a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52279465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c797ba1a5bb063038ba81aca9b021765a2dc5fd1c7d60138d3aa69c1bb51c5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:51:47 GMT
ADD file:5c0cc8b80773608ad255427432daa6a4ea6c6d1257178c16e9fde71fe5f2c803 in / 
# Sat, 30 Mar 2024 20:51:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 20:53:12 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:4c8e6f721d25b23e18d050c75bbf87b16883b01f37acac5142a881b7006f7696`  
		Last Modified: Sat, 30 Mar 2024 20:54:19 GMT  
		Size: 52.3 MB (52279241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f90a8c73b54ddbd795d71bf4715b665f7329604c2fd320b25773123a9d307da`  
		Last Modified: Sat, 30 Mar 2024 20:56:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:19ab7deddef25210e738a297be1f8aede04d3a71b8989fd5f2a2217ecd951103
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50601063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485f69d8f1ef991bee190ca2845a321d4dc63c2d358f64294b7f7585023c8e51`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:54:42 GMT
ADD file:3fab027e6d739287e4b7349292c885c809a65c14845b5d292aebb3844ce27682 in / 
# Sat, 30 Mar 2024 20:54:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 20:59:39 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:cbe55b4cce02b94dd21e3b65d94bdb65a4b1119288ec18dec4cbfe762dc19adc`  
		Last Modified: Sat, 30 Mar 2024 21:01:00 GMT  
		Size: 50.6 MB (50600834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4e3698b541727e4eba0ea8d5e696d8b1fe8fc87b7ef206a078f1ac230900e4`  
		Last Modified: Sat, 30 Mar 2024 21:05:25 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:7a869dabffe1f069906cd004cfc9fd6a826ceb5f6c071b90db8d3717f72688e8
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.3 MB (55287449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22b3742aab6b16d0eefb326e072561a757c23612ad9de1938d085f37389d59d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:03 GMT
ADD file:2bc730d62ee0ff93ea46112c42f75f01e2e6d04449beaf198c5ae6fb388ddd07 in / 
# Sat, 30 Mar 2024 20:55:05 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 20:56:50 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b6224779f10a25b25659a091e0036b5df62f6e69a0c2fe4dc52a3341dae37615`  
		Last Modified: Sat, 30 Mar 2024 20:57:40 GMT  
		Size: 55.3 MB (55287220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456671a9e006aef6617e0ab859a0565d16ba5cfd6c0d7ffc6bedd7e1d446cc8b`  
		Last Modified: Sat, 30 Mar 2024 21:00:01 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:89a3d4cd1d7527f2bbc28072e3a47be7a32453122869f11ba4525b8919c459c6
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49700112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b414ca4056dcd9e1029d3cb0c94835c5cccea52cc6ce37d25e85228a3b556de7`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:15 GMT
ADD file:1794cba0a957e1827904ac718c197ffa00b710464d3140140303007e1771a90b in / 
# Sat, 30 Mar 2024 20:52:17 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 20:54:06 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:16e4421a3b562748342089caab583089b0a176e505692af61640bf0a5aad09c0`  
		Last Modified: Sat, 30 Mar 2024 20:55:01 GMT  
		Size: 49.7 MB (49699884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d96976ce88d3b2664f91d3fb4c0f4833dde2cdda8af9f831ea3e32efa3923d`  
		Last Modified: Sat, 30 Mar 2024 20:57:03 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:20a828858f0eb024691aed0a8c6bc10354daf2bcf62f80d582b924743373ef8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50907402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b258eaa70c6c023b17fdc1537d4f4abc9ff3a2d484cd5188b4e90fd2283db4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 21:09:57 GMT
ADD file:88316cf04f8a7fb87824a6416e9cdf67bcfbf1ca51c2f1bd006913b99521ffb8 in / 
# Sat, 30 Mar 2024 21:09:59 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:26:23 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b0f03a5ad6e4fa7361970002745be26e768ef9bff94fe3f4e4500b11e6b70280`  
		Last Modified: Sat, 30 Mar 2024 21:28:28 GMT  
		Size: 50.9 MB (50907174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914a4b7a12bfae1ff866d122afc6a135fd0e8b9fdb7de97a4016098be09f5097`  
		Last Modified: Sat, 30 Mar 2024 21:30:03 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
