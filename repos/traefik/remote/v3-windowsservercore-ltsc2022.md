## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:2bcfd0b92a9cdba325bce6b6a5bcbf01679c3f6596da445605d8df396f3cb426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull traefik@sha256:00debb02a93bc71dd80739135325f6ca5bae8a3a34ce8b7ccfc9d5b08604fc59
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2301911599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a239d0d3708511c83d8bd63ed23a77b14919067b704d32a0e8bbce2c84cd4de0`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Tue, 10 Dec 2024 20:27:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Dec 2024 20:28:29 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.2.2/traefik_v3.2.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 10 Dec 2024 20:28:30 GMT
EXPOSE 80
# Tue, 10 Dec 2024 20:28:31 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Dec 2024 20:28:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.2.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcb014086282910e361bf05c280719d499aa93dd349f6498f7bc5ce41cc0a20`  
		Last Modified: Tue, 10 Dec 2024 20:28:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40dfb8dae4af9ed46d59a60b3d6686a995ea437d485818f292eeef618841974`  
		Last Modified: Tue, 10 Dec 2024 20:28:40 GMT  
		Size: 49.4 MB (49422232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228e9bdef33e628d6820aae20941bc51a8838475c4284762908662ab2a0202b8`  
		Last Modified: Tue, 10 Dec 2024 20:28:34 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c8ae9793fa07a08548dd38363ea3c688774e265dc52f51168808dd9cade335`  
		Last Modified: Tue, 10 Dec 2024 20:28:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2050eda198b3110bef4a31f080bf9f01985ee63583518b8ad63655eec6d450f6`  
		Last Modified: Tue, 10 Dec 2024 20:28:34 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
