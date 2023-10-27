## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:2dfff9132418c9602296d363dad4e205e785752d73ddca9f4537f91cd4db57c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:29e2152405ed849d5c5589a35cf02b73576e88e08f0adf67040f458759dd892e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110065642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c710ddccc8cd69660a72c1525134e455f160899596c1a5f5155ce6f586ebdf7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 Oct 2023 20:17:42 GMT
RUN cmd /S /C #(nop) COPY file:18d2b201bedf44d6cf20990a5e1d83d3832eede6b2be4d6fa577c7cc28820bc5 in C:\nats-server.exe 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d2c4e1901a577a53d576303c5fb185d5d603a51a5963cce465f38722e9e7e3`  
		Last Modified: Fri, 27 Oct 2023 20:18:46 GMT  
		Size: 5.6 MB (5594656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708131235a1cef76196cb5edbf912ebbc24020f96d3b0d168efe49cd88760665`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43906e90b84754a9e07f7b317810dec4106ba10d159dfe5bad8f536f9e8a376`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f4774c11b47cdb1c9434e6a07a055c33e201ece83051fd6bef2bcb38b955cb`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c20f4d32a522c57acefece567048f4c290d4245799d7957e49dabe8bec88d`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
