## `golang:nanoserver-1809`

```console
$ docker pull golang@sha256:f7684f9e64df48ac053e25fe3b1ebe285ff2421c136e8bb1776095053e5468c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `golang:nanoserver-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull golang@sha256:3992d9da360bd626b38289bf7fce9cbfba1321613e75d4f678c7e7353a4c0ab9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.9 MB (190855128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f893403413e44f3e2a3e3d6675ca85b1f932ba07bbad6437d5274942c491274`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 22:18:33 GMT
SHELL [cmd /S /C]
# Wed, 14 May 2025 22:18:36 GMT
ENV GOPATH=C:\go
# Wed, 14 May 2025 22:18:36 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 22:18:39 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 14 May 2025 22:18:39 GMT
USER ContainerUser
# Wed, 14 May 2025 22:18:40 GMT
ENV GOLANG_VERSION=1.24.3
# Wed, 14 May 2025 22:19:41 GMT
COPY dir:11c24136d74cfff65bad471f7cd999b92a92062aeed3b3acc0519a1823e1187a in C:\Program Files\Go 
# Wed, 14 May 2025 22:19:44 GMT
RUN go version
# Wed, 14 May 2025 22:19:45 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce80d4fb090916019fa82cf60ff7620284f60a1da3013fb400cc1ff17b3ec3`  
		Last Modified: Wed, 14 May 2025 22:19:49 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9a2188939ea16b62c6d944d2332f515e0ce4671491739534d28c4adc1d6666`  
		Last Modified: Wed, 14 May 2025 22:19:49 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9eddc3d6392f5bf426514f6984cd7f8c93500b04777e0d1ed624739676ad9e`  
		Last Modified: Wed, 14 May 2025 22:19:48 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588a3fe1e9e5eee80b49048450817daf1a7bf05b6000b2b771df9f936b8e66ad`  
		Last Modified: Wed, 14 May 2025 22:19:48 GMT  
		Size: 69.8 KB (69794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7b22fcc38c272842106683df47b6ba2d87091cb8ffbbf329e3649f8bb9a23a`  
		Last Modified: Wed, 14 May 2025 22:19:47 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11546c73200690e571012bbf6e17e10268ff51a03d331d7c6972dad091a6924b`  
		Last Modified: Wed, 14 May 2025 22:19:47 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d556710b6422fcecf5741ceea35b43a37dcb2936a5400902d6ac2c6603f5e6f1`  
		Last Modified: Wed, 14 May 2025 22:20:00 GMT  
		Size: 81.9 MB (81920889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0cabae6bb4cac4a641fced5e837e4ca10189c104112d7be83035e3b1edcdff`  
		Last Modified: Wed, 14 May 2025 22:19:48 GMT  
		Size: 77.1 KB (77060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9282c2b8b33b449134a298a0ee889e2b8f4865e24e8b3c227713c8a7b9baca7f`  
		Last Modified: Wed, 14 May 2025 22:19:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
