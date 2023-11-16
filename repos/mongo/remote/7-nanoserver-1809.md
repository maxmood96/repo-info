## `mongo:7-nanoserver-1809`

```console
$ docker pull mongo@sha256:d9b163f52a3b73d6c479c31057abe4eb10867a48b49d84822143a66d4422d175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `mongo:7-nanoserver-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull mongo@sha256:f1913853456997909c4ebc97670933f11abff9b174628894f162236e91c5a215
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.1 MB (716131565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8945076369ae6230163ed32f693aede6dd3c385dce87bbe36dbcd139f2bd460d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 02:55:52 GMT
SHELL [cmd /S /C]
# Thu, 16 Nov 2023 03:26:22 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 03:26:36 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 16 Nov 2023 03:26:36 GMT
USER ContainerUser
# Thu, 16 Nov 2023 03:26:38 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Thu, 16 Nov 2023 03:35:36 GMT
ENV MONGO_VERSION=7.0.3
# Thu, 16 Nov 2023 03:36:22 GMT
COPY dir:7eb07008f9caa03d65261324d8b15c9bab0915a192363e36e5cb23930a2b52b0 in C:\mongodb 
# Thu, 16 Nov 2023 03:36:39 GMT
RUN mongod --version
# Thu, 16 Nov 2023 03:36:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Nov 2023 03:36:40 GMT
EXPOSE 27017
# Thu, 16 Nov 2023 03:36:41 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26eb16ff47ed3c1f3ff64a9920a3407afa035ee398f803b948326dc0e5e4e79e`  
		Last Modified: Thu, 16 Nov 2023 03:13:07 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e02f563a12fbc6846cdd83dd195b52331a6b956d0cadd546aac9d48eafc857c`  
		Last Modified: Thu, 16 Nov 2023 04:24:41 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a67c125c9a773e11ea7d5d4837aab6edb57a3542f5d40eb33917ff54a1764254`  
		Last Modified: Thu, 16 Nov 2023 04:24:39 GMT  
		Size: 68.4 KB (68440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ebb2a529df887c3f03501c0eb37994d3377f525a469a8ec60551d78b6fa67f`  
		Last Modified: Thu, 16 Nov 2023 04:24:38 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2905c85cc48fe93de24f2a5618ed89750c5358332209fa4292ecbd5215833e11`  
		Last Modified: Thu, 16 Nov 2023 04:24:39 GMT  
		Size: 267.2 KB (267195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef1e5f846a6b350097dd83b5b0aad7f14a126efd88bc094474c09370b30cc13`  
		Last Modified: Thu, 16 Nov 2023 04:31:44 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fafae1c3e71c4a3eb95507d28a9b2fd29baf52e285de72f82349a52e126909`  
		Last Modified: Thu, 16 Nov 2023 04:33:14 GMT  
		Size: 611.2 MB (611209900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb4408a9937d50b6dc05897a1eb23ecd50ae5091942a08b5d7ae197546399c4`  
		Last Modified: Thu, 16 Nov 2023 04:31:42 GMT  
		Size: 80.5 KB (80505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c739d86038b74bbaede3bb634b116d3c88a22d19ba0754f1434504c4791720d2`  
		Last Modified: Thu, 16 Nov 2023 04:31:42 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455dba42cac15b042e822d3259754c3920e15a9eebe554d9d766ad24fcf6b816`  
		Last Modified: Thu, 16 Nov 2023 04:31:42 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27901b74a424a4467e409e0fe1292552a45e85b356f0b958e4cc78a0c50f234`  
		Last Modified: Thu, 16 Nov 2023 04:31:42 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
