## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:60e3fe06e1d8e460a686b03c3d61c178a0ad719fc687e4dd4df71b242caf8def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull golang@sha256:ed57550cdea2991f5177174305106306a03c306189b610707932f32e085cdf9e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192370521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ec91e16bb1200e0992ed22b0f082dd2c215e25321a7ef2484b91332ac417a4`
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
# Wed, 07 Feb 2024 02:21:05 GMT
ENV GOLANG_VERSION=1.22.0
# Wed, 07 Feb 2024 02:22:57 GMT
COPY dir:002c9f3689dddf68894e8a396363c27cb258d8144ee0755c02356813e34c4670 in C:\Program Files\Go 
# Wed, 07 Feb 2024 02:23:19 GMT
RUN go version
# Wed, 07 Feb 2024 02:23:20 GMT
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
	-	`sha256:145c60803aa170d5e3b5495fdbd812fbdb2bcd6c45a983f0e68e950579f5c8d8`  
		Last Modified: Wed, 07 Feb 2024 02:28:12 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5029ba1a2ea2cb7724cd470bf21d2a1a7094f37c702140379ec36c8e1494adfc`  
		Last Modified: Wed, 07 Feb 2024 02:28:30 GMT  
		Size: 71.5 MB (71461769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de471bd52a1cf657bb992aa225416bd2ce51992a738ff33d95ba3d2335b60ab6`  
		Last Modified: Wed, 07 Feb 2024 02:28:12 GMT  
		Size: 49.7 KB (49713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a80b42c2d300e0e8992c5969417d1fb69beb98c7e0fdd105dc0d75445f192d3`  
		Last Modified: Wed, 07 Feb 2024 02:28:11 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
