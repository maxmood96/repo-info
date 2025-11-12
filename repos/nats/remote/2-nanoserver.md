## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:2305d83f3cec3eb5203138032578a08c91d04c002319ff45bac3a7d152df4c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `nats:2-nanoserver` - windows version 10.0.20348.4405; amd64

```console
$ docker pull nats@sha256:38eeec170f6af0685d80b89885549b9920889374e448168a9ed26f2e453a3b1c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133090042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469566d2a35006e1241b5e2c60c8af84b5399cfdb0b5cee51e9498ebb8f794cc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:09:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Nov 2025 20:09:43 GMT
RUN cmd /S /C #(nop) COPY file:686e92130a21a0cff4a93b886b2e653659a4511975aa0c795cb937f76795c7fa in C:\nats-server.exe 
# Tue, 11 Nov 2025 20:09:44 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 11 Nov 2025 20:09:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 11 Nov 2025 20:09:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Nov 2025 20:09:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecf6e4ea7acabc7088086f67a6f1d5827a92ebb16b40f917bce6b3978604695`  
		Last Modified: Tue, 11 Nov 2025 20:09:59 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc01e4d05861b92a86a55b56ebf0a323db7cc8fea82f539284bf874b5e42ac1`  
		Last Modified: Tue, 11 Nov 2025 20:10:00 GMT  
		Size: 6.7 MB (6734992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e629d244869a518de24b00a83232334b4d2889a316d2bf3c4cd99fee8f0437`  
		Last Modified: Tue, 11 Nov 2025 20:09:59 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f7be50c76968b969f6a05e70679793ceaa1ec5fc46f677a82d3b8c4bb11ecc`  
		Last Modified: Tue, 11 Nov 2025 20:09:59 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c679fcc1041f6ca08cf203b5b9824dde829680e3b06afc730935f01c1229fd6`  
		Last Modified: Tue, 11 Nov 2025 20:09:59 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b319e77e8f0ef3344ffefb380a392255f0d3baed249dc35cab730a4e2774e73`  
		Last Modified: Tue, 11 Nov 2025 20:09:59 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
