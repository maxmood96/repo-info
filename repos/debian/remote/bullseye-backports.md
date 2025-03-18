## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:78287eb4a3b72f75aa4b4439f6f8fc8b42c8359c164834002a9a08fa135fc4bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:3f37382020c77c643b60d7698ac000fbb3a9e1002654aad665d75cb382a438a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53741500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab84b8b520959d57fd18964f895263a63465693d78fe7d4e2b6c94b7b9a955e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8d1bfb80edb9306e3de72f4095daeae4c281712482255562f2e236ae85233e7d`  
		Last Modified: Mon, 17 Mar 2025 22:17:19 GMT  
		Size: 53.7 MB (53741275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331028e957d40007d97010ffa8b91a5ce99a907c0398530f348761edf4995ac4`  
		Last Modified: Mon, 17 Mar 2025 23:12:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:af9c8bac2bb7883bb4eb9e2882a5b0f7d401c7f64e3e14c96ebe8ec6552be197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03f71a482dd006cd298b426122a85d813eb0b2a1ad30512c9981401ed867871`

```dockerfile
```

-	Layers:
	-	`sha256:9c6e8de0347fff8357870f5e53c950f2a618be0e0341ef1ee27b8d0d8d9f525f`  
		Last Modified: Mon, 17 Mar 2025 23:12:12 GMT  
		Size: 3.9 MB (3917516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa1484c7fa3f656465ce6b23d5d7b4d1879ce4b50b996b4f7c268ad3beb8b358`  
		Last Modified: Mon, 17 Mar 2025 23:12:12 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:652275af1447dae0bd86d51b094178d7f2af307fe795d27e8ebdd012ed243f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49026786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ee48a00f0064e32bf995dc2e2c47645ac64aab70e496255cc47940b2d08730`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c0fd1793bf8bc1764ff6503ad6f86ae0f1151de2bd8b7285b28dc6f5cc6001c3`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 49.0 MB (49026561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e11ef2314be8727d537918f310551e2db4abac453aac126d592baf1b46c59de`  
		Last Modified: Tue, 18 Mar 2025 07:21:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:695fa30ddb29abe3d89ffe48fc399ad0c2600ede061d61402483b184e1915f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3924977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e782d26b7f6730bf418c40c8865d1ae8aa73a0e57ad831ab515010e243f2f8e8`

```dockerfile
```

-	Layers:
	-	`sha256:5a95ce28afaf697a4403d0dbb7a0bdba5cf30d96f4beaccb38db84d0c598184a`  
		Last Modified: Tue, 18 Mar 2025 07:21:13 GMT  
		Size: 3.9 MB (3919078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48d52f7c7fd9da4492ec2735483c09063b0cd29de64fc0e39f5a7b4d5d3b95e5`  
		Last Modified: Tue, 18 Mar 2025 07:21:12 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:3e3aa6d9d47119db6899ef1fecb30026eb82a4b65d762c86562648b649b48bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52248620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7afa18bbeec0ff557545a4f7563e286a4a9b4b8106eb6fe3ab4bf58e85adee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d236aea662d8f469dab5a00e2e08b90aed787cdb781ef4855f7309c237458cc5`  
		Last Modified: Tue, 18 Mar 2025 07:31:09 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d453685c888a21fc97bb4b047e045fe987df8ba276441afb3850909487dcffb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69204f7388bf90fd5e24c7dac3b913b28ce60955fde9cdd5c86b6abec46c647d`

```dockerfile
```

-	Layers:
	-	`sha256:1d643629e4e9a67fafb6b1c1a1689d039836de22e317b6bb0a2bca6d73508992`  
		Last Modified: Tue, 18 Mar 2025 07:31:09 GMT  
		Size: 3.9 MB (3917096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d138f10e99a24f0f6356ba10550c14535f9d440c24ec32b444c6a160c8302d64`  
		Last Modified: Tue, 18 Mar 2025 07:31:09 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:9942657aa1b616e8dbf5710da06ae3381fded996abe4f3364677ef7413e91d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54678842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:495702b27918f621a0ba3a01663cb26af1e553bba6b72afde4403b92b492c1f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b2bf052a55a1540734073d8a106c4845ec09ac4ac8cc46a275584d3eef876deb`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 54.7 MB (54678617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf9d229033160822550a63ef3af6d37558991b7b47d2ff7548aa0ecd986121b`  
		Last Modified: Mon, 17 Mar 2025 23:24:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:bd613016854e52c1cd129f78f82ea2fb8713976ff9a052596f6aa8bc559a0fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc1b2e247abd393e65eedd13450b6b60bed27b16e2256061054d4e90a9723ff`

```dockerfile
```

-	Layers:
	-	`sha256:d5ebe6023455f0a471863147b8a4e6e6f3639f2d8a2ac3b7fd8ec9683db8c41d`  
		Last Modified: Mon, 17 Mar 2025 23:24:52 GMT  
		Size: 3.9 MB (3914023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a446d0041ff120ed0d9622c4645001f3bdc46a631bbb849b0b03a693cef0ec52`  
		Last Modified: Mon, 17 Mar 2025 23:24:51 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json
