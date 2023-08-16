## `mongo:nanoserver`

```console
$ docker pull mongo@sha256:454af10e9a2274e32571164f373c0fc6e10d8b11c6cfe5edaddfe11c6799f44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1906; amd64
	-	windows version 10.0.17763.4737; amd64

### `mongo:nanoserver` - windows version 10.0.20348.1906; amd64

```console
$ docker pull mongo@sha256:24e9ac3c8c00aebe555983d41341fe98d978a1481073352135dd2f2b5334e2d9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.2 MB (638226148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f236bb57f0e3d913927a19019858131bb94f2ddd48fcf2fbba32d84a511a1f9`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 03 Aug 2023 09:40:19 GMT
RUN Apply image 10.0.20348.1906
# Thu, 10 Aug 2023 00:45:25 GMT
SHELL [cmd /S /C]
# Thu, 10 Aug 2023 01:14:21 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 01:14:29 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 10 Aug 2023 01:14:30 GMT
USER ContainerUser
# Thu, 10 Aug 2023 01:14:31 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Tue, 15 Aug 2023 23:20:04 GMT
ENV MONGO_VERSION=6.0.9
# Tue, 15 Aug 2023 23:20:40 GMT
COPY dir:a12ac6ea695bc7285b3454c2236744267f0c36ac9ece5b695f0b6536580cab18 in C:\mongodb 
# Tue, 15 Aug 2023 23:20:59 GMT
RUN mongod --version
# Tue, 15 Aug 2023 23:21:00 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 15 Aug 2023 23:21:01 GMT
EXPOSE 27017
# Tue, 15 Aug 2023 23:21:01 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:ea9613880997b3ab2284a37c0c14a403553457b0c331b41c6bd6d1cc7838a222`  
		Last Modified: Tue, 08 Aug 2023 18:47:21 GMT  
		Size: 120.5 MB (120500677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a528e77cf0bef98e15c3b4194ee340960485498ac4c1bdcbab44307858ecfc4`  
		Last Modified: Thu, 10 Aug 2023 01:03:26 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0247382dbd5864284425d3942427091871bf5f10629f0608efbc6b3303d067`  
		Last Modified: Thu, 10 Aug 2023 01:59:00 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ffaf70bb154004aa4faefa8b8926380d11a591157ac5074e2438ce1696d3ac`  
		Last Modified: Thu, 10 Aug 2023 01:58:58 GMT  
		Size: 77.9 KB (77932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54933f30fc7826d81c7a7731e98cb5ea37dd377d70a605f59fda57f3a196506c`  
		Last Modified: Thu, 10 Aug 2023 01:58:58 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa6daf2a597ffb630f230ca7808bb850f20a800b5ffaf16207e74b4405ba9ff`  
		Last Modified: Thu, 10 Aug 2023 01:58:58 GMT  
		Size: 267.2 KB (267199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4973e2aa3eba3debf9538d9950bd4057204197489424aafcc0ba8e50f3cc0236`  
		Last Modified: Tue, 15 Aug 2023 23:32:54 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d169896013c87fbc31535f4622ceeb16fae361059b8676ca6f56afda47e709`  
		Last Modified: Tue, 15 Aug 2023 23:34:02 GMT  
		Size: 517.3 MB (517319515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f5ab12dd9920822d0a6f0a4e277442298de61def0edcab6938a39aa46135e5`  
		Last Modified: Tue, 15 Aug 2023 23:32:52 GMT  
		Size: 52.7 KB (52715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46721ae0054151dcf38225c696b56c0230684ad912dfe39feb9823f7e3c73803`  
		Last Modified: Tue, 15 Aug 2023 23:32:52 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fafb9ff6adec99dd0d78f7a886cca40ea0a8cf828267ac28e7bf42e00bd852d6`  
		Last Modified: Tue, 15 Aug 2023 23:32:52 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6972ce609fa0472f9d270a2088f87682c925f39f108ccd3f2cf13c0256d1fdb`  
		Last Modified: Tue, 15 Aug 2023 23:32:52 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:nanoserver` - windows version 10.0.17763.4737; amd64

```console
$ docker pull mongo@sha256:9f585e127130be631f57e6eab6ae4ec06e040f2f1982c23cf8ad190eeba2853d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.2 MB (622199327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3af116d1c7b35e7566b84bbcae23bff9d2d58e29fc7db52ed1b5d9a589603f1`
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
# Tue, 15 Aug 2023 23:21:18 GMT
ENV MONGO_VERSION=6.0.9
# Tue, 15 Aug 2023 23:21:57 GMT
COPY dir:a12ac6ea695bc7285b3454c2236744267f0c36ac9ece5b695f0b6536580cab18 in C:\mongodb 
# Tue, 15 Aug 2023 23:22:13 GMT
RUN mongod --version
# Tue, 15 Aug 2023 23:22:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 15 Aug 2023 23:22:15 GMT
EXPOSE 27017
# Tue, 15 Aug 2023 23:22:15 GMT
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
	-	`sha256:8528a4a1b137a0da80fc411f5516b36825a713a30d3ad361d7e3ded4735b147c`  
		Last Modified: Tue, 15 Aug 2023 23:34:19 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46dcbe853873968b61fb5c23178d86e7c3ee36009a7813df257b6d080f74bed0`  
		Last Modified: Tue, 15 Aug 2023 23:35:27 GMT  
		Size: 517.3 MB (517319380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c6655236a3a2fdfe4581b56e08a1a2c08ecad23aff38950c0ea769176b040f`  
		Last Modified: Tue, 15 Aug 2023 23:34:17 GMT  
		Size: 76.2 KB (76185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac8ad9792da98a632de96f4d198a284a4d4c325f1f3e845a85b9ac80418dcae`  
		Last Modified: Tue, 15 Aug 2023 23:34:17 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c387da43e206f1c084826257f3fb18038a2ba39716f9145767458d41060372b`  
		Last Modified: Tue, 15 Aug 2023 23:34:17 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6657f642c6c19f05dca2c1d24702306b79b04a668d89acf6a12d100979cf36a5`  
		Last Modified: Tue, 15 Aug 2023 23:34:17 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
