## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:1457840adf94207a17c173bab674fc30504d1380c21f66d17ccbd73546bdb91f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats-streaming@sha256:0b0c2d56e56312e08501b5c0e8e7264735fc108c6cc2ccb77e4a2a0394c689f3
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107106401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86130c4cb15aed1faf6a8163af65379bc66c24a6a2dbdc9c8a5e367435d78d6c`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 16:25:38 GMT
RUN cmd /S /C #(nop) WORKDIR C:\nats-streaming-server
# Wed, 11 Mar 2020 16:25:41 GMT
RUN cmd /S /C #(nop) COPY file:d30725f7225d14fba35e88513adf63da18fc9fef9c4f6c817dff8f784f19a7c1 in nats-streaming-server.exe 
# Wed, 11 Mar 2020 16:25:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Mar 2020 16:25:45 GMT
RUN cmd /S /C #(nop)  CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f9713fe392f2646ae2d2f19d5b16a0a50f2ad34b42238b83a491ce98e3db76`  
		Last Modified: Wed, 11 Mar 2020 16:26:07 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb6795cc41683bf4138bb6a9aee655d335de3ca1ada829792a6d71ca1504107`  
		Last Modified: Wed, 11 Mar 2020 16:26:09 GMT  
		Size: 6.1 MB (6052165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6d239b735f93015c2db6889b9ad447ab5c094d120fc666f1d7ea07afdf3440`  
		Last Modified: Wed, 11 Mar 2020 16:26:07 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c57c8fe372c8b68b6d9963dcafa248d5b6bebb2d456ff2771938e9a6e72dd1d`  
		Last Modified: Wed, 11 Mar 2020 16:26:07 GMT  
		Size: 937.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
