## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:ab4bc31aafcb80b834c7e728403f917b4e5aeea750e1836822033d1856efec16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull nats@sha256:974a4bde7889b595a1bba76aebbe99f649ca6884c2b2360f3bea768e52c78bca
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107658261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a602aa55a6e6e3b0a5117ef6922270d202387eeac81052ff2ac210e487615d0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jan 2022 05:19:42 GMT
RUN Apply image 1809-amd64
# Tue, 11 Jan 2022 21:15:41 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 21:15:42 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Tue, 11 Jan 2022 21:15:43 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 11 Jan 2022 21:15:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 11 Jan 2022 21:15:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Jan 2022 21:15:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f9d5f05eef69cdb907192f860ff14ce569d925f1f53ac5255a5b37631124fd4d`  
		Size: 103.0 MB (103014618 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d7e0d8adfb71ce7eb5a4fc2b1c6af90cb9e67d616478257638845f142a0ca06d`  
		Last Modified: Tue, 11 Jan 2022 21:19:24 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739ebb4c6030882308ebef55b7148897837131a2805a3d98baadb242faab7193`  
		Last Modified: Tue, 11 Jan 2022 21:19:27 GMT  
		Size: 4.6 MB (4637224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68281b646672bb3a84b93bd50d2d14e34847a4becf6a9f3d7eb286269298d195`  
		Last Modified: Tue, 11 Jan 2022 21:19:22 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9868e84e798c51ff2b35929c327a2390edd165cf4d55d6b4a9aca490e3bc0159`  
		Last Modified: Tue, 11 Jan 2022 21:19:22 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67364c3cb728dd10238169569c4301861dd4d18bd26889b6d679e64b54190faf`  
		Last Modified: Tue, 11 Jan 2022 21:19:22 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e697499e064d8be1d0102be2eb0de04cd08a7caf78f00a86d8ced2501669b5a2`  
		Last Modified: Tue, 11 Jan 2022 21:19:22 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
