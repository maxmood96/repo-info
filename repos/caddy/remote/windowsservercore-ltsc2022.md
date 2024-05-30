## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:c2ac2c98081daa80cbfa807745e176733338271d2c8391ece0320bf580ee177f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:6a18978ffbc393583ec9e82d2f28c38093fb2c46658d422820d3aacff72a5adf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8d0e06f90a0832497aa1f26ffa4bcdcdfa9dfc2266ed0b0dda40414664accd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 29 May 2024 23:02:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:04:57 GMT
RUN caddy version
# Wed, 29 May 2024 23:04:57 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffe20958b72548de73d2e91d2a038ee3291259fa18a8ab56bd19a2814adbb34`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d67ba9da0f386f62c69c34b92f526ec882fc0f6077990820516ae0a83f966`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 362.8 KB (362765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43dadb17334855f531328c9f050ecfc28c2c02ac3e4eac6d51a7f42c6e72696`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86bb3bd6467ecbfc6f9fe75ff873f17d80c85a850b0858d7163defce9b65e6c`  
		Last Modified: Wed, 29 May 2024 23:05:09 GMT  
		Size: 15.2 MB (15220458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6bc83565b198b6a275a4213d058c86d06203d5c6fdc953e60daf54f2a5b7ae`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0c7e36271afc841753c9b2cd4b43fe7a8a8c0a2bd6cf786bb6e15406f5c010`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231223afb2b494150472d15d93576cf24c5b60201ff0464a2a5569132b8c9e9f`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9155bc36233cfd38049c34678d8941361438f257758fd862b1b773954c553c93`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28cdc40021b08cfe18268fa3c96a8b8b9a6b039398cc237d31e5765862169b3`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f086e6518536ea0d024fc0a500a4adbc628720a51b10937b92c94a4f56ac55`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fdb5d71629385e2ff4abad1b668db6b49acf348d1db94c3c7029f955b428b5`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9500b94c744611615ef96f05a6bbcaa5f5cae79da1b2623484cdc311c915e6`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129dfc7ce699794f06660d94ffb64afbebb3ccb21e7f7dae3137bddfc9039010`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194438f949367fcd78c1f63d8c6c8fb456831be2480e496b4900893f05a313db`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969674f6c83757343cd34e24aaaeee6637008597a0d6750bff7b2316267720e4`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2383c4faaa8d33593eee6e6056dd78855b79638bb17e51738a8d647b955716f`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8560a68c3e36b65d6d38792064abbabe3f36e9d1d3bed3ee764cd8412e1a2d`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf1175073624cda6c642d3ae4f407f89695788a94c5e3beac8e942c2a87f1fa`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b50183854a011c9b2265db2d37bd80c3d292add425838b5afaeb14169b9a1fe`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 316.6 KB (316591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ec5990ce164a3773ee451372551985c1d3bb3d6f514ba8e6521883b350815b`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
