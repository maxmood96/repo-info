## `mongo:nanoserver-1809`

```console
$ docker pull mongo@sha256:5ef1e393f45ab96306ddb677fd7b11ac2a3d1ad2f89244666af1081ba893285d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `mongo:nanoserver-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull mongo@sha256:d312d180f121c0d762fd87af133363df74e713c7d8eec39634833e42fada1719
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.5 MB (715463655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b427e1d160faf1ecb0526bb437bfcdb3aed70494425996fb2fb8be261c746399`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 02 Aug 2023 08:33:47 GMT
RUN Apply image 10.0.17763.4737
# Thu, 10 Aug 2023 00:48:08 GMT
SHELL [cmd /S /C]
# Thu, 10 Aug 2023 01:15:48 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 01:15:57 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 10 Aug 2023 01:15:57 GMT
USER ContainerUser
# Thu, 10 Aug 2023 01:15:58 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Thu, 17 Aug 2023 20:23:40 GMT
ENV MONGO_VERSION=7.0.0
# Thu, 17 Aug 2023 20:24:30 GMT
COPY dir:52c2b0def258ae637a0b5523eab235ea2346de3e4d510b59414991e5921a2c6f in C:\mongodb 
# Thu, 17 Aug 2023 20:24:49 GMT
RUN mongod --version
# Thu, 17 Aug 2023 20:24:49 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 17 Aug 2023 20:24:50 GMT
EXPOSE 27017
# Thu, 17 Aug 2023 20:24:51 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:86fab75eb466cadf89d853682179b3b57eba9fe28c78041dd52bced81e18a627`  
		Last Modified: Tue, 08 Aug 2023 17:55:54 GMT  
		Size: 104.5 MB (104459386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298e0f667b1d8252956bc07b8438d68801dd9eb4ebb7ad345fde0bed30609680`  
		Last Modified: Thu, 10 Aug 2023 01:03:59 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814fa0d01fded994ad965ae5487dc312820ecd968291d0bb20ee608f702a9689`  
		Last Modified: Thu, 10 Aug 2023 02:00:40 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021e83a508dc7adbef323d416f3a04d3d4889d441750fa4ecf3ed425ee2e1f0`  
		Last Modified: Thu, 10 Aug 2023 02:00:39 GMT  
		Size: 69.2 KB (69188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956b7c3ad022ed0da478f25e9b64d0c5ac7947ac14c611b3d359ef414b7abf35`  
		Last Modified: Thu, 10 Aug 2023 02:00:38 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf6796c7b91221863b1920e4991f4a08153b38f271641d2b9cd3ab35640e935`  
		Last Modified: Thu, 10 Aug 2023 02:00:38 GMT  
		Size: 267.2 KB (267155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48a6cb4cdc9d90288494febc5de4dc08b3d4d39c232028f28291b5d83eb3d59`  
		Last Modified: Thu, 17 Aug 2023 20:33:38 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199b1fa264149a41db4b9d4377804a62ff23e3fc670d89a8f05c0c49e07e20ab`  
		Last Modified: Thu, 17 Aug 2023 20:35:09 GMT  
		Size: 610.6 MB (610582062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89806b75892fb47d9f818283997f82a318ee59a5512b5eb0a64af1089eff164`  
		Last Modified: Thu, 17 Aug 2023 20:33:36 GMT  
		Size: 77.7 KB (77719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec73148fd3ada4934e5406e895117c903a7ada616f4443863fca8fb38771d64a`  
		Last Modified: Thu, 17 Aug 2023 20:33:36 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee92c8b63dc0c443be3c669c2a0875d61d30a78ed37d75f2ef50c5d606dd98b7`  
		Last Modified: Thu, 17 Aug 2023 20:33:36 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31e8bdc092a95b8227643e0290a9e3eb5cdd2e08cfa0772b940d57c645012c5`  
		Last Modified: Thu, 17 Aug 2023 20:33:36 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
