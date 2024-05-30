## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:7a8c826b69b921eba34d21e8f1432aa2173c0ef6595ac138f64856a830ee1204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:8a859e5b235e64538fa481dfb9bed042aa4775426494d913536d7a417dc36863
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128658583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d212ddc0b7d46916ade47bdfdc02a354cfd896230f4871965d8f54acdaf535d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:08 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:21 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:22 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:54:34 GMT
RUN caddy version
# Thu, 30 May 2024 19:54:35 GMT
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
	-	`sha256:bd28d89657c62bc0a9414370e4d20949cf6d90a3754cc9cc83bbd947d68385d8`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459dffce42b3a93c6dcb89c8119b8de9d2cc7e8e0e8317feaf7cd9196443e84d`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 359.9 KB (359860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5699211ec97142ff5ee8b36eecba7d7b8b8a48b752b256c9bb79be28454478`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e326c3d4cca13916661f8d251ca1ba355ef43aac90cb123a1aae87dd3ff886`  
		Last Modified: Thu, 30 May 2024 19:54:48 GMT  
		Size: 15.3 MB (15255909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14adcda1fdb75ee4a38fda124f290dbde1dc66826431129731382871525f05fe`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525aef206a761d1b5995be7beb217aa838ec7d1e05805608f1e3c88ea496b624`  
		Last Modified: Thu, 30 May 2024 19:54:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e83f0cb1b15632d5728a0fc228889c8328a889816e9e5893bfbfda486e423a`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a35dc8c6b268cac88bea9d7cdbb7a01fe744813bed2b0cd707533e7b8e46fd`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6545c772b737a8fed2a69db09c17cad0a7e111fb1b5b25fc2d25dc67ab06e89`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e122125faf27258b9637497e55eba99d5953cbb2e5d37e885da446b8a6d2db`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de5a85d9349913ad621ac0e58b44c8cfaf909e69519c9db45b0bddeeb899281`  
		Last Modified: Thu, 30 May 2024 19:54:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f7935d97cc7a666b6ed78c3464de92792ef20694f77ea5eb43c223af434255`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e32befc8e35ad3e7d8a49b3ec8496d8135ba9a673c3395cac25733bee2cf60`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caee7d7f23b87127d7a565da580d9427ec3e8ad2e0f5557fde35d249ee4dba46`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fac278d2e30b07f351c267ed6c470101ead2945b6da2001291809755adcdc9b`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b4f0c9b0a843a5437c6c2c859685879c5cc515ccfd0cad0a64fdf09219d4bb`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96febe2e0b0fcb00860b3c6071b9a974a4e5decffc5f7e3ccae60b70b6474cc3`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbe0cecb35714e1d0bd2ba02f4fd4464ede77a9b14a65b57d6e38279b7217a9`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bcc027ca9fc0ea5d69d71480a08928c9279dcb826dc4d50d8d65605f8f6ede`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 349.5 KB (349497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c987e28c39468930d912b006e33d2a7b3b4d5e1c421f748f3907ecd0391489`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
