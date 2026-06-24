## `debian:experimental`

```console
$ docker pull debian@sha256:e4f505d7fff407a21c3352a3f68590f4304f9911e023644b2c539c95be348a4e
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
$ docker pull debian@sha256:8866b9fcfe7f988fce7f8e5654afc896b0c75ee9b9b349c1d7cde051e7740e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50081183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b75e55ff70e2fe4d955f909f611b03b6592b707ff42567a3331bad1b7933c58`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1782172800'
# Wed, 24 Jun 2026 01:15:32 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:bed0e6913ef7c7ed2ab16147605f7d539c9bceaa7c32bb8b2ead5e074741d2bd`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 50.1 MB (50080962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91914a850def70437d0803fd792b7648ad19b439ab37dcf008eb3bab053c9e34`  
		Last Modified: Wed, 24 Jun 2026 01:15:38 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:3221cb256eb16c1b5918a70c4d73a40da5ffec745f9d84e32ef52859ced40906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff74e93bba584262fe089712e08af0e746050081976d6b9fd867794efb9b900`

```dockerfile
```

-	Layers:
	-	`sha256:fcc168c3cb9d1641e96e84ef7e6e0cf29798afd018d5bf83bdde96330c124951`  
		Last Modified: Wed, 24 Jun 2026 01:15:38 GMT  
		Size: 3.1 MB (3148865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87cbb4a9c93d74f7a059212555a479eef8feac94eed4a8023d55b173acce83c7`  
		Last Modified: Wed, 24 Jun 2026 01:15:38 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:1f40db0a107ca092a1ca302573d2657920910aa7b4cd1151ea5639df2a5f459c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54098205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291f2f41a4f476a1efbe05a5ab46555c492692ef104c6c757fec22c0e296b342`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1782172800'
# Wed, 24 Jun 2026 01:15:58 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:df0906e3cb637fbba0e983f5f83d8b95284187794c6fcd307923e2706e29c920`  
		Last Modified: Wed, 24 Jun 2026 00:31:03 GMT  
		Size: 54.1 MB (54097985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366d211411541eda782599897680c0ebe8042b2a8de5229ab7954e38c1771584`  
		Last Modified: Wed, 24 Jun 2026 01:16:11 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:d1ce40afed78f29517ce7618d22e42daac38dd1679f6b08b3634634b891cdb15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c778ec725c3f29c5212514b97c4d4cb50ef1ad616e56321d73ce0ae2f84d3e`

```dockerfile
```

-	Layers:
	-	`sha256:23ef88961c537bc392824d43b7bc35f4c267e216362a732155b31ddfac3e594f`  
		Last Modified: Wed, 24 Jun 2026 01:16:11 GMT  
		Size: 3.2 MB (3155169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc62e639c6b9fee6bbb0c010aefff4705a85d4f4b1878bec076d0ff36ebf903e`  
		Last Modified: Wed, 24 Jun 2026 01:16:11 GMT  
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
$ docker pull debian@sha256:f539a87e5ffc3fd25afc355af5107ff0c5e1e52f85747d7fa71a7a85623f457e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48518024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b303e50f37a85910f6a7aac7930812b71a7a10dcfe10f8bdd0c6f3b82cb713c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1782172800'
# Wed, 24 Jun 2026 01:14:34 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:9d0a24e2e28b0d2f4b1099d1d9891107922d94e2cbcd230e7347b8eb742a5558`  
		Last Modified: Wed, 24 Jun 2026 00:28:47 GMT  
		Size: 48.5 MB (48517803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dee08a47f52be7aaad8537b68398f610b26059f07e2b557ffea6828f505387`  
		Last Modified: Wed, 24 Jun 2026 01:14:45 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:ef33f2b21c86fd08a97845ce9817e2228e558c037f3c08658297cc6ac2c515f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3159218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef41666184a38fdb2e32d72cc9ed513194bccf2e5c958c9a71edac0f48b3275b`

```dockerfile
```

-	Layers:
	-	`sha256:57d0e78c73af40bc94cd66e94900189a2b742e9e044fd63cebe73dd0c7dd6b10`  
		Last Modified: Wed, 24 Jun 2026 01:14:45 GMT  
		Size: 3.2 MB (3153117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53547ea1c95939b7fd211217f55bb3c2eddbb703593f5e981468ccfc18532382`  
		Last Modified: Wed, 24 Jun 2026 01:14:45 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json
