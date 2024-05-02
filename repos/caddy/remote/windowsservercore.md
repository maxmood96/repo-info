## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:1f1ec3d7ab97306a896214557794e5100d6d3d804395a313165c4b4af723e8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `caddy:windowsservercore` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:bae646aeb0fec0bfdb46399ba622b94ec1b8c2fbd9af741aa8fcdaca4d8034d7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2015607174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342e0fa85d1a439ede1ff2a4c10adf06c0b2af787ebda873af7663879115f0e4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Thu, 02 May 2024 00:51:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 May 2024 00:52:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 02 May 2024 00:52:09 GMT
ENV CADDY_VERSION=v2.7.6
# Thu, 02 May 2024 00:52:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 02 May 2024 00:52:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 02 May 2024 00:52:21 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 02 May 2024 00:52:22 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Thu, 02 May 2024 00:52:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 02 May 2024 00:52:24 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 02 May 2024 00:52:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 02 May 2024 00:52:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 02 May 2024 00:52:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 02 May 2024 00:52:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 02 May 2024 00:52:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 02 May 2024 00:52:30 GMT
EXPOSE 80
# Thu, 02 May 2024 00:52:30 GMT
EXPOSE 443
# Thu, 02 May 2024 00:52:31 GMT
EXPOSE 443/udp
# Thu, 02 May 2024 00:52:31 GMT
EXPOSE 2019
# Thu, 02 May 2024 00:52:38 GMT
RUN caddy version
# Thu, 02 May 2024 00:52:38 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd72becda85ed53b7a7bce0782eced475c618c7228c33594dfac257b9e411586`  
		Last Modified: Thu, 02 May 2024 00:52:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f147e619b2c27431faf683e7b9220989c267b8a9a18e790f51624536802c16b`  
		Last Modified: Thu, 02 May 2024 00:52:49 GMT  
		Size: 502.5 KB (502502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9dcd40eaa1907882517cf45dc82a1f8c22a4ea8a4414bdb15909e7515db059`  
		Last Modified: Thu, 02 May 2024 00:52:48 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ece3d3ba49c514e04b17a0b5f10f67b8df6d5dc2b3dea36e2682d44cbc08fe`  
		Last Modified: Thu, 02 May 2024 00:52:51 GMT  
		Size: 15.3 MB (15349999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d285386130a4992c302d863f6b0db44b4ca34147ce89db363b9236251532b940`  
		Last Modified: Thu, 02 May 2024 00:52:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2222b695927cbfe89a50a29d1c432e98d431073c77932ee0c66271e07ce5904c`  
		Last Modified: Thu, 02 May 2024 00:52:47 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02c6bfe97603288d577c3324aac2747da28c1e563dfdd46aa59f011bab0966b`  
		Last Modified: Thu, 02 May 2024 00:52:47 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a19626ef016391d22378d8280512aed8f53d3237284be8316a3e2ea8174495`  
		Last Modified: Thu, 02 May 2024 00:52:47 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6cf785b2dc40a39c74f4122e87120834d27ab06b2546465510faaa80aca64f`  
		Last Modified: Thu, 02 May 2024 00:52:46 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc50aa91996726f63f4b4290d9d6ac0281376150583cacfadad81500ca4dec8`  
		Last Modified: Thu, 02 May 2024 00:52:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113dd516944e0194fa664dd8af7d825303d35e4c7c7f27a4441898b82f3a8de8`  
		Last Modified: Thu, 02 May 2024 00:52:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470ad2810a09cccc6415cbfabbfc03596e46e2939512e7e6fd72981b8a28d80c`  
		Last Modified: Thu, 02 May 2024 00:52:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d11c3593eaff2396d8e4c4f95637bf50c1fbb961ef51ffc4140aa1da518ae4`  
		Last Modified: Thu, 02 May 2024 00:52:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dbcab13bf0572d9f5aa437e2fafc09d8bacafc6a01437c72fff3487486020f`  
		Last Modified: Thu, 02 May 2024 00:52:44 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7295b242664f20100036d77df5f24e1442b6dc31a56a835e248df139d13956db`  
		Last Modified: Thu, 02 May 2024 00:52:44 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d533f2fda5cd22d9bea38c737508d846490ff95e6136e4e339a513d07e3d5616`  
		Last Modified: Thu, 02 May 2024 00:52:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1158ab71cc2a9829b495311db877df27258a78b8593ed700f4c5afd651833823`  
		Last Modified: Thu, 02 May 2024 00:52:43 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb77a89d3f1456c7909caf1aba7c498695993ca0ed66bd8fb194a92aedf4b7d`  
		Last Modified: Thu, 02 May 2024 00:52:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1210f3cc28ceb69a6962f4082d72681ad64aa82b03cf37b923f42c98020b6f54`  
		Last Modified: Thu, 02 May 2024 00:52:43 GMT  
		Size: 359.0 KB (359049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e4b307ddd9b8eb232caa7c522696cb18977f78dd1db4e0012122ebe3a97cc4`  
		Last Modified: Thu, 02 May 2024 00:52:42 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:65d5234e5ff35ff6fe837e01f0d9f7f92e93f945ada7cbb2c5f3d3116e7fe6b6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2180637122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5742e2ecaeb7f5d2c3f183140b64ab822aaacc0c32fa4e2ee8c72a412f61d623`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Thu, 02 May 2024 01:50:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 May 2024 01:52:27 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 02 May 2024 01:52:27 GMT
ENV CADDY_VERSION=v2.7.6
# Thu, 02 May 2024 01:53:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 02 May 2024 01:53:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 02 May 2024 01:53:02 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 02 May 2024 01:53:02 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Thu, 02 May 2024 01:53:03 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 02 May 2024 01:53:03 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 02 May 2024 01:53:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 02 May 2024 01:53:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 02 May 2024 01:53:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 02 May 2024 01:53:06 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 02 May 2024 01:53:06 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 02 May 2024 01:53:07 GMT
EXPOSE 80
# Thu, 02 May 2024 01:53:07 GMT
EXPOSE 443
# Thu, 02 May 2024 01:53:08 GMT
EXPOSE 443/udp
# Thu, 02 May 2024 01:53:08 GMT
EXPOSE 2019
# Thu, 02 May 2024 01:53:36 GMT
RUN caddy version
# Thu, 02 May 2024 01:53:37 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9fc387786d734d0b2f6e355dba43fbe8c736406e3d20f0db2f31e72a567fce`  
		Last Modified: Thu, 02 May 2024 01:53:43 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57effe2d31325e496f7ab3fbd31529d1e138816baf805f01bccd14343d1d233e`  
		Last Modified: Thu, 02 May 2024 01:53:43 GMT  
		Size: 496.9 KB (496869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b765ae7422f59fed3cd9810ba43c3452a5f4406701681120936942261b21b75`  
		Last Modified: Thu, 02 May 2024 01:53:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a942f038a2669863ef2823ba09b4bfb865b521db2eeba3a0f258df0308058e29`  
		Last Modified: Thu, 02 May 2024 01:53:44 GMT  
		Size: 15.3 MB (15344081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740ff30fda2a30e2da7f90ba8d6ab804dcc1c78d8af3a34b39d0b78ab3324069`  
		Last Modified: Thu, 02 May 2024 01:53:42 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d126077bda03a0fca188e33974f0adcee683e5f7b4307b9cf3619c3835d0c8da`  
		Last Modified: Thu, 02 May 2024 01:53:42 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0524e707bd636cf4009d7a784c73e903d6e7dd0a675645ffbc093d4b12bebfa`  
		Last Modified: Thu, 02 May 2024 01:53:42 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea7a2446a939880d0d97113709b8c295d3ed101766648208d4ee955afdefe94`  
		Last Modified: Thu, 02 May 2024 01:53:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8739aa3d6d7be823e2c2184b51f66ca7e699c92d3035a59b0dacc86885e9df28`  
		Last Modified: Thu, 02 May 2024 01:53:41 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4321239c90fdb45bbc8c2d82006aea4da8bf7d305e3aa4f1c13095e9d27cfc`  
		Last Modified: Thu, 02 May 2024 01:53:41 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8abec9a0af8bed0386dbd62c6ea79ed1a917cbbeed998f0be1741dd0f5d0845`  
		Last Modified: Thu, 02 May 2024 01:53:40 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c863ff51e435ed86f30cf638978a095e34bd68018b7d38bdb01872ace97e5041`  
		Last Modified: Thu, 02 May 2024 01:53:41 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f697a5502b82640823ca7e7c65191559713098f9318de64fa0d232ff6e26cc76`  
		Last Modified: Thu, 02 May 2024 01:53:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122e98893a8d788079cc8fabf9b750a953f59c5b275b2eae7a8b1ae2266ae211`  
		Last Modified: Thu, 02 May 2024 01:53:40 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d070d9c6e231473d53216f127acf8354747f0c3dd2e4b013609ab566d6bfb6`  
		Last Modified: Thu, 02 May 2024 01:53:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca879a464b8ec715d465a8bfb0bc95201640b371257f5374697b8b59711e91`  
		Last Modified: Thu, 02 May 2024 01:53:39 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e73e72855c48d199fe22a3c54778c204f54986ea4943083e4cf6240d193b27a`  
		Last Modified: Thu, 02 May 2024 01:53:39 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7e828e4dbad42a439f6093ac800a1c9c62b3dc35c4f94c01a08474dce6b1f5`  
		Last Modified: Thu, 02 May 2024 01:53:39 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f3b07356ffab559bb7ab302151fa959c58b5ea91d7d9e561eb5dcadebb68b5`  
		Last Modified: Thu, 02 May 2024 01:53:39 GMT  
		Size: 346.2 KB (346184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beeecb83bc8324f9461db14d64b5899623c8ccfb72b196f6683ef1ac4b22802d`  
		Last Modified: Thu, 02 May 2024 01:53:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
