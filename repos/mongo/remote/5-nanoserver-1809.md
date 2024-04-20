## `mongo:5-nanoserver-1809`

```console
$ docker pull mongo@sha256:2aaabb14dc34984d9ada4a8f66cb0078060376d15adc0b3f12acf69f00f52920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `mongo:5-nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull mongo@sha256:16278e6b68c31d20578f7d5a7e2a13d0019d890bb26d72ab60b6c3cc01f4ac63
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.5 MB (416463582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3093bb48070cd3dee7f61ed6ec26232b74b114da37df162dc85bed45bccc73f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Wed, 10 Apr 2024 01:00:36 GMT
SHELL [cmd /S /C]
# Wed, 10 Apr 2024 01:00:38 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 01:00:40 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 10 Apr 2024 01:00:40 GMT
USER ContainerUser
# Wed, 10 Apr 2024 01:00:42 GMT
COPY multi:c5f0fbe231f542d852dcd0a8e1790eb7694672a9238df11d11d4dd7ca117b6a8 in C:\Windows\System32\ 
# Wed, 10 Apr 2024 01:00:42 GMT
ENV MONGO_VERSION=5.0.26
# Wed, 10 Apr 2024 01:00:58 GMT
COPY dir:c5a2113c049daa407c2563884632bc242bc44a6af608518dbd20ed2fd2c8f561 in C:\mongodb 
# Wed, 10 Apr 2024 01:01:03 GMT
RUN mongo --version && mongod --version
# Wed, 10 Apr 2024 01:01:04 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Apr 2024 01:01:05 GMT
EXPOSE 27017
# Wed, 10 Apr 2024 01:01:06 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd206b40b8fb82360be04c860b4369f74a48fdb605714b15457a0c5d0de82762`  
		Last Modified: Wed, 10 Apr 2024 01:01:11 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5211227c8a280c34e52081fa12573035896b1eccfd47c8077f63992cc14020`  
		Last Modified: Wed, 10 Apr 2024 01:01:11 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fdc77c7f0d691b9449c1f445cc52bf1511b2209482fa1dfd1cf93b14c314fb`  
		Last Modified: Wed, 10 Apr 2024 01:01:10 GMT  
		Size: 74.8 KB (74786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989390ffce547c90660101d3e7808e35382135330f5572e26089295a5313e263`  
		Last Modified: Wed, 10 Apr 2024 01:01:10 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d6f2c230a70f9248f92d7b0e8de72824414a86098f1d46f959ba11e243a299`  
		Last Modified: Wed, 10 Apr 2024 01:01:10 GMT  
		Size: 267.4 KB (267450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce283f58076068d772149823a9ba1059676dbd0e2631a774178662f2b5b3e8e`  
		Last Modified: Wed, 10 Apr 2024 01:01:10 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5504f734188749b2cbb7c9d4abcafc3393e7fcaf184fe97c41f17eb2acbc25d8`  
		Last Modified: Wed, 10 Apr 2024 01:01:39 GMT  
		Size: 311.1 MB (311135557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803ab450fd8c2bea874e292ea3f0f0971404ecbed9286733e3d3b609d25d45d3`  
		Last Modified: Wed, 10 Apr 2024 01:01:09 GMT  
		Size: 89.4 KB (89412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51827385d3ed8d5c442dc59e54b7f9e1dd1530d4e758a9effe8140fd98b79874`  
		Last Modified: Wed, 10 Apr 2024 01:01:09 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f79e2a130ad24f695c01226fa52fcab34cd8d248c90540d7e81313992c9995`  
		Last Modified: Wed, 10 Apr 2024 01:01:09 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1acabad0fc45988fcde07118f71459d167e0df624b81cea391720d06fb805d`  
		Last Modified: Wed, 10 Apr 2024 01:01:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
