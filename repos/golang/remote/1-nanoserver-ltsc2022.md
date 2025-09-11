## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:f34b27472376dedc4392c8045462e71a1360bbd2180784d8bed3c2fe847747ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull golang@sha256:c931caddd8a46cb8400bfed48ca37f5d9f1244041e320c6118e33041fa723374
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184771944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54c1fcf8ff9ce21c1fbe5b6636bdc532dacdaa932eafcbab7f3d8fbd9fc077c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:20:13 GMT
SHELL [cmd /S /C]
# Wed, 10 Sep 2025 22:20:14 GMT
ENV GOPATH=C:\go
# Wed, 10 Sep 2025 22:20:14 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:20:16 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 10 Sep 2025 22:20:17 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:20:17 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 10 Sep 2025 22:21:25 GMT
COPY dir:46dbacc0e72cd22b14f45437dee8650bb541c131ae32b6892fb4b828e1a13b73 in C:\Program Files\Go 
# Wed, 10 Sep 2025 22:21:28 GMT
RUN go version
# Wed, 10 Sep 2025 22:21:29 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33fc9624add6648cdc967f7a290f91ee246c7f8bfb56e7226e52f8dbe0f74af`  
		Last Modified: Wed, 10 Sep 2025 22:22:04 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eb33d13225d1dee351bd7f9ab5b57e7f9dfca73a16eb98c3f3a4e68e7e0ac2`  
		Last Modified: Wed, 10 Sep 2025 22:22:04 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ba29d93538ce8f29ab9c9967156ecb6a06ead0437693858f8f5d2fc821381d`  
		Last Modified: Wed, 10 Sep 2025 22:22:04 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b38ce7c9a1572741254413c939e4adedaf8b3bf8261e1f30c26b0bc55abebca`  
		Last Modified: Wed, 10 Sep 2025 22:22:04 GMT  
		Size: 77.0 KB (76978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7edf7a154cf647c7c4e05b1ec22d1a5e4a23451f0b12b7d0fa8c03a081a8fe`  
		Last Modified: Wed, 10 Sep 2025 22:22:05 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5e11bbc321dd35d4a0a61c655f199843d1ebdb5f1f9007e87f02f095122bed`  
		Last Modified: Wed, 10 Sep 2025 22:22:04 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d70401fef9e541be7b43ed6c810433fc44e3b7620251484d95b926ef069b677`  
		Last Modified: Wed, 10 Sep 2025 22:22:11 GMT  
		Size: 61.9 MB (61882757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7f2404d1aee528b38b7fcf1c1a0d5383852a86b0dd0a01b6b9cbf3f71ca699`  
		Last Modified: Wed, 10 Sep 2025 22:22:05 GMT  
		Size: 85.7 KB (85665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246be777f9a5d322a718a84f549c1e395e5ebb2753f983439350d8c3e5d2f24a`  
		Last Modified: Wed, 10 Sep 2025 22:22:05 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
