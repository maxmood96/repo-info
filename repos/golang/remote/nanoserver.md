## `golang:nanoserver`

```console
$ docker pull golang@sha256:a9d9521f056ebb7e0b65e94890a671bc3812f588c824d2553f92dc20cb074301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `golang:nanoserver` - windows version 10.0.26100.4349; amd64

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

### `golang:nanoserver` - windows version 10.0.20348.3807; amd64

```console
$ docker pull golang@sha256:49f11bad83a88366bc3839066432d113a67d69659c88ca30de533999af61ed1d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.6 MB (204594833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8baf2da3aad1b95b97f14fb76b1c7c0e2d22fb7dacae1d31dcbc8f0091287f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:19:17 GMT
SHELL [cmd /S /C]
# Tue, 10 Jun 2025 22:19:18 GMT
ENV GOPATH=C:\go
# Tue, 10 Jun 2025 22:19:18 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:19:21 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 10 Jun 2025 22:19:21 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:19:22 GMT
ENV GOLANG_VERSION=1.24.4
# Tue, 10 Jun 2025 22:21:25 GMT
COPY dir:70f015619b03b14f09ca45829787e7bb802d481fe7480466582aed33ddb74b24 in C:\Program Files\Go 
# Tue, 10 Jun 2025 22:21:28 GMT
RUN go version
# Tue, 10 Jun 2025 22:21:29 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95c04ed807a191fa9cea8c099db320fc1a2f3728a713a3776f348d67ca884df`  
		Last Modified: Tue, 10 Jun 2025 22:22:08 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c3671d22f823fa0435720d46dbc628088c74929317ef291ef76f26fd4d8644`  
		Last Modified: Tue, 10 Jun 2025 22:22:08 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a1d76e1c812722a021ac32804d97b8a008f201253932a6e5fa467755713ccb`  
		Last Modified: Tue, 10 Jun 2025 22:22:09 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6757b1e2ef91d9865a9a6f936bf5773240766d16da5fc7c3521051aac9ddb4`  
		Last Modified: Tue, 10 Jun 2025 22:22:09 GMT  
		Size: 80.2 KB (80188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9363f34515787e68d7643120191c4622d5a7f9c99c32c79d50c01f12b524b2d4`  
		Last Modified: Tue, 10 Jun 2025 22:22:09 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06acd84b440187cdefe29217a4ceb4ce900d104f6180230827acde1f951f8801`  
		Last Modified: Tue, 10 Jun 2025 22:22:09 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072f8eee5398f7edea979320ce198adac712585471f0ac6837e429c0488f77d4`  
		Last Modified: Tue, 10 Jun 2025 22:22:13 GMT  
		Size: 81.9 MB (81879721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f264e6987f88fbf00042cd601a659ff863d96d7b1af1681f01ddf036a40356de`  
		Last Modified: Tue, 10 Jun 2025 22:22:09 GMT  
		Size: 88.0 KB (88016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63a3ed4244f35176aa957d81ec6fb6700c681ad436e06c63647980f63c84871`  
		Last Modified: Tue, 10 Jun 2025 22:22:09 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
