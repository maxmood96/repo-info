## `mongo:4-nanoserver-1809`

```console
$ docker pull mongo@sha256:b082405670620da997cab1336905d8d9993f9d9556088cfa0f6b41dfe57f51a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `mongo:4-nanoserver-1809` - windows version 10.0.17763.4131; amd64

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
