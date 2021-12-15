## `golang:rc-nanoserver-1809`

```console
$ docker pull golang@sha256:4ebf6b3b9b569130e9a661bdea141c26368f78f4d596f230f6fc9fc2010c0580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `golang:rc-nanoserver-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull golang@sha256:6dd521b0c5ee99ca08bf0c5dfce8dfb3e3e81237379483ab19efa46e174d8f19
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254723314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2bb278a66a85a47f146ab6687330e2028d4ae131c60ce1cbee481fb54e1ac3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Wed, 15 Dec 2021 01:05:08 GMT
SHELL [cmd /S /C]
# Wed, 15 Dec 2021 01:05:10 GMT
ENV GOPATH=C:\go
# Wed, 15 Dec 2021 01:05:11 GMT
USER ContainerAdministrator
# Wed, 15 Dec 2021 01:05:35 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 15 Dec 2021 01:05:35 GMT
USER ContainerUser
# Wed, 15 Dec 2021 01:05:36 GMT
ENV GOLANG_VERSION=1.18beta1
# Wed, 15 Dec 2021 01:08:07 GMT
COPY dir:abc41c2687fe2e0d7e54b068cc7bb77e17d59bec655dd6e83b05fea7910e798c in C:\Program Files\Go 
# Wed, 15 Dec 2021 01:08:52 GMT
RUN go version
# Wed, 15 Dec 2021 01:08:53 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f6e2c96db2bf5f7145097ec413d670382424bdefcc277e5a2fc8226ab4fe949`  
		Last Modified: Wed, 15 Dec 2021 01:56:22 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f891f84ddd60832c4b29ece068492db0be44693d884f38408d2dda2a55dd43`  
		Last Modified: Wed, 15 Dec 2021 01:56:22 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01532dba2d359c6d6d0acbd787b3e509dfc8aae8306343c0406a301c57fdab25`  
		Last Modified: Wed, 15 Dec 2021 01:56:21 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3dc4a9978971608524735fe0bed920bb9046e2609ceb7dddc5c86ed6a199611`  
		Last Modified: Wed, 15 Dec 2021 01:56:21 GMT  
		Size: 70.7 KB (70700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b255b2f880492b8241cd7b4a6b151a9ca9065d34321b683d84c37206a0f4a552`  
		Last Modified: Wed, 15 Dec 2021 01:56:19 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a66eeb574c994f28af7f7455ffa2d16e80bda3996ac3dea4b5164db6413bece`  
		Last Modified: Wed, 15 Dec 2021 01:56:19 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db1a5c652b73f1c475f907987272750504bc2b5218f7caecfbb5fe6a56ffa18`  
		Last Modified: Wed, 15 Dec 2021 01:56:54 GMT  
		Size: 151.7 MB (151658015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f6e375c3ce2cba8e643fb90e4e6a61dcf585c9e83e96289b19dee98f7992ca`  
		Last Modified: Wed, 15 Dec 2021 01:56:19 GMT  
		Size: 83.4 KB (83430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ced23771c89d0597b1bea64e2c15d4203d91b1674216793458641366bbfd64`  
		Last Modified: Wed, 15 Dec 2021 01:56:19 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
