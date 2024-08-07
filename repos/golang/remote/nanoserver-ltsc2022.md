## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:fc13c7a4a9352dc719a90a8f77ce90e6ebcb80356921f2462008aa9625386566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull golang@sha256:01278f29ee2a7f36313d38114409a9f2019a885da87b397f69c4570988c4fc9c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192012821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6b35b362b0389d8d13460e634e949fc197cf26f796c3808953fae4214b3559`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Tue, 06 Aug 2024 23:58:43 GMT
SHELL [cmd /S /C]
# Tue, 06 Aug 2024 23:58:44 GMT
ENV GOPATH=C:\go
# Tue, 06 Aug 2024 23:58:44 GMT
USER ContainerAdministrator
# Tue, 06 Aug 2024 23:58:49 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 06 Aug 2024 23:58:50 GMT
USER ContainerUser
# Tue, 06 Aug 2024 23:58:51 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 23:59:59 GMT
COPY dir:bdd617378b73a2613b1de19da8dc0bcf601e92f64d55ab6d89960978f470f279 in C:\Program Files\Go 
# Wed, 07 Aug 2024 00:00:02 GMT
RUN go version
# Wed, 07 Aug 2024 00:00:03 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:652774a5d82a114642848f8b0b8d486ec1b4995f9dda56e36fe4ac7563429990`  
		Last Modified: Tue, 09 Jul 2024 20:33:26 GMT  
		Size: 120.5 MB (120490378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053e8d88c0a9ed26afe09094aed3a2fe417d2792d3490f59cad4082f59e7cb9b`  
		Last Modified: Wed, 07 Aug 2024 00:00:14 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c6f3c54458928fa016c9a8ff9f9267ec214323cd5e9ef97e015646a2c42388`  
		Last Modified: Wed, 07 Aug 2024 00:00:15 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbeb0dd893a8af639b857a843fbd98e5b313a1e5fff86cf1abc862e13e68e0c`  
		Last Modified: Wed, 07 Aug 2024 00:00:14 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c2cb3968f60fc8ba1efea29779fa8342a8f04057afad6148d1eb954b38ce40`  
		Last Modified: Wed, 07 Aug 2024 00:00:14 GMT  
		Size: 73.8 KB (73808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b655ac09bc1ca80659115d4a03bbf5bf76e427f5ee189a0c06f5857e733d3b6c`  
		Last Modified: Wed, 07 Aug 2024 00:00:12 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d295d2be4dcde0f2cb59827221109b1976081f8481863f694fea3f6be56c1f4`  
		Last Modified: Wed, 07 Aug 2024 00:00:12 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2504ee006aaf5746db24b1bd4fae954e1f92df129c08e1745949cb451e06054`  
		Last Modified: Wed, 07 Aug 2024 00:00:22 GMT  
		Size: 71.4 MB (71362449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84648f6b5c78ba90ea431d71c32e84827a040ddb96675c04a2231958e2cf0af7`  
		Last Modified: Wed, 07 Aug 2024 00:00:12 GMT  
		Size: 79.8 KB (79783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b08b09a85099fd49624dc6c60751ac714758e9f295dfde826533a32689bf27`  
		Last Modified: Wed, 07 Aug 2024 00:00:12 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
