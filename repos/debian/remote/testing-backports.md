## `debian:testing-backports`

```console
$ docker pull debian@sha256:af6b740265ff5eae1da019d046ee273f895ebc3985a8ff3f3623afc52cd14092
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:d09a4a1ef6d1753416ccbdea5122041caf25dc0867d6e4a60bc72428087204ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52212568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721b4eec083572e567f655fdd1a46d64db41653e79b9fd1dd0a84430d1702069`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3f347830cf4f7180f9222c78a85b4f11b0f1761b935fc19393d6dbbe312d61d2`  
		Size: 52.2 MB (52212346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78ecb5873c6e0407b8f61e262e8399cbe14f8de8950dcd87f11d4df7ea0fe15`  
		Last Modified: Tue, 24 Dec 2024 22:13:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1a93a917fb2ea6b39445f7d78be6b9577211225ad57c16eb486cc20c37b6c7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3235900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0906c4729cf0938c38a64e7261c68e6cce3564dd7bcdaf88f3f58ab7e82bfc73`

```dockerfile
```

-	Layers:
	-	`sha256:c0f468012c61e0a8cf3ac55a6dcb9d43509bef0718b8cf956711eca33bde67ae`  
		Last Modified: Tue, 24 Dec 2024 22:13:51 GMT  
		Size: 3.2 MB (3230063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aac46d4904f229f43747eca439a75e8b74cbbf5abbdb9c1176637c4c05e598d`  
		Last Modified: Tue, 24 Dec 2024 22:13:51 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:b3b100ae6595ec9f959eda14f008c5f8f9bedaca7eb7d22fb9c12b3a519a93ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48739132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004a030d38eda2e4b80ba8ccc28280652b29ae17d30fa41661c040af725b4562`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'testing' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:be52cc98ec10663a1753e40008f3d9f6ebc40519fb17a595374acb5ba672c60d`  
		Last Modified: Tue, 24 Dec 2024 21:35:12 GMT  
		Size: 48.7 MB (48738912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c05e3c155a1ea9fc46c97bb66ab34cc7cef63f9b0cc142e444376987d3e2d7`  
		Last Modified: Tue, 24 Dec 2024 22:21:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d91b7422a216fb0d480c93dcc6b335a111268d4ab62907fdee619e5df3b3ecd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3238769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee1f392c73853cb8779854fea6322410d449cd30d211a5ead4fd791352611fb`

```dockerfile
```

-	Layers:
	-	`sha256:286919cad263ef2964cae4189b855b19947861685d1cc5061d4c1e1164458c3a`  
		Size: 3.2 MB (3232880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc0f4b472210eccf1ee4741597ccc8d5e31c2f48cf8948a201e593c1805065f`  
		Last Modified: Tue, 24 Dec 2024 22:21:13 GMT  
		Size: 5.9 KB (5889 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:d6eb105288f22d20a7e289554442da42424773ed982093cedc26d7b738df3018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46768181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012dc5bffff44d918345e219a209be03d970b02d5a1d29a7add6d7628a4ab838`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:09224a7e0b4e703929eacf79312b0755eeb8650608fb40c1847f2fcd131fc2e7`  
		Last Modified: Tue, 24 Dec 2024 21:36:48 GMT  
		Size: 46.8 MB (46767960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2869db4a4b843aee7d1ecc8efebad181f86464bb28e43e52bd4075da651195`  
		Last Modified: Tue, 24 Dec 2024 22:17:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:38cbd4f939b83f9ed18731c6f78bc7b44822e6de143d88e41f463bbeb1e44832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3237512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69e5c7c739f9c593bea6d7cac3e0a6af9eb1bcd26f4195c065b588a1ed85294`

```dockerfile
```

-	Layers:
	-	`sha256:09050b23e0bbec4e593699e29bc5e780183bbd76c47e5e7118207e3ca6a465b7`  
		Last Modified: Tue, 24 Dec 2024 22:17:55 GMT  
		Size: 3.2 MB (3231623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9afc645d3b90f49a8549b1dbe56a9b090eabec58570cfe432a094383f2c60bd6`  
		Last Modified: Tue, 24 Dec 2024 22:17:55 GMT  
		Size: 5.9 KB (5889 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:3db3b8c45d6e190d062ab95de6d9f8ac46f605ebe98047c0427dea22d7ca540e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52425791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338bb529176bf3ab425c489ef6761d0109ab818a6ef667f081024f3226ba97f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d8f29bdf85a39ccdf4b160ab3b37a62a8a18cc6101304fdffacb1bc375df5185`  
		Last Modified: Tue, 24 Dec 2024 21:36:39 GMT  
		Size: 52.4 MB (52425571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c57c1aafa4352f100107e0a81a6a817c13d674fe244adecd395d1b3acd7144`  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c61b88e9dd83089b65ba69e98e0f61b00252f5b30b62389f71fbef8a50b88798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3240175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704cb8ae2dfca2b7a034db1d8fec9f2b7fe44a52b943e4e2f05ae747c64c5056`

```dockerfile
```

-	Layers:
	-	`sha256:59cd86610564420cee0a44a3a56c880f072e3509620da777782dc9332bfbc833`  
		Last Modified: Tue, 24 Dec 2024 22:18:35 GMT  
		Size: 3.2 MB (3234271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e993dc8a4f50b29fba0409df9a266ef2fedc800afb9a9153fd902efc897d0585`  
		Last Modified: Tue, 24 Dec 2024 22:18:34 GMT  
		Size: 5.9 KB (5904 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:df40d2c4bc7ed31375b8421c9cf5a34e15098af94c28f3597698c94e56c21135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53029274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b858785d6bbc8c356aa7df3f1b93bd8b49bfde50333309efe49430363157010d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:afd04a62df45475c34ab1a55e9da73d216061aab75b5ca654ec0dbabfaa9bcd9`  
		Last Modified: Tue, 24 Dec 2024 21:32:40 GMT  
		Size: 53.0 MB (53029052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cfab0e1c19ee0ac0910581a7194e4ca55047a10f46fb924b46aa66186adbec`  
		Last Modified: Tue, 24 Dec 2024 22:13:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:71685132acd3cda3e989728ed83fc3e89ce52119367760a7c20e68a6c2539e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3232369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9822e4ad61267369e8ab853d330fa6f4ebe747ca266af4a67b6d0fe06bddef5`

```dockerfile
```

-	Layers:
	-	`sha256:ad3edb96e3f81e0eba4ebae7b5177b013e015d8b5072f946ef3c9501d7d078b5`  
		Last Modified: Tue, 24 Dec 2024 22:13:56 GMT  
		Size: 3.2 MB (3226551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25c39f560fbaf94c9515d272e6461cce6ab3d44be0ac71056cbb5e24bd7c85f9`  
		Last Modified: Tue, 24 Dec 2024 22:13:56 GMT  
		Size: 5.8 KB (5818 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:daba44d86e96af88b0325fcb9447e816ddb44a7f560ff47e4f186b5f75346df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51717061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ef21c765de46f7d1b4fc014b0fa59e8f931a6c6e6ac09a95bdf58a486b947c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'testing' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e6da5ba483963578b536e0d31f44abe8df72fbbe64f88e19e8a81b34ebfc3c65`  
		Last Modified: Tue, 24 Dec 2024 21:35:19 GMT  
		Size: 51.7 MB (51716839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f1ed4989c227923066721850e1221aa777dd25f6ac637b8abc0b4bf20bb5d7`  
		Last Modified: Tue, 24 Dec 2024 22:18:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:134b714e7c8d1c547f561bbb3055ac0653bde7715e2030c13de5e205d079b6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:841885af7726f8d5d62c637a97acd7e2d0d19f64437cb1d104b99574e2b97faf`

```dockerfile
```

-	Layers:
	-	`sha256:4443ef231d182376b226d90246da359c41a4230cc8ce17fdba9f46d95084a216`  
		Last Modified: Tue, 24 Dec 2024 22:18:35 GMT  
		Size: 5.7 KB (5661 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:03bbb2bdb2c6220a23871e588e8fec12d76354a41d6e0f6fbe85c5b279e8b795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56044321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bed6351c0a502f4c66ca6db8ba64a9700a78e1aa4f218e426a13bd3fd053c5a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d89488f7de60286ea45b026cff74b45fd66aadb657ccac6b26bfb68c2217f900`  
		Last Modified: Wed, 25 Dec 2024 00:35:20 GMT  
		Size: 56.0 MB (56044099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efd05aa869e026f639a11b1ce9609a42011656cb52790da08def5077e2f7148`  
		Last Modified: Wed, 25 Dec 2024 03:52:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c9c5c51eacfd45bf51c49cf59e23e187e301139d00f416dea53da46e15a3d472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3239611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3acbe9fd20288595c47d59372dd569545bc88d8d98e21febcb1e1206eb5f06e`

```dockerfile
```

-	Layers:
	-	`sha256:f1bb120fa669f1298af36e70dc3064b945e596ed645c78f7974e5bac2bd097b7`  
		Last Modified: Wed, 25 Dec 2024 03:52:11 GMT  
		Size: 3.2 MB (3233748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c70bb7d618e2a9be018bfa35350370ae2046ad425cf71b56f1fce7b63ddeefa`  
		Last Modified: Wed, 25 Dec 2024 03:52:11 GMT  
		Size: 5.9 KB (5863 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:fa3521d4b938839a08198830955d373a906b564b0ed2972ca434a0f0d7cd4b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50704795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8fcea4ebcbdce232dfa3bc7b63a2720e00135c4e3cba930a83031db7cd3fa1e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:08472a2c71afb313a23a9d9330a521aada323417db4b4a4aa870241914d76d46`  
		Last Modified: Tue, 24 Dec 2024 21:38:38 GMT  
		Size: 50.7 MB (50704574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4269dbf6e198128198bbad03a3f8ca83784d24402a09cb221d8e41cf9a0fe621`  
		Last Modified: Tue, 24 Dec 2024 22:17:31 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c9515a74a6e7ce8209ac6e1ce86f43912951d07ca0e9a03502fefbe91e9e989e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3229308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81da1338d7c5bb91fe31857dfd8ef84739104c9ad5d1053c0ac6d7bde8407c23`

```dockerfile
```

-	Layers:
	-	`sha256:fdf9527aa9b2d7e9a4dcb66c00fb019f53b72947b2286da9efad223fd2c7f2cd`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 3.2 MB (3223445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9cbfc259e24d9eecd9ed76163f4eea80c730b92ff63b73133aaa0a43ddf02a1`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 5.9 KB (5863 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:56d82821b99f0606e9c25ee0b6604e3f31316e876e158bbd31dcc139f0ad5964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52167752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7edabdaa07be7a957275faaf1c2d1392365294715d3f064574eb741c0997f1a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d4ad176155d7de1a9408f8a75122ec6d1bfb314b586705e42bcec6225e2d35ea`  
		Size: 52.2 MB (52167532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d30cd1db5ade3694e3356fd97cc384f566adb4d1f0eeda11df2396503d5fff8`  
		Last Modified: Tue, 24 Dec 2024 22:15:50 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9906426dc3d4d4d6807015dac14efaba026e8954f1761b86a1b1aad643d5e2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3237493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229d3d50bfc35523674c219dd26bdc6374a3169de3f136699c9c20c8c4dd817c`

```dockerfile
```

-	Layers:
	-	`sha256:a4bbf0470465340465ca634621e343f41f2d45d06bc005c17aa036eb79ea41cc`  
		Last Modified: Tue, 24 Dec 2024 22:15:50 GMT  
		Size: 3.2 MB (3231656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:023552034157a3308dc83707d32bcb06ab936ff837b6dbbbcec45cc7fa28c4fc`  
		Last Modified: Tue, 24 Dec 2024 22:15:50 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.in-toto+json
