## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:ec994d877f87622e6e0fe82b0ea8e3b3efabf1e0d8c57fe110f822b211243c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.4131; amd64

```console
$ docker pull traefik@sha256:38c71b3285dd02b9aa56ad826495f85e854606a04db526dcf7bf770ca9936a20
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2049781176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f645f991b33f438d120607abe7a2a158d8300068ceb916e0d7a6d2eaa095526e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Sat, 11 Mar 2023 10:37:22 GMT
RUN Install update 10.0.17763.4131
# Thu, 16 Mar 2023 00:41:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 Apr 2023 18:17:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.9.10/traefik_v2.9.10_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 06 Apr 2023 18:17:04 GMT
EXPOSE 80
# Thu, 06 Apr 2023 18:17:05 GMT
ENTRYPOINT ["/traefik"]
# Thu, 06 Apr 2023 18:17:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92048040b3b13af10f8287baabaddbb2759dfc77b1fb43f89b38b3275467f93`  
		Last Modified: Thu, 16 Mar 2023 01:42:29 GMT  
		Size: 305.6 MB (305565048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8e4e0836091bdd33e8adb56d1e13b8096550727a20534e2a2ab9298c86fa09`  
		Last Modified: Thu, 16 Mar 2023 01:41:16 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b184b38bee4a888e16184a05c4770d36d87ad320077cbee08f12000fd700abed`  
		Last Modified: Thu, 06 Apr 2023 18:18:10 GMT  
		Size: 36.3 MB (36266505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32de5c550068bdd6a0e71f6aaae2c5ba100294dbb52006ca1247bc09cfb87e17`  
		Last Modified: Thu, 06 Apr 2023 18:18:00 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8b65f112c430971f5c46a3133c30bd210125ddcf9493bca90d0553685871a5`  
		Last Modified: Thu, 06 Apr 2023 18:18:00 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8510431814f07a8c701f707dabf5daf9283df8769147fefe8634a06b3edf2a`  
		Last Modified: Thu, 06 Apr 2023 18:18:00 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
