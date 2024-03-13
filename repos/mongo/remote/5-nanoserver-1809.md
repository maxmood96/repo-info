## `mongo:5-nanoserver-1809`

```console
$ docker pull mongo@sha256:48c3cbad1b35023cabf310e1e017537903ead5bf60e99d8e84b105922e2e4c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `mongo:5-nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull mongo@sha256:d39f440886c6c461b208453bb890ac688cb3f46bd7c446dfd7299eb29f4f5ba1
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.2 MB (421201662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf02bec8190067e01db7a485fa34ccef6f39572b3497c6dd84cf06bc9923bcdc`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:07:01 GMT
SHELL [cmd /S /C]
# Wed, 13 Mar 2024 02:07:02 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 02:07:05 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 13 Mar 2024 02:07:05 GMT
USER ContainerUser
# Wed, 13 Mar 2024 02:07:07 GMT
COPY multi:c5f0fbe231f542d852dcd0a8e1790eb7694672a9238df11d11d4dd7ca117b6a8 in C:\Windows\System32\ 
# Wed, 13 Mar 2024 02:07:07 GMT
ENV MONGO_VERSION=5.0.25
# Wed, 13 Mar 2024 02:07:30 GMT
COPY dir:95d30a603d2e71c517181ebf96eae248a855a0fc4e8e1503c7f181fcfaf159de in C:\mongodb 
# Wed, 13 Mar 2024 02:07:36 GMT
RUN mongo --version && mongod --version
# Wed, 13 Mar 2024 02:07:37 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Mar 2024 02:07:37 GMT
EXPOSE 27017
# Wed, 13 Mar 2024 02:07:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb0a36bfa9ebb63f925e797796a76fe2bed2f5e2040d6eddc504e4c7ddef48b`  
		Last Modified: Wed, 13 Mar 2024 02:07:46 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d834c091acbe99b43c4e103576a1dbc5ce6e4077ff88319c5fa3f03fea5620a`  
		Last Modified: Wed, 13 Mar 2024 02:07:45 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06724998e2ccd9aacd59c4f90cbd94e5ccd0c120b9584c61c69978bedce245e`  
		Last Modified: Wed, 13 Mar 2024 02:07:44 GMT  
		Size: 71.0 KB (71049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419f67f83ef08f82dd6e75db13476a3389888cd9514b78152372b4609df50641`  
		Last Modified: Wed, 13 Mar 2024 02:07:44 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc35f3205df89fb1b962bc0e1e43e550d205d9f066dadac879ae1674741fe2d6`  
		Last Modified: Wed, 13 Mar 2024 02:07:44 GMT  
		Size: 267.4 KB (267445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61f80df8f42c19257ba220ddb6bc0c7d0a3df7dd213a6f5476369f4ebe3a6b9`  
		Last Modified: Wed, 13 Mar 2024 02:07:44 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c9ac61a74284645f1a215fb6cf1ec701e6dd1187444bd706d75f8dc590d1cc`  
		Last Modified: Wed, 13 Mar 2024 02:08:13 GMT  
		Size: 314.9 MB (314913696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b234c998a049d8e79f6a1b87a06f2d193bcf9bc8589140e1058c8a0bc3c12b`  
		Last Modified: Wed, 13 Mar 2024 02:07:42 GMT  
		Size: 1.3 MB (1322111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512d94d718a967c071b01569cdd64693d12ddd9be3b1ce8d9de7b66211d566e`  
		Last Modified: Wed, 13 Mar 2024 02:07:42 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75143f59786126be76a8ea8bd2017f00b40b39eae36ac51f316123a2c89e8b43`  
		Last Modified: Wed, 13 Mar 2024 02:07:42 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b5817569be970c79d41c89fbc32cf56918bb6aa735f4eecab1c7ff4597a385`  
		Last Modified: Wed, 13 Mar 2024 02:07:42 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
