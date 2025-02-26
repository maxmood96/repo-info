## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:e37f384db2351a1bb09c1e1640b7571e012bece8e5579c2660ec07bf788b53ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull nats@sha256:6a4cc4d864f9bac7dc07b623679bf121113d41d21fc9b5e640e3c92fca1e5111
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112965803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0766c346c8b6c207312a07351709a6e4da8cd036fbaaa8c380d71c1d32ae393`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Tue, 25 Feb 2025 22:17:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:1eb0b36109ac529ab5d5db4ea880cfd63ed514d1f542c8bd20a200d73207ed8e in C:\nats-server.exe 
# Tue, 25 Feb 2025 22:17:41 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 25 Feb 2025 22:17:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 25 Feb 2025 22:17:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464c91c36773a1621c7277522f95c645dc9866e58b0867242b34277fc4145ada`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0903b195c823336fbd58a8a52901057cbde5d4f8e8a3fe8d643f7f0b1008ee5`  
		Last Modified: Tue, 25 Feb 2025 22:17:46 GMT  
		Size: 6.0 MB (6044491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a624018395b9843449197873a8dfbfcd7cc07efd09eb9f5cb1fe8b5638255438`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbf5f27ca2dfe7fd5ede70769269354cf7852fe304a1af5d4b7bd17e201a74`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0a43a1bf148b020d83f3b26345be5a7f7cdc277350321ce4ad5a4e0fc73662`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3091f851d62e9660edca35a087ab74e6ce5c1ab16cd2dcc10c87c3b1e04be8`  
		Last Modified: Tue, 25 Feb 2025 22:17:45 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
