## `mongo:7-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:2ae25e6100bf8a55928257bb06949d65aca261c4419251c7d4c99a949313a472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `mongo:7-nanoserver-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull mongo@sha256:3beb2437953bc1eb91e42baaa74f1e35f06418f4ccd812c9cd329ffb5dc430e7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.8 MB (731808720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a690aec9f5a82854dfeb596f23b8d16c21fb373f6c00731778fcc8b63581ffaa`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:19:12 GMT
SHELL [cmd /S /C]
# Thu, 13 Feb 2025 01:19:12 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:19:15 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 13 Feb 2025 01:19:15 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:19:17 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Thu, 13 Feb 2025 01:19:17 GMT
ENV MONGO_VERSION=7.0.16
# Thu, 13 Feb 2025 01:19:36 GMT
COPY dir:e2287a32285406d829d215fee89db1b9fbd999270c712cc0faadfea5bebebee9 in C:\mongodb 
# Thu, 13 Feb 2025 01:19:55 GMT
RUN mongod --version
# Thu, 13 Feb 2025 01:19:56 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 13 Feb 2025 01:19:57 GMT
EXPOSE 27017
# Thu, 13 Feb 2025 01:19:58 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f432fa88a36b4214c7a6d65e8abea387f9cd0357a64d2dd71f99012d97109444`  
		Last Modified: Thu, 13 Feb 2025 01:20:03 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3501165b1ea4b078cd64163176b606149b18a9e195ac92f4a2404246a765ad60`  
		Last Modified: Thu, 13 Feb 2025 01:20:03 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89238655b2f808c224ff61ef35fee589b0652e5ffed7e3c37cbf0c92285dd2f`  
		Last Modified: Thu, 13 Feb 2025 01:20:01 GMT  
		Size: 77.3 KB (77279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96f5b2636ee0ac1e8b71d4c7aeca8a0adee7249955b5e7a505a442e514164f6`  
		Last Modified: Thu, 13 Feb 2025 01:20:02 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95e3c2119b1b0b8022b128ff28d2d389cef7afce35aca6fc56db047bb985c48`  
		Last Modified: Thu, 13 Feb 2025 01:20:02 GMT  
		Size: 275.2 KB (275159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91da82b25453bc7e447db2fd692f1013094795bc6e0631a3e50a4d95e7990895`  
		Last Modified: Thu, 13 Feb 2025 01:20:02 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26b14c3c294560f360e07d62eb2ec101d8d9b7ac81f12c19bf099e8a55a8f43`  
		Last Modified: Thu, 13 Feb 2025 01:20:47 GMT  
		Size: 610.7 MB (610683466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b68bf47cbc467f053d94adb4cbac2f9072c9010c3d67c92a565b39e4de97dc`  
		Last Modified: Thu, 13 Feb 2025 01:20:00 GMT  
		Size: 99.0 KB (98965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e0c0b4e86be83838f6d97727755a14d8a8968691fde43b3047742204172299`  
		Last Modified: Thu, 13 Feb 2025 01:20:00 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdef46a0195e28166382b33fab4eaa8b9aa0e0ee287a5ba376a2f4a475c8213`  
		Last Modified: Thu, 13 Feb 2025 01:20:00 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f1f67d34a97ee8b64d009a4c917f0c8259dde8423f58012fb4c2d90c9f058c`  
		Last Modified: Thu, 13 Feb 2025 01:20:00 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
