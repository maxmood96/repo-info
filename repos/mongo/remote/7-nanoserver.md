## `mongo:7-nanoserver`

```console
$ docker pull mongo@sha256:5e4d7bed6230b78e176e702f3baa6964baba8b22415836cedc0819ddccc92ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2527; amd64
	-	windows version 10.0.17763.5936; amd64

### `mongo:7-nanoserver` - windows version 10.0.20348.2527; amd64

```console
$ docker pull mongo@sha256:71f69ad44d433485cc12b86e8e356a802c75579547ed561c49327e116e5ddb89
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **739.1 MB (739110298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f34c0dbe268fa072b7e0a8eae67e154704e57630d392ac64c13cd9b91e0f68c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Jun 2024 08:41:16 GMT
RUN Apply image 10.0.20348.2527
# Wed, 12 Jun 2024 19:09:17 GMT
SHELL [cmd /S /C]
# Wed, 12 Jun 2024 19:09:18 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 19:09:22 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 12 Jun 2024 19:09:22 GMT
USER ContainerUser
# Wed, 12 Jun 2024 19:09:24 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Wed, 12 Jun 2024 19:09:25 GMT
ENV MONGO_VERSION=7.0.11
# Wed, 12 Jun 2024 19:09:46 GMT
COPY dir:19a9c5e7b92e67df364a58952a43fa9635a4cea236c07894dad5b3a27bc56ae4 in C:\mongodb 
# Wed, 12 Jun 2024 19:10:04 GMT
RUN mongod --version
# Wed, 12 Jun 2024 19:10:06 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Jun 2024 19:10:06 GMT
EXPOSE 27017
# Wed, 12 Jun 2024 19:10:07 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:f9825bcd6f9509654677a23b5fa1d32b32e1e32ff51914ebfaa76d5e79c22b50`  
		Last Modified: Wed, 12 Jun 2024 02:27:19 GMT  
		Size: 120.5 MB (120488969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b0edd5ac735d13397fa81bd6bf5a46768d69cb2e2f8d199301f8d82b81f568`  
		Last Modified: Wed, 12 Jun 2024 19:10:12 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d547799d4cb0740a57cc12106886d18be3d736bec47ef86bd0449cf614a496`  
		Last Modified: Wed, 12 Jun 2024 19:10:12 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9caaf03c2a16a962d64af544c7a56e0dfdf600c24ccb4c3adebde992c8cbc40`  
		Last Modified: Wed, 12 Jun 2024 19:10:11 GMT  
		Size: 76.5 KB (76505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a79b28a874f889039afc88e68559cf4271b05f9ca9775a02609175c9287a992`  
		Last Modified: Wed, 12 Jun 2024 19:10:11 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e43dc7210d4c45a44fc36de5e66eb341742672a983e66c86ad07aea3619fa4`  
		Last Modified: Wed, 12 Jun 2024 19:10:11 GMT  
		Size: 267.1 KB (267059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf4c054ef908cc180f735c9839e38cbdeaee1ed35453c46a4d445b59f7cedee`  
		Last Modified: Wed, 12 Jun 2024 19:10:11 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ac0077ab8436425eda6e1dc604479bd99a195bef734f3c75cc136418dd60ef`  
		Last Modified: Wed, 12 Jun 2024 19:10:58 GMT  
		Size: 618.2 MB (618172396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aee9db38620070a696fa5ff55fa085159eb3422ce343cc38294258f2999038a`  
		Last Modified: Wed, 12 Jun 2024 19:10:10 GMT  
		Size: 98.2 KB (98151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6538b475886df193ceed52cb6477dafd8a0cd66c72576df618e5d2e465df7e9c`  
		Last Modified: Wed, 12 Jun 2024 19:10:10 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa64d49060d7e8d5ec5bf1f5cb0474dba8464778f39674d148258f7e7f4bdd5`  
		Last Modified: Wed, 12 Jun 2024 19:10:10 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52bc4c13eef0b9a998a9412fa24f9eb70447af65cf777a8456479a424b5e380`  
		Last Modified: Wed, 12 Jun 2024 19:10:10 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull mongo@sha256:a4fcb16e3118a18e4340e4c6dcb78d8147473b06369f20c68550844e54fdb9f0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **773.6 MB (773638707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29979dfe19c7ff2b68ba4326e9cc9c049f60f2668b2e2a8afbdb88066be994d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:13:30 GMT
SHELL [cmd /S /C]
# Wed, 12 Jun 2024 19:13:32 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 19:13:35 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 12 Jun 2024 19:13:36 GMT
USER ContainerUser
# Wed, 12 Jun 2024 19:13:38 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Wed, 12 Jun 2024 19:13:38 GMT
ENV MONGO_VERSION=7.0.11
# Wed, 12 Jun 2024 19:14:08 GMT
COPY dir:19a9c5e7b92e67df364a58952a43fa9635a4cea236c07894dad5b3a27bc56ae4 in C:\mongodb 
# Wed, 12 Jun 2024 19:14:18 GMT
RUN mongod --version
# Wed, 12 Jun 2024 19:14:19 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Jun 2024 19:14:20 GMT
EXPOSE 27017
# Wed, 12 Jun 2024 19:14:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae69cd7483b9057bbcc5d2786ac0a57b432e0e8850942c3a3bc1de20bdd366a0`  
		Last Modified: Wed, 12 Jun 2024 19:14:25 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45da027f7657918198292e6a349b42635f1ae7cc509f90a6bbcbc05e1345a0f6`  
		Last Modified: Wed, 12 Jun 2024 19:14:25 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82619258ee773b85a9b4ba4b89bc7bdb1de2981c38716661635fda225932f346`  
		Last Modified: Wed, 12 Jun 2024 19:14:24 GMT  
		Size: 71.7 KB (71666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e73b4c76f4e1950b359c62935bd4b252942c6f89989c34720f645a38b45374`  
		Last Modified: Wed, 12 Jun 2024 19:14:24 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa6aec6d841df7d24a1eb9431484b21a62974e7b6f6d0b552545b5fac7d6f68`  
		Last Modified: Wed, 12 Jun 2024 19:14:24 GMT  
		Size: 267.1 KB (267060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bf0d189d5ab2a7a13a51e14926129b8fdcc11015702f78b3b5d30b07721652`  
		Last Modified: Wed, 12 Jun 2024 19:14:24 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1317d60f055acf3a9cb0badf445b9a5ffb8e0d7ad60969a7e5b0895aca39d2`  
		Last Modified: Wed, 12 Jun 2024 19:15:11 GMT  
		Size: 618.2 MB (618172202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7741f32eb13ee9b126eaab58a40bd66007cf92a473dd49c79f914ef2ab62a7bd`  
		Last Modified: Wed, 12 Jun 2024 19:14:23 GMT  
		Size: 87.3 KB (87277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbfa992d0b38ee61058c12c595f8e3ce77230a813135c9c3e690bd22412d8f6`  
		Last Modified: Wed, 12 Jun 2024 19:14:23 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067376a717a31483d00c2ab64d8da606a771e9d04dcf8faab04337f1ca908a40`  
		Last Modified: Wed, 12 Jun 2024 19:14:23 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307776a55d35f9403ec370e9a8254a1de6ebee0e8a3eb9a14c54e627420d46d1`  
		Last Modified: Wed, 12 Jun 2024 19:14:23 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
