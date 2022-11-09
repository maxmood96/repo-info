## `golang:1-nanoserver-1809`

```console
$ docker pull golang@sha256:529258f7cf3531695b04c11c0ae51cdb5da34a9b117fdf98f8539dc04107fc34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `golang:1-nanoserver-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull golang@sha256:41a67362e7192260b83f0765cdd737f54a8ddde8f059865d0797145f78d94c12
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264197295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c182f4ba55f8a5fb2a770873750161423384aaf04457f6e7b4c439133fe681`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Wed, 09 Nov 2022 14:09:15 GMT
SHELL [cmd /S /C]
# Wed, 09 Nov 2022 14:09:16 GMT
ENV GOPATH=C:\go
# Wed, 09 Nov 2022 14:09:17 GMT
USER ContainerAdministrator
# Wed, 09 Nov 2022 14:09:59 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 09 Nov 2022 14:10:00 GMT
USER ContainerUser
# Wed, 09 Nov 2022 14:10:00 GMT
ENV GOLANG_VERSION=1.19.3
# Wed, 09 Nov 2022 14:12:46 GMT
COPY dir:798189c13a6684903929b21a3bd6bf202dfc338c18563ac8fe1e55a8be7c980c in C:\Program Files\Go 
# Wed, 09 Nov 2022 14:13:29 GMT
RUN go version
# Wed, 09 Nov 2022 14:13:30 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83e42a06a19f2d133476fa58d61bf56ed65a782146e4f8b37b3fc8727440fbd`  
		Last Modified: Wed, 09 Nov 2022 14:35:26 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d5f782c7567ec2c9cf757def907e4a540324f1214e9d33dba05ce0c41f3117`  
		Last Modified: Wed, 09 Nov 2022 14:35:26 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67651bffb2b07a227838e94750adbf37f15fe0f26d209f1e80f34f6e508077cf`  
		Last Modified: Wed, 09 Nov 2022 14:35:26 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba67c7baacb632dceb9b260126dcd011a1bdd570f6068decca6106fd87f9cd0`  
		Last Modified: Wed, 09 Nov 2022 14:35:25 GMT  
		Size: 77.1 KB (77078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1daf5190bbe54c04de26fde1d8743bbed1573873c68606a4eee93cd6ff162a3f`  
		Last Modified: Wed, 09 Nov 2022 14:35:23 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0e5e52e93e94a3efdf869abd02049d98a136ce131f38a87d815387aab108c3`  
		Last Modified: Wed, 09 Nov 2022 14:35:23 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c3d93fc9895cd700c9af627b6c92e5aa971ce23510167897a867ee4b6cd92e`  
		Last Modified: Wed, 09 Nov 2022 14:36:16 GMT  
		Size: 157.3 MB (157307312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1c9d3d3ec03b7a70bf1527f8d4d7dbbc6fdcce238de542b3c1c9deec01b881`  
		Last Modified: Wed, 09 Nov 2022 14:35:23 GMT  
		Size: 82.1 KB (82087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd84f94cf20e4cab6bdddba7f8c152ff3518d5af550adcd237c47dce55b672f`  
		Last Modified: Wed, 09 Nov 2022 14:35:23 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
