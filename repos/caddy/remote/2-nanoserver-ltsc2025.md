## `caddy:2-nanoserver-ltsc2025`

```console
$ docker pull caddy@sha256:3db4a3d99457a9c0738e1cfcf46aba5598dc87ad7b36198830bea76a073683da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `caddy:2-nanoserver-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull caddy@sha256:debe284b9e73f8001607af97887c3179518f3ae05e2089875e067927a39e7b5f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214865983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c4149388db8a6181c6f50794ff0d97d30105c7675c90f04719ac1a5efdaeb1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Tue, 09 Jun 2026 23:21:56 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Tue, 09 Jun 2026 23:21:58 GMT
RUN cmd /S /C #(nop) COPY file:7d2f419889d1c745e8d01a18ec688d43a6c8f6363f61c1964c7e88fd70b1b987 in c:\caddy.exe 
# Tue, 09 Jun 2026 23:22:01 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Tue, 09 Jun 2026 23:22:03 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Tue, 09 Jun 2026 23:22:04 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Tue, 09 Jun 2026 23:22:04 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Tue, 09 Jun 2026 23:22:05 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.4
# Tue, 09 Jun 2026 23:22:05 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Jun 2026 23:22:06 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Jun 2026 23:22:07 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Jun 2026 23:22:07 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Jun 2026 23:22:07 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Jun 2026 23:22:08 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Jun 2026 23:22:09 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Jun 2026 23:22:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 09 Jun 2026 23:22:10 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Tue, 09 Jun 2026 23:22:10 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Tue, 09 Jun 2026 23:22:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Tue, 09 Jun 2026 23:22:14 GMT
RUN caddy version
# Tue, 09 Jun 2026 23:22:14 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37b0be4bd77ffeb8d4d05ea7bd50fd51120e6c65761b71ed6f1c1fed23540c2`  
		Last Modified: Tue, 09 Jun 2026 23:22:24 GMT  
		Size: 71.9 KB (71885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c82059a2088a5a70556199e145e7a97a30d379a44da9d8cc307a4263ece7ed`  
		Last Modified: Tue, 09 Jun 2026 23:22:26 GMT  
		Size: 17.6 MB (17619896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e2158f5372809bc6d4c826f3e10637b691c6ca9c3be8df18ec9f0902f96809`  
		Last Modified: Tue, 09 Jun 2026 23:22:24 GMT  
		Size: 267.6 KB (267558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438e61381d0ad68de58775a38849654ca47a1ea1a6310eced53491a622299d1d`  
		Last Modified: Tue, 09 Jun 2026 23:22:24 GMT  
		Size: 112.1 KB (112103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:771fb040f0b2ddbe7d1209d723992a2f3ad4685f06502ebeed84a546a57dfe49`  
		Last Modified: Tue, 09 Jun 2026 23:22:24 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7150eb1beed03114414658dc904e08691facf15c3f2a7366fbb7a1b58041a335`  
		Last Modified: Tue, 09 Jun 2026 23:22:22 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9b87fc66caf9546fc3396ff1ab0f3344d15a0ffc72458a97d5f9ef8ad5cb32`  
		Last Modified: Tue, 09 Jun 2026 23:22:22 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8972068130947c03bc9271be9bfa6651c67572986c537c845b8ef2c947eca33`  
		Last Modified: Tue, 09 Jun 2026 23:22:22 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9541831730e5f24b50543a16d9c0b8a19a869c7d3bd5cd0520c27d72c1e78289`  
		Last Modified: Tue, 09 Jun 2026 23:22:22 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfcd9790e557698c750aed053e74e46b9163dacede68f974d66da8f61162190`  
		Last Modified: Tue, 09 Jun 2026 23:22:22 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868eb12cf5470424f81eead6dab87de3f785eae174751deb05617197768fc817`  
		Last Modified: Tue, 09 Jun 2026 23:22:20 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a832ad1014aa05c0621a33c0c4b73e5906e8458d635ac96e9b2274da337b4a9`  
		Last Modified: Tue, 09 Jun 2026 23:22:20 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d542359496b94347188c50dd60ef609ab58537a82c71bc0aac2b87b3320b847`  
		Last Modified: Tue, 09 Jun 2026 23:22:20 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f69b7023faa1758aee780bc36be2ff45bf92cd3073c6a2533324a4a3a5ec08`  
		Last Modified: Tue, 09 Jun 2026 23:22:20 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7a332e94794e91d054bb0d6945dc7cd1748966ad75f544c2286aab47184a7d`  
		Last Modified: Tue, 09 Jun 2026 23:22:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e80388c9151dd28d66aabbdcefdee9039c2deed6dc20272a9144fc277ba84`  
		Last Modified: Tue, 09 Jun 2026 23:22:19 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066cc56fa9d183788775f8680cb4d684e3ffd1d77535fb9ea1d9131de79116ca`  
		Last Modified: Tue, 09 Jun 2026 23:22:18 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c917147f481dda79a23746f10c4574489e183e65fc966df01e835140f2182af`  
		Last Modified: Tue, 09 Jun 2026 23:22:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d66699f6bbb54f16b6f181fc9ec4fa5c8c7a4e3d00cb42a78654eff6a9abfb`  
		Last Modified: Tue, 09 Jun 2026 23:22:18 GMT  
		Size: 111.0 KB (111022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3724ea3fa2e7f81270018de5a06a24b31f45e5011ceb9a1030e668696d7783bf`  
		Last Modified: Tue, 09 Jun 2026 23:22:18 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
