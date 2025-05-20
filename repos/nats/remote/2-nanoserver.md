## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:a07df4097a4c1873483b76056063eb213f9ab0d0f6fd8ee605afdc6aa54b7dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:642d8ac9e0f7bc76792c08a25b9cacf71d116f1fc48701d53e0b036972d7f948
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115265569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9784848fd15a61547f896c95456c69a4624a5ccfa6f84f14f47b55784e7b4294`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:16:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:597800b942878c0dcccccdeec13566a54f5747a8b41cbc437b6c383be7c26c87 in C:\nats-server.exe 
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:16:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad300c79b9fb6f66461ded839672cf5492f7b7af1319ba6344cb0f67263cfaa`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2d6584ea4f816da9da1b5bde7348f1a160d02be028974fdec19ec192f9658c`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 6.5 MB (6478829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e50007f7d9408bcf642455e42c149e2cf2daa0055501cd7dae3b7667d00cd6`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71cf377f3df963a9df597c52163edb65f2c3248bf2de4f778ff73143482f0ad`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa2abb8e2da4d28cdfdade0dc0170836c44ba60c406a99fb05c0a8625b2a455`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed03abb4afa45ed75da236ad6dbc36cce574ce5dfb494e488e44f5f1e4ef4a`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
