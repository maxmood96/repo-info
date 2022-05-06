## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:6981021d22ae2b424d7b900a922e503937ec9adb962fceb0a562a9d528214048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.643; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.643; amd64

```console
$ docker pull caddy@sha256:4891c547e59ee06c3f36f38a6cf0d3854f666cf3a7102905a4f85a6b06eb10b7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2242218231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f11abe3323e9d5a83d1c02165ee78ad8288270f75ed2835f3486e093747c79f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 May 2022 19:19:44 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/69bb1c539b3ee03fc91271a71653a77ca1e9d131/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/69bb1c539b3ee03fc91271a71653a77ca1e9d131/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 06 May 2022 19:19:46 GMT
ENV CADDY_VERSION=v2.5.1
# Fri, 06 May 2022 19:20:19 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.1/caddy_2.5.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4294796c4bd4bed0c593d83606a5413de30f35f88d624e1b1e5b6cd8672ffbcc7a689d7ce4ef30c1abea0e95eda62220faac15d2a6aca0c3e2b418abe7a74118')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 06 May 2022 19:20:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 06 May 2022 19:20:21 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 06 May 2022 19:20:22 GMT
LABEL org.opencontainers.image.version=v2.5.1
# Fri, 06 May 2022 19:20:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 06 May 2022 19:20:24 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 06 May 2022 19:20:25 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 06 May 2022 19:20:26 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 06 May 2022 19:20:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 06 May 2022 19:20:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 06 May 2022 19:20:30 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 06 May 2022 19:20:31 GMT
EXPOSE 80
# Fri, 06 May 2022 19:20:32 GMT
EXPOSE 443
# Fri, 06 May 2022 19:20:33 GMT
EXPOSE 2019
# Fri, 06 May 2022 19:20:53 GMT
RUN caddy version
# Fri, 06 May 2022 19:20:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08302266da05c1f24af487663c0bedd823c99dc6b45b75cdff92e100785cafb6`  
		Last Modified: Fri, 06 May 2022 19:24:18 GMT  
		Size: 638.2 KB (638209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a58fd60b60c3e652ed7807026b51f90c4659bd57acfa5cd77eca6416d227076`  
		Last Modified: Fri, 06 May 2022 19:24:18 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e18635f42ebe6e9400dc3cc7ece88e2e2491ef5f53517ba24b11970dd44127`  
		Last Modified: Fri, 06 May 2022 19:24:21 GMT  
		Size: 14.2 MB (14244843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafbf6694f9ca3ac86a12b32246617e0d8d1807fdcaafdf9a12d342a8e36aa5d`  
		Last Modified: Fri, 06 May 2022 19:24:16 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563c0c8b1a1a772a3183d87ca3f21168dabc632d6acae039334516c7a0d14514`  
		Last Modified: Fri, 06 May 2022 19:24:15 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c8d74501d1dd33a957f817765f1551bbfe7c09a4012889d42b002043ce11b1`  
		Last Modified: Fri, 06 May 2022 19:24:15 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6894b6429bf42747bbc27e01fc8e78b730aa5816b1794a2ab2cdc96da8e09bff`  
		Last Modified: Fri, 06 May 2022 19:24:15 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65d72a2f1f58ed2ea9b4f1f2ebee2236c628e4589c7b6e962953f2d66565ecf`  
		Last Modified: Fri, 06 May 2022 19:24:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9093a3f434d5ca5240f51e45e6889d3ed7d33b2e6694c6f923253b84dbeeafcb`  
		Last Modified: Fri, 06 May 2022 19:24:13 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1165f546a7a4f921eccc7537b7b8bb93602a1d2a39e74cfa77ef39391377db5`  
		Last Modified: Fri, 06 May 2022 19:24:13 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae632f2a81a034824c2a2f5b0cc37bc7ac9ebd885e8c67561a989cc8938beb24`  
		Last Modified: Fri, 06 May 2022 19:24:13 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8cd2d094652c0a732948eec9e46871a4c92bb0ebce46ce30b36b940e946bcc`  
		Last Modified: Fri, 06 May 2022 19:24:13 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9488f78327df74a4100bcc318a1b8c3a1f3f9b01ba51103bfa280ea1463f63`  
		Last Modified: Fri, 06 May 2022 19:24:13 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc812ed21e0fc83cbf6ac270b74877d05e19df1758c7ec66b0bed7fe64a230af`  
		Last Modified: Fri, 06 May 2022 19:24:11 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f866e3b4267926d6876eee95f1b6b78d42b173b63fc7086d4595e5716efd05e3`  
		Last Modified: Fri, 06 May 2022 19:24:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706ff642e0cfb73863dbb5537a3c529f317363a2945322ea9dbd997d5d6577f1`  
		Last Modified: Fri, 06 May 2022 19:24:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1156a4bf93ba03ba5b6010733740f99ed47ff4b2c7779149bd49b9887d821b`  
		Last Modified: Fri, 06 May 2022 19:24:11 GMT  
		Size: 357.8 KB (357828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9848d2aaaedc3fcb62b2b98199351fe3f1ab8f9bd5a5d576842fe7dbe7d963d6`  
		Last Modified: Fri, 06 May 2022 19:24:11 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
