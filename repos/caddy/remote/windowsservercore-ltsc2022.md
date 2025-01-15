## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:4d4fc4b1242a7788c646c9d733cf131cea76ed6ee655570a41d2ea783cb56e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:56c41ce28bd71deed123237c5ccad4bcb2e75cefa1cc83f50934431f754898b3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2269648313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e673d78eb576696f429fcb8037be7a928126308758a8d7f01b4edc41f8f9e8c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 08 Jan 2025 23:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:32:18 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:32:18 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:32:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:32:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:32:34 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:32:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:32:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:32:38 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:32:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:32:39 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:32:41 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:32:46 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:32:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Fri, 13 Dec 2024 16:30:53 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7042d18fb8683285697559e73cf74aeef0c8a08f9315bb518e5e3a9bee608aa8`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095376267f84cb3f81d900e0aa588d4a676110ea800da2c966dc31bdcfda6849`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 369.6 KB (369626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40af7f69b729ba457e22d4c258942b0e9ba55aad071c02851490628a9dc0e29`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19359de01ce18a398018bff964ffac6e17d57873939a38cb2bed7ae94c477dee`  
		Last Modified: Wed, 15 Jan 2025 02:12:13 GMT  
		Size: 15.0 MB (15020893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c432a0ce2d7b884d62e387761503f71c77992ee8e3b67178c7d07714cb24385`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f810aa041d9e2b10e4afbecb82dfdc23e3153aee8365e6e273cbc4a5084d9d67`  
		Last Modified: Wed, 15 Jan 2025 07:14:24 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a594fb8b58f33ce0d2733acf23484cc35d1e1f1e74818993953063066e0ac12e`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb726a2aae3e529211313e9c317c354f9e5019b9398fb43b8279de811c8b4e7`  
		Last Modified: Wed, 15 Jan 2025 02:12:11 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9f25566dc57e22fd9869aa43110ed993010b3327aa1b94766139b4886e550c`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e6518d0c8a8caa9aea40aba7f422aa00934d1f63eebde9d7c8625c8fbba140`  
		Last Modified: Tue, 14 Jan 2025 22:09:32 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56d2e1abbf379532e617d59db773b4242dea07354b6596b4a7075a3fcf8ecf2`  
		Last Modified: Tue, 14 Jan 2025 22:09:33 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07b612812d8d9a05a7aece9c59b6bf041d593d0269b5829a3663df750baaafe`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c93d9ea6936ab90e3d698344de15aa396b30101cc8f53d01519a769dd9f5e4`  
		Last Modified: Wed, 15 Jan 2025 02:12:15 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848574a2d0f941f796997862219f22e1a2c7350a48314676a585b3dd87369465`  
		Last Modified: Tue, 14 Jan 2025 22:09:34 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f421bb87e2bbe43daed75d8c4c0984c892858c5cc14b90a665e53730131b34e0`  
		Last Modified: Tue, 14 Jan 2025 22:09:35 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a960d19f1b123d25bf6d5e8150adbe2192e29347a5e2624220159449b292b0`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d799d17a45ee9b9c740f1c29d16dc8f38cf9896646171a2e11091a0c35f0abe`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5217a118992089f0da676390ceda6841fa8daa325e605167851d1f622311a1a5`  
		Last Modified: Wed, 15 Jan 2025 02:12:18 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abef5de6df9be951588bee6cc08178c55646c714a695418724c3da142911f10c`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 362.3 KB (362301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094ada08a213f863107606b70e3d03d1fd0c85c6f4041c794671a63ba9e32410`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
