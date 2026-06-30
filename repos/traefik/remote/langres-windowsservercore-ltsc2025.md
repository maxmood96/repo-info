## `traefik:langres-windowsservercore-ltsc2025`

```console
$ docker pull traefik@sha256:abc33f26063d0a53c173d6928724f1f90e052b0ac477004a33c81ac9614bf82e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `traefik:langres-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull traefik@sha256:b88bd45248d7874b0d510fa60ad97a91b9c43523c5349796608bb93aecb9475f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329648821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9cc65741c23ffa4f49a6d8706bd07763e0e2196ad08378804b80df649bbc5b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 30 Jun 2026 20:40:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 30 Jun 2026 20:41:48 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.7.6/traefik_v3.7.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 30 Jun 2026 20:41:49 GMT
EXPOSE 80
# Tue, 30 Jun 2026 20:41:50 GMT
ENTRYPOINT ["/traefik"]
# Tue, 30 Jun 2026 20:41:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.6 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:395309c1248f014724e832731ec584b4b2bd3a1df0e9076bb6f3365a8c7e0a82`  
		Last Modified: Tue, 30 Jun 2026 20:42:04 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58a687e68f03ebcc009d8a80eaeb42ca9d2a5ee3e778bf42e331b95e0628364`  
		Last Modified: Tue, 30 Jun 2026 20:42:12 GMT  
		Size: 50.5 MB (50500584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6469ed36724004e34d5dbbbe812d682e1a14b4fcd9f612ea88304e1f79f87688`  
		Last Modified: Tue, 30 Jun 2026 20:42:04 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f1b2afaa0abb1edb6a1a64b3ac689b047a3f7527362c1853ea5af2930b726f`  
		Last Modified: Tue, 30 Jun 2026 20:42:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279e391fdbd70dcd6f9f1fc5f25b2aaf4170d8e986fe56f2a56852802595de30`  
		Last Modified: Tue, 30 Jun 2026 20:42:04 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
