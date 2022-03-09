## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:5fd488e5fff30480c88610d1907786362e8ba0a2e06fc646a4320b5346f7bf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:16018303f8883d0b618c73bb51b73367af79afee54399caf17580a4ab8132e7f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110236791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba14e10d46fb18c3615d883ddc1e929197b6d59e5aae5f21c6eb5fe5ab8f968`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 19:07:25 GMT
RUN cmd /S /C #(nop) COPY file:e7d7513784103e13d5583158634b243440959de7cdfaf3602d16eec752946fe4 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 19:07:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 19:07:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 19:07:28 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae434cf0b0889cb39a60312866cfbd6bced1f92991045cbfeb9cea4c44bd1509`  
		Last Modified: Wed, 09 Mar 2022 19:08:12 GMT  
		Size: 7.2 MB (7177899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7c446d1df8e0d38d307a4447d7b715fd3907ef0af25e9e5dd9366dd03e8606`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6e9207650a9cec087f8f7a765e3e8169c789ccdd259d105098b89d0e0cf37`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2fda85f9d643a2b20fca975f07a6ef77ebc839369a60e2dc853ee418e1dc1a`  
		Last Modified: Wed, 09 Mar 2022 19:08:05 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
