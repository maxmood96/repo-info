## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:f5a16d5fbfa6c7b8235e489918b70dd15c387ee9adbe40592e3e6c9846429742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull golang@sha256:3d97423c3963076dc275d8cddf9cffae8b82a611805b4d45e3a0aa139b748a6c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192025446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca72612b0a9f8d11f91c12aae307bff91329b8d993192a2e49898f54ec022242`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Wed, 10 Jul 2024 18:07:41 GMT
SHELL [cmd /S /C]
# Wed, 10 Jul 2024 18:07:42 GMT
ENV GOPATH=C:\go
# Wed, 10 Jul 2024 18:07:43 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 18:07:45 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 10 Jul 2024 18:07:46 GMT
USER ContainerUser
# Wed, 10 Jul 2024 18:07:47 GMT
ENV GOLANG_VERSION=1.22.5
# Wed, 10 Jul 2024 18:08:59 GMT
COPY dir:df9ea26aca7559ebf2412d95343abd7f451e9742ee3cc83124365ec0b4f8b5ea in C:\Program Files\Go 
# Wed, 10 Jul 2024 18:09:02 GMT
RUN go version
# Wed, 10 Jul 2024 18:09:02 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:652774a5d82a114642848f8b0b8d486ec1b4995f9dda56e36fe4ac7563429990`  
		Last Modified: Tue, 09 Jul 2024 20:33:26 GMT  
		Size: 120.5 MB (120490378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f7a610263e8c4d5756d59e63118730e5a257911d04a49e5823801e4e5c2543`  
		Last Modified: Wed, 10 Jul 2024 18:09:09 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de177b590aea957cf1825d795457cb6072f6cbea1bfc7c93e3444fef5f2875f3`  
		Last Modified: Wed, 10 Jul 2024 18:09:09 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3976045ed75ba8049796c8da51a7be2ce82c4d1b4ca1dc776aee7ab9a6194581`  
		Last Modified: Wed, 10 Jul 2024 18:09:08 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee9f00b84ed1a26e0a289808c228330cd0aeb7658601ad1f58ce90d098bf43b`  
		Last Modified: Wed, 10 Jul 2024 18:09:09 GMT  
		Size: 78.8 KB (78841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb36fcac3b1b1c0756bf734054b6409bcdf543f744383c0f004408aea9544460`  
		Last Modified: Wed, 10 Jul 2024 18:09:06 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa8ad420e8176380a47331fe156b8df507eb7921d952f97dcee23cbf8b69ce5`  
		Last Modified: Wed, 10 Jul 2024 18:09:07 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b640cf9562cf806b58672bd0baf9f36f000b2100fac95fd7400c4957e1592a86`  
		Last Modified: Wed, 10 Jul 2024 18:09:18 GMT  
		Size: 71.4 MB (71368621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012730654880ca38c6104c1a22f6654d24f0e4f2dd677561e4b1f10add903e55`  
		Last Modified: Wed, 10 Jul 2024 18:09:07 GMT  
		Size: 81.2 KB (81221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3475c5476a5d38d06c35dec140e9a08384630c876c393e0e96e35c5b7cf4e154`  
		Last Modified: Wed, 10 Jul 2024 18:09:06 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
