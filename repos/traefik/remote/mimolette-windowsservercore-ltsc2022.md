## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:2dca81380c754154e1b1c0631de5f8e56126eec1409cd9dbaa6ac8917439218b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull traefik@sha256:27ecf1b8730643f8fda31322e2c88e1cf5d97f28d3417ba95f285532798a1a09
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186097159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f198df98d864e1fe5d3b6dcc644144dfa6488669a644314deec6abc7f8a5588f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Fri, 06 Sep 2024 20:59:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Sep 2024 21:00:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.8/traefik_v2.11.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 06 Sep 2024 21:00:54 GMT
EXPOSE 80
# Fri, 06 Sep 2024 21:00:55 GMT
ENTRYPOINT ["/traefik"]
# Fri, 06 Sep 2024 21:00:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d838cd3f383a400021eee8cbff925b28363f7e029a0f9d71c1f8a65bd6e8df0`  
		Last Modified: Fri, 06 Sep 2024 21:01:00 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81df675df228cfbc3dcecabe502d9fd98cc8b023c37ca49b2911ada5a16604ed`  
		Last Modified: Fri, 06 Sep 2024 21:01:05 GMT  
		Size: 44.3 MB (44326986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ba6e3c58b475555d8290bdd2a92a78d5905982ce3fc3589fa60f5d0d61eed`  
		Last Modified: Fri, 06 Sep 2024 21:01:00 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3238a3b00035541fc0a400dfc92d098021b278d65978c28483bc32b08537dc5`  
		Last Modified: Fri, 06 Sep 2024 21:01:00 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31714f731529fedf64e43214ac06f1cbc0bd8e4b4b7d02eb97d9137274ca35e`  
		Last Modified: Fri, 06 Sep 2024 21:01:00 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
