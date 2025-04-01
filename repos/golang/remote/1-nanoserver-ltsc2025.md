## `golang:1-nanoserver-ltsc2025`

```console
$ docker pull golang@sha256:ee9f166f26c6848ddb291e15383da6d307359d9c007f515c4272b758a66531f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `golang:1-nanoserver-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull golang@sha256:329362e7fa84027d5637b2bbf1f6155ab6391f2ce4b4dd3e7c1174841eb6875e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.3 MB (288331858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f5ebd5320d15298ccbd0ebca9ff1a65c7577ce445e847b6c255b428a0aa443`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Tue, 01 Apr 2025 17:28:31 GMT
SHELL [cmd /S /C]
# Tue, 01 Apr 2025 17:28:32 GMT
ENV GOPATH=C:\go
# Tue, 01 Apr 2025 17:28:32 GMT
USER ContainerAdministrator
# Tue, 01 Apr 2025 17:28:35 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 01 Apr 2025 17:28:36 GMT
USER ContainerUser
# Tue, 01 Apr 2025 17:28:36 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 17:29:42 GMT
COPY dir:c31dd4b35955c3b7ad87aee80c32a76880e815054766f9fc2b5a42c53d1c95ce in C:\Program Files\Go 
# Tue, 01 Apr 2025 17:29:45 GMT
RUN go version
# Tue, 01 Apr 2025 17:29:45 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a45e3cccd2ae12fb90daf625e91220de2e37b6f1945e6a32b934f97e8da74a`  
		Last Modified: Tue, 01 Apr 2025 17:29:49 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc6ea8630b514a7996e523a878589754084c9f4ab242c0ee2db073c63a41d67`  
		Last Modified: Tue, 01 Apr 2025 17:29:49 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f595e9a6287e5667dca76e88b331e4b95b7a0306ecc8252502e0b0c4646dc36`  
		Last Modified: Tue, 01 Apr 2025 17:29:49 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67bdc0b8938e2956b98d42691d78cb09b6ba8ce1ba577885215ec71993b3d270`  
		Last Modified: Tue, 01 Apr 2025 17:29:49 GMT  
		Size: 76.2 KB (76197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c401643380ed63d30b82a2443ff180e5cf6305588eba493b81593aef0ad2980`  
		Last Modified: Tue, 01 Apr 2025 17:29:48 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f00d1343466e0f85d2024ce127a9c7658beacabe22526846633b2c588c3f2c`  
		Last Modified: Tue, 01 Apr 2025 17:29:48 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86ad42d15b3374cc4c8dbc249af4857ea13e0f578527f2b5b4f06bcbad1b7c6`  
		Last Modified: Tue, 01 Apr 2025 17:30:00 GMT  
		Size: 81.9 MB (81858092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392e053fccbd47b6163a2616e9cf54da0580f73b1c5a8833537b1c18998c1a04`  
		Last Modified: Tue, 01 Apr 2025 17:29:48 GMT  
		Size: 88.8 KB (88848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a9511ec71dc99a69cd3c16e3d8c175d0a1b90d0b3b69c35760edf0d61c0110`  
		Last Modified: Tue, 01 Apr 2025 17:29:48 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
