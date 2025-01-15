## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:6eaa77c0e77c611854ee3ea9103ffe71527ec6219b405fea415decd2a21b7947
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
$ docker pull debian@sha256:da641547453ee83a328e36215cc2f377a2cb95f776dcd4d69dd7c39a9aa9054f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53739383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee65466ad0cbc327b4cb1fe964fd43c3e1a9421e72e71a18c67f50051aa92efc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2f17e2ee9135b1d360fc5e64ca989812e125720bce28c28c09337332095a71e3`  
		Last Modified: Tue, 14 Jan 2025 01:33:22 GMT  
		Size: 53.7 MB (53739158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7eb8af3bed3a2e70512c1bd4a4c070ace2a923d01fb1f7f42fe329ed0ba642`  
		Last Modified: Tue, 14 Jan 2025 22:05:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:941de96c5b51b70dfafa5a4d9878240dc147dbceeeb44adecf4372c78b190b9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6785547de95845fa06e750b3797149c159590eb95ba2c6f4eb770239a6ca9b`

```dockerfile
```

-	Layers:
	-	`sha256:d71761a54b3879011ec877b7435901cc0329a44a9478552f7f4eb0f238fa8eff`  
		Last Modified: Tue, 14 Jan 2025 02:15:36 GMT  
		Size: 3.9 MB (3917518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:338d478d0a739c23dbee4dcb480775a30cb9e269f05810969cb2b3b7be0fd3ed`  
		Last Modified: Tue, 14 Jan 2025 02:15:36 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:c37fd2dd368f5efd2a5f85f3bc8510891ad6e4b8942287353491d2c962a83fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49025287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fb62c4b8c98a8255338040e84b536bedf46465984246632bf9fa30cb5acec7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3f18350182a4c7fc977397850f7888add71b67bef94f26475e4f63fac0e058b2`  
		Last Modified: Tue, 14 Jan 2025 22:22:29 GMT  
		Size: 49.0 MB (49025062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb879acc7549316eeacbca8a5eec5b35773b1709221971051198af4f396311e`  
		Last Modified: Tue, 14 Jan 2025 02:17:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d28bed755d8ba8e46583845373c5926712c7ac47a63de2664c3b2517ecf64ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3924985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82dff8ca9389e154d28c6ca0978723a225eb6ddf49146b25599370f2b1a5a52`

```dockerfile
```

-	Layers:
	-	`sha256:05b8e9e6c94f0d980dbdbcd20fcfeb9f1c457a36063d576dd1e9dc2425afe62b`  
		Last Modified: Tue, 14 Jan 2025 02:17:56 GMT  
		Size: 3.9 MB (3919080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:015d59bf14b0f348c3de22983d2bbcd1055e31d8ca5fe77969ad5228669f202b`  
		Last Modified: Tue, 14 Jan 2025 02:17:56 GMT  
		Size: 5.9 KB (5905 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:13636cbff54ba4a08e3926ea95ec2388c24f48a00ef5dfc13d7c22690a82907e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52246282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c8ca8d95373431bc0d4e0ef7611f42469dcd3e18a00e484b0086fad1bdb05e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ba93fbb694f6fb4f1ae7a51edb1c93c52ce1928f6ff5ab4f496ccf03feb66ffb`  
		Last Modified: Tue, 14 Jan 2025 20:36:23 GMT  
		Size: 52.2 MB (52246059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d28304b65c4653ac8ac046a7b53203f911c0ddb77e4d79a7c4f620d154dd2f`  
		Last Modified: Tue, 14 Jan 2025 02:22:51 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1a45c8ee694d07b588b8070c9e9906213cbda2b2e2f3a3b9c8f227e714d22441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4abd66d6177c603ac73ddea20ac8c1f7854fc478762bd91ba7d7f9241f6527`

```dockerfile
```

-	Layers:
	-	`sha256:bf7668fcd3bcaaf417918d0ab23ee3a0a010d681985b74266b0664123ef48efe`  
		Last Modified: Tue, 14 Jan 2025 02:22:51 GMT  
		Size: 3.9 MB (3917098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf7b1ae2c5090d45ac32dcfc3acf9369255ae805b8a67ceb9ed556f9ddba7c8b`  
		Last Modified: Tue, 14 Jan 2025 02:22:51 GMT  
		Size: 5.9 KB (5921 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:2006ebbc9144b38ca52db34e2c1339e388bd08dd51f2c8093a9a43f5f232e559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54676506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf0566b3546d66ef14e7edc358059baa9b7d584002677306d9740a72f0bb986`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:04073b2ecb954970d431e52a302f2e518618791f9ab977b671b817e967542cb0`  
		Last Modified: Tue, 14 Jan 2025 01:33:16 GMT  
		Size: 54.7 MB (54676282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1808fb8a8c827da2fad4855fb824294ca4ea161d5888b5dbfca449a40a7ae44f`  
		Last Modified: Tue, 14 Jan 2025 02:15:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a13be38aa5716b38e005f956c565b09f40a153b32de32f0ea1bc18653004c18f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b19c3b3d594010d0294a961ba2c749f87509c031a6f62699f90553b1cf2e67`

```dockerfile
```

-	Layers:
	-	`sha256:d2a950809dd55adc5050a9b4a55f8ba9381b90762c7a8dc2cc8a8c949d03fe00`  
		Last Modified: Tue, 14 Jan 2025 02:15:47 GMT  
		Size: 3.9 MB (3914025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c147d2a55e710dc3c515ac8a1e5d1a60a743f1e5b2837999c7ead9a62e38b0fd`  
		Last Modified: Tue, 14 Jan 2025 02:15:47 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json
