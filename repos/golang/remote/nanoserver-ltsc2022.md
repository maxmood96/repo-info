## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:b35a33363b1b976db41b48ce3b641bf47f6baeb49b56aa2f33673860d6c01ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1970; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.1970; amd64

```console
$ docker pull golang@sha256:7e0d35eacbe89ec787477af4945e15e6678190fdfc449159d3c5754393652431
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.8 MB (189779645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d1f410bbf787f67ceec046895cade50ee7e99b0c828453cea9e5d5a26f94fd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 01 Sep 2023 00:20:14 GMT
RUN Apply image 10.0.20348.1970
# Wed, 13 Sep 2023 01:45:13 GMT
SHELL [cmd /S /C]
# Wed, 13 Sep 2023 01:45:13 GMT
ENV GOPATH=C:\go
# Wed, 13 Sep 2023 01:45:14 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 01:45:30 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 13 Sep 2023 01:45:30 GMT
USER ContainerUser
# Tue, 10 Oct 2023 19:20:24 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:22:08 GMT
COPY dir:af619581ed50e9a9022bf0c987a1da2c20aafc1c50d911f1206fcd3d4c232de2 in C:\Program Files\Go 
# Tue, 10 Oct 2023 19:22:20 GMT
RUN go version
# Tue, 10 Oct 2023 19:22:20 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:8f8cef0759210af9d01a2fb45d79956a2db738bbd3734b7244b17e14ad945cab`  
		Last Modified: Tue, 12 Sep 2023 18:47:39 GMT  
		Size: 120.6 MB (120567584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c795bb9d48e9fa247e549604525fcb2599507cf1008aa1df12036f428ea236d`  
		Last Modified: Wed, 13 Sep 2023 02:18:07 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfefaf16c2467f3b414f23f271a0b3500e0e6e4b5a6c283d9d4504942bb41d0b`  
		Last Modified: Wed, 13 Sep 2023 02:18:07 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8af5eba6c23e059dfc62ac724d10f9b02be442608028bed7e0439b86b148da`  
		Last Modified: Wed, 13 Sep 2023 02:18:07 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b58761750bd8ba8ee22556e6be99c30963fbac0e030c41564ed881a6a80fcf`  
		Last Modified: Wed, 13 Sep 2023 02:18:07 GMT  
		Size: 80.9 KB (80890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c227eff309d8eb3e6b97da880ffba88c776a248aa79e78574def6dd088dbe6f7`  
		Last Modified: Wed, 13 Sep 2023 02:18:05 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd7906b3fb429bedd1142ae5461b49d902b5beb0536582d6dd372c96614bb7f`  
		Last Modified: Tue, 10 Oct 2023 19:35:50 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0135972fe9ebe6f214af19e32b14885ad4e7bb5d133865519de44b6ce36add2`  
		Last Modified: Tue, 10 Oct 2023 19:36:08 GMT  
		Size: 69.1 MB (69071980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da628efce8017c66e99857470108bed6d1fd4afdf8380fb8e5247ecddb6ce466`  
		Last Modified: Tue, 10 Oct 2023 19:35:50 GMT  
		Size: 52.0 KB (51981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ecb49129705560af62bd53ad4be2e4e4151a8a3d77978c3aaeb063fc0ccb14`  
		Last Modified: Tue, 10 Oct 2023 19:35:50 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
