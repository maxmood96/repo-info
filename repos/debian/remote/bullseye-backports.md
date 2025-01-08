## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:67f174affbf5f6ac78fd3801a5027ce3b92097955f46a8c4773363f12e4fd316
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
$ docker pull debian@sha256:84ed1790bc7f4868ffa67c6d9191fc896589c533edacc46aec5a048a270b99de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53739181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f204ecd13199a97742e508205ff61d94b3e12eaba52e59c85d7a3130f170ed28`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dccc9591d21115ff55cb68b6ad3e23a2b3172462d076dee682b220d4ebf1d1a`  
		Last Modified: Tue, 24 Dec 2024 22:13:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ff561b0ede2ea93d151066b77e987b405b5da27c837a55ef8efba5069461ce39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16009a604b8397edda3817fb89f28724b307865ffe1dd52acb5b20a74767f33`

```dockerfile
```

-	Layers:
	-	`sha256:29faa879d2ae9ba99c17776802b2e7f1267ce94ab40246231c2e225b1faecdfd`  
		Last Modified: Tue, 24 Dec 2024 22:13:58 GMT  
		Size: 3.9 MB (3917516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:826889499f82cc68d24f4c9b6da4633827ca9bf411eea8438de5f253b68252f9`  
		Last Modified: Tue, 24 Dec 2024 22:13:57 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:1d379a4c81142e1556af8df05b1326acbcca909758a70f8e04912c3da1374fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49024991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d53db00b50fafd465a2b22c574c4333d2cbbe83ed91c37ac14fe305b14f60d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 24 Dec 2024 21:34:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c25abad382fb7b17466665da9d935de024d7b6f207e3437ef03e70ae8676435`  
		Last Modified: Tue, 24 Dec 2024 22:16:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:21a84fdfb5ae40b3127ba61136375d069980fa4ee74841a0cf6744b108f10258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3924977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d09ffff1b6f13a1944d3d1552b5967c8d7cda18f381277a5a583c9b4e351e4ab`

```dockerfile
```

-	Layers:
	-	`sha256:af10a8747720b54c00f98e864772f36890c5ade988a4a373113bcde0ecf0e97a`  
		Size: 3.9 MB (3919078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a120924482a066181da1c7a26758b90acc47f4df02b3f65e730fa9652cadeb60`  
		Last Modified: Tue, 24 Dec 2024 22:16:58 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:150775c55d6b024ce32869a4a064cbaeb6c3f734c01328eb35f65dde70d884b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52245923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba9e1a4cccdf458e6215795dd2b0fbf577e19aa76c46bad56783a9ef91b093e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a911210198b8398970aeec573144fb776017c7731555a24369243ebea84ebf08`  
		Last Modified: Tue, 24 Dec 2024 22:17:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9fe078e2a1c858062ceb89a8bc19ac4df7c267f112452cb797bde8c98cb49257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4609c6107350ab065595b42696499ea8e0a511700ccc34873ce57843ad9ab3dc`

```dockerfile
```

-	Layers:
	-	`sha256:3c369765ad3403d6dfed7020b5596e42a2e69ace80dc6a8e1435cf744bc555b6`  
		Last Modified: Tue, 24 Dec 2024 22:17:44 GMT  
		Size: 3.9 MB (3917096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85d64a51f64009aa682f76d4a6fd9ccfeeb7046379a3eb12386cd9b63b8d8c12`  
		Last Modified: Tue, 24 Dec 2024 22:17:44 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:67a5736c8632116893ebac7488223f219f55aae9ec51a65e8a3a2c1f49427cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54676240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:464eb68cb4e10da5074969cdd5c02be9fbee6fcb0c33f7458da56dab62ffcbd7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a55e8c1d476cce2b4e35296e308f64a29659366cc595b7e6019851c3e8bbe7cf`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 54.7 MB (54676016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20959c9f3f2802e9401195b1c92330155537b3e5601619db66e5286a0a9391c`  
		Last Modified: Tue, 24 Dec 2024 22:13:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e9483ca78c92728ed86eac8ed966fc6925dca6be63b60b9876813855781bf6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f6e6989617e28d7bce3b5de58da36ecd883029de72db9a7266412af4c1621a`

```dockerfile
```

-	Layers:
	-	`sha256:349551f25bee8b925593725fa3071e5fcdc684223e96098de1724c97ef6b6be5`  
		Last Modified: Tue, 24 Dec 2024 22:13:55 GMT  
		Size: 3.9 MB (3914023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcb752c759c824d2617fb5557c713ce38be9b370d64b863ef3553a06ef852f00`  
		Last Modified: Tue, 24 Dec 2024 22:13:55 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.in-toto+json
