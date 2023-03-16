## `mongo:nanoserver-1809`

```console
$ docker pull mongo@sha256:c9a9d363f06ca7cc277b324ad225c2812db746d76fa5d229ba16a35fd9e67651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `mongo:nanoserver-1809` - windows version 10.0.17763.4131; amd64

```console
$ docker pull mongo@sha256:bd6d5984057dc2db79f7e0bbd2e430fdb91f4ac70be2ffcbe1571df2c3697ed3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.4 MB (621407935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4212ba00f7858bbae242e2821777d2889338a3243ea50c28f6b3bd7a484a43e2`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 02:20:46 GMT
SHELL [cmd /S /C]
# Thu, 16 Mar 2023 03:07:20 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 03:08:00 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 16 Mar 2023 03:08:01 GMT
USER ContainerUser
# Thu, 16 Mar 2023 03:08:03 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Thu, 16 Mar 2023 03:08:04 GMT
ENV MONGO_VERSION=6.0.5
# Thu, 16 Mar 2023 03:08:58 GMT
COPY dir:8cafabdc84824168ccb42f1fb38dd461d1f5833e45f22346735df9067c52e6a6 in C:\mongodb 
# Thu, 16 Mar 2023 03:09:38 GMT
RUN mongod --version
# Thu, 16 Mar 2023 03:09:39 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Mar 2023 03:09:40 GMT
EXPOSE 27017
# Thu, 16 Mar 2023 03:09:41 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5cc414fce78380e134ec2315d713a8a9040bff5d1298887a2a68029cfc0922`  
		Last Modified: Thu, 16 Mar 2023 02:48:05 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1a233254ba5f14e1070a15977726a5b4df112b5b0262b272ea76a367494e42`  
		Last Modified: Thu, 16 Mar 2023 03:47:51 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3263ac1a13295ff69bbe88e22f0e3624eaac310642d5dcc0a5236ef526d1d4bd`  
		Last Modified: Thu, 16 Mar 2023 03:47:49 GMT  
		Size: 69.4 KB (69440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e43090cb5cef65a97ac19c1867ef724287872689f8abc9c92bdddefa56ea21`  
		Last Modified: Thu, 16 Mar 2023 03:47:49 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79618e6e28cf559aa0f46b783b88faf8a009eba9d183481cf43004bc8681b780`  
		Last Modified: Thu, 16 Mar 2023 03:47:49 GMT  
		Size: 267.2 KB (267170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d99d10c40b1abbe5ed4da1aa8100deb3f8ea7c0fa83a69797e2fea2d6ffb83`  
		Last Modified: Thu, 16 Mar 2023 03:47:49 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e919d156e282734169a5d08897fab6bca42c28f5c146a2d984e0755bcf004089`  
		Last Modified: Thu, 16 Mar 2023 03:49:14 GMT  
		Size: 514.3 MB (514297465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23b2de5f15c2a2ca153dbbc3d5370aeacb5be328f4163ba8ce9e6c1d5149264`  
		Last Modified: Thu, 16 Mar 2023 03:47:47 GMT  
		Size: 81.5 KB (81489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf63f6732172caee786d581ae554521e81ff0599de88a675b64a21f9bf41d241`  
		Last Modified: Thu, 16 Mar 2023 03:47:47 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e7f1180f49b761101e4f2c7a2475ec4e8e4b32166cb0208bce56efeeccc605`  
		Last Modified: Thu, 16 Mar 2023 03:47:47 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd901e00e1a4b0e4327cab4e16369118218a81cb9d008957fc5d0fac98f9cca`  
		Last Modified: Thu, 16 Mar 2023 03:47:47 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
