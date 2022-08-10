## `golang:nanoserver-1809`

```console
$ docker pull golang@sha256:0b5347935f54a5a1a12c22a8098850fc4ff871aff561c3edebd9ab2a7bc9146c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `golang:nanoserver-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull golang@sha256:d5843e74790da22bd3d84d098dcbe21c7318a7c7c4db6bf1de09cb193e64c513
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.6 MB (260552831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ddab813e8e75d63c0af8a5f52f1ada63b89d9153862dfa7e2a511b05e9aeb0d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 13:04:30 GMT
SHELL [cmd /S /C]
# Wed, 10 Aug 2022 13:04:31 GMT
ENV GOPATH=C:\go
# Wed, 10 Aug 2022 13:04:32 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 13:05:04 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 10 Aug 2022 13:05:05 GMT
USER ContainerUser
# Wed, 10 Aug 2022 13:05:05 GMT
ENV GOLANG_VERSION=1.19
# Wed, 10 Aug 2022 13:07:35 GMT
COPY dir:a0f94dd1112f1f27c08d5ea3b68903d61c05f30a36f261cf395a623cb13deea1 in C:\Program Files\Go 
# Wed, 10 Aug 2022 13:08:17 GMT
RUN go version
# Wed, 10 Aug 2022 13:08:18 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9982991b820814ad737b2a161e973194e66b8d7b0a9890bee49cd158d7e77dec`  
		Last Modified: Wed, 10 Aug 2022 13:27:27 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb374f741579c100c895dcc59aa9485366514d2070780d936afb0cee10e2c3f6`  
		Last Modified: Wed, 10 Aug 2022 13:27:26 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732dbfa4c42c7cd3f8c88016834d3c06de0f03922e792273a4257c96c56f23b5`  
		Last Modified: Wed, 10 Aug 2022 13:27:25 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bbe06a1892b7650171a49f4f4a90a5d222516df1bf6d09c1f1cdd9d42d2188`  
		Last Modified: Wed, 10 Aug 2022 13:27:25 GMT  
		Size: 72.1 KB (72078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15263a6e39d76b9d2d60ec9ccee1249c09eb3e08cfb05422d0269497e268aeca`  
		Last Modified: Wed, 10 Aug 2022 13:27:25 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ebeb495bd3febf68a3488d7c73fdd53c7d6c65b91fa0f4d82092eb0d1f1af0`  
		Last Modified: Wed, 10 Aug 2022 13:27:24 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460984e65c4676f6a3f5c044ee98684b91f7b2c8c70b1954af144a2e6057b28e`  
		Last Modified: Wed, 10 Aug 2022 13:28:12 GMT  
		Size: 157.2 MB (157223995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109a63e20d99e5e7e6e5f4c629141b41e03f80db5d78196621049b1e91d7255e`  
		Last Modified: Wed, 10 Aug 2022 13:27:23 GMT  
		Size: 45.5 KB (45451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c52c6cbb5c1e1852256ea647463128f3d6850b4f8ab902b9ef9a23b2d30c1a`  
		Last Modified: Wed, 10 Aug 2022 13:27:23 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
