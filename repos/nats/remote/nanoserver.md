## `nats:nanoserver`

```console
$ docker pull nats@sha256:eb088aff92f49bf823f3933a4d582aeb4ac99d4dd48270914e683be32c62f966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `nats:nanoserver` - windows version 10.0.20348.4171; amd64

```console
$ docker pull nats@sha256:5d311b75455af9a9577fdf1c3a27f400749e68befe8a95018d435e3ee0488e9f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129263636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6927cb3ba9055375243425e0c1412a10b6e79543add6d3d4cfbb21bd94b633ad`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:17:47 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Sep 2025 22:17:47 GMT
RUN cmd /S /C #(nop) COPY file:9c1a83152c2e39446c19aa7a7278dd5b50096719eab3aa3800141409e06312d9 in C:\nats-server.exe 
# Wed, 10 Sep 2025 22:17:48 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 10 Sep 2025 22:17:49 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Sep 2025 22:17:49 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Sep 2025 22:17:50 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f455bbd7d7fbd02e945ceb4ecf6b633775c5357b5d18c7546dbd40f42e1ee01c`  
		Last Modified: Wed, 10 Sep 2025 23:06:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81baa6ae2590d20f9276bb5c5ca35522f8f37e620c90d28a754e8fcfa9e5916`  
		Last Modified: Wed, 10 Sep 2025 23:06:47 GMT  
		Size: 6.5 MB (6537789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c9a7bb0554449bd4c40021e473a63190f3f244386283a8df430ea8d3c7a7b5`  
		Last Modified: Wed, 10 Sep 2025 23:06:47 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00587ed76196b7c1ffd9e82df97374fab43e0554f03759b5596b1557de649c94`  
		Last Modified: Wed, 10 Sep 2025 23:06:46 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3031a870d459aac4d4d6d60f9383f6fa771c2a6c985c9553b2522ef835071f7e`  
		Last Modified: Wed, 10 Sep 2025 23:06:47 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5aa83bf6c3a16b6a678b51ad9efba4d06e394f6235643fd49fdf3d4c7ecb065`  
		Last Modified: Wed, 10 Sep 2025 23:06:46 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
