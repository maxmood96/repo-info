## `golang:nanoserver-ltsc2025`

```console
$ docker pull golang@sha256:c49fd67c260a4e40e59dfb868afe5553aeac6c722eda2018df9d065ff9932a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `golang:nanoserver-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull golang@sha256:9f58e20f48939f3df331030d4155e8fc443ab030cf473eea849491a07d699d4e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255542553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656835dfcbd1922114af1b50c7ee8a94bab60c7604057dd24885887c5e05ddf3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 10 Aug 2025 02:44:20 GMT
RUN Apply image 10.0.26100.4946
# Wed, 03 Sep 2025 19:11:04 GMT
SHELL [cmd /S /C]
# Wed, 03 Sep 2025 19:11:05 GMT
ENV GOPATH=C:\go
# Wed, 03 Sep 2025 19:11:06 GMT
USER ContainerAdministrator
# Wed, 03 Sep 2025 19:11:09 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 03 Sep 2025 19:11:09 GMT
USER ContainerUser
# Wed, 03 Sep 2025 19:11:10 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 19:12:36 GMT
COPY dir:0a07ceb8157b02a258e918dff195f7bc678184f2bc7d0201c6839d88e50214c1 in C:\Program Files\Go 
# Wed, 03 Sep 2025 19:12:39 GMT
RUN go version
# Wed, 03 Sep 2025 19:12:40 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:6d63d98dae9e3419e8c965c24a11d30e40947cf35ee17c204c5d8b7bae7ff2ef`  
		Last Modified: Tue, 12 Aug 2025 21:13:38 GMT  
		Size: 193.5 MB (193469373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9699f57920c53fd549719447592ff86930b1daf8a600e5e1ce90de9093b1ab`  
		Last Modified: Wed, 03 Sep 2025 19:13:18 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d990cd4b78735d10ac005d6f88faea0bc145d3e221bc1e357a593613e0c8971`  
		Last Modified: Wed, 03 Sep 2025 19:13:18 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f475abb82f87cf9db40439df2e99eb1402986007113f2a6ce61fda985a54171`  
		Last Modified: Wed, 03 Sep 2025 19:13:18 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d553cd867d86a11e8e381d58bc1feb787e6f96963bfd3cb12e976270555a18c`  
		Last Modified: Wed, 03 Sep 2025 19:13:18 GMT  
		Size: 75.8 KB (75829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd2824e2216cf40c57bfb01b8a0f20e1723dc51d85616c3907ef4f0a1865d68`  
		Last Modified: Wed, 03 Sep 2025 19:13:18 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4d3294af002b38bd3b071a901215f48a481467197980ebd7935aa8ff3ed20c`  
		Last Modified: Wed, 03 Sep 2025 19:13:18 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e57279cfadff88ed795803e56edb9b16653b895ae4382fdc756ae7afcca8463`  
		Last Modified: Wed, 03 Sep 2025 23:13:41 GMT  
		Size: 61.9 MB (61902544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7350668d10639011b9a32f33223a9d2c68cdd6c60a78c201f1d972a354d0c889`  
		Last Modified: Wed, 03 Sep 2025 19:13:18 GMT  
		Size: 88.2 KB (88240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23991f368b036abac231d72adb89357fe1da040aea6b1f211d9aecb540ca6fee`  
		Last Modified: Wed, 03 Sep 2025 19:13:18 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
