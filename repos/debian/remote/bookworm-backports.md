## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:4c3cb3f1516045a6ab20ed5d1e07fd122a706e6c037bdffd2243a4553efcba0c
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
$ docker pull debian@sha256:40fcc1902a3f4f40ac28a68d5fb0acd37d78362a784c86517954f630b8b996ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48488854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0582ef4b639582a13b0565bedca464bbb8080f5da8442b1f5e7e34d11c975dca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:14:53 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704dcfc20539d2071021b0928d5463d8ec18b198fc26135bc5dbe126873ea552`  
		Last Modified: Wed, 22 Apr 2026 01:14:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b93cfcfce1061a489916288deab676843ae9e729bd5b5439f20ed63a3a1c597c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e19ab0e6d372081c8e79e47b6757d8656873dd3dd84af0099002df65060dd5b`

```dockerfile
```

-	Layers:
	-	`sha256:72cb221cac1d7dc32939cc821bedde8db003199254d4f2f7b04d341a1b273313`  
		Last Modified: Wed, 22 Apr 2026 01:15:00 GMT  
		Size: 3.7 MB (3734074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5132d060e7f07ace38bde82de2c1ab440473169bdab0ba3904597a37b1ded09`  
		Last Modified: Wed, 22 Apr 2026 01:14:59 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:59efb53adfb2a296750714858eb2e554f51dbbe16f72c57c4e26c6baec59eada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46021892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525d6c0209c6c3e0e91faf2861f424dcea8bf973b3908477f6c18b17185b02f2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:31:55 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c4564d3f444801f4c4ab3e01fd62e7dd3bd91054769ac22888b9bef61823a830`  
		Last Modified: Tue, 07 Apr 2026 00:10:20 GMT  
		Size: 46.0 MB (46021666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a90a216d1031db6d29303b33d55963a8cceef8f1b9ed71480501428b334783f`  
		Last Modified: Tue, 07 Apr 2026 01:32:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0de792e8c430dab2edc6ecee7fd56e823e43a55e11c8e7a28bab42cac15e4a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4031aa4d7430ecc6d94442595fe2e697cb944ae2c52770c0bbad50d78525200`

```dockerfile
```

-	Layers:
	-	`sha256:27dfe2774b44de12c989a16f2e5885e8bc18cfe0109eee5f0f11059897054187`  
		Last Modified: Tue, 07 Apr 2026 01:32:01 GMT  
		Size: 3.7 MB (3734275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1422265204b9896932260e73a90cc80425689d38db0fae263eab224c2913ea93`  
		Last Modified: Tue, 07 Apr 2026 01:32:01 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:220973eabc534591fa5337dc2b77cf0f133901d2e578a5d86f3ccc00523e6f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44207880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb222913ab4303ae31859fd0f720188db034b6009dbb1422b95c4c5498a4a83`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:14:26 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a78e7b2123c5c35e65ee1cc17df0d11c1db8ab3c4fe80b457270c2d9ae5003b1`  
		Last Modified: Wed, 22 Apr 2026 00:16:29 GMT  
		Size: 44.2 MB (44207655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ecbc41b1ffa11c8aca5f55316103fdfd4fd622e29d09b9978a038fcfbe3c38`  
		Last Modified: Wed, 22 Apr 2026 01:14:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:21a053ba722afc9c2a3c189ab9bfc6533d340b227501b6681f4e336c6c8dbf64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2729a3a7ff0b1507195805448a6fd97b7bbfc60c2179ac74402f9cd63d3f32a6`

```dockerfile
```

-	Layers:
	-	`sha256:4918a653f0fc4d455cfd73122f2be42ec1e7c0d14d92d3d81856c4c1722e838b`  
		Last Modified: Wed, 22 Apr 2026 01:14:33 GMT  
		Size: 3.7 MB (3736253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0b363f1f0b014b79c799cb3e35d686fd2441c74ff88f709819623e3145cbb0f`  
		Last Modified: Wed, 22 Apr 2026 01:14:33 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:da1a0be836c8b84a5417ab149b490c1bd16dc142f13cc61f12a5efeae7be6fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48373295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b46cba66d0a968abf1ff1cc47ed6463052558474f6216e2bd594f4accf5a25`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:14:38 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72a4f55194fd7bd6bc949b7c9f0f3a1b4f0ff21c67f42d855c34fccb0138365`  
		Last Modified: Wed, 22 Apr 2026 01:14:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:73840076b1274a9b44d5a61c65736c83c91bc1d8643e6c9f445b0f24429cb11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039e348aaa8ab07d84ef7bedd27f8ecb30ce3b7c4ceae5556cbd6ef09bbef973`

```dockerfile
```

-	Layers:
	-	`sha256:e75460ed71d34102c688dcd19a60db7f45b0feb7e84f8096191e30c3bc96d2da`  
		Last Modified: Wed, 22 Apr 2026 01:14:45 GMT  
		Size: 3.7 MB (3734289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1e92b8f218bad77077cfc6819167cc97779bf26091e998fa25bc531b760cdaf`  
		Last Modified: Wed, 22 Apr 2026 01:14:45 GMT  
		Size: 5.9 KB (5872 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:75d097f309cb8bd63d0fd88d3dee4e862b29b8425416ffcd8cd24f3da8b53129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49478138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44cca8449fa4c5e18e23fdcef2c966d3f491232e50d95b90043cf39484aec19`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:15:24 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6b838e591408b61fcf923bcc567649c4053d737a0dcf488cb215bcd633b7d70f`  
		Last Modified: Tue, 07 Apr 2026 00:10:40 GMT  
		Size: 49.5 MB (49477915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b09c7b20dc45df2879aeb4e61a350bc4444bc4bb69f1046c9609227ad7a852`  
		Last Modified: Tue, 07 Apr 2026 01:15:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0c594aaf93adc89abfb12c42bde7d30b49dd89ef348ec4e6adeec8271d6bad21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563af9ce58e61087ae6dd8083bc4200bf0e6fdca47e3529d22cdb96039913072`

```dockerfile
```

-	Layers:
	-	`sha256:a1f81dc846478326b845a167a9a72bf7c7d08b384eba156901923e0490b4cfe7`  
		Last Modified: Tue, 07 Apr 2026 01:15:31 GMT  
		Size: 3.7 MB (3731270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:027d259444e83e44264075f5eaa4ba854be8b8be6eff56b4bea02a5e9de24e98`  
		Last Modified: Tue, 07 Apr 2026 01:15:31 GMT  
		Size: 5.8 KB (5787 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:8809401abffe07befb9e4c2e9df167c2cd4e8bd18c483cc0f8479f4dae3f13ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48782670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869e05f97a8044f4af9a0ecb8607ff59447b2f1379b5796d57fc116af9cd52d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:20 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d3be957b775aeb19be93537211a85a2a31f49a07f3bbc6044dcea43e1c8ad87b`  
		Last Modified: Wed, 22 Apr 2026 01:25:51 GMT  
		Size: 48.8 MB (48782445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712f134d6beafef8a798620ebd5bf84e54fb94eeff9d3fb9335769e12519a252`  
		Last Modified: Wed, 22 Apr 2026 02:18:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d1141929f710aafb31c3394dd97d25d75876c3e2c3efd24f9af0d04cdac555bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6609b59824a355cc9e179eab68d785d239f68185542888531baa69b4030405a7`

```dockerfile
```

-	Layers:
	-	`sha256:a1bce92d8b51456602e5666772c7a74aee932febd737822b7e9100b43734b470`  
		Last Modified: Wed, 22 Apr 2026 02:18:37 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:a1acda4117a8e54b991d4ccc10f53c3de21e4d1878fa1ac3c9313c95005f5cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52337163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82fb0426ba4ba75e408046ad5a2b7b10cda6799ff0d3d15b5e81312104bc8da7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:15:32 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6758f39ca54389f9a277f38a7bb3476c7bf14ee0a9d3bf6cec18b29dde4c5969`  
		Last Modified: Tue, 07 Apr 2026 01:15:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:aeec6c6f77dc850a7cf0afcd963e502505fd4ad53c063bea92d046a6e965060d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c83f6446c3d9bebc58c9ba82756ca6e3265a9558ff346f6a8f6aff73b4115e`

```dockerfile
```

-	Layers:
	-	`sha256:c16507a720c6c621c7ea54c83a4b3a50f9bd1b104cf38539f50340fba58ef12f`  
		Last Modified: Tue, 07 Apr 2026 01:15:48 GMT  
		Size: 3.7 MB (3738432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:733ac97c92aa74cb56ba8cf98263f64c8b77617b30a466e049b2bde060498ff7`  
		Last Modified: Tue, 07 Apr 2026 01:15:47 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:8136613527f18f03b543fb8e52b6dde5ab3363310bbedc9e4f6e6a060220e3ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47148194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4adb743f4ce165c81bdd668134a25b6dfdb62a3e13c81661607a36e8dbc5618`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:14:01 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139a27f74c8272ec3fe01116621131d155f567a643402bf3afc136c7e188aa06`  
		Last Modified: Wed, 22 Apr 2026 01:14:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b5fbc01b921cc4e80e597a92bab8840671880604314dc5b52c804095c31c3833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1d1d7a4c3ca02381d180b038cc147fd7a84ab423bd71318c53048f3857c50e`

```dockerfile
```

-	Layers:
	-	`sha256:5630cab3b5a6363ec8fad7a1a197dcabeb8cc1df16c37bff81ad91209a50a039`  
		Last Modified: Wed, 22 Apr 2026 01:14:13 GMT  
		Size: 3.7 MB (3730912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3415ee064c3c9252bce1f9d8d00092c6b7c92e726c1ff5c856e8ef9e17011cb6`  
		Last Modified: Wed, 22 Apr 2026 01:14:13 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json
