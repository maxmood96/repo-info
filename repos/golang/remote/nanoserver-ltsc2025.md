## `golang:nanoserver-ltsc2025`

```console
$ docker pull golang@sha256:745bb7b0efd25f7f117cf5618f44c2bea3ea999c876a6df51a910be866c44b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `golang:nanoserver-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull golang@sha256:bb8416b7852b3498e859719888baa3c20b87c3d71936e4a54be68a8d7fcbb351
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.1 MB (266059770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4972822e95b0459aa8558b4e1da12906607c0ab89b8c6fff09020e237b84d3bc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Tue, 09 Jun 2026 23:22:17 GMT
SHELL [cmd /S /C]
# Tue, 09 Jun 2026 23:22:18 GMT
ENV GOPATH=C:\go
# Tue, 09 Jun 2026 23:22:19 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:22:21 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 09 Jun 2026 23:22:21 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:22:22 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 09 Jun 2026 23:23:37 GMT
COPY dir:a4d5515d1dbeb183f1060174907c1c319fc78bf773c3b4147ef7f7bec4c9f4ad in C:\Program Files\Go 
# Tue, 09 Jun 2026 23:23:40 GMT
RUN go version
# Tue, 09 Jun 2026 23:23:41 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef213a1a807cc466b6d945fdc09dbbb9327169ff63b8ec54e28a5e8836f00050`  
		Last Modified: Tue, 09 Jun 2026 23:23:49 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5db72efba64a0a1e3a4a45abc9694380ce86717996e96da66951978a5442af`  
		Last Modified: Tue, 09 Jun 2026 23:23:49 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a57ede2eb09e9602c008da7754a11439854e0833e993928b3f876b1eec8a557`  
		Last Modified: Tue, 09 Jun 2026 23:23:49 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08868a794fec3608e8a5007c7126b40794628ef61c5c7dae217ed9505f6fe839`  
		Last Modified: Tue, 09 Jun 2026 23:23:49 GMT  
		Size: 72.3 KB (72259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12db7374c7a8ddc231a370bb4fa384f4e71f62b0b1e61d8bb0bec64975951692`  
		Last Modified: Tue, 09 Jun 2026 23:23:47 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfc80367a82c3d4d9f5ffc7093d0088a557b5ec6ea4f198ad134b3a32ec5eb3`  
		Last Modified: Tue, 09 Jun 2026 23:23:47 GMT  
		Size: 1.0 KB (1005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1dee35a2fc244904ee23d2826c5e74354f83fbeee298f0be7d1b58ee0ce038`  
		Last Modified: Tue, 09 Jun 2026 23:23:59 GMT  
		Size: 69.2 MB (69234620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b2628e60bf145f0578ad6b8d653a7fefa0fae0c4e6ea82264788c790b8f1c4`  
		Last Modified: Tue, 09 Jun 2026 23:23:47 GMT  
		Size: 78.4 KB (78417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f560bb0e21e9f7b54aab9a9518c60ddde567affd42d78ec4d3c76261cedbc696`  
		Last Modified: Tue, 09 Jun 2026 23:23:47 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
