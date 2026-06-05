## `traefik:ramequin-windowsservercore-ltsc2025`

```console
$ docker pull traefik@sha256:a5047cbf4ad4d4da2cd161494033617e2f1197af9e39d37ecf5eb4ab7aebbcf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `traefik:ramequin-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull traefik@sha256:6b538f1a714e3fec6a7ea6e3acad7f514414ec8fa0376f714ed163230f276090
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2255927332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62e65c80ba143617598cf83af7de0f1a66cc3a3c5e5f0b7310ecd9c5fe1b93c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Fri, 05 Jun 2026 17:27:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 05 Jun 2026 17:29:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.20/traefik_v3.6.20_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 05 Jun 2026 17:29:10 GMT
EXPOSE 80
# Fri, 05 Jun 2026 17:29:11 GMT
ENTRYPOINT ["/traefik"]
# Fri, 05 Jun 2026 17:29:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3776593c0e1b07a2a6a4c0424b206ae03420c3bbc6a4e197d1df2953858c94f4`  
		Last Modified: Fri, 05 Jun 2026 17:29:20 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd6ad3988e176fa5e8fb505dbbe3be5c53d25011621f927f672e0e9e8e5093c`  
		Last Modified: Fri, 05 Jun 2026 17:29:44 GMT  
		Size: 50.0 MB (49980287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d546b18753cd0f8b558d9b7d40a79f9307b75011296d993ee5bba629d07846`  
		Last Modified: Fri, 05 Jun 2026 17:29:20 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af50a5b26b115c679c4bca2093260427ced5a4f30537348f082235f49eb29084`  
		Last Modified: Fri, 05 Jun 2026 17:29:20 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722cecd0d52011e2b17ad225efa63ddf5ad0f51798e08926efc8625f044275dc`  
		Last Modified: Fri, 05 Jun 2026 17:29:20 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
