## `golang:1-nanoserver-1809`

```console
$ docker pull golang@sha256:ce4d398184ee0e983dc73f06b8129ed333e6f9965c54a9bd35de9ffb34cd064a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `golang:1-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull golang@sha256:2dcc81e48c6e4e20a92746f725b03f3463285ab3ff27fbc1d402e59c10ba350d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188890876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e8d9703e6a0998d2cf7745d4e68d4e07c6c69760777146360c279293a34ae1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 01 Apr 2025 17:31:06 GMT
SHELL [cmd /S /C]
# Tue, 01 Apr 2025 17:31:08 GMT
ENV GOPATH=C:\go
# Tue, 01 Apr 2025 17:31:08 GMT
USER ContainerAdministrator
# Tue, 01 Apr 2025 17:31:11 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 01 Apr 2025 17:31:12 GMT
USER ContainerUser
# Tue, 01 Apr 2025 17:31:13 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 17:32:18 GMT
COPY dir:c31dd4b35955c3b7ad87aee80c32a76880e815054766f9fc2b5a42c53d1c95ce in C:\Program Files\Go 
# Tue, 01 Apr 2025 17:32:21 GMT
RUN go version
# Tue, 01 Apr 2025 17:32:22 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc31d6c038d749833e21948d93766a0135dd234568edf4e86a0f37618e751e9`  
		Last Modified: Tue, 01 Apr 2025 17:32:28 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e5c90995d73a1dac4c18b9c78ec1fd6d2995cb4f2b056734cbe0e84b5ea354`  
		Last Modified: Tue, 01 Apr 2025 17:32:28 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d58c2c2e4967a6c524100baa9bb4d82b241335f3b005993caf5418454818d2`  
		Last Modified: Tue, 01 Apr 2025 17:32:28 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662cc801973619f027a72710a89f2c515070f90ee4fe3d8035487e41284d87e6`  
		Last Modified: Tue, 01 Apr 2025 17:32:28 GMT  
		Size: 74.5 KB (74521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efebc188bb4b974b13946799cff75c4890bc598db1a1736efb2091cc79ed132a`  
		Last Modified: Tue, 01 Apr 2025 17:32:26 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d472898db608ad7349ae15a15c0f9e45f7df20246a5d8d82d1e96d14587c07`  
		Last Modified: Tue, 01 Apr 2025 17:32:26 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e47cdae98ac53c184f1bd73524f843fdb18e3f37eefccfe82528ea51b6c6fb9`  
		Last Modified: Tue, 01 Apr 2025 17:32:39 GMT  
		Size: 81.8 MB (81824169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57e6d52f22fb163e72257a0505ae0a7112c574aa217a5ab579f1f3187d570ab`  
		Last Modified: Tue, 01 Apr 2025 17:32:26 GMT  
		Size: 77.8 KB (77829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8ca359e538af600271f10943bad06397b98d9454c30f96cc5bbbc15f289c7d`  
		Last Modified: Tue, 01 Apr 2025 17:32:26 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
