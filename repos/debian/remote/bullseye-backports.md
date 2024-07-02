## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:af68d6b98dd94e3837c0f487aebc36023cf84f008631eaea9a8cf171bbfa4250
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

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:91e6da93e3ea2624f2285009163d4da5c9bf85fb1d15e18b693f8b8e385ae054
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55099415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543d38697ee8da8482cfc82e868cdc3b1ea1c965a21ef1e02725ecb6b1aaec5e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:05 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Thu, 13 Jun 2024 01:21:06 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:10 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae9dbdeca981eb6513f5812e966c7f90fd17180da8d0190d27934ba32985290`  
		Last Modified: Thu, 13 Jun 2024 01:26:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:f3d18ef99f5048742ed025e778f273340841e44f3ce7ec9e922f4d6e7deee935
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52585976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28b5917efabc87188d77eb5dc2706fd5daba907e5d5a923cf982d9767773afc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:48:35 GMT
ADD file:cb32078a57dd8b6e640717e8afff9bcae9ea1cf42a7bd24509f83795da6d69ed in / 
# Tue, 02 Jul 2024 00:48:36 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:48:38 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cbbd165d7f0cb06245f1b11503844a1b512035157df3061a56ffc65bcd1fb0fa`  
		Last Modified: Tue, 02 Jul 2024 00:51:50 GMT  
		Size: 52.6 MB (52585748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e66598105fb1684cdb73823a57ee302a2fd885d366762da4a1597df024cb6f`  
		Last Modified: Tue, 02 Jul 2024 00:52:02 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a8ba1e2f532735cc812329d1b355045192aae9bf258505bc120ebd591cb85eba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50239222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f6e87697d78bfe9c6da21c95c8558eff0956c83827907ed9e9568ef88993f8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:11 GMT
ADD file:6e828fd5dbd54f949f96129ea922c27ff88709484119faef51401e338e900e6e in / 
# Tue, 02 Jul 2024 01:00:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:00:15 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a0610bbe9cb80952dba5ef5efb55f03668fd4f8ab63ade3ba30e22a4c03c42da`  
		Last Modified: Tue, 02 Jul 2024 01:03:38 GMT  
		Size: 50.2 MB (50238998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb989d6012106b1fe9f1370196797624fe22434b5a0f795f8165dd6c3fed2c2`  
		Last Modified: Tue, 02 Jul 2024 01:03:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:11a5daca385942e799b1f008c9fad581fac207f511e7988fdfe00f59d56f3acd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53721878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0d4362a6e6fd859eb061aa887ef422ed6b7fb9532b4c49e962a6cb67582651`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:43 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Tue, 02 Jul 2024 00:39:44 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:39:47 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0802ad790d16cc0b0b6d030ca18bc113a8bfdc85df9c5cecee9d492f178b6fb8`  
		Last Modified: Tue, 02 Jul 2024 00:42:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:0d6fc75881955af7eeecf03141dbc75e50f7d6515744314fe8891d644cb84ecf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56065197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede74306a4843b031c0a5f6ebe86d20b41cbcaa84df90a7e1d6b1dc0aa0c1659`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:05 GMT
ADD file:e6fa59569d6234c463e39f7c2465f2984240a5e8cd613c1ffdc14ab3abb4a7ad in / 
# Tue, 02 Jul 2024 00:39:06 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:39:09 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:72a2b38d7f88bb9b0be6097180e8f8261c31815017cb512a158422c2bfba6973`  
		Last Modified: Tue, 02 Jul 2024 00:43:02 GMT  
		Size: 56.1 MB (56064975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fced53f0a17d48e59eb7ed5e0cd45af16d35557fd1f50d0b0e21769b3b57ad`  
		Last Modified: Tue, 02 Jul 2024 00:43:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:cfa8be9c5080706b5cb78aa8da9063b97050b7dbcee357c7ded73ae803a9aea5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53322730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cbf058adbd36dd5bc7f53db2051538969c3498066693b4b7965b352737b80cc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:11:08 GMT
ADD file:2fd9c13efc7b13ca68928f53acc0c79d5841bd49e5aea46b2e1906120bba2a4f in / 
# Thu, 13 Jun 2024 01:11:14 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:11:29 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6c9f7b7d6baf92c8cec25b325ea14db33b8c298218a5bcd368bb24184c5645b6`  
		Last Modified: Thu, 13 Jun 2024 01:22:39 GMT  
		Size: 53.3 MB (53322503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5f945d1cdc70b3b504a30d262b4521614a83da89b69d4f2ad1cc62d27c0934`  
		Last Modified: Thu, 13 Jun 2024 01:22:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:862895c97f978c812b8563be8de0bbc7dd2c55e9251c306704b12ef94c9f3231
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58950624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c622e98c3c3b302bd571ed74dae21fd579831e01366ee84366da626f0d631bc9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:17:47 GMT
ADD file:288859e020cf9178f55732ac2eaa62400e2c2d66b3ca500ac7df69c8025abba9 in / 
# Tue, 02 Jul 2024 01:17:50 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:17:55 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:202e493da11eac96a36d754afa396feec67f46e0492e70c0cc4d61dfb06d6a75`  
		Last Modified: Tue, 02 Jul 2024 01:22:20 GMT  
		Size: 59.0 MB (58950397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bea6143222d3d493b60f2341e82e3bd8fea53c10291b862da110c8ffb79b67`  
		Last Modified: Tue, 02 Jul 2024 01:22:32 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:b0b47bccee416384f12e628a9039aaa1fa371a0d3c5893f72fb945b7b5b52a66
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53320049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6f324528afed221c68866499ba4fe39ce58c908315de0bcf3c5d65108b461a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:43:57 GMT
ADD file:5752d26037cbb262eeafd1819ecd77ecf8a8cd0019683c05fb92c50c6a458861 in / 
# Tue, 02 Jul 2024 00:44:00 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:44:06 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:aa9549a3d8effd17bc1f93fd40d83261d2505d37791c5aa837c9f7c0fff5c9e3`  
		Last Modified: Tue, 02 Jul 2024 00:48:47 GMT  
		Size: 53.3 MB (53319825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059ddb8aeeb47ef6d85f95438f328ba6d43193c824c76e3e1ad3abbce4f0a598`  
		Last Modified: Tue, 02 Jul 2024 00:48:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
