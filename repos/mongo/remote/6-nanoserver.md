## `mongo:6-nanoserver`

```console
$ docker pull mongo@sha256:0cd72fb9bddd3bb24cf12c2c87605095559ae0f17da3ececb38bf91617d57e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `mongo:6-nanoserver` - windows version 10.0.20348.3932; amd64

```console
$ docker pull mongo@sha256:35b89ec312bf26d6b9a57b4876dddfb0cb9b4110152909f36bbfd29d2b9fefb7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.0 MB (648995851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5fb3ff94cffd7b490c009a7042394f4c9b89939516fdb179e3b45c2a04a3ecb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 05 Jul 2025 05:15:23 GMT
RUN Apply image 10.0.20348.3932
# Wed, 09 Jul 2025 19:12:47 GMT
SHELL [cmd /S /C]
# Wed, 09 Jul 2025 19:12:48 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:12:52 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 09 Jul 2025 19:12:53 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:12:54 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 09 Jul 2025 19:12:55 GMT
ENV MONGO_VERSION=6.0.24
# Wed, 09 Jul 2025 19:13:11 GMT
COPY dir:cba4e76c3274759dc0518bf251e036b8561f41ea07b83e09dbbba9a2cc67c594 in C:\mongodb 
# Wed, 09 Jul 2025 19:13:22 GMT
RUN mongod --version
# Wed, 09 Jul 2025 19:13:23 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Jul 2025 19:13:24 GMT
EXPOSE 27017
# Wed, 09 Jul 2025 19:13:25 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:b1cf2c299ff70c52cb8ecf52e66d64d5068519867510919d8807ed2c58a54ba2`  
		Last Modified: Tue, 08 Jul 2025 21:55:51 GMT  
		Size: 122.6 MB (122630906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47393bdf99bb6d25b512dc046f518c545c5ed91119ec02ee36987231560923c`  
		Last Modified: Wed, 09 Jul 2025 19:14:24 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d122348cd5b726dba7abb2e0d88599677f261fa84709495208addb725e31e156`  
		Last Modified: Wed, 09 Jul 2025 19:14:24 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1721b606cf9bf31fff444f94da8279696d189ee0cd63d915fd34d07ffbe9ae24`  
		Last Modified: Wed, 09 Jul 2025 19:14:24 GMT  
		Size: 78.0 KB (78050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006c8c59a7f211534357a24b68faaf2df2680c0f560912c0d951e616ae65b69d`  
		Last Modified: Wed, 09 Jul 2025 19:14:25 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e410a76a3c0eaeb8833e28d58481f755be427fb81eb1476b7d6df8cb73639fc6`  
		Last Modified: Wed, 09 Jul 2025 19:14:25 GMT  
		Size: 275.2 KB (275152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ce016ce924fee410aa38b99847c6de2aa952133ca554b8b099e4f0c08b0f4d`  
		Last Modified: Wed, 09 Jul 2025 19:14:24 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277077a3a378e204ee251a954f38869e2d2e7f98a8e13c205054f109e46f8fe9`  
		Last Modified: Wed, 09 Jul 2025 22:08:07 GMT  
		Size: 525.9 MB (525908246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d34853824c5432ff2e0e130f00404f587aae9edb7d810dfc3a15cb179e2cb70`  
		Last Modified: Wed, 09 Jul 2025 19:14:25 GMT  
		Size: 96.3 KB (96286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96b37338bacb75e11d82a6032314f9374733f6f0656e875164fa5eb38d951e2`  
		Last Modified: Wed, 09 Jul 2025 19:14:24 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2869a470fca7ca8bfaefdd1919d896f1eb1b8e0c5c58c2883c0190e348506da`  
		Last Modified: Wed, 09 Jul 2025 19:14:24 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb9fc34b7353efe88c5d3204461fc83de09a7b0594a6ee6a3bfef6dc89aac6f`  
		Last Modified: Wed, 09 Jul 2025 19:14:24 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
