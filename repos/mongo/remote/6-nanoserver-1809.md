## `mongo:6-nanoserver-1809`

```console
$ docker pull mongo@sha256:ba4d9d64ef0f0d31ad405191621a9182f11f2276614bb0a0640b0dc904e89a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `mongo:6-nanoserver-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull mongo@sha256:7c54a39271c2966921043314bced2e73980ca3b0c4155eaa0c6636fd7114baa4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.1 MB (619064224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e4d41080a693bc313ae7c5a2ee3336f83f9f32ff79baa3cf4c061ffeb050e1`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 07 Jan 2023 05:17:01 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 03:12:03 GMT
SHELL [cmd /S /C]
# Thu, 12 Jan 2023 04:10:28 GMT
USER ContainerAdministrator
# Thu, 12 Jan 2023 04:11:03 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 12 Jan 2023 04:11:04 GMT
USER ContainerUser
# Thu, 12 Jan 2023 04:11:05 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Thu, 12 Jan 2023 04:11:06 GMT
ENV MONGO_VERSION=6.0.3
# Thu, 12 Jan 2023 04:12:03 GMT
COPY dir:504ba3c422010154364f85a9b7f5ebcd0252fe3e628d277d138a4248175996a9 in C:\mongodb 
# Thu, 12 Jan 2023 04:12:43 GMT
RUN mongod --version
# Thu, 12 Jan 2023 04:12:43 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 12 Jan 2023 04:12:44 GMT
EXPOSE 27017
# Thu, 12 Jan 2023 04:12:45 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:e58f9ad3b15a2a4882ab0a845e8e619cc8c3c411ddbe8b50046c1618a95c1397`  
		Last Modified: Thu, 12 Jan 2023 02:40:44 GMT  
		Size: 106.7 MB (106666138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070163efc0c5001bb289dc56cc98506d4d920f7b1eecdd95fad44822625d1509`  
		Last Modified: Thu, 12 Jan 2023 03:50:00 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa79cc8c7933e5e2801bd7e32cf2ec15c495d4c084f894cb6e620f4d72d9f4f`  
		Last Modified: Thu, 12 Jan 2023 04:42:54 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831ebdd21f8d72263638b121334b6d0d7d2e3146b2630be9aae72ca6b56ed0d6`  
		Last Modified: Thu, 12 Jan 2023 04:42:52 GMT  
		Size: 74.6 KB (74603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e649ad9f4edadb284416c870eae927ee2bec76ccaae77676c2541797eb3c8e`  
		Last Modified: Thu, 12 Jan 2023 04:42:52 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e578eeb9dbd53ee94e479a46caa6405215092c071b11118c64468678debe66`  
		Last Modified: Thu, 12 Jan 2023 04:42:52 GMT  
		Size: 267.2 KB (267193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9de9f8306a2dff2c1ba49904189b69a071efdc43ff3f8de2f8698e182170b8`  
		Last Modified: Thu, 12 Jan 2023 04:42:52 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b9440b44824804581584394508a5f3121aa42f3310e2c5dedeff8cfe81dad2`  
		Last Modified: Thu, 12 Jan 2023 04:44:24 GMT  
		Size: 512.0 MB (511967857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc3accc58ff9d9a2a753aaee1cf17d12a3a29bafa754057ae6192535dc11b81`  
		Last Modified: Thu, 12 Jan 2023 04:42:50 GMT  
		Size: 80.4 KB (80393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fa29c7dd876f72802b0b27fd74bd342f1040e75b4743e08412d909c18a390f`  
		Last Modified: Thu, 12 Jan 2023 04:42:50 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de11d8135fec0aa7b376174d79e5161ec45e8b1f7466ac3e4f03426c792ac74`  
		Last Modified: Thu, 12 Jan 2023 04:42:50 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4da8d85c126836a562eddd2d059b7c6f79bfcaab398e9299c400ca3324d1af`  
		Last Modified: Thu, 12 Jan 2023 04:42:50 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
