## `mongo:7-nanoserver`

```console
$ docker pull mongo@sha256:1064e4cb5ec7e91718e8d629df50afb3acfa6083a30a196335595e3b367f334f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `mongo:7-nanoserver` - windows version 10.0.20348.2966; amd64

```console
$ docker pull mongo@sha256:cf5b2c2299559fa289f439a34be876f52200ec8f51a4ba13277bf8a8595f3f8a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.4 MB (731407913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29ec3bd4c58dde1f238f4b632aa636d97ffefbd8eea6232181486a3ee63cf05`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 05 Dec 2024 01:18:54 GMT
RUN Apply image 10.0.20348.2966
# Wed, 11 Dec 2024 21:50:34 GMT
SHELL [cmd /S /C]
# Wed, 11 Dec 2024 21:50:35 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:50:37 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 11 Dec 2024 21:50:38 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:50:40 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 11 Dec 2024 21:50:41 GMT
ENV MONGO_VERSION=7.0.15
# Wed, 11 Dec 2024 21:51:00 GMT
COPY dir:420a97257b8f41b5187b8c509722525c37efef8c1a1591fc20aa57d257fef5d8 in C:\mongodb 
# Wed, 11 Dec 2024 21:51:16 GMT
RUN mongod --version
# Wed, 11 Dec 2024 21:51:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2024 21:51:18 GMT
EXPOSE 27017
# Wed, 11 Dec 2024 21:51:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:f9d5d5ca3244fc2c429a892cbe6066394790f649f32d59acfdf012e490896378`  
		Last Modified: Tue, 10 Dec 2024 18:34:17 GMT  
		Size: 120.6 MB (120601318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb164bf03b9a2a4e63d6e2bb34ce9f4c108a446008a3eb32da3cf71245aced58`  
		Last Modified: Wed, 11 Dec 2024 21:51:23 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a448ff5abd6217ace4a5a2277490d69783eedddea7cfcd5a3a69e6857cdbce25`  
		Last Modified: Wed, 11 Dec 2024 21:51:23 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213d363a0948075b5d3fce8e92654000603c9322099ced3a4c332c6afc9755be`  
		Last Modified: Wed, 11 Dec 2024 21:51:22 GMT  
		Size: 79.7 KB (79735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb99ea532f20736a82dc305bf90e74df65cabd62baa6813799b21dde8411028c`  
		Last Modified: Wed, 11 Dec 2024 21:51:22 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4570e60b92f063131d08766d4c5e2a452e98dfdd2bc32a1c04fab44651368703`  
		Last Modified: Wed, 11 Dec 2024 21:51:22 GMT  
		Size: 275.1 KB (275137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd87e31f04561827223bf750ee150e84a68b1be438ccc827c731089f84401805`  
		Last Modified: Wed, 11 Dec 2024 21:51:22 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018bb7d922147b4ff74ca56d5235d02576bdb252df33b5746f645a878c822669`  
		Last Modified: Wed, 11 Dec 2024 21:52:08 GMT  
		Size: 610.3 MB (610337738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1207111af45128f38b1e1e45860b544c57f4e8f5cb34ac56dd0f436f22b20e`  
		Last Modified: Wed, 11 Dec 2024 21:51:21 GMT  
		Size: 106.8 KB (106777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea02499fd6397e406ef44e2ad841a5117336c99389cd00704fb808be7fd6663`  
		Last Modified: Wed, 11 Dec 2024 21:51:21 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7844ec2175d5e9eb78f713f11c3ca23cac60406c8e3f449016470600443ce0`  
		Last Modified: Wed, 11 Dec 2024 21:51:21 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7916125559131aa4a9d1f01e7e3b6af79b3bf18e011df7303a77101373071e84`  
		Last Modified: Wed, 11 Dec 2024 21:51:21 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-nanoserver` - windows version 10.0.17763.6659; amd64

```console
$ docker pull mongo@sha256:37a8946430609b3e96c8bfe74b8e9044f1f175cdcbc5615b18231860bd6853f6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **766.0 MB (765994316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1227e94edfc1eaf94c6b041f460de6bf4e9a5ec3b6866405452907896e8bef`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Wed, 11 Dec 2024 21:44:53 GMT
SHELL [cmd /S /C]
# Wed, 11 Dec 2024 21:44:54 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:44:56 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 11 Dec 2024 21:44:57 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:44:59 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 11 Dec 2024 21:45:00 GMT
ENV MONGO_VERSION=7.0.15
# Wed, 11 Dec 2024 21:45:33 GMT
COPY dir:420a97257b8f41b5187b8c509722525c37efef8c1a1591fc20aa57d257fef5d8 in C:\mongodb 
# Wed, 11 Dec 2024 21:45:41 GMT
RUN mongod --version
# Wed, 11 Dec 2024 21:45:42 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2024 21:45:43 GMT
EXPOSE 27017
# Wed, 11 Dec 2024 21:45:43 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933dacdcaa08c06c2816e936e572cfcc1b52d5c4c48991b624124f1b787867b9`  
		Last Modified: Wed, 11 Dec 2024 21:45:48 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90efdd1aa13a924c075e8688fd6f77fcb70245b28f981de2224aec90523814c0`  
		Last Modified: Wed, 11 Dec 2024 21:45:48 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9a54e4c954f6711db272dba33a9b63bd3f173dba206c813a7b7827ad3aa4b4`  
		Last Modified: Wed, 11 Dec 2024 21:45:47 GMT  
		Size: 69.7 KB (69686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7bffc1fcb27594968e5f090bc0b71e410ee3d2c3c87c655a5221a32816f4863`  
		Last Modified: Wed, 11 Dec 2024 21:45:47 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6955b6a90bd3db1e57afac844fe5f300c27a53186e8328fd170d5c722185f78a`  
		Last Modified: Wed, 11 Dec 2024 21:45:47 GMT  
		Size: 275.2 KB (275187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5a39c48ef22cabc392b22a7882e8895df4079a329684725bafd410783d012c`  
		Last Modified: Wed, 11 Dec 2024 21:45:47 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbd9dd1bf442fa7aced725ecd1959610d90d52b01b35d8f609e2dd0d82d651d`  
		Last Modified: Wed, 11 Dec 2024 21:46:34 GMT  
		Size: 610.3 MB (610337489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8004af9ca1942ba80cb7396741807103c42fc40826158eb38d086074bdbb76ea`  
		Last Modified: Wed, 11 Dec 2024 21:45:46 GMT  
		Size: 73.1 KB (73089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3244a485303cd69eb0541bdd23cf97b3deea4b8b56ccecf0ddaa8cf49c99a881`  
		Last Modified: Wed, 11 Dec 2024 21:45:46 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ce9a15f164f6795fc820c9af12495463a8575a35bc27d9591738896ebfa629`  
		Last Modified: Wed, 11 Dec 2024 21:45:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83fa084b035899e46d963f4bd467c181ab02dcc9e94ef004f09064f970db94d`  
		Last Modified: Wed, 11 Dec 2024 21:45:46 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
