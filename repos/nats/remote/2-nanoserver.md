## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:822151cc4833578c40f664ff32c6a4f4e36cf3d8d3388dfe50ef72e07ba93ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `nats:2-nanoserver` - windows version 10.0.20348.4529; amd64

```console
$ docker pull nats@sha256:b7344e8fe4fb2e9826f183e435fd7f69e38244f076474f25f8985a388f1f0451
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133123840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18afd930c1273558b2940a438abb5eea26a609fc8afe400f118343084bb9d01e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 09 Dec 2025 21:11:35 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Dec 2025 21:11:36 GMT
RUN cmd /S /C #(nop) COPY file:535a93d60857154c5ac55d0d7af70be7681f4504034f15d5ac0c21df03a88e61 in C:\nats-server.exe 
# Tue, 09 Dec 2025 21:11:37 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Dec 2025 21:11:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Dec 2025 21:11:39 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Dec 2025 21:11:39 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be690722ebdf830c94db50b75ec2bf6ba64d3f61fc6b61ab47ae69601ab75e87`  
		Last Modified: Tue, 09 Dec 2025 21:11:52 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25661e806d2e0a2132d7128454dee61e7ae978aaa3e710b13ea848b97f5865ae`  
		Last Modified: Tue, 09 Dec 2025 21:11:59 GMT  
		Size: 6.8 MB (6759586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42701aaf11df484f4204213bf8c5a26460accc07129910334c4af0706645c289`  
		Last Modified: Tue, 09 Dec 2025 21:11:52 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18b442cb5d529d5d0eaa769bc03aa39195bd9e000146e2fea92f9f0e7328956`  
		Last Modified: Tue, 09 Dec 2025 21:11:52 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4a85d38f9688ad77734919ca2475747578e72aa4901c80cc779d91bd814379`  
		Last Modified: Tue, 09 Dec 2025 21:11:52 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d053bdb1fa008e614e5ac5c74444bbd0b4e0e24de0eac21c8ff6166413a44e`  
		Last Modified: Tue, 09 Dec 2025 21:11:52 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
