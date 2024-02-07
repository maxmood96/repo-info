## `golang:nanoserver`

```console
$ docker pull golang@sha256:d679b9052ef7af5cf7d6ecf3e57afb900b115821ef6827b39aeac381ffb12ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `golang:nanoserver` - windows version 10.0.20348.2227; amd64

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

### `golang:nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull golang@sha256:2b54a9deee09d93f0d27d46b330bc38aa6908b684e1c262cb9eeacf74ea97747
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176197555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3e469877baaabc4a9bc3e8a8fd31724855872b5531ea47a871ace7042869c6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Wed, 10 Jan 2024 23:35:47 GMT
SHELL [cmd /S /C]
# Wed, 10 Jan 2024 23:35:48 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:35:48 GMT
USER ContainerAdministrator
# Wed, 10 Jan 2024 23:35:58 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 10 Jan 2024 23:35:59 GMT
USER ContainerUser
# Wed, 07 Feb 2024 02:23:33 GMT
ENV GOLANG_VERSION=1.22.0
# Wed, 07 Feb 2024 02:25:23 GMT
COPY dir:002c9f3689dddf68894e8a396363c27cb258d8144ee0755c02356813e34c4670 in C:\Program Files\Go 
# Wed, 07 Feb 2024 02:25:48 GMT
RUN go version
# Wed, 07 Feb 2024 02:25:49 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4359fc279f6237926816561ae1d2b91635d62f4054c41225432d1e891648a1`  
		Last Modified: Thu, 11 Jan 2024 00:05:11 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b82c9961fa54075d432c10bfadc90379a518456fb02e499df24a877541ac94`  
		Last Modified: Thu, 11 Jan 2024 00:05:11 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28323fdaacc7793676850ff73c132c20076785bf195fa0399ca7f38d71126f5`  
		Last Modified: Thu, 11 Jan 2024 00:05:11 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0130ba848c13896810ce8496ef1b534ba38a9f82a6b7e8585c8c2060721ad52f`  
		Last Modified: Thu, 11 Jan 2024 00:05:10 GMT  
		Size: 68.6 KB (68647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b417f6b6e79c03bf6187db98994d1da138adad475d8e228b80bcf55b4a08622`  
		Last Modified: Thu, 11 Jan 2024 00:05:08 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d4d4b3b4a7419b74c325ec3d14ba84c234fbaa165d64329b43dabe8b422727`  
		Last Modified: Wed, 07 Feb 2024 02:28:45 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81133773eda856ceabe856433999eb31d6913ca22d98c6dd3e075a32625866c`  
		Last Modified: Wed, 07 Feb 2024 02:29:02 GMT  
		Size: 71.5 MB (71456836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e86c770a39c2342fa3c821d5eed8c12f7191368586041cbdaa5350e0b5d091`  
		Last Modified: Wed, 07 Feb 2024 02:28:45 GMT  
		Size: 73.7 KB (73677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c5e0c0a239881e3e77b02a7c26fdc9837a41bb2626b39e920551a783e5f7d4`  
		Last Modified: Wed, 07 Feb 2024 02:28:45 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
