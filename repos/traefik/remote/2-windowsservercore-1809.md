## `traefik:2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:0e9706f6a3b28e8bb64bbf6d7d4e58a76b6575ca1437ad6d8689269aa8674a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `traefik:2-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull traefik@sha256:0ca7475a621d7495c3f7289f6b48e185f3b7180554a3cf7523aa7d1c0874cac5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2217697619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bcab543764efb6c6befe48ee07ee8bb07a6ade39886ee1ee07b24b5df59fad`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:23:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:24:46 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.22/traefik_v2.11.22_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 18 Apr 2025 03:24:48 GMT
EXPOSE 80
# Fri, 18 Apr 2025 03:24:49 GMT
ENTRYPOINT ["/traefik"]
# Fri, 18 Apr 2025 03:24:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.22 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5c06beb543fb7621fef29658db9da8837336d169f96d071c647ceb72ce64e8`  
		Last Modified: Fri, 18 Apr 2025 03:24:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8370a2431275d70ebc256d9d268be4a43662571d6536a6bf495e665a06606be`  
		Last Modified: Fri, 18 Apr 2025 03:24:58 GMT  
		Size: 52.2 MB (52166638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658fb355e535c027e5105410071c48254bed3bd1cabf7871a9ba3a834728420c`  
		Last Modified: Fri, 18 Apr 2025 03:24:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc2241206cb0d126a6f2f3dff944f21e596547b66620bceccf00e164a62b192`  
		Last Modified: Fri, 18 Apr 2025 03:24:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241dba6bd90865df4e3cc8b813d74613a5ef4df3ee933549e50d3ead74e9b92c`  
		Last Modified: Fri, 18 Apr 2025 03:24:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
