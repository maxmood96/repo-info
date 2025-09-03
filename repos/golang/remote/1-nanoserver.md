## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:6fcb95d2fa50e1cca23912ae45a9b901bb2c8c3e84e8842d8da5297bbf20abdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `golang:1-nanoserver` - windows version 10.0.26100.4946; amd64

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
		Last Modified: Wed, 03 Sep 2025 19:12:58 GMT  
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

### `golang:1-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull golang@sha256:906ef73eab2e6b55f29a9406243d0f88455b5ca2051d86a1d0f2947a2a26d307
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184682868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9ed77c3c0e5b0629f894d8e8c671d14c8d27e43a2314ad7406ba087d7b0428`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Wed, 03 Sep 2025 19:05:10 GMT
SHELL [cmd /S /C]
# Wed, 03 Sep 2025 19:05:11 GMT
ENV GOPATH=C:\go
# Wed, 03 Sep 2025 19:05:12 GMT
USER ContainerAdministrator
# Wed, 03 Sep 2025 19:05:18 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 03 Sep 2025 19:05:18 GMT
USER ContainerUser
# Wed, 03 Sep 2025 19:05:19 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 19:06:55 GMT
COPY dir:0a07ceb8157b02a258e918dff195f7bc678184f2bc7d0201c6839d88e50214c1 in C:\Program Files\Go 
# Wed, 03 Sep 2025 19:06:59 GMT
RUN go version
# Wed, 03 Sep 2025 19:07:00 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f4bf14ada8ee3c16d71bbb4c87b70cccf3e027a0428c77ad36cef1cd10573d`  
		Last Modified: Wed, 03 Sep 2025 19:07:51 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d293f5c94f9a79f2315dcb54a8593b7a73f470ea2a8204d1d8ae3f93b2d526`  
		Last Modified: Wed, 03 Sep 2025 19:07:52 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f167d94c568b0d369843e4e214719b3d6d6931a549365cb178eebf346f343c`  
		Last Modified: Wed, 03 Sep 2025 19:07:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ea89bc09f3dd6bedbb28a998c5959fa3b480ecf7617206f45f4f01e5c8e6c4`  
		Last Modified: Wed, 03 Sep 2025 19:07:51 GMT  
		Size: 73.6 KB (73637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1dc1846745a137ce29c51c2203a95307111cb6e3192dc0f7f08ccf425dce2b5`  
		Last Modified: Wed, 03 Sep 2025 19:07:52 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7acc20722ab994b64c7e442ad30fb8e4434031a096aa9df815a10d4911cd46c`  
		Last Modified: Wed, 03 Sep 2025 19:07:51 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3595f35aa961f5666dd8ca87af00f32d4d1f3519cb62e124583be80e97ba3dfb`  
		Last Modified: Wed, 03 Sep 2025 19:08:02 GMT  
		Size: 61.9 MB (61864695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0001bdb7ba545790477ecf7b35ab2ff355b098115eebf6a4d7eb75031fbf2513`  
		Last Modified: Wed, 03 Sep 2025 19:07:52 GMT  
		Size: 77.7 KB (77720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d144d0fbe8aea49ca76810494b638301507a52f22c25c8700b0539a389c5c275`  
		Last Modified: Wed, 03 Sep 2025 19:07:52 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
