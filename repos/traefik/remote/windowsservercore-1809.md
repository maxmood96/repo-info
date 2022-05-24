## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:9cc1fc96a29434e876cd844956058fcf251880a00491631ab40e1b7bfd17ea65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull traefik@sha256:3532cfd35349328b4a15d09000a1a48f8c23897b07934d8461917ff8c7cb9dc5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2532220952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5ce5f8ef5fcf2dff945182af78103d1ef9419c10fc1effd78fc8838fee5acb`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Tue, 10 May 2022 17:40:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 24 May 2022 19:16:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.7.0/traefik_v2.7.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 24 May 2022 19:16:34 GMT
EXPOSE 80
# Tue, 24 May 2022 19:16:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 24 May 2022 19:16:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c8a0a0d5642a312541382f8fd8cc5463eea7b9c29d4f71cd1c2592aa0e22160e`  
		Last Modified: Tue, 10 May 2022 18:17:19 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceda28be92f24dac77b9cc8f58e4045cbe58a3f8c7af7208cce204b17a20df41`  
		Last Modified: Tue, 24 May 2022 19:18:40 GMT  
		Size: 28.2 MB (28159383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b0477a83d8980fdfb79b288a40002cbf9e138fb8133f05100f4075b7fad6f0`  
		Last Modified: Tue, 24 May 2022 19:18:33 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f00623df4801a2288518a3ac402be1093b6f0678463222fb5f4a64a5a9f715b`  
		Last Modified: Tue, 24 May 2022 19:18:33 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e6d787195dfc001d7ed79ac049b2628394ececad7a9e59b0bac29e046eeaa5`  
		Last Modified: Tue, 24 May 2022 19:18:33 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
