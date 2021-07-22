## `debian:stretch-backports`

```console
$ docker pull debian@sha256:593dcb99da72372c78a4a7361bf31a4eca289949897cbfca16f2f6b0e6911e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:85613541931b7a403a28ef8148e73d4a1dfb94447e2714bcbb916eafcc1bf056
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45380005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd838e8a8bcbb604ec5a1feb0e2a746a15c65e95130d9c3bd6e161c553e0c149`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:05 GMT
ADD file:fc9409352ad67880b83ccf1ccd1587eb2666715eae04e4dd98fca919f1bb98d7 in / 
# Thu, 22 Jul 2021 00:47:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 00:47:09 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:08224db8ce18b31a78a0a26d1b344d173528e50a7067797c9df4de5d8df353e2`  
		Last Modified: Thu, 22 Jul 2021 00:52:52 GMT  
		Size: 45.4 MB (45379781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920845f63d19919aaaa464a25c6e38838eb5a02cfb6f7838f6882432620e96b2`  
		Last Modified: Thu, 22 Jul 2021 00:53:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:d9520ecdba160f0cd24d4ef9967967740123dc45f57f586c0be7a56ce3a28328
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44091957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c54c6002013b76ce23ec21e1c238e99416fb7791ad3327e533137f9d4275aed`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:53:04 GMT
ADD file:bfe848278f8374ee4e7de4946371b7176fc2bbcf40afce8ee1f9738af7b06694 in / 
# Thu, 22 Jul 2021 00:53:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 00:53:19 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:984fc5232b7d0db08285a008f512c6a5de7610d4f37c8c97ecd7b1bb98e2dd65`  
		Last Modified: Thu, 22 Jul 2021 01:06:29 GMT  
		Size: 44.1 MB (44091732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef83b703cc32b6e5fb7f211fdc2408f0726379728d1ae0f30ddb6db6b1c6df4`  
		Last Modified: Thu, 22 Jul 2021 01:06:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:1557050e4f9b274633b757d05b228f14053ce6436c428852d44efd1c2708fb00
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42120212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52f326f8f6a73092da241604831ae46ae6f950da31e44cabb59f5e040384ad4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:23:06 GMT
ADD file:8c289b4c3c40ee076e3b3563f38ccd72dee8b2ee3122170cf1bdd417ae9e03c0 in / 
# Wed, 23 Jun 2021 00:23:08 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 00:23:23 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d2f34e8839b40d84b70d62e2c8a6909422dad9688919bf387ad4a092d38ab62f`  
		Last Modified: Wed, 23 Jun 2021 00:36:08 GMT  
		Size: 42.1 MB (42119988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0303ae55196fdd51981e427fffff63147d663c96bfd017c180b0170bc65f88b4`  
		Last Modified: Wed, 23 Jun 2021 00:36:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:cb2fbe583c1cf16b7b77c9da6f294cdaf609869d05dd40d26a5baa365ec7e0df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43178663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae30f0f3f33df53a427a4f1da08d921edb9076c06ac7edf717568b636a66c8d3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:41:26 GMT
ADD file:fab290162e6d28cbe115c866c49a1e09d955450dc9e831ccbeefe40e18cfa3a7 in / 
# Thu, 22 Jul 2021 00:41:27 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 00:41:33 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:28ed64be8f9ee39d8ded09482441a288852dd40c2e535b64e1f9c0271c10eb44`  
		Last Modified: Thu, 22 Jul 2021 00:48:16 GMT  
		Size: 43.2 MB (43178440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cda289b5952cc5e03bebf8fcedee078dadd570a42f38b258ee47e993c36e3a`  
		Last Modified: Thu, 22 Jul 2021 00:48:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:ae65c086bcc0a6411b7e6f1cbd87e943a158b0cbdaa980faab806cb1323ebd92
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46097509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710483e4197137f480ef7b7252fce11cafe4cde02a85afd3f54343921f4a0068`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:41:29 GMT
ADD file:c83a7d581497b7df343b529417c3b904cf901379d5124d738ac2539c778912a3 in / 
# Thu, 22 Jul 2021 00:41:29 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 00:41:36 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:27f236654eb1268b8d3986746d9f9fc7ef6d5ea038754025d6953961a088aff0`  
		Last Modified: Thu, 22 Jul 2021 00:49:20 GMT  
		Size: 46.1 MB (46097283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d3f3899a81aee5f07eec9ea56d260e1441f5ac4a70766e9dab504ed41d1a32`  
		Last Modified: Thu, 22 Jul 2021 00:49:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
