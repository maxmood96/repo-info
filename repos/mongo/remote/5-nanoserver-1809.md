## `mongo:5-nanoserver-1809`

```console
$ docker pull mongo@sha256:ec3d8144c12cc4187923d6e47bab990dd6d6fb996d0349cf27dea7b3ac05e6eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `mongo:5-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull mongo@sha256:120c2d8b4c277d10e02bd4422aeb0b4f9c2d6e3a800962b4863b9637c8f9cb22
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.8 MB (417817279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa52640b138fcba96dbf6499e28eda430b1b5312b050b2eedbcdc562f600775`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:58:29 GMT
SHELL [cmd /S /C]
# Thu, 11 Jan 2024 00:58:30 GMT
USER ContainerAdministrator
# Thu, 11 Jan 2024 00:58:32 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 11 Jan 2024 00:58:33 GMT
USER ContainerUser
# Thu, 11 Jan 2024 00:58:34 GMT
COPY multi:d83167ee7f0a01f519841410f1f031c3bdfa566af08cc1936efaf3b3f20e2b0f in C:\Windows\System32\ 
# Thu, 11 Jan 2024 00:58:35 GMT
ENV MONGO_VERSION=5.0.23
# Thu, 11 Jan 2024 00:59:04 GMT
COPY dir:2659c84e3b8fc52d2b276105c78a0f2d3093204246f7c91798b9f2aabebcfb2d in C:\mongodb 
# Thu, 11 Jan 2024 00:59:06 GMT
RUN mongo --version && mongod --version
# Thu, 11 Jan 2024 00:59:06 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jan 2024 00:59:07 GMT
EXPOSE 27017
# Thu, 11 Jan 2024 00:59:08 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae8c7a0a665bba98f9ddf6c18136efeca55f38d3af5786b2c428238c250675b`  
		Last Modified: Thu, 11 Jan 2024 00:59:12 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf46c898ce7eb52bcc223b83f003d511aa45ac406c8734741e760dda766d1347`  
		Last Modified: Thu, 11 Jan 2024 00:59:12 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d666c018d277b70fae214b52eda9f612a24789e73f8364738211879025ddc3b`  
		Last Modified: Thu, 11 Jan 2024 00:59:11 GMT  
		Size: 71.1 KB (71121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d512f3a567b59e12803a6c24ebbb92f0ef4c4e48df8979c247ba5042787fdb`  
		Last Modified: Thu, 11 Jan 2024 00:59:11 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd91eef770abd668254123f78a6447abf84679afe83a9ebef310e60f6b62b26`  
		Last Modified: Thu, 11 Jan 2024 00:59:11 GMT  
		Size: 263.4 KB (263383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95b45547f5571d63cbe89f68dca86fb42733451c8695486014f6480374116ca`  
		Last Modified: Thu, 11 Jan 2024 00:59:11 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41bcc598538464eabee607546ad1f375a30bbbae06af33ca57f2aa725f3c448`  
		Last Modified: Thu, 11 Jan 2024 00:59:40 GMT  
		Size: 312.8 MB (312794173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c8587acb781c8ee9c3af4ce9b9f024736c927b1c124bf4e61b4730beb0d567`  
		Last Modified: Thu, 11 Jan 2024 00:59:10 GMT  
		Size: 90.1 KB (90099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a2f3d57be59b8d86ce9f1679f913334f59bd9c666a8fc295d144f692dbabff`  
		Last Modified: Thu, 11 Jan 2024 00:59:10 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114d72598fa2a5e4e37d6336c56f30e092e13a5c6d62adb44230a7b2185d0f45`  
		Last Modified: Thu, 11 Jan 2024 00:59:10 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190a544be9001589e880aaa00d637d1676fa04fc14bcac934cafe3e1609fbadd`  
		Last Modified: Thu, 11 Jan 2024 00:59:10 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
