## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:70212b4f2bf088d8d52bd8401f2a9f5dfe6228941bd8a7b27eecac561c51306d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull golang@sha256:52cc479501899feb5a4cb8b81b6645d9b908b49455782e91d100d05bf08aef9a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202688338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45c3f1257d0b1abf92358e7a97e79c84add1c4a73e0ea3bf413c7125be6d46f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 19:27:15 GMT
SHELL [cmd /S /C]
# Wed, 12 Mar 2025 19:27:16 GMT
ENV GOPATH=C:\go
# Wed, 12 Mar 2025 19:27:17 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:27:19 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 12 Mar 2025 19:27:20 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:27:20 GMT
ENV GOLANG_VERSION=1.24.1
# Wed, 12 Mar 2025 19:30:19 GMT
COPY dir:1c8a5df65fcdbd0ad306edfb20884d0712989c03ff01d990889cdc983af886a3 in C:\Program Files\Go 
# Wed, 12 Mar 2025 19:30:22 GMT
RUN go version
# Wed, 12 Mar 2025 19:30:23 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b988595f898b0b1e6d121af9ac8ba05d50f030dd62f43800cb38da30a7da9a4c`  
		Last Modified: Wed, 12 Mar 2025 19:30:26 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea84ad22ce04b58026335535ef698fb6007861f5e6e9072d72f5c5361bb8922`  
		Last Modified: Wed, 12 Mar 2025 19:30:26 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c77ea7941a0fc69da704fd559569c1d89bbeb159dc95567432f6dc9b67c023`  
		Last Modified: Wed, 12 Mar 2025 19:30:26 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593385bfa2390a88f54e9d745ff2d8ff720ffa15b1c4e56f119e8eff0c167645`  
		Last Modified: Wed, 12 Mar 2025 19:30:26 GMT  
		Size: 75.8 KB (75807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210a9f8dd71ff800a06706cbb58cd49f4cb17cfd0ac72607a94280c906cf52a9`  
		Last Modified: Wed, 12 Mar 2025 19:30:25 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e78b3f00393b6bcfe09db97f8a2701ddc220de879d298e181544b5f95f1775`  
		Last Modified: Wed, 12 Mar 2025 19:30:25 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9bb95302fc56cbf376cd818bd33b7647c21d7b1b5f276906f167cc79872d79`  
		Last Modified: Wed, 12 Mar 2025 19:30:37 GMT  
		Size: 81.8 MB (81818864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f840a999cb19cd09db90d5064c11b0bedd699aaa92358530f86ced88e50730`  
		Last Modified: Wed, 12 Mar 2025 19:30:25 GMT  
		Size: 91.6 KB (91553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb27deb048e4ad109f3c751dbd157213127d9190b8cfaa6eee783c5aa375235`  
		Last Modified: Wed, 12 Mar 2025 19:30:25 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
