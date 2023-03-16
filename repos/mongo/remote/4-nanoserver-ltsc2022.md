## `mongo:4-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:cf8619a693641070d57f9fd6af455f31eac168b657c59b9b18eb18fdced38342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1607; amd64

### `mongo:4-nanoserver-ltsc2022` - windows version 10.0.20348.1607; amd64

```console
$ docker pull mongo@sha256:d1b243c27faf16a436a364bb5b992fd43f78e284b5a95c54f036a7bbfbc81bac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.1 MB (367102697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f4bf32f0e5d4254c65ff62bb456e3fc66ff706eb9f6ac5029118469ea65ba5`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 10 Mar 2023 06:31:34 GMT
RUN Apply image 10.0.20348.1607
# Thu, 16 Mar 2023 02:15:36 GMT
SHELL [cmd /S /C]
# Thu, 16 Mar 2023 03:04:16 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 03:05:08 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 16 Mar 2023 03:05:08 GMT
USER ContainerUser
# Thu, 16 Mar 2023 03:17:16 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Thu, 16 Mar 2023 03:27:17 GMT
ENV MONGO_VERSION=4.4.19
# Thu, 16 Mar 2023 03:27:43 GMT
COPY dir:3f48adb7f7619e85ce25694a6fca8d00c40e20a6b52409c21f5809d88aff497a in C:\mongodb 
# Thu, 16 Mar 2023 03:28:28 GMT
RUN mongo --version && mongod --version
# Thu, 16 Mar 2023 03:28:29 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Mar 2023 03:28:30 GMT
EXPOSE 27017
# Thu, 16 Mar 2023 03:28:31 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7abf0a70d48bf65f3d985f5780d4bdaece36f1f4bb8be10d5a6aacce33dacc75`  
		Last Modified: Thu, 16 Mar 2023 01:54:24 GMT  
		Size: 122.2 MB (122171731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa68b8cf98c4e81d0a56e6860ff5347ca921b2991f0fca1a397b892e862ec97`  
		Last Modified: Thu, 16 Mar 2023 02:47:12 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38818021eafe80428d533486402f82f6a153761f59981c81574a3e0c2408dc5`  
		Last Modified: Thu, 16 Mar 2023 03:46:07 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65de860560f9b0e2f325b55686740703531054e4be4a3e58f40d88e3d9e969b`  
		Last Modified: Thu, 16 Mar 2023 03:46:05 GMT  
		Size: 84.6 KB (84635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7402b3f8ba1353ed1a390bc558b163d5c7f7c70f9889ab381b34e82d05cc0e9c`  
		Last Modified: Thu, 16 Mar 2023 03:46:05 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74d41f41e06a86d9900047685f97aca38309bc334a853ef39c6d49dd50321af`  
		Last Modified: Thu, 16 Mar 2023 03:51:56 GMT  
		Size: 263.4 KB (263383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fafb0915f17625c9e1cdb5ddaf94ae502a7b013e271fa4d0eb6d3e7d7a9373`  
		Last Modified: Thu, 16 Mar 2023 03:56:32 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abdaf8ceb6711d1d3f63da1544fc1f08c4e796aad7c06fefb1fd0d6e1b872de`  
		Last Modified: Thu, 16 Mar 2023 03:57:21 GMT  
		Size: 244.5 MB (244521692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfabb2aceef5296558c2a9fb2f6ee6b66151953f4d64a3e0fd2edf5678179323`  
		Last Modified: Thu, 16 Mar 2023 03:56:30 GMT  
		Size: 53.2 KB (53192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982a367adb05f9361cab8372e926717f394844ebd2cd70408e7fdfd57006a3bd`  
		Last Modified: Thu, 16 Mar 2023 03:56:29 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afaba47e729beccd0b46e0c5fe320e3f5d1204681d5606e48166bf782167a04`  
		Last Modified: Thu, 16 Mar 2023 03:56:30 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61097fedbfa8386a841b761fc2e2b5d7636ef46ceecaf313109e1fb9bc1359bd`  
		Last Modified: Thu, 16 Mar 2023 03:56:30 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
