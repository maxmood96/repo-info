## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:e148f4762bdd9323ac1b9f0d5c59e64ce563a329b92f892e66998f131e7ae32c
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:0e75dc48efef655a6f7a4efd18d062de38fce2f24d9dc4f1051a39524f622341
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49237498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8527e8bd3510ed76b434734092a57968f5bda60807471b5c54338f1e248f3a2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:21 GMT
ADD file:74b4e0fbcb9cb38344c32a0512a72d8179f885de4b7bb127215f8d96a6262664 in / 
# Wed, 01 Mar 2023 04:09:22 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:09:26 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9d915a4248d2913bb8451eba978ac348a983990eca9186543367f5f44900e0fb`  
		Last Modified: Wed, 01 Mar 2023 04:13:25 GMT  
		Size: 49.2 MB (49237273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbdf461f58d9b4bfeca1878bc23d12676f12febee37ef0493e75610a8299c5a8`  
		Last Modified: Wed, 01 Mar 2023 04:13:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:104c0466a075f1cd7ca16ed7801a72b79bea9dc63ab604ce46c3054e4399504c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48073064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57517505edda4579869169dbee7d4f0a4e766250e01909274026463da917529`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:48:24 GMT
ADD file:1685939a153ab7a7aa03035565c60e99663abd3a416ef0d00bddaf24e0ae6f08 in / 
# Wed, 01 Mar 2023 01:48:25 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:48:30 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f7516928cdf57280d137bb31220dd9f0b6ca54e290189b42a68ab64d0d2065b7`  
		Last Modified: Wed, 01 Mar 2023 01:51:43 GMT  
		Size: 48.1 MB (48072838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba9b375e1769f8d21f3b65be340b87906da55908c4f4f61398d46209bcd997b`  
		Last Modified: Wed, 01 Mar 2023 01:51:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:8575f0588ab580eea1d3f29474ab334b64fd607a2ad5767e61f7bbda7b1d2d91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45843527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93284d62e0881b589c00663dc4f98c77b9f4666f08a41b28196c0519b573cb67`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:26 GMT
ADD file:9f8ce83cf3e75c63cb351ec688378ffe29d7105ff8e8892b3cef95aeacbf6779 in / 
# Wed, 01 Mar 2023 01:57:27 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:57:31 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4c5d14f15cd67359c9f8d5dbc636ce6ffee972aa4acbeb663e40e865b0dd7dee`  
		Last Modified: Wed, 01 Mar 2023 02:01:54 GMT  
		Size: 45.8 MB (45843301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243101e199090a32c224d7f3a66065d74d6119b53f7a8be67ca6fb61023a0a28`  
		Last Modified: Wed, 01 Mar 2023 02:02:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:31d30aa4da4250e472385ec0b40c66a3d3a9939d428ce90896bebc0ba4c29a71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49274215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341f2edc1e811d1e98ffc5dd123b681c82b876e820dad80f329482c71be482c1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:13 GMT
ADD file:5b81699b80066f9e3bc967bdf130a67f54ebe15cd80df6c952262d6132b1cabf in / 
# Wed, 01 Mar 2023 02:20:14 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:20:17 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cf639a903cc04a00c81ac77b3b9f9a79644c51b7f515895fd60403c20ff34a80`  
		Last Modified: Wed, 01 Mar 2023 02:23:22 GMT  
		Size: 49.3 MB (49273990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09d8381eede514e5da67ec0c71259dcc04516cb388863f50a1fea7d66b06876`  
		Last Modified: Wed, 01 Mar 2023 02:23:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:70f41689d5310ed27d2d69f5ce0830989a82f0603c516c8d167a39751ee5cad5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50273623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:679e55a95b6df57d6780a952d7c5b9b15d643c57186526e011b945118cb0617f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:38:40 GMT
ADD file:0ccdbb7b1f104c23abcf77c506eed771d5759d210c2284a95f85e558405a5390 in / 
# Wed, 01 Mar 2023 01:38:40 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:38:45 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b5ba6d7d02dd42cc6291ae5b4e129956756f664662a78db71f320107a1b6d189`  
		Last Modified: Wed, 01 Mar 2023 01:43:30 GMT  
		Size: 50.3 MB (50273396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219c1a640e788bbd25f45ea5863a88fe5370ca164281e6d9bd5a22c500903b28`  
		Last Modified: Wed, 01 Mar 2023 01:43:40 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:426644b7c42f4bfbf79c83df43c9259ba4cf8e87a7b748e69cd2cdfc425ff148
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49245700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc6fa77ce6a06ef64509c5e404fd8c94c27d7f0e72bba49fc8aff64cbd52ef0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:09:05 GMT
ADD file:77abd413b6799ae4f1f24f3bcc389dd12515fc4f732e81239d8c25475bc37fac in / 
# Wed, 01 Mar 2023 02:09:10 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:09:20 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:65f9863fa983221d5b14b7a7e06e92e49a04fbced0e7af12bdafbdfcbc7a2deb`  
		Last Modified: Wed, 01 Mar 2023 02:16:56 GMT  
		Size: 49.2 MB (49245473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64374528e42fffb9a9f08b972942128c40c8f8b48283c666fb226f8e5b6bfb75`  
		Last Modified: Wed, 01 Mar 2023 02:17:05 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:6952c55216b84107295acd48cf512b88d7ff3727ade295e10d373e24aa6d5f06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53250456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4fd735caf91c9b1f4d03b260ad3172101c05be5e0b2b7da50ce1ff9b01d42a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:46:00 GMT
ADD file:311d9174b941eeaaa2babe3a94b035ab7c3880d5908d630bdec420f42eff6a06 in / 
# Wed, 01 Mar 2023 04:46:05 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:46:21 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6b61b4a96c9a944bd44d67cc885cdb2ef5f9aa35a0a94dba6ea2b6372ad27e48`  
		Last Modified: Wed, 01 Mar 2023 04:52:26 GMT  
		Size: 53.3 MB (53250230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695a39025abf7b07d247dc12f9d0b285b7f824b1690a656b54cb321d27e1586f`  
		Last Modified: Wed, 01 Mar 2023 04:52:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:2234b77bb8aa233d365ee21532ac136d2d9f6e4b07c865e764fffc29f4ad595c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47608327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba0e614ef62d2ada0aa7d99f35a3e0280d092b88621af4278994b749adf3ee5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:49:37 GMT
ADD file:55baf50ca3524103dfcb38a8784744d482a5cdb19f66a7baa92d44dc18483a58 in / 
# Wed, 01 Mar 2023 02:49:40 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:49:45 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e95e47ef2a5cde1145fe4af2db22dbfe40c09cf83dbb9ff00d400d23e6dd5331`  
		Last Modified: Wed, 01 Mar 2023 02:53:58 GMT  
		Size: 47.6 MB (47608102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5fb95c020caf770f3cb3169be1c67a60312cb03ae692be255a30216a5cca4a`  
		Last Modified: Wed, 01 Mar 2023 02:54:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
