## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:d89ec06495cc2dc66c48b53b4057c728646dd337c7da31b31c03054d25f8b25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull nats-streaming@sha256:c42aea98792b22c600b56fd4fcd22d8df0966a6bd53133c29e207357a2a740da
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162885879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77524099012a276a37924d94090d5d34db0a59ba1a3b20563c283a7e5440d27a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 21:08:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 May 2024 21:18:36 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 15 May 2024 21:18:36 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 15 May 2024 21:18:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 15 May 2024 21:18:38 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e15682c89e7337c581629534d634fb5bc56c6cea86ed0785b8309b2876701a`  
		Last Modified: Wed, 15 May 2024 21:13:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b50135c931c2eff14ccb25dcde35f918d806ef7f95b29d816ca9fc1dc8be8c9`  
		Last Modified: Wed, 15 May 2024 21:19:15 GMT  
		Size: 7.9 MB (7939863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5083bfc177927413ca43209f27f3e2a80fedac0eec7773bf07cac2d0715c46a1`  
		Last Modified: Wed, 15 May 2024 21:19:13 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d759caf620adf6e2c39e5978210a9d89cd14844ce9320abcd00629e185076e6c`  
		Last Modified: Wed, 15 May 2024 21:19:13 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861f28a52450eeac31fe9fe9072bf68ac02dc69abeb35cfeb6e3445a65a4ad3f`  
		Last Modified: Wed, 15 May 2024 21:19:13 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
