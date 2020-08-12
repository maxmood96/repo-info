## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:721776712ea5abbd5baef79a760bc7d1ee00e50d6f45e619eb642aec031b5305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64
	-	windows version 10.0.14393.3866; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.1397; amd64

```console
$ docker pull caddy@sha256:6fe7722afe7f2a04904666b05e8b95bacc3ace24dc70c232c3da08a456a5eb4e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2363011231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2edf58a1b9a89ae4c32c405481fbdadf112e71860ce5ae3289e300961996bc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Tue, 11 Aug 2020 20:36:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 18:20:12 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 12 Aug 2020 18:20:51 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 12 Aug 2020 18:20:52 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 12 Aug 2020 18:21:25 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 12 Aug 2020 18:21:26 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 12 Aug 2020 18:21:27 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 12 Aug 2020 18:21:28 GMT
VOLUME [c:/config]
# Wed, 12 Aug 2020 18:21:29 GMT
VOLUME [c:/data]
# Wed, 12 Aug 2020 18:21:30 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 12 Aug 2020 18:21:30 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 12 Aug 2020 18:21:31 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 12 Aug 2020 18:21:32 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 12 Aug 2020 18:21:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 12 Aug 2020 18:21:33 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 12 Aug 2020 18:21:34 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 12 Aug 2020 18:21:35 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 12 Aug 2020 18:21:35 GMT
EXPOSE 80
# Wed, 12 Aug 2020 18:21:36 GMT
EXPOSE 443
# Wed, 12 Aug 2020 18:21:37 GMT
EXPOSE 2019
# Wed, 12 Aug 2020 18:21:53 GMT
RUN caddy version
# Wed, 12 Aug 2020 18:21:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:43065500f09f35124a5d71517aa493fd23ad75660682600f7f6b40aa7629ac78`  
		Last Modified: Tue, 11 Aug 2020 20:54:54 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee0c1b06dd703a6d5247afb68291748c99b4f9de1c9e2ae9e90b6115b87117a`  
		Last Modified: Wed, 12 Aug 2020 18:26:38 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c2c051346b0f0aef066e3b4ad72a01809f8403d1021122c7ad6c80579624d9`  
		Last Modified: Wed, 12 Aug 2020 18:26:38 GMT  
		Size: 9.2 MB (9156082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a07e46ea2519a094a5803c355dad838f87a366d6743b5f08594933603918e6`  
		Last Modified: Wed, 12 Aug 2020 18:26:35 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54bec25576d66f070dadca03df4f2326052c693797df2cf7cf08f802ea4ab629`  
		Last Modified: Wed, 12 Aug 2020 18:26:46 GMT  
		Size: 17.7 MB (17676360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9439354479a9b9ea242f62263aa94dee60053ab3adb58d309d98e64b44fc0016`  
		Last Modified: Wed, 12 Aug 2020 18:26:33 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16291dc3e63bda8ff560d924dc41414b9dc32bad594914bc6ab097c2a948781`  
		Last Modified: Wed, 12 Aug 2020 18:26:32 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedab8476a2860f0d7de59a0b4f06b6eaf1f3ded4ff5790d1b3f5a4b4cbc6bcb`  
		Last Modified: Wed, 12 Aug 2020 18:26:32 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8649d8c083bd21fda11da6f2529e851f3b287690ee965e0998941fec946fd5`  
		Last Modified: Wed, 12 Aug 2020 18:26:33 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faddf1f4f68667d81626e152e392a3d61cdc83170e14ff63d891d3941b38ed9`  
		Last Modified: Wed, 12 Aug 2020 18:26:31 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30332dcef86cb8c8e6f3245d12535df0ebf06190116bb6348465cf6912bfb554`  
		Last Modified: Wed, 12 Aug 2020 18:26:30 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f5b14ecf0c1f35c6670fa00efbbcc272a38e1416f3acc8b160e51dc6e115cb`  
		Last Modified: Wed, 12 Aug 2020 18:26:30 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191f0f12602e0731b99f83f0398d369d0873f08ad3d082f80b19ddeb8257f2e7`  
		Last Modified: Wed, 12 Aug 2020 18:26:28 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d883df69b591966b718187d2d291242be743bd4fead8120733ac08479b0f13b3`  
		Last Modified: Wed, 12 Aug 2020 18:26:28 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4150978f9389a2ebf8b36a8e2ba95ab279748935ee59a5391387a140f9213371`  
		Last Modified: Wed, 12 Aug 2020 18:26:28 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa221c48f90ca5f19482982a18f17d06c5ee39094c7f1834c6dd56bb335d0e83`  
		Last Modified: Wed, 12 Aug 2020 18:26:28 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74fccce77db6e74ca68b1979012aee5727734baad68fe9c05261cb24d7dcb71`  
		Last Modified: Wed, 12 Aug 2020 18:26:27 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d040f084082fb82dc8d77d688563c38c86c7ced0e30f81491b5ef6930a618e9e`  
		Last Modified: Wed, 12 Aug 2020 18:26:25 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0150e9e30dbce51e16baa13a2cfdf8f8c357bf83402bd5efc9261b6c1cca2c`  
		Last Modified: Wed, 12 Aug 2020 18:26:25 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4964b178be4f0bf5b7acbc0571d22fdaf33dacf0dbf6018c3aaea694b66779c`  
		Last Modified: Wed, 12 Aug 2020 18:26:25 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a67939412cb526125d5df3254e959808d9f0a8a3dea02cb75d122f60f18b0ac`  
		Last Modified: Wed, 12 Aug 2020 18:26:25 GMT  
		Size: 290.2 KB (290230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e0a69b1373af956fc482a92110fc6b9d21ce160e6e802f33c3ed5e5c998c27`  
		Last Modified: Wed, 12 Aug 2020 18:26:25 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.14393.3866; amd64

```console
$ docker pull caddy@sha256:2e72d4c6fad10d389ee9269c3afb2c59e086bdff525f75b20d54f5955c54f83a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5771148566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5911145356d44266e7c91c58c32736a59af78e56944c17913ce02544739e62fd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Aug 2020 20:31:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 18:22:08 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 12 Aug 2020 18:23:27 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 12 Aug 2020 18:23:28 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 12 Aug 2020 18:24:51 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 12 Aug 2020 18:24:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 12 Aug 2020 18:24:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 12 Aug 2020 18:24:55 GMT
VOLUME [c:/config]
# Wed, 12 Aug 2020 18:24:56 GMT
VOLUME [c:/data]
# Wed, 12 Aug 2020 18:24:57 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 12 Aug 2020 18:24:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 12 Aug 2020 18:24:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 12 Aug 2020 18:25:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 12 Aug 2020 18:25:00 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 12 Aug 2020 18:25:01 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 12 Aug 2020 18:25:02 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 12 Aug 2020 18:25:02 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 12 Aug 2020 18:25:03 GMT
EXPOSE 80
# Wed, 12 Aug 2020 18:25:04 GMT
EXPOSE 443
# Wed, 12 Aug 2020 18:25:04 GMT
EXPOSE 2019
# Wed, 12 Aug 2020 18:25:47 GMT
RUN caddy version
# Wed, 12 Aug 2020 18:25:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:32838d9637dc39d4acee78700b0f93d6c8c9d2db755f12c8009c1b51687d3fbd`  
		Last Modified: Tue, 11 Aug 2020 20:54:28 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43a86f007ceca8251e384223d65f32931f84f5eaab12f53e7aa26d516a017b3`  
		Last Modified: Wed, 12 Aug 2020 18:27:15 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9c5d103ff70248238b4264ec049dbdeeb49fb8c6ebd2f3ac67e87ee0c2ccad`  
		Last Modified: Wed, 12 Aug 2020 18:27:15 GMT  
		Size: 9.9 MB (9885669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90fb79de83d5704b382045fdca2eae660b0e6a785ca2e3430dfd1133e0e9122`  
		Last Modified: Wed, 12 Aug 2020 18:27:11 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2693981b98fcce2e17fc0b4bf3f20cb5967a773969303ab342383be6740739a3`  
		Last Modified: Wed, 12 Aug 2020 18:27:18 GMT  
		Size: 22.9 MB (22854209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b034aa5ed985b9516ddf63ec579597e71ca87b3abbd520aa9b97ab2be96dc47`  
		Last Modified: Wed, 12 Aug 2020 18:27:11 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2109a5f31d92a8711132ded43517c75a955ce39c775240d1c57521798117e7e`  
		Last Modified: Wed, 12 Aug 2020 18:27:10 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fff09751cabb85773ed00a407970132d5ebb804fb8e582c7e568d159f00e42`  
		Last Modified: Wed, 12 Aug 2020 18:27:08 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca3f5fd2aa85425fe8a61f1588e9c8e8e81636f61c5d958e50a44ede3b9370d`  
		Last Modified: Wed, 12 Aug 2020 18:27:08 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808cbe3437a1a12f04ac41855557ca1d69d7ee7fd33a3f235109599166a83996`  
		Last Modified: Wed, 12 Aug 2020 18:27:08 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795ef36d78825131d8e347fcaacfa951d026b1a6ba22f5ba1ed6901ec8092d4f`  
		Last Modified: Wed, 12 Aug 2020 18:27:08 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f28801f98ff78ea7fc378ac7b7a0368e183ad612050def5c78e9642a6378399`  
		Last Modified: Wed, 12 Aug 2020 18:27:08 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88279510d22b36b9eeb40fff3bd12114dc2f6b9f4833f88d9c97d93835c55c8`  
		Last Modified: Wed, 12 Aug 2020 18:27:06 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7d56735e63ef7963447f7aa0bd49914d031c399e1fabb9262c87e8cf4d9fa8`  
		Last Modified: Wed, 12 Aug 2020 18:27:05 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6047705d42f4a7a216a4d1cb3e2083b895874cedbd1ae40e6eb2c7008c6fc684`  
		Last Modified: Wed, 12 Aug 2020 18:27:05 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32ac73604d42daeaf8c539a5cb80ffbc7f8e3a7e82897d97869d50e1a0bf420`  
		Last Modified: Wed, 12 Aug 2020 18:27:05 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33651212c65fcca362e652e1b0f8dae59bccd9b6a2e67c6b6a1de274f075a21`  
		Last Modified: Wed, 12 Aug 2020 18:27:05 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c29359fbbdbd6c36070f1d4bff445df9e41117fa0d77e023401e11bee1763f`  
		Last Modified: Wed, 12 Aug 2020 18:27:02 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca98bb596b991bdab98937fa187545269ab725c7f6930fcea9ca191e30f9c3f`  
		Last Modified: Wed, 12 Aug 2020 18:27:03 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7789a12a5d8f91e9b2a5e0ce0821192e0ad6977159a96f4f21d54dd5bbc132db`  
		Last Modified: Wed, 12 Aug 2020 18:27:02 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602852425a5a34a59c885f93d92cbc027a26dc3dbd7f00c9522c99036c8268f5`  
		Last Modified: Wed, 12 Aug 2020 18:27:03 GMT  
		Size: 239.7 KB (239658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3f8533a57e3bbd15a96c7a518b4c975c8bd3bfaec7ad49eb42e2fffcae0692`  
		Last Modified: Wed, 12 Aug 2020 18:27:03 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
