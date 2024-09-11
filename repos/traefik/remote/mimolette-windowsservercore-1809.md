## `traefik:mimolette-windowsservercore-1809`

```console
$ docker pull traefik@sha256:60cc6d999c00df4208c386c97d9b0f6f7e21948f250fcea925d286a219cbcd78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `traefik:mimolette-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull traefik@sha256:f95bcbcd60981280adc7e4b0fdfafb2d5567722ac79f8c9bc3a877aa028d1acc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1764566493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616b536457e75492f37de4ce9fb66babab2d9e63760047ca3928e328da90578f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:03:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:03:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.8/traefik_v2.11.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Sep 2024 00:03:41 GMT
EXPOSE 80
# Wed, 11 Sep 2024 00:03:42 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Sep 2024 00:03:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ca2b53efe7ce5877cbe591ff85f37c66f26c87cbf238d9cf624dd35da0f782`  
		Last Modified: Wed, 11 Sep 2024 00:03:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4807e943837fdce7787be82281f08cb2847ba708e894488fb9f79511c7d847ad`  
		Last Modified: Wed, 11 Sep 2024 00:03:52 GMT  
		Size: 44.3 MB (44292948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006d13249cd3b7e32c6bd162a7a259d36e4f651188ca44a7897722735c4d86c2`  
		Last Modified: Wed, 11 Sep 2024 00:03:46 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8581d74ff33d10a6cb2262549b66b2d352c75a2a41d989d28f9feab41236211`  
		Last Modified: Wed, 11 Sep 2024 00:03:46 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3635d025de4084631cd5ca6e3b1bf43f562479861f9b48f9f84adfd2d0cd00`  
		Last Modified: Wed, 11 Sep 2024 00:03:46 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
