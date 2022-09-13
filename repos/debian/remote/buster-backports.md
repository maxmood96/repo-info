## `debian:buster-backports`

```console
$ docker pull debian@sha256:8e382a18cea070aa4ffc082ee9fbd0d0ca774cafeb05b32a4e4658e4b854aeee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:19b57f3c28b7bf5881244cac08971c3c68ca9345173efcd10b1afaee40e73bc4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50440597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20db46d819c66f4131ef33f59cddacb0e267bcc1fd6bbecbab928cbd5a1263c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:38 GMT
ADD file:4649a893b2859f2ff51182a13c9c8eeaeaea866161b3f4a1c4f0bb48bc01d007 in / 
# Tue, 13 Sep 2022 00:56:38 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 00:56:42 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:86467c57892b6bb48d563cb5940c68b69c431b2e79c3547df60d1c761c21c156`  
		Last Modified: Tue, 13 Sep 2022 01:00:51 GMT  
		Size: 50.4 MB (50440374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde92056eabda90361e2ba789480d2522d5a66be24614cb17532dec10fbb1352`  
		Last Modified: Tue, 13 Sep 2022 01:01:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:2d94d465d188c23263c1a5725ec93e52ceac700bf91fba8c93b22d873c33347f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45915111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6af3b6b66385dda2eacb2abde86bded79237785f85a9ccf67a9e7f23dc6851`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 03:42:55 GMT
ADD file:28e8fbd48a4aa7f5294aa6046899d5d5cbbd70ba28f7c6d3570d4f92dab36103 in / 
# Tue, 13 Sep 2022 03:42:55 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:43:03 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:03c0a108fceb58ca60977e45057eccb02892db7412dc4da52f05ebeacf68951d`  
		Last Modified: Tue, 13 Sep 2022 03:50:16 GMT  
		Size: 45.9 MB (45914887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626abd6ed2635ad63c86dc7741c8dc4957c409f15eeebc4c0610df632579cb26`  
		Last Modified: Tue, 13 Sep 2022 03:50:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c6bef0c8d2f6140c5762dce7c02c1b7c4ce00b127bba5f2f6a77720c03bb1a07
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49228483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5732b724927a0f90de2431e08f7218d7a5e0811e5f2d96d02aa727b183db7e09`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 02:11:06 GMT
ADD file:304a544562f139d7ab96511b7f1e059966cf90169117e835072f132468bf91c8 in / 
# Tue, 13 Sep 2022 02:11:07 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 02:11:14 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e2406a452ad23ba9085e0708f5e15309206a618eb828aa307becbb239414392f`  
		Last Modified: Tue, 13 Sep 2022 02:16:42 GMT  
		Size: 49.2 MB (49228261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58810989165c468e5c4851931baad1a1dd2ccffda704e5b669af2fa9c872155`  
		Last Modified: Tue, 13 Sep 2022 02:16:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:707ba340508d67249b7e1bf0e181e89ca39c9cccd936f5777695e54c76433657
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51203197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05290ef7828987be180d4ab50fdd49b09ab847bac42f2d918ff2ff879c8e01d5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 01:39:56 GMT
ADD file:abd47beae46939f6ebc8cc566b1f23f170bd1b9318b1ef10dd16ea4209140bd0 in / 
# Tue, 13 Sep 2022 01:39:57 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 01:40:04 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a0702c36e95be838f5e174ceb286969e8527f17111141f2c8a8ecda44d0a14d4`  
		Last Modified: Tue, 13 Sep 2022 01:45:44 GMT  
		Size: 51.2 MB (51202973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73952a9b7f8c569d38f521146ad21be78f0e1280deb27b9a4e115cb4d204cc13`  
		Last Modified: Tue, 13 Sep 2022 01:46:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
