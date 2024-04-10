## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:6713488700839c523e0560fffd3c75c9cc5dcd2377238b2c64d386517aba75cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:f5c456da18453e1eb009e9c3617d0a7f33abf3ec8288fbc257d419b7dabf7be2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2041714363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80fc70cf10c52c295796b45a099f6864f465f18c4a626065fbbf491cf5fa108`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 18:19:50 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.1/traefik_v2.11.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 18:19:51 GMT
EXPOSE 80
# Wed, 10 Apr 2024 18:19:52 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 18:19:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7fe10f81aa64a4d4c857c16a8103840b868532450a2cf40e7984011546f579`  
		Last Modified: Wed, 10 Apr 2024 18:23:32 GMT  
		Size: 42.3 MB (42335049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e086039e87a01cca00d697b8cf948f73b77c0586360c9c14db03ac52c2ba712`  
		Last Modified: Wed, 10 Apr 2024 18:23:23 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b40de7fe203e3823ae5b80570182563d7f7b865efc21e09968ad7202e8dac3d`  
		Last Modified: Wed, 10 Apr 2024 18:23:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e9d4dc98185f884781a3206ee9abeaa8ad971667f3fa910a27bee065c5ee79`  
		Last Modified: Wed, 10 Apr 2024 18:23:23 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
