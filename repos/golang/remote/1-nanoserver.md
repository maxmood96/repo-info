## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:08631106929029809975f0aeca36ed737245be3914a3561368db5ca70c5e08a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `golang:1-nanoserver` - windows version 10.0.26100.32230; amd64

```console
$ docker pull golang@sha256:8ecc4a23e6b4ea27e6a0e352c0c5c86b60f278bbd056121929899e62c3f287b7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261148455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc11481f6b31c58d5e0016e743081e31cfa9f2dfab8598717534d51e32d9ba5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Wed, 04 Feb 2026 17:45:02 GMT
SHELL [cmd /S /C]
# Wed, 04 Feb 2026 17:45:03 GMT
ENV GOPATH=C:\go
# Wed, 04 Feb 2026 17:45:03 GMT
USER ContainerAdministrator
# Wed, 04 Feb 2026 17:45:13 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 04 Feb 2026 17:45:13 GMT
USER ContainerUser
# Wed, 04 Feb 2026 17:47:39 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:49:44 GMT
COPY dir:9551509bddcc9697c221a356620da0668487e2429eb6403c42f240a09abbbb1a in C:\Program Files\Go 
# Wed, 04 Feb 2026 17:49:48 GMT
RUN go version
# Wed, 04 Feb 2026 17:49:49 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e167a119d4fef19b90250c86d648c9eca3074c3aa0cae6926d4835020d9c4c93`  
		Last Modified: Wed, 04 Feb 2026 17:47:11 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afc7077969dd15b9bc1930929c7ea0812d1c6d7c2e16404950b5630b79cd55e`  
		Last Modified: Wed, 04 Feb 2026 17:47:11 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6f6a47e34c3f5dd95acd52a7b6b79a84b81d08b5f18e24a58a689384a13566`  
		Last Modified: Wed, 04 Feb 2026 17:47:11 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f824a774793845f1805ab57d0608deb4fd931bc7b5be008ffc8643a97a5d6f45`  
		Last Modified: Wed, 04 Feb 2026 17:47:11 GMT  
		Size: 71.2 KB (71176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3c8c6ff36b81acb58b3954915cbc4ed1b450f5164dd848f50cbeb7d50f8bf5`  
		Last Modified: Wed, 04 Feb 2026 17:47:09 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef350d3f12fd309b39a3f07bd6a6152b08c41498cc23aa54c934561eecaefbab`  
		Last Modified: Wed, 04 Feb 2026 17:49:53 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37315326da7ecec6d96bca6841adaae456519d31ea96a115a497b111116614cc`  
		Last Modified: Wed, 04 Feb 2026 17:50:04 GMT  
		Size: 61.9 MB (61916807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e76ce53206c6cb40ec5ee1b5baee4611bcfe0ed4382d728924de6bc7df5d77`  
		Last Modified: Wed, 04 Feb 2026 17:49:53 GMT  
		Size: 77.3 KB (77325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96db37315a311d0c4f59e816d5d35a8fd88f8a86428de26cb1c85d643c999d0`  
		Last Modified: Wed, 04 Feb 2026 17:49:53 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull golang@sha256:4f9e13b35970de52f3d45a2fe073e095034391a323e6e4b0d871aa9c3818c7f2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188766535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a4ff3936d1016029923b474e81ec2c6380d6545745b2a622be63510e212fd1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 04 Feb 2026 17:44:37 GMT
SHELL [cmd /S /C]
# Wed, 04 Feb 2026 17:44:38 GMT
ENV GOPATH=C:\go
# Wed, 04 Feb 2026 17:44:38 GMT
USER ContainerAdministrator
# Wed, 04 Feb 2026 17:44:45 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 04 Feb 2026 17:44:46 GMT
USER ContainerUser
# Wed, 04 Feb 2026 17:44:47 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:46:42 GMT
COPY dir:9551509bddcc9697c221a356620da0668487e2429eb6403c42f240a09abbbb1a in C:\Program Files\Go 
# Wed, 04 Feb 2026 17:46:45 GMT
RUN go version
# Wed, 04 Feb 2026 17:46:47 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f99ed5cff77c4c563c4c0374114b3eadc943ef12031b2fc6d2f3d874147be9`  
		Last Modified: Wed, 04 Feb 2026 17:46:59 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972f6dc6c01f9a284e6e3de1b564c306740d9223641267e484cca4fd9a04855d`  
		Last Modified: Wed, 04 Feb 2026 17:46:59 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3001684575e5930b5440bed7c46fc3433debf2750693d0d62e34b5a20b824040`  
		Last Modified: Wed, 04 Feb 2026 17:46:59 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5a9a8c5b38e80d40ee85a24fc72876477bad62e5a6baadb9804e18e1d5a383`  
		Last Modified: Wed, 04 Feb 2026 17:46:59 GMT  
		Size: 73.0 KB (72956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd30aa13042aca891e9832d37bbeb6b717b522f1a8f0622bfd33d15c3e12f1ff`  
		Last Modified: Wed, 04 Feb 2026 17:46:57 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73720230f8ad13b694f6d74ddeab0b868b19f7cabf20f763e1eafaadf984665`  
		Last Modified: Wed, 04 Feb 2026 17:46:57 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20558062b5622fd55bbca416229b7c22b421012cfdb8214d7189390f6d7ba6d`  
		Last Modified: Wed, 04 Feb 2026 17:47:09 GMT  
		Size: 61.9 MB (61914927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5165bc631d65cb97a5a1657c8ad0bc884921f5ec1991c7d2209c74aa7bdf883f`  
		Last Modified: Wed, 04 Feb 2026 17:46:57 GMT  
		Size: 75.2 KB (75220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80afb5564b0408d11e58abac7ca9bbf698ea88a74511a5ad4d2a21ee5b8465d5`  
		Last Modified: Wed, 04 Feb 2026 17:46:57 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
