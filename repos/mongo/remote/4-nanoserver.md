## `mongo:4-nanoserver`

```console
$ docker pull mongo@sha256:0c4df34968d3766613719f82fc3441af9b3407417f47acec38e325817254efcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1607; amd64
	-	windows version 10.0.17763.4131; amd64

### `mongo:4-nanoserver` - windows version 10.0.20348.1607; amd64

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

### `mongo:4-nanoserver` - windows version 10.0.17763.4131; amd64

```console
$ docker pull mongo@sha256:8f62f7b29095d3a23c73a1e2b9669228aaa8fbbc3342e0176376f9ae32b9e950
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351629781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a916da4ebc3f2808f64036878d491b05a17b8091a0011d7831b4541eae3539a`
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
# Thu, 16 Mar 2023 03:19:02 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Thu, 16 Mar 2023 03:28:47 GMT
ENV MONGO_VERSION=4.4.19
# Thu, 16 Mar 2023 03:29:15 GMT
COPY dir:3f48adb7f7619e85ce25694a6fca8d00c40e20a6b52409c21f5809d88aff497a in C:\mongodb 
# Thu, 16 Mar 2023 03:29:51 GMT
RUN mongo --version && mongod --version
# Thu, 16 Mar 2023 03:29:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Mar 2023 03:29:53 GMT
EXPOSE 27017
# Thu, 16 Mar 2023 03:29:54 GMT
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
	-	`sha256:d627e884652ce7cc34439052c446c4167e28e502301e59a05a1f97f41eee4110`  
		Last Modified: Thu, 16 Mar 2023 03:53:09 GMT  
		Size: 263.4 KB (263397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0f29f9c1b73a82358b235baccdc36f4b0b18c655ab33fab837052a50690906`  
		Last Modified: Thu, 16 Mar 2023 03:57:35 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf0129497dd4871db30f3b85219483b9177edbba6637e79ac03ff9de7f59c73`  
		Last Modified: Thu, 16 Mar 2023 03:58:23 GMT  
		Size: 244.5 MB (244521785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9018cb5bb7572463e78bd5af69b9daa3bb0cef1327da6e732a8eadda554818e6`  
		Last Modified: Thu, 16 Mar 2023 03:57:33 GMT  
		Size: 82.8 KB (82770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad43b09daa2b2dadc6b660fc8a327612f222fd82d66f48d5cba01bd07a2cc3e`  
		Last Modified: Thu, 16 Mar 2023 03:57:33 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd57d00a9d89456624b65f04021add23729e882da07d08091cbc40c463f5a52`  
		Last Modified: Thu, 16 Mar 2023 03:57:33 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd278d1bbb96931cc684d61ddad578406b360402285166563b95df8fba423f8`  
		Last Modified: Thu, 16 Mar 2023 03:57:33 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
