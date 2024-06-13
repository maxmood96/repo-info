## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:dd26a05d3cebeb60c9e2e6498b6753e028f30f316f2051bdffddd11d81e566a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2527; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.2527; amd64

```console
$ docker pull golang@sha256:f09967e12f17cbd35c80ed23e7ddd7d4fd1835b464cc8bdea83a148cdb2d3b1b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192013547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b4fbb2014bf6d657e2d807aaa540fbf95596d63ded01f47225aec23362f279f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Jun 2024 08:41:16 GMT
RUN Apply image 10.0.20348.2527
# Wed, 12 Jun 2024 19:08:07 GMT
SHELL [cmd /S /C]
# Wed, 12 Jun 2024 19:08:08 GMT
ENV GOPATH=C:\go
# Wed, 12 Jun 2024 19:08:08 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 19:08:10 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 12 Jun 2024 19:08:11 GMT
USER ContainerUser
# Wed, 12 Jun 2024 19:08:11 GMT
ENV GOLANG_VERSION=1.22.4
# Wed, 12 Jun 2024 19:09:59 GMT
COPY dir:5740e62168801895135af54bbf9a0c0e6996b1c9f19a0a4d6d32e83e842d4de4 in C:\Program Files\Go 
# Wed, 12 Jun 2024 19:10:01 GMT
RUN go version
# Wed, 12 Jun 2024 19:10:02 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:f9825bcd6f9509654677a23b5fa1d32b32e1e32ff51914ebfaa76d5e79c22b50`  
		Last Modified: Wed, 12 Jun 2024 02:27:19 GMT  
		Size: 120.5 MB (120488969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd18125e30e573dd8a00e97e4a84fc9aaf6afbb2f7ba9fe5caa942723d94d634`  
		Last Modified: Wed, 12 Jun 2024 19:10:08 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96916df0eabb96b618fca0b3290ffd5411ea58a60368ca997e9d73edd6400ff`  
		Last Modified: Wed, 12 Jun 2024 19:10:07 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd02acd28479cda6352f175555db99c943aba015b874771ce74eed6b82d15bc`  
		Last Modified: Wed, 12 Jun 2024 19:10:08 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5f28d7e630209158c5e9f2bfc447804b3718260ab170dd2aa55cd580fcffb7`  
		Last Modified: Wed, 12 Jun 2024 19:10:08 GMT  
		Size: 75.4 KB (75367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b488aba23053d3d7069e665a127f6622e1f60f57e06da23bbcae0cb36990995`  
		Last Modified: Wed, 12 Jun 2024 19:10:06 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62eb56aeb2bc9b25e2833cac407eb22c74466703bc1766cfbc1cddb24d213fd`  
		Last Modified: Wed, 12 Jun 2024 19:10:06 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf67fd0b89bbff254274910b6959b93fede1946f8401108f6db7f438ea51f4a`  
		Last Modified: Wed, 12 Jun 2024 19:10:16 GMT  
		Size: 71.4 MB (71354942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4193fcedbe8885741aea303f724e33cf4c75d3820f2f23ff6ef69d726ef51c`  
		Last Modified: Wed, 12 Jun 2024 19:10:06 GMT  
		Size: 87.7 KB (87739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e10c4346774dbc4dfa790a169612294e7b9ae1dfa3ea3ef5e8e595f2f3e96f6`  
		Last Modified: Wed, 12 Jun 2024 19:10:06 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
