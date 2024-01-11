## `mongo:5-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:b8be94ba15d1cf795dcf15d15db5f652a6810c98d48af853c3adacf6df45651b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `mongo:5-nanoserver-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull mongo@sha256:161c5abc44ace5d8d0339447a5081a9ba3e73a3787676b17d25d5ffd585f7bca
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.0 MB (433996276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7e3be4a30d659a4f39c6a1703787e5cb41f1a806935214e420a4c6ea902a3e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Thu, 11 Jan 2024 00:56:53 GMT
SHELL [cmd /S /C]
# Thu, 11 Jan 2024 00:56:54 GMT
USER ContainerAdministrator
# Thu, 11 Jan 2024 00:56:56 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 11 Jan 2024 00:56:57 GMT
USER ContainerUser
# Thu, 11 Jan 2024 00:56:58 GMT
COPY multi:d83167ee7f0a01f519841410f1f031c3bdfa566af08cc1936efaf3b3f20e2b0f in C:\Windows\System32\ 
# Thu, 11 Jan 2024 00:56:59 GMT
ENV MONGO_VERSION=5.0.23
# Thu, 11 Jan 2024 00:57:19 GMT
COPY dir:2659c84e3b8fc52d2b276105c78a0f2d3093204246f7c91798b9f2aabebcfb2d in C:\mongodb 
# Thu, 11 Jan 2024 00:57:23 GMT
RUN mongo --version && mongod --version
# Thu, 11 Jan 2024 00:57:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jan 2024 00:57:25 GMT
EXPOSE 27017
# Thu, 11 Jan 2024 00:57:25 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:11d5cdc5eaac7bace3ae1ecd3c0df2a27ef5005ab296c56b7f83e24bf25c236c`  
		Last Modified: Tue, 09 Jan 2024 20:57:18 GMT  
		Size: 120.8 MB (120769267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ddb751b56c0488a10783b417420f69ada077cdc0f0b7ec504fcfb29c7e5fe1`  
		Last Modified: Thu, 11 Jan 2024 00:57:34 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f751efafeefef1c21950e522dab099ee651d780a714f969433937caeb9beac68`  
		Last Modified: Thu, 11 Jan 2024 00:57:33 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b60bbadd5fb92ae80778e97f6067e81ef34aaff0cf151ed530c6a3c5080a76`  
		Last Modified: Thu, 11 Jan 2024 00:57:32 GMT  
		Size: 78.4 KB (78404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4fe64c04517f4fc3f6376441720ad4827f69f3d7afc657e2a7e7b49108b058`  
		Last Modified: Thu, 11 Jan 2024 00:57:31 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3890e0cd8b6bbc560d0f89da59268559a7d4a46dacf2d669f7cb8a68cb839e99`  
		Last Modified: Thu, 11 Jan 2024 00:57:32 GMT  
		Size: 263.4 KB (263360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a76f8e103b6aab8bc7df2d453364e2721d646b4609bf5053867e65e9442dcb2`  
		Last Modified: Thu, 11 Jan 2024 00:57:31 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe73169d795830681afc8624a27532b69b833b8ea244c0dda31c98b8256305ef`  
		Last Modified: Thu, 11 Jan 2024 00:58:00 GMT  
		Size: 312.8 MB (312794245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8f713fc80fe86b7bf3b23fef76442933216e5cf2a115613b50c450da52cbbd`  
		Last Modified: Thu, 11 Jan 2024 00:57:30 GMT  
		Size: 83.7 KB (83729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2c4e450bd6b94d1fb162d07595d862e5bc122d2183844b772deb16a6a3e02f`  
		Last Modified: Thu, 11 Jan 2024 00:57:29 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d093b409b2402072dfda38fc0d78c9a12768b7e3d84f602f82a446f351bad85`  
		Last Modified: Thu, 11 Jan 2024 00:57:29 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd2fffa8906e4e4ad97b152a8a169eea8cd3ce74a648595d21383a82977e3e0`  
		Last Modified: Thu, 11 Jan 2024 00:57:29 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
