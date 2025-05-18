## `mongo:6-nanoserver-1809`

```console
$ docker pull mongo@sha256:9027c5ab080dad167817ac5b0eae629a25bc4f0066f5d71bc75686e8da9a2d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `mongo:6-nanoserver-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull mongo@sha256:4c58d3077373acc4acb18237cb7e9168d5ab466c085e7765f369911f4b8e904e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.1 MB (635103664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb3ab2c84fe0c54ec2978e6bb30aff6c1e007de09f77ddce515bb61619f8943`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:13:51 GMT
SHELL [cmd /S /C]
# Wed, 14 May 2025 21:13:53 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:13:55 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 14 May 2025 21:13:55 GMT
USER ContainerUser
# Wed, 14 May 2025 21:13:57 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 14 May 2025 21:13:57 GMT
ENV MONGO_VERSION=6.0.23
# Wed, 14 May 2025 21:14:18 GMT
COPY dir:61cfe29ccc038afb3fae0bca0d9d2a1c9c8488076e3e2305b0edb2748a3a7149 in C:\mongodb 
# Wed, 14 May 2025 21:14:28 GMT
RUN mongod --version
# Wed, 14 May 2025 21:14:29 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 May 2025 21:14:30 GMT
EXPOSE 27017
# Wed, 14 May 2025 21:14:30 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Thu, 15 May 2025 19:27:12 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3d1a34185ce58f76deeeaad93b451736fb282f4050a266353cf2b27382f880`  
		Last Modified: Sun, 18 May 2025 13:30:50 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060a4a9d42e384fe802f07c3e611bc8bf99a48fbd21438ee07a5ba4b41f31294`  
		Last Modified: Sun, 18 May 2025 13:30:50 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6703c49d120b80008930a13957ebc28ed160c16dfe4ffadb6532442a23d24e50`  
		Last Modified: Sun, 18 May 2025 13:30:51 GMT  
		Size: 70.0 KB (69963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe99a5d04b5fb685a4c58e351d970920725a5c4589e6e2d82038ade52e16c26`  
		Last Modified: Sun, 18 May 2025 13:30:51 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b23175d12a8d9b4daeaa41bd93d8eb68c5d6c49c276b728f3b3d8af981c602c`  
		Last Modified: Sun, 18 May 2025 13:30:51 GMT  
		Size: 275.2 KB (275213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344472dff56f53e75f203136dd0aed263c152dfeecd03e0ce5516991293de693`  
		Last Modified: Sun, 18 May 2025 13:30:51 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9353e198a43eb2591cdc59ef1a90dffa0f5e048167ac3b4a08333682351f306`  
		Last Modified: Sun, 18 May 2025 13:31:10 GMT  
		Size: 525.9 MB (525897387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef6bccad31a3dcb4b77d9ee09a30b49f6de0bbf2b2acfa285ac3ffd4edc3b8b`  
		Last Modified: Sun, 18 May 2025 13:30:52 GMT  
		Size: 72.9 KB (72931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b88e0154bb07d5e6216919e6d97cee5039b831c3f52268e152ddb7bb29faf3`  
		Last Modified: Sun, 18 May 2025 13:30:53 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b623f2accdcb97d60cf6ae3d7ef732fe207bb955c38851f30454a660c5b487e4`  
		Last Modified: Sun, 18 May 2025 13:30:53 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7457c968db6cda6931bfc58f133c76b4528f1358e1d1e3368c4020aba82dfc63`  
		Last Modified: Sun, 18 May 2025 13:30:53 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
