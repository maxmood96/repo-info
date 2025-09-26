## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:c978598a76ae84edb8234a51b94adb8e48d2e866939db6b798fda70fbe241834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0ed5a343ccff58480a0eabdb028dc6171fd65e71b787084afb5055f1e26f91b4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168940516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab44b025f4e25b4bc45528b85336f47e2065682135e28e1541becf4fc2b6573`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Fri, 26 Sep 2025 17:09:37 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 26 Sep 2025 17:09:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020b3d9e5186e58d6b6b9f80992bfec3380bd94f1a67489f919224438e5e54a`  
		Last Modified: Fri, 26 Sep 2025 17:10:19 GMT  
		Size: 46.2 MB (46217409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4543f95ca8abb90dfeef1ae83568ad3fe92ffc55985271408029c40155cfc43e`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f9160480d9602d2fa2a1a6a532430d811dc892c13eb11b35f261864b35a906`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d022905abf031d9d253a719e6549a7ecd31e3f89ecb38ae6278af0cdc66051f0`  
		Last Modified: Fri, 26 Sep 2025 17:10:12 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
