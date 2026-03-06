## `golang:nanoserver`

```console
$ docker pull golang@sha256:001d86ea06efeeeeea58ecdae8b6de92dcb213cfa8d11469ab3c0ba1c940788b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `golang:nanoserver` - windows version 10.0.26100.32370; amd64

```console
$ docker pull golang@sha256:f8c01b327ef0c9a39fa5eeb32c65b3d9f7e3cd944cadd9dbd9c4326997bee945
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268548660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc34178efb42de30a58ed51d9ff34d2ec393cc4f504c044d977823aceb3f414f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Fri, 06 Mar 2026 01:58:33 GMT
SHELL [cmd /S /C]
# Fri, 06 Mar 2026 01:58:34 GMT
ENV GOPATH=C:\go
# Fri, 06 Mar 2026 01:58:34 GMT
USER ContainerAdministrator
# Fri, 06 Mar 2026 01:58:44 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Fri, 06 Mar 2026 01:58:45 GMT
USER ContainerUser
# Fri, 06 Mar 2026 01:58:45 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 02:00:54 GMT
COPY dir:075c372929040b7949c230fc01c695c61ff90e3e4ea8f5872f2353ec5724269a in C:\Program Files\Go 
# Fri, 06 Mar 2026 02:00:56 GMT
RUN go version
# Fri, 06 Mar 2026 02:00:57 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b138462fb51229ac30cd47110e1c7b6f7cacea7a4d24bc3248261f7cb33a77`  
		Last Modified: Fri, 06 Mar 2026 02:01:13 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbaab251b5a9f3b7f101de9235bceb8ab1eef2c3ca917f7b683048543cc566ca`  
		Last Modified: Fri, 06 Mar 2026 02:01:12 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02871027d0508cfaa6e887bffa8f35bf1f0c636f092e280690cf070fe2d9419`  
		Last Modified: Fri, 06 Mar 2026 02:01:13 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd18aae7407a52bddd71e3e5f1dcf0874f7944a07e6e56e19868aed753feafc4`  
		Last Modified: Fri, 06 Mar 2026 02:01:12 GMT  
		Size: 70.1 KB (70099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9b0e4038b3ae16306f32a1e56fb1e38c0060b09ae22846c06f8a105a5ccbe9`  
		Last Modified: Fri, 06 Mar 2026 02:01:11 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7df8bb889d059dc6d35214803bf78ee0bc901745db2c2a68d2ee059c1706c1`  
		Last Modified: Fri, 06 Mar 2026 02:01:10 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb3c0a6cfb6ae5b1037ed014c1da0a2f5e8f3b9623e4df4e5c65fbd96120be9`  
		Last Modified: Fri, 06 Mar 2026 02:01:21 GMT  
		Size: 69.1 MB (69145656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad8a51ef1af59d92d11d94f08e1129707308bee60da0a2aeaca5931395162fe`  
		Last Modified: Fri, 06 Mar 2026 02:01:10 GMT  
		Size: 74.7 KB (74663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c553f8b5914f0dca47f0b7d1043fb1afdffa0a08f6d28967fd5462b8ca93445`  
		Last Modified: Fri, 06 Mar 2026 02:01:10 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.20348.4773; amd64

```console
$ docker pull golang@sha256:c8aba46dc242c725c0c4a03851affe3c17c9cf7208334351fe48159d6d9df06e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (195961348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3943852ac998e9388a40c475b51b0bd42253a0e8622681d5f2e715bdf68ea56`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Fri, 06 Mar 2026 01:58:36 GMT
SHELL [cmd /S /C]
# Fri, 06 Mar 2026 01:58:36 GMT
ENV GOPATH=C:\go
# Fri, 06 Mar 2026 01:58:37 GMT
USER ContainerAdministrator
# Fri, 06 Mar 2026 01:58:47 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Fri, 06 Mar 2026 01:58:47 GMT
USER ContainerUser
# Fri, 06 Mar 2026 01:58:48 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 02:00:47 GMT
COPY dir:075c372929040b7949c230fc01c695c61ff90e3e4ea8f5872f2353ec5724269a in C:\Program Files\Go 
# Fri, 06 Mar 2026 02:00:50 GMT
RUN go version
# Fri, 06 Mar 2026 02:00:51 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc23f689fca79e6ee35d1d5e9ccbdfcc9d474e108238a51ab930273a21e36b72`  
		Last Modified: Fri, 06 Mar 2026 02:01:01 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b163dd429141ef8aa080bc5dd8eaeb45924e23aa4db498b307ee4eeacd7241d`  
		Last Modified: Fri, 06 Mar 2026 02:01:02 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f4e7b55e9031b83386ba9222e97d6211bcd44c8a8b8f5fe20b9a912cb3a657`  
		Last Modified: Fri, 06 Mar 2026 02:01:00 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ab1fabc6fd2a1381c7271de08744d97ca0fcb579e3dc1f66f29be9cb1bbb87`  
		Last Modified: Fri, 06 Mar 2026 02:01:00 GMT  
		Size: 82.6 KB (82610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9d41105b193d32f8769196d34cf4443db4232eb657daeac4114e5a507389e8`  
		Last Modified: Fri, 06 Mar 2026 02:01:02 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bdc2da1c78966f66efbfd862db1d8c4a3bf494f0c18901905787b43a3eadfc`  
		Last Modified: Fri, 06 Mar 2026 02:00:58 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cff3833e6c6cfbd1965ace1f2cc6435de155a4521b1143ec1865e2c28175af1`  
		Last Modified: Fri, 06 Mar 2026 02:01:09 GMT  
		Size: 69.1 MB (69144953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad68ea4b971ea3dc7c72f23b0aef2397bdb8530b671cb5650022b89e3c05b9f1`  
		Last Modified: Fri, 06 Mar 2026 02:00:58 GMT  
		Size: 81.4 KB (81414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42be92490a015d23a1ba5d9952d15d526011594e91e5cc549647687bf65b9d9d`  
		Last Modified: Fri, 06 Mar 2026 02:00:58 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
