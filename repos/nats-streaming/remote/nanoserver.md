## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:4de80fbfeb8277288ff367518b4c7c5eb4e13ceb10eda02f84719b6695fc2716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats-streaming@sha256:70457d59bf8f641124aa7b3c848841338ee28f012260a0f6458186aed0ccb5d3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110376627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f0f50108112053bde00c6f878cdbf5c09cc7e463174a06e20bc5ee3b2b09b8`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 14:45:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 05 May 2022 01:19:37 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Thu, 05 May 2022 01:19:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 05 May 2022 01:19:39 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 05 May 2022 01:19:40 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a6063f744e542c21ce471bdd7ff0dd6063d8d2a9670afbbc64d086813afd6385`  
		Last Modified: Wed, 13 Apr 2022 14:46:35 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626ed23ac1eee671c5c89470fe85f192d11e27753dbd11a1247ff5dd42789274`  
		Last Modified: Thu, 05 May 2022 01:20:36 GMT  
		Size: 7.3 MB (7275843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc19d983b61231bf40f681d8042f2acfca8443e1639df10ce95d575f5a02d7d5`  
		Last Modified: Thu, 05 May 2022 01:20:29 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e73853c427db84509c80e49720d7689e966d235b52a8a9b19cd39aad28568b`  
		Last Modified: Thu, 05 May 2022 01:20:28 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73881baa094fec2fd243f7ad489585665de0fab78678f7953b88f2234e863093`  
		Last Modified: Thu, 05 May 2022 01:20:29 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
