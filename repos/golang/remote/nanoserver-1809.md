## `golang:nanoserver-1809`

```console
$ docker pull golang@sha256:ca6c716efa79205160afcec5a2de1fb9d408526898ba971c0b8784780a29a55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `golang:nanoserver-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull golang@sha256:df507fe950fd6aefb1a457c4c1d7828533e4fe810f4efab8df4c76474c8073ae
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 MB (248340320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb28922f80ad23575306645a342f25e7081bc7207d9b727c6321d48f84dc8cf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 13:53:17 GMT
SHELL [cmd /S /C]
# Wed, 09 Feb 2022 13:53:18 GMT
ENV GOPATH=C:\go
# Wed, 09 Feb 2022 13:53:18 GMT
USER ContainerAdministrator
# Wed, 09 Feb 2022 13:53:36 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 09 Feb 2022 13:53:37 GMT
USER ContainerUser
# Wed, 09 Feb 2022 14:08:02 GMT
ENV GOLANG_VERSION=1.17.6
# Wed, 09 Feb 2022 14:10:19 GMT
COPY dir:7d325dd3c7e81bd29326c5fb7b320ff307098f97c2703658681dad899622f617 in C:\Program Files\Go 
# Wed, 09 Feb 2022 14:11:09 GMT
RUN go version
# Wed, 09 Feb 2022 14:11:10 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4cc9ef1ef09cb03b1e0bcf4dd4f522871216249d6274e1708e2d4ac554954f34`  
		Last Modified: Wed, 09 Feb 2022 14:37:35 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5779598c13bb3e08d7f4d935491fb18f653c01203f588ca53b5b7cfbad87853`  
		Last Modified: Wed, 09 Feb 2022 14:37:34 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ed348d246f1144e12e763bcccfe197870daa37a206e81fda25e13da6216d2c`  
		Last Modified: Wed, 09 Feb 2022 14:37:33 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a586a7e6e6c370d20a3b167c8aaf3fe683d12d23e8fbb17581c8abc4bf8b0c`  
		Last Modified: Wed, 09 Feb 2022 14:37:33 GMT  
		Size: 71.3 KB (71275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d22d16652ddca955c0d35dcfa5f7485e68e36021e320dbff745d0b025700e3`  
		Last Modified: Wed, 09 Feb 2022 14:37:31 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e13770aa248904ab77f57da834b68e650f6dedc02320085a35704c86a5555d`  
		Last Modified: Wed, 09 Feb 2022 14:49:17 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29034f053051cfb37fb9fae96ce93fc8fb3c63b5be06ff44ec3e4413cc305e5b`  
		Last Modified: Wed, 09 Feb 2022 14:49:51 GMT  
		Size: 145.1 MB (145100880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14083e947fb54ea11a3e729218bbe545261ebee460d31d1d79e6d4c19c90d9e9`  
		Last Modified: Wed, 09 Feb 2022 14:49:17 GMT  
		Size: 74.0 KB (73981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e58015c6124d78995d89d8b46b53052f93f3d1ca53bc638261c9610e52d01d5`  
		Last Modified: Wed, 09 Feb 2022 14:49:17 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
