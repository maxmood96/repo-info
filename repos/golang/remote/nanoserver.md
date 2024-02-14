## `golang:nanoserver`

```console
$ docker pull golang@sha256:ec2bc730c57c21d545fb2176082df2f754a09c8494c27be793da03c363d4eb1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `golang:nanoserver` - windows version 10.0.20348.2322; amd64

```console
$ docker pull golang@sha256:5a98f4ef16cef6f23364fa153c2a72061ed8d2de799813561440befa9ff0049d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192333072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53493986832cf817828a19d500c92b269ec3d83a30173f8a7d1f9f3bcff37854`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 07 Feb 2024 06:29:10 GMT
RUN Apply image 10.0.20348.2322
# Wed, 14 Feb 2024 20:38:31 GMT
SHELL [cmd /S /C]
# Wed, 14 Feb 2024 20:38:32 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:38:33 GMT
USER ContainerAdministrator
# Wed, 14 Feb 2024 20:38:46 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 14 Feb 2024 20:38:47 GMT
USER ContainerUser
# Wed, 14 Feb 2024 20:38:48 GMT
ENV GOLANG_VERSION=1.22.0
# Wed, 14 Feb 2024 20:40:42 GMT
COPY dir:002c9f3689dddf68894e8a396363c27cb258d8144ee0755c02356813e34c4670 in C:\Program Files\Go 
# Wed, 14 Feb 2024 20:41:08 GMT
RUN go version
# Wed, 14 Feb 2024 20:41:08 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:ccff18da882d371921351307d169380d3ac22ef981f2bb4f14fb2b332b395439`  
		Last Modified: Tue, 13 Feb 2024 23:39:47 GMT  
		Size: 120.7 MB (120735093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd94364bba9212ea1145a07f60f20ecf74c1dbc066173a684a62d1c37f703d9`  
		Last Modified: Wed, 14 Feb 2024 20:59:00 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa87a65471f78f724c29e15f68da820559b690fbbf284729f3141bada288976`  
		Last Modified: Wed, 14 Feb 2024 20:59:00 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07cffd36429f90db815314b0e1d56ae23d39c757e6c690d62e416f6980606a0`  
		Last Modified: Wed, 14 Feb 2024 20:59:00 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07d3a8e7a85c8642a74056e633243371183a63335c92d8c763ec6f76fcaace1`  
		Last Modified: Wed, 14 Feb 2024 20:59:00 GMT  
		Size: 76.6 KB (76634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f284a08144c3064f8cf5b43b650415ee52adbd1a41834f82fc958d44aa46de`  
		Last Modified: Wed, 14 Feb 2024 20:58:58 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9c483b240103390865ad7b98e0a53fd30c6f13a9e2129b1a00c94f1dc97209`  
		Last Modified: Wed, 14 Feb 2024 20:58:58 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6772877a7bfaf84179ac3cf76cc2f6c75253c678563408ce32c07b8ba48de1`  
		Last Modified: Wed, 14 Feb 2024 20:59:20 GMT  
		Size: 71.5 MB (71461817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e725f5365ee50df65ad5f879c56cd404997e3c3ae05d1a6ff7f3fd5cdadf92d1`  
		Last Modified: Wed, 14 Feb 2024 20:58:58 GMT  
		Size: 52.4 KB (52413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca35e51deffdb238af20bef5c8ea42b6a6cdcae8f5824df884f85b88b5917c0b`  
		Last Modified: Wed, 14 Feb 2024 20:58:58 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.17763.5458; amd64

```console
$ docker pull golang@sha256:5c344b8353d34b54b22bdc121fdd580f07828848d05533be4f6953ba40808ea8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176240730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c378f6ff1b00d6b1ddf56509f2d9912f39f0bbce4d2190a1ff59c1f7482fbb27`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 20:41:15 GMT
SHELL [cmd /S /C]
# Wed, 14 Feb 2024 20:41:16 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:41:16 GMT
USER ContainerAdministrator
# Wed, 14 Feb 2024 20:41:28 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 14 Feb 2024 20:41:29 GMT
USER ContainerUser
# Wed, 14 Feb 2024 20:41:29 GMT
ENV GOLANG_VERSION=1.22.0
# Wed, 14 Feb 2024 20:43:24 GMT
COPY dir:002c9f3689dddf68894e8a396363c27cb258d8144ee0755c02356813e34c4670 in C:\Program Files\Go 
# Wed, 14 Feb 2024 20:43:46 GMT
RUN go version
# Wed, 14 Feb 2024 20:43:47 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d248fdc6ec2b1d559770e63dd96445cd0911b26f5aa34668bd0f97d8dcbf30dc`  
		Last Modified: Wed, 14 Feb 2024 20:59:40 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6586f461b549b8a21faa95d36d7d137b98e16be3d4378291ed02e515a45d16a`  
		Last Modified: Wed, 14 Feb 2024 20:59:41 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4a5e46c8ca02db6d6ce18763316cbc25eab61375eee1c1d30cb916693e7651`  
		Last Modified: Wed, 14 Feb 2024 20:59:40 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de7f9916de5860d517b863d5d66cad66e2c53492daba2f203e310de3d375e81`  
		Last Modified: Wed, 14 Feb 2024 20:59:40 GMT  
		Size: 68.8 KB (68790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6bbbec11a627dc9592bd963e17221216fb42732b6373e6b9722796eb69b04a`  
		Last Modified: Wed, 14 Feb 2024 20:59:38 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1c7d9c39f1a7b4f6a9c94aff5077ea064a5d897fa6b9536c4e5e154d4e587b`  
		Last Modified: Wed, 14 Feb 2024 20:59:38 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a64da6129cb03830ef8cb875081696b3ffe1f967227eca602f608dd88bacea`  
		Last Modified: Wed, 14 Feb 2024 21:00:00 GMT  
		Size: 71.5 MB (71462069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903b1a6c59bf6847d382a4b3ce8d59fb59d47e957039eae7ed3e30bd6eaff97a`  
		Last Modified: Wed, 14 Feb 2024 20:59:38 GMT  
		Size: 81.1 KB (81108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1affeaa1bccf89b9a93b46fbb8f02cecf99e2272f2ca21da53e9648b49c70a3`  
		Last Modified: Wed, 14 Feb 2024 20:59:38 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
