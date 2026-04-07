## `debian:experimental-20260406`

```console
$ docker pull debian@sha256:5b5759523c5c1693929b523ba16f2f4296cdb6dcec5ed019855da6609c2e7863
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:experimental-20260406` - linux; amd64

```console
$ docker pull debian@sha256:18df5244f3e6e42f45569d150077fcdca9cba742baffa953aa26f26c5cff9578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48710875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923e3be1a38b921bf3279d34aa6d7432afc6bec041bcdb15f77ef7a6451824c6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1775433600'
# Tue, 07 Apr 2026 01:16:28 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:64512d0cfe353cbb263c251e301212a0804a3dd6863f2f353cae58ebcaa15a0c`  
		Last Modified: Tue, 07 Apr 2026 00:11:38 GMT  
		Size: 48.7 MB (48710653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95a6cd95a7680c731ac462847d9b5a361ea980b798d40d37c9c838b8a501a64`  
		Last Modified: Tue, 07 Apr 2026 01:16:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260406` - unknown; unknown

```console
$ docker pull debian@sha256:2c93903fe56c96c24fe1ad1118db15f36856c23ba3a8f5e090504178f7f78af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141b6d7fabf658d69a413779608ad0bfebf13c3c6a39341960ff721a5a51f8cf`

```dockerfile
```

-	Layers:
	-	`sha256:4bb602f02153b62464e104aa93258b71ae2d53de220cb78178143e4cc9b11dfd`  
		Last Modified: Tue, 07 Apr 2026 01:16:34 GMT  
		Size: 3.1 MB (3140680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54a820e8087835ae873e92592860961aa9c0bbc2f9ae8425ed961f32946dbc6b`  
		Last Modified: Tue, 07 Apr 2026 01:16:34 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260406` - linux; arm variant v7

```console
$ docker pull debian@sha256:61d527d0ee0502de492c7ea7594c62fe601e6e99cc062a2b5286de4beb4bf17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45638190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3453f0fc8d2cdc656a99a4c36e99ed294316c6cf7bb41dc8671ca75f03025a1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1775433600'
# Tue, 07 Apr 2026 01:16:13 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:70d568ffc41f56f1bf9a0768102a2d6ab01d2bf2bd7691997300ae6c17237af6`  
		Last Modified: Tue, 07 Apr 2026 01:00:05 GMT  
		Size: 45.6 MB (45637969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df095a2e1228c77e8c828f1223e833e09631c3a1cb0b85a58c88c3c08c3ddf7a`  
		Last Modified: Tue, 07 Apr 2026 01:16:19 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260406` - unknown; unknown

```console
$ docker pull debian@sha256:6b1b3ec31d534d900136f24197b1e048385be940198a2a53e3f0731f9436c423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f729b57bab213000ba0bf6b482b61edd81f353d7cc204e945217820fa671ef31`

```dockerfile
```

-	Layers:
	-	`sha256:26606ba33261507b705e0abbb8af5870d2ac4b294de980bf4653f3317bcdb809`  
		Last Modified: Tue, 07 Apr 2026 01:16:19 GMT  
		Size: 3.1 MB (3142050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2f3bdd6f3548c37199c278c390f27559af700847d0c578e8fa5472a111d96ab`  
		Last Modified: Tue, 07 Apr 2026 01:16:19 GMT  
		Size: 6.2 KB (6165 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260406` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:bea882de9cfb6a02346a3a5970df1608875561f3219725b98582c94054222568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48745173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4244864c97235bc1fda67fb5321d7cbdf3ec624da9cf4f6c5590bd10dbd329`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1775433600'
# Tue, 07 Apr 2026 01:16:33 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:33e25202c8f77f614c3f21ac484c116a0717f8307b53aa837ec8be4aba7a9545`  
		Last Modified: Tue, 07 Apr 2026 00:11:22 GMT  
		Size: 48.7 MB (48744951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b3b0261f73e054268ae48b3b29ea8170ef4f0540dd86bdccc4af025ea79afa`  
		Last Modified: Tue, 07 Apr 2026 01:16:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260406` - unknown; unknown

```console
$ docker pull debian@sha256:97abcc65b72a8ed63f19e38b392fa9de8170e2f0f738376513ae0fc26191ccd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb83629c712c70ef268e4434bef573b66e34acbddb0fd88fa131588d720acc49`

```dockerfile
```

-	Layers:
	-	`sha256:9adb3af0d616f9d1da2884579ea6c83c92da1d48017a98bf41cf9acb3c0a79df`  
		Last Modified: Tue, 07 Apr 2026 01:16:40 GMT  
		Size: 3.1 MB (3146642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d10a631c55bb230bf52c348350cb4282ae36a2e18b8f79532a1c0bceae18899`  
		Last Modified: Tue, 07 Apr 2026 01:16:39 GMT  
		Size: 6.2 KB (6180 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260406` - linux; 386

```console
$ docker pull debian@sha256:bcc264fc3aaec08da54f6f04aacde8e782e4521664862c72a3bb6a42e1df60d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49993938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6e8df44c3ae6ce33fe6f030a4a6c2f6dd15b8fa7e9aa4ad771f6e35aca74ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1775433600'
# Tue, 07 Apr 2026 01:16:03 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:4764180096084920e70cc5e56f0e47fb932f74cca424c3f071122ba47089eb62`  
		Last Modified: Tue, 07 Apr 2026 00:11:29 GMT  
		Size: 50.0 MB (49993716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd58640cd35bd36c0e8bdb8fd43695309cb3ae3a7ee30657cad089581cb0fd9`  
		Last Modified: Tue, 07 Apr 2026 01:16:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260406` - unknown; unknown

```console
$ docker pull debian@sha256:b2268528c05a62c440fdadbbe8068dbefb86a4ba8c8caabb0fce5cfd72876879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3143958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dcfa518e6483a5cbdb45baa038bcfaf3d7841d303c49e321275dde077ac732c`

```dockerfile
```

-	Layers:
	-	`sha256:93cd24fd0226d265f57a11277e77470f55cb4a66075dfe31732a47798f9e7e79`  
		Last Modified: Tue, 07 Apr 2026 01:16:09 GMT  
		Size: 3.1 MB (3137880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e47cf80e0a9843a6270a005dd8e73c4f6b165f7e2f7328dd777f2a44dff0ae49`  
		Last Modified: Tue, 07 Apr 2026 01:16:09 GMT  
		Size: 6.1 KB (6078 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260406` - linux; ppc64le

```console
$ docker pull debian@sha256:80ad64455fc9f9423797e254b6cd010193594a8867307e237ea7d408b3b64ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54002176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583933e0b16e2bf8beac41590befcd2c8c7a6697c71439c898206c866a6e031b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1775433600'
# Tue, 07 Apr 2026 01:17:56 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:7c41d1c1a7ebaeb63460fe4a5bdb4736ce54dee76d51374cca420a0c3207e46e`  
		Last Modified: Tue, 07 Apr 2026 00:13:25 GMT  
		Size: 54.0 MB (54001955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8db8473556d9a6908877e480abfaeb46ee0d821aa405aab08dc0d70dd4af48e`  
		Last Modified: Tue, 07 Apr 2026 01:18:10 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260406` - unknown; unknown

```console
$ docker pull debian@sha256:61ce3c86dda0de315ff090fb970acffc7bb727ed4f99694e43a303f0a61c711b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536ea8a495f5b9f73c9b4b4250184fc9bce623fba8cb309f462744254fb0f5ea`

```dockerfile
```

-	Layers:
	-	`sha256:8f9c0104854b4ad0abe9d112367e9522f77d12b310419d935fcaa26d6176d103`  
		Last Modified: Tue, 07 Apr 2026 01:18:10 GMT  
		Size: 3.1 MB (3144181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a57af1eba440ec81ae4ffe5ad97aeae3859b4468e35c5a3b736786b2cb0f98`  
		Last Modified: Tue, 07 Apr 2026 01:18:10 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260406` - linux; riscv64

```console
$ docker pull debian@sha256:f38fca7cf6a64c472d957bf3d26668ae0991553f67b6fe57e8f38ff8b34b1e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46787131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d25b3390cf15d79b39ba92b5efb77a9de23a58b6bfe9094c97c7d1d6d86265`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'unstable' '@1775433600'
# Tue, 07 Apr 2026 02:34:40 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:f1c7c989041d5fbbbc2c691d1ea45ba71f6db74810cc60b3fbc75c9f47cdc42c`  
		Last Modified: Tue, 07 Apr 2026 01:57:31 GMT  
		Size: 46.8 MB (46786911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488aef6b297527845ada7bc197b6b04d3409b7ee75a61ca750e6a90229b94107`  
		Last Modified: Tue, 07 Apr 2026 02:35:31 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260406` - unknown; unknown

```console
$ docker pull debian@sha256:578408daeea8cc2831b505e517d15a8289ce5cd8f076a5a155c0b1d002bb0a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df011a514ac841bdc2ab13145537f7b8801078e3d2962df4bab6c7436420a44`

```dockerfile
```

-	Layers:
	-	`sha256:6e0515993353fdbb107b9b72e4be9e7334c468d91afdd796a9eda9b9cba61e60`  
		Last Modified: Tue, 07 Apr 2026 02:35:32 GMT  
		Size: 3.1 MB (3132184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee6a9b4a923f065580e7165e10544198096fbe1f062bbea8e7a8e48d196db76`  
		Last Modified: Tue, 07 Apr 2026 02:35:31 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260406` - linux; s390x

```console
$ docker pull debian@sha256:953dccf02ff687942d2a8ec9fad23beadd464e56f20601589a0278954673d04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48425604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285df6a086cc701e595571b95866701fa7565c1164d0e4c89f6c41b9cf39bea6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1775433600'
# Tue, 07 Apr 2026 01:17:22 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:c1a74ee5804d58cefa756b83552fceaf4da92d9dee10781b0deadadd5556cbf4`  
		Last Modified: Tue, 07 Apr 2026 00:14:06 GMT  
		Size: 48.4 MB (48425383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cfd31f9aa9136e8aa6ecea4ee0242845b1bdaa627af31abc4d4e8e0b0309c3`  
		Last Modified: Tue, 07 Apr 2026 01:17:39 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260406` - unknown; unknown

```console
$ docker pull debian@sha256:292202b8ebfce709eeebfc0e09a896ef7d983c5062c25a116f4acb646c07d78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35c52031c9e2b7cff1652b51f0a270eafcc0a02484a8a614df962a16eb4b396`

```dockerfile
```

-	Layers:
	-	`sha256:7f6aca5df2d8818a5da0b5261515ce9e42c01f8b23d7747c9089474d96d5854c`  
		Last Modified: Tue, 07 Apr 2026 01:17:40 GMT  
		Size: 3.1 MB (3142131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac0d4253812f33556dcda8dca12a6b7aa1a0a899d32507518589e863bf1fc3c8`  
		Last Modified: Tue, 07 Apr 2026 01:17:39 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.in-toto+json
