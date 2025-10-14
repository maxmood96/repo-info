## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:5af12613b8fca792670ec10879facc989bab4b36b94af6b4d9307bcd389bfe50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull caddy@sha256:8ffdcd060c7bca2b5182de34056ea24a6e4ca4dc52bc69d02dd1f71371527c94
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1506323712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c860029e9e4be4a680867c39dc1b7704c98e5975004afe5e390b1e5afdde8fd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:41:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:53:28 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 14 Oct 2025 20:53:28 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 14 Oct 2025 20:53:37 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 14 Oct 2025 20:53:37 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 14 Oct 2025 20:53:38 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 14 Oct 2025 20:53:38 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Tue, 14 Oct 2025 20:53:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 14 Oct 2025 20:53:39 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 14 Oct 2025 20:53:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 14 Oct 2025 20:53:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 14 Oct 2025 20:53:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 14 Oct 2025 20:53:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 14 Oct 2025 20:53:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 14 Oct 2025 20:53:43 GMT
EXPOSE 80
# Tue, 14 Oct 2025 20:53:44 GMT
EXPOSE 443
# Tue, 14 Oct 2025 20:53:44 GMT
EXPOSE 443/udp
# Tue, 14 Oct 2025 20:53:45 GMT
EXPOSE 2019
# Tue, 14 Oct 2025 20:53:50 GMT
RUN caddy version
# Tue, 14 Oct 2025 20:53:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c73b68129a17f163f24c548f99fac1fa06db5f2df83addedaeeccc104c116fd`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944442d4fa7228ae2f72213ece9c5856e0e07144c4c67b533d6bf974b82130bb`  
		Last Modified: Tue, 14 Oct 2025 20:54:09 GMT  
		Size: 360.4 KB (360369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931dac62e54b188592dc164c0c85e3c851af4cae9f98cb24d9194a32b28dfcb9`  
		Last Modified: Tue, 14 Oct 2025 20:54:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532ce732b24177e7d02bc20cdae96cfc5c2fcafa993b7faf3d4659804d32aae3`  
		Last Modified: Tue, 14 Oct 2025 20:54:10 GMT  
		Size: 16.6 MB (16568804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208a75d0f90591ee1a1b98c56684e3c108ac64bdd27910ce49f6906828e25a3a`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d0d78bed108d4d575590ed89585bbf50ee47ef2128e28c6e6888525379d7ec`  
		Last Modified: Tue, 14 Oct 2025 20:54:09 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9d62e15af93f70a0120a76ff688280a0f26922e2475476bc839ea5860dd35c`  
		Last Modified: Tue, 14 Oct 2025 20:54:09 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91e5a016c80f277af8960cbbe745684becde789f0ea0c77d8eef18144e40151`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65627fbb9732f4b7a1424282c94f426b5ee430e3e32bad43980dad12dde0cd`  
		Last Modified: Tue, 14 Oct 2025 20:54:09 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3c142d1b0d5feb26ea3f65d417f686975c3ec2f48590950878c1a3258c899`  
		Last Modified: Tue, 14 Oct 2025 20:54:09 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc126eb2b4ccd18b17f552b6c2c1edc97d0068b73b72a628246d24413626bd5`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5935984c3d857c1f7fdb1ab04bd59d22e04ad899a12c522235d775582783a3`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a06f791eb1ce34828e0032694bf72acc53e3c2cacc95a6193e846a1293bdfc2`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11c9522644201c2133e3f6e150b8d6dd19c2b3796a5b962c6a8e5b5e768cefb`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a588903917c9ff4e649725da099bc2e0d8bf6ca7fb3f8f36b7605642c2b1d772`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0ea40d67aa66a6eb56827258102feedff5c6a9918965a4340241fd92d04cf3`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f93546e931773eef69740cb6f175bb6c0bacf55ed43701fc243840beda9a81`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ecc941028812c3ef88faa90a87a0021846ccea1b6feeb766e7887849be39e5`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55d9824d28a313143b9dfde65c62fcb5e7e9a99ccf537c11e4293d9ef406926`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 353.2 KB (353164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7372194261cb1b9866efb7908b2117b73e5bad498e307991eda5a1e2be22cccb`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
