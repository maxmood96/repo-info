## `golang:nanoserver`

```console
$ docker pull golang@sha256:5c091e92e74ecd19c3db3dbc89c14505b030a558c95a51830e2d3908341664d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `golang:nanoserver` - windows version 10.0.20348.2700; amd64

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

### `golang:nanoserver` - windows version 10.0.17763.6293; amd64

```console
$ docker pull golang@sha256:aa6b2d3529d0cdfe5accc9fb4e2b87b6a05756c63617278f6d5a4a42b28afa64
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232142033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f840f5a8f6361cdfc31c9c7fe69e99b4659ce8b6e9bda20ddf79443763c1ddf7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Tue, 01 Oct 2024 23:01:09 GMT
SHELL [cmd /S /C]
# Tue, 01 Oct 2024 23:01:12 GMT
ENV GOPATH=C:\go
# Tue, 01 Oct 2024 23:01:13 GMT
USER ContainerAdministrator
# Tue, 01 Oct 2024 23:01:34 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 01 Oct 2024 23:01:34 GMT
USER ContainerUser
# Tue, 01 Oct 2024 23:01:34 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 23:03:17 GMT
COPY dir:c6fb990fe30b997cadb6a7ba3c4a7d5a2c2077f37e11b2dbb8f33ee41ec246ca in C:\Program Files\Go 
# Tue, 01 Oct 2024 23:03:20 GMT
RUN go version
# Tue, 01 Oct 2024 23:03:21 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367163ab877cae93c0be9aa87b0595351b5a743c4fe00f80e6f931289b8cc105`  
		Last Modified: Tue, 01 Oct 2024 23:03:25 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69998d641fc27d13508602c7fe6f77e7f2dd87cc9f465e1e6cc7451466963383`  
		Last Modified: Tue, 01 Oct 2024 23:03:25 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbd7318d6847675b9f16ba07eaf5674bafc56ba77c6f2e1e845541b888c8776`  
		Last Modified: Tue, 01 Oct 2024 23:03:25 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b553af2da71395d6935af528ba65b5452ea92f062584d91647d698eb924651`  
		Last Modified: Tue, 01 Oct 2024 23:03:25 GMT  
		Size: 66.6 KB (66569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623dce569635429538cceb4c25fab3180e80e77864db73542d0889ab6effa815`  
		Last Modified: Tue, 01 Oct 2024 23:03:24 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f0d0cb0b5604979b980c6a27020644335a6ed9342e9b6b39aa7691d569f89f`  
		Last Modified: Tue, 01 Oct 2024 23:03:24 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d58b1d0cc3157056c1c0bbda4b0bade23167665ebe84e93e94f79f362ef579a`  
		Last Modified: Tue, 01 Oct 2024 23:03:35 GMT  
		Size: 76.9 MB (76920268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7b0d1db43c644dc19ef9f6a261f22225bd10e8a8f663cff466caed47fa7084`  
		Last Modified: Tue, 01 Oct 2024 23:03:24 GMT  
		Size: 67.9 KB (67861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cd30ed395e9c080756c99b8b20ba6bd99e10646217137fa96ad0cc601f3d22`  
		Last Modified: Tue, 01 Oct 2024 23:03:24 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
