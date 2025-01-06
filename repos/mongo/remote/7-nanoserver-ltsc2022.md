## `mongo:7-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:3f3ea0ce648b07335fd1f6c6663e982aeacd247307440df38b64a9db080e2822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `mongo:7-nanoserver-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull mongo@sha256:efa2ab509db3abf3babcd3e88e0d1f8b98c9e7541578758dfafe4a70e7ebf79d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.7 MB (731729487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba7377fce0a006a132fa5492d59237c34621beb7261666cac8e9b2a281b7bc2`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 05 Dec 2024 01:18:54 GMT
RUN Apply image 10.0.20348.2966
# Mon, 23 Dec 2024 18:08:32 GMT
SHELL [cmd /S /C]
# Mon, 23 Dec 2024 18:08:32 GMT
USER ContainerAdministrator
# Mon, 23 Dec 2024 18:08:46 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Mon, 23 Dec 2024 18:08:46 GMT
USER ContainerUser
# Mon, 23 Dec 2024 18:08:48 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Mon, 23 Dec 2024 18:08:48 GMT
ENV MONGO_VERSION=7.0.16
# Mon, 23 Dec 2024 18:09:09 GMT
COPY dir:e2287a32285406d829d215fee89db1b9fbd999270c712cc0faadfea5bebebee9 in C:\mongodb 
# Mon, 23 Dec 2024 18:09:30 GMT
RUN mongod --version
# Mon, 23 Dec 2024 18:09:30 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 23 Dec 2024 18:09:31 GMT
EXPOSE 27017
# Mon, 23 Dec 2024 18:09:32 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:f9d5d5ca3244fc2c429a892cbe6066394790f649f32d59acfdf012e490896378`  
		Last Modified: Tue, 10 Dec 2024 18:34:17 GMT  
		Size: 120.6 MB (120601318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbfe4644aa9008d89c206390f1e7e1e9c0a719cc215f454dc23fc6f222df7d5`  
		Last Modified: Mon, 23 Dec 2024 18:09:39 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf55d6ab07aeaa73eb9b4e5191b8c1bd20cae90af972700ac56376530c4fd03c`  
		Last Modified: Mon, 23 Dec 2024 18:09:39 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e87d2816884cdbd387006637e238702329e636953ea254cb509c8f61c7d993`  
		Last Modified: Mon, 23 Dec 2024 18:09:38 GMT  
		Size: 77.7 KB (77725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63f0ecc64521b7998304e4bdc765cc0ba1c5480f1a97080f1f175b9a4b11f67`  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04075add1a0454e19250d0b761f8c5d4b18da312e7d287d342024dd79f91916e`  
		Last Modified: Mon, 23 Dec 2024 18:09:38 GMT  
		Size: 275.1 KB (275140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c4686e7c6e09eadd5aa598893703b1fe6565d2b7d380778a081b353b326136`  
		Last Modified: Mon, 23 Dec 2024 18:09:37 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c29791c1b19ac917a5a34a9761d4a7faf0e9e0aba35fd001393a244cbfa59e9`  
		Last Modified: Mon, 23 Dec 2024 18:10:25 GMT  
		Size: 610.7 MB (610683500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bf7bd734b59dc5dd0cfd7bc5c12d5fb908c8e14b7733553408148b5d0807dd`  
		Last Modified: Mon, 23 Dec 2024 18:09:36 GMT  
		Size: 84.4 KB (84389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c47c1fcab2016713bbabe1419fb9858dded4ebaaa7a11a2e50a392d7936765`  
		Last Modified: Mon, 23 Dec 2024 18:09:36 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1be0795ac99a8016d7773b1c2b0165f148bfd0795183ed0458f33b8a6a4843e`  
		Last Modified: Mon, 23 Dec 2024 18:09:36 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed4a6d2721d9a575664fe9194c4e73cbb0ef8247d97fcc25b5419c7e3c3e6ec`  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
