## `golang:nanoserver`

```console
$ docker pull golang@sha256:3c7d153d8ed8a78f7b76cc2ca4dd88c0f98b454e98e3b2a220e0d19dcfba94e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `golang:nanoserver` - windows version 10.0.20348.2461; amd64

```console
$ docker pull golang@sha256:7226ddd2cbd6e9471711e0529760925592b5868b998b5487f55895ee35023014
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191958199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267ad4bac0b3f8b0ac67c8136455bf2e400e5a27ec3190a98dd52104725621bf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 10 May 2024 20:16:48 GMT
RUN Apply image 10.0.20348.2461
# Tue, 04 Jun 2024 20:49:40 GMT
SHELL [cmd /S /C]
# Tue, 04 Jun 2024 20:49:40 GMT
ENV GOPATH=C:\go
# Tue, 04 Jun 2024 20:49:41 GMT
USER ContainerAdministrator
# Tue, 04 Jun 2024 20:49:57 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 04 Jun 2024 20:49:57 GMT
USER ContainerUser
# Tue, 04 Jun 2024 20:49:58 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 20:51:17 GMT
COPY dir:5740e62168801895135af54bbf9a0c0e6996b1c9f19a0a4d6d32e83e842d4de4 in C:\Program Files\Go 
# Tue, 04 Jun 2024 20:51:21 GMT
RUN go version
# Tue, 04 Jun 2024 20:51:22 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:90b3a5622f8d62905d0a3029df4f91b934558ad375bef25c596214df31acac88`  
		Last Modified: Tue, 14 May 2024 17:22:15 GMT  
		Size: 120.4 MB (120425316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d1cdfb89364ef99f3d1f29beda7b7f44b743a40954ce95c425a11a233e78fe`  
		Last Modified: Tue, 04 Jun 2024 20:51:26 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b42220b3a9edabd5b0f079aa4c850c2941d24d67eff73c7fbf173742215a986`  
		Last Modified: Tue, 04 Jun 2024 20:51:26 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0448ca4c3adb542d98120e63e0e4f9f500a23c3c90619e42cd9f85be1fa240`  
		Last Modified: Tue, 04 Jun 2024 20:51:26 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aabf5f164d9b2cf6ad14644d958d8b27f15befb932412d2363392bca2c30cd8d`  
		Last Modified: Tue, 04 Jun 2024 20:51:26 GMT  
		Size: 84.6 KB (84551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1621ec1d7d8c6ca2e3eb82e8da82e2361d92d191be9c73fcbaf75464c9e0a111`  
		Last Modified: Tue, 04 Jun 2024 20:51:25 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05cf36a3f9a283a2e69ee8a74741140aee96d86bb1b789f05e4939e9905b106`  
		Last Modified: Tue, 04 Jun 2024 20:51:25 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4ccb7d3bd0306b3df2ef0f041996b19edb63d0b09621a268e7522f8e2000ce`  
		Last Modified: Tue, 04 Jun 2024 20:51:35 GMT  
		Size: 71.4 MB (71354155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45a678a8e738e0fb3008b4ea50327a3b987066ffbc42e1699514cceb6d8a96e`  
		Last Modified: Tue, 04 Jun 2024 20:51:25 GMT  
		Size: 87.7 KB (87730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f580edbcf3fecf6c19d762bd5dc62a41618e10aa7939cfb4f92f2c73eaa0619`  
		Last Modified: Tue, 04 Jun 2024 20:51:25 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull golang@sha256:eec8ba535febdbf113afc952615bf3068a57fe2a13e4664f180383d06b89ba02
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226429744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7874c3bc34f3f9416665e117db4b5330bf3b2f529bf716d3fbace0cd77d7f643`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Tue, 04 Jun 2024 20:49:15 GMT
SHELL [cmd /S /C]
# Tue, 04 Jun 2024 20:49:17 GMT
ENV GOPATH=C:\go
# Tue, 04 Jun 2024 20:49:18 GMT
USER ContainerAdministrator
# Tue, 04 Jun 2024 20:49:37 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 04 Jun 2024 20:49:38 GMT
USER ContainerUser
# Tue, 04 Jun 2024 20:49:38 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 20:50:55 GMT
COPY dir:5740e62168801895135af54bbf9a0c0e6996b1c9f19a0a4d6d32e83e842d4de4 in C:\Program Files\Go 
# Tue, 04 Jun 2024 20:50:59 GMT
RUN go version
# Tue, 04 Jun 2024 20:51:00 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53eb3f034b75941fc2373b8938b26c95454ab1b2d9ed7f329856bf58639d9b53`  
		Last Modified: Tue, 04 Jun 2024 20:51:04 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985b1a19e4ea6445c00a0648756170477130d9b1493b72831bc236e406d980b8`  
		Last Modified: Tue, 04 Jun 2024 20:51:04 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9fb0161492e65195e867bbdd4daceef59cc2c174a58347dd7c03c088924cd40`  
		Last Modified: Tue, 04 Jun 2024 20:51:04 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72981189aa0d82f33c545f531f75036f494437b03a7b8ce3c9b7b9cd771fe7d1`  
		Last Modified: Tue, 04 Jun 2024 20:51:04 GMT  
		Size: 66.5 KB (66464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89c30912b70946861c812159c828ecaef270790ded8eadfe594d27845c446ee`  
		Last Modified: Tue, 04 Jun 2024 20:51:03 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f88e666a22b7295e1262d398a2cb1a9c48be446818c9782140fb478fc98d0f`  
		Last Modified: Tue, 04 Jun 2024 20:51:03 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201d42e9477077ed6cee58b9c9a30e6e769360fd9e3150ab91437cc1cac33621`  
		Last Modified: Tue, 04 Jun 2024 20:51:13 GMT  
		Size: 71.3 MB (71348932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c0aaf458c684739a3a8cfd771ceb324199b3ceab737da738e3c89ab3d22ec0`  
		Last Modified: Tue, 04 Jun 2024 20:51:03 GMT  
		Size: 66.5 KB (66531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddea578575e7ae693d0e09588cdbea8816cc0de954ad02fb5bc419dbba62312`  
		Last Modified: Tue, 04 Jun 2024 20:51:03 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
