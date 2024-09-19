## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:dbbd39c32f1e2f7e01b224ff92dad86a8f852bdd47cac17e85ead6e5704bef5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull traefik@sha256:ea4e7884a07562792d37f7a2935909e91a42c52c080baeb1274dc204663bfaa7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164456536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a44080d4af960ab44d9b709223f69f127034cd77cae70817cb10ac1eaba67b`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 05 Sep 2024 23:48:03 GMT
RUN Apply image 10.0.20348.2700
# Thu, 19 Sep 2024 17:49:30 GMT
RUN cmd /S /C #(nop) COPY file:dd7ed9b2fbf9bd90b8a02a01f8c98cfed43d2b89c86b122c251aec625d07f8a0 in \ 
# Thu, 19 Sep 2024 17:49:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 19 Sep 2024 17:49:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 19 Sep 2024 17:49:34 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a447243899be39b01c34fc7e1bcecb47ce42b14668876fdd121f8b5e2d4d4a86`  
		Last Modified: Tue, 10 Sep 2024 22:28:02 GMT  
		Size: 120.5 MB (120509521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8352bdf4b35b248ad3ec7481d610e531556bf37a547b777f225a55a796e0ec0`  
		Last Modified: Thu, 19 Sep 2024 17:49:43 GMT  
		Size: 43.9 MB (43943934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3639d850ddd3b7eb8393dfd78701df1b96093466839f97b4d8174349585a9c`  
		Last Modified: Thu, 19 Sep 2024 17:49:37 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c5c436aa79a1bb3c67aa5983482f2f0db554123986ecd9d1c522cfa1df04bb`  
		Last Modified: Thu, 19 Sep 2024 17:49:37 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a190a816f9737f572d704107850ad233008c6233ae7bc8e477420e04f3a4313`  
		Last Modified: Thu, 19 Sep 2024 17:49:37 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
