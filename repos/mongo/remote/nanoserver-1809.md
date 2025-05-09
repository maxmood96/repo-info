## `mongo:nanoserver-1809`

```console
$ docker pull mongo@sha256:ca8e84b627a16fa0ba4be1210ad321c7c10990f2471a54e576ac7b0a14b4054b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `mongo:nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull mongo@sha256:2eed87560e55be2ef06724209cf3eebe40f5d0eb2bc25a893c9bfbee2bd306f3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **881.5 MB (881536379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27257933f4281590fb9923fdd18dc6085445465d84d84268fd67de362fb07ee4`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Thu, 01 May 2025 23:09:38 GMT
SHELL [cmd /S /C]
# Thu, 01 May 2025 23:09:40 GMT
USER ContainerAdministrator
# Thu, 01 May 2025 23:09:56 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 01 May 2025 23:09:56 GMT
USER ContainerUser
# Thu, 01 May 2025 23:09:58 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Thu, 01 May 2025 23:09:59 GMT
ENV MONGO_VERSION=8.0.9
# Thu, 01 May 2025 23:10:48 GMT
COPY dir:2013d81808dfe3aedec29f0fe3f5cee2f3dde8ce99732a408b9c6918c9a5780a in C:\mongodb 
# Thu, 01 May 2025 23:11:00 GMT
RUN mongod --version
# Thu, 01 May 2025 23:11:01 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 01 May 2025 23:11:01 GMT
EXPOSE 27017
# Thu, 01 May 2025 23:11:02 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c088050258572ba3368f7c965f601239a38adea2b66c45bb62ef4095030b95`  
		Last Modified: Thu, 01 May 2025 23:11:06 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce10dde42931e2c453b6f72cefbb6f067dc89959972540b1dafa51bc3296f823`  
		Last Modified: Thu, 01 May 2025 23:11:06 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0537d561b3542b9ca5acf148a330307fa8e989c2f1463d75dca834ca3a9638`  
		Last Modified: Thu, 01 May 2025 23:11:05 GMT  
		Size: 67.9 KB (67913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8b3b064065ed32c59c210107312aa6a7e91c3fb2f7760377d0d85c59cf240f`  
		Last Modified: Thu, 01 May 2025 23:11:05 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8145362e11fd6829bc597ba71efd5a68d63df395ba755164b845500db75bb09e`  
		Last Modified: Thu, 01 May 2025 23:11:05 GMT  
		Size: 275.1 KB (275149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef06cfe233c34b0d0523f093395dbc16e63b563dec2ce5302fef0a3aaa761f26`  
		Last Modified: Thu, 01 May 2025 23:11:05 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06d1316ba194acce1d026d104c632b3aae1c728954c203b4d3a1d64be723f02`  
		Last Modified: Thu, 01 May 2025 23:12:06 GMT  
		Size: 772.4 MB (772366160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7122cba359a85ea7dea36877369b7807b519f074aae3ae80aea408e23c53c7`  
		Last Modified: Thu, 01 May 2025 23:11:04 GMT  
		Size: 67.6 KB (67634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd315805e343847795e286dd8c02f2e5e16bc33b68e193623cb94c0aba597e61`  
		Last Modified: Thu, 01 May 2025 23:11:04 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a87923c34a7cff2a60f6b3780fecc34c8200a4799e75f605a8d78a223696c3f`  
		Last Modified: Thu, 01 May 2025 23:11:04 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba904ea6154a46b26ed84eaf4f83806f382730e631bb55cb6cfd5869d8607712`  
		Last Modified: Thu, 01 May 2025 23:11:04 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
