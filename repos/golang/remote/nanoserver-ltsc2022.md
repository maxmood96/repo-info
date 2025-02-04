## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:53be89bcaccf501c6c822a73cd167ff8c85769054ef054f26fd64d096a8d6db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull golang@sha256:dd00cb71c20516db3c398fa0f55516c9e3f443aeb24eb6c49126593f735b3b2a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 MB (197765645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e9390c196dc4bfe1fecac5fe1ee7656b2933e7d0035caa7c4d08e7fb185fc7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Tue, 04 Feb 2025 20:31:26 GMT
SHELL [cmd /S /C]
# Tue, 04 Feb 2025 20:31:27 GMT
ENV GOPATH=C:\go
# Tue, 04 Feb 2025 20:31:27 GMT
USER ContainerAdministrator
# Tue, 04 Feb 2025 20:31:32 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 04 Feb 2025 20:31:33 GMT
USER ContainerUser
# Tue, 04 Feb 2025 20:31:34 GMT
ENV GOLANG_VERSION=1.23.6
# Tue, 04 Feb 2025 20:32:46 GMT
COPY dir:66ad27fa53c5925702ccb0207e4d01d56d92ab3a463eb1f7283af2dd3485b1fd in C:\Program Files\Go 
# Tue, 04 Feb 2025 20:32:50 GMT
RUN go version
# Tue, 04 Feb 2025 20:32:51 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9581c6c3deb77d640ee11bee80855575dee62405b60d06388716f8195740a96`  
		Last Modified: Tue, 04 Feb 2025 20:32:56 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ef988a3c509e0dd846455a28596b414f6cc7e60041daccfb7ecaa2abaf2a6c`  
		Last Modified: Tue, 04 Feb 2025 20:32:56 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1fb8d9aa7e9348f1ffc6ee1b10d67b873ccd61c4326d6c112dd9b9a57508a3`  
		Last Modified: Tue, 04 Feb 2025 20:32:56 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a630b83fdd46c237cf4c1f896d710ea48e121c5937b3731c8fb8030e8a1ee473`  
		Last Modified: Tue, 04 Feb 2025 20:32:56 GMT  
		Size: 74.1 KB (74092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acb99e805c30a563c547a2345a50b507447c4a7e41cd5b0fad0139d9334d44d`  
		Last Modified: Tue, 04 Feb 2025 20:32:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c488c7851242909d21fcda7aacf84931bda893b2754ad2b1dbe82924fe856598`  
		Last Modified: Tue, 04 Feb 2025 20:32:55 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af294ef00ef50e0c9d477f4a43917f33fe98f45befee06e05e4e897622ae31e`  
		Last Modified: Tue, 04 Feb 2025 20:33:06 GMT  
		Size: 76.9 MB (76947445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130034765e12e9637febf400989aaa824486e3610da5c8f02e4f830c325ce54a`  
		Last Modified: Tue, 04 Feb 2025 20:32:55 GMT  
		Size: 76.2 KB (76167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34713de33b7abcc2ca5ae494b0cb93243574ee3275e8777949d8440fed731d4`  
		Last Modified: Tue, 04 Feb 2025 20:32:55 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
