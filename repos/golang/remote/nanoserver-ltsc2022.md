## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:722c7bdb03f60dc413778c94619d7e4c2b130a52d9ba22779f83f4e939d5df04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull golang@sha256:7f8221dd247920f1b1cfc7878208a585e3f8416a8dbb224145ad4af6ba8b7aea
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.6 MB (197625983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335c4a6ea3f590f9018aae0cea0f39c3803b7b06d15b0cfa157158bb5fc406b4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 05 Sep 2024 23:48:03 GMT
RUN Apply image 10.0.20348.2700
# Tue, 01 Oct 2024 22:58:53 GMT
SHELL [cmd /S /C]
# Tue, 01 Oct 2024 22:58:53 GMT
ENV GOPATH=C:\go
# Tue, 01 Oct 2024 22:58:54 GMT
USER ContainerAdministrator
# Tue, 01 Oct 2024 22:59:09 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 01 Oct 2024 22:59:10 GMT
USER ContainerUser
# Tue, 01 Oct 2024 22:59:10 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 23:00:27 GMT
COPY dir:c6fb990fe30b997cadb6a7ba3c4a7d5a2c2077f37e11b2dbb8f33ee41ec246ca in C:\Program Files\Go 
# Tue, 01 Oct 2024 23:00:30 GMT
RUN go version
# Tue, 01 Oct 2024 23:00:31 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:a447243899be39b01c34fc7e1bcecb47ce42b14668876fdd121f8b5e2d4d4a86`  
		Last Modified: Tue, 10 Sep 2024 22:28:02 GMT  
		Size: 120.5 MB (120509521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c331bf536f6b209e8646c926e06e86d98a840f09b2506e2a273233c119ef947`  
		Last Modified: Tue, 01 Oct 2024 23:00:37 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf20ab4c69a44a8dd32da794b77ca2c1cb5c5935403cb9f65bcbf0189c590e8f`  
		Last Modified: Tue, 01 Oct 2024 23:00:37 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0a4f85d82d70d85442bfeb1ed4c3cbc885fdd4f80b53e63f4e73741722f588`  
		Last Modified: Tue, 01 Oct 2024 23:00:37 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20464516c6b03e57c2cddc97c56c3654d77e057ace786cf1d483faae5630f32e`  
		Last Modified: Tue, 01 Oct 2024 23:00:38 GMT  
		Size: 100.9 KB (100912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5557a3c8326aadd4adfcb98e4a52661fac3ed5cd6d8c35025d1b973711e96d2`  
		Last Modified: Tue, 01 Oct 2024 23:00:36 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea70c043968ee4b05a09c59e05842c507188d969fca627b0fd5b3c8d2f800f4b`  
		Last Modified: Tue, 01 Oct 2024 23:00:36 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd6dabd60d5d347a317a6e0669c430f67acd01772828f961e1d183b9e49dc80`  
		Last Modified: Tue, 01 Oct 2024 23:00:47 GMT  
		Size: 76.9 MB (76922251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97060295aac92509f805959bfa63968a004cd9fc4ae982493afba5acacf8b9b`  
		Last Modified: Tue, 01 Oct 2024 23:00:36 GMT  
		Size: 86.9 KB (86872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ba47ff26bad7b4b4dd789cdc6f90a91582d58eee8f4d445f0d17968aacf64f`  
		Last Modified: Tue, 01 Oct 2024 23:00:36 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
