## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:8378b2f81d6e9272271d635c79caf521c72244a3a9c9367f1132889fb3235624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull traefik@sha256:fd9e012ae7c8c83981bfdb3becdba88bd3b1dfc28501aace29d5048d5fcac013
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169514236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d55d7dc4b8572b03c0df71837fbc12ff499c9b1a5b5547c3c462a5b441e84dc`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 05 Dec 2024 01:18:54 GMT
RUN Apply image 10.0.20348.2966
# Mon, 16 Dec 2024 18:28:38 GMT
RUN cmd /S /C #(nop) COPY file:4a9c1d00f4aa3b14b3bc19c47d4fc7e5a0e838dc0a22306b0e1aaf7dcd63ddd6 in \ 
# Mon, 16 Dec 2024 18:28:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 16 Dec 2024 18:28:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 16 Dec 2024 18:28:41 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.2.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f9d5d5ca3244fc2c429a892cbe6066394790f649f32d59acfdf012e490896378`  
		Last Modified: Tue, 10 Dec 2024 18:34:17 GMT  
		Size: 120.6 MB (120601318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59cc936849d3944e75da7831ec277c629a44057e54d4449471df0962df137592`  
		Last Modified: Mon, 16 Dec 2024 18:28:51 GMT  
		Size: 48.9 MB (48909810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe1a2d82684cb818c95144f5312b1e9d3ff5b28f9cd66f92f98b0ae55ec1dc3`  
		Last Modified: Mon, 16 Dec 2024 18:28:44 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1a4ea19267110c0081139a0d0f4c11f6d89248c7f766969023743eead3bdc7`  
		Last Modified: Mon, 16 Dec 2024 18:28:44 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3a532c12025e1166efbc2659a9866675c310ead17e095e1ab83da281949993`  
		Last Modified: Mon, 16 Dec 2024 18:28:44 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
