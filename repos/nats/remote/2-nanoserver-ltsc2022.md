## `nats:2-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:b8d325261e82cfa9b4561b3752e5791fc51c257bde48ca6e1ae65580749766a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:ad04df86864a0653927e5ff2293212d694588db88edc746ce8b917417317c0f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134078105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7e5bd03f66dabebd5917cf13f4067081477a5934e86d07357d04db10e33ec4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 20 May 2026 19:09:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 19:09:15 GMT
RUN cmd /S /C #(nop) COPY file:5d608f6a5cbf80544d196a9ac38d66b2635084a5e0a392611785993205e5329d in C:\nats-server.exe 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c815e3255991cc2df065c98a27664be46d8b5db04231449f637ecaf64c5c098f`  
		Last Modified: Wed, 20 May 2026 19:09:24 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68983020294e3083531b7192194e9d5172d2a1449eac04682b7544bb139048b5`  
		Last Modified: Wed, 20 May 2026 19:09:27 GMT  
		Size: 7.0 MB (7033380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730756958a80b0245caf373feb8024993ecef9e67a8ade759511f66d001f3f07`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec9d4f153ff90a362ff5591192559ff2e3584441d0bee4e4fdd8b0a4845b833`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb6e35267fc994af8eab6412783ba571dd4c1d14e5fa8771f50a386e61ef655`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838e55b2d659c4cc5f4e0db1773fbe38aa8487984688f5a0f60b202907588e42`  
		Last Modified: Wed, 20 May 2026 19:09:22 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
