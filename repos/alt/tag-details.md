<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `alt`

-	[`alt:latest`](#altlatest)
-	[`alt:p10`](#altp10)
-	[`alt:p9`](#altp9)
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

## `alt:p9`

```console
$ docker pull alt@sha256:6e22e9d79d1e1329e9d4817a4f03fbf9bc651a0a3f1691c751031379722c29bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `alt:p9` - linux; amd64

```console
$ docker pull alt@sha256:f221359928d06fbd44e68a41d6e350d3bc8ed9e128bf11f720e9bc9ed7453392
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43153381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358e918635f9514343d7250ab41954e0d679ed9deb112e0f204c4a65cd08cb6c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 22:28:37 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:20:20 GMT
ADD file:d8242110452bcf5ddab4588a7f08e599d097a1a7c895878121f4f05ce7b98cc5 in / 
# Tue, 26 Sep 2023 00:20:21 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:20:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a71abbdd5e26300bfc77703fc0298a0dd33562d0d2fa0170006aaefc80249f1f`  
		Last Modified: Tue, 26 Sep 2023 00:21:01 GMT  
		Size: 43.2 MB (43153190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c413b96361246a5033686233d189b6f4553f8797382550a1586bb1927427288`  
		Last Modified: Tue, 26 Sep 2023 00:20:55 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:p9` - linux; arm variant v7

```console
$ docker pull alt@sha256:12ae5d23a0959833292fe7c45d5636254421b2862636463ac3c7de53b2b700c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38635105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d06e79101beac990e5fa088fdaad4116e132bde82ff3d5bfdf4f5f2d87055ac6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Mar 2023 16:13:31 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:57:33 GMT
ADD file:50b42ecb394014f2e3cb8098382fa5611a228210496bf4c8c5a6c3135b658c50 in / 
# Tue, 26 Sep 2023 00:57:35 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:57:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:69277cf044c1becb541c51054ea4e419f530f20bb8839f83163f9d4f590cc674`  
		Last Modified: Tue, 26 Sep 2023 00:58:14 GMT  
		Size: 38.6 MB (38634913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49baa735343f2f32a662eea00106b89e744805f2768449de5844aa919106004e`  
		Last Modified: Tue, 26 Sep 2023 00:58:08 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:p9` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:f27d9e4e6a8596ab300613684df7d3fae8dc89ee3d16b78de3f94bc841b7660c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41947315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b1b9226a6f580e989dd3d2cb9eefc5461f3221f00182e0e0bc3f7e964c1a35`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:39:36 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:39:26 GMT
ADD file:ce5d1f47adde45854462ae072d9cf9bb93eabc5e84a8c7206aa646dce73dd243 in / 
# Tue, 26 Sep 2023 00:39:27 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:39:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f12633f1b989acb82780f56e4b2dd7571242a5862224d94d1b4ef41c51403bde`  
		Last Modified: Tue, 26 Sep 2023 00:40:01 GMT  
		Size: 41.9 MB (41947125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1327fc42bf1c6d792ae368f63a11f606819cdb57aefdde8c3a531f098d5b5b59`  
		Last Modified: Tue, 26 Sep 2023 00:39:55 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:p9` - linux; 386

```console
$ docker pull alt@sha256:520bc632e10f7a16cb0b9d505939b1d9975f5a368e2728412819cc45ff41ae33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43289880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231f30f1536732b1be662aec8e7de070df630e9fc24b9daffd8d14d9e49302d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Jul 2023 23:38:46 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:39:04 GMT
ADD file:c235c6b804723addec4fffbc791c26c3b42437c836e2dd57c235a057a13f101e in / 
# Tue, 26 Sep 2023 00:39:05 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:39:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5a059694dc47ce9a1816aac59118833bce316d8cc8241bea58ee3bb227685fc9`  
		Last Modified: Tue, 26 Sep 2023 00:39:49 GMT  
		Size: 43.3 MB (43289689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111454471b31627c091a876e28ba9015e00448ea2692adacdd3c537600123649`  
		Last Modified: Tue, 26 Sep 2023 00:39:41 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:p9` - linux; ppc64le

```console
$ docker pull alt@sha256:bab06b7a9a7566cdc23011b5925d0175d765421c04be8a645dab0bd7b4070255
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46885044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b600fe3a3fb201d584e18534e93b2439340007a132153fb0d5c78537ca9a0ab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:16:44 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:16:52 GMT
ADD file:683d80ddf5044790ee282736c9f246568be2ed3990241a8977d55eae1bfbc511 in / 
# Tue, 26 Sep 2023 00:16:57 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:16:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4ff179bec0aadb6a0ffd3675589552330df52bed4aa2f97c485cd66fe87f9a93`  
		Last Modified: Tue, 26 Sep 2023 00:18:02 GMT  
		Size: 46.9 MB (46884852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b59576dcf664fc874bdb1af5e4e689f3eeb0e04c871b4bd41107754b79a368`  
		Last Modified: Tue, 26 Sep 2023 00:17:50 GMT  
		Size: 192.0 B  
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
