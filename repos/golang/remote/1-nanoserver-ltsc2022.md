## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:9a2e8628caf59dd3f51bf0fe189795c075ee630bff33dbe57f8eba22c436f8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1487; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.1487; amd64

```console
$ docker pull golang@sha256:d64ce3e54b6c0f4951ead02ea42276e8fd56d965f4051b98506e9bec00bd0faa
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230154466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f9b7c9dc78a7ada83ef053788ad2e5a926cb43b1fd17a15d893465b95f1f196`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 06 Jan 2023 23:36:49 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 03:07:34 GMT
SHELL [cmd /S /C]
# Thu, 12 Jan 2023 03:07:34 GMT
ENV GOPATH=C:\go
# Thu, 12 Jan 2023 03:07:36 GMT
USER ContainerAdministrator
# Thu, 12 Jan 2023 03:08:26 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 12 Jan 2023 03:08:27 GMT
USER ContainerUser
# Wed, 01 Feb 2023 22:24:32 GMT
ENV GOLANG_VERSION=1.20
# Wed, 01 Feb 2023 22:27:14 GMT
COPY dir:c7140b386197a562a25dc3c23e0af1e46a3c2afadf221ac74e00b24bfef62bb7 in C:\Program Files\Go 
# Wed, 01 Feb 2023 22:28:05 GMT
RUN go version
# Wed, 01 Feb 2023 22:28:06 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:83e9437e818022c1c28f0e07002dd46995c8614e62b9366138fa23b94f43d9ad`  
		Last Modified: Thu, 12 Jan 2023 02:51:06 GMT  
		Size: 122.1 MB (122099566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e0e139d1c09b743fda52fd8a19bdc3c829ac2aed829d2e16beec0fbbd5dd5d`  
		Last Modified: Thu, 12 Jan 2023 03:48:59 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4e8737aebbf1207ce8659de66f3d575194350678800b69a174bc516a329dea`  
		Last Modified: Thu, 12 Jan 2023 03:48:59 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611ab0a2da8d60a13ec497aa6f89b840f936a6c6f7450f0386f808c000f44970`  
		Last Modified: Thu, 12 Jan 2023 03:48:59 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3c63725f8ca8d354e6c46948328eda4a7c428e21bfedbd5005b674e23fbf73`  
		Last Modified: Thu, 12 Jan 2023 03:48:59 GMT  
		Size: 84.0 KB (84048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42b910fe2ecce44f108e85c2c03f9acb106e857aa6b7f2e4622891aa961b4bf`  
		Last Modified: Thu, 12 Jan 2023 03:48:57 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564d0cd2cfdd10c13970163cf6020756bda9c61af5ce64d49a47c2a6dcee78d7`  
		Last Modified: Wed, 01 Feb 2023 22:35:01 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813e312e2cd44e361feb8185efd5e0b91c10e8330d68cfbd8a1287de1ecb243f`  
		Last Modified: Wed, 01 Feb 2023 22:35:31 GMT  
		Size: 107.9 MB (107914655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43eb2e42eb273413aaca607e25623bb9ef49fc113e72bfd4c9cf62f550c69eb`  
		Last Modified: Wed, 01 Feb 2023 22:35:00 GMT  
		Size: 49.3 KB (49273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52996914f6da0438b4178d6f682d298fdfae97b100aa670414c1dde32e847e3d`  
		Last Modified: Wed, 01 Feb 2023 22:35:00 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
