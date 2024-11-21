## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:923c5146fe5646b44fa9728ddc4a04391b09a986eda757e13cc7a5a6e4d4cbc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull traefik@sha256:c0fd6fee9c161c50b82111cb45685603f04614e26925303867590091540c2b4b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169513029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a828815036ca2eb4be92518fd1839a8ce36e5beabd259dc5554162be3598e4d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Sat, 02 Nov 2024 23:34:35 GMT
RUN Apply image 10.0.20348.2849
# Thu, 21 Nov 2024 00:23:49 GMT
RUN cmd /S /C #(nop) COPY file:cb89cc19e8226754d9d0b5b9ac2698de81bd7d300b5b5d2c4af6993dcd53182d in \ 
# Thu, 21 Nov 2024 00:23:52 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 21 Nov 2024 00:23:52 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 21 Nov 2024 00:23:53 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.2.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:815d6b7f925aef8327c34c34073ae54cc1c82120f1058682eac4c8c14ca21c70`  
		Last Modified: Tue, 12 Nov 2024 22:44:32 GMT  
		Size: 120.6 MB (120604951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbbbf261d4ac5437c4fa51f9dcba2370e15b4f34c9be937c9ef3a849f8bab16`  
		Last Modified: Thu, 21 Nov 2024 00:24:01 GMT  
		Size: 48.9 MB (48904995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c524691b14452fd666f08e851b15f0af90bef61f5f7825bd4ce56a20ce8c7e`  
		Last Modified: Thu, 21 Nov 2024 00:23:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9df384dad23257a84cb6a0e0908befe2d51f684a3ddb1b9a407867bf4711b0e`  
		Last Modified: Thu, 21 Nov 2024 00:23:55 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8897cce221daf85d1bf722ed09a04e7af4de91e9674e47c78f1a1eb37b1a33c0`  
		Last Modified: Thu, 21 Nov 2024 00:23:55 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
