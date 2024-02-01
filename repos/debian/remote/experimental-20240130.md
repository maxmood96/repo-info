## `debian:experimental-20240130`

```console
$ docker pull debian@sha256:4fc25a9afb88f84c9fccf71ed0ca1fdecf684ed38645825adb08fe66d6536266
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

### `debian:experimental-20240130` - linux; amd64

```console
$ docker pull debian@sha256:c7d8f3488ecd79e6b01b8f18466a757cdf6be2682c12fe9b562a7eaca7f4316e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52333094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb8857ce5bd8bb5fd9226a3a5ebdc7d2eac023e8328ca710575616a1124e4fc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:38:21 GMT
ADD file:3aefc80bb198cd847af817f27239d2161b0a93820e11ac0ebee1b649d6acf6fc in / 
# Wed, 31 Jan 2024 22:38:21 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:38:34 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c6aace34c14ee26c018062e3b4751001e160a414dc850e6ad5ec3f44f6ef4d02`  
		Last Modified: Wed, 31 Jan 2024 22:45:17 GMT  
		Size: 52.3 MB (52332874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9dc2304e3abc55d2c6994e9fa6335ef85ac3b76c74eee88d79ec76dcba04dc2`  
		Last Modified: Wed, 31 Jan 2024 22:45:42 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240130` - linux; arm variant v5

```console
$ docker pull debian@sha256:c7b49375c5a02038a4741c50ba2ac361666aeb2e19411ba27c6f0e966c542c87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49419567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d27cbcfcd84283b2f017e2d672af9bf0286119e7f67c9b9ef6e1b8f4b62a114`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:30 GMT
ADD file:a04f5627ddf29fe5594482750e702fd2c15a94154671dc889f1455c3e800e37d in / 
# Wed, 31 Jan 2024 22:46:32 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:46:42 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:aa0d09e4745f77eb3244d0502603dca34f7d3d1c0e9d60a048ff98a434bfcf47`  
		Last Modified: Wed, 31 Jan 2024 22:52:03 GMT  
		Size: 49.4 MB (49419346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f666b971d739eb61b91f5cbd61f6971b0456b104ffc92cbfea2ebc299a5b329`  
		Last Modified: Wed, 31 Jan 2024 22:52:28 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240130` - linux; arm variant v7

```console
$ docker pull debian@sha256:57612fe4aa4c91a146134260ca8d6ded2acd18984c465629a1dd932f52a77bba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46917798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6d155b67a336e00b1d1a15cb40ee8ab6e2eaad5031678beca07e9bc8e30ca4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:47:20 GMT
ADD file:e12186661fd64702574eddbe873220dd09090bc7a291aaae6f3087f3c4409ef7 in / 
# Wed, 31 Jan 2024 22:47:20 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:47:30 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5223450f5c6f7bff029fa3d499952af391ddda01599e08c4753cfbe4f0d49408`  
		Last Modified: Wed, 31 Jan 2024 22:53:54 GMT  
		Size: 46.9 MB (46917579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cff1cc809962033d2c6b877ebd4432daa3047bf6ec477f3451c0edad28976f7`  
		Last Modified: Wed, 31 Jan 2024 22:54:14 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240130` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ce2fd6a6183f8f524798b6ecd3084f59eea0b86b660281027214dcf050070fd9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52190727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10fbcada9bd1c30bf08153cbd78cb792e7fe5453c648a6216a317400c126b9c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:33 GMT
ADD file:4f8393e363c2d316a9c61c8a12680a9d59baba6854ca36f395ddea7391b862ef in / 
# Wed, 31 Jan 2024 22:46:34 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:46:42 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c85ecc2731828d12f3899df470b1dd8715749e26552900d2aa5fdad4cb762a48`  
		Last Modified: Wed, 31 Jan 2024 22:53:03 GMT  
		Size: 52.2 MB (52190506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854def3b7e6654d2f9ac2541bd710806d01c0f9540451ba787874177db5faf2c`  
		Last Modified: Wed, 31 Jan 2024 22:53:25 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240130` - linux; 386

```console
$ docker pull debian@sha256:0b312caec07fda6f307464c31af1fff21d65ba232322aab98347ae771c18d520
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53169431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7b28757bd5f5ee6ad9224c92876367b6103142f43a93cf49e0d6ef4711112c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:42:04 GMT
ADD file:9ce8dff96302f69b8f20114b01e601565055bd81aa92f6c5006cf09d47e676c8 in / 
# Wed, 31 Jan 2024 22:42:05 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:42:17 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:925bce2a010688299d93d833a5406b03a67559012d29deaf0c8757b8f8b92738`  
		Last Modified: Wed, 31 Jan 2024 22:49:53 GMT  
		Size: 53.2 MB (53169210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49cc93f557910e235dde73bddc4cc1776dd7380cb6cc1592656abf99778c82b`  
		Last Modified: Wed, 31 Jan 2024 22:50:18 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240130` - linux; mips64le

```console
$ docker pull debian@sha256:27e3d0c256fa500b829a44e75abef825a06e44abc352d635715fad37f66932b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51406789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8358c94c0092f64678f1a163495abba956e0e4a5ef52b927d08a48adc1b556ce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:19 GMT
ADD file:ef7d40039734eb3e122bddab482b487c07b45bcfeb1e4abcab670a75577650cb in / 
# Wed, 31 Jan 2024 22:35:25 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:36:06 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:81adfccdd0d111918c16fa4b2bf2d4e886d3088b3272a7d02ce82fb58a4a11b0`  
		Last Modified: Wed, 31 Jan 2024 22:46:44 GMT  
		Size: 51.4 MB (51406567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c3b4770f0023fc8ad173f38375d971f094d8a35e88a1c6dcccb1a503726058`  
		Last Modified: Wed, 31 Jan 2024 22:47:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240130` - linux; ppc64le

```console
$ docker pull debian@sha256:be8e0fa1a8572906af3ac6d074f777a85647046e815b157b4ac48ed2aa4046c9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56238069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64b2b2f64d4545fe7a0a5fcdadccf81bcd5dbdddbf4e6131e888457c680d491`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:32:42 GMT
ADD file:6c3d244494a622f4634c205e232e67a69a747d6280b5fe60e739a8a91aa71f39 in / 
# Wed, 31 Jan 2024 22:32:45 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:33:01 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:8aecae30dca63cd3fe52685a456649798c8e7cfd30da4da378b732f33d96e0a3`  
		Last Modified: Wed, 31 Jan 2024 22:39:03 GMT  
		Size: 56.2 MB (56237848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8dbd7e4845b662298e22440f5be769b92e2425a097905dae505450d8833724`  
		Last Modified: Wed, 31 Jan 2024 22:39:31 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240130` - linux; riscv64

```console
$ docker pull debian@sha256:47f6109f7d8a2ab5898c981073f4d57d1db29a43c119a5d33bb4d401ed97ab27
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50540600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1f17c82fbf7251d50962c88b1193521547800811779f0fc570564d78636ce3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:10:43 GMT
ADD file:a968cefffc2712d61926df7336c07c1cd9ce8223f399fa219766e72e5dbde552 in / 
# Wed, 31 Jan 2024 22:10:45 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:11:20 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ebc931821cbbcfe2fe9c159576b63ec85ed85cf1d10c3d653705732adf8f12d6`  
		Last Modified: Wed, 31 Jan 2024 22:13:58 GMT  
		Size: 50.5 MB (50540377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e5293e6f4f8b2095b0f623ed264e956259a2c6c956193898a88938ffae1364`  
		Last Modified: Wed, 31 Jan 2024 22:14:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240130` - linux; s390x

```console
$ docker pull debian@sha256:c3ff2bf13d7a8a609194dce2eb9594ff1c8b941885caf0773468f2b9c9376276
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51740816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d7ad3d5cb6a6f6e73f9a1f4977d737b94b0c9bb0b9ad2b767a117f4504a02e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:22:32 GMT
ADD file:416abfe619dec0e9729fafe0c264230831101720bc8176e9db216e94cc3da213 in / 
# Wed, 31 Jan 2024 23:22:37 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:25:18 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:48ee0605b2a629a7a1b1c036b8459e6845418549e48e2f9baeaa1a68bc5f0a19`  
		Last Modified: Wed, 31 Jan 2024 23:32:08 GMT  
		Size: 51.7 MB (51740595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3120b04f2ab42fe5c17a5844838f54593c04cede7d7b68576fe1b786b81828`  
		Last Modified: Wed, 31 Jan 2024 23:32:25 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
