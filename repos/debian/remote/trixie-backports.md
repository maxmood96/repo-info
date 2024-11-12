## `debian:trixie-backports`

```console
$ docker pull debian@sha256:6ac049bc87f8669f86144e3929d2fe8b9f8e50864f95852f1be67cd87eab9e80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:24cb582b7e75794bf7ec62753320c6625ab27d98c8ff9b5a413ccd9ccac5f3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53226985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493613530154faab53511ebb921d5d86fe84b201476c620a66ed9882fb6a69a9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:723f7d6ce61509bbccf2af45aa75a4c5cd83b188d6e85822321cdc68268417bf`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 53.2 MB (53226763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc8d5ff90e18f3b967763a695420870e4a7d4c12c1e46fc4df292a02a5490ad`  
		Last Modified: Tue, 12 Nov 2024 02:01:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3b8826d3bff77c14f787f6adea58fabd68f90b130bd8fed89e9424eaec443aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3256207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd885a4d06821cab47fc35dd9aa677d76e1bebb825af69dd08cb47d7d5f8294`

```dockerfile
```

-	Layers:
	-	`sha256:126273a006d2f618bde047a16d451a91e78676a3024635df4e606614dd4a0e49`  
		Last Modified: Tue, 12 Nov 2024 02:01:51 GMT  
		Size: 3.3 MB (3250382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d7d0255cf969c3492ce0c59b82b63f63877de1d1533d39d8f6ffc1c4364f399`  
		Last Modified: Tue, 12 Nov 2024 02:01:51 GMT  
		Size: 5.8 KB (5825 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:4189cdc1cbe1b6eb0e2a447e0412740120a53bc566842d95fcd4011a8faebcde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50091746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb51ceeaeba2f93d3add994c02fb5ab54b7b00828d6f16e36909694c9825ff3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4ff391534f557bd19067799d6e6b7e386e43cbf7d061a795a182546eb2145e99`  
		Last Modified: Tue, 12 Nov 2024 00:58:57 GMT  
		Size: 50.1 MB (50091523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc778ec34a81ada63c63093f7da7ab9d9460091f4cefa742b79e1c31097eedc`  
		Last Modified: Tue, 12 Nov 2024 02:02:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:412296b4e718bc1bacbe3dee0d351e4ffe23122cdcb385f9ee455b97aa628dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3259083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec8655f53d4878e4d2003d7b015bba8ed8beb76a4128c1dbc2a0f151746a608`

```dockerfile
```

-	Layers:
	-	`sha256:51f3b3dfd2048ffc562095c090ada4c9b59853a4193d2b65f31496d664b775fa`  
		Last Modified: Tue, 12 Nov 2024 02:02:30 GMT  
		Size: 3.3 MB (3253204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07654f490ec6ea13312f0e612a73a4636dd6fa4a11d63e08078ab5e2f1ee62f7`  
		Last Modified: Tue, 12 Nov 2024 02:02:29 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:bf50540e695151357239471e0bc41328f43ecea69ce5394aa5e04f1d5acf6755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47681987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea6fcbe73d1d07afbd9848ba50491ee0f6637f8e8980977a9ccf4442b95d8c0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:da23906b82d0da338b0e507d1bef5cf2747e130d745e77708e8f5279af9a4764`  
		Last Modified: Tue, 12 Nov 2024 01:02:46 GMT  
		Size: 47.7 MB (47681766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f645fa86919288fac3af0a88745cac35c61fd7f590a06a8d08e3f86c3851db9f`  
		Last Modified: Tue, 12 Nov 2024 02:21:59 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4cbeeeb1e64cde955d3c15b8586a24d359a75b4abfdd31be41d7daf20f2b21c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3257819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11f2ff652bd8506e22366ecd23bd4aa1aef6c58d208082469db974fa9133ac2`

```dockerfile
```

-	Layers:
	-	`sha256:7d76932ea3897e008a6be95bb81f776e880b1c46020c500cce666d9cbfeb3249`  
		Last Modified: Tue, 12 Nov 2024 02:22:00 GMT  
		Size: 3.3 MB (3251940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc0136525c8da0ddc0cf1428da7c1bf6a58d9403fc68598640f0331f6566ad5c`  
		Last Modified: Tue, 12 Nov 2024 02:21:59 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:97c15acbe2431caf894faf964dc956303cf442ad60f8a7382b4c5ec46715a8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53670199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59afbc58f90c05b3446050fc84fd0770f4926411ebd6b98acb78137c66641e14`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4de57c6718ff0fb4c76cd3ff1a33db2bde24e482395a89d0d4f6c7e6b3c20f53`  
		Last Modified: Tue, 12 Nov 2024 01:03:14 GMT  
		Size: 53.7 MB (53669977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79d30893a4c9ead20450d3dfeb609ef4d4de4477791f8bf25531d3467537cec`  
		Last Modified: Tue, 12 Nov 2024 02:24:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e779e472293ddc9e96a4ba9ef51c3f83d3dbb7bb5a3eb6afae72827a08927ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3261768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed78f7ccc6df7d42f72062016ad4063e8ecb830f9dacc474b6170529e80e720c`

```dockerfile
```

-	Layers:
	-	`sha256:dba16b84faa8e84efa89dbbe5a116c70366eb1655c049d703f081b1aab424372`  
		Last Modified: Tue, 12 Nov 2024 02:24:04 GMT  
		Size: 3.3 MB (3255873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edd737662c6a6c2149af1bc107cb48c8de1be2229115e2f15ff400467f13bb19`  
		Last Modified: Tue, 12 Nov 2024 02:24:03 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:eb73fef64a60f5a7161f7f7a790cafd05e5f174998e224410a9c278e8fb7c025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54095380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449fcfe133c2c2c0a0bc415660df8e4f401d4141c7e9e231f250bdf695ec42ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a04f0591b5521dc9360454fa2fd6b21d9b7d989bb4c88327ad94f8282af3b267`  
		Last Modified: Tue, 12 Nov 2024 00:55:13 GMT  
		Size: 54.1 MB (54095157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053d9f9276c32dbe4ca6bf5b44d6716d251039c0647a019397c21981828ccd9f`  
		Last Modified: Tue, 12 Nov 2024 02:01:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4767e33f7950cf234ce2aa24c3c59635f7829d3309942659d9770ddee66290a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7300a2ea2819fd8f2668d990a411e43c788f2e5ae5c3d1127d71121d9a89495a`

```dockerfile
```

-	Layers:
	-	`sha256:8c9271c9bbaee1f4f2c8191ecc94fea3ba8f6cd5d907b52be8b3a9a21277e3e1`  
		Last Modified: Tue, 12 Nov 2024 02:01:53 GMT  
		Size: 3.2 MB (3246858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7d395d0c2af655c0f7d26c49075d05aa0d1f0b022f4918fd3456c9cfbde3f8`  
		Last Modified: Tue, 12 Nov 2024 02:01:52 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; mips64le

```console
$ docker pull debian@sha256:a282b1b269acd1c37bc38c4269cdef8c1706ed99156449b1837dd6c385a8f22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52200638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a98376c095b6cf4fc8c290647f56ce539154cd2fec7521bc5ec0bfea824c571`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e85824c3ce994136e0b1f6545ca38052c56e3faf7dc4ab5102ef2c2e357cee02`  
		Last Modified: Tue, 12 Nov 2024 01:08:01 GMT  
		Size: 52.2 MB (52200415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec1cd6bc910d20a14e158b826bed8e0da676c2c2f0c6429559a6cdd2a9fd269`  
		Last Modified: Tue, 12 Nov 2024 02:04:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fd8ffc1043310c71c57405ebd58e1bc1a5cb9f41119e29f441c3c653e7203f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1b0c4b9334fce1de44b26643e78da7e9d857b2284d3ba6a1c01f82fa410749`

```dockerfile
```

-	Layers:
	-	`sha256:8cc27ab190d27dbcb830710292e934b16ef488f123734fc528b45078cd426e42`  
		Last Modified: Tue, 12 Nov 2024 02:04:39 GMT  
		Size: 5.7 KB (5651 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:dff4b5985b212021c3d7797a13ca7c3a73480d7b753b336b0288e0f33f835115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57193822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5ecc5189aaa854562c076578254811953102b694cb7313fe2c8046f6fab79d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:554b3bf5ec10b22cc962f7afc042e96c50635c0e2b0d817544a202afc2a52711`  
		Last Modified: Tue, 12 Nov 2024 01:05:47 GMT  
		Size: 57.2 MB (57193598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258d7779756f8e8832c392e4d3d28e7c493d78eb9c24bf6eeaa11d2c9d614c12`  
		Last Modified: Tue, 12 Nov 2024 02:24:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:837008b73d709f22359d92f070cd62e902790e5574e28947626ef94624cf1d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3259938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44544c2185ab7d40f511c2fc25ab6774aa04bdbcbe703bfae33fff01b965c9a2`

```dockerfile
```

-	Layers:
	-	`sha256:5e8654e858ad409f8e57ec984c1beebebd293749de3d7737dbc984a5fe09c8d1`  
		Last Modified: Tue, 12 Nov 2024 02:24:51 GMT  
		Size: 3.3 MB (3254085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6de1160be441ecf0d930f10b454e138f7e48c6d2c91c9cb1d4fa668172e48d4`  
		Last Modified: Tue, 12 Nov 2024 02:24:51 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:f3a98a85dca871e514eaab9c42948cf56e447216019e04a894fa61bbc0317c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51645541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583d2500856d6240b36dba3455398a26d411d4067289b8365bc6a933bebee810`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6c0644a53f9d8330b6a97aeb19064d71ab40683038fde43670fa8e947f67221c`  
		Last Modified: Tue, 12 Nov 2024 01:07:41 GMT  
		Size: 51.6 MB (51645318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b6c31ee34e2cc28bd83bc2b4b7e49e18ab416b5954b144a6f7234005799b50`  
		Last Modified: Tue, 12 Nov 2024 03:44:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c32e2c48c92cbd7bbc5b91b5c33b7a2b02ab678cf545eed9321d23d99b9cc158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3248845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cee84bb60766bea7062cfdc13afe3ba5b83fe8af53b7c6479b1837939bbd715`

```dockerfile
```

-	Layers:
	-	`sha256:5d5cc61e4f043ae21c510538dc025595ce0cd44cd3004203a1b4cf14c5be9b38`  
		Last Modified: Tue, 12 Nov 2024 03:44:03 GMT  
		Size: 3.2 MB (3242992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:198d719974663fc36c26eca339ffef5256a737c524c895640da3e33cad10aceb`  
		Last Modified: Tue, 12 Nov 2024 03:44:03 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:cc25530837551c52687d531df25df50e3c79e3b7a2551c6be1ec80a898d6c257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52885708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088b85158f9bf987847e5da024b7be9e75b9f362b030ec5f7795c51d8f3d13c3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a54a131d29bb2d4a9258476cdcb51efa9314272b8894e2474e100e5d38d85679`  
		Last Modified: Tue, 12 Nov 2024 01:05:54 GMT  
		Size: 52.9 MB (52885488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132c034f46e8d32b8281daeb19a8322031a7b33bbf3ef4f583d516ff6efcc790`  
		Last Modified: Tue, 12 Nov 2024 02:23:06 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:306d1c68cced549e8b5de01c8d9439b0dbf8ab8704a79dbeafa7d1c5d9ada48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3257805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03939dde68a99fdfa5ed38292142f56aea0a2265dbf3f95cc3c9265ca04ee08`

```dockerfile
```

-	Layers:
	-	`sha256:0910122bb8d8e268a194246d8509164833593a462e42185d0c78ced378d35fd6`  
		Last Modified: Tue, 12 Nov 2024 02:23:06 GMT  
		Size: 3.3 MB (3251978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8818c777342fdd1aa0a7d9c80461a3760147f6a1e96a7b30aa0417381644ecc9`  
		Last Modified: Tue, 12 Nov 2024 02:23:06 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
