## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:b71786ae47a870274bbe0d4fe3f5b1e20b2c0d3eae29e3dacae2d4e7422e7cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1129; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.1129; amd64

```console
$ docker pull golang@sha256:be239a4f223fe8471715660c0dbb31d7461f1da45256d76fb5ff5e64dfeb358c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 MB (279403540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a92b811d78615219eacadb769195a255b9dd793d3142c4f1252eae9e80ddb2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Oct 2022 21:37:41 GMT
RUN Apply image 10.0.20348.1129
# Wed, 12 Oct 2022 12:51:25 GMT
SHELL [cmd /S /C]
# Wed, 12 Oct 2022 12:51:26 GMT
ENV GOPATH=C:\go
# Wed, 12 Oct 2022 12:51:26 GMT
USER ContainerAdministrator
# Wed, 12 Oct 2022 12:52:17 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 12 Oct 2022 12:52:17 GMT
USER ContainerUser
# Tue, 01 Nov 2022 19:26:08 GMT
ENV GOLANG_VERSION=1.19.3
# Tue, 01 Nov 2022 19:29:05 GMT
COPY dir:798189c13a6684903929b21a3bd6bf202dfc338c18563ac8fe1e55a8be7c980c in C:\Program Files\Go 
# Tue, 01 Nov 2022 19:29:59 GMT
RUN go version
# Tue, 01 Nov 2022 19:30:00 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:b6520318982addabaf67d0cef5499282d15348f205cf5d7328925bcd681e85bd`  
		Last Modified: Tue, 25 Oct 2022 22:04:15 GMT  
		Size: 122.0 MB (122003513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9abf6e1518124a035a9bbaf0dad0924d5286be7dc0ee052f1225355c2e68da7`  
		Last Modified: Wed, 12 Oct 2022 13:17:17 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1a05eb086128aa5209bbd6a53d080b706f5ba02d90319bac1ae748bd277b59`  
		Last Modified: Wed, 12 Oct 2022 13:17:17 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6cf59dc3a7ca9816cacef203e2e6a8a4cde3060b92affa21d3bb48afe3ac78`  
		Last Modified: Wed, 12 Oct 2022 13:17:17 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48576001e81f34a54b49993c9d72be646fbb21c51288f1bff0dc553c777f83a2`  
		Last Modified: Wed, 12 Oct 2022 13:17:17 GMT  
		Size: 85.9 KB (85857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fbc6112ad01bb79cdee313cd41d392c340336479be92f8fd30e677bc61543be`  
		Last Modified: Wed, 12 Oct 2022 13:17:14 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed4632e454a63e191c04bd156fad07e38d45757c518e83a71c0efff01771bcf`  
		Last Modified: Tue, 01 Nov 2022 19:55:51 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9db10181eb9fecb943802fb246ebeef439950df04b1f80f1f694f610d9f68cb`  
		Last Modified: Tue, 01 Nov 2022 19:56:43 GMT  
		Size: 157.2 MB (157242276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea882d3efe6a01aed8329526dcd68e0100ea0841ac58d05156fee018f0e141f`  
		Last Modified: Tue, 01 Nov 2022 19:55:51 GMT  
		Size: 64.8 KB (64777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e63b48a27cabdc28c19334f055060b2be049ce17052405cf1c534b1364249c`  
		Last Modified: Tue, 01 Nov 2022 19:55:51 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
