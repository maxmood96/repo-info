## `mongo:6-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:9a7933f4aea1a9d910b728664875dfd298b927161dfb39a3121b72025f2f2ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `mongo:6-nanoserver-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull mongo@sha256:99d75a384311e370653efc29a1215313d392788b5680b65fde4d6b8c6d2bdd0b
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.5 MB (639543647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6cd070924c9e423f965560a4c47525e283e9198c4332bfeb9ff2916f4ca60a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Fri, 19 Jan 2024 00:52:04 GMT
SHELL [cmd /S /C]
# Fri, 19 Jan 2024 00:52:05 GMT
USER ContainerAdministrator
# Fri, 19 Jan 2024 00:52:35 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 19 Jan 2024 00:52:36 GMT
USER ContainerUser
# Fri, 19 Jan 2024 00:52:38 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Fri, 19 Jan 2024 00:52:38 GMT
ENV MONGO_VERSION=6.0.13
# Fri, 19 Jan 2024 00:53:00 GMT
COPY dir:52c8844300bd1267892ff953bada283f10975ec77346ef3bec4c64101fde69fa in C:\mongodb 
# Fri, 19 Jan 2024 00:53:14 GMT
RUN mongod --version
# Fri, 19 Jan 2024 00:53:15 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 19 Jan 2024 00:53:16 GMT
EXPOSE 27017
# Fri, 19 Jan 2024 00:53:16 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:11d5cdc5eaac7bace3ae1ecd3c0df2a27ef5005ab296c56b7f83e24bf25c236c`  
		Last Modified: Tue, 09 Jan 2024 20:57:18 GMT  
		Size: 120.8 MB (120769267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975922d243cb3e3c27332e7aa449ee806913fcbd2c06d5a2182638d40d668ef2`  
		Last Modified: Fri, 19 Jan 2024 00:53:21 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e437e560ceecd609b6d2f2818f95cc8e743d3cee9013bb9e31d744670dc121e`  
		Last Modified: Fri, 19 Jan 2024 00:53:21 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec00f06b062f683df2915f66d63525b2d2ab6bf0426798bb32b9d273bf6f742`  
		Last Modified: Fri, 19 Jan 2024 00:53:21 GMT  
		Size: 104.2 KB (104247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4214e008817d9685409a29d43bd7909a3d3477b05aad971afe0fa79709caf2d`  
		Last Modified: Fri, 19 Jan 2024 00:53:20 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e43ba30f519a9895b5748d271b4087693ad594642ea09552574c1c66674c9b2`  
		Last Modified: Fri, 19 Jan 2024 00:53:20 GMT  
		Size: 267.1 KB (267089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf2d1083e81c7cf9288292f6e66b9c12bf3c45a2bdc3d2be054ba8f61ef7c8f`  
		Last Modified: Fri, 19 Jan 2024 00:53:20 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8570a1824708c698f0615156ddf6768e51ce8688d5bf880e076a2c1f812726`  
		Last Modified: Fri, 19 Jan 2024 00:54:02 GMT  
		Size: 518.3 MB (518294162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f85f4c02ceae76deb5609a1067cfd0eb1f8a09c7c14f190ef0840eb7565d2d`  
		Last Modified: Fri, 19 Jan 2024 00:53:19 GMT  
		Size: 101.6 KB (101578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5e8f1bb2e230fceaa3bd9b8ee14c6616a8c48c549e492d76eff685d826f219`  
		Last Modified: Fri, 19 Jan 2024 00:53:19 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cab4095b7199c3cf4569cdac7a23b7f4d0a3c29f6a7f6ac9190c3413c49e9b`  
		Last Modified: Fri, 19 Jan 2024 00:53:19 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699c06b5981a03720301fb7983a805796ce3548466d8a22910e9f68ae6bd8f69`  
		Last Modified: Fri, 19 Jan 2024 00:53:19 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
