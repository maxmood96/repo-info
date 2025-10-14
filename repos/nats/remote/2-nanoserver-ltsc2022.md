## `nats:2-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:1ae9540d9af3c477920201ef4464f4d316baaf0e46a9e6bc229c58ea021e3bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `nats:2-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull nats@sha256:c9f7197c61282c83acf57a3687a62f01ae0e9caf07852546c836ac028ef35e2c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129460850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4972d008c093bd74500118be02d44207980d13db190ad107d45764d969f09b4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Tue, 14 Oct 2025 17:53:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Oct 2025 17:53:04 GMT
RUN cmd /S /C #(nop) COPY file:686e92130a21a0cff4a93b886b2e653659a4511975aa0c795cb937f76795c7fa in C:\nats-server.exe 
# Tue, 14 Oct 2025 17:53:05 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Oct 2025 17:53:06 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Oct 2025 17:53:06 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Oct 2025 17:53:07 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd8bfc0d24c64fa0fd6139249c56cf710d34e1fb61d4f38b23da6e85496ebb7`  
		Last Modified: Tue, 14 Oct 2025 17:53:23 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2c08fe839b984b6af77296c5b54ae2edcbed3d654f6ee3b2555f790d627f39`  
		Last Modified: Tue, 14 Oct 2025 17:53:24 GMT  
		Size: 6.7 MB (6734978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc41d284aeeda50d4551eae6725d5b5f7ca38dc95e23ba286b9440e57a7d081`  
		Last Modified: Tue, 14 Oct 2025 17:53:22 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0597a886f3f8f28c83d2e30dbe02019b67a1785de9d80244b9173ee2b45035d`  
		Last Modified: Tue, 14 Oct 2025 17:53:22 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5082a13ecb1018e29923a6fdbdb66ab214ea673cf89974078d7213180a53c7`  
		Last Modified: Tue, 14 Oct 2025 17:53:23 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9dcdd7a6b5767957c7ba583fae351a4e0006dd7da067432eaf20b4590fd314`  
		Last Modified: Tue, 14 Oct 2025 17:53:23 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
