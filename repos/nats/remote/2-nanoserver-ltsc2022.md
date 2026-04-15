## `nats:2-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:67c59681dcbe87f3ec27cdadc3ddaa6ffc47d3adae4c474940844954900fcd5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
