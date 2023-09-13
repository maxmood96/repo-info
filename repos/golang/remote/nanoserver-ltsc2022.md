## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:444ee0385132b293f370cb079b655c82af3f535ab3119c0bf2a1f7889c8349a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1970; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.1970; amd64

```console
$ docker pull golang@sha256:253adb1d4f5834aa880af3fde3b4d4b3e75039afa9ac7af382ab97b73dd3b321
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.8 MB (189773678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0e041e170d752aab0ebebd6a53e7f1284383a6b44f8f37f7172d456b1f4474`
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
# Wed, 13 Sep 2023 01:45:31 GMT
ENV GOLANG_VERSION=1.21.1
# Wed, 13 Sep 2023 01:47:27 GMT
COPY dir:be682b819fc6157c5849876d4d281ecc9c26fd804e58407c442594a19c48910f in C:\Program Files\Go 
# Wed, 13 Sep 2023 01:47:48 GMT
RUN go version
# Wed, 13 Sep 2023 01:47:49 GMT
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
	-	`sha256:e3bb04f7817d1ddc6dc09af8bcc3fbe2c3f9140ceb4ca0a5e6f32b598dba143a`  
		Last Modified: Wed, 13 Sep 2023 02:18:05 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94149b2e36ddd8d71f890c3ba166c9c2acc6b525b6262f0ba0927200bef04ee`  
		Last Modified: Wed, 13 Sep 2023 02:18:30 GMT  
		Size: 69.1 MB (69065548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a493bb5868f6736575b12e30a877e646b3c98170ea99f72c851687b3f937c8a4`  
		Last Modified: Wed, 13 Sep 2023 02:18:05 GMT  
		Size: 52.4 KB (52443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728dba616efa80715b71d75121489b9d58415e1273e975cc8d859b6a456431f9`  
		Last Modified: Wed, 13 Sep 2023 02:18:05 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
