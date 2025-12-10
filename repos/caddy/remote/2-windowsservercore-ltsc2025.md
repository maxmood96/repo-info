## `caddy:2-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:b05546ec367e1cca616b5915b843adb0e43ad55320600c0b80a5cc2adb527cda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `caddy:2-windowsservercore-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull caddy@sha256:f1252de56df5009719f763901220ace93db2a809d9f35e9c04898ba1619c4716
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3270448570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b1f7217c0661cf79f7ad33d4b15b09ca36de24d5aa965e9685c51cd47bb015`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:35:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:49:44 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 09 Dec 2025 20:49:45 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 09 Dec 2025 20:49:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 09 Dec 2025 20:49:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 09 Dec 2025 20:49:54 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 09 Dec 2025 20:49:55 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Tue, 09 Dec 2025 20:49:55 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Dec 2025 20:49:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Dec 2025 20:49:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Dec 2025 20:49:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Dec 2025 20:49:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Dec 2025 20:49:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Dec 2025 20:50:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Dec 2025 20:50:00 GMT
EXPOSE 80
# Tue, 09 Dec 2025 20:50:01 GMT
EXPOSE 443
# Tue, 09 Dec 2025 20:50:02 GMT
EXPOSE 443/udp
# Tue, 09 Dec 2025 20:50:03 GMT
EXPOSE 2019
# Tue, 09 Dec 2025 20:50:08 GMT
RUN caddy version
# Tue, 09 Dec 2025 20:50:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddd1b21f748d7bd5a12a32efdb01af38a511a65bb4cea3055088ab5607942fc`  
		Last Modified: Tue, 09 Dec 2025 20:44:54 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838391e1b7a050ea171f8630744858d13e1bf2b67627078e73d92376fe7aaf44`  
		Last Modified: Tue, 09 Dec 2025 20:50:26 GMT  
		Size: 367.6 KB (367633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992dc692530153ea17e970aa41952eca262b04248f1b23a512b278a3756bf966`  
		Last Modified: Tue, 09 Dec 2025 20:50:26 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ac3237d04d0063dbca3e8b4bb8a69688ff12416ec23533af3e08d051c45f65`  
		Last Modified: Tue, 09 Dec 2025 20:50:28 GMT  
		Size: 16.6 MB (16582943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83656c43b6019cd16bafbf59728c734211c8fd33b864d6f16331b422d0df505c`  
		Last Modified: Tue, 09 Dec 2025 20:50:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1f36fd3606d55da0bb080e7727ac85d1bb657a873cd77667c00c174e6f2de4`  
		Last Modified: Tue, 09 Dec 2025 20:50:26 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f38e9f33c9b4bc750bc36758642bde79b3ab28a445ffbec0a9b3d2954feacf`  
		Last Modified: Tue, 09 Dec 2025 20:50:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c431a7a861c911d6722de40544f50c2648647209fdfe7a890d97fb3aa58a24`  
		Last Modified: Tue, 09 Dec 2025 20:50:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f09afb27f9139f2546c9ebe529e7d77b250af0e3f4469d9b99bbe60aaf51161`  
		Last Modified: Tue, 09 Dec 2025 20:50:27 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466bb6fc1010cbcd5d21ded8ecfa027b8dd76267715e326bb5bec5d1f410819c`  
		Last Modified: Tue, 09 Dec 2025 20:50:27 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df154dd9d53baf25d8cee3d67ae1864680dc4261457a5252740874c6bdcfbb21`  
		Last Modified: Tue, 09 Dec 2025 20:50:27 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1058b0a7f432a4b123b759bde7553fc2f624e54b2ad779ee36100dca5bc76c1`  
		Last Modified: Tue, 09 Dec 2025 20:50:26 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4cdba4d96476ccacf92632d3135391442408e36e457f4508a3d464257706ebe`  
		Last Modified: Tue, 09 Dec 2025 20:50:26 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2f95ccee1e8aa287fc5715324db2687f2700155c468312fa8353dd2851db95`  
		Last Modified: Tue, 09 Dec 2025 20:50:26 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5598f8e9f65a1cccc507b4d6a0cc3ac082009a08de5fe96eaf52e2e27bedac47`  
		Last Modified: Tue, 09 Dec 2025 20:50:26 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13f753db24dd9e3e99f34206c38a6aa18bd3f9de61fd7beebdac49239c7906c`  
		Last Modified: Tue, 09 Dec 2025 20:50:26 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a244e1931213f483def5c8eb565f061e6212b5cd0d5ae9f284a0087e3f092ca5`  
		Last Modified: Tue, 09 Dec 2025 20:50:26 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467cb3ce5ceff899e7ba5d5763a926ffd6bb3f36a02c39ec499e7359f82cda26`  
		Last Modified: Tue, 09 Dec 2025 20:50:26 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52202732909ba1efbab6eac4c8e87a4143d5092e136f9d17158a786c55e3c15b`  
		Last Modified: Tue, 09 Dec 2025 20:50:26 GMT  
		Size: 355.1 KB (355069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e71b5dc1aa4fc67a5516abcb9bdca20f41dcd53e8dcdde3a4f96eb5aa3ea2d`  
		Last Modified: Tue, 09 Dec 2025 20:50:26 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
