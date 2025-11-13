## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:aae61788f09632acda1661d4b8f0039f06eaec12a701472695359c7a558d2b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2425040de232b4cf1e501dc9cdd6d41eba06e8b9b4ed21567e77cabc5af660a6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173791425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aade119d4b861c64935ccab38b6f95b9b11902339794dd0efda73b7ee46547b`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:16:12 GMT
RUN cmd /S /C #(nop) COPY file:538c737733185d849e52445ceb96a70617c3af70afe4dbb5098c99241fd9e5ca in \ 
# Thu, 13 Nov 2025 20:16:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:16:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:16:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a21b752eabead63b7e7b00c2f75e92023d4c4bf19e0a0553b4b862fcc08b64`  
		Last Modified: Thu, 13 Nov 2025 20:16:56 GMT  
		Size: 47.4 MB (47439167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db78d6f4429872e31d3bf74c6e476dcd4f000ff0fa7e1c54e9412734616acc38`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e87288450ccf7480a3d43579bac23ad32a78057dae732166ea3f1f7d8843bb`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f7f7c5f1bce20ad2fbacf0fb555a564ee4f41af53f6c10b308cf39491cc6e0`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
