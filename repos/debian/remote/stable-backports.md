## `debian:stable-backports`

```console
$ docker pull debian@sha256:af7e05bef15ae15bf53659f921fcd4b92250ccaa376ff947de7b75bd40977d96
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:a9e588d7d476d00648bf1365709b4eda3970e1e912dec00132647728f765b986
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54933019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f1b27a1422147523451dae0c7b818c307488bdb67beb78d8c60bc7ddf26f935`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:22:08 GMT
ADD file:7b727d1890d4b095dff203b031a2a19e353a385750824429519a9f040d8ba95a in / 
# Wed, 17 Nov 2021 02:22:09 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:22:12 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7e1d655ca55b087f26e6a4d1f91da9a4cc4fa789bfd442795a832c7df3e00d9a`  
		Last Modified: Wed, 17 Nov 2021 02:28:33 GMT  
		Size: 54.9 MB (54932796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d008e1150512b7fa05e2d552c4bd757024deb58c5f018bec01e22d4455d8757c`  
		Last Modified: Wed, 17 Nov 2021 02:28:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:639a9aa0feed80dfea328cffb6e717ff1aaa0e16f0896734e94ed18bb339a889
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52468083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97d8e81279709a13221d6f98915ad5ad1181b2b320a24c47ee311e5f4fe3052`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:54:47 GMT
ADD file:dc0277c2d1117cc93ebc43a4f89edada90697fad31cfe1d92a3fb87f17f8a9b3 in / 
# Wed, 17 Nov 2021 02:54:48 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:55:01 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:793e32da4ddbfcd80d9f2c88ccf7f1e4b1f8f3dcbf7b21649551274d2bafa5dd`  
		Last Modified: Wed, 17 Nov 2021 03:12:16 GMT  
		Size: 52.5 MB (52467858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0aecba74d1721ca83227f246931939b0c3d0e0ab07a2e516e3c2df44f5c386`  
		Last Modified: Wed, 17 Nov 2021 03:12:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a0a962ea97c7eb3e7f392816727f7ce54b15e0314cb8464dd0bad786aae7dd64
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50134369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26fc5ba15848f589fec1b4d50fdc2aebc3170114d9a80eba6699a072e4e1f54`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:03:59 GMT
ADD file:ca44c08236db78d5b80510c54cdee9150d6a9d941329c2beae1caac598751e6a in / 
# Wed, 17 Nov 2021 02:04:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:04:13 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:189f1a1f83bebf899831dd3d429cbad6c3a317cf7441cd397d2170d70a38bb63`  
		Last Modified: Wed, 17 Nov 2021 02:20:52 GMT  
		Size: 50.1 MB (50134145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b577c408d3e309c68e7e84153c035102adc60605230ac923be81173287988e`  
		Last Modified: Wed, 17 Nov 2021 02:21:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b7d77d784950050b9142e76ff2a4332f3d703ebe7d870ea351a4424430146df5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53619268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1080748dd6feefa12216691874d26c7285642aa8a08df2e753f2e9d88a6d9d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:07 GMT
ADD file:1a630039cb75bd98ec72465cbb0b0d8d5c5dc123f40d39f719d2bdd7d3e13210 in / 
# Wed, 17 Nov 2021 02:42:08 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:42:15 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f9d8cc8f1c6c951399aaf87bff2af9b7abf020cb01d5d29652d4654f5bf5e5bf`  
		Last Modified: Wed, 17 Nov 2021 02:50:27 GMT  
		Size: 53.6 MB (53619046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fbc4590ebb15316daaed18526114b8809eab2fa6dd2c42e1ce5811ad0500d3`  
		Last Modified: Wed, 17 Nov 2021 02:50:38 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:6107cd62b5d53991f2f61753044244ad4c580e8e2ba45d1a7c3b2d155d907f59
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55937796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ecbb7566b708aea1a420ff32e15567b664600fa67dde761660df9bded5867a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:41:54 GMT
ADD file:38ff296db73332304b676e3a4e5824dc9ce4327981ae00635074b24912464bff in / 
# Wed, 17 Nov 2021 02:41:55 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:42:01 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ca2ec0b8fb28a6ea0abe69c11184f760b137b0963c71cbb1039a7fa1ad757e0f`  
		Last Modified: Wed, 17 Nov 2021 02:51:29 GMT  
		Size: 55.9 MB (55937575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba31ead7ae256e458b038ab313a0f3015006f62508163e4d98a10c36cc5330ac`  
		Last Modified: Wed, 17 Nov 2021 02:51:40 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:9690345c0d0d1d882c0e935beca1d71525bf5aedb48d96f0b560004bf47e4a9e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53183968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95800ebf7376002f7c7d3e1fedc6a14df0d2bc1f98a6540b69087f5a24fe4712`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:13:11 GMT
ADD file:d9591a3b684c28012c5d38989bd97f91aea1a6c8fb10be2fcbdc4deda95400e3 in / 
# Wed, 17 Nov 2021 02:13:12 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:13:19 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b9eee255421b7127efa1307fe2a0eaaf2375a87446e236df18c87f8d2f7dd067`  
		Last Modified: Wed, 17 Nov 2021 02:23:49 GMT  
		Size: 53.2 MB (53183745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c034ff3c389aba87742de0c03d82fd56f2677bb1da0f9774b33def1c4650411a`  
		Last Modified: Wed, 17 Nov 2021 02:23:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f9d1a613941ab711d46f651e2bdff5dfb03990319e2862f183b23d7f0be49d02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58809102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2cc8c6a11ac4da588195f52aec612546ecebdf7035b94a4af27f1cd2a3a5d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:28:41 GMT
ADD file:50a64f2cbd267a73c297febc1aac2d0a0ff0966d105e37c199477a326aa29e76 in / 
# Tue, 12 Oct 2021 01:28:47 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:29:07 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f2a063c91861196790fc45eaacac95fcbb278654c161c3397bc453aafb71bc96`  
		Last Modified: Tue, 12 Oct 2021 01:42:23 GMT  
		Size: 58.8 MB (58808876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57eddd7aa238ee81fabbae668fbfcc0a525fba6c00d486f0d622a00a6347a06a`  
		Last Modified: Tue, 12 Oct 2021 01:42:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:4c4742de8edf8878fd23c7cd11e2a71a07ee3230b604143237af932d6ec1ac09
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53207379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e76f0a1673c1760155300519c0fa60733713fab06ff835210b7f2e77823082`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:44:11 GMT
ADD file:f1ea9110d656eb3478ede77049c3fea3eadf89037d13f2b6799ce8c86708778b in / 
# Wed, 17 Nov 2021 02:44:13 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:44:20 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7a62fd5c373212657c719868b2144dd6f23387e47af5bda68af8785210025ec9`  
		Last Modified: Wed, 17 Nov 2021 02:50:12 GMT  
		Size: 53.2 MB (53207157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1393d13e4a191ed8615f817e0422c47b3976ea05c8ea4c2688b4492d0e5bd2`  
		Last Modified: Wed, 17 Nov 2021 02:50:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
