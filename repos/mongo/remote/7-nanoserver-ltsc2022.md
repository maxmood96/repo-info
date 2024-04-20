## `mongo:7-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:05d6298d9d141c62b8934ea9ea0be053ce4c0c40cf4d32f47d8389fe5f90d1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `mongo:7-nanoserver-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull mongo@sha256:d60960919c6536906db23f624f23ccaacf2835a0eab4e3c636ea503833f0d9b5
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.0 MB (738019624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368b388aa0f6d6dd1f0b5e6bcd12cb60a03e8c8ec8b1ac722728e38af9ac137f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Wed, 10 Apr 2024 01:02:02 GMT
SHELL [cmd /S /C]
# Wed, 10 Apr 2024 01:02:02 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 01:02:05 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 10 Apr 2024 01:02:06 GMT
USER ContainerUser
# Wed, 10 Apr 2024 01:02:07 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Wed, 10 Apr 2024 01:02:08 GMT
ENV MONGO_VERSION=7.0.8
# Wed, 10 Apr 2024 01:02:35 GMT
COPY dir:4a345f3390b35b1b56d808fec53236340ce99accef71314ef04d72a18e5c5b17 in C:\mongodb 
# Wed, 10 Apr 2024 01:02:47 GMT
RUN mongod --version
# Wed, 10 Apr 2024 01:02:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Apr 2024 01:02:49 GMT
EXPOSE 27017
# Wed, 10 Apr 2024 01:02:49 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c3f2a971fe24288bd87ddd1d24e0a12a3184912acffd84558d526b516aa9a8`  
		Last Modified: Wed, 10 Apr 2024 01:02:57 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcae8eb48ce6a6f4ca53cfc772b9d4cbf365622352b972406de24f6b3ef9e42a`  
		Last Modified: Wed, 10 Apr 2024 01:02:56 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8601ff5a01d800dea393c26265457347d862c6fceb1df7ff2ee5550816d0c1db`  
		Last Modified: Wed, 10 Apr 2024 01:02:55 GMT  
		Size: 75.3 KB (75330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fa835391c57733e39383cd69dac131b7c06f8c4569d246c8022e70d38f7ec1`  
		Last Modified: Wed, 10 Apr 2024 01:02:55 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97698f584b864416701526a78fe39ef4a0173961f46af99f1768b5fc7353473a`  
		Last Modified: Wed, 10 Apr 2024 01:02:55 GMT  
		Size: 267.2 KB (267159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d901cfe15c642daae1bedb583d4ffe2fbcd155a9456a2eca16db26675885b6`  
		Last Modified: Wed, 10 Apr 2024 01:02:54 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeca9f07ffe54e8f622b8a187a5a9d8cc17c2ec689c630276ab5453ea04905f`  
		Last Modified: Wed, 10 Apr 2024 01:03:42 GMT  
		Size: 616.6 MB (616579730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb9fb314f2f09c7d70a7cb6ba0a32930eb1aab4fc52c36b641a735dd66b9762`  
		Last Modified: Wed, 10 Apr 2024 01:02:53 GMT  
		Size: 96.1 KB (96052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788811c614d79353ac738dab378aa3baab0d3d8b43d61a8a5a62b84b00ebe91f`  
		Last Modified: Wed, 10 Apr 2024 01:02:53 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f7494e50633a81451963454dcf361a49258f7900c7f5ecd9c09402f9ac7051`  
		Last Modified: Wed, 10 Apr 2024 01:02:53 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2765e8b29c187a760efb81e578810fb79f7ee37b01ead5f9ed90bc9604a9d3`  
		Last Modified: Wed, 10 Apr 2024 01:02:53 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
