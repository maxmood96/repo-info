## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:20482a378759deedd7166b16e815327d2bcd992496a6fd8d9619da0a6197b393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:c9c636486ff1dc545be9b180e9d5b9fc0082f67215e6da7a799fb302615059a8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176211547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e99f842b929588a924ce2fbf5aff655ad7ff59b30cfb596498e8223f687c16`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 27 May 2025 15:17:58 GMT
RUN cmd /S /C #(nop) COPY file:924b82a6802fb4e8cf126ab6f07a4372c6070c83b784fcb0de9440d142a32bb4 in \ 
# Tue, 27 May 2025 15:18:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 27 May 2025 15:18:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 15:18:02 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d009a39cfa2ec096f4b9305fb6c88444ba99b07f9f00274d8e7c43eb87885`  
		Last Modified: Wed, 04 Jun 2025 18:26:19 GMT  
		Size: 53.6 MB (53631658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e349971c9ecaeaae66d83dbd41ecb0e9e356bfaf4411d7aa31e935e81b78f476`  
		Last Modified: Wed, 04 Jun 2025 18:26:15 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd47b4c43feba126f6c436b6c0417e0ec7aea01f5fe47138de39bd5c47d3fe30`  
		Last Modified: Wed, 04 Jun 2025 18:26:16 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be31ab4f88c09d2ebb9fcef11f5dd558c7cce9d42119d5eef5b1fa6715d32402`  
		Last Modified: Wed, 04 Jun 2025 18:26:18 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
