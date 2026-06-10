## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:0f149706848e208226b947a3ae52c5616d4dd191898b966744db99753bbb7659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `caddy:windowsservercore` - windows version 10.0.26100.32995; amd64

```console
$ docker pull caddy@sha256:51c1b116f8f4f6fda9de99f516961a77fa8500d30de0c00b65600d2be4ff82e7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2297924575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421fcd3c134ca86b455dc5dd056a06f5254731142cecefeee1cd79d193e538ba`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:13:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:26:05 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 09 Jun 2026 22:26:06 GMT
ENV CADDY_VERSION=v2.11.4
# Tue, 09 Jun 2026 22:26:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.4/caddy_2.11.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cd5ccfd86a4b40732cf715890d0dca5bf3f63adefec5a7914de85adf240c60ce7e5d2791631b88ef9758e46b23bb1730e020b9c5d696889740b284ffd4788e35')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 09 Jun 2026 22:26:14 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 09 Jun 2026 22:26:15 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 09 Jun 2026 22:26:15 GMT
LABEL org.opencontainers.image.version=v2.11.4
# Tue, 09 Jun 2026 22:26:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Jun 2026 22:26:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Jun 2026 22:26:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Jun 2026 22:26:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Jun 2026 22:26:19 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Jun 2026 22:26:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Jun 2026 22:26:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Jun 2026 22:26:21 GMT
EXPOSE 80
# Tue, 09 Jun 2026 22:26:21 GMT
EXPOSE 443
# Tue, 09 Jun 2026 22:26:22 GMT
EXPOSE 443/udp
# Tue, 09 Jun 2026 22:26:23 GMT
EXPOSE 2019
# Tue, 09 Jun 2026 22:26:28 GMT
RUN caddy version
# Tue, 09 Jun 2026 22:26:29 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde3f87c92fa7d0ae280c09db445ee43c8fe0d6469fc2c7ef39eccb597a279d6`  
		Last Modified: Tue, 09 Jun 2026 22:15:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e360bfbda1e55ce94d337b5396421db6756ed730505064e75449e4c60b02b88a`  
		Last Modified: Tue, 09 Jun 2026 22:26:38 GMT  
		Size: 393.8 KB (393813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5db79a01bebb17426e9b63f6c5a9351bd28366b97688d431c9adf7cf743e446`  
		Last Modified: Tue, 09 Jun 2026 22:26:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd01e82f72949e6e033175232354022fbc995decbeb33041869425875482067e`  
		Last Modified: Tue, 09 Jun 2026 22:26:41 GMT  
		Size: 18.0 MB (17999796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6904fb58d8987fbdd0326c44975ca3008acd8d3f925b652bd37073d14f72a01a`  
		Last Modified: Tue, 09 Jun 2026 22:26:38 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c67c318d923890a514bbbfbd42ceeccff672769626d04ca84c20e6bef69888d`  
		Last Modified: Tue, 09 Jun 2026 22:26:36 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf3b950dd87965e5d0fc17ef866484aff2c0684da8604ceb49718059d186e7d`  
		Last Modified: Tue, 09 Jun 2026 22:26:36 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c539e77d231f1c663e7736ad60597c429ed078d7a67fcfe8e15b9cd9d9cd2a1`  
		Last Modified: Tue, 09 Jun 2026 22:26:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:763dcbde3a685b5d2599dec4a51f16821a89dc3a2aef7915ec5cdb676534e3ad`  
		Last Modified: Tue, 09 Jun 2026 22:26:36 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe284cc5ceb3675165b1a3f4c94b1ff7273d52d584dec68fb17d67e7b3b9714c`  
		Last Modified: Tue, 09 Jun 2026 22:26:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52096844f631ca485ade87ba458bb042eb910c873ae05e1f1e3725ad538e1997`  
		Last Modified: Tue, 09 Jun 2026 22:26:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1920ec21746b52c33204de41aa730aa89fd34fadf22ef821221b8eba556bdfb`  
		Last Modified: Tue, 09 Jun 2026 22:26:34 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9d1281e77880d885857c611af2061356a1e62d0f432b3b6308ac326e08204c`  
		Last Modified: Tue, 09 Jun 2026 22:26:34 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11cff14d774f7dd06ea184d1d8186889ea5ece5376022233e98311f397a3fa2b`  
		Last Modified: Tue, 09 Jun 2026 22:26:34 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d4e104ab5016dccf3965ba864f0da5836043e7cfa36cd7e6cfd2e3cc197bb8`  
		Last Modified: Tue, 09 Jun 2026 22:26:34 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1dd04d423ce6e72102c59a3d1bed79b34980bcdd6f9e3152999d97de5c5c34`  
		Last Modified: Tue, 09 Jun 2026 22:26:33 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce261bf443f00253a550ae1beae6523ecddbacdff0db6394c2a9627e082adc2`  
		Last Modified: Tue, 09 Jun 2026 22:26:33 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46150411ec27e77a50981a8ad544762fb2fc0c8c7476cc7d954a5db44bdffb01`  
		Last Modified: Tue, 09 Jun 2026 22:26:33 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ae57b0fb0f96f19b0cf1337a131c6b7d01d1b0d14fa7ceec2897b4a984d6f0`  
		Last Modified: Tue, 09 Jun 2026 22:26:33 GMT  
		Size: 366.1 KB (366092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72c619e12cdea49a12f9bd7cc1f8b242b3c4b9a9eb7734b50755b1d5021b1ab`  
		Last Modified: Tue, 09 Jun 2026 22:26:33 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull caddy@sha256:140fcc7a6e190b97d806beddc8537da542465595002e9e8aac3cfcf9acd04e7b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2150950622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee2c6790e1e370908c8961c76b15b867108f1c453d0ce40b1af3bee187be27f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:28:01 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 09 Jun 2026 22:28:02 GMT
ENV CADDY_VERSION=v2.11.4
# Tue, 09 Jun 2026 22:28:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.4/caddy_2.11.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cd5ccfd86a4b40732cf715890d0dca5bf3f63adefec5a7914de85adf240c60ce7e5d2791631b88ef9758e46b23bb1730e020b9c5d696889740b284ffd4788e35')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 09 Jun 2026 22:28:11 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 09 Jun 2026 22:28:11 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 09 Jun 2026 22:28:12 GMT
LABEL org.opencontainers.image.version=v2.11.4
# Tue, 09 Jun 2026 22:28:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Jun 2026 22:28:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Jun 2026 22:28:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Jun 2026 22:28:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Jun 2026 22:28:15 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Jun 2026 22:28:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Jun 2026 22:28:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Jun 2026 22:28:18 GMT
EXPOSE 80
# Tue, 09 Jun 2026 22:28:19 GMT
EXPOSE 443
# Tue, 09 Jun 2026 22:28:20 GMT
EXPOSE 443/udp
# Tue, 09 Jun 2026 22:28:20 GMT
EXPOSE 2019
# Tue, 09 Jun 2026 22:28:25 GMT
RUN caddy version
# Tue, 09 Jun 2026 22:28:26 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02c9b713a469c080f684d10fd327070faf916b6d9b86f859442eebbd39bdd7b`  
		Last Modified: Tue, 09 Jun 2026 22:13:08 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b1ced4c8cfa0dbbd43af9b93396b3af2b091d98cbd1bea6a3ddad62a96687d`  
		Last Modified: Tue, 09 Jun 2026 22:28:35 GMT  
		Size: 494.1 KB (494064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f60bbec883fbc888217b91d0f1736a41acdca276532afee89bc5fdf94ce32d`  
		Last Modified: Tue, 09 Jun 2026 22:28:35 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba522b73e146dcae1eb1f6b94c4309dfc2ed50b2543860b7ab8501b57745fed2`  
		Last Modified: Tue, 09 Jun 2026 22:28:37 GMT  
		Size: 18.0 MB (17970188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c06a0832629ff422d4ade1ba10a0c86ff623f04caae7de03ac40cf77ed8c4c`  
		Last Modified: Tue, 09 Jun 2026 22:28:35 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffff5f23115b6af13fa1b2e7deef2d5a2976dec31238b904a5ee87760b4d885`  
		Last Modified: Tue, 09 Jun 2026 22:28:33 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16c09915e69a7ed78317c058b8420472631522a93ff39ce3c31806facad9460`  
		Last Modified: Tue, 09 Jun 2026 22:28:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b173b02d4fc9fb06437e8597e172c651eaacb6b645789159394afad94c33af05`  
		Last Modified: Tue, 09 Jun 2026 22:28:33 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce704cd1d3b50bba17eb54234fe2f423647f81369fd4435e14aeced3a13703d`  
		Last Modified: Tue, 09 Jun 2026 22:28:33 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c758878291e8ad8eeb7eeb698f6691cb053e6d428384143c9086ded8426e04`  
		Last Modified: Tue, 09 Jun 2026 22:28:33 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1623806b1a0ea02a5340f4eae7a87692ac1115a895a831283d79b908a591ecd`  
		Last Modified: Tue, 09 Jun 2026 22:28:32 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49698f8a7c3460243731067b2a60fd9bdb8a577c7d9df52a00813ef0dc45b9e7`  
		Last Modified: Tue, 09 Jun 2026 22:28:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97ca9f506dbcb70c6b905a82b256d8ae8ec7a8bc6c9a16794738bdb5ff46c0e`  
		Last Modified: Tue, 09 Jun 2026 22:28:31 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62533b1e80e1580bf0fc529d872ca32c04c11ffacbda48b5638ad42d5d9d3aa7`  
		Last Modified: Tue, 09 Jun 2026 22:28:31 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9c40f3270080665d0f39706de4e1dc7f07d250510c9ee6149ae78c89ca1cbf`  
		Last Modified: Tue, 09 Jun 2026 22:28:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7397445385fbf996a2443c3292565babfd3e54744e10831eeb699fb55575d319`  
		Last Modified: Tue, 09 Jun 2026 22:28:30 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93427fdf559bf2543c84e6916926f82c41f8df911013aed752654128450cc297`  
		Last Modified: Tue, 09 Jun 2026 22:28:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cfc50bf1fc1145ca044f46bf27e2739e26226d697d52edafbf6cb3f9e765af`  
		Last Modified: Tue, 09 Jun 2026 22:28:30 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d07fe0891d24efe790869dff272546f15bc7571a36912ccc161c15c3cb0baf4`  
		Last Modified: Tue, 09 Jun 2026 22:28:30 GMT  
		Size: 338.6 KB (338615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36af44d06925143e0ffa6271d7e6f569b18767de9fa6bda62decc87fff083bb5`  
		Last Modified: Tue, 09 Jun 2026 22:28:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
