## `golang:nanoserver-1809`

```console
$ docker pull golang@sha256:bed123442cf35a89ffd3773414bbc52f60589733cc97ea8814e30157311ae5dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `golang:nanoserver-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull golang@sha256:a9c211e589f5a94236702d0d8dcbc7fb149b7d75bb967e74629a99ac1e6ceaea
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252500836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1672d715efa200e2d7b7e2a19af1a464a88544bd5d350f80710d64cdaad14e1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Jun 2022 19:20:11 GMT
RUN Apply image 10.0.17763.3046
# Wed, 15 Jun 2022 13:18:02 GMT
SHELL [cmd /S /C]
# Wed, 15 Jun 2022 13:18:03 GMT
ENV GOPATH=C:\go
# Wed, 15 Jun 2022 13:18:04 GMT
USER ContainerAdministrator
# Wed, 15 Jun 2022 13:18:45 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 15 Jun 2022 13:18:45 GMT
USER ContainerUser
# Wed, 15 Jun 2022 13:35:59 GMT
ENV GOLANG_VERSION=1.18.3
# Wed, 15 Jun 2022 13:39:02 GMT
COPY dir:f2d0f4a9267a591c33858aceb464994502f206b1bde0c83972e6f9e2e21fe641 in C:\Program Files\Go 
# Wed, 15 Jun 2022 13:39:50 GMT
RUN go version
# Wed, 15 Jun 2022 13:39:51 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:d555a7e4de4dd775379d5c43c1419374bff7908670dc7444be5e8e8f386f3d26`  
		Size: 103.2 MB (103153235 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ec2e0a40359897e8d5f91d9806e952d9783f2bc30dd279b63a217ee6985ef3c`  
		Last Modified: Wed, 15 Jun 2022 14:07:45 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f18dc68851662b98200fb7de7f822468bd93a0f0f293f59b3db2e755bc1249`  
		Last Modified: Wed, 15 Jun 2022 14:07:44 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a7460e7150b7c82d66f95948c85585275de203b44fd138f064986b85e4b466`  
		Last Modified: Wed, 15 Jun 2022 14:07:44 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e78abf157090fa6fe2e0a1171a2d4a3a921c8121c0e5ac21f8436392572c8d`  
		Last Modified: Wed, 15 Jun 2022 14:07:45 GMT  
		Size: 76.6 KB (76615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdf601a0023b7c1d8e5be26abe357dcb4fd83d3105312c67a3eea6e77810658`  
		Last Modified: Wed, 15 Jun 2022 14:07:42 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284617b435fa22960577123df406652281d515928f7bb7d868343666846a5184`  
		Last Modified: Wed, 15 Jun 2022 14:17:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f88e2919916a088c98a63c4a892d71bbf67b886f2fac5a7671bc1115a8cba1`  
		Last Modified: Wed, 15 Jun 2022 14:20:40 GMT  
		Size: 149.2 MB (149183428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53ecc952e75400d2e66ca89aec381124a1f20dc15921ea9919111d77ea28b8b`  
		Last Modified: Wed, 15 Jun 2022 14:17:55 GMT  
		Size: 80.6 KB (80590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f788f3f2e9fe353bf9881b4ae3c0d67b5c9bc6cdd2ad195a8c24e83ea87b82`  
		Last Modified: Wed, 15 Jun 2022 14:17:55 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
