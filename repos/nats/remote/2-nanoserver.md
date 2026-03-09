## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:225d0e6e6cd57a0c9784fa5a176acf49e20ee295e6327388a74dcdb8cd3ccc33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `nats:2-nanoserver` - windows version 10.0.20348.4773; amd64

```console
$ docker pull nats@sha256:c3a7a2d0e439177741b86cf21780b58ecbdea1409215df892b025d62e3417892
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133462538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328630bb8297212012272b4483caa99000a2b1170ed01d4def5cf37e4a7ea569`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Mon, 09 Mar 2026 19:11:17 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 09 Mar 2026 19:11:19 GMT
RUN cmd /S /C #(nop) COPY file:43ca0d983360e736f84645c39fd7ae598025f6a645ae4c2ce4b8bae51bced147 in C:\nats-server.exe 
# Mon, 09 Mar 2026 19:11:21 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 09 Mar 2026 19:11:21 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 09 Mar 2026 19:11:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 09 Mar 2026 19:11:23 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ee60fc4b917c336cd905b0b17d74c86282430370aa1958931b8eb44b53a77f`  
		Last Modified: Mon, 09 Mar 2026 19:11:29 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec66611e27513817705276776fffa484fb996781abbe6097473ef8f8093a091`  
		Last Modified: Mon, 09 Mar 2026 19:11:29 GMT  
		Size: 6.8 MB (6810721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd63af06503a87a28a3a71022f8fe158e610f6c914161650533270bceea28330`  
		Last Modified: Mon, 09 Mar 2026 19:11:27 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef490510ddb6582f873f4e4bb3b95a201f866f1f749efe7c450c362b1cceff9`  
		Last Modified: Mon, 09 Mar 2026 19:11:27 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882d8cf87a36788b87434d5ea68706b754d28bfbf96ae8b7ba29c2221ad35f25`  
		Last Modified: Mon, 09 Mar 2026 19:11:27 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8607cbcdafcc6d4412572d357c5eed736919f0d0aa1fa9606bb7baead14726b0`  
		Last Modified: Mon, 09 Mar 2026 19:11:27 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
