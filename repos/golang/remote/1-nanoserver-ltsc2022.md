## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:e45c906cf3615d224013f55752144c274b21333a22fdb9365ca35920507207ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull golang@sha256:a4e45fdad7c1074ab0d33513f172b315554031a52fbcc240038eed933003b1fe
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184792913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592bff007039e99c37725427c8b3847cfd4690b391461b982c15bcebe2d38b83`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Tue, 07 Oct 2025 20:10:07 GMT
SHELL [cmd /S /C]
# Tue, 07 Oct 2025 20:10:08 GMT
ENV GOPATH=C:\go
# Tue, 07 Oct 2025 20:10:09 GMT
USER ContainerAdministrator
# Tue, 07 Oct 2025 20:10:17 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 07 Oct 2025 20:10:17 GMT
USER ContainerUser
# Tue, 07 Oct 2025 20:10:18 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 20:11:42 GMT
COPY dir:496933bd3f8baf9b0f0140181539534e76964b44160358c52007ad2d67277e76 in C:\Program Files\Go 
# Tue, 07 Oct 2025 20:11:45 GMT
RUN go version
# Tue, 07 Oct 2025 20:11:46 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c16e74a58eff68d11263d8ab9b2d34386a4fd4ab77d326ecc9d1c84e7c0e32`  
		Last Modified: Tue, 07 Oct 2025 20:12:20 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc60e342f158be0cab599e01556f8acce85feaf493cac9ccf540c5b4b4aa36f`  
		Last Modified: Tue, 07 Oct 2025 20:12:20 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0a04dd4c483160ddf9569c5436dbd14715c76a83ac15d26270c63adc440793`  
		Last Modified: Tue, 07 Oct 2025 20:12:20 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78039a19c211d3090e31adb3fd29338e57f8295b09d18acdca9e5bfd1dd9738e`  
		Last Modified: Tue, 07 Oct 2025 20:12:20 GMT  
		Size: 85.0 KB (84966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e53904f3aa367f2c2b1597435ea71ac75ae538a5349786dd7795641e1c6b42`  
		Last Modified: Tue, 07 Oct 2025 20:12:20 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28878e9ec120a0083dad8213b47577bfbba830569bb8e33d7e1aa94687bbd0fe`  
		Last Modified: Tue, 07 Oct 2025 20:12:20 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d760ae347a9717894b29cd109dcdf490f6082e17c1447d8151f0c443513076e0`  
		Last Modified: Tue, 07 Oct 2025 20:12:25 GMT  
		Size: 61.9 MB (61898118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c04a1abafecb144f223605bfb8acf73f20e8e2dfefa451f0533b724744b0e90`  
		Last Modified: Tue, 07 Oct 2025 20:12:20 GMT  
		Size: 83.3 KB (83319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e75951a11137c6a456d584e33e104e8929e2653c717f4f03a33fb99984792a`  
		Last Modified: Tue, 07 Oct 2025 20:12:21 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
