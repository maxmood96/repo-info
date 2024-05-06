<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `alt`

-	[`alt:latest`](#altlatest)
-	[`alt:p10`](#altp10)
-	[`alt:sisyphus`](#altsisyphus)

## `alt:latest`

```console
$ docker pull alt@sha256:0b4a08164be7f597146b1b5a98ead6ce49fb97c495c82ec4210c46b68c2ef7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `alt:latest` - linux; amd64

```console
$ docker pull alt@sha256:79102c50d99ec026c51c95f220b9b4d80c214066ac7e988e9411f2ffc9c68315
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43995970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4d2d33ad597aa08980c56d6fc8e79a38822125109e671ffc1038f7bb08e19f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 22:28:37 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Mar 2024 00:34:44 GMT
ADD file:618d531559b14019c7909934ad14719a85bb58a9b127f0ec3d403d32e2f6d920 in / 
# Tue, 26 Mar 2024 00:34:45 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Mar 2024 00:34:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:475d8f73519df7bab1fc56cabfb75410f5d7bb8b95bdfb9830005766290b7318`  
		Last Modified: Tue, 26 Mar 2024 00:35:17 GMT  
		Size: 44.0 MB (43995778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3807f2c3a2e35f554cc2475b040058c5b301d351b28b5e1e5c97f8961f088b4e`  
		Last Modified: Tue, 26 Mar 2024 00:35:10 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; arm variant v7

```console
$ docker pull alt@sha256:0393734c407ea4026e2dd3b04272552099ff94120f91c574aac7c2b9dbc9057b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40212429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6488719d5ac09c1f074829963e35b82f12d93194824260910ed58a0a81deb895`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Mar 2023 16:13:31 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Mar 2024 00:57:41 GMT
ADD file:bace52f0adf42b7d183f069367bc743aacfc138925b8061e346ad06f4fecab94 in / 
# Tue, 26 Mar 2024 00:57:44 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Mar 2024 00:57:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4f8bd306681c1511cfc6524e6155b56bcd5090fc4803165f54c30dca6ea62845`  
		Last Modified: Tue, 26 Mar 2024 00:58:07 GMT  
		Size: 40.2 MB (40212239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860b7ac26d36d8522975a050b915ea037a8e9fbe948161dcebba70046266f37c`  
		Last Modified: Tue, 26 Mar 2024 00:57:59 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:c831dc270b8d04cc6b40f600e46c75f464914699eda9e4ab28972afbd7107492
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43207857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3371129c9fa4cd8280c9fcd94fdfec2da5b0171f749b231ecf6e0c19c4dca6b6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:39:36 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Mar 2024 00:27:34 GMT
ADD file:464b73a0a4e7e611c1e9bfb06a33188428f2f4e1ce2372e6ba1c90decd3afcd7 in / 
# Tue, 26 Mar 2024 00:27:35 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Mar 2024 00:27:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6ac60b6d26d53fc2a403207e6c6af42c76edc8a3aad45af5e76e52064c7184d`  
		Last Modified: Tue, 26 Mar 2024 00:27:59 GMT  
		Size: 43.2 MB (43207666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3154bda171f7d3c2fff4daf3ff18fb8947537671c39cb1c6afd9ea1627f0f2f`  
		Last Modified: Tue, 26 Mar 2024 00:27:54 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; 386

```console
$ docker pull alt@sha256:5f3b81b59d7ec2b52048f64b3a4c6d616e4954966729023eede628478c9bf0f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44671346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b232ecacaa018e5be77ebf3eae652ba2521b2ccc2ab9c70998dd28e8866054`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Jul 2023 23:38:46 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Mar 2024 00:59:59 GMT
ADD file:b50c2b1bd9a9ec798d1fe5b2e1d71f5c3a8f3d3a3e6e7b6e2c45a2651264ff61 in / 
# Tue, 26 Mar 2024 01:00:00 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Mar 2024 01:00:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c32866586cdafe17b1575cace69314f4a635f8656687c8d66152a58616070c70`  
		Last Modified: Tue, 26 Mar 2024 01:00:32 GMT  
		Size: 44.7 MB (44671154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb4dacabbbe46ac9677a2f1db210e49fde6b0199273724884bc18554d3f761f`  
		Last Modified: Tue, 26 Mar 2024 01:00:23 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; ppc64le

```console
$ docker pull alt@sha256:3b309dd4f5b8aa3d59b0b0bc64e2f1fb133bd5ddfed9d749266bc3beb2eddc87
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46926777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f6850034e12f25a213e4dac93ac92f5675bedcfa1679cdfa123e28913117dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:16:44 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Mar 2024 00:18:32 GMT
ADD file:58493639f2fd9a0a51fa2ceb9049a5e6833acd8c530cb5e96da2d56414fbf92a in / 
# Tue, 26 Mar 2024 00:18:37 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Mar 2024 00:18:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d626015173e562c30e7a5b3826b5aa0ecb84c25f1f0fd03732fcf37fc4074d40`  
		Last Modified: Tue, 26 Mar 2024 00:19:32 GMT  
		Size: 46.9 MB (46926586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd1a2d0d2f637deec30b07039be7504ca0b3e727913bca10167c198398e8063`  
		Last Modified: Tue, 26 Mar 2024 00:19:24 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `alt:p10`

```console
$ docker pull alt@sha256:0b4a08164be7f597146b1b5a98ead6ce49fb97c495c82ec4210c46b68c2ef7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `alt:p10` - linux; amd64

```console
$ docker pull alt@sha256:79102c50d99ec026c51c95f220b9b4d80c214066ac7e988e9411f2ffc9c68315
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43995970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4d2d33ad597aa08980c56d6fc8e79a38822125109e671ffc1038f7bb08e19f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 22:28:37 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Mar 2024 00:34:44 GMT
ADD file:618d531559b14019c7909934ad14719a85bb58a9b127f0ec3d403d32e2f6d920 in / 
# Tue, 26 Mar 2024 00:34:45 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Mar 2024 00:34:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:475d8f73519df7bab1fc56cabfb75410f5d7bb8b95bdfb9830005766290b7318`  
		Last Modified: Tue, 26 Mar 2024 00:35:17 GMT  
		Size: 44.0 MB (43995778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3807f2c3a2e35f554cc2475b040058c5b301d351b28b5e1e5c97f8961f088b4e`  
		Last Modified: Tue, 26 Mar 2024 00:35:10 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:p10` - linux; arm variant v7

```console
$ docker pull alt@sha256:0393734c407ea4026e2dd3b04272552099ff94120f91c574aac7c2b9dbc9057b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40212429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6488719d5ac09c1f074829963e35b82f12d93194824260910ed58a0a81deb895`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Mar 2023 16:13:31 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Mar 2024 00:57:41 GMT
ADD file:bace52f0adf42b7d183f069367bc743aacfc138925b8061e346ad06f4fecab94 in / 
# Tue, 26 Mar 2024 00:57:44 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Mar 2024 00:57:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4f8bd306681c1511cfc6524e6155b56bcd5090fc4803165f54c30dca6ea62845`  
		Last Modified: Tue, 26 Mar 2024 00:58:07 GMT  
		Size: 40.2 MB (40212239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860b7ac26d36d8522975a050b915ea037a8e9fbe948161dcebba70046266f37c`  
		Last Modified: Tue, 26 Mar 2024 00:57:59 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:p10` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:c831dc270b8d04cc6b40f600e46c75f464914699eda9e4ab28972afbd7107492
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43207857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3371129c9fa4cd8280c9fcd94fdfec2da5b0171f749b231ecf6e0c19c4dca6b6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:39:36 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Mar 2024 00:27:34 GMT
ADD file:464b73a0a4e7e611c1e9bfb06a33188428f2f4e1ce2372e6ba1c90decd3afcd7 in / 
# Tue, 26 Mar 2024 00:27:35 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Mar 2024 00:27:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6ac60b6d26d53fc2a403207e6c6af42c76edc8a3aad45af5e76e52064c7184d`  
		Last Modified: Tue, 26 Mar 2024 00:27:59 GMT  
		Size: 43.2 MB (43207666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3154bda171f7d3c2fff4daf3ff18fb8947537671c39cb1c6afd9ea1627f0f2f`  
		Last Modified: Tue, 26 Mar 2024 00:27:54 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:p10` - linux; 386

```console
$ docker pull alt@sha256:5f3b81b59d7ec2b52048f64b3a4c6d616e4954966729023eede628478c9bf0f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44671346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b232ecacaa018e5be77ebf3eae652ba2521b2ccc2ab9c70998dd28e8866054`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Jul 2023 23:38:46 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Mar 2024 00:59:59 GMT
ADD file:b50c2b1bd9a9ec798d1fe5b2e1d71f5c3a8f3d3a3e6e7b6e2c45a2651264ff61 in / 
# Tue, 26 Mar 2024 01:00:00 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Mar 2024 01:00:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c32866586cdafe17b1575cace69314f4a635f8656687c8d66152a58616070c70`  
		Last Modified: Tue, 26 Mar 2024 01:00:32 GMT  
		Size: 44.7 MB (44671154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb4dacabbbe46ac9677a2f1db210e49fde6b0199273724884bc18554d3f761f`  
		Last Modified: Tue, 26 Mar 2024 01:00:23 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:p10` - linux; ppc64le

```console
$ docker pull alt@sha256:3b309dd4f5b8aa3d59b0b0bc64e2f1fb133bd5ddfed9d749266bc3beb2eddc87
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46926777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f6850034e12f25a213e4dac93ac92f5675bedcfa1679cdfa123e28913117dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:16:44 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Mar 2024 00:18:32 GMT
ADD file:58493639f2fd9a0a51fa2ceb9049a5e6833acd8c530cb5e96da2d56414fbf92a in / 
# Tue, 26 Mar 2024 00:18:37 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Mar 2024 00:18:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d626015173e562c30e7a5b3826b5aa0ecb84c25f1f0fd03732fcf37fc4074d40`  
		Last Modified: Tue, 26 Mar 2024 00:19:32 GMT  
		Size: 46.9 MB (46926586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd1a2d0d2f637deec30b07039be7504ca0b3e727913bca10167c198398e8063`  
		Last Modified: Tue, 26 Mar 2024 00:19:24 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `alt:sisyphus`

```console
$ docker pull alt@sha256:fd749c14bcd6f85bc5bad4d63fa6c593ea29905e297abcb55b5c365b5a7410a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `alt:sisyphus` - linux; amd64

```console
$ docker pull alt@sha256:0bb07859639e226337aaf22bc8b293d79d170054d3b902ffb45c6a23001bf7e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42190568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d051b620ce6b5d039d249bd0ffe717809be04fc4936c7c7381356a020625267`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 22:28:37 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Mar 2024 00:35:00 GMT
ADD file:59d874d2e1cbfacc14696915b0d10b77fa761491452b8b7332bd8344e13832c8 in / 
# Tue, 26 Mar 2024 00:35:01 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Mar 2024 00:35:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e92e2a59e32fb52c3c83bbd2f579d708bba44c585a2040277eb38bd3d74a2340`  
		Last Modified: Tue, 26 Mar 2024 00:35:32 GMT  
		Size: 42.2 MB (42190377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0185efb53c2a20a12339ee5c0df91560e00533bdae3d97ff827430bc71202579`  
		Last Modified: Tue, 26 Mar 2024 00:35:25 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:84728c610032152137915d52536da0b03c3d99ab83853d9efef2749fa876f753
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40999397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58c7ab0dc86b582fddbf456eef18c05812b43d2d0828aa026d86b8a1e90a393`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:39:36 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Mar 2024 00:27:44 GMT
ADD file:b726b3f38b840775128aca0361fa2d16d662710d2e5144bbfa3d6477b57c9d6e in / 
# Tue, 26 Mar 2024 00:27:45 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Mar 2024 00:27:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ae0204cee66384724a36827a5d0e71933ed4b89470905532630fead17af75204`  
		Last Modified: Tue, 26 Mar 2024 00:28:13 GMT  
		Size: 41.0 MB (40999205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81c43f59c9c5296f22a87148501ec55fd4cbeb41baee2b53ced5ba9945a6ec9`  
		Last Modified: Tue, 26 Mar 2024 00:28:08 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; 386

```console
$ docker pull alt@sha256:c366a71922398907e0ab02f26f39b0fa4342717479967c2ac6d64aa1f6f8e4bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42330009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1ea1c88c71fe1278cf31d65763bb1aa6531c1d62ab6789c7fca7b742bc0806`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Jul 2023 23:38:46 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Mar 2024 01:00:13 GMT
ADD file:0b365b70061f0a638d24b52f6a5cf6de460d3c0361d4b8a653fe21c42f92f46f in / 
# Tue, 26 Mar 2024 01:00:14 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Mar 2024 01:00:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b895f6cc6490b4c7324f648bc3e02f7def799d31e26454588f22b68383681bd3`  
		Last Modified: Tue, 26 Mar 2024 01:00:51 GMT  
		Size: 42.3 MB (42329819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b71ceec1145e7f71adc79fed3272948bfaff4d6c77ae8a2cdc2595700a039b`  
		Last Modified: Tue, 26 Mar 2024 01:00:42 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; ppc64le

```console
$ docker pull alt@sha256:133619f2b08779fdb3d1a3c085a8823646940fd4a01023880e86d332cd6c9d95
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44451882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843a0c05676c605d455a9cd00deca8c1cf41a2a4bec14a300c90dcc9fd508625`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:16:44 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Mar 2024 00:18:53 GMT
ADD file:53af9cc2d9792fbc30ab3bb757b1e7554a8c9e176ac506e30623944aab59670e in / 
# Tue, 26 Mar 2024 00:19:10 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Mar 2024 00:19:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:93301f406215feca246cf97ed1854abe85a246980fb5893137bb0a7e1da40a8c`  
		Last Modified: Tue, 26 Mar 2024 00:19:48 GMT  
		Size: 44.5 MB (44451691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e54f39ecf389639638882b96fdb17664956e2792039ba2449040d1e78f4efd`  
		Last Modified: Tue, 26 Mar 2024 00:19:41 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
