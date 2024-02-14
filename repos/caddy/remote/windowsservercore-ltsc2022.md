## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:6e915ccce3def5db60e3af13d28e398bfdbde6a3298781b0cf53cbb174b0f23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:f6e8f7815f3e03bc5d239d52a2bdeb473ff959a4b74bb86ee94b410cc2407c35
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1926683398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d9ff1f8c7723994d4a4f7c520159beedff8fe440b855a9fb6f57afdcae7b2b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:22:32 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:22:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:23:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:23:00 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:23:01 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:23:02 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:23:03 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:23:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:23:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:23:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:23:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:23:09 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:23:11 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:23:26 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:23:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ebcfc7e63facc5463d681dd534f084e021cc447cf46213aae377066d573493`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 458.4 KB (458447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bee2047afe4426d5715972f534b35ce0bc5ae241ae42982e37a64185c7a482`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39da07145bbe64c3ec2c032dafa6eb6ddf62130dba67e03a627cc2cb3788f9e2`  
		Last Modified: Wed, 14 Feb 2024 21:26:37 GMT  
		Size: 15.3 MB (15267126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c47f482128a80b23df310b1c1b71bfa176b010cdd91761fb1a9aa71c4812738`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dab75e60136c0cf03ae7e7ad030b7adb3aff8014f4fc0e412d1ce9c217bdd60`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db7f5e1b9057131a3d1e7f1439de34f87684add5ac177612296925ed37b654d`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ac08dfbec3219d30d64f54cc8e1b46009cf4327d55c288ca43d875eaff3763`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4fad3dd8e3739d27a2d3793ae4740b4cbf52999f2295ad370545f048730492`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91f700224a04849cd48e2ab6525d47b7188051110718ca045ca50452ce26cb3`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fe7f9176dbfd4a89d170a117169a90cd5f49a2c5b7a55ac4026288812b8b60`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4fc40cf63828021df321258238a85d39918d2749a117bb0538bda0afce3aef`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9621f5d2e06bf68f778ba42ec6ec5d4a80d1cfb1204ea19b5a2b42d2b1d87d`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398c5b0cde2fcd40c8ce079d93fd115bd8ee7d8028cabc4baf9ecc07ab226410`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60cb86bd52f82372e11b1b851709ccb6c10537dc9262f63ef8bcd0152efb235`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c35a9695bf632732db6dd52a7531c75c5243819b2b8d7c019a1e8fc796e13c7`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c98226f721bed207883df26f4d35276821dd38299a62458d2ba6c55fab5b0d`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b23541f7ccf5a2debb904fdc41eccc03284d7fbf3baff61798b726d7c9ba12`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ce3a452fdfcd413ac385a157633a0fe389a8c2fdb281ce79b5cdd4d16dcb9b`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 281.4 KB (281363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7be2379ebd2e4d0fca0bbf81dd2628e93d8efd2ef3ea28c3872855ca6e50ed`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
