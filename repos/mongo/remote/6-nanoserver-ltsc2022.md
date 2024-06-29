## `mongo:6-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:0c720cbcdb658020b03a821e97920c94ae9e904d1575a8f5af64d4af4aa6a192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `mongo:6-nanoserver-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull mongo@sha256:edd5de7a47ca85ca3b79bb3ce46cd3bc1f95e8b30f86b0ed353d97451004ed26
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.0 MB (644002254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abef89a687cf9312b713e3bd31faca0b56b8e4a7cfa81cb7ba34a07eda68787e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 19 Jun 2024 19:27:30 GMT
RUN Apply image 10.0.20348.2529
# Sat, 29 Jun 2024 00:50:46 GMT
SHELL [cmd /S /C]
# Sat, 29 Jun 2024 00:50:46 GMT
USER ContainerAdministrator
# Sat, 29 Jun 2024 00:51:11 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 29 Jun 2024 00:51:12 GMT
USER ContainerUser
# Sat, 29 Jun 2024 00:51:13 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Sat, 29 Jun 2024 00:51:14 GMT
ENV MONGO_VERSION=6.0.16
# Sat, 29 Jun 2024 00:51:33 GMT
COPY dir:6f4af2768a9f782f0ee6ba32759515874004eaed990f1ac643f6b3295b8b75af in C:\mongodb 
# Sat, 29 Jun 2024 00:51:47 GMT
RUN mongod --version
# Sat, 29 Jun 2024 00:51:47 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 29 Jun 2024 00:51:48 GMT
EXPOSE 27017
# Sat, 29 Jun 2024 00:51:48 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a8c295c425a912de308ded279124ae45fec44d55a451843fe5877155417f453c`  
		Last Modified: Fri, 21 Jun 2024 02:24:34 GMT  
		Size: 120.5 MB (120499549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c331f39de145d18599841bc43208c07d679753b3adcc462840e4c3f83974e7`  
		Last Modified: Sat, 29 Jun 2024 00:51:52 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bd70f26801d18dd77fb9f8054cd569f9605171497f726a1b0185ad05cdcc19`  
		Last Modified: Sat, 29 Jun 2024 00:51:52 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0b2a3f318d7653d1bab1a492df747f919fe4f5be207d288ddb06f027759c92`  
		Last Modified: Sat, 29 Jun 2024 00:51:52 GMT  
		Size: 88.8 KB (88750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c580f6cc56fc4363f25260bef55241019dea02c73c0aaa5e7c1156e163c9df`  
		Last Modified: Sat, 29 Jun 2024 00:51:52 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af785d3c44405613b3f286bae8d5b601906925317485702a258e8dce1e45081f`  
		Last Modified: Sat, 29 Jun 2024 00:51:52 GMT  
		Size: 275.2 KB (275159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5977ab174455a5e95767becaf80039158457dc09f09c5bc0b633149e0f966b8`  
		Last Modified: Sat, 29 Jun 2024 00:51:52 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7bd558d9a513d8567fc3c2dc0f53ef8765180953a9a4f88f252f6459777bba5`  
		Last Modified: Sat, 29 Jun 2024 00:52:33 GMT  
		Size: 523.0 MB (523038500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e8301d8c2fe203e29562de58143da0557048aecc555d381ab679e318a4413f`  
		Last Modified: Sat, 29 Jun 2024 00:51:51 GMT  
		Size: 93.1 KB (93089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44eb3ab035f7a0da634d760243610e5a4dd3179bd3f628f0e7801cd96b3c3616`  
		Last Modified: Sat, 29 Jun 2024 00:51:51 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283c59301b9a7b1914f85ee536823ffe0299b9186ef8e01f2f83a2728350ca93`  
		Last Modified: Sat, 29 Jun 2024 00:51:51 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc7cc9308919b522168c4515ea5b5539802eeececf03509924c3b43ab83ac3f`  
		Last Modified: Sat, 29 Jun 2024 00:51:51 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
