## `golang:1-nanoserver-1809`

```console
$ docker pull golang@sha256:548489d1f8d9302fa58bb4a231f65a599c1b7a37e92727dd4757867e1f305ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `golang:1-nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull golang@sha256:adb4b43d573fbde375ed55dd591b018f502125cb9d73af74ee038d60dba3e10e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176215850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335d1bdad75abb3d6788cd8ad8d80688376cfa3f8cb2937166c4353591d15ed3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 01:59:02 GMT
SHELL [cmd /S /C]
# Wed, 13 Mar 2024 01:59:02 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:59:03 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 01:59:14 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 13 Mar 2024 01:59:14 GMT
USER ContainerUser
# Wed, 13 Mar 2024 01:59:15 GMT
ENV GOLANG_VERSION=1.22.1
# Wed, 13 Mar 2024 02:01:07 GMT
COPY dir:ff4ed0e5730af1cd3210a0325ec904ffc63fb0554a3b82d7c5005a8b1ff65baa in C:\Program Files\Go 
# Wed, 13 Mar 2024 02:01:29 GMT
RUN go version
# Wed, 13 Mar 2024 02:01:30 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e998e91ab9f58f57c6ca70c379d030a21b28280ed8962d20187d84c7e40892`  
		Last Modified: Wed, 13 Mar 2024 02:15:15 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef0f18a81628cdba357f375c56e2362aed7f1227adb3fdf824b290c564c0fe8`  
		Last Modified: Wed, 13 Mar 2024 02:15:15 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087ff42eeee5ba095c5de2c7cd7f8c68b7c88638c7a98a6b584f65f1c6c1a74c`  
		Last Modified: Wed, 13 Mar 2024 02:15:15 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385861676603ba1b9c3a4e81a062d75def332a7f3df4fa90b122925de8d968a0`  
		Last Modified: Wed, 13 Mar 2024 02:15:15 GMT  
		Size: 67.4 KB (67380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085f9592bfc6528f53b6d07f5ea7edca4b639fd3f143db532c88d65a4b9d85ce`  
		Last Modified: Wed, 13 Mar 2024 02:15:13 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cb06f5db2b1a439e41a2c7114d8bbacf38036a14109a336a76bc3d7c190d39`  
		Last Modified: Wed, 13 Mar 2024 02:15:13 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd340d89ddca328bc37c0ffe54e9e51589f5c962ca0c7f6fa34685c04fceb6a2`  
		Last Modified: Wed, 13 Mar 2024 02:15:32 GMT  
		Size: 71.4 MB (71440884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e8401c99463925bed5df4cb2f795cabd39b0473502479bafe7d0c16fd9084b`  
		Last Modified: Wed, 13 Mar 2024 02:15:13 GMT  
		Size: 80.3 KB (80308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8f41d96975ec67082495b39ea62ee1e794c1aa0fcc29f48a96381f3aaf991a`  
		Last Modified: Wed, 13 Mar 2024 02:15:13 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
