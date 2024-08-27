## `mongo:7-nanoserver-1809`

```console
$ docker pull mongo@sha256:392c26ab7601566dc3a72f305df0105ba33696b458a4e8a0397dd040c44fbe0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `mongo:7-nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull mongo@sha256:cf349de4211f48a1e3ffbd8d03abbac091a10bd889aa82d13a22eae88490c8ec
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **765.1 MB (765080078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81847b05c7c0bae385b53b377156ba0626cc18b51f3016837092439800dcce7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Mon, 26 Aug 2024 23:59:02 GMT
SHELL [cmd /S /C]
# Mon, 26 Aug 2024 23:59:03 GMT
USER ContainerAdministrator
# Mon, 26 Aug 2024 23:59:12 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Mon, 26 Aug 2024 23:59:13 GMT
USER ContainerUser
# Mon, 26 Aug 2024 23:59:16 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Mon, 26 Aug 2024 23:59:17 GMT
ENV MONGO_VERSION=7.0.14
# Mon, 26 Aug 2024 23:59:50 GMT
COPY dir:569dc595e568429f713bfa17916f5a0425b14e2551565b8dcffbac1d9a45d806 in C:\mongodb 
# Tue, 27 Aug 2024 00:00:05 GMT
RUN mongod --version
# Tue, 27 Aug 2024 00:00:06 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 27 Aug 2024 00:00:08 GMT
EXPOSE 27017
# Tue, 27 Aug 2024 00:00:09 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41747ab582a5eacae9507a2e0fd8893e2e4bd59f680b56a2f863eb4fa077084`  
		Last Modified: Tue, 27 Aug 2024 00:00:19 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993abd6bf5c8533cbfb4a263e9d48813d56e781345c4504d9421cef88a4a92d3`  
		Last Modified: Tue, 27 Aug 2024 00:00:20 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206c8de63844600001402a26a437d8f443a4df80d0384248ce478ca7a9d501ad`  
		Last Modified: Tue, 27 Aug 2024 00:00:19 GMT  
		Size: 67.4 KB (67401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cb8c64d52d9583820ae958713d6403e58b85b698a7096b87c6da43f668f09e`  
		Last Modified: Tue, 27 Aug 2024 00:00:18 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2ef19858d528962e00f7aeffc7ca4457a68285d525bd5d94fce257f011fa15`  
		Last Modified: Tue, 27 Aug 2024 00:00:18 GMT  
		Size: 275.2 KB (275153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a106a1ddf64cba946113cf053cf420c0b0c42c69be1bfaeb935bab8ed3a42ba3`  
		Last Modified: Tue, 27 Aug 2024 00:00:18 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25b5576f33fc0a7097f406f82cddbc5c6da1bcaa35eef30604e1d36e57c7050`  
		Last Modified: Tue, 27 Aug 2024 00:01:07 GMT  
		Size: 608.5 MB (608452567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafa2e92d4af7b53c47556a98996e755bd0b367a40613a95279dd30248ce30ad`  
		Last Modified: Tue, 27 Aug 2024 00:00:17 GMT  
		Size: 1.2 MB (1194512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c4fc0aa9144690aacd50c40abf7c1af45744a1e95b269c969ce1d5464b920b`  
		Last Modified: Tue, 27 Aug 2024 00:00:17 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8a5ff92efa2ab19f5975ab61d412b9cff9678228dfbc13ad351a6a2c0d89c8`  
		Last Modified: Tue, 27 Aug 2024 00:00:17 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346735b9e1ad14590a1bb35d436fea6c5295d4a0a90d63a6c51d00cb1756baef`  
		Last Modified: Tue, 27 Aug 2024 00:00:17 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
