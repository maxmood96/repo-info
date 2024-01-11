## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:5be02b392a70f1ebd94cfabcf1926e303cfac46b6daa3e4afa6be0c040f80b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull golang@sha256:5b77a8d01cc9a2c0cf952f720a914faac1544a1e2e70e3d2205cdefb804b4d3f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190055572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f1015ceb5d7bc2a6e1f4d67e35a0e6d8a7e81c664a1f04fcd64bbfc4e524a1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Wed, 10 Jan 2024 23:32:48 GMT
SHELL [cmd /S /C]
# Wed, 10 Jan 2024 23:32:49 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:32:50 GMT
USER ContainerAdministrator
# Wed, 10 Jan 2024 23:33:01 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 10 Jan 2024 23:33:02 GMT
USER ContainerUser
# Wed, 10 Jan 2024 23:44:15 GMT
ENV GOLANG_VERSION=1.21.6
# Wed, 10 Jan 2024 23:46:11 GMT
COPY dir:88ad6b13f81204befa1505e1ba8ab9ae8e92f1d6e3e59add9d3f52dacc733b9e in C:\Program Files\Go 
# Wed, 10 Jan 2024 23:46:32 GMT
RUN go version
# Wed, 10 Jan 2024 23:46:33 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:11d5cdc5eaac7bace3ae1ecd3c0df2a27ef5005ab296c56b7f83e24bf25c236c`  
		Last Modified: Tue, 09 Jan 2024 20:57:18 GMT  
		Size: 120.8 MB (120769267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a3fdc7b4c9c4ac9deedc06b4598923ec0d94c6d945ce4d4953be581c9abb5d`  
		Last Modified: Thu, 11 Jan 2024 00:04:32 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa38390b58348a7b1422c3e3360cfe643e258663bc5fbdbce13723921f4d76c`  
		Last Modified: Thu, 11 Jan 2024 00:04:32 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8b5b645e529e03cc73171bc9daaebebcefff9646cc7ee4de998bc3ab57e51d`  
		Last Modified: Thu, 11 Jan 2024 00:04:32 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55bcffd1a1d5e79c55e758c8bd7031d6ef9fe12556d3f5483916a7869a5d23f`  
		Last Modified: Thu, 11 Jan 2024 00:04:32 GMT  
		Size: 83.1 KB (83127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5474cded3332a5a52d3bbcdf976cb1dec649aaa0fc1fda2828dbba3750e3566`  
		Last Modified: Thu, 11 Jan 2024 00:04:30 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054417305524d4871a7781a6afd5dc140a9f25303017ddf6961b2774a5e4ac9b`  
		Last Modified: Thu, 11 Jan 2024 00:07:10 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3bf43129e87af1f83ad732b3b28ec33a58ba46107066e968d1c448ce4f1468`  
		Last Modified: Thu, 11 Jan 2024 00:07:28 GMT  
		Size: 69.1 MB (69144041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fef885a5e13da89fbc6efaf97c7ca644f3a7b5a0bb168f5ae04352591d1af5d`  
		Last Modified: Thu, 11 Jan 2024 00:07:10 GMT  
		Size: 52.5 KB (52460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89dd7422bda9c56a1f914d714e236430db3c0dbd03aa3cc1a23e5295668191e0`  
		Last Modified: Thu, 11 Jan 2024 00:07:10 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
