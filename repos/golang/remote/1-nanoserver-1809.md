## `golang:1-nanoserver-1809`

```console
$ docker pull golang@sha256:d1f5b160fbac5e0ae31dfa3336419bba54cc765ab8a7a28099704a42384ba7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `golang:1-nanoserver-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull golang@sha256:4f372d942e524ae4311696899d21aeaf1c7fff44c9a786350a92fe6990027dbd
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235047267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12ea16be8c6737f28edc4d6086de05a90e94424365317f109f86e823d89e474`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 13:41:58 GMT
SHELL [cmd /S /C]
# Wed, 09 Dec 2020 13:41:58 GMT
ENV GOPATH=C:\gopath
# Wed, 09 Dec 2020 13:41:59 GMT
USER ContainerAdministrator
# Wed, 09 Dec 2020 13:42:15 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\go\bin;%PATH%"
# Wed, 09 Dec 2020 13:42:15 GMT
USER ContainerUser
# Wed, 09 Dec 2020 13:42:16 GMT
ENV GOLANG_VERSION=1.15.6
# Wed, 09 Dec 2020 13:44:13 GMT
COPY dir:4d3209dd6dc0a28e201f1dba6a02512d8e7c8ebc13640177c71b45b1bb90fef7 in C:\go 
# Wed, 09 Dec 2020 13:44:28 GMT
RUN go version
# Wed, 09 Dec 2020 13:44:29 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ef62a6c873d742d2352d72aa47cbe24e03af8176a7a65e82afc21e7ce96268ea`  
		Last Modified: Wed, 09 Dec 2020 13:56:30 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4205eb72db05f020d79acbdc856520ee378829d913710e9515a412b6989e1b2`  
		Last Modified: Wed, 09 Dec 2020 13:56:29 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b7945a0e13b94f56a6a71a712e89439fbcd9d0c261d03dec9f6acb55654b0`  
		Last Modified: Wed, 09 Dec 2020 13:56:28 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f1bd520f12866b93e98eccb99b343aecc0e009c059872eae2dfb46899519d4`  
		Last Modified: Wed, 09 Dec 2020 13:56:29 GMT  
		Size: 64.3 KB (64336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44b7628f5b5064fb21e8bcb843efa4aa8db9073a95e47098b17b3b32ed95e0c`  
		Last Modified: Wed, 09 Dec 2020 13:56:26 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3e347eeefce092f30bda0cb9f1734829fc27dca20359a9dc235fbaa8c4f347`  
		Last Modified: Wed, 09 Dec 2020 13:56:26 GMT  
		Size: 884.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea742b07d02307e1905f6216fc7a05a5f35cdf5b934036f1791713cd778c7607`  
		Last Modified: Wed, 09 Dec 2020 13:56:54 GMT  
		Size: 133.6 MB (133641250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce9690ad6522a18e8d00b22563e0af612c189ae559f59a480fb961997f70b0b`  
		Last Modified: Wed, 09 Dec 2020 13:56:26 GMT  
		Size: 71.4 KB (71447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4e844fae4af91e4a3e43f452814ba043429976d318f814c060f072ac3a1270`  
		Last Modified: Wed, 09 Dec 2020 13:56:26 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
