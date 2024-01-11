## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:cdb4600df8fe3e27d97f1fb21ba9d5fdb1bd8198a1f025ca2458154f28d76934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull caddy@sha256:05a3dbd22c8c2ab815187427fd6c4c93118d8ef0f894a4c8ea63e2f94a614660
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1916234157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33367b5c991e5b0e4f4752a83d92a2427c6e9d98fbfdf37769b0924602a0139c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:27:50 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 11 Jan 2024 00:27:51 GMT
ENV CADDY_VERSION=v2.7.6
# Thu, 11 Jan 2024 00:28:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 11 Jan 2024 00:28:18 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 11 Jan 2024 00:28:18 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 11 Jan 2024 00:28:19 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Thu, 11 Jan 2024 00:28:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 11 Jan 2024 00:28:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 11 Jan 2024 00:28:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 11 Jan 2024 00:28:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 11 Jan 2024 00:28:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 11 Jan 2024 00:28:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 11 Jan 2024 00:28:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 11 Jan 2024 00:28:26 GMT
EXPOSE 80
# Thu, 11 Jan 2024 00:28:27 GMT
EXPOSE 443
# Thu, 11 Jan 2024 00:28:27 GMT
EXPOSE 443/udp
# Thu, 11 Jan 2024 00:28:28 GMT
EXPOSE 2019
# Thu, 11 Jan 2024 00:28:44 GMT
RUN caddy version
# Thu, 11 Jan 2024 00:28:45 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddb0a528ee25f289459dfa0d84bac9a14b9127f771882f0b60425ffaab79933`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320a9722b5187c98507b3945fbc5f2610abcc5d11d2a15edefb980c3890b4e62`  
		Last Modified: Thu, 11 Jan 2024 00:32:14 GMT  
		Size: 453.3 KB (453259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752dd8672cb5e334b293f934bde801e1be65eefc21179ec32a474b467094ac33`  
		Last Modified: Thu, 11 Jan 2024 00:32:13 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a96d6e9a72b624c3ca3d2ef154de09ab3922aeb66434dca1c3ada99bf483f7`  
		Last Modified: Thu, 11 Jan 2024 00:32:17 GMT  
		Size: 15.3 MB (15265727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c07cef1770381d1bd7e459337ce742ee1284a3a4f8aac9a8fa9021d44757d3`  
		Last Modified: Thu, 11 Jan 2024 00:32:13 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82192ad642e7980cf5f189cbec9102a5d27ebe938505fb7f1d3f00f6aed19f7b`  
		Last Modified: Thu, 11 Jan 2024 00:32:12 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4803481e3aae3efca19bc8239515b896f31b9c62936eff5e6b5f1f6e993027f`  
		Last Modified: Thu, 11 Jan 2024 00:32:12 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a2a948dcaeaac0c98b7c989af28731ccb460e44746d30876190f5a9533d4c3`  
		Last Modified: Thu, 11 Jan 2024 00:32:11 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb1fe3167023a8395dfb5d81d67735c3fac4f60265929a599be827819517ac5`  
		Last Modified: Thu, 11 Jan 2024 00:32:11 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe6c398a041f35ff13cb508ddac27bcfebcb67648963fa20c8a1674e0e272c0`  
		Last Modified: Thu, 11 Jan 2024 00:32:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823f94dc7cc6da16f64623b1be06863d7e5fd9537404d44d75bce4c9286d99d7`  
		Last Modified: Thu, 11 Jan 2024 00:32:10 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc6ad89630dde06deaf62bae99287cff6f9527eb0e4c0285b80c4b9f8b3392a`  
		Last Modified: Thu, 11 Jan 2024 00:32:10 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57f987c615a8934b60b413c4fb87f01bc1da99f905a3875ae15c1aa9e27972d`  
		Last Modified: Thu, 11 Jan 2024 00:32:10 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02382ce5c206a96e1663dafb2c888a7f7e97c9ce90d2b4e909e7a9b35b9456b8`  
		Last Modified: Thu, 11 Jan 2024 00:32:09 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60fd2eca8dc0381fd073410f4a3fb823dbd8ace74b7e02c761dbbf3fe531cff`  
		Last Modified: Thu, 11 Jan 2024 00:32:09 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7f66b6ee25ed55a56fb5128546b63989de6134ebbaca4e28b5486e3f64978b`  
		Last Modified: Thu, 11 Jan 2024 00:32:07 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba2deb7a206bc3d9388c2ac7b452b6399c7640b5f133e5ebfecfe63f1b33203`  
		Last Modified: Thu, 11 Jan 2024 00:32:07 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0838841899be257f01da94634e7b567988eaabe9d86f896573bf1cd1115c60`  
		Last Modified: Thu, 11 Jan 2024 00:32:07 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79396b6f9c050e882d6c88bfe39e8289153fe98a4b83c004731ab90e32fb4be`  
		Last Modified: Thu, 11 Jan 2024 00:32:08 GMT  
		Size: 278.6 KB (278612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2225d4cc5c0d44fab26c5a88559b5fb67343364f0ae80e4689ee11674d61a9`  
		Last Modified: Thu, 11 Jan 2024 00:32:07 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
