## `golang:rc-nanoserver-1809`

```console
$ docker pull golang@sha256:903b3a81e1e6667ba842297a2dbdf3d76ca8a091dff7ebac077ecf50093d4aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `golang:rc-nanoserver-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull golang@sha256:32721ea7740e66fa4aaac9a7135c207ac735a23ba49049b701143e3f5b7175e6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255290380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1688f60e1747e59da2488cd93fc305388ca2480a572dbe1ce1aca0ff7b7f1160`
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
# Wed, 09 Feb 2022 13:53:38 GMT
ENV GOLANG_VERSION=1.18beta2
# Wed, 09 Feb 2022 13:56:17 GMT
COPY dir:71b79cea25a0f7926c53d5d3ecfe583efc6c6e6b413ed2254acd66bf37c90389 in C:\Program Files\Go 
# Wed, 09 Feb 2022 13:56:59 GMT
RUN go version
# Wed, 09 Feb 2022 13:57:00 GMT
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
	-	`sha256:92dc5e14b4a39a72d38377fe9510bef7efdaecce40b5c1e50e089bfb0fdeacac`  
		Last Modified: Wed, 09 Feb 2022 14:37:31 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bc0e61e126def4f981acbff65953367d3af49f53c9e1acd6f7d22da58b28df`  
		Last Modified: Wed, 09 Feb 2022 14:40:20 GMT  
		Size: 152.0 MB (152048220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b2457be0dd72ba30b99e494eb687ef3c43a8e7aac6bad93c395fe64d8c3ea4`  
		Last Modified: Wed, 09 Feb 2022 14:37:31 GMT  
		Size: 76.7 KB (76729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97db88ba542048408b35c5400f8aab59eaed623303ca9b44a950e33e183f8de1`  
		Last Modified: Wed, 09 Feb 2022 14:37:31 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
