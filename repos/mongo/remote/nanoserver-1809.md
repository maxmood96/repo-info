## `mongo:nanoserver-1809`

```console
$ docker pull mongo@sha256:1ac504f687e4cd40371a6c2c5baf62e6fb7df138e2f319faba3af051db06691b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `mongo:nanoserver-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull mongo@sha256:d816f67dba7af7f822a1759cecc4f97f3933e22983b07756c757c374203ded23
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.9 MB (612864085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3a18f611416f3b9561cd0f7ec0bf91925b64c1487b33e2db30731444399d3d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 13:04:30 GMT
SHELL [cmd /S /C]
# Wed, 10 Aug 2022 18:22:41 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 18:22:55 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 10 Aug 2022 18:22:56 GMT
USER ContainerUser
# Wed, 24 Aug 2022 22:27:55 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Wed, 24 Aug 2022 22:27:57 GMT
ENV MONGO_VERSION=6.0.1
# Wed, 24 Aug 2022 22:28:45 GMT
COPY dir:9bc3bf7ac427acc5da2a94db90fd2f879ea935b4a3cfd676cbd1fb49e16c8f3c in C:\mongodb 
# Wed, 24 Aug 2022 22:29:01 GMT
RUN mongod --version
# Wed, 24 Aug 2022 22:29:03 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 24 Aug 2022 22:29:05 GMT
EXPOSE 27017
# Wed, 24 Aug 2022 22:29:07 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9982991b820814ad737b2a161e973194e66b8d7b0a9890bee49cd158d7e77dec`  
		Last Modified: Wed, 10 Aug 2022 13:27:27 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7180e2213de155098394f0dbf886f68478c49bc5ef2c0977d6e28da9593090df`  
		Last Modified: Wed, 10 Aug 2022 18:55:17 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0b5eb91e7b8da02b963c0e45697ecd1e88fdea8a134974bf17366b2dc3a68e`  
		Last Modified: Wed, 10 Aug 2022 18:55:15 GMT  
		Size: 77.8 KB (77802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c59fe6b6f7e47222898a3f00c7f02b87dcb9f4480cf874d6f00b55cbcede826`  
		Last Modified: Wed, 10 Aug 2022 18:55:14 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c449d540f8ba413c721750688e7af7832423419eb90d4fa1448b22adb02d76a`  
		Last Modified: Wed, 24 Aug 2022 22:55:10 GMT  
		Size: 267.2 KB (267226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7994b921415fcdb162f73fcd6a32f37b2b28bdbffa21a848f7c484b59aa74014`  
		Last Modified: Wed, 24 Aug 2022 22:55:10 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de98ef741eaee7a83f088d85ddf8d2b47d43f8c0b90b54deed4488627139a86`  
		Last Modified: Wed, 24 Aug 2022 22:56:29 GMT  
		Size: 509.2 MB (509224359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0044d7c45d1c340be2a2010875e85990e4b84726423e9665fdd90e278912647a`  
		Last Modified: Wed, 24 Aug 2022 22:55:07 GMT  
		Size: 82.4 KB (82423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957a1db6405e02f7fa59fad1a80834aa0ac28d8bee08e3cea9c16ef8074648c9`  
		Last Modified: Wed, 24 Aug 2022 22:55:07 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84e2f3d9e0ecc2be8a1cd6a14efbca393eb6b00cda34c80f2fddfcaf009bb3b`  
		Last Modified: Wed, 24 Aug 2022 22:55:07 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2c240eb4e3001203222cac4718d161789de55cb4398c967741ac0a4792a413`  
		Last Modified: Wed, 24 Aug 2022 22:55:08 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
