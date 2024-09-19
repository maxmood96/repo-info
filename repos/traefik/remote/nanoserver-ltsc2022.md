## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:579dd21f7b972bcd0061d2fe894dd0bc0120e6986ce0e7b066c53bfe0ef9abc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull traefik@sha256:86bdc5a105057ba82713f281a9128a5564574d09264c483b724ba5667c7a442c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166009286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d39a75a02f0235a6e7cefba112921217e18d6f3247721c4aa03cf21dadda9e`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 05 Sep 2024 23:48:03 GMT
RUN Apply image 10.0.20348.2700
# Thu, 19 Sep 2024 17:50:01 GMT
RUN cmd /S /C #(nop) COPY file:8e6225f1589e2f585b290fcc0eb57e9d83ba3c0b079fab70457b18c3f54f1ac5 in \ 
# Thu, 19 Sep 2024 17:50:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 19 Sep 2024 17:50:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 19 Sep 2024 17:50:05 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a447243899be39b01c34fc7e1bcecb47ce42b14668876fdd121f8b5e2d4d4a86`  
		Last Modified: Tue, 10 Sep 2024 22:28:02 GMT  
		Size: 120.5 MB (120509521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed04404d61e298e2ee3844a3dfa075468b7940a436cf847a6120518857df76f1`  
		Last Modified: Thu, 19 Sep 2024 17:50:14 GMT  
		Size: 45.5 MB (45496676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666be415ae7284a9e6efecfdea347a28c55b096377bf5b930f39235043c1328d`  
		Last Modified: Thu, 19 Sep 2024 17:50:08 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b547422da8e511e32fa8186c3846fc589bccf78e65bb2e02f8e1f39402994bd7`  
		Last Modified: Thu, 19 Sep 2024 17:50:08 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8646c723a87a8decb00ec08317cd83ffab1f53efae7a0e6fe00d31605a3f2861`  
		Last Modified: Thu, 19 Sep 2024 17:50:08 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
