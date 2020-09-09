## `golang:nanoserver-1809`

```console
$ docker pull golang@sha256:d8c5d9a8ef08bacba2b040d85aef5a1cc0bb1e1c4e98f11e072bb70fa4231826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `golang:nanoserver-1809` - windows version 10.0.17763.1457; amd64

```console
$ docker pull golang@sha256:f52e540ed544f42122bad53eede7263ccd328e70a8c63769ce7a245a53e00ab4
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235270358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9386b83f02802cd6af94b2061515997ead9a0336ae4ba553344b71c09fc4a49a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 02 Sep 2020 12:08:18 GMT
RUN Apply image 1809-amd64
# Wed, 09 Sep 2020 12:25:43 GMT
SHELL [cmd /S /C]
# Wed, 09 Sep 2020 12:25:43 GMT
ENV GOPATH=C:\gopath
# Wed, 09 Sep 2020 12:25:44 GMT
USER ContainerAdministrator
# Wed, 09 Sep 2020 12:25:58 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\go\bin;%PATH%"
# Wed, 09 Sep 2020 12:25:59 GMT
USER ContainerUser
# Wed, 09 Sep 2020 12:25:59 GMT
ENV GOLANG_VERSION=1.15.1
# Wed, 09 Sep 2020 12:28:10 GMT
COPY dir:670e359cfc47c3086f7be2274dac61c6e323dc7365e926c707fa3a42e92c5d24 in C:\go 
# Wed, 09 Sep 2020 12:28:24 GMT
RUN go version
# Wed, 09 Sep 2020 12:28:24 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:ecf9bb62dc6eedea9fd367628f8715dea75b7d2053afa4b5121e7809aa692139`  
		Size: 101.2 MB (101239122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25f13e08d7a0e3b2b29d1fb7e68650856359fb6b1d9c4483355792f74eaf5d86`  
		Last Modified: Wed, 09 Sep 2020 13:10:56 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9345b592b700f53a9f967f8b587b68e9f98e06b8f2f4167efcbde55c32aa15e`  
		Last Modified: Wed, 09 Sep 2020 13:10:56 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e436ea9c720124551c1604eba40293baa8f824446a509c97eee817155660c704`  
		Last Modified: Wed, 09 Sep 2020 13:10:55 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096203a5fb8f8c94dba3f84977f78311294d06aaab1cf538e7ea43047824ecd0`  
		Last Modified: Wed, 09 Sep 2020 13:10:55 GMT  
		Size: 64.4 KB (64375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860da1581fa820b6de88c5b8df6f48418484de94171e9751c536b20718bd49a4`  
		Last Modified: Wed, 09 Sep 2020 13:10:53 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad54724e7057d76fcb998ec9b814ee234d8e0788fbc96a43be8ebc86218ab10`  
		Last Modified: Wed, 09 Sep 2020 13:10:53 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f399b0166b1a175430b968a888790bade2c2e9eed67777e698d0606b85031e`  
		Last Modified: Wed, 09 Sep 2020 13:11:19 GMT  
		Size: 133.9 MB (133887518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2e4790243d21186a14512a3becd0ddcbd6520e1f8946097c54fcd429336ea5`  
		Last Modified: Wed, 09 Sep 2020 13:10:53 GMT  
		Size: 73.8 KB (73845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ee4f70b96dd8f39b76404d03744fb5433f876f12425cc820208f16cece4abc`  
		Last Modified: Wed, 09 Sep 2020 13:10:53 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
