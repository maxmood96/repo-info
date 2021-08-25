## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:e5e5fb2f39e631146f8c890d36e0a2e6e150c66d5ee959a580002e4032761392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2114; amd64
	-	windows version 10.0.14393.4583; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.2114; amd64

```console
$ docker pull caddy@sha256:277245d2976e25118dde31aa817da26aab9a54b716478e335e7e47a655680fdf
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2698757766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efdb54faaf1277fc5d472259e6d51ac14101b59691359db53c189a9f55df03c8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:21:11 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 25 Aug 2021 19:21:12 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:22:15 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 25 Aug 2021 19:22:16 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 25 Aug 2021 19:22:17 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 25 Aug 2021 19:22:18 GMT
VOLUME [c:/config]
# Wed, 25 Aug 2021 19:22:19 GMT
VOLUME [c:/data]
# Wed, 25 Aug 2021 19:22:20 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Wed, 25 Aug 2021 19:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 25 Aug 2021 19:22:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 25 Aug 2021 19:22:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 25 Aug 2021 19:22:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 25 Aug 2021 19:22:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 25 Aug 2021 19:22:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 25 Aug 2021 19:22:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 25 Aug 2021 19:22:28 GMT
EXPOSE 80
# Wed, 25 Aug 2021 19:22:29 GMT
EXPOSE 443
# Wed, 25 Aug 2021 19:22:30 GMT
EXPOSE 2019
# Wed, 25 Aug 2021 19:23:15 GMT
RUN caddy version
# Wed, 25 Aug 2021 19:23:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc78244c47d63e7118efa5a81aeac258859631816cf0d2e335045eddd6d4562c`  
		Last Modified: Wed, 25 Aug 2021 19:29:08 GMT  
		Size: 390.1 KB (390074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308e85659c5ef3d6f1826cce92e5c35cbda668ec96e58661902ea89472385a68`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ad534458f62e8592943908290a647cce35c3f5ed0761b80f7d17f55393900e`  
		Last Modified: Wed, 25 Aug 2021 19:29:10 GMT  
		Size: 12.0 MB (12023423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e1aa1a15f7618a90c91ce39aeb28f0b14d0fb039a0a5c387e2d7a4460443aa`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26a259cd0cf699d1891ff65f72aaf75b8b53d32409fdbab40fa8aa3594f4edb`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb72b357bee0361ca5587e675d3a832276f086a2d6535147bfe92a000cf044f`  
		Last Modified: Wed, 25 Aug 2021 19:29:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cbe28f726b8cddbd0398281cfc45f2dc82f378bef80fa1dfe4dec201451721`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233a73648024b9f42aeeda4c4309ba545e089e6943b686c93ea09cec6ac83373`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ad45ece5f60db2673be4be17ca0ac1ff391d32d88f7a84e2e671fca6744e0`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a424371920e55efd886bea3b4671eca80436677674986f299b919e72c49d4289`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c2b299f27503c9be94a9a16c137b08ba7e2b84cc07b96a281d4b2886b231f0`  
		Last Modified: Wed, 25 Aug 2021 19:29:03 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d7c231726719db989f9746b39a4b4b9b54646376e1dc36c124a1401fc15132`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa20ae0be18044dcf67b8832f125744410261cc8601712176399a3cd632b8843`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1b94a88e7f4db3aa538dad13b42b51168525142c8268098dbe8a7175decee6`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0f35247abb67063d217ea9963f29270e1716b21409196f0e935710342a9dd9`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fa12b6daf14192bb460b568c8c3f65625b384fbcfa33e4b227d39de751374d`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43dbbbd0c30fabb616088a2f902ad0177c216707c4e134d10b9a1cd4fde8cb`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee931681f757a39ac6ce152aa1d64f251a68f63dca6dbe3459c2cec9bed0d90e`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6deb6e04a956a5c619ff2eb344a4e5fcf8384d890b8120ce2ffd91cf20e0b5f`  
		Last Modified: Wed, 25 Aug 2021 19:29:00 GMT  
		Size: 320.7 KB (320709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426b510aa21fdb81bb0a2156b0a977a69ea8187f959ceb05869b1450d9359814`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.14393.4583; amd64

```console
$ docker pull caddy@sha256:bd0551e2eeef6d131272af5e4214599dfc85e2a18d421264005a4f8dc3025a02
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6283675023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f96c9f880047fab4000d8bad0dceb15c3e478898181805e15b864f3ae980f11`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 25 Aug 2021 13:16:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:24:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 25 Aug 2021 19:24:21 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:25:22 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 25 Aug 2021 19:25:23 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 25 Aug 2021 19:25:24 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 25 Aug 2021 19:25:25 GMT
VOLUME [c:/config]
# Wed, 25 Aug 2021 19:25:26 GMT
VOLUME [c:/data]
# Wed, 25 Aug 2021 19:25:27 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Wed, 25 Aug 2021 19:25:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 25 Aug 2021 19:25:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 25 Aug 2021 19:25:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 25 Aug 2021 19:25:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 25 Aug 2021 19:25:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 25 Aug 2021 19:25:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 25 Aug 2021 19:25:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 25 Aug 2021 19:25:35 GMT
EXPOSE 80
# Wed, 25 Aug 2021 19:25:36 GMT
EXPOSE 443
# Wed, 25 Aug 2021 19:25:37 GMT
EXPOSE 2019
# Wed, 25 Aug 2021 19:26:16 GMT
RUN caddy version
# Wed, 25 Aug 2021 19:26:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f888b02e4880b5280aedf776d35ce62a07f97c9f4671b4e167d0fadfbcd663f`  
		Last Modified: Wed, 25 Aug 2021 13:39:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c9dee8014da227cc8c6b8d14f6464fefc307c265b07a34d6e2ccc5de24a92a`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 352.7 KB (352700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d26c5819d131639ab53b8e099ab2ed93c63f759072d3a5ce4b9f69f13b8a66`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcb3ea0fdbcaf7cab1dbac86676ab00ca78ebf68e3b5c476c5984201c357976`  
		Last Modified: Wed, 25 Aug 2021 19:29:35 GMT  
		Size: 12.0 MB (12025369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7a331953cb55eb8482f8b09c1ccb30b06198b0da91f196aa230d56d4f626c3`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65c66a58bae64f63c34265474f15131687cba250a5cbeb2166a25d383630b68`  
		Last Modified: Wed, 25 Aug 2021 19:29:31 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b60346916eaf0cd70873400273d0f0de4f72aa7ee5a5bd6a8cfbe446d62499`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe74af1f53b1dc6d2f58a23760f463877d707150f1cae25c0ca6a727c64cd7e9`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4467e0d432e5bba7c8e197c057837e438ae63c8748b9765a8d7591c0ea12c0`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c92db8b514f6d653c3d0ba5a7e695e808f5880504124fb94648c10590f7f3c9`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d63a5575b8310dcb9cbe40352e7753a4bb8f66f1c3fbea055abda03136638d6`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1415f534f6818ea980cf13f9a08c0efb9d60c9f86760129563e203ba93e399c8`  
		Last Modified: Wed, 25 Aug 2021 19:29:27 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be354de1af39afc991030861814f135bfde0267a02f004fd4caf9ccc31d0bfd`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a0ebb3c5c8d126c85ccbad571fef0051ac62cfec3fe5885c82110381049ed9`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4893f40ed74354bd380ee49a7141c654ea10f5a43f1e050539bde502c7214c9f`  
		Last Modified: Wed, 25 Aug 2021 19:29:27 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffd03947508d81a8a5c939b4a1697e4cf18bc8722cc1650732f8df2c6924941`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19c43d724632362e78f09ee6bf53a8359cdd6db65300cb3687f2ad3a59e1a5d`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baeaec774cf06dd02e7ebdf8d5e9aa9b8d4578a60c7a54ce84421910922396b7`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fb3d76a117ff8038563015df19972676ff4aea085431ef698f57799559b334`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9341d5f41a06e42738b97ffd6ca2835680879ba4113b882c5cd8accd857c0551`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 305.6 KB (305571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd0dece66bb4a5f39d723d7d27311fa04d1de60c084735f41cb588c7b4d5701`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
