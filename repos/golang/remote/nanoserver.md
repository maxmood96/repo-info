## `golang:nanoserver`

```console
$ docker pull golang@sha256:fed13aba2a48b23f4051030d5fa9d8ad9c49218c4a5d923db8974a367117ffbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `golang:nanoserver` - windows version 10.0.20348.2582; amd64

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

### `golang:nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull golang@sha256:3181c04c222339cb6d2525cd05dab464559b476eb4e7219eddc4a79a4c127d2d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226584044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f1ba2925688a4b8690f9df86ebd39940d799beaccf3b7eaf00c0821f4af022`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Tue, 06 Aug 2024 23:58:36 GMT
SHELL [cmd /S /C]
# Tue, 06 Aug 2024 23:58:37 GMT
ENV GOPATH=C:\go
# Tue, 06 Aug 2024 23:58:37 GMT
USER ContainerAdministrator
# Tue, 06 Aug 2024 23:58:41 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 06 Aug 2024 23:58:42 GMT
USER ContainerUser
# Tue, 06 Aug 2024 23:58:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 23:59:48 GMT
COPY dir:bdd617378b73a2613b1de19da8dc0bcf601e92f64d55ab6d89960978f470f279 in C:\Program Files\Go 
# Tue, 06 Aug 2024 23:59:51 GMT
RUN go version
# Tue, 06 Aug 2024 23:59:52 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c211f6473d9da5ddfb5337dd4b3ddbe37e1c17d0c4ff817bf3d42fb8cc99bc`  
		Last Modified: Tue, 06 Aug 2024 23:59:58 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94d98bdaf6faa349ed3d02d8cc2d788bb72471349309ea04568f5b582314057`  
		Last Modified: Tue, 06 Aug 2024 23:59:58 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bdc5986754efaf7703624906b6d419986bd5b7f68977413f73d6bdc1075acc`  
		Last Modified: Tue, 06 Aug 2024 23:59:58 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369440aaaed007d0864e864d7a038c890655b03b4967afeae59f67b6c48a37ef`  
		Last Modified: Tue, 06 Aug 2024 23:59:59 GMT  
		Size: 68.2 KB (68179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bf1d947e093cbd6861a70df06f5f4e4c86c37bc230db7e24bf8c566b828203`  
		Last Modified: Tue, 06 Aug 2024 23:59:56 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765cbb3822f95530b1370983f0d0a95cd5bb94f8d222d1cc05d33d480090fe2d`  
		Last Modified: Tue, 06 Aug 2024 23:59:56 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a7ea1345767639c88aa087b71016be1a1ecab3edf07df97064685c0798276f`  
		Last Modified: Wed, 07 Aug 2024 00:00:11 GMT  
		Size: 71.4 MB (71361020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3e877d1a3106a65a6178ce5d88fcd786e7e30c5864b54659425627279435ff`  
		Last Modified: Tue, 06 Aug 2024 23:59:56 GMT  
		Size: 67.0 KB (66987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb0e1a884a9e7f949ba13a618ea17704902216c13fcd4b852bf904dc13f049b`  
		Last Modified: Tue, 06 Aug 2024 23:59:57 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
