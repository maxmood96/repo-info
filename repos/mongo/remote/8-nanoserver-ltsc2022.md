## `mongo:8-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:3b74e52a446a4cf4b83df07299a4624c04d9c9b8f5e0f8709136d3a8e81e7906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `mongo:8-nanoserver-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull mongo@sha256:6abac777d681eb002b436fa791b381cf17a6a1245c67f97c2764060301a41a4c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **906.3 MB (906310485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c471e6276542958bf27696da52ff8de5e60f36b0a957eacc71cc0fa4cee823`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Oct 2025 07:34:08 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 21:13:53 GMT
SHELL [cmd /S /C]
# Tue, 14 Oct 2025 21:13:53 GMT
USER ContainerAdministrator
# Tue, 14 Oct 2025 21:13:55 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 14 Oct 2025 21:13:56 GMT
USER ContainerUser
# Tue, 14 Oct 2025 21:13:57 GMT
COPY multi:540d6dd70b1e7484f1958dc08b337aeb56cf8a92fe38be4c279dd406990d6935 in C:\Windows\System32\ 
# Tue, 14 Oct 2025 21:13:57 GMT
ENV MONGO_VERSION=8.0.15
# Tue, 14 Oct 2025 21:14:38 GMT
COPY dir:89b20cfef212bf62f3fb0088593a9d18ace7d3301ef41ba939226bd62ac05cd1 in C:\mongodb 
# Tue, 14 Oct 2025 21:15:07 GMT
RUN mongod --version
# Tue, 14 Oct 2025 21:15:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 14 Oct 2025 21:15:08 GMT
EXPOSE 27017
# Tue, 14 Oct 2025 21:15:08 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:f68a3bbf3ee20b515c5b8b801e5627a9dac3782ef264e37060c34ed80e5d8874`  
		Last Modified: Tue, 14 Oct 2025 20:41:53 GMT  
		Size: 122.7 MB (122688886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39053b67d4b1b82c7ed2b40da74e1b42ac5427dcea459236b699109e487882ab`  
		Last Modified: Tue, 14 Oct 2025 21:16:41 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809c94e9044759e185c15d8c04151c4f82d18c84b495edfd6b67c238e9d774e6`  
		Last Modified: Tue, 14 Oct 2025 21:16:40 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb03aae3902412f48bcf041fde4a7046f46197a6afb60c1d3d938d1c68984f6a`  
		Last Modified: Tue, 14 Oct 2025 21:16:41 GMT  
		Size: 79.0 KB (78990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbfd238808bb926c985587b335f9b612bd7448b82d5ee1deb1edfd29e115b62`  
		Last Modified: Tue, 14 Oct 2025 21:16:41 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094403bcf2c29af99a68239690d16b75e3a21ec1297a6e26928be6188193c3da`  
		Last Modified: Tue, 14 Oct 2025 21:16:41 GMT  
		Size: 275.2 KB (275221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a0a489069791988520fd26fd08206f1d43dd58ae4063796e39859ce8eefc66`  
		Last Modified: Tue, 14 Oct 2025 21:16:41 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463dadf9f6719ab6d2c44b8a2de12fe8ac89bd0e85e0875c7d01eafe7ccdb1af`  
		Last Modified: Wed, 15 Oct 2025 01:08:53 GMT  
		Size: 783.2 MB (783172881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718721ef789a91fcb327ac63a61b105621e755aa3544b57f03d9098ef6fb141a`  
		Last Modified: Tue, 14 Oct 2025 21:16:41 GMT  
		Size: 87.1 KB (87067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23426dd6e3fd8b09c0d4c8269d9d8e6199ca1eb24dd320026f048c7d8d7fa08`  
		Last Modified: Tue, 14 Oct 2025 21:16:41 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5193d88c159e9c05f4613214db9cdb0d48491d05db6c3496505c54ba6bbc68`  
		Last Modified: Tue, 14 Oct 2025 21:16:41 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c6ebb8e2efac58f4f89034161f8ced2a513669352234fd75f39673bfc001cd`  
		Last Modified: Tue, 14 Oct 2025 21:16:41 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
