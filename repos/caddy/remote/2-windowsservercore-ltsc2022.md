## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:673a3de58869b257c604d2139842c59b86f6883268e415b4f1b97f18ded1ca27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull caddy@sha256:253379b09fd2b4c4cf14ddc66d26fccc76ca0a2f77c78c14c9c40156ba14b524
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2134160217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2d00636606e653011d99e71d920e0e4ee0157de350bb997d3d2fde20e64d52`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Sat, 22 Jun 2024 00:05:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Jun 2024 00:05:56 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Sat, 22 Jun 2024 00:05:57 GMT
ENV CADDY_VERSION=v2.8.4
# Sat, 22 Jun 2024 00:06:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Sat, 22 Jun 2024 00:06:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Sat, 22 Jun 2024 00:06:07 GMT
ENV XDG_DATA_HOME=c:/data
# Sat, 22 Jun 2024 00:06:08 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Sat, 22 Jun 2024 00:06:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 22 Jun 2024 00:06:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 22 Jun 2024 00:06:11 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 22 Jun 2024 00:06:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 22 Jun 2024 00:06:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 22 Jun 2024 00:06:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 22 Jun 2024 00:06:13 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 22 Jun 2024 00:06:14 GMT
EXPOSE 80
# Sat, 22 Jun 2024 00:06:15 GMT
EXPOSE 443
# Sat, 22 Jun 2024 00:06:15 GMT
EXPOSE 443/udp
# Sat, 22 Jun 2024 00:06:16 GMT
EXPOSE 2019
# Sat, 22 Jun 2024 00:06:20 GMT
RUN caddy version
# Sat, 22 Jun 2024 00:06:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2145505ecf961269c72a4053b3037c7fd3f0de30e204156c3e1d5fe575d5a84d`  
		Last Modified: Sat, 22 Jun 2024 00:06:26 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13756c85f9bff193779e8330ce14ca61623f69cbc25134d81193af0dbf2f69cd`  
		Last Modified: Sat, 22 Jun 2024 00:06:26 GMT  
		Size: 362.1 KB (362075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26976d0f572aa3f41d681d6e64a3e30dac8f9f2c5cb5dcea7666fc911092fa8`  
		Last Modified: Sat, 22 Jun 2024 00:06:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7320af513d1536efe2ef42fa90d966adff0d3b9a190c2fdfa056991f021ea0`  
		Last Modified: Sat, 22 Jun 2024 00:06:28 GMT  
		Size: 15.3 MB (15257562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f51cff5eeba5effe375125a9743df96371e09a3c4a60465771726357568420`  
		Last Modified: Sat, 22 Jun 2024 00:06:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a229918130246d7f339bf25586593ae279a781c71bcf1fc675b88103808d56`  
		Last Modified: Sat, 22 Jun 2024 00:06:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774f6ded77d96c08da94960ae6d2a2501288467b674068dbe6440f050fc7e5e6`  
		Last Modified: Sat, 22 Jun 2024 00:06:25 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdea6eba4835060c9e9a9110b7b57963d2dd9e5f6e24cdad068d0f35f05097c7`  
		Last Modified: Sat, 22 Jun 2024 00:06:25 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fdf49dc4132a07f8f6f8836cd3dfd3364a44b7ee316870075264091c16d0391`  
		Last Modified: Sat, 22 Jun 2024 00:06:25 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d29d1d0df234298207221488ba3181f7fce124eb6c06b4838709270bbeb6fa`  
		Last Modified: Sat, 22 Jun 2024 00:06:25 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e92e4238c9fef13f45f44ef49b40da8a34a63aae500d4c336537e81b93a3afd`  
		Last Modified: Sat, 22 Jun 2024 00:06:24 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c73fb746526eb7521dbee46c8db9581d5e9d9be3460cd0cd2e71fcf72a0a67`  
		Last Modified: Sat, 22 Jun 2024 00:06:24 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef5f35bed8efd589ceaa117c86668b736baa15c0d381071c1a701c3c291e394`  
		Last Modified: Sat, 22 Jun 2024 00:06:24 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44dbcd3474948f274c5271f333da31e69bfe85d9c92aa8b9ba3c8d756fd2fe6`  
		Last Modified: Sat, 22 Jun 2024 00:06:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b921abad0a235059e51f731fe9b4d2ae510f2947cb41974129869246e362d938`  
		Last Modified: Sat, 22 Jun 2024 00:06:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241215d7eb62f3cbc5d49f1a9070f5308dde368919ec8c6c9647340e787356aa`  
		Last Modified: Sat, 22 Jun 2024 00:06:23 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2552f135b0ccdb93e308102ab43b2a46bd845fb61b0f50046fdbe246066d627`  
		Last Modified: Sat, 22 Jun 2024 00:06:23 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6179786efc935347b140cd325239f0202ae12179fe70bd054b0b6ff0396f79e`  
		Last Modified: Sat, 22 Jun 2024 00:06:23 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb8269a50111e081ea24b7414f5ea472de8e9d7983e3a6b4469da57e380dbf4`  
		Last Modified: Sat, 22 Jun 2024 00:06:23 GMT  
		Size: 328.4 KB (328403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25d7536e77eaee2e6914b6b487bb787bebc1556b6b97e10d9597b02f802abba`  
		Last Modified: Sat, 22 Jun 2024 00:06:23 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
