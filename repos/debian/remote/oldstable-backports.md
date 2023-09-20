## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:ef76079f2b4c81dcb41e84fc04f498943751c1a7161154fa206d5e5bac5c4e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:bde4642431cb6c0887dec5d74258f72ca6a0135124114c636f7d54a5bdc1318e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55056924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486429588c85b5b240b918a7a728c16563854cfd71e1165adc2f3c3abd417855`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:56 GMT
ADD file:5ddd46193e88de9c4805490b6be8adec88d9fff72c6abdc4180fb2b03d02de64 in / 
# Wed, 20 Sep 2023 04:56:56 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 04:57:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c9b646f5dff3118490eab81e47a0b1c7c1f431f0da99a0c786b44c335ebefe95`  
		Last Modified: Wed, 20 Sep 2023 05:02:36 GMT  
		Size: 55.1 MB (55056698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d9b10f01dfece3ede37f62a0c0345afcda139a56d7e2ef4b7d24b2d8eb4a7c`  
		Last Modified: Wed, 20 Sep 2023 05:02:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:4386958b015f7e44bd738ec9710928c4faeddd65d50fe1816273ca03abb9bb68
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52558398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d825a2d2e14dc9c06d92736da5da3ba08f9e249ac0c03e784080641e592eb6fa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:50:35 GMT
ADD file:6585afdc8b7840bcbfa96fcb0bf0d7d7e9eb5539dd1cec70e5ee6f31209ad3d3 in / 
# Wed, 20 Sep 2023 00:50:36 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 00:50:40 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ea4d6080a0290f592c439c3add7fef2662b6e325c704d049e34f299626e409dd`  
		Last Modified: Wed, 20 Sep 2023 00:56:03 GMT  
		Size: 52.6 MB (52558171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4209b7809d4853aa26fd899302544e9e1180418b029b1ce42bd978582e9dbf05`  
		Last Modified: Wed, 20 Sep 2023 00:56:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:46885fa518d66ef5616858e12ef3e68388b8e26c05ea2ad2c6ed5810d8aa0456
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50219802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7dfd7078a4f07624b7eeceee0551adce1a26de4efdcb926b783fbdc50b9bee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:58:21 GMT
ADD file:da06a7eb60fa7e98b33b11573c74311e8a114bdf9f9f053590847f8c28037f22 in / 
# Wed, 20 Sep 2023 04:58:21 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 04:58:24 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d1bdee0ed20ecdbbdfdf6a7d4894a70819216c123c0e73cfc069612c7fcfe1ca`  
		Last Modified: Wed, 20 Sep 2023 05:03:31 GMT  
		Size: 50.2 MB (50219579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b33f03296d522300dd33b4ffa583b59a4a14e682b978fe604569082661436f6`  
		Last Modified: Wed, 20 Sep 2023 05:03:40 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c0015d6f7e307abf5e8dbbc0e59256b24225e5a2519b6027d45a10239c6c119a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53705106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d856472b558fc55d617578865a34db42d1fb4bfc86510e7a6a8e9958f6435a3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:45:02 GMT
ADD file:d17683ba7f6b9175b6b7355c2a92df3ac32d932885900024a59637e9e84daed8 in / 
# Wed, 20 Sep 2023 02:45:02 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 02:45:05 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0250f3c681d4d2407c6615b27e9cef12ae5c5df4efb11d3c6073565ea79cd584`  
		Last Modified: Wed, 20 Sep 2023 02:49:35 GMT  
		Size: 53.7 MB (53704883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d21f03d83f060d7bd6a6596a5f7cdde8753dd313babc062d554d186fd03e07`  
		Last Modified: Wed, 20 Sep 2023 02:49:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:4ba1e830424d3a22ddde701827c75cace333d24ebc11a12962d85387bcae17cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56040710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b63c27a3887663d71b353e811a74bf4cf99096ed1b86d514f781a8ca6ea2bd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:43:15 GMT
ADD file:4972d10c6107fd20bf98c1c94a441e2cb3d14a625feb9e293d0b7527d3c8efbf in / 
# Wed, 20 Sep 2023 00:43:16 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 00:43:19 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:73d05fbd9bfd3b656f84a6e1bc2e910f22de1d965198a98739ccd97ffb57a9cb`  
		Last Modified: Wed, 20 Sep 2023 00:49:26 GMT  
		Size: 56.0 MB (56040484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3508dc8e0165a6fa72f96bd91e0c60ed4728c023d52bc243d580fe6177926b06`  
		Last Modified: Wed, 20 Sep 2023 00:49:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:6d9a9a5685c9c2b118859c74005a6dbc36b4c4c212670e197fa9225076653da0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53271806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c0daec3f99022821762b122540811baf035ca3bd95f6c201cceae7c07e1f8f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 03:11:50 GMT
ADD file:b66228ed1d56adafcf09e54a7851e635c035f251b00b1b0d21a0abaa88ecbf07 in / 
# Wed, 20 Sep 2023 03:11:55 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 03:12:10 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a544bd17008b1d9674e58ea820849b847656ef432805f1935b82a7322697869f`  
		Last Modified: Wed, 20 Sep 2023 03:23:10 GMT  
		Size: 53.3 MB (53271579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb732a0ea07be713dfd4b4a74f744ab03dca30dade7566c99c957621e4fd56f`  
		Last Modified: Wed, 20 Sep 2023 03:23:19 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:adeff5bb5581d2bd6fb2cfd44fd4107fe80c99093335b1188c46bbf13ba730e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58928725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861f4d8abdeef1be45bbefc806bac31545a475c35ba0d803e33a82746ce7f212`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 07:53:46 GMT
ADD file:9b72928499a8bf43f01e19e05193caf855704b43fe5718d7366a402ccd064902 in / 
# Wed, 20 Sep 2023 07:53:48 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:53:54 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:aec31260297ea68be330bf171fc9766db9b899db3aaf1b9e92ab5cfe9a7bc7a0`  
		Last Modified: Wed, 20 Sep 2023 08:51:10 GMT  
		Size: 58.9 MB (58928500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f615a8abaaf69cc6d93f68420017e340ebe0dc5dce4dd0c3bdd03927eceb272d`  
		Last Modified: Wed, 20 Sep 2023 08:51:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:c8dab8cadc970bb49ccf10d4c9aeb77b0b1ff0fd529361512d9a284ab9415449
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53291009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277eca3e137e8ce45e36aef3ec6074f26f1da1d3a1bd094baae86c9302efec2c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:55:06 GMT
ADD file:70ff196e59910a6b186b452eceb08d0c1512341259f133883037b5a812790449 in / 
# Wed, 20 Sep 2023 02:55:13 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 02:55:20 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3f4df5cb857850953aef5626bd4096d5e588a823a5d9609a0e147b118c9a539e`  
		Last Modified: Wed, 20 Sep 2023 03:00:37 GMT  
		Size: 53.3 MB (53290785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efd46ce1d19cb915e216266c3c1042d60d099d39b16c8e34477dc62a0818686`  
		Last Modified: Wed, 20 Sep 2023 03:00:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
