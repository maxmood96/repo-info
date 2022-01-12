## `caddy:windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:a9e92c548fe7a4f2ba833491ab4c485649b81a9cee1b0f2c1011e1d94d117240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4886; amd64

### `caddy:windowsservercore-ltsc2016` - windows version 10.0.14393.4886; amd64

```console
$ docker pull caddy@sha256:233a258cecc5be55e8f0ea9b975d0a4ac5997106af403053e9f90750f9f908da
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6291025981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9182db4cbb2d6fb6af4711c4020c4b88883dbabd90df2f7765b5acf7b6a36a96`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 06 Jan 2022 14:33:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Jan 2022 19:14:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jan 2022 06:29:07 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 12 Jan 2022 06:29:08 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 12 Jan 2022 06:30:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 12 Jan 2022 06:30:15 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 12 Jan 2022 06:30:16 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 12 Jan 2022 06:30:17 GMT
VOLUME [c:/config]
# Wed, 12 Jan 2022 06:30:18 GMT
VOLUME [c:/data]
# Wed, 12 Jan 2022 06:30:19 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 12 Jan 2022 06:30:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 12 Jan 2022 06:30:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 12 Jan 2022 06:30:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 12 Jan 2022 06:30:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 12 Jan 2022 06:30:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 12 Jan 2022 06:30:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 12 Jan 2022 06:30:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 12 Jan 2022 06:30:28 GMT
EXPOSE 80
# Wed, 12 Jan 2022 06:30:29 GMT
EXPOSE 443
# Wed, 12 Jan 2022 06:30:31 GMT
EXPOSE 2019
# Wed, 12 Jan 2022 06:31:09 GMT
RUN caddy version
# Wed, 12 Jan 2022 06:31:10 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8428508ffd63b4af1ba690ec41e82a116f10ec6c3fb70962348f5448d42e5835`  
		Size: 2.2 GB (2208216859 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9b5116c05ddf6ecb5a348f7628e3f3264afbb9909d86798316dbaff4a0e991a2`  
		Last Modified: Tue, 11 Jan 2022 19:35:13 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e465f058579c4d79c1199cedd5286fc4d992a5befe43c0606f35ffa3230434`  
		Last Modified: Wed, 12 Jan 2022 06:35:09 GMT  
		Size: 352.3 KB (352302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd504dbb2b04267c2d233361cdd455cca76512d5143d85f5d4738d62933eae5`  
		Last Modified: Wed, 12 Jan 2022 06:35:08 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1042de120ef2b2719c45e4c894c8ba85def07af1026f12b09f6db2c313c3467c`  
		Last Modified: Wed, 12 Jan 2022 06:35:21 GMT  
		Size: 12.1 MB (12144738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01de2ac0687932d5d12177faa3601c4fc5eb6482992bc0cdda7ddf4a82a53692`  
		Last Modified: Wed, 12 Jan 2022 06:35:07 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46a4039150ef71928d2f495e5942a3f50218e903c1a7e40adcd9599436501ed`  
		Last Modified: Wed, 12 Jan 2022 06:35:07 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34078ca3059b4b044bee8cb9d400dc60811b9eec5b09fc1427ea7650d3445a0`  
		Last Modified: Wed, 12 Jan 2022 06:35:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0c4dd249b86f0977b7b132a66c48c7f461cf31fa4de79a128b88dbeeccf278`  
		Last Modified: Wed, 12 Jan 2022 06:35:05 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efefc1bf7f1db1276ba069e897a9aa0047b1591acf13cec6638d8b5593f1fadf`  
		Last Modified: Wed, 12 Jan 2022 06:35:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76437ce17b3e5637e1e639a444f54bfadb9e3efd9b55650ad99e98ba12ddb6dd`  
		Last Modified: Wed, 12 Jan 2022 06:35:05 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a15fde1ce9b05beb8cda3f8b11e0dc2b70bc54cee44de541f621c4315381a5`  
		Last Modified: Wed, 12 Jan 2022 06:35:05 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049449a144b9913ed2991debfd2c985535e9a2ca642ec416958def85fb90c30f`  
		Last Modified: Wed, 12 Jan 2022 06:35:03 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de353153972073df7d6bc0cad4513db2362aca7d562ab99cce052103a921a113`  
		Last Modified: Wed, 12 Jan 2022 06:35:03 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712ab20361dcedadf75156d50b922d320af3f8fe4c405005a48aa10cd2bd6ee7`  
		Last Modified: Wed, 12 Jan 2022 06:35:03 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf57e8a2631ddf98bcf45e599d5d680d736fc3e25f6ac5bac2360382b7d60bb9`  
		Last Modified: Wed, 12 Jan 2022 06:35:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0055b2df47960fdd8ede6c71301e52030a04754a217ef7257d0e4663c8f2c0`  
		Last Modified: Wed, 12 Jan 2022 06:35:03 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8d92f1c23c1ecf22e6d3e828185dfd895277f95de1291644333165b3134565`  
		Last Modified: Wed, 12 Jan 2022 06:35:00 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d69885494ed7409cc17c26b0ef0e59dbc18c6232a355921db62df44083bca4b`  
		Last Modified: Wed, 12 Jan 2022 06:35:00 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17f83455892b3042ca93758bf12f1e3dd96680528b27d2280925699168986cd`  
		Last Modified: Wed, 12 Jan 2022 06:35:00 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0a28eedbd96ae90ba5dd9f14cc7bd4fe6a6480e487a446d7379af09780327f`  
		Last Modified: Wed, 12 Jan 2022 06:35:01 GMT  
		Size: 300.8 KB (300767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8f99304a19b8711bf997dfbfd7a23b55bc8d94229239c3b074d3c5560326ee`  
		Last Modified: Wed, 12 Jan 2022 06:35:00 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
