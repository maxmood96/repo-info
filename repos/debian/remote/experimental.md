## `debian:experimental`

```console
$ docker pull debian@sha256:80566e7a9c863bba64f4dbf4259ee8c598f2199fa2b4c43172cd57c3487f4d2b
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

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:83e3364aa8f8bbd991e5f5366e8532a2d22e5192d63867276f301e5d7a8f7117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48801435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e83a34174a05a80d3933d7a4fbd7e27c61ca4ff6fb419ac0df3529447d48ab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1781049600'
# Thu, 11 Jun 2026 00:16:06 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:3bf41c6beac627021d00de42cf6ec15c7e1b1f56b8857804c3893be504a82e66`  
		Last Modified: Wed, 10 Jun 2026 23:40:28 GMT  
		Size: 48.8 MB (48801215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da87f6a4185f0e90d1549b40e78e1dedca2e09d94eaab16b00cfd5f99fae651a`  
		Last Modified: Thu, 11 Jun 2026 00:16:12 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:db6ee3541c372553c0613836d626e256a1caa9d4f1dc15181a72721c106d7efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3159594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8bafd259de70f50d0332f4230e8da1be75ccc3bb29a2be183ff0d026d90898`

```dockerfile
```

-	Layers:
	-	`sha256:1bff96540666e8667544dbcf2a5222be8ad4d01c9b602c81fce022f63e682b49`  
		Last Modified: Thu, 11 Jun 2026 00:16:13 GMT  
		Size: 3.2 MB (3153493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c299b1cef527b87f6c729e3d41738093ac84744fe0ed0b96b00f1068fe62229`  
		Last Modified: Thu, 11 Jun 2026 00:16:12 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:50a67414152700293c945167d9e02373fb0d7511285c483190064539b528d41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45703464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6f574bfa6ae48ce19331c44d94214f6901c3f7704611114394145058b0808f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1781049600'
# Thu, 11 Jun 2026 00:15:50 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:1524f6b4e8c9238ab55d3db908a3db18254dd322b4c42e2ff2f1cc19fa718dc4`  
		Last Modified: Wed, 10 Jun 2026 23:42:36 GMT  
		Size: 45.7 MB (45703243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcebbc1308c4e2bb83478e863f02948b3ecd8b3ab345643bd56c51f18cab18a0`  
		Last Modified: Thu, 11 Jun 2026 00:15:57 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:c297f7de97d8bcdbe3ab5d6e2c1a698c32e3ff79683294c6ba4e255bba3b024f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9f2b5e9d545189e392ff777410de7cdc034473d31d02e34646398d8e2f43a3`

```dockerfile
```

-	Layers:
	-	`sha256:91d4815d2a28aec96c95980d1709a7fe11cee3d1cb538e1f4c521d49e059eb58`  
		Last Modified: Thu, 11 Jun 2026 00:15:57 GMT  
		Size: 3.2 MB (3154863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:057828255ae1c117d342abf1e3a41d98f4afa342d4e56305c0367b1620e69acb`  
		Last Modified: Thu, 11 Jun 2026 00:15:57 GMT  
		Size: 6.2 KB (6165 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:44d484272f49bf8bc16a05f872eb2956e54658d9926a59c691a3c4818fef1f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48818777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd91d46301b455256e2f1c837c6c277da08d46f536e98bc88bc055dae55e0ae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1781049600'
# Thu, 11 Jun 2026 00:15:51 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:2013e29d14d262335067ba78e4030316bbcc25514ad364894aa708695da87bba`  
		Last Modified: Wed, 10 Jun 2026 23:40:19 GMT  
		Size: 48.8 MB (48818559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc67737f39cda1b652ebdfcd83c11dc9aa1b51ed95da3688d6a9812cb271559`  
		Last Modified: Thu, 11 Jun 2026 00:15:58 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:39e1816679712620a28ac5b589d554ba85b91dc6d38171b1e0afc1ef95ed3b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3164356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539fe234bd6b4a1127d71d3e25d5a25235e86a6507862769c8b83d83d7d34f6d`

```dockerfile
```

-	Layers:
	-	`sha256:ad0884aa2fb43be419a21b75d141a64cd64a101b63ebf447dcaef94e7b7b3dd0`  
		Last Modified: Thu, 11 Jun 2026 00:15:59 GMT  
		Size: 3.2 MB (3158175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b2132ad385c7f881fb1a7bb8820a1bbc81075cd663a885faf2a57d21feb2ba5`  
		Last Modified: Thu, 11 Jun 2026 00:15:58 GMT  
		Size: 6.2 KB (6181 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:26f6d11ad1bfef1d369a49cd71f1fda5c12d2941a4c14bebb7dd917ed4b45b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6352d4ce8d436504cbc45bc2638a87792491b90d06e5d0a44b0305d6f78e995d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1781049600'
# Thu, 11 Jun 2026 00:15:33 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:768c0954354968ae3f6b8b077e8778267e5fec1936ef4c8e36cc858383809c83`  
		Last Modified: Wed, 10 Jun 2026 23:40:33 GMT  
		Size: 50.1 MB (50105402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08f245d9a01887feaf0ccc011c1c456af5a3a3f856e12c1b76bbd6fd591ef6b`  
		Last Modified: Thu, 11 Jun 2026 00:15:39 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:c1eb0cde974fdeae5c9b717618c446a8c50a2f3a6e1f7a1e0e3a0d27b0346f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8de0ca0eca418e652ff485b10e30bad6154db78da3f7c070e45424d4f5821b`

```dockerfile
```

-	Layers:
	-	`sha256:28143d97027aa10c04c89c735c6b088a0b74cfe5b6ec2b82796a062774740cab`  
		Last Modified: Thu, 11 Jun 2026 00:15:40 GMT  
		Size: 3.2 MB (3150689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e32371006008cdc991d0e5fb2509e98a96e265d7a8753b2bd5d43465d24d9b76`  
		Last Modified: Thu, 11 Jun 2026 00:15:39 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:a127be86b5667c1d78b33dee5628f2077e37691ec03fbbfcca4592d9415892ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54132734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf1c0cf98fceaaa3de688c7c54f1e7be4f25cb44718d7c56b3a841371d1efe7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1781049600'
# Thu, 11 Jun 2026 02:22:20 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:b481f6aea326660f823bd35084f00f23cdb96d598146df1d638885c65095306c`  
		Last Modified: Thu, 11 Jun 2026 00:25:13 GMT  
		Size: 54.1 MB (54132516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fd137f50bd290bc4f72df068ca753f04bcfd4895ba9e58c1364c117b110949`  
		Last Modified: Thu, 11 Jun 2026 02:22:43 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:6d955d6641bfd2521b1539ade2a862f3454e435a4c1f9384052c5c6f309fd28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3163135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99197869a78e4be5133edc9059b22a1302b136bb6a21b184fc61159edc49c6e`

```dockerfile
```

-	Layers:
	-	`sha256:827d18228c7f5146bbba7d42e75406cabaf51a3ee824664f5119f8d213eefa8a`  
		Last Modified: Thu, 11 Jun 2026 02:22:43 GMT  
		Size: 3.2 MB (3157002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1bca700a70f18471bca28c060d0a3d8b19495c95e3b4b91f9350cafd21e1d34`  
		Last Modified: Thu, 11 Jun 2026 02:22:43 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:b56ec6111581afe56aa28dfe61ecb8edf36ddaed78bef1e125ecead72e96d902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46911859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbef248d2f952ca8c9caeb3f0973e73eae59881fa0a36f1140aac413af0bcd31`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'unstable' '@1781049600'
# Thu, 11 Jun 2026 22:14:15 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:c0e26051220654ff731ce974aa5b98e09608b81b7a542d07c0e9586937157194`  
		Last Modified: Thu, 11 Jun 2026 03:03:08 GMT  
		Size: 46.9 MB (46911639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15008377acd341f6b2ed0f296696b334cb8e460ec71c448623514405606a9926`  
		Last Modified: Thu, 11 Jun 2026 22:15:10 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:ba806cfcbae54e97a67ad78167291d441da4e27a2da223458edcdba0bc138c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0d911827598b917e47143d3493b3216751602218aed3cf6309fce80eb5ec2a`

```dockerfile
```

-	Layers:
	-	`sha256:5a63e786df95b881b1e231eaedf42fa3fc37f10c4c0111cb0c80f88d32b90595`  
		Last Modified: Thu, 11 Jun 2026 22:15:10 GMT  
		Size: 3.1 MB (3145005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f382a92d62d2af8c082055f6a128d4970f8b34493b14075d55485107479c3f`  
		Last Modified: Thu, 11 Jun 2026 22:15:10 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:a9212d9cc48e1016641bcf74d23b49458cb35e349d5fe1e880119f90aa2d43b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48542043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366b8ff7bcdc80798023ef964c3346d4ddf891ffeb9075f83443a5b21ebda6b2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1781049600'
# Thu, 11 Jun 2026 00:15:47 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:bdfbdfa7b5eb06aab01b204c86c236e56fdbbfb4b11c743782ba3d02d5b5aa6d`  
		Last Modified: Wed, 10 Jun 2026 23:42:44 GMT  
		Size: 48.5 MB (48541822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be07f659ce4c0ee0c20d69e8a878cfc8b0222560d932cd147567796a2cd4f3c`  
		Last Modified: Thu, 11 Jun 2026 00:15:59 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:f7d110eaa84dfdf92ee61c49c505fba8bc9398b484cd6a0462e02e449f0a19e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e5a74c4ee64079a87c4097e445a39419f5ddc56554cb9efd91825dbcd01cd1`

```dockerfile
```

-	Layers:
	-	`sha256:ad9b4db57cc19a71e9418e47cbbd974acdce92fd59e7c5bfe8b2802b7d5e2882`  
		Last Modified: Thu, 11 Jun 2026 00:15:59 GMT  
		Size: 3.2 MB (3154944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec4c699563eb395369c394c977566e98118d8667da09b107aa2e5cc61af00754`  
		Last Modified: Thu, 11 Jun 2026 00:15:59 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json
