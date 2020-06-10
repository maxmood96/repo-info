## `caddy:windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:c5e137c3575e37688a5ec6f3a628bde1fade7f6c99278fae9f865f24a52accc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64

### `caddy:windowsservercore-ltsc2016` - windows version 10.0.14393.3750; amd64

```console
$ docker pull caddy@sha256:64246e00b3c6726a42b20440c70003c72bc6e652f821982345b87928bc79cae5
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5756998229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6c0b59ae11bc16763ab0732bf43ae0dead1bbded3284e54191f687f4a670e1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 09 Jun 2020 22:36:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jun 2020 18:04:40 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 10 Jun 2020 18:06:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Jun 2020 18:06:15 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 10 Jun 2020 18:07:58 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('636bb25c9738400b480ca243a605da74988deb1bc856a1cabe7ee36511db0e048ec0a2688b1640d7b157bc239d437944e43500d91881c8acc7f2b8aa138945f9')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Jun 2020 18:08:00 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Jun 2020 18:08:01 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Jun 2020 18:08:03 GMT
VOLUME [c:/config]
# Wed, 10 Jun 2020 18:08:04 GMT
VOLUME [c:/data]
# Wed, 10 Jun 2020 18:08:05 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 10 Jun 2020 18:08:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Jun 2020 18:08:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Jun 2020 18:08:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Jun 2020 18:08:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Jun 2020 18:08:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Jun 2020 18:08:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Jun 2020 18:08:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Jun 2020 18:08:12 GMT
EXPOSE 80
# Wed, 10 Jun 2020 18:08:13 GMT
EXPOSE 443
# Wed, 10 Jun 2020 18:08:14 GMT
EXPOSE 2019
# Wed, 10 Jun 2020 18:09:10 GMT
RUN caddy version
# Wed, 10 Jun 2020 18:09:11 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c938241e0507e1ada5f864325483d86fd08533a5a31e7cb6ec1357db9891b245`  
		Last Modified: Tue, 09 Jun 2020 23:18:33 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22985925139cd6a6e83b6eb5286a8a6e1053a5c6ddd9762f34deea2aa6bcaacc`  
		Last Modified: Wed, 10 Jun 2020 18:10:17 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43c028d6768e901bc64b3edb7e2e5f72050d3ed78ea4e7337fe85725d250c15`  
		Last Modified: Wed, 10 Jun 2020 18:10:17 GMT  
		Size: 5.4 MB (5404509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab96ccdd2dbffb13487e758409eaae25905b86a83e7b7a51a692c7ff18579b8d`  
		Last Modified: Wed, 10 Jun 2020 18:10:14 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aac2a7ea7e1f98bb6027b5090912006abeb6f367523aac337f6705ba4d7bb6b`  
		Last Modified: Wed, 10 Jun 2020 18:10:19 GMT  
		Size: 17.3 MB (17325836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7acf530d8fe0b1ea1f35f0e20ca267e447936a8edbae3889184d180b44c1a6`  
		Last Modified: Wed, 10 Jun 2020 18:10:13 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7609e5df44616b1f91e5434a43518cf253a69c406c062ef6b99035b20a437`  
		Last Modified: Wed, 10 Jun 2020 18:10:13 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1384cb066181208a5bb3be7023fe3f0b9cedf5483885cf330f7dcd95525302`  
		Last Modified: Wed, 10 Jun 2020 18:10:11 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f2a49d3e0a25e1871a3dcb23fa333268062b4d027ae041e3bb5c0827dd0c2a`  
		Last Modified: Wed, 10 Jun 2020 18:10:11 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b5ec5b8bc911e1426e8c8dcc06a149b90edee45636d75da5b63e83fe91398a`  
		Last Modified: Wed, 10 Jun 2020 18:10:12 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dab68d41796a58e20ae80dc2528cfe6a2e71a04c8c88bb5595a6e0a5d7f7646`  
		Last Modified: Wed, 10 Jun 2020 18:10:10 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68da8c08840ea413933ac718a42b86738f90a6a5647e151252d4b5193ee40a8d`  
		Last Modified: Wed, 10 Jun 2020 18:10:11 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946bc1b557fc88846697a1a1308c7af5ef52918f700f7dc8bd4c53e915c4a1a3`  
		Last Modified: Wed, 10 Jun 2020 18:10:09 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7ea127cbc59b2799852a077baa3bc9e46ad415abc4de6305396739a257a25e`  
		Last Modified: Wed, 10 Jun 2020 18:10:08 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e77ea136bb911d1a64b32d1d139522e0e52ca1bc43b5d12aeeef7be91483d50`  
		Last Modified: Wed, 10 Jun 2020 18:10:08 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a29c745913025b3a12451ab689a6186ec7756b5d99d0fa379a39ae81d510b0b`  
		Last Modified: Wed, 10 Jun 2020 18:10:08 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4ae08e24e91168918350e7422b8f47200d09a7313216990ba6a672b5372280`  
		Last Modified: Wed, 10 Jun 2020 18:10:08 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e219b4ef296fd92d145bf1f1a7b7d79e09c26a996daf350eb5ee70cbfeed02`  
		Last Modified: Wed, 10 Jun 2020 18:10:05 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc81bd4365ed96954980b554e769048c1e4cc97035385e22ee8364bd2856d4af`  
		Last Modified: Wed, 10 Jun 2020 18:10:06 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec6f99a5c3e003e6dd16b75770a2762bb5de2737ffdd11b1c707f6aefce201a`  
		Last Modified: Wed, 10 Jun 2020 18:10:05 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26ba6de29355852954f97260ed4e96f1d30d7e675356cc21cac59feb841cf3e`  
		Last Modified: Wed, 10 Jun 2020 18:10:06 GMT  
		Size: 248.4 KB (248359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef895a3d9501c41dd42a22a3e2a0458c59b35892005f5fb18b8937101a1fb50`  
		Last Modified: Wed, 10 Jun 2020 18:10:06 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
