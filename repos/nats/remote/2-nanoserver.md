## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:09420b20941c6825adadfec46bf24ceca4dc4531a0c4f920322c3ee310f0b7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `nats:2-nanoserver` - windows version 10.0.20348.4405; amd64

```console
$ docker pull nats@sha256:a13d4c853cf9b2d63e09e38454c0afd979770d3ab84dbfefdd73d3b240150551
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133114588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea7d03ab96edc5906c396f4414b9607f1f88355d8c64a6d02db9275d068703c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:13:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 13 Nov 2025 20:14:01 GMT
RUN cmd /S /C #(nop) COPY file:535a93d60857154c5ac55d0d7af70be7681f4504034f15d5ac0c21df03a88e61 in C:\nats-server.exe 
# Thu, 13 Nov 2025 20:14:03 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Thu, 13 Nov 2025 20:14:03 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 13 Nov 2025 20:14:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 13 Nov 2025 20:14:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb700c6245ddf0de0a7495954ea0de771edf25a34598f0f4ac3b9423b981635`  
		Last Modified: Thu, 13 Nov 2025 20:14:23 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5bf8300008e6e623ee0afbe95c0f4e2d2510035571d1f0481ae66da882b9f0`  
		Last Modified: Thu, 13 Nov 2025 20:14:24 GMT  
		Size: 6.8 MB (6759603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbd79a682e5841e93a99b804d735145c796fbfcf7c8fe9e5b848fb15b453a7b`  
		Last Modified: Thu, 13 Nov 2025 20:14:23 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a20d8d277e649225666a359aca7a6c7927b6c9a2e765c1d8f854065a539ab5`  
		Last Modified: Thu, 13 Nov 2025 20:14:23 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d5a6c86d2741f9074b2d1508c31c730808a9d8e7834b7ea92d67233c57f9bb`  
		Last Modified: Thu, 13 Nov 2025 20:14:23 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f53e92b8e88b48ec8c1ef155092d872e5d9c40356684b995dd4bb0eb8390849`  
		Last Modified: Thu, 13 Nov 2025 20:14:23 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
