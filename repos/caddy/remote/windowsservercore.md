## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:f7f8dc0763df47cc1285260431092e16536f20edd4d1eb1dc36d9665c0d74ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `caddy:windowsservercore` - windows version 10.0.26100.7462; amd64

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

### `caddy:windowsservercore` - windows version 10.0.20348.4529; amd64

```console
$ docker pull caddy@sha256:978ef3477b8fdb8cbea33aed19a9b837c10581a8de34507baa1c87ab03fbd279
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1797325008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d936cc1fede84b35c0d9283d2320d3eac40f574c7ee5a7ff55a9ab994285e9b2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:40:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:48:58 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 09 Dec 2025 20:48:58 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 09 Dec 2025 20:49:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 09 Dec 2025 20:49:07 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 09 Dec 2025 20:49:08 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 09 Dec 2025 20:49:08 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Tue, 09 Dec 2025 20:49:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Dec 2025 20:49:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Dec 2025 20:49:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Dec 2025 20:49:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Dec 2025 20:49:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Dec 2025 20:49:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Dec 2025 20:49:13 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Dec 2025 20:49:14 GMT
EXPOSE 80
# Tue, 09 Dec 2025 20:49:14 GMT
EXPOSE 443
# Tue, 09 Dec 2025 20:49:15 GMT
EXPOSE 443/udp
# Tue, 09 Dec 2025 20:49:16 GMT
EXPOSE 2019
# Tue, 09 Dec 2025 20:49:21 GMT
RUN caddy version
# Tue, 09 Dec 2025 20:49:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323d6571ea86abd0158f636013b118b7f30b9fdb6aa70348177419fb48c2c825`  
		Last Modified: Tue, 09 Dec 2025 20:41:56 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d787c99f495c9b7612aaac2f8c5953c2b0d12439d9cd3a3b73e15c9821b197`  
		Last Modified: Tue, 09 Dec 2025 20:49:38 GMT  
		Size: 499.6 KB (499624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46faf54d55ff6f0330741de430f2ee181229d73829ac30ef9414befb43eaed89`  
		Last Modified: Tue, 09 Dec 2025 20:49:38 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bbb49265b2518fdec8b04dbaeb15055b9ed4c9a2465693bc4ef01b770553c2`  
		Last Modified: Tue, 09 Dec 2025 20:49:40 GMT  
		Size: 16.6 MB (16570194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b30a55e73225b95d49ed42719d9f52a72640a48fe80c36dd66fb7cf50c5fea`  
		Last Modified: Tue, 09 Dec 2025 20:49:38 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ec907fe1c6568f25efca53fe759cf8d3f7ff1b9396bdc6b03810f1bb8eb311`  
		Last Modified: Tue, 09 Dec 2025 20:49:38 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea7bb0296617a4bce4d009d581aad5a0babf608fb83ab1d8f3711fdc4b83c0f`  
		Last Modified: Tue, 09 Dec 2025 20:49:38 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e118664343182b1a535b86f1e9485f7862557d7d7eb3f21c27fcb8e4a0b9361`  
		Last Modified: Tue, 09 Dec 2025 20:49:38 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e199424308a6fd8fab7b48e8ad963af53473b2e7c28cfe20c49640fd8ea35e3`  
		Last Modified: Tue, 09 Dec 2025 20:49:38 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b694e8f53525ac1048e1c3718ea635e138f6ef6752c349e58d3c00f1872ff07`  
		Last Modified: Tue, 09 Dec 2025 20:49:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9aa536deaea880cd8236281ec50955d8211ca7f1644fdcf42d405ea094e354f`  
		Last Modified: Tue, 09 Dec 2025 20:49:39 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:771d826dda175c21297f7c26f0191f7965bbbfa07f485ad12dc07341a02c2b3b`  
		Last Modified: Tue, 09 Dec 2025 20:49:39 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54100b746f394594a87d726e95a7b9ee744afb4d9855b8f653c6fe235799b3d`  
		Last Modified: Tue, 09 Dec 2025 20:49:39 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0263b00750effc6f300d5246366e199aa84dfe4026378df2d09f3aaf914d986d`  
		Last Modified: Tue, 09 Dec 2025 20:49:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b70bbf0f2d8707992fd0b19f5d640db14e74425c42bed8559d5274a36f46f64`  
		Last Modified: Tue, 09 Dec 2025 20:49:39 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa7c0088b06d8a8f933c5afae52be8316c3f1ea35ec53a7765e1647c52f4bb3`  
		Last Modified: Tue, 09 Dec 2025 20:49:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f913bf2580834b3e912fd3d3e2f514847cf6302421fc9bc5e57ddfb08d0404e`  
		Last Modified: Tue, 09 Dec 2025 20:49:39 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74d490814233e683827c0e5e6221d34d086db553973143048188658d254ca53`  
		Last Modified: Tue, 09 Dec 2025 20:49:39 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e0f763febce5e11272dd98712a155e4f2f801f59bc2bb283da490abc7e614d`  
		Last Modified: Tue, 09 Dec 2025 20:49:39 GMT  
		Size: 353.6 KB (353620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97f97c13e343dadb26d757411612b5ccab4487c9110157f7c95ea58aff7662a`  
		Last Modified: Tue, 09 Dec 2025 20:49:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
