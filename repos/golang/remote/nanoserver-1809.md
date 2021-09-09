## `golang:nanoserver-1809`

```console
$ docker pull golang@sha256:1677ffbff47d29ff69121a6d55dca0ea7673bb3db935f12d7d3517685d36f320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `golang:nanoserver-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull golang@sha256:df37ab93b1563df079605ad4ea0e8c42f6f3c8d24e008e90ef6f6c848f1f430b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 MB (247940472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460bdc288603af3f3311df8ee7a8c66a25f5afd9c8da4e4b8074953f867d7566`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 05 Aug 2021 19:15:20 GMT
RUN Apply image 1809-amd64
# Wed, 25 Aug 2021 13:22:41 GMT
SHELL [cmd /S /C]
# Wed, 25 Aug 2021 13:22:41 GMT
ENV GOPATH=C:\go
# Wed, 25 Aug 2021 13:22:42 GMT
USER ContainerAdministrator
# Wed, 25 Aug 2021 13:23:22 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 25 Aug 2021 13:23:23 GMT
USER ContainerUser
# Thu, 09 Sep 2021 21:29:12 GMT
ENV GOLANG_VERSION=1.17.1
# Thu, 09 Sep 2021 21:31:37 GMT
COPY dir:96b2db49684f355600a0eba9c6bf46049724e901f0e48267d1df305ef566f9f1 in C:\Program Files\Go 
# Thu, 09 Sep 2021 21:32:22 GMT
RUN go version
# Thu, 09 Sep 2021 21:32:23 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:bc8517709e9cfff223cb034ff5be8fcbfa5409de286cdac9ae1b8878ebea6b84`  
		Size: 102.7 MB (102741177 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:72633ba98485460151f22e8084221e58c46cf1423b1ae99cf70a91bcd409a2dc`  
		Last Modified: Wed, 25 Aug 2021 13:40:36 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc1785bd046b44f66be3015e99d1614dfb3fbea263af87621af6c6fc1b96f34`  
		Last Modified: Wed, 25 Aug 2021 13:40:36 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a258bd0b66f48ebdb249f95a06ec1e526732f04152f28f6c37461e9b4bc51454`  
		Last Modified: Wed, 25 Aug 2021 13:40:36 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94199995894240f334fa8f377f3cbb662ba200bf9e5118935fddb142c4281fde`  
		Last Modified: Wed, 25 Aug 2021 13:40:36 GMT  
		Size: 69.4 KB (69419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508d30dddb17b20007581400c3f93b7e660737cd97fbe5d1ffd899a12da06b06`  
		Last Modified: Wed, 25 Aug 2021 13:40:34 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9d0a03b3d0b6384ba1fd8d89dc64f5d621a448a5aa380328dc1571e67fdf47`  
		Last Modified: Thu, 09 Sep 2021 21:52:44 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2232b97e4f5e29a4291c444401408dce6c9613ad016c5cc6e1f081b09510a7`  
		Last Modified: Thu, 09 Sep 2021 21:53:20 GMT  
		Size: 145.0 MB (145049854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a91671592fabd51b33be292fb81b906639b1833dfe5d8de588582d7cf8ca72b`  
		Last Modified: Thu, 09 Sep 2021 21:52:44 GMT  
		Size: 72.9 KB (72894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb49476dbfe18afca3b120047781d9f1c620d58366413044906977904722712`  
		Last Modified: Thu, 09 Sep 2021 21:52:44 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
