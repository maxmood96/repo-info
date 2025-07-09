## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:661d410e1df35e36c6209c8a30e72267c26db5bee7a7feb73a473f8b183e2fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.3932; amd64

```console
$ docker pull traefik@sha256:711d2567295c60618d49000ef9aed699d139b1ab72166918aa833648477436e9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.9 MB (176861139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3b66b0d9760142a7567643ea0c8809982320c1bffdfc39c630b3386b86c841`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Sat, 05 Jul 2025 05:15:23 GMT
RUN Apply image 10.0.20348.3932
# Wed, 09 Jul 2025 19:12:47 GMT
RUN cmd /S /C #(nop) COPY file:169a3ea4663e2bd3f2252ce5b32f3c905cc3a0f2c3d93d1b96f38afee3b2705d in \ 
# Wed, 09 Jul 2025 19:12:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 09 Jul 2025 19:12:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 09 Jul 2025 19:12:52 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b1cf2c299ff70c52cb8ecf52e66d64d5068519867510919d8807ed2c58a54ba2`  
		Last Modified: Tue, 08 Jul 2025 21:55:51 GMT  
		Size: 122.6 MB (122630906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c6dedbd6b30fce077caa83dd1d1788f1c5969ae88a9bd7d090e3ca44938adc`  
		Last Modified: Wed, 09 Jul 2025 19:13:18 GMT  
		Size: 54.2 MB (54227113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f56f0200c25dd3cc82da41aaa226eb1123947d6728e4e542454ba79f64a10a9`  
		Last Modified: Wed, 09 Jul 2025 19:13:11 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079b9537de57d7265a4762a8f8103be7449e1e701fcc5fe363b3cd070e2c7f35`  
		Last Modified: Wed, 09 Jul 2025 19:13:11 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af36c72d297a745ce1b4c9d5ed4efaf2bb5b528094525065480fc6fe299da9e`  
		Last Modified: Wed, 09 Jul 2025 19:13:11 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
