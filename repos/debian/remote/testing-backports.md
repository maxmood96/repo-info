## `debian:testing-backports`

```console
$ docker pull debian@sha256:97fc82e6e51151b460d39b583e372144b8a310433f48c36dbff5dfdd2b793627
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:24275d9e2ba720ef8812ad86f2c298c2ef977599138ef0b7a0356546bc03c5ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50106716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d99c9f63f2d5b2e294ab6a1760d14ef45edddf9b6617fec1a2a87782a2ac23a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:36:25 GMT
ADD file:22d1bfbf515d54cfb8cc550ff465c1c0cb9a4abf7a340310c25b479079210d01 in / 
# Wed, 11 Jan 2023 02:36:26 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 02:36:29 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:37f2817160f3b2632e4625bfb13687ea793d896785b941bf53c171a4f2951c49`  
		Last Modified: Wed, 11 Jan 2023 02:41:43 GMT  
		Size: 50.1 MB (50106493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69581142712563d1f4a4b629b26f87ad2c870811609a9fb37f577ae57c1ffae9`  
		Last Modified: Wed, 11 Jan 2023 02:41:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:4fc33c6484c52eb8ff80d0e6ee04714118cc72fae161bd2d8ccd3a5ebdc53228
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49082555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7fe54d5d99feb3aada8673aed66f9390ee29c060bddae0653691ce960713d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 01:56:39 GMT
ADD file:70ecdbbe1efef529c0262baf0ad4072331a784785df28c8fee2d93b1a5223887 in / 
# Wed, 11 Jan 2023 01:56:41 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 01:56:47 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0d7ef8a27395ecf9c3176f897cf0e5c4e27b796ea9f36aa4f95220793cec6517`  
		Last Modified: Wed, 11 Jan 2023 02:02:27 GMT  
		Size: 49.1 MB (49082332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7598b76a08178bf193c5a3b0b7c15f3865a23edf193e22c8e789db3502296ff5`  
		Last Modified: Wed, 11 Jan 2023 02:02:37 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:5ab5fdd42b7ee8e9715eb9673816fa66d57b316ee01067185595efee282e028e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47101498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665aac10d1e249b528687669700ea6ba099060c5c4073263dc2fc42b3d50701b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 02:00:23 GMT
ADD file:2464d580ef377342093ea4da0745280f6d8fba2b913d8f3728bf125268e2065c in / 
# Wed, 21 Dec 2022 02:00:25 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:00:31 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:35b273b4faaae730a4309cfd0e073cfa7605d57066ec7dc0223010364de06667`  
		Last Modified: Wed, 21 Dec 2022 02:08:23 GMT  
		Size: 47.1 MB (47101274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe1010a70ea4c1c98419b91746d67668040a3fd028dba57a3e59bbde58d3a88`  
		Last Modified: Wed, 21 Dec 2022 02:08:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:3cd07d32cf922018823fedbc3d084dd431798bb57c6d77fb4c436da071fed0e7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50161839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03bbfbb9cb427d27dcb41bff76da44cbc3ea4796ab2a0a901d6ce5bc5b654077`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:58:45 GMT
ADD file:c23924e713ab52b9d332f43e0c153ad7676a8ebae8388a7b66e72a85167a3573 in / 
# Wed, 11 Jan 2023 02:58:46 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 02:58:48 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:df0aed7e9ae695c99ecd2ff90171c1fba9f80c00a6b0d37535d97eb1cc63c0cb`  
		Last Modified: Wed, 11 Jan 2023 03:03:50 GMT  
		Size: 50.2 MB (50161618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67153c3c50f70e92dc818da99b8171b63df39546a4ceb4c39be81457b88befe9`  
		Last Modified: Wed, 11 Jan 2023 03:03:59 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:ce5780f1c63a5c5777795b1229032f3bd227ac91478951d86b85ef7d99afe886
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51145242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ea49ebc3017e5cc14b962db842e3952b4001101a4abdd34634af1f6be4c1d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 03:18:06 GMT
ADD file:6844d4a2dc67679bd73a46761f113cb7f8966710bd5a9b2c6bb11aaa98558eae in / 
# Wed, 11 Jan 2023 03:18:07 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:18:13 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f8a2a12389e2c4a78c1b304491d95bc5cdfc352a48454885618037364b690bb1`  
		Last Modified: Wed, 11 Jan 2023 03:24:57 GMT  
		Size: 51.1 MB (51145018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f382fe9eb3f42c0537d0a37a3c28253532baf5d788966d123f63536467dfe8ae`  
		Last Modified: Wed, 11 Jan 2023 03:25:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:a791edfe77bcbac554a24c6ad63240495f41ca53fd9b689211fc0de9c7aff904
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50336974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbcb6471465eee3c21095b46a9e5673ebbdbbd2efe84d814ac1d17aa9a8c5534`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:13:23 GMT
ADD file:0ea57818080c1e2a27e984470ee82b0bab064d2e4b4be6ca9d01d22a5809e021 in / 
# Wed, 21 Dec 2022 01:13:29 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:13:41 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9ca4c0ef78d0e2f931410fff75dce27a7514137f55186f813fab43dee045e67b`  
		Last Modified: Wed, 21 Dec 2022 01:21:51 GMT  
		Size: 50.3 MB (50336750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deef66fb7c7edf26847770ed5aaf0895d243ba7188a88fe333f07c0b706d9489`  
		Last Modified: Wed, 21 Dec 2022 01:22:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:2496a891fd3de654847a8b871d4e83c4b0d5bf9541a59244fcabc2cdc2e3eac2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54374071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a3af2cacf3a5bb06b49e26f4797afe4e7b1949038f2ec4d4a471c55f02bfac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:19:07 GMT
ADD file:c58cc45feb60d65ccecf542b088f713fa2decc069cecaf0ff37bbca477c34ac4 in / 
# Wed, 21 Dec 2022 01:19:11 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:19:16 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2a152fa39f694f5032f5c8d0a519acb4cdafaf4169f0b86827d60fcd95708b5a`  
		Last Modified: Wed, 21 Dec 2022 01:25:23 GMT  
		Size: 54.4 MB (54373846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27485ef592734350f4a51c35679d38f5d41266df9e21251f5019aab13d59f177`  
		Last Modified: Wed, 21 Dec 2022 01:25:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:09683d091bfb2ab1032df0b2012d5e95a77a13652413b39562b7a2fe9b7dd36b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48490565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5081795c1115a2e2233280f4af78eff9e980bc91f59a0596dff1b5c4975b2c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:23:40 GMT
ADD file:ac9964771c4e7224346f001dc091e76636dd09c018508912039d5c864dbc00bc in / 
# Wed, 11 Jan 2023 02:23:43 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 02:23:50 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fe4bbb99e2d8a8d2b4ec0efe0d3e7ec02880eff2464668330a95c54e25ecf0fa`  
		Last Modified: Wed, 11 Jan 2023 02:27:59 GMT  
		Size: 48.5 MB (48490343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15ee0fbaeaa9d316beade558486ffd0592729569a654459c626b9973e7d8837`  
		Last Modified: Wed, 11 Jan 2023 02:28:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
