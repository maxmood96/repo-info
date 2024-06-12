## `mongo:5-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:dabbf5eb754f311c360b2999be826b1df85d3c88acef460223ea38f59be48d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2527; amd64

### `mongo:5-nanoserver-ltsc2022` - windows version 10.0.20348.2527; amd64

```console
$ docker pull mongo@sha256:26fe2c2c670a9bcfa09a6febe5c40d49f47a35f2eb496000d331af8ebe387423
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.4 MB (432378144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b79c940bc2de880e6325aebcf20ed37588ce58a20cbbbe6a4b1b31476b6c157`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Jun 2024 08:41:16 GMT
RUN Apply image 10.0.20348.2527
# Wed, 12 Jun 2024 19:02:27 GMT
SHELL [cmd /S /C]
# Wed, 12 Jun 2024 19:02:28 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 19:02:32 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 12 Jun 2024 19:02:33 GMT
USER ContainerUser
# Wed, 12 Jun 2024 19:02:35 GMT
COPY multi:c5f0fbe231f542d852dcd0a8e1790eb7694672a9238df11d11d4dd7ca117b6a8 in C:\Windows\System32\ 
# Wed, 12 Jun 2024 19:02:36 GMT
ENV MONGO_VERSION=5.0.27
# Wed, 12 Jun 2024 19:02:55 GMT
COPY dir:a6cc57be35b0b4e87dfd208aad2e6306c874b8418531c7b4d2f073d45bf72812 in C:\mongodb 
# Wed, 12 Jun 2024 19:03:03 GMT
RUN mongo --version && mongod --version
# Wed, 12 Jun 2024 19:03:04 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Jun 2024 19:03:05 GMT
EXPOSE 27017
# Wed, 12 Jun 2024 19:03:07 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:f9825bcd6f9509654677a23b5fa1d32b32e1e32ff51914ebfaa76d5e79c22b50`  
		Last Modified: Wed, 12 Jun 2024 02:27:19 GMT  
		Size: 120.5 MB (120488969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060d2ac4a6dc867e7cad265da26f50e35afbc6daf7b523bb8f726fa2c7f05ee8`  
		Last Modified: Wed, 12 Jun 2024 19:03:16 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fd3aa36dcafa91a133198d9a03db84a8dea43ea48ccaec7e182468c9032553`  
		Last Modified: Wed, 12 Jun 2024 19:03:16 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f06449ec694a88c8f7128c25f7cc1b818e325380a2a042f2a607438e2e0557`  
		Last Modified: Wed, 12 Jun 2024 19:03:15 GMT  
		Size: 78.9 KB (78854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb199a7c6888db90dda31dbef9f4383689aef6c3a1ecc9ebe41000034946aa2`  
		Last Modified: Wed, 12 Jun 2024 19:03:14 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9368b648255e4e5b889ec7ef51c2c7a2537a08eaec50c218711ad5a1bcea1f55`  
		Last Modified: Wed, 12 Jun 2024 19:03:14 GMT  
		Size: 267.4 KB (267447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4777087025f758746607a6fce4beac6b94a8734850b2d5b2b8c38ba4578b960c`  
		Last Modified: Wed, 12 Jun 2024 19:03:14 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8a61cec1f28b9c658e8259a93460b693407860690f330ba01e2de01e9d6e35`  
		Last Modified: Wed, 12 Jun 2024 19:03:42 GMT  
		Size: 311.5 MB (311452685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23da42cc6e2943a0ac942815b23c77e951c726e9d73ce5ec575608f67a745403`  
		Last Modified: Wed, 12 Jun 2024 19:03:12 GMT  
		Size: 82.9 KB (82929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0cddae3720e10f8a0a298a38e0a877910aa08e4a8a9b90507db3eb84412d94`  
		Last Modified: Wed, 12 Jun 2024 19:03:12 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f29061445dfe9de70dcc8e7ebbf3e1112181c85a83c7835874e50d2aab1636`  
		Last Modified: Wed, 12 Jun 2024 19:03:12 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1981a8caba350ed858d4947d28f0b450976e74c1cf033b6c0848db50b2ec49ff`  
		Last Modified: Wed, 12 Jun 2024 19:03:12 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
