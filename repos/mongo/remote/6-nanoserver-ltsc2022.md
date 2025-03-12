## `mongo:6-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:a02a40729782143d7f785fd79b4e2d70e414e04d8f0b7e819902baf38a13c8fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `mongo:6-nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull mongo@sha256:0963581f77642ebfd166282d2ccc7444d8acca3364ee22756452024eb895cb09
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.1 MB (647076034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2554453b72fe0173eba1ae9b839f50bf22e19ebd222f26ff8e7ae078434ead9e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 20:16:56 GMT
SHELL [cmd /S /C]
# Wed, 12 Mar 2025 20:16:57 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 20:17:00 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 12 Mar 2025 20:17:00 GMT
USER ContainerUser
# Wed, 12 Mar 2025 20:17:01 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 12 Mar 2025 20:17:02 GMT
ENV MONGO_VERSION=6.0.20
# Wed, 12 Mar 2025 20:17:20 GMT
COPY dir:c42938a835e62388cb112585ef444a3c80db492841d999b4012ee48981a81e59 in C:\mongodb 
# Wed, 12 Mar 2025 20:17:33 GMT
RUN mongod --version
# Wed, 12 Mar 2025 20:17:34 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Mar 2025 20:17:35 GMT
EXPOSE 27017
# Wed, 12 Mar 2025 20:17:36 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ea37dd80144c6f7677723a7512d0b5c7e9a01da920ce29af4cd4b5bab1d548`  
		Last Modified: Wed, 12 Mar 2025 20:17:44 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b5bea14c0c27e500937e0b1cc4fed2f2f34819f028436b440f3b53a9a61ca4`  
		Last Modified: Wed, 12 Mar 2025 20:17:43 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd7564993ef56fa0b207298bab9079b8a80e843095cf7f3794099baa02b6345`  
		Last Modified: Wed, 12 Mar 2025 20:17:42 GMT  
		Size: 75.8 KB (75807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8cc57bb02d2bf135f642ffb751653475d97048428173ecd4766cf8f20161c3`  
		Last Modified: Wed, 12 Mar 2025 20:17:42 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646d96b4a087b8312d00300a1f3c1ce8b0b920efc5e7a94c76fdf9bb8ce85c6d`  
		Last Modified: Wed, 12 Mar 2025 20:17:42 GMT  
		Size: 275.2 KB (275158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f092a1aaf8f59f22b971d4ee2576d8800cdfa64efbece6191e836541d3f0b920`  
		Last Modified: Wed, 12 Mar 2025 20:17:41 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f560017b770fc9221748f32914e943eeaf470af13bef2a72ae158158c40d54`  
		Last Modified: Wed, 12 Mar 2025 20:18:21 GMT  
		Size: 525.9 MB (525926711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07efdcdc2e6710146eeeaf6e192179e25593e167c6f50b1d7201b936f915eb1`  
		Last Modified: Wed, 12 Mar 2025 20:17:40 GMT  
		Size: 95.6 KB (95599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8792ab91210d9f492291cd12bf7ed4a76eb5226b496d71324f66efc69a9f6f`  
		Last Modified: Wed, 12 Mar 2025 20:17:40 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12bff11ff9a0535324470284fb0861005d54f977a4fa71c2b032a4bb6b4e103`  
		Last Modified: Wed, 12 Mar 2025 20:17:40 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c774edd85bf3395cedf8b257fb6dda37f534c1d58587ce93624ba72cf67cc4c2`  
		Last Modified: Wed, 12 Mar 2025 20:17:40 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
