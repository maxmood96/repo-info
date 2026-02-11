## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:84ae15fb98951a4cf75aa35232f8fdc3b15ef6eb611ac5316d082ade9a76c2ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

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
