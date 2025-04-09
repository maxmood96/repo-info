## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:1513b5b972dd52f47f2b37fabb4bc025223d63fd38f34c31495ef88ebe898d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull golang@sha256:9e69fbce3ab15b2f3d5fe4c82f55164862e476849737db029091c2e73c300e45
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202721028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66415b6a86291ceac146db2bd5d0925115f553facdc0b4378f8baadcbe28b8f1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 01:22:28 GMT
SHELL [cmd /S /C]
# Wed, 09 Apr 2025 01:22:29 GMT
ENV GOPATH=C:\go
# Wed, 09 Apr 2025 01:22:29 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:22:32 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 09 Apr 2025 01:22:32 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:22:33 GMT
ENV GOLANG_VERSION=1.24.2
# Wed, 09 Apr 2025 01:24:25 GMT
COPY dir:c31dd4b35955c3b7ad87aee80c32a76880e815054766f9fc2b5a42c53d1c95ce in C:\Program Files\Go 
# Wed, 09 Apr 2025 01:24:28 GMT
RUN go version
# Wed, 09 Apr 2025 01:24:28 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc3ddc7301e8f3e22b42f3c3a6f001e006eb4adc38ff152e029ae45044c841e`  
		Last Modified: Wed, 09 Apr 2025 01:24:32 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1be42b7509310fa4f1e903f10b3abed420cda3ae4cc17d589e12303b7f2941`  
		Last Modified: Wed, 09 Apr 2025 01:24:32 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716fa522579dee364f7a233abfc2a15bb6b8decc6292a8f32cb887f907346d26`  
		Last Modified: Wed, 09 Apr 2025 01:24:32 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c19066c440307925bab270a98df411ac79207490ea1baf566260c2cf2c0d46`  
		Last Modified: Wed, 09 Apr 2025 01:24:32 GMT  
		Size: 75.9 KB (75881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44aaf82202852056d91b7ad081cf9c43db0638af98551daa3c4b43e6aa21d7de`  
		Last Modified: Wed, 09 Apr 2025 01:24:31 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89b6f041d9935b9b85aa2228f077a260f4854a6d2442e95b5b4ed70e0f7afb1`  
		Last Modified: Wed, 09 Apr 2025 01:24:31 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265f600cff2eb976f6d349579e3431d634d23d7179eaf53df94456a471b56396`  
		Last Modified: Wed, 09 Apr 2025 01:24:43 GMT  
		Size: 81.8 MB (81823960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f9cfafc7e8452e9503c4590aa723a5138696f79452501eecebbdc0e5ec6d46`  
		Last Modified: Wed, 09 Apr 2025 01:24:31 GMT  
		Size: 78.4 KB (78367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6ffbe17aa8cad8eaeba86be588e2487d890e9c8e21f99bbdf14f272fbee543`  
		Last Modified: Wed, 09 Apr 2025 01:24:31 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
