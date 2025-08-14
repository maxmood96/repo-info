## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:d9fbfe64e0392838e3c26b5f42abfb2c4dd022c070fd6cbde87dc39508563c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:83dd1151b9ecc6779d8aef7c89fc758ebb2218579125cf6648d5faff5aa6437a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298038256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420223ec99237a574c8efbd800fe16f33d04fbebca6bc65d111ae296fcd72da9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:35:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 Aug 2025 20:35:20 GMT
ENV CADDY_VERSION=v2.10.0
# Tue, 12 Aug 2025 20:35:29 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cb97adb2bff5de752e470486ae72d55a6ddcfe4bfa43f09ed849260955df7f61385ac1e2d28fc80458b6910d71fa38d4295bb0689263dcc1743f2050d847c2ad')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 Aug 2025 20:35:30 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 Aug 2025 20:35:31 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 Aug 2025 20:35:32 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Tue, 12 Aug 2025 20:35:33 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 Aug 2025 20:35:34 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 Aug 2025 20:35:35 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 Aug 2025 20:35:37 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 Aug 2025 20:35:38 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 Aug 2025 20:35:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 Aug 2025 20:35:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 Aug 2025 20:35:41 GMT
EXPOSE 80
# Tue, 12 Aug 2025 20:35:42 GMT
EXPOSE 443
# Tue, 12 Aug 2025 20:35:42 GMT
EXPOSE 443/udp
# Tue, 12 Aug 2025 20:35:44 GMT
EXPOSE 2019
# Tue, 12 Aug 2025 20:35:49 GMT
RUN caddy version
# Tue, 12 Aug 2025 20:35:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225ce48837d104264ddb5fc63df8bdfb2048f18fb07f80e338f435e6d5c245d4`  
		Last Modified: Tue, 12 Aug 2025 20:37:35 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06de9f985b6e54bd6982dde5f6eab7fb30edee56efea6599cfba67883d60913e`  
		Last Modified: Tue, 12 Aug 2025 20:37:37 GMT  
		Size: 358.3 KB (358275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5395eaaf55e87f1dcf3bc53c470a466a3c2b686a10ffa67b7a34fc1e9ae5c455`  
		Last Modified: Tue, 12 Aug 2025 20:37:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a310ef8241ddb2e190225015ec074c39ee1bd92f4a0d16b982206d146117674`  
		Last Modified: Tue, 12 Aug 2025 20:37:39 GMT  
		Size: 15.6 MB (15616687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122bd471691cea70b7ec98377929285e4017b986095ac29387dca37eab17858d`  
		Last Modified: Tue, 12 Aug 2025 20:37:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01c1e73de8533515c7c676d4e703d431caea9da35394a5a577ad5fdde5d7e62`  
		Last Modified: Tue, 12 Aug 2025 20:37:38 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3a304d1be1813894472244c769d75cb098e7298cf6eb49c55fd2c0a4238b87`  
		Last Modified: Tue, 12 Aug 2025 20:37:37 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5566c34f5f72aeb34d135f5b0bb03c222d8cf4a7294d7728f28ee23c757553`  
		Last Modified: Tue, 12 Aug 2025 20:37:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8927d217022fc8835a437effc68b05ffdb2b86996f7611e9e673635c95aca6`  
		Last Modified: Tue, 12 Aug 2025 20:37:37 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713c82d43f38b994235709b6b026dd0ff816323196da1f4f4183cccdbd62e083`  
		Last Modified: Tue, 12 Aug 2025 20:37:37 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ae87ab6fe7475b1dd979bd33b49554374c19ecea4e0d206ded49729812b5c3`  
		Last Modified: Tue, 12 Aug 2025 20:37:37 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda205cda42bfa32d41fce67c74512027ddb90424507585ccba70d9ee96f6395`  
		Last Modified: Tue, 12 Aug 2025 20:37:37 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649b1c254e39d0d3eab6caacd96f151d0996101f5ff194700a9e6aded1f0d678`  
		Last Modified: Tue, 12 Aug 2025 20:37:37 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc83f4cc54b950e19221a4054f44b225fe6206a77abe5e460b73328fa843f8ae`  
		Last Modified: Tue, 12 Aug 2025 20:37:38 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba4338ccace1a4846d4a9d097cead0992ef91a60e0a3481d393598b0c71e278`  
		Last Modified: Tue, 12 Aug 2025 20:37:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6db602f00e50e112ba4d69549a97fa3907584b81c7d7d94bbe6c6f0f114a066`  
		Last Modified: Tue, 12 Aug 2025 20:37:37 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61693f2d3e65fc0cee677ddd7aba0e4c5198ac6d53e22c248677c1499606e19`  
		Last Modified: Tue, 12 Aug 2025 20:37:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638edb9999bd0e43f4ddbfeb8b937ded57db2bebca5acc10bc2b0a8fdf38685c`  
		Last Modified: Tue, 12 Aug 2025 20:37:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab01157572e0ed3555878e0fb9e3834033f2fac728955fe4d9699da281162f76`  
		Last Modified: Tue, 12 Aug 2025 20:37:39 GMT  
		Size: 349.4 KB (349404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ff32f07648fbc5f82974610dd2aecf61c521ba386e7cf8507804c461a60121`  
		Last Modified: Tue, 12 Aug 2025 20:37:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
