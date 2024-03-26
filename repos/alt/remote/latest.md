## `alt:latest`

```console
$ docker pull alt@sha256:f74029451441d27c8cb81b913b442dfb3b26d75eb17be191794dfb6dc428ee5e
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
$ docker pull alt@sha256:1c59e77d911e717d6730df713cba11241fb78a79eac162b22177a91bf3af53f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40169888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a077c79aeeba81e9624572e8794da9b9a3eb9748a6d15810b9c9979f74982d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Mar 2023 16:13:31 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:57:22 GMT
ADD file:a311881d32f36eb465f0c4d861c96e900a3a670e9a2d6bc5dcfb56207777be15 in / 
# Tue, 26 Sep 2023 00:57:24 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:57:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:00a9dbf753a7bd9a8c0c19b8aa1dbba1d03ebc9fdf1a1fc365ceb857593050ca`  
		Last Modified: Tue, 26 Sep 2023 00:58:00 GMT  
		Size: 40.2 MB (40169695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ddaa2053142cb3f63cfdb596357a1bd13c264738bfa4550740caddc1edd6ba`  
		Last Modified: Tue, 26 Sep 2023 00:57:54 GMT  
		Size: 193.0 B  
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
$ docker pull alt@sha256:634f0b6f91dec963463c1efe7d049b7d1d1a2cb96c687f0a89b58dc98a577820
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44616420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a676c0c2ea30a8399c558e02c1471770db47c72ea7e477bda27d444f4bd73b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Jul 2023 23:38:46 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:38:50 GMT
ADD file:27876d998eb510e342fb882d7f52ffc853e2c3f8be4bb5fc06dc849bc771b533 in / 
# Tue, 26 Sep 2023 00:38:53 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:38:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:53ad182393cc445f9cc01f60fe83e0e32a713ae008eed39659dd006ea63013a6`  
		Last Modified: Tue, 26 Sep 2023 00:39:33 GMT  
		Size: 44.6 MB (44616229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a017a4d6457905cb693950d9bb3b31b886c943a4d0c2f0d0dc9699fdb854af20`  
		Last Modified: Tue, 26 Sep 2023 00:39:23 GMT  
		Size: 191.0 B  
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
