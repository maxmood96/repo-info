## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:6aeb13202b32cb5ee6115b99425359ab45d6f71295b769cad673adff6f7a91a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:e7b3574eb92d0faed0033c73d333a6084ef0f9ec93763b40cbc900744d8219f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48481021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55edcfb6c20bc1852bc9852c085e440afcddb6353fa1ca04f6edb3f144610ec`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:15:03 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3055c5157dfc41cb7127175c0ac1558234d4f6783bed768064bed70bb1272f6d`  
		Last Modified: Mon, 29 Dec 2025 23:15:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:499812c13d9e4cf8fa51b8146e1890327108b8fd67853a23467681254a816c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac3a4de3213107a0265aa9002fe64d7c2a8ce7a538b9fe35bac8e6585198b2f`

```dockerfile
```

-	Layers:
	-	`sha256:8a1d4fb274ee0c14c604767d4a7a80c668ee14c60151f8ba59256ee8a560f310`  
		Last Modified: Tue, 30 Dec 2025 04:24:38 GMT  
		Size: 3.7 MB (3733431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c51ddac21a3cef52ac9a60832edfec5bc3d2910c02435c6ab6f0aebdbb811bcc`  
		Last Modified: Tue, 30 Dec 2025 04:24:38 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:ae305bb24331b01fddc78a2ba2582b09f25f48d305b8abf80695d70106869844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46016097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bd64c1bce4566dc9cdc1666a5df233e867dd0e086426b66cf9e0b561070c40`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:14:43 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:382890ab3968ba1cefa561463cb731ea178ca7d67e9b6d5bb6fac532b4127c25`  
		Last Modified: Mon, 29 Dec 2025 22:25:07 GMT  
		Size: 46.0 MB (46015872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d30a7cb9a6508d4cf05e63a2b319a7b16970ba5dee9a035f32974fdb42c94a0`  
		Last Modified: Mon, 29 Dec 2025 23:14:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:03a2be1e1bd3134cb0dbbbc489b80e9f693b48f723b39b942f2376c126dda105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6548e03392e95b2f8ff01a135146b5cf42361dd1523a565037726130ee234eb7`

```dockerfile
```

-	Layers:
	-	`sha256:46614b2cd6ea435fb0d1820e890b44d798908c8158d59f2a5358ab045db8460e`  
		Last Modified: Tue, 30 Dec 2025 01:26:28 GMT  
		Size: 3.7 MB (3733632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46388dcd97216d1cfa9e0d90564ce8db75ef9ac4244cc8d40dc12945059ef351`  
		Last Modified: Tue, 30 Dec 2025 01:26:28 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:02cc9e166b61b6715fd9cb90f8d1c2ce98803017d55f40ef6d8c6dffb6ef95c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44196355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5d860e83095a8a1842bb9b0d98daa78f98fa87113ee91888c40d83a31f4b16`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:14:45 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e89c6396ded32c2f8dc71a0c5aae48558ec631543500fcbbe7dbc428401a7361`  
		Last Modified: Mon, 29 Dec 2025 22:25:09 GMT  
		Size: 44.2 MB (44196130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04552302d7d8a12261f815a77d8fb59f2a318f6fd8d0aa3224df61f02634387e`  
		Last Modified: Mon, 29 Dec 2025 23:14:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:cecbaa54dc94d832f88f0c017d9cb4d2ee589e8b405314b2d199d2992c97368f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e5b9830ac03fc894fd1ba84b8e506e3e1ecc99efcdbbadb8ff50e45275c324`

```dockerfile
```

-	Layers:
	-	`sha256:87342e7a3fdc1739274c50568eab9c8c04ea9475f889de7c793789b091c0d2d1`  
		Last Modified: Tue, 30 Dec 2025 04:24:46 GMT  
		Size: 3.7 MB (3735610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31a3f836525bc896b3d566fa50bf0c7c1a48dd60bbf9475bd10302ea9a18390f`  
		Last Modified: Tue, 30 Dec 2025 04:24:47 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:52e26a022706666b47c8997b949cec2720b4aafa7699b31b522b263cd0ced5da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48359371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c10a93b1da0d180beaeacf0028639d75115fb6dde394efc5c80c7a76b575d6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:14:37 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea14343c8664aa6db9fae8d4e3073a78e3b7eec85308c101c18c45e222ceef5`  
		Last Modified: Mon, 29 Dec 2025 23:14:52 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2fa42010c6d3dff8be3e01d88f65b80caa775a55f51afa42cfa2f6d242f31788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5f695aa3a33ff70b403c9b65d4aa5715bd45e24e48d24d65e4e1e8d1dab320`

```dockerfile
```

-	Layers:
	-	`sha256:f0d00d1ec86e94acae9b0473fbb24ce1befd54d1e9db7cad43caa1a74fb59e73`  
		Last Modified: Tue, 30 Dec 2025 04:24:51 GMT  
		Size: 3.7 MB (3733646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a689cd1e06be128421a44b6eed04b8f7db1b78772a147bef32ea1df9e5149ad`  
		Last Modified: Tue, 30 Dec 2025 04:24:52 GMT  
		Size: 5.9 KB (5872 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:3b0d2a27044d0a5d4c7a6a6b53d170d9ac2ffeb99b857b4f8abaeb1e0c412a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49467103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7aba7541db1f6a8383f87382885faa90c00c1bab2dc0526b80d1028968fa664`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:14:30 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d27cc9ffb7903d292157edf3b1fb57175a2a59b66ae4855d328a6a97d9b4a6e9`  
		Last Modified: Mon, 29 Dec 2025 22:24:49 GMT  
		Size: 49.5 MB (49466879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f53869456ba3628380188e89fede12993b59ae36d614391c11eb3ef00f0aa20`  
		Last Modified: Mon, 29 Dec 2025 23:14:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b6bbd244e6578301f12afe88dd06c85c2ff823acbb4d33d5f844ef3c9aa412e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be2c97707be92eec7ebccfd67b05187dd629df66344bfcce85b5691735cf2cf6`

```dockerfile
```

-	Layers:
	-	`sha256:815445c34f95c0eb020fdd0de65c0bcbd2541c87944bf5af238d01136f53e982`  
		Last Modified: Tue, 30 Dec 2025 04:24:56 GMT  
		Size: 3.7 MB (3730628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b98ca6e3d853ba344c270e19b02c490315b3a051dc4e78c8312bf801ab5e9e7e`  
		Last Modified: Tue, 30 Dec 2025 04:24:57 GMT  
		Size: 5.8 KB (5787 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:ceb5db898e87c9596a2173122aaa6f13661e0c9a82a8a0c15e6971b3f8f32669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48761153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561476f2a320ed7423cb136170904ed846876d16e0b65f6ca41413ba160cd91d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:14:25 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6a43d59f754c088126249c7de1413be451574eda24274414bef9aea85a3ac886`  
		Last Modified: Mon, 29 Dec 2025 22:38:14 GMT  
		Size: 48.8 MB (48760925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f5ec2d33e56eb5456f37014106db4e3100b63e0816802cde1f288f551d3c6e`  
		Last Modified: Mon, 29 Dec 2025 23:14:49 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:994591fabf93c4dd4f826995f2400212dce5c84bb2bc007693566d0fcf850319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90c6bda4cb75bb864700000e255fc935707c4e7047816f87cc955b4dade629c`

```dockerfile
```

-	Layers:
	-	`sha256:0a3ef6759ca880ba87ba0e250e95f1a92822af12da618462890af86948e718b9`  
		Last Modified: Tue, 30 Dec 2025 01:26:43 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:fc0b2f67174ed4a9ae43af794c4a5f1961cdfef1f4bd67e2f3582724b078d6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52327223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f54a61095f0d1f43bad39f8fcafd2249840a0b4aae1b0b5658da4ff66d38d36`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:29:43 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:48e256c4119c0ad256492d6a930e99d2b2d7f8d7920d619aa2de4f616c37076e`  
		Last Modified: Mon, 29 Dec 2025 22:25:39 GMT  
		Size: 52.3 MB (52326998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074ee30261a2e3d9fd1b3d2e6809c63851fa2a727b2fb1cd689d9881653fb253`  
		Last Modified: Tue, 30 Dec 2025 01:30:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b794a7c9188c0df62f9ba50302da8559b5e6e32d35b9461677e4718efa22eb85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d280dfcd1fe847377c2c8b01105db75f1e7a494f9efc7e8f6c6cda56dd470b`

```dockerfile
```

-	Layers:
	-	`sha256:18b50d3c9bea3cdf24ee7b76c5087a9bf934fd3b248beca5a58e3773a67d2489`  
		Last Modified: Tue, 30 Dec 2025 04:25:02 GMT  
		Size: 3.7 MB (3737787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4729908b52666ef6f50b041ea405ccc758b2e718793948b6f6ea8bef8213f42`  
		Last Modified: Tue, 30 Dec 2025 04:25:12 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:48e0d516f8dddb0d985557d56cc507e5167bf015ad5f0ba936452f5ab7692664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47137952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4a91e0a76f4396157c22ec4e5abe2aaac2e4be42a0f065d2e0b35cce3e0fac`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:13:47 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ce8a6983b315f7ccc96b582192afffde7bfdc0a45f357f2cd098b4f88aab2be4`  
		Last Modified: Mon, 29 Dec 2025 22:25:37 GMT  
		Size: 47.1 MB (47137727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7886c5cc715ec0fec61cb8443dbfe51eddc7e66f72bc102aa46cdfb68bab09aa`  
		Last Modified: Mon, 29 Dec 2025 23:14:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1cc4da8b4bfa82b05ad90eb125c04d856727537d7f71b27035901a9d33c3a93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bb5724fae1121e858d3ea2a806fcc8f144ebe5ecc555347ac47c689cbff04c`

```dockerfile
```

-	Layers:
	-	`sha256:8b7d09cf667a5175454287e1defe9ae301c84c8eba3dcaef5d746fd840f5e4d5`  
		Last Modified: Tue, 30 Dec 2025 01:26:49 GMT  
		Size: 3.7 MB (3730269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18a47429a39d689e5eacf34219c828ab4960b7c04c7c1f6f3c3c9cbdf04fbe85`  
		Last Modified: Tue, 30 Dec 2025 01:26:50 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json
