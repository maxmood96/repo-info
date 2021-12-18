## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:ec91695b78a45504a24d95c1383e94c25408a6354c5dabe66dc42a146f371ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull caddy@sha256:63a9dfdb9dbdded9758f2d65068b30e42a562cf8621adc94d298175aea2fcae0
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2721453453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9028a9672d4350a935450ce527035909b85c400b7d1d952df7f80ad1aaf9f67b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 07 Dec 2021 04:56:01 GMT
RUN Install update 1809-amd64
# Fri, 17 Dec 2021 23:26:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 18 Dec 2021 07:49:10 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Sat, 18 Dec 2021 07:49:11 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 18 Dec 2021 07:50:19 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Sat, 18 Dec 2021 07:50:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Sat, 18 Dec 2021 07:50:21 GMT
ENV XDG_DATA_HOME=c:/data
# Sat, 18 Dec 2021 07:50:22 GMT
VOLUME [c:/config]
# Sat, 18 Dec 2021 07:50:23 GMT
VOLUME [c:/data]
# Sat, 18 Dec 2021 07:50:24 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 18 Dec 2021 07:50:25 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 18 Dec 2021 07:50:26 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 18 Dec 2021 07:50:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 18 Dec 2021 07:50:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 18 Dec 2021 07:50:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 18 Dec 2021 07:50:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 18 Dec 2021 07:50:30 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 18 Dec 2021 07:50:31 GMT
EXPOSE 80
# Sat, 18 Dec 2021 07:50:32 GMT
EXPOSE 443
# Sat, 18 Dec 2021 07:50:33 GMT
EXPOSE 2019
# Sat, 18 Dec 2021 07:51:28 GMT
RUN caddy version
# Sat, 18 Dec 2021 07:51:29 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ee7a7ea9cf22f75886179907a41810a992e21f3d0c57cc10d2147ce9237701c`  
		Size: 990.3 MB (990271574 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31b2acce136e44984ba36d64717a6a67fbf1a98ed7ffcf0a14df848c1502a345`  
		Last Modified: Fri, 17 Dec 2021 23:47:14 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41872cf291fe6613ea557ec907ac1b118a8e4abb221eecd365989adb35aeb286`  
		Last Modified: Sat, 18 Dec 2021 07:57:46 GMT  
		Size: 383.2 KB (383229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dd413c535150899a7980b35e96c987d26f98ffd9312c1bb3e20f9ea94e825b`  
		Last Modified: Sat, 18 Dec 2021 07:57:45 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22480f9a4d088fbff8901e96b868cc3a55ebd3061d974492b99e98dc6bb67d4`  
		Last Modified: Sat, 18 Dec 2021 07:57:48 GMT  
		Size: 12.1 MB (12144370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed670ceeb666ad94e1034bf3224ca8355f1e731aeca093fc9384c2233f09a10`  
		Last Modified: Sat, 18 Dec 2021 07:57:45 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa3a7408f1dbd27f9efc89cf5e87d99cd82080d1f217929f91812decff3a411`  
		Last Modified: Sat, 18 Dec 2021 07:57:45 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188b18065bfd482510dfe86044d131a835cc91b1511cf55278e8fcf01ddbd6be`  
		Last Modified: Sat, 18 Dec 2021 07:57:43 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39920c0ce1a9a1588d5ba997c46ff276b0974d705f14bacc6bd1b60142c54827`  
		Last Modified: Sat, 18 Dec 2021 07:57:43 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca98f67f5984d4e2483fe80e761774efa7792b67d2dbb832c3f1f67bd0f98b7d`  
		Last Modified: Sat, 18 Dec 2021 07:57:43 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6cbf4f55f9fa2a90d5f4ffecd753fb720185e15d02504308c98daae9fdbff4`  
		Last Modified: Sat, 18 Dec 2021 07:57:43 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc796ddd4ece787df1a98cba7748a8eec4761924689719ee5d63e7e11dccedba`  
		Last Modified: Sat, 18 Dec 2021 07:57:43 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7637c0ca388c8f47e5e5b649f573ffa5c546863f4a3265f629bcf6f6d93e980b`  
		Last Modified: Sat, 18 Dec 2021 07:57:41 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e735ce3a2360c960ec20150766b73b8468ba8578188091b49d30674a4f99b659`  
		Last Modified: Sat, 18 Dec 2021 07:57:41 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3caa56d549bae3f2e84e9bebdbb666a32803abf409839063c8591da8bd26c7`  
		Last Modified: Sat, 18 Dec 2021 07:57:41 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace5fdcbb5509d64e7a9ea4c9a10c1a9df4d5062b3f01df3972e779cfb767859`  
		Last Modified: Sat, 18 Dec 2021 07:57:41 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44dd3854e049581681bf2f9769271bc2d9b34c0c2c02273deeeaaad6428c1da`  
		Last Modified: Sat, 18 Dec 2021 07:57:41 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2897a8e2ad22b571108a7133c61d9a13f47ec226a0f1eb663adb6dcd699aecb9`  
		Last Modified: Sat, 18 Dec 2021 07:57:39 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959f24f60e6edd7f3c0e1f01a2e21793882bd7019003e0e11a2e7c5ef14232ef`  
		Last Modified: Sat, 18 Dec 2021 07:57:38 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fadcfd3fef03e123f671af59b06838229ff440e2a6f856231f3ef1032453ed4`  
		Last Modified: Sat, 18 Dec 2021 07:57:38 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cce859126f470aaa169b451fea397b54e1eb6a2ccd8da7d5763453680c20269`  
		Last Modified: Sat, 18 Dec 2021 07:57:39 GMT  
		Size: 295.9 KB (295923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0215143e028203246e3e105fea1ebd611ad253d492e964cb33670bed21aa66ac`  
		Last Modified: Sat, 18 Dec 2021 07:57:38 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
