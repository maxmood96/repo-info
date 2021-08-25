## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:d86bdcb9e19d16a21ea8eb07693268eab508df92a0df40021ca3b296412ba430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull nats-streaming@sha256:6cf5f132f44fee4ec7d112868c7525aac42e5eef00cd0298e1efdffcb1df5251
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110038648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7863a1802021516178bb5e20547b7e410590d3ad269287d3d99fd163070dc55b`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 Aug 2021 19:15:20 GMT
RUN Apply image 1809-amd64
# Wed, 25 Aug 2021 16:07:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 25 Aug 2021 19:33:43 GMT
RUN cmd /S /C #(nop) COPY file:9670e5d1fe5a71e47c78fde01235a0bcbcafcfdeeacf96a7669f6e49343fb03b in C:\nats-streaming-server.exe 
# Wed, 25 Aug 2021 19:33:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 25 Aug 2021 19:33:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 25 Aug 2021 19:33:46 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bc8517709e9cfff223cb034ff5be8fcbfa5409de286cdac9ae1b8878ebea6b84`  
		Size: 102.7 MB (102741177 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ae8616c17f5cca409a4b1289387e37dc532657ba2b52bb60713ff621acccd506`  
		Last Modified: Wed, 25 Aug 2021 16:11:20 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa124ed4fe9f29ce6e3db339e67e84f8667fe9ad034f27a42d6554c473e49de1`  
		Last Modified: Wed, 25 Aug 2021 19:37:03 GMT  
		Size: 7.3 MB (7293262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e47ccb646b6561c33cebea3e0f6ffb755fbcec2983095a9fcd42cda5c49b519`  
		Last Modified: Wed, 25 Aug 2021 19:37:01 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993faf624f9f41d879898713c9dd7875da6724079bf4f9d0a8af4c5a780dd6c0`  
		Last Modified: Wed, 25 Aug 2021 19:37:00 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df1fdf71a2973683c32f5a7cbf28584f357d292855672645e4fda8b1200e200`  
		Last Modified: Wed, 25 Aug 2021 19:37:01 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
