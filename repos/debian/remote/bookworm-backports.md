## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:e2c135b5a74d812d02ef0048a75d81edacc11056ee0cb43f4db7890ec778517f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:55b1858f3b8b8a22988424da0897c075f606115010dcdbcd40110f02159dd7bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48497289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378cb9e88dc794b0509245cc85ab416c5c3acdf7d7fa1f8a87c47d9db491df10`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f457a5d6ab73a557b2bfb216daea5ca4100c68b5ff61e2fa24accabf124e680`  
		Last Modified: Tue, 24 Dec 2024 22:13:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fc807435d8c53d3302db0493d370d669f6db88055b4bfff197b57ef6708fba77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbe49874d7ea7e2c531c67dd007697f33f42add10df004d5dbbd316f058dd32`

```dockerfile
```

-	Layers:
	-	`sha256:5e939ef767b2cd4b64162fc5513f216296028a0c368572ab841e4705a55fa2c5`  
		Last Modified: Tue, 24 Dec 2024 22:13:34 GMT  
		Size: 3.6 MB (3619210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a5d598f7dcc00a8180e4e917b780cdecff40d1e576f2ee07ee24833fb8d7cb2`  
		Last Modified: Tue, 24 Dec 2024 22:13:34 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:a092acf448e4fdae4788852e14cbfda9da45ae8418e27f3e26134ce945516856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46024467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8238452189664381c9d912a027ed9df7daae5291d21f7a9f90a35e1ca4da15`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9bbb619898c2cd76f2f957a170378432dffd62e9bd50226234d805ff7ac0d544`  
		Last Modified: Tue, 24 Dec 2024 21:33:13 GMT  
		Size: 46.0 MB (46024242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb32a10127d938bd16992601370c9a31e761d62af3d54ad2e249a6525b669d14`  
		Last Modified: Tue, 24 Dec 2024 22:20:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:18f150f2f4b994c5230397ee2d27a1b12fc17057a2b7724a6ff71d3dece764cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f81d72b45aa483ccd475329c03963fe0ffdedb78ebad400e5c713502631287`

```dockerfile
```

-	Layers:
	-	`sha256:73431ae75380695b5202fc69912a3f7016cc99757b8e81017c8860c0d96f285f`  
		Last Modified: Tue, 24 Dec 2024 22:20:30 GMT  
		Size: 3.6 MB (3619411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee1dff5d56ab82030f78fdc02a57d7a7c63f1108d3e9ee9b453e4509a3cbf81`  
		Last Modified: Tue, 24 Dec 2024 22:20:30 GMT  
		Size: 5.9 KB (5898 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:557045cfda0a5bc69fdc0c67291bbc69d143b1412743693398eccbbde12cd212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44200191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be13756d02c7299457f3533d21fd0a3ea7aa3aed86d1d1aea75653c039336eef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14b1fcde3bff40c5d2c8f3bd6f6dc4e38d3cc3fadac1b82467952036f7550d6`  
		Last Modified: Tue, 24 Dec 2024 22:16:40 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9eb223c0aa5aa81b3f876d353873492ae4aafa5c30d9441165e4f6522f2f2272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9309d0c074a2a99925a9c86b35de48d586ebb08c34eb5c7e20367ff10352f7`

```dockerfile
```

-	Layers:
	-	`sha256:fb1c75b34989b6674c4348adb13b8a518c2a0765fdefdb526f735d868186eb9a`  
		Last Modified: Tue, 24 Dec 2024 22:16:40 GMT  
		Size: 3.6 MB (3621389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:848ca72fd3c23e3a148a7c4dc3a81ec36f03063a044b92a7841ecd78b8db14b5`  
		Last Modified: Tue, 24 Dec 2024 22:16:40 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b371339d55f79bc65c58e239aeb86acd821abfbf78ac027405a04a209c664639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48325709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b43bf3642104efc321f18e8a47df792c38d3d6f3cbc6a2a59aeb9e3c25cb51`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95960be7e0bbed626283b5fda294fad26cec329e0509258001eca10bea93432f`  
		Last Modified: Tue, 24 Dec 2024 22:17:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:23689afd37c5263a3607cb5af51991882921a5672abbe738f42f85e0d7f46017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe36bac5e7b804c2fc3f21b8a0d30dbcfaa7101b3ec6935ec299b07205300a2b`

```dockerfile
```

-	Layers:
	-	`sha256:c956f9632741d19259d27de702687ad778d836ad18734a5b4b4fa4f80b7408f7`  
		Size: 3.6 MB (3619425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:814a1b1ac3438d3f694c304b01570828531602029c091db5b7af1bb906716d26`  
		Last Modified: Tue, 24 Dec 2024 22:17:29 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:709f672806a7273833b052860eda321b89594ead7ba64aaf33c5096097de2ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49476149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56246e0c9492306740e6780f9354278aad46325a65cf48d17ef74f668e0f77b1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:dd322311a74f01b8b9ba5bb8502c37125af9fcf12a3c2deee1502f4932057adb`  
		Last Modified: Tue, 24 Dec 2024 21:32:22 GMT  
		Size: 49.5 MB (49475925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0f91e7179f16a117defd8c49b2368dc781c6995764589ea7adb1def1024ffc`  
		Last Modified: Tue, 24 Dec 2024 22:13:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:23bee6322dcb60255e0a3cf106db743a11ec853a6c9f4e15779698f231046074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3622201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2efd89be3ecee35183e37dde70ecf1f23225fa619875523b9c1d87f0ef34fef`

```dockerfile
```

-	Layers:
	-	`sha256:7ade672c7f88cda1b3825e619730bccbe743a95339ebe853222cb94c5130fe17`  
		Last Modified: Tue, 24 Dec 2024 22:13:56 GMT  
		Size: 3.6 MB (3616371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c371684432bdcf81773371fc96ecaa10b93bba9e92872e5c32116e85d30c012`  
		Last Modified: Tue, 24 Dec 2024 22:13:56 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:9c0b7a4aea4f1a52e3c134a1b8060d8cece243320305abd5a4779a55ce0bd1f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48771868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381c551039cb7d59ee811cecee2aa1785a7b022fd0b9947d7ba850e1d9160e8a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:fa42b2983a081afbe5b1653f1c107472f7b73564ae2a3f6a75d6b4702023cc0c`  
		Last Modified: Tue, 24 Dec 2024 21:33:19 GMT  
		Size: 48.8 MB (48771644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6e8e1f7fdd5310d62e802665746fa1fd6af87e97fe7a4d430ceaaae255fdbe`  
		Last Modified: Tue, 24 Dec 2024 22:16:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:999bad2a76b990593e8b006a955f91dd79eb07324892f603591a6737e665d021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43062c5e2282f3f75bb68e295c561273c7cbce5872c88158b23309e9c080076a`

```dockerfile
```

-	Layers:
	-	`sha256:63fa52b4128d374fa5345e91ecbe54518ce29ff79450d6478abaadb0ae1f52ac`  
		Last Modified: Tue, 24 Dec 2024 22:16:31 GMT  
		Size: 5.7 KB (5671 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f20830764caf7c462e6b7d9a1ccf92d1d63e58cba00c9b51072b5c7af816168e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52328300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b009b6c9e8841acd8ff28e2a89764b1ef88f134e0bdf21118460f941f7c860`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3c2ef19bde71e2b0389d85d8d7fbb661b54c54bf3cd31f57b4d15788f16890`  
		Last Modified: Wed, 25 Dec 2024 12:49:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f18a75518b663ab4a0f05fa4cf3934065f902804a56e9da5409fd095d937419a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f929bf902c15d3471e2ca88bc1f91991cfcceb9a43564068748f05448bab105c`

```dockerfile
```

-	Layers:
	-	`sha256:d04703dffa7eafb77a11e73603016abcf1054169d9457fa1d9a258a11e5d272f`  
		Last Modified: Wed, 25 Dec 2024 12:49:27 GMT  
		Size: 3.6 MB (3623470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9a183c27b0dcc321089bbb2c25a3adb698ab1701cc1595fe0314775e5682b7b`  
		Last Modified: Wed, 25 Dec 2024 12:49:27 GMT  
		Size: 5.9 KB (5873 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:6ca160d86abddc3e365d71b3f01c9a60b740f9a4971349bc7146400f229fea4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47149848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b881831f16d5066b6bc0c739d2032fa6ea29697ef060ea614eae5f97add87c6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Last Modified: Tue, 24 Dec 2024 21:33:12 GMT  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d326bef67d327323484b84067a4ca8b10c90607707ec0c0a73d374912093094`  
		Last Modified: Tue, 24 Dec 2024 22:13:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0f8700d860c81677d0b14f32e436bffe7f105345b6995d6fc0247accd3c7db04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3624786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26246480d0a32dc9d5a0acb08d47311b3373532510791541cce7b09d858e308`

```dockerfile
```

-	Layers:
	-	`sha256:91b4f88cbf30e742e9e5c2242764ff7259a9e7ec4defdd96feba17ce18711640`  
		Last Modified: Tue, 24 Dec 2024 22:13:41 GMT  
		Size: 3.6 MB (3618940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01392a046fa542efd4d882b4c8d7eb3528b704df7a6112c82dd9230d693afc60`  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.in-toto+json
