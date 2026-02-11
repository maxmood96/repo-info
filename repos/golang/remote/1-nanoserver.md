## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:90303951667310b1d7d086a95df28eaf3183a812854ff1e85c45c3a09b79e597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `golang:1-nanoserver` - windows version 10.0.26100.32370; amd64

```console
$ docker pull golang@sha256:64ea73b7601e9a5eb4523cef267bbb21909fb022bfc0cf984767d8162be174a2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268534025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0817e421883d515a470c99ba47a2fc769849c8a743337e2b5d50f9ad67a115`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Tue, 10 Feb 2026 23:37:37 GMT
SHELL [cmd /S /C]
# Tue, 10 Feb 2026 23:37:37 GMT
ENV GOPATH=C:\go
# Tue, 10 Feb 2026 23:37:38 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 23:37:39 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 10 Feb 2026 23:37:40 GMT
USER ContainerUser
# Tue, 10 Feb 2026 23:37:40 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 23:38:42 GMT
COPY dir:e78f50a609fea5ca46e1d1addc58169ec10f3d2953a55005b52ef7e0adbd1c09 in C:\Program Files\Go 
# Tue, 10 Feb 2026 23:38:44 GMT
RUN go version
# Tue, 10 Feb 2026 23:38:44 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8af003c79506de00089d0ecc77ceeb9516ce1a877f649124573fe21c7a8221`  
		Last Modified: Tue, 10 Feb 2026 23:38:53 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba3a7c60c5cdeef07c784bea7a8fc2f33b9e80a6027ea1111069cca00ad567d`  
		Last Modified: Tue, 10 Feb 2026 23:38:53 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ad84da6fd250aecdb81010751551eeb69134736993381bc10614eccb4d41b6`  
		Last Modified: Tue, 10 Feb 2026 23:38:53 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd3e464b076d7901104b8aa87cd44331418ae35b4b481a34348866ab2abeaee`  
		Last Modified: Tue, 10 Feb 2026 23:38:53 GMT  
		Size: 72.2 KB (72181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029424eccf75ce02ccb302f3905d9e1d8618d57f1baafc3101638ad04d304072`  
		Last Modified: Tue, 10 Feb 2026 23:38:51 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a56fa2cc9c4889889a6177f46a235310cff7fd1b51c7790e3373ac77126643`  
		Last Modified: Tue, 10 Feb 2026 23:38:51 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf7fd1fd91fb4d16103b4e43828ec1f677c906169570b36cfb221a47712314b`  
		Last Modified: Tue, 10 Feb 2026 23:39:02 GMT  
		Size: 69.1 MB (69126967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b9f57e4cb68c077cd7ede946257ddaf8166d4afd088d24ff345342e84e600d`  
		Last Modified: Tue, 10 Feb 2026 23:38:51 GMT  
		Size: 76.6 KB (76633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3446d0df009f5f1288b4cbb2260ff852a96228f355454f12ed8057267e365f61`  
		Last Modified: Tue, 10 Feb 2026 23:38:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-nanoserver` - windows version 10.0.20348.4773; amd64

```console
$ docker pull golang@sha256:cb3b285012067fbac4c5e8ac802c1dcacf4059bd7ca4498e98cd77286c2efd44
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195937117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa84e1fe35f67cab8fccdb74b7c7a80632f586cca19bdae0b9334d7e7f5982a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Tue, 10 Feb 2026 23:31:27 GMT
SHELL [cmd /S /C]
# Tue, 10 Feb 2026 23:31:28 GMT
ENV GOPATH=C:\go
# Tue, 10 Feb 2026 23:31:28 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 23:31:30 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 10 Feb 2026 23:31:31 GMT
USER ContainerUser
# Tue, 10 Feb 2026 23:31:31 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 23:32:49 GMT
COPY dir:e78f50a609fea5ca46e1d1addc58169ec10f3d2953a55005b52ef7e0adbd1c09 in C:\Program Files\Go 
# Tue, 10 Feb 2026 23:32:52 GMT
RUN go version
# Tue, 10 Feb 2026 23:32:53 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c592d958978a1eb418b421fa4f8d7b3c6d8752f27db3059e0fe8371a3b55d28`  
		Last Modified: Tue, 10 Feb 2026 23:32:58 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6888029b4d2d7ac65d32c58f46afff9ad910b184c2e501066293c5bab1ea8409`  
		Last Modified: Tue, 10 Feb 2026 23:32:58 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7f83fff6d5d37f113944f9b0e5cf2e99e794b8592ff206f769813bac144863`  
		Last Modified: Tue, 10 Feb 2026 23:32:58 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6599e6edd5e943a4dd0d5906ebf06326efe200240c9d6ce0689eeae80ff623fa`  
		Last Modified: Tue, 10 Feb 2026 23:32:58 GMT  
		Size: 75.0 KB (75011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5306f95d09f7bed1a699d9cf1f8af95a6b4f2ac4e3f0b771caf221acb4386d1e`  
		Last Modified: Tue, 10 Feb 2026 23:32:57 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9573e767b12e3c8c97cf2b3620163421f31c9c66acdd2bf0258d57919d54cec4`  
		Last Modified: Tue, 10 Feb 2026 23:32:57 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a642e4f674c72ce3cd9d9299a315e64535ee6058b74dc5879d0f33a267fc1c`  
		Last Modified: Tue, 10 Feb 2026 23:33:09 GMT  
		Size: 69.1 MB (69126010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af884e0bee3faf3812087c1a51a3d02a7e7d2c7cc29d920ee6ab7ae36ebacde`  
		Last Modified: Tue, 10 Feb 2026 23:32:57 GMT  
		Size: 83.7 KB (83716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe43aacf287c070afd2b0c61754d2f54885effb4a81d73cc423362ae5636a2d`  
		Last Modified: Tue, 10 Feb 2026 23:32:57 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
