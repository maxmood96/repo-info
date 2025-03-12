## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:7176f8e6782c9e7d0d4587ae3281dc2a83b5c71747a73519dcf137d51ce9507c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `caddy:2-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull caddy@sha256:10f83c0297969c9792d0de4d36ba317a1674c7617d3b46ce1793c32eb316779b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2285697500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdea3f00c57482c0db0bf3afe64f92658d6114d94641b4456cc3ab579162891c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:53:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:54:03 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 12 Mar 2025 18:54:04 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 12 Mar 2025 18:54:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 12 Mar 2025 18:54:13 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 12 Mar 2025 18:54:13 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 12 Mar 2025 18:54:14 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 12 Mar 2025 18:54:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 12 Mar 2025 18:54:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 12 Mar 2025 18:54:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 12 Mar 2025 18:54:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 12 Mar 2025 18:54:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 12 Mar 2025 18:54:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 12 Mar 2025 18:54:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 12 Mar 2025 18:54:19 GMT
EXPOSE 80
# Wed, 12 Mar 2025 18:54:19 GMT
EXPOSE 443
# Wed, 12 Mar 2025 18:54:20 GMT
EXPOSE 443/udp
# Wed, 12 Mar 2025 18:54:20 GMT
EXPOSE 2019
# Wed, 12 Mar 2025 18:54:24 GMT
RUN caddy version
# Wed, 12 Mar 2025 18:54:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bcb83f0aff619c900e941cab3a8589e2379504ce3fc98eca1c6537baa4dd71`  
		Last Modified: Wed, 12 Mar 2025 18:54:34 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66650fb2116f44625fe4aa9242c888e770d7034ba618ad431e9c7caed4643b9d`  
		Last Modified: Wed, 12 Mar 2025 18:54:34 GMT  
		Size: 369.7 KB (369703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037ba3c778c9412f65eac8662451eb1183a350d3b712dc5f6bf6438674e3fbe6`  
		Last Modified: Wed, 12 Mar 2025 18:54:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4ae97f896590d8f7acb9de59fc6a38707c59461326b89dd4f6872f3817082d`  
		Last Modified: Wed, 12 Mar 2025 18:54:36 GMT  
		Size: 15.0 MB (15017945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb111f58b81fee05e952f051daeadb88f9326c6df0d6e3f7bc3c206bf08ac22`  
		Last Modified: Wed, 12 Mar 2025 18:54:34 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc525ed3bb002d164d8ad32a014508283e27d7febd91b964f73e255c7f53f698`  
		Last Modified: Wed, 12 Mar 2025 18:54:33 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ff145a2ae902c0cfa096f63ca127b87319d5ef3e3c94cccd9e42b152262b98`  
		Last Modified: Wed, 12 Mar 2025 18:54:32 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4256dcf2bf256325dbae0bee59d0482b4b99d7b3eea92f216db16e98f1d786`  
		Last Modified: Wed, 12 Mar 2025 18:54:32 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ecc18213568f6eb93fbde677b72c213decbead4ffe60f9ba7269631ea587aa`  
		Last Modified: Wed, 12 Mar 2025 18:54:32 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8b9aa99bdc4a1e78891e8216cde1123472f34771ed5cb1a89b3fc1973c7385`  
		Last Modified: Wed, 12 Mar 2025 18:54:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515300d81e0a99394b1378aeb4ce20cbd795c8e9b148ceb85da6d02569c697a7`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad3f6abbc105cb53e3f29e232d7dcf6bd82fc317d98a7a2b5bb5d3539b03145`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7b45f62872964bb6536e57d82cf62a914893ad4ac5964bd22d9cac7639d236`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3634c1ee0c97b1ab18896f905d43af42972e5b3d580d08e1ac5fe0e90fa3f367`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc0e8988f9135a335fc0a1f2a42b8e61c46e2696692e8ac0b3ed013d5bb4744`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b5c4dbee50096aa31258d400ab462b7727c063bfa1b1490de03a1cfbe8ad0e`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe5dd34988e058946524f61be4ffe91d0ec32e3e2d48e73c49219f0cdef2ca7`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a339e8d89fb174333cae1d26868433387caaa10b16aa8a872a525ce6ff20ff6`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9585ff132d954ea66174102ccd31309ea0625bfcbbfabc14869e090795e46bac`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 346.8 KB (346764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f4adc15b49fc2459e81f6e2d0763b88e3ef9669f85bb73d2fcbedf7c8e436a`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull caddy@sha256:fcd7b0c701fd0b2e28ad58ddb03c7b05dd089f697e5cfba9147891689cd30e7e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167335537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49538e47b959210c49da9cebcb6f0213eb7dcf03dc9fe3183b676ec2fa8713aa`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:46:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:12 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 12 Mar 2025 18:47:13 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 12 Mar 2025 18:47:23 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 12 Mar 2025 18:47:24 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 12 Mar 2025 18:47:25 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 12 Mar 2025 18:47:26 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 12 Mar 2025 18:47:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 12 Mar 2025 18:47:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 12 Mar 2025 18:47:28 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 12 Mar 2025 18:47:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 12 Mar 2025 18:47:29 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 12 Mar 2025 18:47:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 12 Mar 2025 18:47:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 12 Mar 2025 18:47:32 GMT
EXPOSE 80
# Wed, 12 Mar 2025 18:47:33 GMT
EXPOSE 443
# Wed, 12 Mar 2025 18:47:34 GMT
EXPOSE 443/udp
# Wed, 12 Mar 2025 18:47:35 GMT
EXPOSE 2019
# Wed, 12 Mar 2025 18:47:40 GMT
RUN caddy version
# Wed, 12 Mar 2025 18:47:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc0c4bb2d0220227f457267c48b8b05622b5a83afbc3026d4b39dd575c05de3a`  
		Last Modified: Wed, 12 Mar 2025 18:47:51 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089c0ab037c6a430ef561f326e9937208d21a1074d3e628a6c8f06298d985daf`  
		Last Modified: Wed, 12 Mar 2025 18:47:51 GMT  
		Size: 342.1 KB (342148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16b776cff3f47b06da06c9770771101745b5b95634f98465357d523645be9e6`  
		Last Modified: Wed, 12 Mar 2025 18:47:51 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0498cc3702dd49a2a399de9f37b93a5ce1645ff82dee9e973209f6d2e0609af3`  
		Last Modified: Wed, 12 Mar 2025 18:47:53 GMT  
		Size: 15.0 MB (15002278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c319e3076b2ee7245a9de9840d6c0b1c5d15c04a170af4eddafeafa3514e467`  
		Last Modified: Wed, 12 Mar 2025 18:47:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dad9eeb2454b823530c41c97f66efe6d456893b36304625af00c1c2631ec17`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80203d078e3ae007fb0bd7311b5369c46f3daf4b2218d1ea3bb14a8b8ec9a94`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d495466f2e8de169be7302068793587f6dd07bd6a16d1e84bf2af6d3c6495f`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25eaff429bee4ca466fb094a20a25119b336e3434bf79e2526b09b1bbe2d53e`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8cdf5b58fc5cc5a75bc299356534b7d54519857873ce9e3db3514839fbda01`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de0967722fde7ba30e01ed1474b95646eddd8ff9483ecb4026ecf70d42974f1`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dda06e0ea33b9df4124562577790d63bf894f2a705651c30073df07c3a2266e`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88daaa748bd3065007b925a424ed0167ce9aa4bd6250d279ebe7299ec31d7ee2`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e26ec9c4f5d853ac0439cc64c551e76a153acc77c93bb0af15d975a29553c41`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89a90cf3438bdbc9499ffb916150bc715a519e58ed3c3fe99b675160b47a870`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010c889dd5cbd5383e5ea985eafc6234d507416b5dd2637112947b6e422c863e`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd5e3905b9a5601b8d3b5c72f4db0bad5c4ba8a68bbd0f16579267460e35ce0`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eaf3c65c2679d95ef34b87941c305ec878285bc389ba79c379e9abb07b04d26`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3028a1484fe765d3859dc9f4bbb6a329b15671a5fa24253fcd35e9d3afb2905d`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 334.5 KB (334485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267f277f7ead5674a53c2926751dc033541be2211b3d97184034a08f84305629`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
