## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:d25a2810dc741fb4e6889d5c73a64d71be4e0310064dbf6c79fdce30bcd957f9
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:704698a024f9899a66912596f4bd8d38019b788ca7d25372f97fb02e68875b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53755045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d45e925e6d55f1b929d054f3dc21635869c26dd2c7d320a8302ac3bed961c28`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a84cd87e5aba123271aeaf81ab0b9ea33c2b6a414776af8d01450ff6da5e38a9`  
		Last Modified: Tue, 01 Jul 2025 01:14:48 GMT  
		Size: 53.8 MB (53754820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba65660cca29c2b791a9dfd13620f5e27078498f7dc441c543569181334b068f`  
		Last Modified: Tue, 01 Jul 2025 02:12:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5ddac947983bd50424a64dc8754973bf201b90d4176b0c0fc6f90b414197ebb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4030156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82fcbe02d1680a43a246934636cd1786179106bdeefabc65c04758934da57ec`

```dockerfile
```

-	Layers:
	-	`sha256:7d4450d8553444b3c556addfd4124ddf8ffd61057fad04f8f442d13b59b1c232`  
		Last Modified: Tue, 01 Jul 2025 06:24:06 GMT  
		Size: 4.0 MB (4024303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81054747fe999b448cfa448757c2468c17a70814f8b12775ebb8e0b87c83d080`  
		Last Modified: Tue, 01 Jul 2025 06:24:07 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:133b8a4546889ee0e674c265ec741fe932261d18c379da0914f786d563fd4398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49044183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f03a423fd0954b1f04de1307af4690f2dd2c161f63c3a85bec6a6c8497c4a75`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:eb1b44127d1e0d27f757751db0380a5f7436e974eccd722e7a1c39b83fec10fb`  
		Last Modified: Tue, 01 Jul 2025 01:15:48 GMT  
		Size: 49.0 MB (49043959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51237059759dd4e00c09a8c5fe98ce2f5bd102dc5ef52509d440a176c2c0253`  
		Last Modified: Tue, 01 Jul 2025 02:12:54 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:246c5177a1fce0c0b211b56f7d5a246449b34b6811f28cecf125ada8d4c7fba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2325ad8ffb413607ca4053842987ab98df251560c3773146dbf6e842e1d3d4f1`

```dockerfile
```

-	Layers:
	-	`sha256:51cc8284087354958dc8e6e06248ececbced3c5b40b6e3834fe85847e1202ccd`  
		Last Modified: Tue, 01 Jul 2025 03:25:49 GMT  
		Size: 4.0 MB (4025865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5d02f08acc0bc2f30f9869c787eda2041e51e6364a5eb4f8dffc072c5e53ca9`  
		Last Modified: Tue, 01 Jul 2025 03:25:50 GMT  
		Size: 5.9 KB (5905 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:023fa510e2979366e1c83b27cca34dd33ef8e2069e78bf620095098a208e96e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52252479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff320b48a368fb793a191365a58f1e44dcc858064e437b31cc7b1b97f66a4ff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6c6aa54391cf0ff1eab3978db38a7d687bbcbaa42e8a7f57087f011dafd742dc`  
		Last Modified: Tue, 01 Jul 2025 01:15:58 GMT  
		Size: 52.3 MB (52252255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21df08bb908d89b4efdd097985455098a780c1860e502076d3fb19da28c7be12`  
		Last Modified: Tue, 01 Jul 2025 02:12:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:57e72460a73e302f6a487d4c9512354c268c8045962cc3ebdcdf99f458e38d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4029803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a77d2957b283e3d2f331d10958aebe639671ab88f9d90e1cd1e3a7811a228ba`

```dockerfile
```

-	Layers:
	-	`sha256:cc2b787154f2f7fe41f6bb91568279a08ae82cd241684078a788f8c922a8d151`  
		Last Modified: Tue, 01 Jul 2025 03:25:54 GMT  
		Size: 4.0 MB (4023883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aed4866746adc72b600f4b12bf70d6b6203361ae6a7594db1dff07ad074c282c`  
		Last Modified: Tue, 01 Jul 2025 03:25:55 GMT  
		Size: 5.9 KB (5920 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:6b33a2628693c56642ac9f1139d4eed4252f5fc0c2b399f5c2c356f1c567883b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54690149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf027d56fb65ec842c8e2eb4e623bd5eed4ef873f1beb9905dacc85c3475041`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4caf33a126d214f74fcc2c924e937e11d8d12faa5288e6db912b2af5e2dcae76`  
		Last Modified: Tue, 01 Jul 2025 01:14:57 GMT  
		Size: 54.7 MB (54689926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f4f50aee75eb714133c369708077074acd38a5c9d1bc0ea7b68b254ff91c1c`  
		Last Modified: Tue, 01 Jul 2025 02:12:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b82a0215a2775ce79b26b7976688ccc077e5e5f308feef0a19af686373f884f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4026693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704e63399850b6526aeb69a6cc3b42bb2f33597780effca91c5d97623ce84001`

```dockerfile
```

-	Layers:
	-	`sha256:d8ed63d938bf0384e7ebf9289eaec6991e246d71e45d6ec09b60cec5774bc168`  
		Last Modified: Tue, 01 Jul 2025 03:25:59 GMT  
		Size: 4.0 MB (4020857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed4d10be01a7cf5b431a2603fc8db2423cdfa8d6df3da507b3a51e6c96268867`  
		Last Modified: Tue, 01 Jul 2025 03:26:00 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json
