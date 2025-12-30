## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:86f9e832cb6c3037ac87f0553600980d46d4adab0c293c4cb2ba3cdb8828c1fe
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
$ docker pull debian@sha256:070210843a821869e01663e1a0e9a3b8f6408c9cbd2167e1427bd38b327d9c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48480960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2876ed11457d95b69237342ed69de3cce42924ee177a159357c73562945a36d5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:30:09 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331c5f57c9e3af7c6ae0c840a249aa0c2d150370f827990f4fb5b0aca52025e7`  
		Last Modified: Mon, 08 Dec 2025 22:30:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:71498323fff2ed423d8efc1dd0f5397ba5b400f174e96533637ec84396b70d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe4b1953d7f1c8606946be2aaf00d396404b658b1c985f3e12ed44dc9ce3574`

```dockerfile
```

-	Layers:
	-	`sha256:af1dc46de6915fdddfc12fa225eb9d9f9c114c774c480aebb411ab66e9f28f26`  
		Last Modified: Tue, 09 Dec 2025 01:25:50 GMT  
		Size: 3.7 MB (3733431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08447cb2a0b432be84d385b9190dd7ed734cf169f4e6389891fcd548c91621b0`  
		Last Modified: Tue, 09 Dec 2025 01:25:51 GMT  
		Size: 5.8 KB (5803 bytes)  
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
$ docker pull debian@sha256:fc7c41d7b7671aec501b368a7cf010ec37e7ce131033211719d0de38a869c8d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44196291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00df010ca61ba13bd4a4c4cf9efc65fd1bf0736e3b7b0350d7fa1931d3629f7f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:30:43 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c3d6a83e736aa77820543663b2d6579ddd98b0f465c0fcad8aa9bd98a5b72a9c`  
		Last Modified: Mon, 08 Dec 2025 22:16:46 GMT  
		Size: 44.2 MB (44196066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a6a6e00f823990b2007b70315037a49e78132472635e0ce568354cc348876b`  
		Last Modified: Mon, 08 Dec 2025 22:30:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a104e5bb3f8976be25517d649cc1be4887f28d76485109aacf1ec939812a49d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8144ff814b62be975e228b0b41f05eb0db7c2a0b07ee745c5ed004c26fddba`

```dockerfile
```

-	Layers:
	-	`sha256:5610be9c4c57fcc9f8a7a9b747c5a39da43d99ebda375665d9b2c1197067eb91`  
		Last Modified: Tue, 09 Dec 2025 01:26:02 GMT  
		Size: 3.7 MB (3735610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2515095d3da570392292d7d137ea6d2b4804056deec09208cf613ca80b08e2a2`  
		Last Modified: Tue, 09 Dec 2025 01:26:03 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8ffafff7908b72e58ceeef3c164f9a90346999613b79661752855b26ee361fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48359294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76974ea4ba34a35b9259bc0e918e8795e98d43c0f9a4bd0345c1135ad9c631d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:30:40 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828938335f630cb0dfde2ba1364267fe8c2014b444f7b288e3cc504bc773aa38`  
		Last Modified: Mon, 08 Dec 2025 22:30:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6cfded8efad8e43eba39e811ebac930fabc0eaafd50cc6b5c4ddd06b2ef9c1c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e469d4459b109c67c85fa547b6db7d43a0538075fbc79504b3593c232cda48f9`

```dockerfile
```

-	Layers:
	-	`sha256:ed9aa5ac897d07a3b52d3bd5cde28c0b9eff70452e1189a09bfb72be74cbe2a4`  
		Last Modified: Tue, 09 Dec 2025 01:26:07 GMT  
		Size: 3.7 MB (3733646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e93d18db7353afc73e31ead51eb6b7c550e682162b881f6ce15f7128def1f20c`  
		Last Modified: Tue, 09 Dec 2025 01:26:08 GMT  
		Size: 5.9 KB (5872 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:4f5d6d31b0a4d0d1cbdaa19ac35cc95641236a3f92f9d9a8833de04d0d66bdf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49467043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6984dbfefa89496b2c028f982e614722575f0297e7f6ecff0f7cb1ab6d1ae8e5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:28:50 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5a0767b6533dfa923197197a2adf3860bde889326cc3199fec46ced873deb7e1`  
		Last Modified: Mon, 08 Dec 2025 22:16:44 GMT  
		Size: 49.5 MB (49466819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c797626a5eaed98a64a3896975bf3dc7f6a5e624586e3f868570c47fa071976`  
		Last Modified: Mon, 08 Dec 2025 22:29:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:be0405aa07a932f57426c0e318f5378960918ad474bec13f2ab1e008a950a6b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c3c9498f6c5fde5de49be0e7860b6c81281dcd73ca3fd899efcbb9213717f8`

```dockerfile
```

-	Layers:
	-	`sha256:7402bb26e0148385949cd1cfac6d4410b39e7e8d0cd0b6c25fe33aebbd2be33e`  
		Last Modified: Tue, 09 Dec 2025 01:26:13 GMT  
		Size: 3.7 MB (3730628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac9ea2c3549eb828c64aa5a441c583e9c41da997a7db92cdd6828db2ee8d45d1`  
		Last Modified: Tue, 09 Dec 2025 01:26:14 GMT  
		Size: 5.8 KB (5785 bytes)  
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
$ docker pull debian@sha256:855ecd7f8fc22d0a893056481e7156dff9d273259a64063d3a27f48a8ce8e10b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52327201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70a64a7f812a50a2bda0239f37e6da75a0458878ce812ed531b289f52a53b03`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:28:40 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05e646fc339a50d2316d41f42c0c2ab33e239048067d0c885cf96edabeddfb8`  
		Last Modified: Mon, 08 Dec 2025 22:28:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8074ad0e8d3044408640c38476faa4847dde839dcabb97a24ff50b25939a521f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d085dc8a70237a634d884a06c69162faada64ac476caf5b2b29bd15dd09befa`

```dockerfile
```

-	Layers:
	-	`sha256:33f456afab1e69286ead76e360d9628d6e649a2daff58bb3133474781f39e167`  
		Last Modified: Tue, 09 Dec 2025 01:26:22 GMT  
		Size: 3.7 MB (3737787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7b7ea477988d1546b2de7caf0782aac7fc99dda1412893617a8c7adcbf79894`  
		Last Modified: Tue, 09 Dec 2025 01:26:23 GMT  
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
