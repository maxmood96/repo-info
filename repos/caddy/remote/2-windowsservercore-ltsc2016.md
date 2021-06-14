## `caddy:2-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:076e0573f1533c025ab55f299e32833e09ed22b4c52605a2351aba5baa2f585d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4467; amd64

### `caddy:2-windowsservercore-ltsc2016` - windows version 10.0.14393.4467; amd64

```console
$ docker pull caddy@sha256:4d5c4f12af6b434f907c262accbfeef1c9eb948d91bb5113bde117904152d9bb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278396558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0d047c64024dd8b9ee7374a59e2e19a219277308f3db92d25f22e903b4f6fb`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 06 Jun 2021 15:37:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Jun 2021 12:41:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jun 2021 20:11:27 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Jun 2021 18:17:52 GMT
ENV CADDY_VERSION=v2.4.2
# Mon, 14 Jun 2021 18:19:36 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.2/caddy_2.4.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8d5cf4479e471d47fd067ce2fbe34c2015a96caedab95ca042aeb633956cbc2bb89c1bc4fe6593c1f96ca58bc66b21f32caa6b099122b9d500a3902245fa5105')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Jun 2021 18:19:39 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Jun 2021 18:19:41 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Jun 2021 18:19:43 GMT
VOLUME [c:/config]
# Mon, 14 Jun 2021 18:19:46 GMT
VOLUME [c:/data]
# Mon, 14 Jun 2021 18:19:48 GMT
LABEL org.opencontainers.image.version=v2.4.2
# Mon, 14 Jun 2021 18:19:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Jun 2021 18:19:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Jun 2021 18:19:55 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Jun 2021 18:19:57 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Jun 2021 18:20:00 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Jun 2021 18:20:02 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Jun 2021 18:20:04 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Jun 2021 18:20:07 GMT
EXPOSE 80
# Mon, 14 Jun 2021 18:20:09 GMT
EXPOSE 443
# Mon, 14 Jun 2021 18:20:11 GMT
EXPOSE 2019
# Mon, 14 Jun 2021 18:21:14 GMT
RUN caddy version
# Mon, 14 Jun 2021 18:21:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2f52abeee6d6f4a925ad418b5e6200d4fca9bf92834ffc918b8bbaccd34251db`  
		Size: 2.2 GB (2195741359 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c82e82e95dbad4ccc260b42e03767eb07222e2f00ec57a69b3c87b17da1d2fd3`  
		Last Modified: Wed, 09 Jun 2021 13:04:25 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a28e390d3b8e7b9369b102914eaee6e1fa0d14eb258b628be67f99f32f06f81`  
		Last Modified: Wed, 09 Jun 2021 20:20:01 GMT  
		Size: 357.4 KB (357370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd5fde0219b866984e02c69748a7c533734e7d3ce1c605e00b2794ba719ca78`  
		Last Modified: Mon, 14 Jun 2021 18:25:40 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ff67696fba822eac7dc90ce8b74a3463e180c1277ce1b5235dd553efd54d37`  
		Last Modified: Mon, 14 Jun 2021 18:25:53 GMT  
		Size: 12.0 MB (12011979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb05b150667473f58bd9ff97143e7addb941c15c23d7c0190462052e171a5d3`  
		Last Modified: Mon, 14 Jun 2021 18:25:40 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417ec686bccf8c11c7e167450f76c56e965e0d895b8a67d2959fa0cd8e0f46c6`  
		Last Modified: Mon, 14 Jun 2021 18:25:39 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e7f7e817f7b000e684b2477e658283e3bc5e32f705e2a1af3eb2171451ab1a`  
		Last Modified: Mon, 14 Jun 2021 18:25:38 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9adbfef5bd1c4ce567e8643e7eb3ac228fc89e60afffa0d4ad65188836ee10e`  
		Last Modified: Mon, 14 Jun 2021 18:25:37 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46951e23f2c6f042a74af530655917c470e7e58bd428811bea889f06ece060f3`  
		Last Modified: Mon, 14 Jun 2021 18:25:37 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b702d713b07cb19c098b0a4c2ad22de8111ab140c99b88deb21ffa5f10870f`  
		Last Modified: Mon, 14 Jun 2021 18:25:37 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1554c780202a1e2bfb6cafbf73148847f97c535c407f63f750903997105d516f`  
		Last Modified: Mon, 14 Jun 2021 18:25:37 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a72ab2ef98ce84364537328634d5a56cb6c9080cdec9988778c0e15d451dc51`  
		Last Modified: Mon, 14 Jun 2021 18:25:35 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0cb0fb150ef4d4bb3e78339539c6453dcdf1d1b11d50728bb72e262b603fa9`  
		Last Modified: Mon, 14 Jun 2021 18:25:35 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d8666b345f227a53b8d4cc8698ebe05b454caf116f8329e30d4328ba56896e`  
		Last Modified: Mon, 14 Jun 2021 18:25:35 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7bce3d7ad9504e8b1a2a5f46b50605a7e895686efeae62529b2fb0c8210a2e7`  
		Last Modified: Mon, 14 Jun 2021 18:25:35 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d806bd36723a790387c5f61446d9b73da291b1e1592e6943b28686f3dc50fb39`  
		Last Modified: Mon, 14 Jun 2021 18:25:35 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddf127d6e3c5443190a309b2f703cfd1d079beea71723b1507958dbbf2b5cab`  
		Last Modified: Mon, 14 Jun 2021 18:25:32 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace91f2d94fe0fd5d53fce078d832db72cc38e2ef7692a44f57f9377dcbf3f8f`  
		Last Modified: Mon, 14 Jun 2021 18:25:32 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f8adfaab4745797ca3869f6e54a87e5c399e56609635f7b74b039fb8f9fc00`  
		Last Modified: Mon, 14 Jun 2021 18:25:32 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca3d4ed717fc9e7154ad94da8a5ea30b61ba4dfe9ec25bdcfcb55e6291cbec7`  
		Last Modified: Mon, 14 Jun 2021 18:25:32 GMT  
		Size: 274.6 KB (274630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deafc6c05519d23d4709cd8504c83ff6c43943477ddcaf57ae7a871acdbdf489`  
		Last Modified: Mon, 14 Jun 2021 18:25:32 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
