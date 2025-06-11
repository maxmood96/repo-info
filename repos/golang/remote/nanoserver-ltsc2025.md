## `golang:nanoserver-ltsc2025`

```console
$ docker pull golang@sha256:bc773132ba6813b897b054882192ab1dc1d75054a4f184727880246d05a01485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `golang:nanoserver-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull golang@sha256:2f890028e6d85f75f966fe36e127188004f0ae117ca667a2d45159a7a38ec635
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274162443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d887cf17a00cb0f310e94f2feac95cff2cc6d1a6c19ecee4bdf65da175fbe942`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Tue, 10 Jun 2025 22:16:07 GMT
SHELL [cmd /S /C]
# Tue, 10 Jun 2025 22:16:08 GMT
ENV GOPATH=C:\go
# Tue, 10 Jun 2025 22:16:10 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:16:13 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 10 Jun 2025 22:16:14 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:16:14 GMT
ENV GOLANG_VERSION=1.24.4
# Tue, 10 Jun 2025 22:17:17 GMT
COPY dir:70f015619b03b14f09ca45829787e7bb802d481fe7480466582aed33ddb74b24 in C:\Program Files\Go 
# Tue, 10 Jun 2025 22:17:22 GMT
RUN go version
# Tue, 10 Jun 2025 22:17:24 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3638b1f0eecdf95328348d20f0ab1a895b3e3a618856dd9dbfc2485d04fadcc`  
		Last Modified: Tue, 10 Jun 2025 22:18:07 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013afb36f5b2067994fe4dfa22fb1e9d1302c458e56c13b3f778fb9954211187`  
		Last Modified: Tue, 10 Jun 2025 22:18:08 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc379e6e33778f5041a40ee6f78bde4b2819760e3219ca5f2150474c2afc338`  
		Last Modified: Tue, 10 Jun 2025 22:18:08 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ab924fd3ef27b1c130f0025008a7dbfd8ed6a21e07d23359426cefdb77ac9b`  
		Last Modified: Tue, 10 Jun 2025 22:18:08 GMT  
		Size: 76.5 KB (76494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8162633c75b764c498828d0278d71001ca1bb7b334e969d4e941727e6ba78b46`  
		Last Modified: Tue, 10 Jun 2025 22:18:08 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d3750d52eb78089a847ecaafa10a5e50510c3117799464bd1026c5eed3a451`  
		Last Modified: Tue, 10 Jun 2025 22:18:09 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507934d42c3efb6d053617e5f3353232c19ddb3fab533e1d1dfe0287d4105d89`  
		Last Modified: Tue, 10 Jun 2025 22:18:18 GMT  
		Size: 81.9 MB (81908417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc655f87c7804c5ce34cba4490566379091611f31fd8bc517a1bcdd23447331`  
		Last Modified: Tue, 10 Jun 2025 22:18:09 GMT  
		Size: 88.4 KB (88389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea06b6ad599542a76682f69af0b016783b5a383506727b9a87081ea34509fb8f`  
		Last Modified: Tue, 10 Jun 2025 22:18:09 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
