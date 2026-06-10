## `traefik:v2-windowsservercore-ltsc2025`

```console
$ docker pull traefik@sha256:ee1a6e8549ef565047ece00a5bce4f00d8e4180be196c0bf817e7b1abb1b6766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `traefik:v2-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull traefik@sha256:06ad0f291eb558c787f638ccacbffb2a1df684515d0b3bd07ecd8d12360f117e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329185656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b730afed2bc4f4bb76c23ebcc9f121895e1882f4b156005e085ddb4435a838`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Wed, 10 Jun 2026 18:07:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jun 2026 18:10:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.50/traefik_v2.11.50_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Jun 2026 18:10:07 GMT
EXPOSE 80
# Wed, 10 Jun 2026 18:10:08 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Jun 2026 18:10:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.50 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045e7ebee4bb03acac5364df00dfc993bdf486e074f69ea697b75f4c609e9b5e`  
		Last Modified: Wed, 10 Jun 2026 18:10:19 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bccb87da3aa793f2eb6e3fbe391c63ece5db22dafde57991256857053aefb1a`  
		Last Modified: Wed, 10 Jun 2026 18:10:26 GMT  
		Size: 50.0 MB (50037429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43131f1665a3e09d00f5d0e74ea3d091963189da47d57dc298eb9eda5e4dd247`  
		Last Modified: Wed, 10 Jun 2026 18:10:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a723a2675f44c6fb30ba6e5a0005f3ccb37f1477c9553aad17cc86a1470e4a7`  
		Last Modified: Wed, 10 Jun 2026 18:10:19 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6b80c93c6ed6e5ee3639ed8eea1df2cc83516d239375dc2da54701373a5098`  
		Last Modified: Wed, 10 Jun 2026 18:10:19 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
