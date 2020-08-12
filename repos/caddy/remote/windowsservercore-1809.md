## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:c11b198f695a66e3690d752dd7dc202e03e06d4804d8aec6f953d1edbbe7c23b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.1397; amd64

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
