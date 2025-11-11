## `golang:nanoserver`

```console
$ docker pull golang@sha256:3b377cd220fc2c24d1a05a9b63423655d2ae647ff20b4c202bfc6590e4188346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `golang:nanoserver` - windows version 10.0.26100.7171; amd64

```console
$ docker pull golang@sha256:ce68d6636862f2eaabe3ae277acf6cc0895cd1facd075261050e03931bc12b16
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (260008041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20800b2bff7463be7508b81f5709e33ba64b4f254fe53159e6adaa071c55ee1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 09 Nov 2025 10:04:50 GMT
RUN Apply image 10.0.26100.7171
# Tue, 11 Nov 2025 20:14:33 GMT
SHELL [cmd /S /C]
# Tue, 11 Nov 2025 20:14:34 GMT
ENV GOPATH=C:\go
# Tue, 11 Nov 2025 20:14:34 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:14:36 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 11 Nov 2025 20:14:37 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:14:37 GMT
ENV GOLANG_VERSION=1.25.4
# Tue, 11 Nov 2025 20:15:40 GMT
COPY dir:3cd50d34ed67d71dc6ad2837dc9665403756fda3aa14b5be3225998e6b9c9021 in C:\Program Files\Go 
# Tue, 11 Nov 2025 20:15:43 GMT
RUN go version
# Tue, 11 Nov 2025 20:15:44 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:87c91227213eb6e7c8cfe33b6bd0429350e524756878f37f3860b013f804bf59`  
		Last Modified: Tue, 11 Nov 2025 20:41:49 GMT  
		Size: 197.9 MB (197936447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28b66bb162c025ca8aa2cf43f0a43684c5601e5b80d77256bb69e4fa8b2eb30`  
		Last Modified: Tue, 11 Nov 2025 20:16:09 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf860d5a777467912b3ba8039108398dae557e5e2dfd522a1d56d8e19248d757`  
		Last Modified: Tue, 11 Nov 2025 20:16:09 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8135cf28904ef8618c5431c9de729f446f0325a71de0a5625dbd4f9686f9fc`  
		Last Modified: Tue, 11 Nov 2025 20:16:09 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e55b49878576df3eb933d1a63fbcb4e6751123c061f849cac49c52e0623c048`  
		Last Modified: Tue, 11 Nov 2025 20:16:09 GMT  
		Size: 73.4 KB (73390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bf5520b84e425f229d904b04c39676fe0b801a3e14e020756a6ac521f0966c`  
		Last Modified: Tue, 11 Nov 2025 20:16:10 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cbc3216d712be3b553c9ec368216142c8f03e5f4b2d75f6f8412811b1dc028`  
		Last Modified: Tue, 11 Nov 2025 20:16:10 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42cd60356c6ad456f4dc8673ddae233e3f4a684639d8acafa0c96bb2e7738e02`  
		Last Modified: Tue, 11 Nov 2025 20:16:13 GMT  
		Size: 61.9 MB (61905739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c69e59c0c9ed5e8097f7cad7b7edac22a92e1c1dc5f2660d1b6b61e3c39c42d`  
		Last Modified: Tue, 11 Nov 2025 20:16:10 GMT  
		Size: 85.8 KB (85837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7870e51174bc55d70b321559653e3022119f88071049a2c244593f8c69d717`  
		Last Modified: Tue, 11 Nov 2025 20:16:10 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.20348.4405; amd64

```console
$ docker pull golang@sha256:385d99e46951629a2e2137ec6de80a05c996b0fc14b8d208a92d3ead1636065b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 MB (188420437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9d967c2590ceac274981e4b16e6758b479a1de9ba94fe55090f0911cb9f0de`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:12:45 GMT
SHELL [cmd /S /C]
# Tue, 11 Nov 2025 20:12:46 GMT
ENV GOPATH=C:\go
# Tue, 11 Nov 2025 20:12:46 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:12:48 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 11 Nov 2025 20:12:48 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:12:49 GMT
ENV GOLANG_VERSION=1.25.4
# Tue, 11 Nov 2025 20:13:46 GMT
COPY dir:3cd50d34ed67d71dc6ad2837dc9665403756fda3aa14b5be3225998e6b9c9021 in C:\Program Files\Go 
# Tue, 11 Nov 2025 20:13:49 GMT
RUN go version
# Tue, 11 Nov 2025 20:13:50 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbc1ba9d37133a27962b82cd3c02534daa291c4b22a77caa43f4647238a135e`  
		Last Modified: Tue, 11 Nov 2025 20:14:18 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f608e2c7aa231443cb99380ec64fa52cdd12fe5447c16c271964181617531a`  
		Last Modified: Tue, 11 Nov 2025 20:14:18 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8072fd6e9a45814a6a922df7002940427b0e9319413f9c315c0a09bedbb660d7`  
		Last Modified: Tue, 11 Nov 2025 20:14:18 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae76a87ba3420c26b78d83e1e50ce4bff4617780f65df7d18d856c6dfc47eec7`  
		Last Modified: Tue, 11 Nov 2025 20:14:18 GMT  
		Size: 76.9 KB (76923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c483d72390ff1268018951d22f25dd3e712564572a2361ee8cd4254894a5f392`  
		Last Modified: Tue, 11 Nov 2025 20:14:18 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72085cf47bcb324b3e5a550240bf97a54b9c0d7e75841f9a781c0d42d245eb6`  
		Last Modified: Tue, 11 Nov 2025 20:14:18 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1461b9011d4e6dceb4d81b80da6d3885a42a0fbc7096ead20843677f3f749d0a`  
		Last Modified: Tue, 11 Nov 2025 20:14:26 GMT  
		Size: 61.9 MB (61905577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711bfc626a89f95a7d0ac2700de076afb8ff5189412f9e05a534b21dd6de3f0c`  
		Last Modified: Tue, 11 Nov 2025 20:14:18 GMT  
		Size: 82.2 KB (82242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a586d10987f294662f97bb9eb5bf2ac7a18554c502b9eb74cae5325b90137a49`  
		Last Modified: Tue, 11 Nov 2025 20:14:18 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
