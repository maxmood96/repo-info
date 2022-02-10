## `alt:latest`

```console
$ docker pull alt@sha256:747841551740b17e2bbb948c158bb62ea3ffa37af11b10092a3a4cadf644d961
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
$ docker pull alt@sha256:0054b7dcda3129adb591780aafa94cb707a27a6017f50f06e84e4089a5a3a5c3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41851870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b2b53e813f5743de937458b5d7e22bbdd5ebc6f0de65be020718710baa42f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 22:28:37 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Wed, 09 Feb 2022 22:19:49 GMT
ADD file:11e7012d33c06e547e6f0c7050c32bd4747261f3b07e4096adec660fed669e4b in / 
# Wed, 09 Feb 2022 22:19:51 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Wed, 09 Feb 2022 22:19:51 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ccaf2fae478c64c9c51bc3ac8c0066b6f0a61444bd3c22d0d0ece5317d4b9281`  
		Last Modified: Wed, 09 Feb 2022 22:20:27 GMT  
		Size: 41.9 MB (41851677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f64ac690d0b5b33d640b678b3666e65d37559a3309d65c7d7d53e9d3a7860e`  
		Last Modified: Wed, 09 Feb 2022 22:20:20 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; arm variant v7

```console
$ docker pull alt@sha256:e8d0a6450f871c923d47be878549906dcf1779645d8f32a4543ab78d4c78be6d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38374141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f88de11e67e936706c4b76999d04daf0dd9c6bc201403e5ddcf8c80acaa00f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Aug 2021 01:09:27 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Wed, 09 Feb 2022 22:57:40 GMT
ADD file:1b4b8e377e4ef5b4ff3bb99efee62768aaae90f1f4b9777b8a52690de84f2137 in / 
# Wed, 09 Feb 2022 22:57:42 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Wed, 09 Feb 2022 22:57:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fa69d6a0aa46c0aa2d2c80393ceb37a905f248aee6bdba719629703f2804ddbd`  
		Last Modified: Wed, 09 Feb 2022 22:59:29 GMT  
		Size: 38.4 MB (38373949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53bb3083884347d79abf922a2b3be50725762a89a53cd85af04516e0b799fb4`  
		Last Modified: Wed, 09 Feb 2022 22:59:05 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:b9ceeae2c0b3607849063d85581616b12db4706e453af60fb74e42cd3d39ad2f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40850498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f393a00779c03226e463902b51064ac8e2d41412d0fa4d1e3e21c3fb121897`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Dec 2021 16:01:29 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Wed, 09 Feb 2022 22:41:14 GMT
ADD file:cefc9474a3343690ded41893cedfa9702b5aadd11cc4644a18abef329db64bd7 in / 
# Wed, 09 Feb 2022 22:41:15 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Wed, 09 Feb 2022 22:41:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e66c94493244eb26cd6285f52e4b56186139b486bcc33f5389576d467d0adfd9`  
		Last Modified: Wed, 09 Feb 2022 22:41:58 GMT  
		Size: 40.9 MB (40850307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4abbe5c7b4c822c8171587ce22aa2a1732433d7fbcf3183954b2efc8ec804c0`  
		Last Modified: Wed, 09 Feb 2022 22:41:52 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; 386

```console
$ docker pull alt@sha256:bfffd61e23cc13cba719f44b7e4da1f579bddf66187c03814a78e33992593fde
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42571025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e9ebc0e8096c9812a25901c843ff68ccda7d5a5740966077e82eb72ce9a092`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 22:45:24 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Wed, 09 Feb 2022 22:38:45 GMT
ADD file:7799cb8f0a62798da9293d48173d9b7c8419f9850591ee956204d5519702ab3f in / 
# Wed, 09 Feb 2022 22:38:46 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Wed, 09 Feb 2022 22:38:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4441a20ee0a0b56420444739743c56b7c01e42b1085492df7acf045fb034e4a2`  
		Last Modified: Wed, 09 Feb 2022 22:39:34 GMT  
		Size: 42.6 MB (42570834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcfd87f65f665afce177ccd4dd0e87ace85645adfb85f937629ac71c8834d08`  
		Last Modified: Wed, 09 Feb 2022 22:39:25 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; ppc64le

```console
$ docker pull alt@sha256:1baf30444fc00d6d994bb52f8cbee11fbc73b89afbe3f46eee74abdfb41c367f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44664023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696e86df5719f2f89a9897f22e1ecbbb6b8abf0c87f5f047651b356f97c508e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 22:29:43 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Wed, 09 Feb 2022 22:23:30 GMT
ADD file:b27281c63dae2e0067286c0d584a2ae761072d75c968cd067c440fa87327ad55 in / 
# Wed, 09 Feb 2022 22:23:42 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Wed, 09 Feb 2022 22:23:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:73d67dccc54e0dadc0e7c48320aaf1ee7adf55abc728da94c299ba1209883630`  
		Last Modified: Wed, 09 Feb 2022 22:25:17 GMT  
		Size: 44.7 MB (44663830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb08477591ec9af6cba91bdeb7702ce3b0da6c323cb046f14759600d34b76d3`  
		Last Modified: Wed, 09 Feb 2022 22:25:09 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
