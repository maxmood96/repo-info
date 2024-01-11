## `nats:nanoserver`

```console
$ docker pull nats@sha256:9e7653cadc9f2e1210a6f4d7cf95f6882e73a1fbfb9af317a2a8759cb1080853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:0237da0c92869cc89b906549bcd163a0fa0c35e4600d249088a38e24acedf0c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656365da7eb279cc4f4b5ce458d452faacd307a572871edca17499eabb5e566b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 17:57:22 GMT
RUN cmd /S /C #(nop) COPY file:f77b98ffa708fbfcf6aa9d766be9e893df4ae6e45b22fd61597a9746c6211313 in C:\nats-server.exe 
# Thu, 11 Jan 2024 17:57:23 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 17:57:25 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b10e2b988ab2be124746af1ddc26c710ea2f77b50009cc4ae6ac2dc88f31904`  
		Last Modified: Thu, 11 Jan 2024 17:58:31 GMT  
		Size: 5.6 MB (5616197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3c333f008880fe22df9882712558f049da18a2f7d116c14ebc99123dc1629f`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb66675f422186e1d9598585f1b449fe84330d2c93232ce521b53f522686151`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843ec2a1ec7a58ad21a5616d5baae229ae6070726a34c8bed83a4b9454cfcea7`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5598974f6bf9da7c1b0f0bbfb58c0a658c40e80d22a29302d195b0fcc910ba`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
