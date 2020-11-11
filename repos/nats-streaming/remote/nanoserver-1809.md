## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:12751d89716d394331c32e35fbed0b0bdb912c970c0b5823ed7ebb6198731757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats-streaming@sha256:44cd613007d0ae80aa675e256fcf7ab09154970b8489a02e0d1969c6143d1f61
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107798464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7c11af94433f8f6727ec8b965b09721a359d79801411d21199752bff82c385`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 21:08:21 GMT
RUN cmd /S /C #(nop) COPY file:cc6bae0f50b6e35b12e8233f240d95e093f7e44257bc87e06aed691866ec1477 in C:\nats-streaming-server.exe 
# Wed, 11 Nov 2020 21:08:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Nov 2020 21:08:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Nov 2020 21:08:24 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bdd54301a97b4ec40a4f7841d98c5c1650eb782b9fa39fa6fd69336f53ee64`  
		Last Modified: Wed, 11 Nov 2020 21:12:25 GMT  
		Size: 6.5 MB (6515173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e84d935a5287b8d02f7d552ad42e43d116f9f8e81a3ab6938ce0bf2f6a98cd`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9847a1462f5644588430244c224e5ee90473d31bf4d0c11157ec2a823aaae1ca`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 927.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e882e784f1673e88e962c1e9a1239de9107334f963eef6c696f80bd1a04f063`  
		Last Modified: Wed, 11 Nov 2020 21:12:18 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
