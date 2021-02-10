## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:b89cba5cf792b4be014bbb1be1a2fbca1c0019946c989c8a903c7ed865c0e7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.1757; amd64

```console
$ docker pull nats-streaming@sha256:d13b43d591f725a510ae54f0f2efa114399a0a0c9e85f0652bc802e7e8d45187
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107432722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc67b6d7f9c859b2a9e9272dfda84571744e233c3ada49fdd3505d40e586c859`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 02 Feb 2021 13:06:30 GMT
RUN Apply image 1809-amd64
# Wed, 10 Feb 2021 16:02:26 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Feb 2021 20:00:55 GMT
RUN cmd /S /C #(nop) COPY file:f2450ffeda74e33f820191eccf78b6647ce56865170e966bfa8e72afe6e46c36 in C:\nats-streaming-server.exe 
# Wed, 10 Feb 2021 20:00:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 10 Feb 2021 20:00:57 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 10 Feb 2021 20:00:57 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ba17af31b9276ee11fdf859681b442db50979a39eff4cea2a559a5755cedbe01`  
		Size: 101.4 MB (101406193 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23b613036f8aee9066e712b3aa58f10f2fde093623511a5658867f53a6d01b18`  
		Last Modified: Wed, 10 Feb 2021 16:06:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546c4d75ec4cbc867ea01774757b0a9303906569a30157fd804f8c1bc5d4e63e`  
		Last Modified: Wed, 10 Feb 2021 20:06:15 GMT  
		Size: 6.0 MB (6022164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d942fdcd6082f7ac407761ffc6d739677d6fe08f0f51db38d32d33398e9073f`  
		Last Modified: Wed, 10 Feb 2021 20:06:07 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c29c3e2255d5f0292ecd161299cb57afc896ff1c7002836b53577f1d57e6fe`  
		Last Modified: Wed, 10 Feb 2021 20:06:07 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12923e759dcf1b0d858f5bfacd7f73cffa442500803639aa349428d981cd881f`  
		Last Modified: Wed, 10 Feb 2021 20:06:07 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
