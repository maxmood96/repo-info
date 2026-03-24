## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:419eda332cc243b564050f8ff6c94e9df148f930aa3184aaabda593a7313786b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2-nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:270c8d8463baa51263649bb7edccca8023ff18cb3d3e2b7c50c18f66842fcf63
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133481939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e273b1f3c093291412f2567a093288ae663ff189298335e43c0b4843054227a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 24 Mar 2026 18:39:02 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:e4db7c8068a18ff6128cb4e29dc113730e5e5bba4a56f7dd5ff0f84a46b740da in C:\nats-server.exe 
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:39:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:39:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:39:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351c93818316b8da5c0ea0e81ae0f1287bb470901778b5ed4f873c38627b928`  
		Last Modified: Tue, 24 Mar 2026 18:39:12 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b23a6e5cc7736a9f8f4af4b4592aeec779d74315a2ae986e1c61954c30566c`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 6.8 MB (6825438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ccd3dac508a5cfb9034d3c13be911cf02ab3328a3c89f770fca378c699b45e`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d2f227f27ba8db3b1d452511a545f8dceca13ccda3041ed3815eaa39206d89`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54af9b204ea2f0fccd137eda046a7b9d75b76bdcbec8dac0d6b70c9330ddd1e`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8cb95ef4ed26bb079ed5404f2127da438bff5d4b0e02a68597191ce0068b1`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
