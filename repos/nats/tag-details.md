<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.19`](#nats2-alpine319)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.19`](#nats210-alpine319)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-1809`](#nats210-nanoserver-1809)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-1809`](#nats210-windowsservercore-1809)
-	[`nats:2.10.14`](#nats21014)
-	[`nats:2.10.14-alpine`](#nats21014-alpine)
-	[`nats:2.10.14-alpine3.19`](#nats21014-alpine319)
-	[`nats:2.10.14-linux`](#nats21014-linux)
-	[`nats:2.10.14-nanoserver`](#nats21014-nanoserver)
-	[`nats:2.10.14-nanoserver-1809`](#nats21014-nanoserver-1809)
-	[`nats:2.10.14-scratch`](#nats21014-scratch)
-	[`nats:2.10.14-windowsservercore`](#nats21014-windowsservercore)
-	[`nats:2.10.14-windowsservercore-1809`](#nats21014-windowsservercore-1809)
-	[`nats:2.9`](#nats29)
-	[`nats:2.9-alpine`](#nats29-alpine)
-	[`nats:2.9-alpine3.18`](#nats29-alpine318)
-	[`nats:2.9-linux`](#nats29-linux)
-	[`nats:2.9-nanoserver`](#nats29-nanoserver)
-	[`nats:2.9-nanoserver-1809`](#nats29-nanoserver-1809)
-	[`nats:2.9-scratch`](#nats29-scratch)
-	[`nats:2.9-windowsservercore`](#nats29-windowsservercore)
-	[`nats:2.9-windowsservercore-1809`](#nats29-windowsservercore-1809)
-	[`nats:2.9.25`](#nats2925)
-	[`nats:2.9.25-alpine`](#nats2925-alpine)
-	[`nats:2.9.25-alpine3.18`](#nats2925-alpine318)
-	[`nats:2.9.25-linux`](#nats2925-linux)
-	[`nats:2.9.25-nanoserver`](#nats2925-nanoserver)
-	[`nats:2.9.25-nanoserver-1809`](#nats2925-nanoserver-1809)
-	[`nats:2.9.25-scratch`](#nats2925-scratch)
-	[`nats:2.9.25-windowsservercore`](#nats2925-windowsservercore)
-	[`nats:2.9.25-windowsservercore-1809`](#nats2925-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.19`](#natsalpine319)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:48c5f766b807ecc4c1d1cbd8ae4cb613e9239c698d2483b907d94cfccb4431ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5696; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:dbab4c53c0de6b089ceb67849d41bdf54a0ad29e50f1105048fc5f19508db803
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cbf0fba619173e5c4542920b1d7278a5a780baf2b54bff413b32cc0016433c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:06 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Sat, 16 Mar 2024 08:49:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:06 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866d738de7ab782f2ba4b31cfeee8894a26c596bed7b85f7072494d10cd5618`  
		Last Modified: Sat, 16 Mar 2024 08:49:54 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:23b831c97175a24dafc1e4858d66d89b5daea7b40475fa65a5a2cc646495f69f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f14c4fc39384124daeb9de82f2f548ed59cf95ac2c5163a4e7cb933758b47c6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:37 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Sat, 16 Mar 2024 08:44:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dcfc63d9869b797864f5925982e824e3b9ba24796e45cee98fa32eacb80c21`  
		Last Modified: Sat, 16 Mar 2024 08:45:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:d7d36063a70b3f92e87214db9cf07a81799734321a44db81a32d60f4dbe9747d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ed0bdac27116af7eb7ddd6d7e6b9ebd5fb952606a5faa4a84779b345103b0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:24 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Sat, 16 Mar 2024 00:53:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:25 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:25 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c56f0b0a93e98e48d30f323ee2f44dcffe8ee47dad4b9701cd95f33b1ad423`  
		Last Modified: Sat, 16 Mar 2024 00:54:16 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:17532cf8a200037fa12e16243b8739bc520937cd82a9a3b96d8db0e85d942071
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b75af84f70f1921e86eaa7dff023270dc485b37e1acca37fe2bc3e4e919f19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:08 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Sat, 16 Mar 2024 04:04:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:08 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:08 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3e7253e56d93fc4ce869656fef13511496d97e58250a301790645656c29acf`  
		Last Modified: Sat, 16 Mar 2024 04:04:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:bc4465dc1a2b2b68a903b34cd70721db4682b6ae49baad493c4fb8f9a54c1699
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123dd70806df1b073fab2d9d0cb4855270a447d3c72569af275ed24af793af46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 02:39:34 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Sat, 16 Mar 2024 02:39:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 02:39:35 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 02:39:35 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 02:39:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405bd5e4b794b6bad044e8744cf63ddd0f2e0001abde3c0b2b5e7a190706d5e`  
		Last Modified: Sat, 16 Mar 2024 02:40:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:b200d259ef6d710b801ba60a7f296791ebc5298d82db48b8f68cfc0bee79d15b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26134424de3ad1af4ffe096901272e7ea3dae1a93eeddcd6c110b08b29af4011`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 16:58:41 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Sat, 16 Mar 2024 16:58:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 16:58:43 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 16:58:44 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 16:58:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea5f20b9222048fdae4e26dc03a3a997375533021a900c72f4e6b338c144ddb`  
		Last Modified: Sat, 16 Mar 2024 17:00:32 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:5c3f90898e8204465bc8f03eeb287f3c4a74ab98abddf8e7133303a697cdcc15
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110558802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c9fe6985208f3c2b3d60ef9ba9dca290d513ed8dfd37ea890a5a30e3309db2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Wed, 10 Apr 2024 01:43:32 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:43:34 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 10 Apr 2024 01:43:34 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:43:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:43:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:43:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826d34fcda621b296890090998100732b227a2fded8eee4d47e58e23e4a707e0`  
		Last Modified: Wed, 10 Apr 2024 01:48:21 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a02eb33a3aa2cfe4eef717c0d9f835f089de87c8bf7a29ada529785e9a766d9`  
		Last Modified: Wed, 10 Apr 2024 01:48:20 GMT  
		Size: 5.7 MB (5663495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba1c2806f1a8f6a751f20ca92a1ce06f1e4694140d4837b6f890ce9e2bef92`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd1781b30607b707f2c7003388ad80836cdb8125e2d4376107843968a0d97ca`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72699a90a0ff719020f44581d9607dc75f34d1b9f79ad4baa1d2dd8a2a111558`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f3e31e8b287637780dd9b544fda9313c77847672463da5487a4f569ad663de`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:bca70839d95348452fb8363f4943e3d2a45fcbea78ff7749e2b5219abb34fdf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:8b4822683d7955dc4a7b69bc138e5a980297f5562d3dc4f8417d80aed7b8a683
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9577903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78fb4abc56d19dcdd801b05d2982e749107d24ec996403c499518e1fec1d0a50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:48:58 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 08:49:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:49:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:49:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:49:01 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:49:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27675e5d86d45eba74328ac05267b7f93df29e2f079892c96c4425c216de74c`  
		Last Modified: Sat, 16 Mar 2024 08:49:37 GMT  
		Size: 6.2 MB (6168174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996c3b4c0f3e26b6ebc651c10f1889f8cf2f401651631836d63f72a1f449e9f2`  
		Last Modified: Sat, 16 Mar 2024 08:49:36 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca260fdf9bf58bec6ebf64f52cc0437d3935f22572653de018a0912f276efc25`  
		Last Modified: Sat, 16 Mar 2024 08:49:36 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:7ea677c7520bfdf6e5e8ca9f6e7ea392d39d8204f89e90b17de4f4216ae2e4fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae73509d5009d4f8bf7d5827db756183e287715cdca6b2c362c186c38d174486`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:44:29 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 08:44:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:44:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:44:32 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:44:32 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:44:32 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c6c88a86c2d4fae1df9dcfb8d0fb887644ffaeea7c7552244d72831f2deff0`  
		Last Modified: Sat, 16 Mar 2024 08:45:05 GMT  
		Size: 5.9 MB (5884864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bd557199bb46ecdb92b5224c44b2fb88b65b1d11eb03799e5d96d916cd4a17`  
		Last Modified: Sat, 16 Mar 2024 08:45:03 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4185eaec9fd629a92d2e2fb33da18b3c5ead72abf7d6f01ab6eaea92405c0031`  
		Last Modified: Sat, 16 Mar 2024 08:45:03 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:cc8f002c98389809a6e45a18f22b1a4a139c42812baaa5d01c1e81d8e4874156
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8795632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a947e574f9d2508db10e0ea9c2958039f03b151091e939cca9d6de03f552ba7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:53:15 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 00:53:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 00:53:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 00:53:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 00:53:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 00:53:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f579c68c28c186f8b3430f408c338b656e0cb429709b80e5f128a681b11be03`  
		Last Modified: Sat, 16 Mar 2024 00:53:58 GMT  
		Size: 5.9 MB (5875734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aeaa4c17e704f2825dcc8ca7892e9f8f7ca1022cf1aaa902c2ac011371fce0a`  
		Last Modified: Sat, 16 Mar 2024 00:53:56 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92b079a7c6d0b0e9f500662cfcfa735481d84fa902b2b7a607b5855ba623866`  
		Last Modified: Sat, 16 Mar 2024 00:53:56 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3ffef78bc0ff99629b91518b700220c06965c730059865cb63f18b757b7efad8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9088776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9c7035c53282319802a6491562f8b5922be8f1a7cf414229eca258cc31b74b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 04:03:47 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 04:03:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 04:03:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 04:03:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 04:03:50 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:03:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 04:03:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7be0478b9e8861bced761c3e24515379aae8068c6aea93bb91cab613608206`  
		Last Modified: Sat, 16 Mar 2024 04:04:38 GMT  
		Size: 5.7 MB (5740063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aceb56880d89429044a8d940a472616c66a9a19bd96999dd010d6fdcd95b7ccc`  
		Last Modified: Sat, 16 Mar 2024 04:04:37 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c653aab8018aa291381d9c5f0b4ff56538e6b1d1898554ee4b4b16f5b3a0498`  
		Last Modified: Sat, 16 Mar 2024 04:04:37 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:3bc80e99b7b6d2ec499b278e79ad0f54c297b46fc348702243cfc9b9d8c7f134
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9078987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99796f4dcf8fdff5bfa05a8f5bcd649457ca09cae4aba1f7dd5c08f0c6000ba0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:39:10 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 02:39:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 02:39:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 02:39:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 02:39:14 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 02:39:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 02:39:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1071fa4f216f6a3b40e9ca688766e9de8cde369fb0bfd45a363d74ae53636f6`  
		Last Modified: Sat, 16 Mar 2024 02:39:52 GMT  
		Size: 5.7 MB (5719633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cd77000169deae54f01f9739a3fdb6b49bebed3c942a1574d742e0f559135c`  
		Last Modified: Sat, 16 Mar 2024 02:39:51 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbd40a91a6c30b4a91aed2555db43edf084fff2084b3ac0e2df8f21216f3ec6`  
		Last Modified: Sat, 16 Mar 2024 02:39:51 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:d0b935e12aa8b047de70c249972f46ec57c6f9be3578e0da0f9ba7c52799dddc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9296153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd63ac9e2a4893a8a1ad3ead3903faebfe84d0aa5bdbe202e312a428745a9884`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 16:57:27 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 16:57:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 16:57:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 16:57:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 16:57:29 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 16:57:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 16:57:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bf12bda37fb5c76daad2fd35782e3ee4b626ab41f2b6ced22cec58c28600ad`  
		Last Modified: Sat, 16 Mar 2024 17:00:14 GMT  
		Size: 6.1 MB (6052515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c04c6057db41f701360bac00f880c04931706790543ceaa183b7b35172a5f0`  
		Last Modified: Sat, 16 Mar 2024 17:00:14 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a4186c9454ae05d593569eb01415dd64d39fd53169f11984d7579581b331b`  
		Last Modified: Sat, 16 Mar 2024 17:00:13 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.19`

```console
$ docker pull nats@sha256:bca70839d95348452fb8363f4943e3d2a45fcbea78ff7749e2b5219abb34fdf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:8b4822683d7955dc4a7b69bc138e5a980297f5562d3dc4f8417d80aed7b8a683
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9577903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78fb4abc56d19dcdd801b05d2982e749107d24ec996403c499518e1fec1d0a50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:48:58 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 08:49:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:49:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:49:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:49:01 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:49:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27675e5d86d45eba74328ac05267b7f93df29e2f079892c96c4425c216de74c`  
		Last Modified: Sat, 16 Mar 2024 08:49:37 GMT  
		Size: 6.2 MB (6168174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996c3b4c0f3e26b6ebc651c10f1889f8cf2f401651631836d63f72a1f449e9f2`  
		Last Modified: Sat, 16 Mar 2024 08:49:36 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca260fdf9bf58bec6ebf64f52cc0437d3935f22572653de018a0912f276efc25`  
		Last Modified: Sat, 16 Mar 2024 08:49:36 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:7ea677c7520bfdf6e5e8ca9f6e7ea392d39d8204f89e90b17de4f4216ae2e4fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae73509d5009d4f8bf7d5827db756183e287715cdca6b2c362c186c38d174486`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:44:29 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 08:44:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:44:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:44:32 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:44:32 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:44:32 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c6c88a86c2d4fae1df9dcfb8d0fb887644ffaeea7c7552244d72831f2deff0`  
		Last Modified: Sat, 16 Mar 2024 08:45:05 GMT  
		Size: 5.9 MB (5884864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bd557199bb46ecdb92b5224c44b2fb88b65b1d11eb03799e5d96d916cd4a17`  
		Last Modified: Sat, 16 Mar 2024 08:45:03 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4185eaec9fd629a92d2e2fb33da18b3c5ead72abf7d6f01ab6eaea92405c0031`  
		Last Modified: Sat, 16 Mar 2024 08:45:03 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:cc8f002c98389809a6e45a18f22b1a4a139c42812baaa5d01c1e81d8e4874156
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8795632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a947e574f9d2508db10e0ea9c2958039f03b151091e939cca9d6de03f552ba7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:53:15 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 00:53:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 00:53:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 00:53:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 00:53:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 00:53:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f579c68c28c186f8b3430f408c338b656e0cb429709b80e5f128a681b11be03`  
		Last Modified: Sat, 16 Mar 2024 00:53:58 GMT  
		Size: 5.9 MB (5875734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aeaa4c17e704f2825dcc8ca7892e9f8f7ca1022cf1aaa902c2ac011371fce0a`  
		Last Modified: Sat, 16 Mar 2024 00:53:56 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92b079a7c6d0b0e9f500662cfcfa735481d84fa902b2b7a607b5855ba623866`  
		Last Modified: Sat, 16 Mar 2024 00:53:56 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3ffef78bc0ff99629b91518b700220c06965c730059865cb63f18b757b7efad8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9088776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9c7035c53282319802a6491562f8b5922be8f1a7cf414229eca258cc31b74b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 04:03:47 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 04:03:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 04:03:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 04:03:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 04:03:50 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:03:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 04:03:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7be0478b9e8861bced761c3e24515379aae8068c6aea93bb91cab613608206`  
		Last Modified: Sat, 16 Mar 2024 04:04:38 GMT  
		Size: 5.7 MB (5740063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aceb56880d89429044a8d940a472616c66a9a19bd96999dd010d6fdcd95b7ccc`  
		Last Modified: Sat, 16 Mar 2024 04:04:37 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c653aab8018aa291381d9c5f0b4ff56538e6b1d1898554ee4b4b16f5b3a0498`  
		Last Modified: Sat, 16 Mar 2024 04:04:37 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:3bc80e99b7b6d2ec499b278e79ad0f54c297b46fc348702243cfc9b9d8c7f134
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9078987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99796f4dcf8fdff5bfa05a8f5bcd649457ca09cae4aba1f7dd5c08f0c6000ba0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:39:10 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 02:39:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 02:39:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 02:39:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 02:39:14 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 02:39:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 02:39:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1071fa4f216f6a3b40e9ca688766e9de8cde369fb0bfd45a363d74ae53636f6`  
		Last Modified: Sat, 16 Mar 2024 02:39:52 GMT  
		Size: 5.7 MB (5719633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cd77000169deae54f01f9739a3fdb6b49bebed3c942a1574d742e0f559135c`  
		Last Modified: Sat, 16 Mar 2024 02:39:51 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbd40a91a6c30b4a91aed2555db43edf084fff2084b3ac0e2df8f21216f3ec6`  
		Last Modified: Sat, 16 Mar 2024 02:39:51 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:d0b935e12aa8b047de70c249972f46ec57c6f9be3578e0da0f9ba7c52799dddc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9296153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd63ac9e2a4893a8a1ad3ead3903faebfe84d0aa5bdbe202e312a428745a9884`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 16:57:27 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 16:57:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 16:57:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 16:57:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 16:57:29 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 16:57:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 16:57:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bf12bda37fb5c76daad2fd35782e3ee4b626ab41f2b6ced22cec58c28600ad`  
		Last Modified: Sat, 16 Mar 2024 17:00:14 GMT  
		Size: 6.1 MB (6052515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c04c6057db41f701360bac00f880c04931706790543ceaa183b7b35172a5f0`  
		Last Modified: Sat, 16 Mar 2024 17:00:14 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a4186c9454ae05d593569eb01415dd64d39fd53169f11984d7579581b331b`  
		Last Modified: Sat, 16 Mar 2024 17:00:13 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:0a31000c798112718df04a19491c39f2dd8e36ba4955b8b7a9987581d5f8a033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:dbab4c53c0de6b089ceb67849d41bdf54a0ad29e50f1105048fc5f19508db803
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cbf0fba619173e5c4542920b1d7278a5a780baf2b54bff413b32cc0016433c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:06 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Sat, 16 Mar 2024 08:49:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:06 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866d738de7ab782f2ba4b31cfeee8894a26c596bed7b85f7072494d10cd5618`  
		Last Modified: Sat, 16 Mar 2024 08:49:54 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:23b831c97175a24dafc1e4858d66d89b5daea7b40475fa65a5a2cc646495f69f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f14c4fc39384124daeb9de82f2f548ed59cf95ac2c5163a4e7cb933758b47c6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:37 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Sat, 16 Mar 2024 08:44:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dcfc63d9869b797864f5925982e824e3b9ba24796e45cee98fa32eacb80c21`  
		Last Modified: Sat, 16 Mar 2024 08:45:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:d7d36063a70b3f92e87214db9cf07a81799734321a44db81a32d60f4dbe9747d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ed0bdac27116af7eb7ddd6d7e6b9ebd5fb952606a5faa4a84779b345103b0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:24 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Sat, 16 Mar 2024 00:53:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:25 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:25 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c56f0b0a93e98e48d30f323ee2f44dcffe8ee47dad4b9701cd95f33b1ad423`  
		Last Modified: Sat, 16 Mar 2024 00:54:16 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:17532cf8a200037fa12e16243b8739bc520937cd82a9a3b96d8db0e85d942071
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b75af84f70f1921e86eaa7dff023270dc485b37e1acca37fe2bc3e4e919f19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:08 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Sat, 16 Mar 2024 04:04:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:08 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:08 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3e7253e56d93fc4ce869656fef13511496d97e58250a301790645656c29acf`  
		Last Modified: Sat, 16 Mar 2024 04:04:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:bc4465dc1a2b2b68a903b34cd70721db4682b6ae49baad493c4fb8f9a54c1699
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123dd70806df1b073fab2d9d0cb4855270a447d3c72569af275ed24af793af46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 02:39:34 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Sat, 16 Mar 2024 02:39:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 02:39:35 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 02:39:35 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 02:39:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405bd5e4b794b6bad044e8744cf63ddd0f2e0001abde3c0b2b5e7a190706d5e`  
		Last Modified: Sat, 16 Mar 2024 02:40:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:b200d259ef6d710b801ba60a7f296791ebc5298d82db48b8f68cfc0bee79d15b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26134424de3ad1af4ffe096901272e7ea3dae1a93eeddcd6c110b08b29af4011`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 16:58:41 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Sat, 16 Mar 2024 16:58:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 16:58:43 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 16:58:44 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 16:58:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea5f20b9222048fdae4e26dc03a3a997375533021a900c72f4e6b338c144ddb`  
		Last Modified: Sat, 16 Mar 2024 17:00:32 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:fb9a7b002fc37c676f80fe35573e4ade35e3429aa09510c6c9e90025dc498535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:5c3f90898e8204465bc8f03eeb287f3c4a74ab98abddf8e7133303a697cdcc15
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110558802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c9fe6985208f3c2b3d60ef9ba9dca290d513ed8dfd37ea890a5a30e3309db2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Wed, 10 Apr 2024 01:43:32 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:43:34 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 10 Apr 2024 01:43:34 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:43:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:43:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:43:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826d34fcda621b296890090998100732b227a2fded8eee4d47e58e23e4a707e0`  
		Last Modified: Wed, 10 Apr 2024 01:48:21 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a02eb33a3aa2cfe4eef717c0d9f835f089de87c8bf7a29ada529785e9a766d9`  
		Last Modified: Wed, 10 Apr 2024 01:48:20 GMT  
		Size: 5.7 MB (5663495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba1c2806f1a8f6a751f20ca92a1ce06f1e4694140d4837b6f890ce9e2bef92`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd1781b30607b707f2c7003388ad80836cdb8125e2d4376107843968a0d97ca`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72699a90a0ff719020f44581d9607dc75f34d1b9f79ad4baa1d2dd8a2a111558`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f3e31e8b287637780dd9b544fda9313c77847672463da5487a4f569ad663de`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:fb9a7b002fc37c676f80fe35573e4ade35e3429aa09510c6c9e90025dc498535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:5c3f90898e8204465bc8f03eeb287f3c4a74ab98abddf8e7133303a697cdcc15
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110558802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c9fe6985208f3c2b3d60ef9ba9dca290d513ed8dfd37ea890a5a30e3309db2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Wed, 10 Apr 2024 01:43:32 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:43:34 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 10 Apr 2024 01:43:34 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:43:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:43:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:43:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826d34fcda621b296890090998100732b227a2fded8eee4d47e58e23e4a707e0`  
		Last Modified: Wed, 10 Apr 2024 01:48:21 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a02eb33a3aa2cfe4eef717c0d9f835f089de87c8bf7a29ada529785e9a766d9`  
		Last Modified: Wed, 10 Apr 2024 01:48:20 GMT  
		Size: 5.7 MB (5663495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba1c2806f1a8f6a751f20ca92a1ce06f1e4694140d4837b6f890ce9e2bef92`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd1781b30607b707f2c7003388ad80836cdb8125e2d4376107843968a0d97ca`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72699a90a0ff719020f44581d9607dc75f34d1b9f79ad4baa1d2dd8a2a111558`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f3e31e8b287637780dd9b544fda9313c77847672463da5487a4f569ad663de`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:0a31000c798112718df04a19491c39f2dd8e36ba4955b8b7a9987581d5f8a033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:dbab4c53c0de6b089ceb67849d41bdf54a0ad29e50f1105048fc5f19508db803
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cbf0fba619173e5c4542920b1d7278a5a780baf2b54bff413b32cc0016433c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:06 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Sat, 16 Mar 2024 08:49:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:06 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866d738de7ab782f2ba4b31cfeee8894a26c596bed7b85f7072494d10cd5618`  
		Last Modified: Sat, 16 Mar 2024 08:49:54 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:23b831c97175a24dafc1e4858d66d89b5daea7b40475fa65a5a2cc646495f69f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f14c4fc39384124daeb9de82f2f548ed59cf95ac2c5163a4e7cb933758b47c6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:37 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Sat, 16 Mar 2024 08:44:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dcfc63d9869b797864f5925982e824e3b9ba24796e45cee98fa32eacb80c21`  
		Last Modified: Sat, 16 Mar 2024 08:45:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:d7d36063a70b3f92e87214db9cf07a81799734321a44db81a32d60f4dbe9747d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ed0bdac27116af7eb7ddd6d7e6b9ebd5fb952606a5faa4a84779b345103b0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:24 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Sat, 16 Mar 2024 00:53:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:25 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:25 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c56f0b0a93e98e48d30f323ee2f44dcffe8ee47dad4b9701cd95f33b1ad423`  
		Last Modified: Sat, 16 Mar 2024 00:54:16 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:17532cf8a200037fa12e16243b8739bc520937cd82a9a3b96d8db0e85d942071
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b75af84f70f1921e86eaa7dff023270dc485b37e1acca37fe2bc3e4e919f19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:08 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Sat, 16 Mar 2024 04:04:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:08 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:08 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3e7253e56d93fc4ce869656fef13511496d97e58250a301790645656c29acf`  
		Last Modified: Sat, 16 Mar 2024 04:04:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:bc4465dc1a2b2b68a903b34cd70721db4682b6ae49baad493c4fb8f9a54c1699
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123dd70806df1b073fab2d9d0cb4855270a447d3c72569af275ed24af793af46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 02:39:34 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Sat, 16 Mar 2024 02:39:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 02:39:35 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 02:39:35 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 02:39:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405bd5e4b794b6bad044e8744cf63ddd0f2e0001abde3c0b2b5e7a190706d5e`  
		Last Modified: Sat, 16 Mar 2024 02:40:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:b200d259ef6d710b801ba60a7f296791ebc5298d82db48b8f68cfc0bee79d15b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26134424de3ad1af4ffe096901272e7ea3dae1a93eeddcd6c110b08b29af4011`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 16:58:41 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Sat, 16 Mar 2024 16:58:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 16:58:43 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 16:58:44 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 16:58:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea5f20b9222048fdae4e26dc03a3a997375533021a900c72f4e6b338c144ddb`  
		Last Modified: Sat, 16 Mar 2024 17:00:32 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:b04dc3c962bbed963b7ed2272999339683a9eb46cdeaa06a77c1dbbdfe93b834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:29380f4863fb3a6f2b04217f477bee6eac525e6b36400d4446ee1680024de74e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2170781570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa73df6040c74fa785c0df500e4c8a7a76a5ce054b396330c2b4631b211c5a06`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Wed, 10 Apr 2024 01:40:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Apr 2024 01:40:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:40:04 GMT
ENV NATS_SERVER=2.10.12
# Wed, 10 Apr 2024 01:40:05 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.12/nats-server-v2.10.12-windows-amd64.zip
# Wed, 10 Apr 2024 01:40:06 GMT
ENV NATS_SERVER_SHASUM=bc944f832fdc3eaa0072c0a5e278efd672cec394159661070e7aea4f5d483cbc
# Wed, 10 Apr 2024 01:41:22 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Apr 2024 01:43:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Apr 2024 01:43:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:43:16 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:43:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:43:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6ae8ddefe4f7d0224959df0cc91d01044dce7f127ee7c23257cf0b63bfd7ac`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266ac5d9d5680f1e3a65f9d272fc3a2ab7f67eda1b00c961365853e0a9c3e27`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b45aa9398ff56a16e042bfdf01b44ff7daebf93e7cba5d601367d2c0e5a55ed`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe31b64ec7d8949724e118281dfca112c508483cc5b28076aaadd223f212b4a4`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f68caae1490441aa87bfa98ed09fc4717d036f13634615fe4eb4a1efe4925a6`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567ed00bc244d7ef610728b1545d39345e73e8e86ee441b586eea2238d1bf1dd`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 241.8 KB (241850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f8817e79dfbc8f56443618f486d64c5ac11608663b3bdf7a25f87f2412c473`  
		Last Modified: Wed, 10 Apr 2024 01:48:02 GMT  
		Size: 6.1 MB (6099353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60589928d42d9fc2f8e9ccd4a26ba13cebed25894380700f63bace8ca5fc27c0`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbe842b574fe798f092ac13841eea2cee6361f8232a3539375c0503e5911af7`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619674a0794dc85dc23997a189c9659f4612bf24f1fd187f2d26e38dbf6a8691`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd24c8b4dbeddc4174617445fd1d056589be9451dfd07af7f714867654c353f`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:b04dc3c962bbed963b7ed2272999339683a9eb46cdeaa06a77c1dbbdfe93b834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:29380f4863fb3a6f2b04217f477bee6eac525e6b36400d4446ee1680024de74e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2170781570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa73df6040c74fa785c0df500e4c8a7a76a5ce054b396330c2b4631b211c5a06`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Wed, 10 Apr 2024 01:40:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Apr 2024 01:40:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:40:04 GMT
ENV NATS_SERVER=2.10.12
# Wed, 10 Apr 2024 01:40:05 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.12/nats-server-v2.10.12-windows-amd64.zip
# Wed, 10 Apr 2024 01:40:06 GMT
ENV NATS_SERVER_SHASUM=bc944f832fdc3eaa0072c0a5e278efd672cec394159661070e7aea4f5d483cbc
# Wed, 10 Apr 2024 01:41:22 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Apr 2024 01:43:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Apr 2024 01:43:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:43:16 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:43:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:43:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6ae8ddefe4f7d0224959df0cc91d01044dce7f127ee7c23257cf0b63bfd7ac`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266ac5d9d5680f1e3a65f9d272fc3a2ab7f67eda1b00c961365853e0a9c3e27`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b45aa9398ff56a16e042bfdf01b44ff7daebf93e7cba5d601367d2c0e5a55ed`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe31b64ec7d8949724e118281dfca112c508483cc5b28076aaadd223f212b4a4`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f68caae1490441aa87bfa98ed09fc4717d036f13634615fe4eb4a1efe4925a6`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567ed00bc244d7ef610728b1545d39345e73e8e86ee441b586eea2238d1bf1dd`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 241.8 KB (241850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f8817e79dfbc8f56443618f486d64c5ac11608663b3bdf7a25f87f2412c473`  
		Last Modified: Wed, 10 Apr 2024 01:48:02 GMT  
		Size: 6.1 MB (6099353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60589928d42d9fc2f8e9ccd4a26ba13cebed25894380700f63bace8ca5fc27c0`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbe842b574fe798f092ac13841eea2cee6361f8232a3539375c0503e5911af7`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619674a0794dc85dc23997a189c9659f4612bf24f1fd187f2d26e38dbf6a8691`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd24c8b4dbeddc4174617445fd1d056589be9451dfd07af7f714867654c353f`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:48c5f766b807ecc4c1d1cbd8ae4cb613e9239c698d2483b907d94cfccb4431ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5696; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:dbab4c53c0de6b089ceb67849d41bdf54a0ad29e50f1105048fc5f19508db803
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cbf0fba619173e5c4542920b1d7278a5a780baf2b54bff413b32cc0016433c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:06 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Sat, 16 Mar 2024 08:49:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:06 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866d738de7ab782f2ba4b31cfeee8894a26c596bed7b85f7072494d10cd5618`  
		Last Modified: Sat, 16 Mar 2024 08:49:54 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:23b831c97175a24dafc1e4858d66d89b5daea7b40475fa65a5a2cc646495f69f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f14c4fc39384124daeb9de82f2f548ed59cf95ac2c5163a4e7cb933758b47c6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:37 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Sat, 16 Mar 2024 08:44:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dcfc63d9869b797864f5925982e824e3b9ba24796e45cee98fa32eacb80c21`  
		Last Modified: Sat, 16 Mar 2024 08:45:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:d7d36063a70b3f92e87214db9cf07a81799734321a44db81a32d60f4dbe9747d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ed0bdac27116af7eb7ddd6d7e6b9ebd5fb952606a5faa4a84779b345103b0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:24 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Sat, 16 Mar 2024 00:53:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:25 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:25 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c56f0b0a93e98e48d30f323ee2f44dcffe8ee47dad4b9701cd95f33b1ad423`  
		Last Modified: Sat, 16 Mar 2024 00:54:16 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:17532cf8a200037fa12e16243b8739bc520937cd82a9a3b96d8db0e85d942071
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b75af84f70f1921e86eaa7dff023270dc485b37e1acca37fe2bc3e4e919f19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:08 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Sat, 16 Mar 2024 04:04:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:08 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:08 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3e7253e56d93fc4ce869656fef13511496d97e58250a301790645656c29acf`  
		Last Modified: Sat, 16 Mar 2024 04:04:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:bc4465dc1a2b2b68a903b34cd70721db4682b6ae49baad493c4fb8f9a54c1699
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123dd70806df1b073fab2d9d0cb4855270a447d3c72569af275ed24af793af46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 02:39:34 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Sat, 16 Mar 2024 02:39:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 02:39:35 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 02:39:35 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 02:39:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405bd5e4b794b6bad044e8744cf63ddd0f2e0001abde3c0b2b5e7a190706d5e`  
		Last Modified: Sat, 16 Mar 2024 02:40:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:b200d259ef6d710b801ba60a7f296791ebc5298d82db48b8f68cfc0bee79d15b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26134424de3ad1af4ffe096901272e7ea3dae1a93eeddcd6c110b08b29af4011`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 16:58:41 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Sat, 16 Mar 2024 16:58:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 16:58:43 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 16:58:44 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 16:58:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea5f20b9222048fdae4e26dc03a3a997375533021a900c72f4e6b338c144ddb`  
		Last Modified: Sat, 16 Mar 2024 17:00:32 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:5c3f90898e8204465bc8f03eeb287f3c4a74ab98abddf8e7133303a697cdcc15
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110558802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c9fe6985208f3c2b3d60ef9ba9dca290d513ed8dfd37ea890a5a30e3309db2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Wed, 10 Apr 2024 01:43:32 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:43:34 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 10 Apr 2024 01:43:34 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:43:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:43:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:43:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826d34fcda621b296890090998100732b227a2fded8eee4d47e58e23e4a707e0`  
		Last Modified: Wed, 10 Apr 2024 01:48:21 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a02eb33a3aa2cfe4eef717c0d9f835f089de87c8bf7a29ada529785e9a766d9`  
		Last Modified: Wed, 10 Apr 2024 01:48:20 GMT  
		Size: 5.7 MB (5663495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba1c2806f1a8f6a751f20ca92a1ce06f1e4694140d4837b6f890ce9e2bef92`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd1781b30607b707f2c7003388ad80836cdb8125e2d4376107843968a0d97ca`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72699a90a0ff719020f44581d9607dc75f34d1b9f79ad4baa1d2dd8a2a111558`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f3e31e8b287637780dd9b544fda9313c77847672463da5487a4f569ad663de`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:bca70839d95348452fb8363f4943e3d2a45fcbea78ff7749e2b5219abb34fdf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:8b4822683d7955dc4a7b69bc138e5a980297f5562d3dc4f8417d80aed7b8a683
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9577903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78fb4abc56d19dcdd801b05d2982e749107d24ec996403c499518e1fec1d0a50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:48:58 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 08:49:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:49:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:49:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:49:01 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:49:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27675e5d86d45eba74328ac05267b7f93df29e2f079892c96c4425c216de74c`  
		Last Modified: Sat, 16 Mar 2024 08:49:37 GMT  
		Size: 6.2 MB (6168174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996c3b4c0f3e26b6ebc651c10f1889f8cf2f401651631836d63f72a1f449e9f2`  
		Last Modified: Sat, 16 Mar 2024 08:49:36 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca260fdf9bf58bec6ebf64f52cc0437d3935f22572653de018a0912f276efc25`  
		Last Modified: Sat, 16 Mar 2024 08:49:36 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:7ea677c7520bfdf6e5e8ca9f6e7ea392d39d8204f89e90b17de4f4216ae2e4fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae73509d5009d4f8bf7d5827db756183e287715cdca6b2c362c186c38d174486`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:44:29 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 08:44:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:44:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:44:32 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:44:32 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:44:32 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c6c88a86c2d4fae1df9dcfb8d0fb887644ffaeea7c7552244d72831f2deff0`  
		Last Modified: Sat, 16 Mar 2024 08:45:05 GMT  
		Size: 5.9 MB (5884864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bd557199bb46ecdb92b5224c44b2fb88b65b1d11eb03799e5d96d916cd4a17`  
		Last Modified: Sat, 16 Mar 2024 08:45:03 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4185eaec9fd629a92d2e2fb33da18b3c5ead72abf7d6f01ab6eaea92405c0031`  
		Last Modified: Sat, 16 Mar 2024 08:45:03 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:cc8f002c98389809a6e45a18f22b1a4a139c42812baaa5d01c1e81d8e4874156
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8795632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a947e574f9d2508db10e0ea9c2958039f03b151091e939cca9d6de03f552ba7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:53:15 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 00:53:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 00:53:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 00:53:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 00:53:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 00:53:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f579c68c28c186f8b3430f408c338b656e0cb429709b80e5f128a681b11be03`  
		Last Modified: Sat, 16 Mar 2024 00:53:58 GMT  
		Size: 5.9 MB (5875734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aeaa4c17e704f2825dcc8ca7892e9f8f7ca1022cf1aaa902c2ac011371fce0a`  
		Last Modified: Sat, 16 Mar 2024 00:53:56 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92b079a7c6d0b0e9f500662cfcfa735481d84fa902b2b7a607b5855ba623866`  
		Last Modified: Sat, 16 Mar 2024 00:53:56 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3ffef78bc0ff99629b91518b700220c06965c730059865cb63f18b757b7efad8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9088776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9c7035c53282319802a6491562f8b5922be8f1a7cf414229eca258cc31b74b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 04:03:47 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 04:03:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 04:03:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 04:03:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 04:03:50 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:03:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 04:03:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7be0478b9e8861bced761c3e24515379aae8068c6aea93bb91cab613608206`  
		Last Modified: Sat, 16 Mar 2024 04:04:38 GMT  
		Size: 5.7 MB (5740063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aceb56880d89429044a8d940a472616c66a9a19bd96999dd010d6fdcd95b7ccc`  
		Last Modified: Sat, 16 Mar 2024 04:04:37 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c653aab8018aa291381d9c5f0b4ff56538e6b1d1898554ee4b4b16f5b3a0498`  
		Last Modified: Sat, 16 Mar 2024 04:04:37 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:3bc80e99b7b6d2ec499b278e79ad0f54c297b46fc348702243cfc9b9d8c7f134
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9078987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99796f4dcf8fdff5bfa05a8f5bcd649457ca09cae4aba1f7dd5c08f0c6000ba0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:39:10 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 02:39:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 02:39:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 02:39:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 02:39:14 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 02:39:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 02:39:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1071fa4f216f6a3b40e9ca688766e9de8cde369fb0bfd45a363d74ae53636f6`  
		Last Modified: Sat, 16 Mar 2024 02:39:52 GMT  
		Size: 5.7 MB (5719633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cd77000169deae54f01f9739a3fdb6b49bebed3c942a1574d742e0f559135c`  
		Last Modified: Sat, 16 Mar 2024 02:39:51 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbd40a91a6c30b4a91aed2555db43edf084fff2084b3ac0e2df8f21216f3ec6`  
		Last Modified: Sat, 16 Mar 2024 02:39:51 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:d0b935e12aa8b047de70c249972f46ec57c6f9be3578e0da0f9ba7c52799dddc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9296153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd63ac9e2a4893a8a1ad3ead3903faebfe84d0aa5bdbe202e312a428745a9884`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 16:57:27 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 16:57:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 16:57:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 16:57:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 16:57:29 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 16:57:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 16:57:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bf12bda37fb5c76daad2fd35782e3ee4b626ab41f2b6ced22cec58c28600ad`  
		Last Modified: Sat, 16 Mar 2024 17:00:14 GMT  
		Size: 6.1 MB (6052515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c04c6057db41f701360bac00f880c04931706790543ceaa183b7b35172a5f0`  
		Last Modified: Sat, 16 Mar 2024 17:00:14 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a4186c9454ae05d593569eb01415dd64d39fd53169f11984d7579581b331b`  
		Last Modified: Sat, 16 Mar 2024 17:00:13 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine3.19`

```console
$ docker pull nats@sha256:bca70839d95348452fb8363f4943e3d2a45fcbea78ff7749e2b5219abb34fdf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:8b4822683d7955dc4a7b69bc138e5a980297f5562d3dc4f8417d80aed7b8a683
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9577903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78fb4abc56d19dcdd801b05d2982e749107d24ec996403c499518e1fec1d0a50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:48:58 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 08:49:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:49:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:49:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:49:01 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:49:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27675e5d86d45eba74328ac05267b7f93df29e2f079892c96c4425c216de74c`  
		Last Modified: Sat, 16 Mar 2024 08:49:37 GMT  
		Size: 6.2 MB (6168174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996c3b4c0f3e26b6ebc651c10f1889f8cf2f401651631836d63f72a1f449e9f2`  
		Last Modified: Sat, 16 Mar 2024 08:49:36 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca260fdf9bf58bec6ebf64f52cc0437d3935f22572653de018a0912f276efc25`  
		Last Modified: Sat, 16 Mar 2024 08:49:36 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:7ea677c7520bfdf6e5e8ca9f6e7ea392d39d8204f89e90b17de4f4216ae2e4fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae73509d5009d4f8bf7d5827db756183e287715cdca6b2c362c186c38d174486`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:44:29 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 08:44:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:44:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:44:32 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:44:32 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:44:32 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c6c88a86c2d4fae1df9dcfb8d0fb887644ffaeea7c7552244d72831f2deff0`  
		Last Modified: Sat, 16 Mar 2024 08:45:05 GMT  
		Size: 5.9 MB (5884864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bd557199bb46ecdb92b5224c44b2fb88b65b1d11eb03799e5d96d916cd4a17`  
		Last Modified: Sat, 16 Mar 2024 08:45:03 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4185eaec9fd629a92d2e2fb33da18b3c5ead72abf7d6f01ab6eaea92405c0031`  
		Last Modified: Sat, 16 Mar 2024 08:45:03 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:cc8f002c98389809a6e45a18f22b1a4a139c42812baaa5d01c1e81d8e4874156
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8795632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a947e574f9d2508db10e0ea9c2958039f03b151091e939cca9d6de03f552ba7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:53:15 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 00:53:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 00:53:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 00:53:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 00:53:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 00:53:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f579c68c28c186f8b3430f408c338b656e0cb429709b80e5f128a681b11be03`  
		Last Modified: Sat, 16 Mar 2024 00:53:58 GMT  
		Size: 5.9 MB (5875734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aeaa4c17e704f2825dcc8ca7892e9f8f7ca1022cf1aaa902c2ac011371fce0a`  
		Last Modified: Sat, 16 Mar 2024 00:53:56 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92b079a7c6d0b0e9f500662cfcfa735481d84fa902b2b7a607b5855ba623866`  
		Last Modified: Sat, 16 Mar 2024 00:53:56 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3ffef78bc0ff99629b91518b700220c06965c730059865cb63f18b757b7efad8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9088776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9c7035c53282319802a6491562f8b5922be8f1a7cf414229eca258cc31b74b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 04:03:47 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 04:03:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 04:03:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 04:03:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 04:03:50 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:03:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 04:03:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7be0478b9e8861bced761c3e24515379aae8068c6aea93bb91cab613608206`  
		Last Modified: Sat, 16 Mar 2024 04:04:38 GMT  
		Size: 5.7 MB (5740063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aceb56880d89429044a8d940a472616c66a9a19bd96999dd010d6fdcd95b7ccc`  
		Last Modified: Sat, 16 Mar 2024 04:04:37 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c653aab8018aa291381d9c5f0b4ff56538e6b1d1898554ee4b4b16f5b3a0498`  
		Last Modified: Sat, 16 Mar 2024 04:04:37 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:3bc80e99b7b6d2ec499b278e79ad0f54c297b46fc348702243cfc9b9d8c7f134
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9078987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99796f4dcf8fdff5bfa05a8f5bcd649457ca09cae4aba1f7dd5c08f0c6000ba0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:39:10 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 02:39:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 02:39:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 02:39:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 02:39:14 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 02:39:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 02:39:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1071fa4f216f6a3b40e9ca688766e9de8cde369fb0bfd45a363d74ae53636f6`  
		Last Modified: Sat, 16 Mar 2024 02:39:52 GMT  
		Size: 5.7 MB (5719633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cd77000169deae54f01f9739a3fdb6b49bebed3c942a1574d742e0f559135c`  
		Last Modified: Sat, 16 Mar 2024 02:39:51 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbd40a91a6c30b4a91aed2555db43edf084fff2084b3ac0e2df8f21216f3ec6`  
		Last Modified: Sat, 16 Mar 2024 02:39:51 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:d0b935e12aa8b047de70c249972f46ec57c6f9be3578e0da0f9ba7c52799dddc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9296153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd63ac9e2a4893a8a1ad3ead3903faebfe84d0aa5bdbe202e312a428745a9884`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 16:57:27 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 16:57:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 16:57:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 16:57:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 16:57:29 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 16:57:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 16:57:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bf12bda37fb5c76daad2fd35782e3ee4b626ab41f2b6ced22cec58c28600ad`  
		Last Modified: Sat, 16 Mar 2024 17:00:14 GMT  
		Size: 6.1 MB (6052515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c04c6057db41f701360bac00f880c04931706790543ceaa183b7b35172a5f0`  
		Last Modified: Sat, 16 Mar 2024 17:00:14 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a4186c9454ae05d593569eb01415dd64d39fd53169f11984d7579581b331b`  
		Last Modified: Sat, 16 Mar 2024 17:00:13 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:0a31000c798112718df04a19491c39f2dd8e36ba4955b8b7a9987581d5f8a033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:dbab4c53c0de6b089ceb67849d41bdf54a0ad29e50f1105048fc5f19508db803
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cbf0fba619173e5c4542920b1d7278a5a780baf2b54bff413b32cc0016433c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:06 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Sat, 16 Mar 2024 08:49:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:06 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866d738de7ab782f2ba4b31cfeee8894a26c596bed7b85f7072494d10cd5618`  
		Last Modified: Sat, 16 Mar 2024 08:49:54 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:23b831c97175a24dafc1e4858d66d89b5daea7b40475fa65a5a2cc646495f69f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f14c4fc39384124daeb9de82f2f548ed59cf95ac2c5163a4e7cb933758b47c6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:37 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Sat, 16 Mar 2024 08:44:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dcfc63d9869b797864f5925982e824e3b9ba24796e45cee98fa32eacb80c21`  
		Last Modified: Sat, 16 Mar 2024 08:45:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:d7d36063a70b3f92e87214db9cf07a81799734321a44db81a32d60f4dbe9747d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ed0bdac27116af7eb7ddd6d7e6b9ebd5fb952606a5faa4a84779b345103b0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:24 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Sat, 16 Mar 2024 00:53:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:25 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:25 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c56f0b0a93e98e48d30f323ee2f44dcffe8ee47dad4b9701cd95f33b1ad423`  
		Last Modified: Sat, 16 Mar 2024 00:54:16 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:17532cf8a200037fa12e16243b8739bc520937cd82a9a3b96d8db0e85d942071
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b75af84f70f1921e86eaa7dff023270dc485b37e1acca37fe2bc3e4e919f19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:08 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Sat, 16 Mar 2024 04:04:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:08 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:08 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3e7253e56d93fc4ce869656fef13511496d97e58250a301790645656c29acf`  
		Last Modified: Sat, 16 Mar 2024 04:04:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:bc4465dc1a2b2b68a903b34cd70721db4682b6ae49baad493c4fb8f9a54c1699
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123dd70806df1b073fab2d9d0cb4855270a447d3c72569af275ed24af793af46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 02:39:34 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Sat, 16 Mar 2024 02:39:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 02:39:35 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 02:39:35 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 02:39:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405bd5e4b794b6bad044e8744cf63ddd0f2e0001abde3c0b2b5e7a190706d5e`  
		Last Modified: Sat, 16 Mar 2024 02:40:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:b200d259ef6d710b801ba60a7f296791ebc5298d82db48b8f68cfc0bee79d15b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26134424de3ad1af4ffe096901272e7ea3dae1a93eeddcd6c110b08b29af4011`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 16:58:41 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Sat, 16 Mar 2024 16:58:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 16:58:43 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 16:58:44 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 16:58:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea5f20b9222048fdae4e26dc03a3a997375533021a900c72f4e6b338c144ddb`  
		Last Modified: Sat, 16 Mar 2024 17:00:32 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:fb9a7b002fc37c676f80fe35573e4ade35e3429aa09510c6c9e90025dc498535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:5c3f90898e8204465bc8f03eeb287f3c4a74ab98abddf8e7133303a697cdcc15
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110558802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c9fe6985208f3c2b3d60ef9ba9dca290d513ed8dfd37ea890a5a30e3309db2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Wed, 10 Apr 2024 01:43:32 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:43:34 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 10 Apr 2024 01:43:34 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:43:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:43:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:43:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826d34fcda621b296890090998100732b227a2fded8eee4d47e58e23e4a707e0`  
		Last Modified: Wed, 10 Apr 2024 01:48:21 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a02eb33a3aa2cfe4eef717c0d9f835f089de87c8bf7a29ada529785e9a766d9`  
		Last Modified: Wed, 10 Apr 2024 01:48:20 GMT  
		Size: 5.7 MB (5663495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba1c2806f1a8f6a751f20ca92a1ce06f1e4694140d4837b6f890ce9e2bef92`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd1781b30607b707f2c7003388ad80836cdb8125e2d4376107843968a0d97ca`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72699a90a0ff719020f44581d9607dc75f34d1b9f79ad4baa1d2dd8a2a111558`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f3e31e8b287637780dd9b544fda9313c77847672463da5487a4f569ad663de`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:fb9a7b002fc37c676f80fe35573e4ade35e3429aa09510c6c9e90025dc498535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:5c3f90898e8204465bc8f03eeb287f3c4a74ab98abddf8e7133303a697cdcc15
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110558802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c9fe6985208f3c2b3d60ef9ba9dca290d513ed8dfd37ea890a5a30e3309db2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Wed, 10 Apr 2024 01:43:32 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:43:34 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 10 Apr 2024 01:43:34 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:43:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:43:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:43:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826d34fcda621b296890090998100732b227a2fded8eee4d47e58e23e4a707e0`  
		Last Modified: Wed, 10 Apr 2024 01:48:21 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a02eb33a3aa2cfe4eef717c0d9f835f089de87c8bf7a29ada529785e9a766d9`  
		Last Modified: Wed, 10 Apr 2024 01:48:20 GMT  
		Size: 5.7 MB (5663495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba1c2806f1a8f6a751f20ca92a1ce06f1e4694140d4837b6f890ce9e2bef92`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd1781b30607b707f2c7003388ad80836cdb8125e2d4376107843968a0d97ca`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72699a90a0ff719020f44581d9607dc75f34d1b9f79ad4baa1d2dd8a2a111558`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f3e31e8b287637780dd9b544fda9313c77847672463da5487a4f569ad663de`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:0a31000c798112718df04a19491c39f2dd8e36ba4955b8b7a9987581d5f8a033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:dbab4c53c0de6b089ceb67849d41bdf54a0ad29e50f1105048fc5f19508db803
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cbf0fba619173e5c4542920b1d7278a5a780baf2b54bff413b32cc0016433c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:06 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Sat, 16 Mar 2024 08:49:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:06 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866d738de7ab782f2ba4b31cfeee8894a26c596bed7b85f7072494d10cd5618`  
		Last Modified: Sat, 16 Mar 2024 08:49:54 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:23b831c97175a24dafc1e4858d66d89b5daea7b40475fa65a5a2cc646495f69f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f14c4fc39384124daeb9de82f2f548ed59cf95ac2c5163a4e7cb933758b47c6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:37 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Sat, 16 Mar 2024 08:44:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dcfc63d9869b797864f5925982e824e3b9ba24796e45cee98fa32eacb80c21`  
		Last Modified: Sat, 16 Mar 2024 08:45:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:d7d36063a70b3f92e87214db9cf07a81799734321a44db81a32d60f4dbe9747d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ed0bdac27116af7eb7ddd6d7e6b9ebd5fb952606a5faa4a84779b345103b0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:24 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Sat, 16 Mar 2024 00:53:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:25 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:25 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c56f0b0a93e98e48d30f323ee2f44dcffe8ee47dad4b9701cd95f33b1ad423`  
		Last Modified: Sat, 16 Mar 2024 00:54:16 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:17532cf8a200037fa12e16243b8739bc520937cd82a9a3b96d8db0e85d942071
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b75af84f70f1921e86eaa7dff023270dc485b37e1acca37fe2bc3e4e919f19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:08 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Sat, 16 Mar 2024 04:04:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:08 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:08 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3e7253e56d93fc4ce869656fef13511496d97e58250a301790645656c29acf`  
		Last Modified: Sat, 16 Mar 2024 04:04:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:bc4465dc1a2b2b68a903b34cd70721db4682b6ae49baad493c4fb8f9a54c1699
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123dd70806df1b073fab2d9d0cb4855270a447d3c72569af275ed24af793af46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 02:39:34 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Sat, 16 Mar 2024 02:39:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 02:39:35 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 02:39:35 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 02:39:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405bd5e4b794b6bad044e8744cf63ddd0f2e0001abde3c0b2b5e7a190706d5e`  
		Last Modified: Sat, 16 Mar 2024 02:40:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:b200d259ef6d710b801ba60a7f296791ebc5298d82db48b8f68cfc0bee79d15b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26134424de3ad1af4ffe096901272e7ea3dae1a93eeddcd6c110b08b29af4011`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 16:58:41 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Sat, 16 Mar 2024 16:58:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 16:58:43 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 16:58:44 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 16:58:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea5f20b9222048fdae4e26dc03a3a997375533021a900c72f4e6b338c144ddb`  
		Last Modified: Sat, 16 Mar 2024 17:00:32 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:b04dc3c962bbed963b7ed2272999339683a9eb46cdeaa06a77c1dbbdfe93b834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:29380f4863fb3a6f2b04217f477bee6eac525e6b36400d4446ee1680024de74e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2170781570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa73df6040c74fa785c0df500e4c8a7a76a5ce054b396330c2b4631b211c5a06`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Wed, 10 Apr 2024 01:40:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Apr 2024 01:40:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:40:04 GMT
ENV NATS_SERVER=2.10.12
# Wed, 10 Apr 2024 01:40:05 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.12/nats-server-v2.10.12-windows-amd64.zip
# Wed, 10 Apr 2024 01:40:06 GMT
ENV NATS_SERVER_SHASUM=bc944f832fdc3eaa0072c0a5e278efd672cec394159661070e7aea4f5d483cbc
# Wed, 10 Apr 2024 01:41:22 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Apr 2024 01:43:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Apr 2024 01:43:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:43:16 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:43:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:43:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6ae8ddefe4f7d0224959df0cc91d01044dce7f127ee7c23257cf0b63bfd7ac`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266ac5d9d5680f1e3a65f9d272fc3a2ab7f67eda1b00c961365853e0a9c3e27`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b45aa9398ff56a16e042bfdf01b44ff7daebf93e7cba5d601367d2c0e5a55ed`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe31b64ec7d8949724e118281dfca112c508483cc5b28076aaadd223f212b4a4`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f68caae1490441aa87bfa98ed09fc4717d036f13634615fe4eb4a1efe4925a6`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567ed00bc244d7ef610728b1545d39345e73e8e86ee441b586eea2238d1bf1dd`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 241.8 KB (241850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f8817e79dfbc8f56443618f486d64c5ac11608663b3bdf7a25f87f2412c473`  
		Last Modified: Wed, 10 Apr 2024 01:48:02 GMT  
		Size: 6.1 MB (6099353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60589928d42d9fc2f8e9ccd4a26ba13cebed25894380700f63bace8ca5fc27c0`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbe842b574fe798f092ac13841eea2cee6361f8232a3539375c0503e5911af7`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619674a0794dc85dc23997a189c9659f4612bf24f1fd187f2d26e38dbf6a8691`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd24c8b4dbeddc4174617445fd1d056589be9451dfd07af7f714867654c353f`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:b04dc3c962bbed963b7ed2272999339683a9eb46cdeaa06a77c1dbbdfe93b834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:29380f4863fb3a6f2b04217f477bee6eac525e6b36400d4446ee1680024de74e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2170781570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa73df6040c74fa785c0df500e4c8a7a76a5ce054b396330c2b4631b211c5a06`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Wed, 10 Apr 2024 01:40:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Apr 2024 01:40:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:40:04 GMT
ENV NATS_SERVER=2.10.12
# Wed, 10 Apr 2024 01:40:05 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.12/nats-server-v2.10.12-windows-amd64.zip
# Wed, 10 Apr 2024 01:40:06 GMT
ENV NATS_SERVER_SHASUM=bc944f832fdc3eaa0072c0a5e278efd672cec394159661070e7aea4f5d483cbc
# Wed, 10 Apr 2024 01:41:22 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Apr 2024 01:43:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Apr 2024 01:43:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:43:16 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:43:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:43:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6ae8ddefe4f7d0224959df0cc91d01044dce7f127ee7c23257cf0b63bfd7ac`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266ac5d9d5680f1e3a65f9d272fc3a2ab7f67eda1b00c961365853e0a9c3e27`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b45aa9398ff56a16e042bfdf01b44ff7daebf93e7cba5d601367d2c0e5a55ed`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe31b64ec7d8949724e118281dfca112c508483cc5b28076aaadd223f212b4a4`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f68caae1490441aa87bfa98ed09fc4717d036f13634615fe4eb4a1efe4925a6`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567ed00bc244d7ef610728b1545d39345e73e8e86ee441b586eea2238d1bf1dd`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 241.8 KB (241850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f8817e79dfbc8f56443618f486d64c5ac11608663b3bdf7a25f87f2412c473`  
		Last Modified: Wed, 10 Apr 2024 01:48:02 GMT  
		Size: 6.1 MB (6099353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60589928d42d9fc2f8e9ccd4a26ba13cebed25894380700f63bace8ca5fc27c0`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbe842b574fe798f092ac13841eea2cee6361f8232a3539375c0503e5911af7`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619674a0794dc85dc23997a189c9659f4612bf24f1fd187f2d26e38dbf6a8691`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd24c8b4dbeddc4174617445fd1d056589be9451dfd07af7f714867654c353f`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.14`

**does not exist** (yet?)

## `nats:2.10.14-alpine`

**does not exist** (yet?)

## `nats:2.10.14-alpine3.19`

**does not exist** (yet?)

## `nats:2.10.14-linux`

**does not exist** (yet?)

## `nats:2.10.14-nanoserver`

**does not exist** (yet?)

## `nats:2.10.14-nanoserver-1809`

**does not exist** (yet?)

## `nats:2.10.14-scratch`

**does not exist** (yet?)

## `nats:2.10.14-windowsservercore`

**does not exist** (yet?)

## `nats:2.10.14-windowsservercore-1809`

**does not exist** (yet?)

## `nats:2.9`

```console
$ docker pull nats@sha256:ed7d2c4f739ee88e4592880eb2c7541cf81eef672a426c3108ed9bcf16765853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9` - linux; amd64

```console
$ docker pull nats@sha256:a2b677be6bd67324258eee1db031ebfd408991ceba89862e17189288c0d0f9d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765403d3b7754e8f0f9d0c6ae93da0a2297e954b85bca6ec745e84b2d8638fc0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e338e1c824f87e6ce72124da6e3d777f3f418713befd0195137683f46e4e1e`  
		Last Modified: Sat, 16 Mar 2024 08:50:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:26cdc28820c5ca90c7859bc14a64c2b734d5e1e44b0759e066e481fe63137d47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d4e737c294a9b2b10c58350ac2c91069ee7c5e4b0cb875a22e316aeac10c9a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:46 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:46 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f159630d723fb35254591f813277c6864a15b4e1af2c293872364ff35252f485`  
		Last Modified: Sat, 16 Mar 2024 08:45:52 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:5f86fb8a593271cba2f3380a95fbc590bb218a4c487574beeb827b2c56070a6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5259ceafa373a7b7a73148d38f96fec6949447601b0cd46c31de87893969fd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a918e9e80cbfc3e74933281e2854ff73ba86f9528b18448d68e87a9b1da3df6`  
		Last Modified: Sat, 16 Mar 2024 00:54:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c2508454845c92a3431e0106172c3d7fff8acc31851825d2d8123bdbb45d0231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e3e46564e100a7fff7524bfff19ec0019b89f369ab18a289b23e2837c3fa94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992ffd84ea59eedf4b12ad8b56fbe3a496d3deaca06714d77157cc33a5c589b3`  
		Last Modified: Sat, 16 Mar 2024 04:05:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine`

```console
$ docker pull nats@sha256:e40d91bdca974723355b03aaf2bd689d9578a8c6c719efed957a05e0bb2c1f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:1aea9dab74b20605f294be5bd85d0bc480c031d5e95c17fcf78c0dfaf9d4ae7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd29f2466f179a37884517245d3609223965061df9fbb94a0b4ee45c696ab419`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:49:09 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:49:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:49:13 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:49:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52662615decef836729c27772fd956ed34f2b5a42bc2c0e27b7f1eb8ec6e1dd`  
		Last Modified: Sat, 16 Mar 2024 08:50:12 GMT  
		Size: 5.9 MB (5870718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d9309bea9cbbcb371347e1cfc9015482aa44da15dcc2954ecefce3dd2a50e6`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3d9f573e3a20c89b35599721c0737fae89e39e35012f0b2e821fd4d20afc48`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:fdcf74e2d2a66a29dbfadca9fe1d0f87150ada4e71523f5d7cd0f80a6468dbd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8755267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7335266ce3a3608efbcc3f99740205ef5ce3dfd4345afc0f5ef93b70cb13c291`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:44:39 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:44:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:44:42 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:44:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9137c4a337449facc87ef5ee3665c96a549e6e3536ae94d4299bcbc6dfdea7b2`  
		Last Modified: Sat, 16 Mar 2024 08:45:41 GMT  
		Size: 5.6 MB (5607208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a13df67924e990510d98bc0085d0395451ccb1c5d874eeb4f25a87bdba9e01`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64427c3156bb49e3065365fe9f79f632a084854abe87577aab4f8bf4575330cc`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:f7b01de31f9dc6030ea363e5b27203644e726d5dac453948ae77d9df33d8cbe6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6246019087a976ba4d128366d1f88a40d1eaabe7344e6bf5879d2e7022389cb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:53:27 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 00:53:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 00:53:33 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 00:53:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd76eaf9560c3a02d86b302defb4b6b8a8a7ee892505b05ac0ab7ac9038c1a7`  
		Last Modified: Sat, 16 Mar 2024 00:54:35 GMT  
		Size: 5.6 MB (5599769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6e0adcaf71449171b6cbe6d69146a1af1cb15863f657f1c08562110247555e`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5a74349ed6863e93d568b2c4cf9cd67c565717d30af0148dcfb2cc8a41891`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:23eabd89ccf83c14b5f04236e9ae193b90df9cc618adc8b00b5be8624a0dce89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fdb6fbb205a7916b7aa7ed920e3e6dd1e2b458ad0ab1a4fed69b1591900057`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 04:04:12 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 04:04:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 04:04:14 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 04:04:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3560e79b148c5e98949b1f08ed73634c8c7826d700277cf260bf3cb6d5f00d`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 5.4 MB (5408722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b5e756dbfadc026b321fece391fa35f53130fa5c59ebb201fddb9a745238e8`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ad59f09b7cfe9ed625b71c2f8de7ab974a5db023d95fbe97fa8c2d36077d09`  
		Last Modified: Sat, 16 Mar 2024 04:05:13 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine3.18`

```console
$ docker pull nats@sha256:e40d91bdca974723355b03aaf2bd689d9578a8c6c719efed957a05e0bb2c1f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:1aea9dab74b20605f294be5bd85d0bc480c031d5e95c17fcf78c0dfaf9d4ae7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd29f2466f179a37884517245d3609223965061df9fbb94a0b4ee45c696ab419`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:49:09 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:49:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:49:13 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:49:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52662615decef836729c27772fd956ed34f2b5a42bc2c0e27b7f1eb8ec6e1dd`  
		Last Modified: Sat, 16 Mar 2024 08:50:12 GMT  
		Size: 5.9 MB (5870718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d9309bea9cbbcb371347e1cfc9015482aa44da15dcc2954ecefce3dd2a50e6`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3d9f573e3a20c89b35599721c0737fae89e39e35012f0b2e821fd4d20afc48`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:fdcf74e2d2a66a29dbfadca9fe1d0f87150ada4e71523f5d7cd0f80a6468dbd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8755267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7335266ce3a3608efbcc3f99740205ef5ce3dfd4345afc0f5ef93b70cb13c291`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:44:39 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:44:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:44:42 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:44:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9137c4a337449facc87ef5ee3665c96a549e6e3536ae94d4299bcbc6dfdea7b2`  
		Last Modified: Sat, 16 Mar 2024 08:45:41 GMT  
		Size: 5.6 MB (5607208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a13df67924e990510d98bc0085d0395451ccb1c5d874eeb4f25a87bdba9e01`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64427c3156bb49e3065365fe9f79f632a084854abe87577aab4f8bf4575330cc`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:f7b01de31f9dc6030ea363e5b27203644e726d5dac453948ae77d9df33d8cbe6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6246019087a976ba4d128366d1f88a40d1eaabe7344e6bf5879d2e7022389cb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:53:27 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 00:53:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 00:53:33 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 00:53:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd76eaf9560c3a02d86b302defb4b6b8a8a7ee892505b05ac0ab7ac9038c1a7`  
		Last Modified: Sat, 16 Mar 2024 00:54:35 GMT  
		Size: 5.6 MB (5599769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6e0adcaf71449171b6cbe6d69146a1af1cb15863f657f1c08562110247555e`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5a74349ed6863e93d568b2c4cf9cd67c565717d30af0148dcfb2cc8a41891`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:23eabd89ccf83c14b5f04236e9ae193b90df9cc618adc8b00b5be8624a0dce89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fdb6fbb205a7916b7aa7ed920e3e6dd1e2b458ad0ab1a4fed69b1591900057`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 04:04:12 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 04:04:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 04:04:14 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 04:04:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3560e79b148c5e98949b1f08ed73634c8c7826d700277cf260bf3cb6d5f00d`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 5.4 MB (5408722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b5e756dbfadc026b321fece391fa35f53130fa5c59ebb201fddb9a745238e8`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ad59f09b7cfe9ed625b71c2f8de7ab974a5db023d95fbe97fa8c2d36077d09`  
		Last Modified: Sat, 16 Mar 2024 04:05:13 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-linux`

```console
$ docker pull nats@sha256:ed7d2c4f739ee88e4592880eb2c7541cf81eef672a426c3108ed9bcf16765853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:a2b677be6bd67324258eee1db031ebfd408991ceba89862e17189288c0d0f9d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765403d3b7754e8f0f9d0c6ae93da0a2297e954b85bca6ec745e84b2d8638fc0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e338e1c824f87e6ce72124da6e3d777f3f418713befd0195137683f46e4e1e`  
		Last Modified: Sat, 16 Mar 2024 08:50:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:26cdc28820c5ca90c7859bc14a64c2b734d5e1e44b0759e066e481fe63137d47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d4e737c294a9b2b10c58350ac2c91069ee7c5e4b0cb875a22e316aeac10c9a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:46 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:46 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f159630d723fb35254591f813277c6864a15b4e1af2c293872364ff35252f485`  
		Last Modified: Sat, 16 Mar 2024 08:45:52 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:5f86fb8a593271cba2f3380a95fbc590bb218a4c487574beeb827b2c56070a6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5259ceafa373a7b7a73148d38f96fec6949447601b0cd46c31de87893969fd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a918e9e80cbfc3e74933281e2854ff73ba86f9528b18448d68e87a9b1da3df6`  
		Last Modified: Sat, 16 Mar 2024 00:54:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c2508454845c92a3431e0106172c3d7fff8acc31851825d2d8123bdbb45d0231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e3e46564e100a7fff7524bfff19ec0019b89f369ab18a289b23e2837c3fa94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992ffd84ea59eedf4b12ad8b56fbe3a496d3deaca06714d77157cc33a5c589b3`  
		Last Modified: Sat, 16 Mar 2024 04:05:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver`

```console
$ docker pull nats@sha256:c0a08eb6c90b0e52d2a0eb7cbf2bd49e72e51f3a961f9302934a6791391553fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:1e46dbde3ffefa7f4693b42a8a456ff7e4dba33e11f4cab76169d63a3dfcfa65
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110225761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c772dc25544412aa36610022d39cb7861a34d08bc6437239b73ba3359307d28`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Wed, 10 Apr 2024 01:43:32 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:47:28 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 10 Apr 2024 01:47:29 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:47:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:47:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:47:31 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826d34fcda621b296890090998100732b227a2fded8eee4d47e58e23e4a707e0`  
		Last Modified: Wed, 10 Apr 2024 01:48:21 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d02cd79646cc5afd725d708433d5ba70d6669f17f322641f53875e4ad88639`  
		Last Modified: Wed, 10 Apr 2024 01:48:43 GMT  
		Size: 5.3 MB (5330196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae1b62db39eca059a0f47334bc396f4d6baa2f92e6c0d1ffcb7c7cd5d017026`  
		Last Modified: Wed, 10 Apr 2024 01:48:42 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e25184c57e09d3476529e0bd4947414abde9578e48218bf37669081602b5c7c`  
		Last Modified: Wed, 10 Apr 2024 01:48:42 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed8e16ac9c52081dfad87f09fc9887825b185df0aece7fa3eb31ae2701baa6f`  
		Last Modified: Wed, 10 Apr 2024 01:48:42 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c62ba0972ac1c861c8af444f35fe69482a85f41e4158b4dc30e8bf1772d436f`  
		Last Modified: Wed, 10 Apr 2024 01:48:42 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:c0a08eb6c90b0e52d2a0eb7cbf2bd49e72e51f3a961f9302934a6791391553fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:1e46dbde3ffefa7f4693b42a8a456ff7e4dba33e11f4cab76169d63a3dfcfa65
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110225761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c772dc25544412aa36610022d39cb7861a34d08bc6437239b73ba3359307d28`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Wed, 10 Apr 2024 01:43:32 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:47:28 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 10 Apr 2024 01:47:29 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:47:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:47:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:47:31 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826d34fcda621b296890090998100732b227a2fded8eee4d47e58e23e4a707e0`  
		Last Modified: Wed, 10 Apr 2024 01:48:21 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d02cd79646cc5afd725d708433d5ba70d6669f17f322641f53875e4ad88639`  
		Last Modified: Wed, 10 Apr 2024 01:48:43 GMT  
		Size: 5.3 MB (5330196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae1b62db39eca059a0f47334bc396f4d6baa2f92e6c0d1ffcb7c7cd5d017026`  
		Last Modified: Wed, 10 Apr 2024 01:48:42 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e25184c57e09d3476529e0bd4947414abde9578e48218bf37669081602b5c7c`  
		Last Modified: Wed, 10 Apr 2024 01:48:42 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed8e16ac9c52081dfad87f09fc9887825b185df0aece7fa3eb31ae2701baa6f`  
		Last Modified: Wed, 10 Apr 2024 01:48:42 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c62ba0972ac1c861c8af444f35fe69482a85f41e4158b4dc30e8bf1772d436f`  
		Last Modified: Wed, 10 Apr 2024 01:48:42 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-scratch`

```console
$ docker pull nats@sha256:ed7d2c4f739ee88e4592880eb2c7541cf81eef672a426c3108ed9bcf16765853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:a2b677be6bd67324258eee1db031ebfd408991ceba89862e17189288c0d0f9d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765403d3b7754e8f0f9d0c6ae93da0a2297e954b85bca6ec745e84b2d8638fc0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e338e1c824f87e6ce72124da6e3d777f3f418713befd0195137683f46e4e1e`  
		Last Modified: Sat, 16 Mar 2024 08:50:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:26cdc28820c5ca90c7859bc14a64c2b734d5e1e44b0759e066e481fe63137d47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d4e737c294a9b2b10c58350ac2c91069ee7c5e4b0cb875a22e316aeac10c9a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:46 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:46 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f159630d723fb35254591f813277c6864a15b4e1af2c293872364ff35252f485`  
		Last Modified: Sat, 16 Mar 2024 08:45:52 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:5f86fb8a593271cba2f3380a95fbc590bb218a4c487574beeb827b2c56070a6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5259ceafa373a7b7a73148d38f96fec6949447601b0cd46c31de87893969fd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a918e9e80cbfc3e74933281e2854ff73ba86f9528b18448d68e87a9b1da3df6`  
		Last Modified: Sat, 16 Mar 2024 00:54:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c2508454845c92a3431e0106172c3d7fff8acc31851825d2d8123bdbb45d0231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e3e46564e100a7fff7524bfff19ec0019b89f369ab18a289b23e2837c3fa94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992ffd84ea59eedf4b12ad8b56fbe3a496d3deaca06714d77157cc33a5c589b3`  
		Last Modified: Sat, 16 Mar 2024 04:05:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore`

```console
$ docker pull nats@sha256:356aad98f52e72f691fe5e7fa7c32157ebdf19d9a81cbba6fb762dd2203d301b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:f80d25237a29b036cb4dab7cbe24d20b79110116b690b9042724ae58fd2096b3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2170421356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384f62945c116666450b422da2b22c8e1b581e5c4d7bd175895d062c0f0e363c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Wed, 10 Apr 2024 01:40:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Apr 2024 01:40:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:43:44 GMT
ENV NATS_SERVER=2.9.25
# Wed, 10 Apr 2024 01:43:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 10 Apr 2024 01:43:46 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 10 Apr 2024 01:45:11 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Apr 2024 01:47:11 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Apr 2024 01:47:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:47:13 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:47:14 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:47:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6ae8ddefe4f7d0224959df0cc91d01044dce7f127ee7c23257cf0b63bfd7ac`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266ac5d9d5680f1e3a65f9d272fc3a2ab7f67eda1b00c961365853e0a9c3e27`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d000231e1f901cb73596d1eea38d1f99e043c3aed53c558f3a7553a3fe7088d8`  
		Last Modified: Wed, 10 Apr 2024 01:48:34 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dc9fdda7712880d9a01c8bc6a4ce00cbb59e7caae96fc780685d4135f05691`  
		Last Modified: Wed, 10 Apr 2024 01:48:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ffbbcd3f996c8e229ead2b808d37f43898a7612a6be83f747eddd39df99009`  
		Last Modified: Wed, 10 Apr 2024 01:48:34 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d4a1edaf82c4db8b70e77b574a9d7dfe8cfa86293bbf69040dc30865b3b453`  
		Last Modified: Wed, 10 Apr 2024 01:48:34 GMT  
		Size: 191.8 KB (191819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987bf8adc00231373efdfe17dc7ce4f0c4481ba5dff6ac001bf8df8eec03a8c5`  
		Last Modified: Wed, 10 Apr 2024 01:48:33 GMT  
		Size: 5.8 MB (5788404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fefcee4ad4d7b3f763bee3d5dca858f368c1b9f634c506f3e5054751498e83`  
		Last Modified: Wed, 10 Apr 2024 01:48:32 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8efafd4c6558c5f6e1798f38c6445d94dc4d625bd18a4e742b0c4638019d59`  
		Last Modified: Wed, 10 Apr 2024 01:48:32 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3fca3d80cb7613a601459e05c19668accb212dde3b28c4df92b288a65eba78`  
		Last Modified: Wed, 10 Apr 2024 01:48:32 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0da1472d5e10e5bbfc309c1969496a887d9948fe44c387e2c29604f6bfd384`  
		Last Modified: Wed, 10 Apr 2024 01:48:32 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:356aad98f52e72f691fe5e7fa7c32157ebdf19d9a81cbba6fb762dd2203d301b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:f80d25237a29b036cb4dab7cbe24d20b79110116b690b9042724ae58fd2096b3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2170421356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384f62945c116666450b422da2b22c8e1b581e5c4d7bd175895d062c0f0e363c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Wed, 10 Apr 2024 01:40:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Apr 2024 01:40:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:43:44 GMT
ENV NATS_SERVER=2.9.25
# Wed, 10 Apr 2024 01:43:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 10 Apr 2024 01:43:46 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 10 Apr 2024 01:45:11 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Apr 2024 01:47:11 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Apr 2024 01:47:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:47:13 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:47:14 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:47:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6ae8ddefe4f7d0224959df0cc91d01044dce7f127ee7c23257cf0b63bfd7ac`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266ac5d9d5680f1e3a65f9d272fc3a2ab7f67eda1b00c961365853e0a9c3e27`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d000231e1f901cb73596d1eea38d1f99e043c3aed53c558f3a7553a3fe7088d8`  
		Last Modified: Wed, 10 Apr 2024 01:48:34 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dc9fdda7712880d9a01c8bc6a4ce00cbb59e7caae96fc780685d4135f05691`  
		Last Modified: Wed, 10 Apr 2024 01:48:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ffbbcd3f996c8e229ead2b808d37f43898a7612a6be83f747eddd39df99009`  
		Last Modified: Wed, 10 Apr 2024 01:48:34 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d4a1edaf82c4db8b70e77b574a9d7dfe8cfa86293bbf69040dc30865b3b453`  
		Last Modified: Wed, 10 Apr 2024 01:48:34 GMT  
		Size: 191.8 KB (191819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987bf8adc00231373efdfe17dc7ce4f0c4481ba5dff6ac001bf8df8eec03a8c5`  
		Last Modified: Wed, 10 Apr 2024 01:48:33 GMT  
		Size: 5.8 MB (5788404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fefcee4ad4d7b3f763bee3d5dca858f368c1b9f634c506f3e5054751498e83`  
		Last Modified: Wed, 10 Apr 2024 01:48:32 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8efafd4c6558c5f6e1798f38c6445d94dc4d625bd18a4e742b0c4638019d59`  
		Last Modified: Wed, 10 Apr 2024 01:48:32 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3fca3d80cb7613a601459e05c19668accb212dde3b28c4df92b288a65eba78`  
		Last Modified: Wed, 10 Apr 2024 01:48:32 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0da1472d5e10e5bbfc309c1969496a887d9948fe44c387e2c29604f6bfd384`  
		Last Modified: Wed, 10 Apr 2024 01:48:32 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25`

```console
$ docker pull nats@sha256:ed7d2c4f739ee88e4592880eb2c7541cf81eef672a426c3108ed9bcf16765853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25` - linux; amd64

```console
$ docker pull nats@sha256:a2b677be6bd67324258eee1db031ebfd408991ceba89862e17189288c0d0f9d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765403d3b7754e8f0f9d0c6ae93da0a2297e954b85bca6ec745e84b2d8638fc0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e338e1c824f87e6ce72124da6e3d777f3f418713befd0195137683f46e4e1e`  
		Last Modified: Sat, 16 Mar 2024 08:50:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25` - linux; arm variant v6

```console
$ docker pull nats@sha256:26cdc28820c5ca90c7859bc14a64c2b734d5e1e44b0759e066e481fe63137d47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d4e737c294a9b2b10c58350ac2c91069ee7c5e4b0cb875a22e316aeac10c9a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:46 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:46 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f159630d723fb35254591f813277c6864a15b4e1af2c293872364ff35252f485`  
		Last Modified: Sat, 16 Mar 2024 08:45:52 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25` - linux; arm variant v7

```console
$ docker pull nats@sha256:5f86fb8a593271cba2f3380a95fbc590bb218a4c487574beeb827b2c56070a6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5259ceafa373a7b7a73148d38f96fec6949447601b0cd46c31de87893969fd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a918e9e80cbfc3e74933281e2854ff73ba86f9528b18448d68e87a9b1da3df6`  
		Last Modified: Sat, 16 Mar 2024 00:54:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c2508454845c92a3431e0106172c3d7fff8acc31851825d2d8123bdbb45d0231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e3e46564e100a7fff7524bfff19ec0019b89f369ab18a289b23e2837c3fa94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992ffd84ea59eedf4b12ad8b56fbe3a496d3deaca06714d77157cc33a5c589b3`  
		Last Modified: Sat, 16 Mar 2024 04:05:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-alpine`

```console
$ docker pull nats@sha256:e40d91bdca974723355b03aaf2bd689d9578a8c6c719efed957a05e0bb2c1f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-alpine` - linux; amd64

```console
$ docker pull nats@sha256:1aea9dab74b20605f294be5bd85d0bc480c031d5e95c17fcf78c0dfaf9d4ae7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd29f2466f179a37884517245d3609223965061df9fbb94a0b4ee45c696ab419`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:49:09 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:49:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:49:13 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:49:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52662615decef836729c27772fd956ed34f2b5a42bc2c0e27b7f1eb8ec6e1dd`  
		Last Modified: Sat, 16 Mar 2024 08:50:12 GMT  
		Size: 5.9 MB (5870718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d9309bea9cbbcb371347e1cfc9015482aa44da15dcc2954ecefce3dd2a50e6`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3d9f573e3a20c89b35599721c0737fae89e39e35012f0b2e821fd4d20afc48`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:fdcf74e2d2a66a29dbfadca9fe1d0f87150ada4e71523f5d7cd0f80a6468dbd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8755267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7335266ce3a3608efbcc3f99740205ef5ce3dfd4345afc0f5ef93b70cb13c291`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:44:39 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:44:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:44:42 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:44:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9137c4a337449facc87ef5ee3665c96a549e6e3536ae94d4299bcbc6dfdea7b2`  
		Last Modified: Sat, 16 Mar 2024 08:45:41 GMT  
		Size: 5.6 MB (5607208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a13df67924e990510d98bc0085d0395451ccb1c5d874eeb4f25a87bdba9e01`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64427c3156bb49e3065365fe9f79f632a084854abe87577aab4f8bf4575330cc`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:f7b01de31f9dc6030ea363e5b27203644e726d5dac453948ae77d9df33d8cbe6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6246019087a976ba4d128366d1f88a40d1eaabe7344e6bf5879d2e7022389cb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:53:27 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 00:53:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 00:53:33 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 00:53:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd76eaf9560c3a02d86b302defb4b6b8a8a7ee892505b05ac0ab7ac9038c1a7`  
		Last Modified: Sat, 16 Mar 2024 00:54:35 GMT  
		Size: 5.6 MB (5599769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6e0adcaf71449171b6cbe6d69146a1af1cb15863f657f1c08562110247555e`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5a74349ed6863e93d568b2c4cf9cd67c565717d30af0148dcfb2cc8a41891`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:23eabd89ccf83c14b5f04236e9ae193b90df9cc618adc8b00b5be8624a0dce89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fdb6fbb205a7916b7aa7ed920e3e6dd1e2b458ad0ab1a4fed69b1591900057`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 04:04:12 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 04:04:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 04:04:14 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 04:04:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3560e79b148c5e98949b1f08ed73634c8c7826d700277cf260bf3cb6d5f00d`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 5.4 MB (5408722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b5e756dbfadc026b321fece391fa35f53130fa5c59ebb201fddb9a745238e8`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ad59f09b7cfe9ed625b71c2f8de7ab974a5db023d95fbe97fa8c2d36077d09`  
		Last Modified: Sat, 16 Mar 2024 04:05:13 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-alpine3.18`

```console
$ docker pull nats@sha256:e40d91bdca974723355b03aaf2bd689d9578a8c6c719efed957a05e0bb2c1f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:1aea9dab74b20605f294be5bd85d0bc480c031d5e95c17fcf78c0dfaf9d4ae7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd29f2466f179a37884517245d3609223965061df9fbb94a0b4ee45c696ab419`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:49:09 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:49:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:49:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:49:13 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:49:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52662615decef836729c27772fd956ed34f2b5a42bc2c0e27b7f1eb8ec6e1dd`  
		Last Modified: Sat, 16 Mar 2024 08:50:12 GMT  
		Size: 5.9 MB (5870718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d9309bea9cbbcb371347e1cfc9015482aa44da15dcc2954ecefce3dd2a50e6`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3d9f573e3a20c89b35599721c0737fae89e39e35012f0b2e821fd4d20afc48`  
		Last Modified: Sat, 16 Mar 2024 08:50:11 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:fdcf74e2d2a66a29dbfadca9fe1d0f87150ada4e71523f5d7cd0f80a6468dbd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8755267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7335266ce3a3608efbcc3f99740205ef5ce3dfd4345afc0f5ef93b70cb13c291`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:44:39 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 08:44:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:44:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:44:42 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:44:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9137c4a337449facc87ef5ee3665c96a549e6e3536ae94d4299bcbc6dfdea7b2`  
		Last Modified: Sat, 16 Mar 2024 08:45:41 GMT  
		Size: 5.6 MB (5607208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a13df67924e990510d98bc0085d0395451ccb1c5d874eeb4f25a87bdba9e01`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64427c3156bb49e3065365fe9f79f632a084854abe87577aab4f8bf4575330cc`  
		Last Modified: Sat, 16 Mar 2024 08:45:39 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:f7b01de31f9dc6030ea363e5b27203644e726d5dac453948ae77d9df33d8cbe6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6246019087a976ba4d128366d1f88a40d1eaabe7344e6bf5879d2e7022389cb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:53:27 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 00:53:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 00:53:33 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 00:53:33 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 00:53:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd76eaf9560c3a02d86b302defb4b6b8a8a7ee892505b05ac0ab7ac9038c1a7`  
		Last Modified: Sat, 16 Mar 2024 00:54:35 GMT  
		Size: 5.6 MB (5599769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6e0adcaf71449171b6cbe6d69146a1af1cb15863f657f1c08562110247555e`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5a74349ed6863e93d568b2c4cf9cd67c565717d30af0148dcfb2cc8a41891`  
		Last Modified: Sat, 16 Mar 2024 00:54:34 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:23eabd89ccf83c14b5f04236e9ae193b90df9cc618adc8b00b5be8624a0dce89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fdb6fbb205a7916b7aa7ed920e3e6dd1e2b458ad0ab1a4fed69b1591900057`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 04:04:12 GMT
ENV NATS_SERVER=2.9.25
# Sat, 16 Mar 2024 04:04:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 04:04:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 04:04:14 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 04:04:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3560e79b148c5e98949b1f08ed73634c8c7826d700277cf260bf3cb6d5f00d`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 5.4 MB (5408722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b5e756dbfadc026b321fece391fa35f53130fa5c59ebb201fddb9a745238e8`  
		Last Modified: Sat, 16 Mar 2024 04:05:14 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ad59f09b7cfe9ed625b71c2f8de7ab974a5db023d95fbe97fa8c2d36077d09`  
		Last Modified: Sat, 16 Mar 2024 04:05:13 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-linux`

```console
$ docker pull nats@sha256:ed7d2c4f739ee88e4592880eb2c7541cf81eef672a426c3108ed9bcf16765853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-linux` - linux; amd64

```console
$ docker pull nats@sha256:a2b677be6bd67324258eee1db031ebfd408991ceba89862e17189288c0d0f9d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765403d3b7754e8f0f9d0c6ae93da0a2297e954b85bca6ec745e84b2d8638fc0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e338e1c824f87e6ce72124da6e3d777f3f418713befd0195137683f46e4e1e`  
		Last Modified: Sat, 16 Mar 2024 08:50:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:26cdc28820c5ca90c7859bc14a64c2b734d5e1e44b0759e066e481fe63137d47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d4e737c294a9b2b10c58350ac2c91069ee7c5e4b0cb875a22e316aeac10c9a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:46 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:46 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f159630d723fb35254591f813277c6864a15b4e1af2c293872364ff35252f485`  
		Last Modified: Sat, 16 Mar 2024 08:45:52 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:5f86fb8a593271cba2f3380a95fbc590bb218a4c487574beeb827b2c56070a6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5259ceafa373a7b7a73148d38f96fec6949447601b0cd46c31de87893969fd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a918e9e80cbfc3e74933281e2854ff73ba86f9528b18448d68e87a9b1da3df6`  
		Last Modified: Sat, 16 Mar 2024 00:54:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c2508454845c92a3431e0106172c3d7fff8acc31851825d2d8123bdbb45d0231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e3e46564e100a7fff7524bfff19ec0019b89f369ab18a289b23e2837c3fa94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992ffd84ea59eedf4b12ad8b56fbe3a496d3deaca06714d77157cc33a5c589b3`  
		Last Modified: Sat, 16 Mar 2024 04:05:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-nanoserver`

```console
$ docker pull nats@sha256:c0a08eb6c90b0e52d2a0eb7cbf2bd49e72e51f3a961f9302934a6791391553fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:2.9.25-nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:1e46dbde3ffefa7f4693b42a8a456ff7e4dba33e11f4cab76169d63a3dfcfa65
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110225761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c772dc25544412aa36610022d39cb7861a34d08bc6437239b73ba3359307d28`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Wed, 10 Apr 2024 01:43:32 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:47:28 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 10 Apr 2024 01:47:29 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:47:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:47:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:47:31 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826d34fcda621b296890090998100732b227a2fded8eee4d47e58e23e4a707e0`  
		Last Modified: Wed, 10 Apr 2024 01:48:21 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d02cd79646cc5afd725d708433d5ba70d6669f17f322641f53875e4ad88639`  
		Last Modified: Wed, 10 Apr 2024 01:48:43 GMT  
		Size: 5.3 MB (5330196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae1b62db39eca059a0f47334bc396f4d6baa2f92e6c0d1ffcb7c7cd5d017026`  
		Last Modified: Wed, 10 Apr 2024 01:48:42 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e25184c57e09d3476529e0bd4947414abde9578e48218bf37669081602b5c7c`  
		Last Modified: Wed, 10 Apr 2024 01:48:42 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed8e16ac9c52081dfad87f09fc9887825b185df0aece7fa3eb31ae2701baa6f`  
		Last Modified: Wed, 10 Apr 2024 01:48:42 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c62ba0972ac1c861c8af444f35fe69482a85f41e4158b4dc30e8bf1772d436f`  
		Last Modified: Wed, 10 Apr 2024 01:48:42 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-nanoserver-1809`

```console
$ docker pull nats@sha256:c0a08eb6c90b0e52d2a0eb7cbf2bd49e72e51f3a961f9302934a6791391553fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:2.9.25-nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:1e46dbde3ffefa7f4693b42a8a456ff7e4dba33e11f4cab76169d63a3dfcfa65
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110225761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c772dc25544412aa36610022d39cb7861a34d08bc6437239b73ba3359307d28`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Wed, 10 Apr 2024 01:43:32 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:47:28 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 10 Apr 2024 01:47:29 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:47:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:47:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:47:31 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826d34fcda621b296890090998100732b227a2fded8eee4d47e58e23e4a707e0`  
		Last Modified: Wed, 10 Apr 2024 01:48:21 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d02cd79646cc5afd725d708433d5ba70d6669f17f322641f53875e4ad88639`  
		Last Modified: Wed, 10 Apr 2024 01:48:43 GMT  
		Size: 5.3 MB (5330196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae1b62db39eca059a0f47334bc396f4d6baa2f92e6c0d1ffcb7c7cd5d017026`  
		Last Modified: Wed, 10 Apr 2024 01:48:42 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e25184c57e09d3476529e0bd4947414abde9578e48218bf37669081602b5c7c`  
		Last Modified: Wed, 10 Apr 2024 01:48:42 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed8e16ac9c52081dfad87f09fc9887825b185df0aece7fa3eb31ae2701baa6f`  
		Last Modified: Wed, 10 Apr 2024 01:48:42 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c62ba0972ac1c861c8af444f35fe69482a85f41e4158b4dc30e8bf1772d436f`  
		Last Modified: Wed, 10 Apr 2024 01:48:42 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-scratch`

```console
$ docker pull nats@sha256:ed7d2c4f739ee88e4592880eb2c7541cf81eef672a426c3108ed9bcf16765853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-scratch` - linux; amd64

```console
$ docker pull nats@sha256:a2b677be6bd67324258eee1db031ebfd408991ceba89862e17189288c0d0f9d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765403d3b7754e8f0f9d0c6ae93da0a2297e954b85bca6ec745e84b2d8638fc0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Sat, 16 Mar 2024 08:49:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e338e1c824f87e6ce72124da6e3d777f3f418713befd0195137683f46e4e1e`  
		Last Modified: Sat, 16 Mar 2024 08:50:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:26cdc28820c5ca90c7859bc14a64c2b734d5e1e44b0759e066e481fe63137d47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d4e737c294a9b2b10c58350ac2c91069ee7c5e4b0cb875a22e316aeac10c9a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Sat, 16 Mar 2024 08:44:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:46 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:46 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f159630d723fb35254591f813277c6864a15b4e1af2c293872364ff35252f485`  
		Last Modified: Sat, 16 Mar 2024 08:45:52 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:5f86fb8a593271cba2f3380a95fbc590bb218a4c487574beeb827b2c56070a6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5259ceafa373a7b7a73148d38f96fec6949447601b0cd46c31de87893969fd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Sat, 16 Mar 2024 00:53:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a918e9e80cbfc3e74933281e2854ff73ba86f9528b18448d68e87a9b1da3df6`  
		Last Modified: Sat, 16 Mar 2024 00:54:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c2508454845c92a3431e0106172c3d7fff8acc31851825d2d8123bdbb45d0231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e3e46564e100a7fff7524bfff19ec0019b89f369ab18a289b23e2837c3fa94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Sat, 16 Mar 2024 04:04:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:18 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992ffd84ea59eedf4b12ad8b56fbe3a496d3deaca06714d77157cc33a5c589b3`  
		Last Modified: Sat, 16 Mar 2024 04:05:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-windowsservercore`

```console
$ docker pull nats@sha256:356aad98f52e72f691fe5e7fa7c32157ebdf19d9a81cbba6fb762dd2203d301b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:2.9.25-windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:f80d25237a29b036cb4dab7cbe24d20b79110116b690b9042724ae58fd2096b3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2170421356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384f62945c116666450b422da2b22c8e1b581e5c4d7bd175895d062c0f0e363c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Wed, 10 Apr 2024 01:40:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Apr 2024 01:40:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:43:44 GMT
ENV NATS_SERVER=2.9.25
# Wed, 10 Apr 2024 01:43:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 10 Apr 2024 01:43:46 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 10 Apr 2024 01:45:11 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Apr 2024 01:47:11 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Apr 2024 01:47:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:47:13 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:47:14 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:47:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6ae8ddefe4f7d0224959df0cc91d01044dce7f127ee7c23257cf0b63bfd7ac`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266ac5d9d5680f1e3a65f9d272fc3a2ab7f67eda1b00c961365853e0a9c3e27`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d000231e1f901cb73596d1eea38d1f99e043c3aed53c558f3a7553a3fe7088d8`  
		Last Modified: Wed, 10 Apr 2024 01:48:34 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dc9fdda7712880d9a01c8bc6a4ce00cbb59e7caae96fc780685d4135f05691`  
		Last Modified: Wed, 10 Apr 2024 01:48:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ffbbcd3f996c8e229ead2b808d37f43898a7612a6be83f747eddd39df99009`  
		Last Modified: Wed, 10 Apr 2024 01:48:34 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d4a1edaf82c4db8b70e77b574a9d7dfe8cfa86293bbf69040dc30865b3b453`  
		Last Modified: Wed, 10 Apr 2024 01:48:34 GMT  
		Size: 191.8 KB (191819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987bf8adc00231373efdfe17dc7ce4f0c4481ba5dff6ac001bf8df8eec03a8c5`  
		Last Modified: Wed, 10 Apr 2024 01:48:33 GMT  
		Size: 5.8 MB (5788404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fefcee4ad4d7b3f763bee3d5dca858f368c1b9f634c506f3e5054751498e83`  
		Last Modified: Wed, 10 Apr 2024 01:48:32 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8efafd4c6558c5f6e1798f38c6445d94dc4d625bd18a4e742b0c4638019d59`  
		Last Modified: Wed, 10 Apr 2024 01:48:32 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3fca3d80cb7613a601459e05c19668accb212dde3b28c4df92b288a65eba78`  
		Last Modified: Wed, 10 Apr 2024 01:48:32 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0da1472d5e10e5bbfc309c1969496a887d9948fe44c387e2c29604f6bfd384`  
		Last Modified: Wed, 10 Apr 2024 01:48:32 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-windowsservercore-1809`

```console
$ docker pull nats@sha256:356aad98f52e72f691fe5e7fa7c32157ebdf19d9a81cbba6fb762dd2203d301b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:2.9.25-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:f80d25237a29b036cb4dab7cbe24d20b79110116b690b9042724ae58fd2096b3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2170421356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384f62945c116666450b422da2b22c8e1b581e5c4d7bd175895d062c0f0e363c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Wed, 10 Apr 2024 01:40:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Apr 2024 01:40:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:43:44 GMT
ENV NATS_SERVER=2.9.25
# Wed, 10 Apr 2024 01:43:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 10 Apr 2024 01:43:46 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 10 Apr 2024 01:45:11 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Apr 2024 01:47:11 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Apr 2024 01:47:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:47:13 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:47:14 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:47:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6ae8ddefe4f7d0224959df0cc91d01044dce7f127ee7c23257cf0b63bfd7ac`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266ac5d9d5680f1e3a65f9d272fc3a2ab7f67eda1b00c961365853e0a9c3e27`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d000231e1f901cb73596d1eea38d1f99e043c3aed53c558f3a7553a3fe7088d8`  
		Last Modified: Wed, 10 Apr 2024 01:48:34 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dc9fdda7712880d9a01c8bc6a4ce00cbb59e7caae96fc780685d4135f05691`  
		Last Modified: Wed, 10 Apr 2024 01:48:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ffbbcd3f996c8e229ead2b808d37f43898a7612a6be83f747eddd39df99009`  
		Last Modified: Wed, 10 Apr 2024 01:48:34 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d4a1edaf82c4db8b70e77b574a9d7dfe8cfa86293bbf69040dc30865b3b453`  
		Last Modified: Wed, 10 Apr 2024 01:48:34 GMT  
		Size: 191.8 KB (191819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987bf8adc00231373efdfe17dc7ce4f0c4481ba5dff6ac001bf8df8eec03a8c5`  
		Last Modified: Wed, 10 Apr 2024 01:48:33 GMT  
		Size: 5.8 MB (5788404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fefcee4ad4d7b3f763bee3d5dca858f368c1b9f634c506f3e5054751498e83`  
		Last Modified: Wed, 10 Apr 2024 01:48:32 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8efafd4c6558c5f6e1798f38c6445d94dc4d625bd18a4e742b0c4638019d59`  
		Last Modified: Wed, 10 Apr 2024 01:48:32 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3fca3d80cb7613a601459e05c19668accb212dde3b28c4df92b288a65eba78`  
		Last Modified: Wed, 10 Apr 2024 01:48:32 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0da1472d5e10e5bbfc309c1969496a887d9948fe44c387e2c29604f6bfd384`  
		Last Modified: Wed, 10 Apr 2024 01:48:32 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:bca70839d95348452fb8363f4943e3d2a45fcbea78ff7749e2b5219abb34fdf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:8b4822683d7955dc4a7b69bc138e5a980297f5562d3dc4f8417d80aed7b8a683
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9577903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78fb4abc56d19dcdd801b05d2982e749107d24ec996403c499518e1fec1d0a50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:48:58 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 08:49:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:49:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:49:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:49:01 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:49:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27675e5d86d45eba74328ac05267b7f93df29e2f079892c96c4425c216de74c`  
		Last Modified: Sat, 16 Mar 2024 08:49:37 GMT  
		Size: 6.2 MB (6168174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996c3b4c0f3e26b6ebc651c10f1889f8cf2f401651631836d63f72a1f449e9f2`  
		Last Modified: Sat, 16 Mar 2024 08:49:36 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca260fdf9bf58bec6ebf64f52cc0437d3935f22572653de018a0912f276efc25`  
		Last Modified: Sat, 16 Mar 2024 08:49:36 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:7ea677c7520bfdf6e5e8ca9f6e7ea392d39d8204f89e90b17de4f4216ae2e4fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae73509d5009d4f8bf7d5827db756183e287715cdca6b2c362c186c38d174486`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:44:29 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 08:44:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:44:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:44:32 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:44:32 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:44:32 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c6c88a86c2d4fae1df9dcfb8d0fb887644ffaeea7c7552244d72831f2deff0`  
		Last Modified: Sat, 16 Mar 2024 08:45:05 GMT  
		Size: 5.9 MB (5884864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bd557199bb46ecdb92b5224c44b2fb88b65b1d11eb03799e5d96d916cd4a17`  
		Last Modified: Sat, 16 Mar 2024 08:45:03 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4185eaec9fd629a92d2e2fb33da18b3c5ead72abf7d6f01ab6eaea92405c0031`  
		Last Modified: Sat, 16 Mar 2024 08:45:03 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:cc8f002c98389809a6e45a18f22b1a4a139c42812baaa5d01c1e81d8e4874156
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8795632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a947e574f9d2508db10e0ea9c2958039f03b151091e939cca9d6de03f552ba7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:53:15 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 00:53:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 00:53:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 00:53:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 00:53:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 00:53:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f579c68c28c186f8b3430f408c338b656e0cb429709b80e5f128a681b11be03`  
		Last Modified: Sat, 16 Mar 2024 00:53:58 GMT  
		Size: 5.9 MB (5875734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aeaa4c17e704f2825dcc8ca7892e9f8f7ca1022cf1aaa902c2ac011371fce0a`  
		Last Modified: Sat, 16 Mar 2024 00:53:56 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92b079a7c6d0b0e9f500662cfcfa735481d84fa902b2b7a607b5855ba623866`  
		Last Modified: Sat, 16 Mar 2024 00:53:56 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3ffef78bc0ff99629b91518b700220c06965c730059865cb63f18b757b7efad8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9088776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9c7035c53282319802a6491562f8b5922be8f1a7cf414229eca258cc31b74b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 04:03:47 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 04:03:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 04:03:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 04:03:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 04:03:50 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:03:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 04:03:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7be0478b9e8861bced761c3e24515379aae8068c6aea93bb91cab613608206`  
		Last Modified: Sat, 16 Mar 2024 04:04:38 GMT  
		Size: 5.7 MB (5740063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aceb56880d89429044a8d940a472616c66a9a19bd96999dd010d6fdcd95b7ccc`  
		Last Modified: Sat, 16 Mar 2024 04:04:37 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c653aab8018aa291381d9c5f0b4ff56538e6b1d1898554ee4b4b16f5b3a0498`  
		Last Modified: Sat, 16 Mar 2024 04:04:37 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:3bc80e99b7b6d2ec499b278e79ad0f54c297b46fc348702243cfc9b9d8c7f134
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9078987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99796f4dcf8fdff5bfa05a8f5bcd649457ca09cae4aba1f7dd5c08f0c6000ba0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:39:10 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 02:39:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 02:39:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 02:39:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 02:39:14 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 02:39:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 02:39:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1071fa4f216f6a3b40e9ca688766e9de8cde369fb0bfd45a363d74ae53636f6`  
		Last Modified: Sat, 16 Mar 2024 02:39:52 GMT  
		Size: 5.7 MB (5719633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cd77000169deae54f01f9739a3fdb6b49bebed3c942a1574d742e0f559135c`  
		Last Modified: Sat, 16 Mar 2024 02:39:51 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbd40a91a6c30b4a91aed2555db43edf084fff2084b3ac0e2df8f21216f3ec6`  
		Last Modified: Sat, 16 Mar 2024 02:39:51 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:d0b935e12aa8b047de70c249972f46ec57c6f9be3578e0da0f9ba7c52799dddc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9296153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd63ac9e2a4893a8a1ad3ead3903faebfe84d0aa5bdbe202e312a428745a9884`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 16:57:27 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 16:57:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 16:57:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 16:57:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 16:57:29 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 16:57:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 16:57:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bf12bda37fb5c76daad2fd35782e3ee4b626ab41f2b6ced22cec58c28600ad`  
		Last Modified: Sat, 16 Mar 2024 17:00:14 GMT  
		Size: 6.1 MB (6052515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c04c6057db41f701360bac00f880c04931706790543ceaa183b7b35172a5f0`  
		Last Modified: Sat, 16 Mar 2024 17:00:14 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a4186c9454ae05d593569eb01415dd64d39fd53169f11984d7579581b331b`  
		Last Modified: Sat, 16 Mar 2024 17:00:13 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.19`

```console
$ docker pull nats@sha256:bca70839d95348452fb8363f4943e3d2a45fcbea78ff7749e2b5219abb34fdf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:8b4822683d7955dc4a7b69bc138e5a980297f5562d3dc4f8417d80aed7b8a683
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9577903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78fb4abc56d19dcdd801b05d2982e749107d24ec996403c499518e1fec1d0a50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:48:58 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 08:49:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:49:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:49:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:49:01 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:49:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27675e5d86d45eba74328ac05267b7f93df29e2f079892c96c4425c216de74c`  
		Last Modified: Sat, 16 Mar 2024 08:49:37 GMT  
		Size: 6.2 MB (6168174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996c3b4c0f3e26b6ebc651c10f1889f8cf2f401651631836d63f72a1f449e9f2`  
		Last Modified: Sat, 16 Mar 2024 08:49:36 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca260fdf9bf58bec6ebf64f52cc0437d3935f22572653de018a0912f276efc25`  
		Last Modified: Sat, 16 Mar 2024 08:49:36 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:7ea677c7520bfdf6e5e8ca9f6e7ea392d39d8204f89e90b17de4f4216ae2e4fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae73509d5009d4f8bf7d5827db756183e287715cdca6b2c362c186c38d174486`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:44:29 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 08:44:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 08:44:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 08:44:32 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 08:44:32 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:44:32 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c6c88a86c2d4fae1df9dcfb8d0fb887644ffaeea7c7552244d72831f2deff0`  
		Last Modified: Sat, 16 Mar 2024 08:45:05 GMT  
		Size: 5.9 MB (5884864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bd557199bb46ecdb92b5224c44b2fb88b65b1d11eb03799e5d96d916cd4a17`  
		Last Modified: Sat, 16 Mar 2024 08:45:03 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4185eaec9fd629a92d2e2fb33da18b3c5ead72abf7d6f01ab6eaea92405c0031`  
		Last Modified: Sat, 16 Mar 2024 08:45:03 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:cc8f002c98389809a6e45a18f22b1a4a139c42812baaa5d01c1e81d8e4874156
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8795632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a947e574f9d2508db10e0ea9c2958039f03b151091e939cca9d6de03f552ba7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:53:15 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 00:53:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 00:53:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 00:53:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 00:53:18 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 00:53:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f579c68c28c186f8b3430f408c338b656e0cb429709b80e5f128a681b11be03`  
		Last Modified: Sat, 16 Mar 2024 00:53:58 GMT  
		Size: 5.9 MB (5875734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aeaa4c17e704f2825dcc8ca7892e9f8f7ca1022cf1aaa902c2ac011371fce0a`  
		Last Modified: Sat, 16 Mar 2024 00:53:56 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92b079a7c6d0b0e9f500662cfcfa735481d84fa902b2b7a607b5855ba623866`  
		Last Modified: Sat, 16 Mar 2024 00:53:56 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3ffef78bc0ff99629b91518b700220c06965c730059865cb63f18b757b7efad8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9088776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9c7035c53282319802a6491562f8b5922be8f1a7cf414229eca258cc31b74b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 04:03:47 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 04:03:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 04:03:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 04:03:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 04:03:50 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:03:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 04:03:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7be0478b9e8861bced761c3e24515379aae8068c6aea93bb91cab613608206`  
		Last Modified: Sat, 16 Mar 2024 04:04:38 GMT  
		Size: 5.7 MB (5740063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aceb56880d89429044a8d940a472616c66a9a19bd96999dd010d6fdcd95b7ccc`  
		Last Modified: Sat, 16 Mar 2024 04:04:37 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c653aab8018aa291381d9c5f0b4ff56538e6b1d1898554ee4b4b16f5b3a0498`  
		Last Modified: Sat, 16 Mar 2024 04:04:37 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:3bc80e99b7b6d2ec499b278e79ad0f54c297b46fc348702243cfc9b9d8c7f134
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9078987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99796f4dcf8fdff5bfa05a8f5bcd649457ca09cae4aba1f7dd5c08f0c6000ba0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:39:10 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 02:39:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 02:39:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 02:39:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 02:39:14 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 02:39:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 02:39:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1071fa4f216f6a3b40e9ca688766e9de8cde369fb0bfd45a363d74ae53636f6`  
		Last Modified: Sat, 16 Mar 2024 02:39:52 GMT  
		Size: 5.7 MB (5719633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cd77000169deae54f01f9739a3fdb6b49bebed3c942a1574d742e0f559135c`  
		Last Modified: Sat, 16 Mar 2024 02:39:51 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbd40a91a6c30b4a91aed2555db43edf084fff2084b3ac0e2df8f21216f3ec6`  
		Last Modified: Sat, 16 Mar 2024 02:39:51 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:d0b935e12aa8b047de70c249972f46ec57c6f9be3578e0da0f9ba7c52799dddc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9296153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd63ac9e2a4893a8a1ad3ead3903faebfe84d0aa5bdbe202e312a428745a9884`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 16:57:27 GMT
ENV NATS_SERVER=2.10.12
# Sat, 16 Mar 2024 16:57:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 16 Mar 2024 16:57:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 16 Mar 2024 16:57:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 16 Mar 2024 16:57:29 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 16:57:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 16:57:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bf12bda37fb5c76daad2fd35782e3ee4b626ab41f2b6ced22cec58c28600ad`  
		Last Modified: Sat, 16 Mar 2024 17:00:14 GMT  
		Size: 6.1 MB (6052515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c04c6057db41f701360bac00f880c04931706790543ceaa183b7b35172a5f0`  
		Last Modified: Sat, 16 Mar 2024 17:00:14 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a4186c9454ae05d593569eb01415dd64d39fd53169f11984d7579581b331b`  
		Last Modified: Sat, 16 Mar 2024 17:00:13 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:48c5f766b807ecc4c1d1cbd8ae4cb613e9239c698d2483b907d94cfccb4431ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5696; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:dbab4c53c0de6b089ceb67849d41bdf54a0ad29e50f1105048fc5f19508db803
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cbf0fba619173e5c4542920b1d7278a5a780baf2b54bff413b32cc0016433c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:06 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Sat, 16 Mar 2024 08:49:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:06 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866d738de7ab782f2ba4b31cfeee8894a26c596bed7b85f7072494d10cd5618`  
		Last Modified: Sat, 16 Mar 2024 08:49:54 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:23b831c97175a24dafc1e4858d66d89b5daea7b40475fa65a5a2cc646495f69f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f14c4fc39384124daeb9de82f2f548ed59cf95ac2c5163a4e7cb933758b47c6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:37 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Sat, 16 Mar 2024 08:44:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dcfc63d9869b797864f5925982e824e3b9ba24796e45cee98fa32eacb80c21`  
		Last Modified: Sat, 16 Mar 2024 08:45:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:d7d36063a70b3f92e87214db9cf07a81799734321a44db81a32d60f4dbe9747d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ed0bdac27116af7eb7ddd6d7e6b9ebd5fb952606a5faa4a84779b345103b0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:24 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Sat, 16 Mar 2024 00:53:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:25 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:25 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c56f0b0a93e98e48d30f323ee2f44dcffe8ee47dad4b9701cd95f33b1ad423`  
		Last Modified: Sat, 16 Mar 2024 00:54:16 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:17532cf8a200037fa12e16243b8739bc520937cd82a9a3b96d8db0e85d942071
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b75af84f70f1921e86eaa7dff023270dc485b37e1acca37fe2bc3e4e919f19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:08 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Sat, 16 Mar 2024 04:04:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:08 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:08 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3e7253e56d93fc4ce869656fef13511496d97e58250a301790645656c29acf`  
		Last Modified: Sat, 16 Mar 2024 04:04:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:bc4465dc1a2b2b68a903b34cd70721db4682b6ae49baad493c4fb8f9a54c1699
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123dd70806df1b073fab2d9d0cb4855270a447d3c72569af275ed24af793af46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 02:39:34 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Sat, 16 Mar 2024 02:39:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 02:39:35 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 02:39:35 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 02:39:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405bd5e4b794b6bad044e8744cf63ddd0f2e0001abde3c0b2b5e7a190706d5e`  
		Last Modified: Sat, 16 Mar 2024 02:40:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:b200d259ef6d710b801ba60a7f296791ebc5298d82db48b8f68cfc0bee79d15b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26134424de3ad1af4ffe096901272e7ea3dae1a93eeddcd6c110b08b29af4011`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 16:58:41 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Sat, 16 Mar 2024 16:58:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 16:58:43 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 16:58:44 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 16:58:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea5f20b9222048fdae4e26dc03a3a997375533021a900c72f4e6b338c144ddb`  
		Last Modified: Sat, 16 Mar 2024 17:00:32 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:5c3f90898e8204465bc8f03eeb287f3c4a74ab98abddf8e7133303a697cdcc15
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110558802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c9fe6985208f3c2b3d60ef9ba9dca290d513ed8dfd37ea890a5a30e3309db2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Wed, 10 Apr 2024 01:43:32 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:43:34 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 10 Apr 2024 01:43:34 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:43:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:43:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:43:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826d34fcda621b296890090998100732b227a2fded8eee4d47e58e23e4a707e0`  
		Last Modified: Wed, 10 Apr 2024 01:48:21 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a02eb33a3aa2cfe4eef717c0d9f835f089de87c8bf7a29ada529785e9a766d9`  
		Last Modified: Wed, 10 Apr 2024 01:48:20 GMT  
		Size: 5.7 MB (5663495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba1c2806f1a8f6a751f20ca92a1ce06f1e4694140d4837b6f890ce9e2bef92`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd1781b30607b707f2c7003388ad80836cdb8125e2d4376107843968a0d97ca`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72699a90a0ff719020f44581d9607dc75f34d1b9f79ad4baa1d2dd8a2a111558`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f3e31e8b287637780dd9b544fda9313c77847672463da5487a4f569ad663de`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:0a31000c798112718df04a19491c39f2dd8e36ba4955b8b7a9987581d5f8a033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:dbab4c53c0de6b089ceb67849d41bdf54a0ad29e50f1105048fc5f19508db803
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cbf0fba619173e5c4542920b1d7278a5a780baf2b54bff413b32cc0016433c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:06 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Sat, 16 Mar 2024 08:49:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:06 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866d738de7ab782f2ba4b31cfeee8894a26c596bed7b85f7072494d10cd5618`  
		Last Modified: Sat, 16 Mar 2024 08:49:54 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:23b831c97175a24dafc1e4858d66d89b5daea7b40475fa65a5a2cc646495f69f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f14c4fc39384124daeb9de82f2f548ed59cf95ac2c5163a4e7cb933758b47c6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:37 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Sat, 16 Mar 2024 08:44:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dcfc63d9869b797864f5925982e824e3b9ba24796e45cee98fa32eacb80c21`  
		Last Modified: Sat, 16 Mar 2024 08:45:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:d7d36063a70b3f92e87214db9cf07a81799734321a44db81a32d60f4dbe9747d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ed0bdac27116af7eb7ddd6d7e6b9ebd5fb952606a5faa4a84779b345103b0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:24 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Sat, 16 Mar 2024 00:53:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:25 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:25 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c56f0b0a93e98e48d30f323ee2f44dcffe8ee47dad4b9701cd95f33b1ad423`  
		Last Modified: Sat, 16 Mar 2024 00:54:16 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:17532cf8a200037fa12e16243b8739bc520937cd82a9a3b96d8db0e85d942071
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b75af84f70f1921e86eaa7dff023270dc485b37e1acca37fe2bc3e4e919f19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:08 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Sat, 16 Mar 2024 04:04:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:08 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:08 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3e7253e56d93fc4ce869656fef13511496d97e58250a301790645656c29acf`  
		Last Modified: Sat, 16 Mar 2024 04:04:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:bc4465dc1a2b2b68a903b34cd70721db4682b6ae49baad493c4fb8f9a54c1699
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123dd70806df1b073fab2d9d0cb4855270a447d3c72569af275ed24af793af46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 02:39:34 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Sat, 16 Mar 2024 02:39:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 02:39:35 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 02:39:35 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 02:39:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405bd5e4b794b6bad044e8744cf63ddd0f2e0001abde3c0b2b5e7a190706d5e`  
		Last Modified: Sat, 16 Mar 2024 02:40:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:b200d259ef6d710b801ba60a7f296791ebc5298d82db48b8f68cfc0bee79d15b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26134424de3ad1af4ffe096901272e7ea3dae1a93eeddcd6c110b08b29af4011`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 16:58:41 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Sat, 16 Mar 2024 16:58:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 16:58:43 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 16:58:44 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 16:58:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea5f20b9222048fdae4e26dc03a3a997375533021a900c72f4e6b338c144ddb`  
		Last Modified: Sat, 16 Mar 2024 17:00:32 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:fb9a7b002fc37c676f80fe35573e4ade35e3429aa09510c6c9e90025dc498535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:5c3f90898e8204465bc8f03eeb287f3c4a74ab98abddf8e7133303a697cdcc15
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110558802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c9fe6985208f3c2b3d60ef9ba9dca290d513ed8dfd37ea890a5a30e3309db2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Wed, 10 Apr 2024 01:43:32 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:43:34 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 10 Apr 2024 01:43:34 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:43:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:43:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:43:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826d34fcda621b296890090998100732b227a2fded8eee4d47e58e23e4a707e0`  
		Last Modified: Wed, 10 Apr 2024 01:48:21 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a02eb33a3aa2cfe4eef717c0d9f835f089de87c8bf7a29ada529785e9a766d9`  
		Last Modified: Wed, 10 Apr 2024 01:48:20 GMT  
		Size: 5.7 MB (5663495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba1c2806f1a8f6a751f20ca92a1ce06f1e4694140d4837b6f890ce9e2bef92`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd1781b30607b707f2c7003388ad80836cdb8125e2d4376107843968a0d97ca`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72699a90a0ff719020f44581d9607dc75f34d1b9f79ad4baa1d2dd8a2a111558`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f3e31e8b287637780dd9b544fda9313c77847672463da5487a4f569ad663de`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:fb9a7b002fc37c676f80fe35573e4ade35e3429aa09510c6c9e90025dc498535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:5c3f90898e8204465bc8f03eeb287f3c4a74ab98abddf8e7133303a697cdcc15
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110558802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c9fe6985208f3c2b3d60ef9ba9dca290d513ed8dfd37ea890a5a30e3309db2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Wed, 10 Apr 2024 01:43:32 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:43:34 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 10 Apr 2024 01:43:34 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:43:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:43:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:43:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826d34fcda621b296890090998100732b227a2fded8eee4d47e58e23e4a707e0`  
		Last Modified: Wed, 10 Apr 2024 01:48:21 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a02eb33a3aa2cfe4eef717c0d9f835f089de87c8bf7a29ada529785e9a766d9`  
		Last Modified: Wed, 10 Apr 2024 01:48:20 GMT  
		Size: 5.7 MB (5663495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba1c2806f1a8f6a751f20ca92a1ce06f1e4694140d4837b6f890ce9e2bef92`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd1781b30607b707f2c7003388ad80836cdb8125e2d4376107843968a0d97ca`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72699a90a0ff719020f44581d9607dc75f34d1b9f79ad4baa1d2dd8a2a111558`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f3e31e8b287637780dd9b544fda9313c77847672463da5487a4f569ad663de`  
		Last Modified: Wed, 10 Apr 2024 01:48:18 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:0a31000c798112718df04a19491c39f2dd8e36ba4955b8b7a9987581d5f8a033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:dbab4c53c0de6b089ceb67849d41bdf54a0ad29e50f1105048fc5f19508db803
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cbf0fba619173e5c4542920b1d7278a5a780baf2b54bff413b32cc0016433c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:06 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Sat, 16 Mar 2024 08:49:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:06 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866d738de7ab782f2ba4b31cfeee8894a26c596bed7b85f7072494d10cd5618`  
		Last Modified: Sat, 16 Mar 2024 08:49:54 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:23b831c97175a24dafc1e4858d66d89b5daea7b40475fa65a5a2cc646495f69f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f14c4fc39384124daeb9de82f2f548ed59cf95ac2c5163a4e7cb933758b47c6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:37 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Sat, 16 Mar 2024 08:44:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dcfc63d9869b797864f5925982e824e3b9ba24796e45cee98fa32eacb80c21`  
		Last Modified: Sat, 16 Mar 2024 08:45:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:d7d36063a70b3f92e87214db9cf07a81799734321a44db81a32d60f4dbe9747d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ed0bdac27116af7eb7ddd6d7e6b9ebd5fb952606a5faa4a84779b345103b0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:24 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Sat, 16 Mar 2024 00:53:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:25 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:25 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c56f0b0a93e98e48d30f323ee2f44dcffe8ee47dad4b9701cd95f33b1ad423`  
		Last Modified: Sat, 16 Mar 2024 00:54:16 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:17532cf8a200037fa12e16243b8739bc520937cd82a9a3b96d8db0e85d942071
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b75af84f70f1921e86eaa7dff023270dc485b37e1acca37fe2bc3e4e919f19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:08 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Sat, 16 Mar 2024 04:04:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:08 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:08 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3e7253e56d93fc4ce869656fef13511496d97e58250a301790645656c29acf`  
		Last Modified: Sat, 16 Mar 2024 04:04:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:bc4465dc1a2b2b68a903b34cd70721db4682b6ae49baad493c4fb8f9a54c1699
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123dd70806df1b073fab2d9d0cb4855270a447d3c72569af275ed24af793af46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 02:39:34 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Sat, 16 Mar 2024 02:39:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 02:39:35 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 02:39:35 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 02:39:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405bd5e4b794b6bad044e8744cf63ddd0f2e0001abde3c0b2b5e7a190706d5e`  
		Last Modified: Sat, 16 Mar 2024 02:40:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:b200d259ef6d710b801ba60a7f296791ebc5298d82db48b8f68cfc0bee79d15b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26134424de3ad1af4ffe096901272e7ea3dae1a93eeddcd6c110b08b29af4011`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 16:58:41 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Sat, 16 Mar 2024 16:58:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 16:58:43 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 16:58:44 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 16:58:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea5f20b9222048fdae4e26dc03a3a997375533021a900c72f4e6b338c144ddb`  
		Last Modified: Sat, 16 Mar 2024 17:00:32 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:b04dc3c962bbed963b7ed2272999339683a9eb46cdeaa06a77c1dbbdfe93b834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:29380f4863fb3a6f2b04217f477bee6eac525e6b36400d4446ee1680024de74e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2170781570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa73df6040c74fa785c0df500e4c8a7a76a5ce054b396330c2b4631b211c5a06`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Wed, 10 Apr 2024 01:40:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Apr 2024 01:40:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:40:04 GMT
ENV NATS_SERVER=2.10.12
# Wed, 10 Apr 2024 01:40:05 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.12/nats-server-v2.10.12-windows-amd64.zip
# Wed, 10 Apr 2024 01:40:06 GMT
ENV NATS_SERVER_SHASUM=bc944f832fdc3eaa0072c0a5e278efd672cec394159661070e7aea4f5d483cbc
# Wed, 10 Apr 2024 01:41:22 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Apr 2024 01:43:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Apr 2024 01:43:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:43:16 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:43:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:43:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6ae8ddefe4f7d0224959df0cc91d01044dce7f127ee7c23257cf0b63bfd7ac`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266ac5d9d5680f1e3a65f9d272fc3a2ab7f67eda1b00c961365853e0a9c3e27`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b45aa9398ff56a16e042bfdf01b44ff7daebf93e7cba5d601367d2c0e5a55ed`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe31b64ec7d8949724e118281dfca112c508483cc5b28076aaadd223f212b4a4`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f68caae1490441aa87bfa98ed09fc4717d036f13634615fe4eb4a1efe4925a6`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567ed00bc244d7ef610728b1545d39345e73e8e86ee441b586eea2238d1bf1dd`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 241.8 KB (241850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f8817e79dfbc8f56443618f486d64c5ac11608663b3bdf7a25f87f2412c473`  
		Last Modified: Wed, 10 Apr 2024 01:48:02 GMT  
		Size: 6.1 MB (6099353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60589928d42d9fc2f8e9ccd4a26ba13cebed25894380700f63bace8ca5fc27c0`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbe842b574fe798f092ac13841eea2cee6361f8232a3539375c0503e5911af7`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619674a0794dc85dc23997a189c9659f4612bf24f1fd187f2d26e38dbf6a8691`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd24c8b4dbeddc4174617445fd1d056589be9451dfd07af7f714867654c353f`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:b04dc3c962bbed963b7ed2272999339683a9eb46cdeaa06a77c1dbbdfe93b834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull nats@sha256:29380f4863fb3a6f2b04217f477bee6eac525e6b36400d4446ee1680024de74e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2170781570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa73df6040c74fa785c0df500e4c8a7a76a5ce054b396330c2b4631b211c5a06`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Wed, 10 Apr 2024 01:40:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Apr 2024 01:40:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 Apr 2024 01:40:04 GMT
ENV NATS_SERVER=2.10.12
# Wed, 10 Apr 2024 01:40:05 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.12/nats-server-v2.10.12-windows-amd64.zip
# Wed, 10 Apr 2024 01:40:06 GMT
ENV NATS_SERVER_SHASUM=bc944f832fdc3eaa0072c0a5e278efd672cec394159661070e7aea4f5d483cbc
# Wed, 10 Apr 2024 01:41:22 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Apr 2024 01:43:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Apr 2024 01:43:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Apr 2024 01:43:16 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Apr 2024 01:43:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Apr 2024 01:43:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6ae8ddefe4f7d0224959df0cc91d01044dce7f127ee7c23257cf0b63bfd7ac`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266ac5d9d5680f1e3a65f9d272fc3a2ab7f67eda1b00c961365853e0a9c3e27`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b45aa9398ff56a16e042bfdf01b44ff7daebf93e7cba5d601367d2c0e5a55ed`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe31b64ec7d8949724e118281dfca112c508483cc5b28076aaadd223f212b4a4`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f68caae1490441aa87bfa98ed09fc4717d036f13634615fe4eb4a1efe4925a6`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567ed00bc244d7ef610728b1545d39345e73e8e86ee441b586eea2238d1bf1dd`  
		Last Modified: Wed, 10 Apr 2024 01:48:03 GMT  
		Size: 241.8 KB (241850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f8817e79dfbc8f56443618f486d64c5ac11608663b3bdf7a25f87f2412c473`  
		Last Modified: Wed, 10 Apr 2024 01:48:02 GMT  
		Size: 6.1 MB (6099353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60589928d42d9fc2f8e9ccd4a26ba13cebed25894380700f63bace8ca5fc27c0`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbe842b574fe798f092ac13841eea2cee6361f8232a3539375c0503e5911af7`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619674a0794dc85dc23997a189c9659f4612bf24f1fd187f2d26e38dbf6a8691`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd24c8b4dbeddc4174617445fd1d056589be9451dfd07af7f714867654c353f`  
		Last Modified: Wed, 10 Apr 2024 01:48:01 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
