## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:080abea5d37b1c0492aa6b1d45a17bfb0f83c1ada3eee6461dbf3503fdd26b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull golang@sha256:d1300f6620f80b323d76e1032b8609d172979e36a0bc8a4824ab2cd596c077bb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192287818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655bbb41613325936f9e01ac8e1aaa2faf7934d5d965603093bfe6dcdc9b0ff7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 05 Mar 2024 19:20:30 GMT
RUN Apply image 10.0.20348.2340
# Wed, 13 Mar 2024 01:56:18 GMT
SHELL [cmd /S /C]
# Wed, 13 Mar 2024 01:56:19 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:56:20 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 01:56:32 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 13 Mar 2024 01:56:32 GMT
USER ContainerUser
# Wed, 13 Mar 2024 01:56:33 GMT
ENV GOLANG_VERSION=1.22.1
# Wed, 13 Mar 2024 01:58:26 GMT
COPY dir:ff4ed0e5730af1cd3210a0325ec904ffc63fb0554a3b82d7c5005a8b1ff65baa in C:\Program Files\Go 
# Wed, 13 Mar 2024 01:58:50 GMT
RUN go version
# Wed, 13 Mar 2024 01:58:50 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:94ec3b200bababb5c0b6605ad82c23779d8f918fbfe1ef5d1cf51be6f12fa749`  
		Last Modified: Tue, 12 Mar 2024 19:42:37 GMT  
		Size: 120.7 MB (120702694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584fe58316f1cc0966e34105ef3c88ab19e6a95bdb41ca75cdf08cc88b290d5`  
		Last Modified: Wed, 13 Mar 2024 02:14:44 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f3cffc7043949988f679565708042f3602ccd2565491acc56fd549f65849e6`  
		Last Modified: Wed, 13 Mar 2024 02:14:42 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13712b3bbb648bc53a820b1a3612e8ff4d45a163cabdf14b6e0bf1a7b147ee38`  
		Last Modified: Wed, 13 Mar 2024 02:14:42 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2926f1f9e042fdbe7275aaa681c5e48d117dc8adfae105c96616f500bf9f0e`  
		Last Modified: Wed, 13 Mar 2024 02:14:42 GMT  
		Size: 88.1 KB (88092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5883de4f89867f6624e06cb05c3a3741e60dffdcd7674e46116e4057757e4b7b`  
		Last Modified: Wed, 13 Mar 2024 02:14:40 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e729783fce303d672bbaa5ac9a44e0f4db6b493a0d6511bdd8978d2013e24091`  
		Last Modified: Wed, 13 Mar 2024 02:14:40 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80508aba2b3c16566e4716a9a6e9588d42f746b7f2a57663ef1fb8b7b9eeb173`  
		Last Modified: Wed, 13 Mar 2024 02:15:00 GMT  
		Size: 71.4 MB (71440268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bb508190d3d0fa9884508ac85bb16f9cd0f0d3443541a304ecf468a6f2c636`  
		Last Modified: Wed, 13 Mar 2024 02:14:40 GMT  
		Size: 49.6 KB (49563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5704e7f753c62000e68f67f4bd93d8b556bbf8968bbf69defad99db598c1481c`  
		Last Modified: Wed, 13 Mar 2024 02:14:40 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
