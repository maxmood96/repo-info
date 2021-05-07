## `golang:nanoserver-1809`

```console
$ docker pull golang@sha256:e325ef7e16e046f2f5515b6d779e37b3d2265634a5a567ea55b4234a3aa44fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `golang:nanoserver-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull golang@sha256:dff26202962f2d62a1bf3ef78f42222e0aea8237e396683429edebf9dcea3290
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240510603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d076d5b24dcdc95394d987c736805ef750f40043b7f5cac7d62171245d06d8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 12:43:35 GMT
SHELL [cmd /S /C]
# Wed, 14 Apr 2021 12:43:36 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:43:37 GMT
USER ContainerAdministrator
# Wed, 14 Apr 2021 12:44:20 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\go\bin;%PATH%"
# Wed, 14 Apr 2021 12:44:21 GMT
USER ContainerUser
# Thu, 06 May 2021 20:22:47 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 20:24:38 GMT
COPY dir:6c3ff7dce6486232be50a1fa044a7ec0b9d549cc211de30b53d1656eb8f7f197 in C:\go 
# Thu, 06 May 2021 20:24:59 GMT
RUN go version
# Thu, 06 May 2021 20:25:00 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:be6876a5c8fd442b68d04a6a7e144db66f22e7c7aba22b514442a31e0f83c50e`  
		Last Modified: Wed, 14 Apr 2021 13:02:13 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2077d5bc588bdc2938e30cfb02f3928dd2ccd386a44bcf2b6531d858fe1dd2`  
		Last Modified: Wed, 14 Apr 2021 13:02:12 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c020c23ff9ec520045bfa017d66096a8a5358a99779da558caf7e7f070a7de`  
		Last Modified: Wed, 14 Apr 2021 13:02:12 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7d9a60f17fee47fbd5aa1e0b8f6d9e96f2bf0b1eb3bd2742a7b73f0fb88a75`  
		Last Modified: Wed, 14 Apr 2021 13:02:12 GMT  
		Size: 66.6 KB (66580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68b9bedd117801b679f126ab1a3f4c6e345b067246680ca5e36b693e5c14ba7`  
		Last Modified: Wed, 14 Apr 2021 13:02:10 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37299232d45d91468f59b21ffc81e7d64a16cd9896c1087b1e81d9790cfa7618`  
		Last Modified: Thu, 06 May 2021 20:36:26 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d946968ba5cddba1c523ac2eed90f65bf1a18dee3f3092466f102a8289b20bb`  
		Last Modified: Thu, 06 May 2021 20:36:55 GMT  
		Size: 139.0 MB (139015964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf512f6be3b0bf77f9351f56f1c8b276a965ff6af6122d99f194a1744073c4c`  
		Last Modified: Thu, 06 May 2021 20:36:26 GMT  
		Size: 80.9 KB (80869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223e8f585430c6a9de536771c577946c115b998664723fc31ce1554c455b3aa7`  
		Last Modified: Thu, 06 May 2021 20:36:25 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
