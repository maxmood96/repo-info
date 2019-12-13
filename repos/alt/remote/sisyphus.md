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
