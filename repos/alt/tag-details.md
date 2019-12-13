<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `alt`

-	[`alt:latest`](#altlatest)
-	[`alt:p8`](#altp8)
-	[`alt:p9`](#altp9)
-	[`alt:sisyphus`](#altsisyphus)

## `alt:latest`

```console
$ docker pull alt@sha256:1f1c1c14c22921d723cfb1f8d4d83e261ec22e4cdf4784cd2bc0940b93cd48ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `alt:latest` - linux; amd64

```console
$ docker pull alt@sha256:e8ad71e5d3975646358048e79e658bc8af78bbb586a8568c5125c7f8e73224c9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42313198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da94ec073c8064bd288978915b46b97ed34e343c689599ed668f7dedfad989a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Sep 2018 21:19:34 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 05 Nov 2019 01:19:42 GMT
ADD file:8facd6ccfd12784ba6c31f65149811924dc313b55b37e7bde2c82529c9b1d088 in / 
# Tue, 05 Nov 2019 01:19:43 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 05 Nov 2019 01:19:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d7c87d8366c714d4c61cb0110a1b2e77e32d41041a6ae3f7e9c851c077a8918c`  
		Last Modified: Tue, 05 Nov 2019 01:20:27 GMT  
		Size: 42.3 MB (42313014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5ec8147b8137b97fd3c3b4badf3ff9c094c225021ea035ce3ac218e57e370`  
		Last Modified: Tue, 05 Nov 2019 01:20:20 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:14796576ca956279ba546aa5ada6feddd06a7d85da2ca8530f8efd3727edbe7a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41112976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06f625daff8ec633bd31e7ec6aa5935e809d8195c32614b0d0ff4087e68a4aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2019 22:39:34 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Fri, 13 Dec 2019 22:39:52 GMT
ADD file:f83cf05a5dd13072174a4c9efeb98761493560bf0de9cbf63e89c91017bc2fee in / 
# Fri, 13 Dec 2019 22:39:56 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Fri, 13 Dec 2019 22:39:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:60d7cf0ba066512184262e04ba06b2761b39ca5b6085809b05d20af7ced8060f`  
		Last Modified: Fri, 13 Dec 2019 22:40:42 GMT  
		Size: 41.1 MB (41112792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9737ce3c2b506ca6359ea2a584d229ea860a8658ca73ca0830ced100c2fdba`  
		Last Modified: Fri, 13 Dec 2019 22:40:32 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; 386

```console
$ docker pull alt@sha256:85f156275aa48b6be623dc1c34e48d116511568599801e39b3c5bcab63ddb0a6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42504092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d141b92c0765950672a7b29508c9bc5531776645d74b535af457efcbd54d921`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Sep 2018 10:38:37 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 05 Nov 2019 01:38:49 GMT
ADD file:40b3411b1096993e1ced2a87e547cc05692539869eca82a5517126e1164f9d40 in / 
# Tue, 05 Nov 2019 01:38:50 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 05 Nov 2019 01:38:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3c6bfc4016cf07e0655001ba53027d6fbbb756b090886107ac677d5d80d4b2d9`  
		Last Modified: Tue, 05 Nov 2019 01:39:47 GMT  
		Size: 42.5 MB (42503909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134c77697620e4e13cc768264731a1a790223e3587cf231aed3645cbd5ee4827`  
		Last Modified: Tue, 05 Nov 2019 01:39:35 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; ppc64le

```console
$ docker pull alt@sha256:68b552cef0eed089b41a6f8ee275f8e045e6f17e550d00993dec6d1cc6d2f07d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45973541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca81b4d2c37d543b2aec85aa296c270029670b3829ec8400a2c852af18f50ae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Jul 2019 23:03:07 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 05 Nov 2019 01:22:53 GMT
ADD file:50e00fb1ea47a03d1219528d1c54959b5636c5146c91c6c83836ae42d00dd878 in / 
# Tue, 05 Nov 2019 01:23:02 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 05 Nov 2019 01:23:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b0202c1414bfe877d15b4699e1e5ae82bc7af9a5ee01fd3bca5cb282634b7174`  
		Last Modified: Tue, 05 Nov 2019 01:24:05 GMT  
		Size: 46.0 MB (45973355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f2dbe8471172533a813cbb68fbaba53d3c9c10220d95d1c8f9a0d27f17f847`  
		Last Modified: Tue, 05 Nov 2019 01:23:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `alt:p8`

```console
$ docker pull alt@sha256:327ab705fbe56e354a5ec4c8d7d65fa4bb41fee7920c2204d7b833a8f1d01d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386

### `alt:p8` - linux; amd64

```console
$ docker pull alt@sha256:55d60eb86101476fd5ddd507014426ba1224b17a3f8d97928784f92b126b9abd
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35094038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55730270151669338ffa84ef70215cdfb00112923d3d1522f457d8d86342bd61`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Sep 2018 21:19:34 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 05 Nov 2019 01:19:57 GMT
ADD file:59adcb02728cd8ac9260bf4e214af8376f11894099eb8f64d67398b144a0dc0d in / 
# Tue, 05 Nov 2019 01:19:58 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 05 Nov 2019 01:19:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:43b48c0a1d2b8a4610d9032879802617e8d0f0a2bb1dd4c78cd496ceb428ead9`  
		Last Modified: Tue, 05 Nov 2019 01:20:37 GMT  
		Size: 35.1 MB (35093854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db147da0e5959acba167d7fe9024153e7e46b7268227c8728a2ac5d30d5f0b9f`  
		Last Modified: Tue, 05 Nov 2019 01:20:31 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:p8` - linux; 386

```console
$ docker pull alt@sha256:41f91bce1a2ac78a34bb47b174fb0d60f3b1e1394eba4c6ccf916c04253b7d09
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35260681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043cf68956c9b2e4cf8aaef8df012418b5b4819cf978003693ba467803e211c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Sep 2018 10:38:37 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 05 Nov 2019 01:39:08 GMT
ADD file:116e6c1b8b2e8adc740f1560bf87f314a9b7e2dfb8f2e0084180e20160d9e376 in / 
# Tue, 05 Nov 2019 01:39:09 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 05 Nov 2019 01:39:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:101cd90655e8b1248b797a513a2c3eb212e7f5a6ab6b8d4e2f2e959029be41a5`  
		Last Modified: Tue, 05 Nov 2019 01:40:00 GMT  
		Size: 35.3 MB (35260498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b13d4144e3d14a1213cc265be4af279e6d5bdcab9d9197032ac957859182fc0`  
		Last Modified: Tue, 05 Nov 2019 01:39:51 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `alt:p9`

```console
$ docker pull alt@sha256:1f1c1c14c22921d723cfb1f8d4d83e261ec22e4cdf4784cd2bc0940b93cd48ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `alt:p9` - linux; amd64

```console
$ docker pull alt@sha256:e8ad71e5d3975646358048e79e658bc8af78bbb586a8568c5125c7f8e73224c9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42313198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da94ec073c8064bd288978915b46b97ed34e343c689599ed668f7dedfad989a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Sep 2018 21:19:34 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 05 Nov 2019 01:19:42 GMT
ADD file:8facd6ccfd12784ba6c31f65149811924dc313b55b37e7bde2c82529c9b1d088 in / 
# Tue, 05 Nov 2019 01:19:43 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 05 Nov 2019 01:19:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d7c87d8366c714d4c61cb0110a1b2e77e32d41041a6ae3f7e9c851c077a8918c`  
		Last Modified: Tue, 05 Nov 2019 01:20:27 GMT  
		Size: 42.3 MB (42313014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5ec8147b8137b97fd3c3b4badf3ff9c094c225021ea035ce3ac218e57e370`  
		Last Modified: Tue, 05 Nov 2019 01:20:20 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:p9` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:14796576ca956279ba546aa5ada6feddd06a7d85da2ca8530f8efd3727edbe7a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41112976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06f625daff8ec633bd31e7ec6aa5935e809d8195c32614b0d0ff4087e68a4aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2019 22:39:34 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Fri, 13 Dec 2019 22:39:52 GMT
ADD file:f83cf05a5dd13072174a4c9efeb98761493560bf0de9cbf63e89c91017bc2fee in / 
# Fri, 13 Dec 2019 22:39:56 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Fri, 13 Dec 2019 22:39:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:60d7cf0ba066512184262e04ba06b2761b39ca5b6085809b05d20af7ced8060f`  
		Last Modified: Fri, 13 Dec 2019 22:40:42 GMT  
		Size: 41.1 MB (41112792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9737ce3c2b506ca6359ea2a584d229ea860a8658ca73ca0830ced100c2fdba`  
		Last Modified: Fri, 13 Dec 2019 22:40:32 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:p9` - linux; 386

```console
$ docker pull alt@sha256:85f156275aa48b6be623dc1c34e48d116511568599801e39b3c5bcab63ddb0a6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42504092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d141b92c0765950672a7b29508c9bc5531776645d74b535af457efcbd54d921`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Sep 2018 10:38:37 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 05 Nov 2019 01:38:49 GMT
ADD file:40b3411b1096993e1ced2a87e547cc05692539869eca82a5517126e1164f9d40 in / 
# Tue, 05 Nov 2019 01:38:50 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 05 Nov 2019 01:38:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3c6bfc4016cf07e0655001ba53027d6fbbb756b090886107ac677d5d80d4b2d9`  
		Last Modified: Tue, 05 Nov 2019 01:39:47 GMT  
		Size: 42.5 MB (42503909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134c77697620e4e13cc768264731a1a790223e3587cf231aed3645cbd5ee4827`  
		Last Modified: Tue, 05 Nov 2019 01:39:35 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:p9` - linux; ppc64le

```console
$ docker pull alt@sha256:68b552cef0eed089b41a6f8ee275f8e045e6f17e550d00993dec6d1cc6d2f07d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45973541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca81b4d2c37d543b2aec85aa296c270029670b3829ec8400a2c852af18f50ae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Jul 2019 23:03:07 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 05 Nov 2019 01:22:53 GMT
ADD file:50e00fb1ea47a03d1219528d1c54959b5636c5146c91c6c83836ae42d00dd878 in / 
# Tue, 05 Nov 2019 01:23:02 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 05 Nov 2019 01:23:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b0202c1414bfe877d15b4699e1e5ae82bc7af9a5ee01fd3bca5cb282634b7174`  
		Last Modified: Tue, 05 Nov 2019 01:24:05 GMT  
		Size: 46.0 MB (45973355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f2dbe8471172533a813cbb68fbaba53d3c9c10220d95d1c8f9a0d27f17f847`  
		Last Modified: Tue, 05 Nov 2019 01:23:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `alt:sisyphus`

```console
$ docker pull alt@sha256:2e2007a564300dbaf2cfeb7f229c96e4347f95ce6e98f023623fa106d16de66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `alt:sisyphus` - linux; amd64

```console
$ docker pull alt@sha256:d664791feacdd504d02272edb50aa835225a819d7003a61f296856abfc940dd4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42495001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0619238f113bc528f76e69dc47b676b8be2ea6c01f6ecccddd7890763f7dac4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Sep 2018 21:19:34 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 05 Nov 2019 01:20:11 GMT
ADD file:f0c6b6b7b70f35183b1a01b69239174d75800670e047a4c2ebf58265df0ff7df in / 
# Tue, 05 Nov 2019 01:20:11 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 05 Nov 2019 01:20:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:07ed095e5ea6bcd8917c717d87570c82f824e5c9860a92ff80400ea16beb94c3`  
		Last Modified: Tue, 05 Nov 2019 01:20:47 GMT  
		Size: 42.5 MB (42494819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab0dd21e81584817b2431517d8df54166396c41d2a98e09efafa1aa085e9c79`  
		Last Modified: Tue, 05 Nov 2019 01:20:40 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:5b893675078f31b0bc7216ca2c90d73108302dd4a28ccc304ca96ae9186d39c1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41306108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029742de4e99c7c61c0eb63ca4148957946d1e9fa1cf1534b5cdd14a51bb3ba2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2019 22:39:34 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Fri, 13 Dec 2019 22:40:19 GMT
ADD file:3a55fb343d5c1e9866c190a45f6ed01ab539e65b6af83484ec18f175ca741417 in / 
# Fri, 13 Dec 2019 22:40:22 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Fri, 13 Dec 2019 22:40:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dd75d82833b1ac700959183e216aa3f793f0389cb3b52a525657e925d879afd4`  
		Last Modified: Fri, 13 Dec 2019 22:41:00 GMT  
		Size: 41.3 MB (41305924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a90c499664f67cb894d21a7d3b67a0b50ac47b76324272a0528ca7018438819`  
		Last Modified: Fri, 13 Dec 2019 22:40:49 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; 386

```console
$ docker pull alt@sha256:5c27c74b9e9fa72324ddcf649ba0c8f9e1123603f0c1b48d93890fb31a77e770
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42665255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2d53e9e6fa48ced267656004c9268debada923531cca7d30cadb916ce7a91d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Sep 2018 10:38:37 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 05 Nov 2019 01:39:24 GMT
ADD file:c9280baeaf23bca5d8f87d1c3899d5f1bc15800bc67b5e73efcc03964e4929f2 in / 
# Tue, 05 Nov 2019 01:39:24 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 05 Nov 2019 01:39:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:068d1711c5569823403be37b3128c0adfa9307e0bbdae5fbe1fdc5b983baaf91`  
		Last Modified: Tue, 05 Nov 2019 01:40:15 GMT  
		Size: 42.7 MB (42665073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841a68fc6d53dda30a41d0167ed5f30e2c81e43bff5feadb2b99d73ada8e9c8f`  
		Last Modified: Tue, 05 Nov 2019 01:40:04 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; ppc64le

```console
$ docker pull alt@sha256:984b9e2d2f2522ec7187b640b15d260ea6244d99c70c61f9325f0ba98218685a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45980532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada2d9afa61a58b99dcf3e7ff3c8f965ac3dbf96684d518ec138b838def082dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Jul 2019 23:03:07 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 05 Nov 2019 01:23:26 GMT
ADD file:c45db79c22933a6ae1d5b21c59802334e0e964b7a9997a4b70759287089108bd in / 
# Tue, 05 Nov 2019 01:23:36 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 05 Nov 2019 01:23:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7d4fa87bf22deb354fa8c044f7162c07cb390c9a0d1bc655dff1c4c69fb2410b`  
		Last Modified: Tue, 05 Nov 2019 01:24:25 GMT  
		Size: 46.0 MB (45980347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56352067f31c8f7ba273ac33db7e09d625590e9a38842236fd8cb183888dc2fb`  
		Last Modified: Tue, 05 Nov 2019 01:24:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
