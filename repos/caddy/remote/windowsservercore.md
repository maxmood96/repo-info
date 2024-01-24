## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:c6e3f25c93c35d4a519395eb595f46de5889867e37acd83bac72b8d2d9dcef3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `caddy:windowsservercore` - windows version 10.0.20348.2227; amd64

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

### `caddy:windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull caddy@sha256:45db61c754ddd6e5ec06fd28a8099b51b78e0848a64f1b55a89da26731ef2579
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2085736435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d84e958273e9ab44607135820d1cb0a85c662765ec566b7fdfc82c7f819995`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:24:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 11 Jan 2024 00:24:52 GMT
ENV CADDY_VERSION=v2.7.6
# Thu, 11 Jan 2024 00:26:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 11 Jan 2024 00:26:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 11 Jan 2024 00:26:11 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 11 Jan 2024 00:26:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Thu, 11 Jan 2024 00:26:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 11 Jan 2024 00:26:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 11 Jan 2024 00:26:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 11 Jan 2024 00:26:15 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 11 Jan 2024 00:26:16 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 11 Jan 2024 00:26:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 11 Jan 2024 00:26:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 11 Jan 2024 00:26:18 GMT
EXPOSE 80
# Thu, 11 Jan 2024 00:26:19 GMT
EXPOSE 443
# Thu, 11 Jan 2024 00:26:20 GMT
EXPOSE 443/udp
# Thu, 11 Jan 2024 00:26:21 GMT
EXPOSE 2019
# Thu, 11 Jan 2024 00:27:18 GMT
RUN caddy version
# Thu, 11 Jan 2024 00:27:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8ac948dab7d4d3a44ab44e27a80115467b2f5fba68a58b377fef3e920bc5eb`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2628b34eba07214b21750eb21215539642fc79460ac44602f68367c8ef8f1876`  
		Last Modified: Thu, 11 Jan 2024 00:31:48 GMT  
		Size: 460.6 KB (460623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bba07c52b418ca922065149b75e4f078732301d850f6c6a857a0396fa758183`  
		Last Modified: Thu, 11 Jan 2024 00:31:47 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d43dbc97e7f70164392cf4e8ba36666c051180f2d9a5fa749c2ebd8f8902da`  
		Last Modified: Thu, 11 Jan 2024 00:31:50 GMT  
		Size: 15.3 MB (15274872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf65f149b526a7db12aa1cc0a82fee2c91e70e14004538422b70bf463f1e6a`  
		Last Modified: Thu, 11 Jan 2024 00:31:47 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0e80605ac50e370132adb19e7fbd35df1083f20a16f102ba838dcd1fbe6ddb`  
		Last Modified: Thu, 11 Jan 2024 00:31:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbf4dbf98c5ef756b92eec802352998cae9a7a53998309f4d23f3a25fe998ab`  
		Last Modified: Thu, 11 Jan 2024 00:31:45 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5289b1119e5b6b3d21ecba38a21af08402723786c6a0d255d9656bab6fb0e45b`  
		Last Modified: Thu, 11 Jan 2024 00:31:45 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4279deef6070878783847e2a97632c9e6c1c1f4ee240c4582cf8ff0f507a1f`  
		Last Modified: Thu, 11 Jan 2024 00:31:45 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baca7c3ac198520fe83b18575029c9d68d6458b37234869602bf5a246f1cae49`  
		Last Modified: Thu, 11 Jan 2024 00:31:45 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc6cdf36ba1ce7eb637a46f998fd84b12e02b76b737244ac8f6a5a61a2f6d65`  
		Last Modified: Thu, 11 Jan 2024 00:31:44 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0870a17942cc9d0cbbffa15ab03f6401c95d37ab9fd965e63cb8267dfb6a4d5`  
		Last Modified: Thu, 11 Jan 2024 00:31:43 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97548b26d83c7392114297bcfdbf85c8fdf5f812fea56a4c355e28a0f063454e`  
		Last Modified: Thu, 11 Jan 2024 00:31:43 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824baecd8144b0da5828335f980e72f9721a3ac35dbda7f8927ef4e1dc4fdf0f`  
		Last Modified: Thu, 11 Jan 2024 00:31:43 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe4e2c9f762e3bacef96b2394563066a0e8f4b62d3dea44e8a8d6c1a661ac86`  
		Last Modified: Thu, 11 Jan 2024 00:31:43 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f434e7a3223202b5c62896b0b513f7ac33068974c4a3a87c2c13dd95dda313`  
		Last Modified: Thu, 11 Jan 2024 00:31:41 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41470b117bd27755279ab256ba0156bf64796a6fcd06cc26ac6d1e617387d4a0`  
		Last Modified: Thu, 11 Jan 2024 00:31:41 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e389ce50002f8ac47cbbe67517402ca31e7fc2e99945faf3cf392848560faaa8`  
		Last Modified: Thu, 11 Jan 2024 00:31:41 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0990eeef88a51462c1b1e6a7044d57c8b6976e099844570344699067f387a3`  
		Last Modified: Thu, 11 Jan 2024 00:31:42 GMT  
		Size: 254.6 KB (254599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b1fd2b9188ec5f76a81bfc4d7aa53b000672e101a91e51a5df9ab4cfcc2a8c`  
		Last Modified: Thu, 11 Jan 2024 00:31:41 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
