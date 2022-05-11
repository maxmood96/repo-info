## `mongo:4-nanoserver`

```console
$ docker pull mongo@sha256:772814132c5879862bb6c8647b1798f55a69c81b342937de69d4d22b043453b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.707; amd64
	-	windows version 10.0.17763.2928; amd64

### `mongo:4-nanoserver` - windows version 10.0.20348.707; amd64

```console
$ docker pull mongo@sha256:8518d760bb28eb387d29b777d471455c361975c0a204d4b4fe06619d23636a1b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.7 MB (359709251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b85fe2dc29c01b1f9eeb738557a0a1897e489213b3a79ecb4bc1cd288bb563`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 05 May 2022 02:37:33 GMT
RUN Apply image 10.0.20348.707
# Tue, 10 May 2022 22:28:05 GMT
SHELL [cmd /S /C]
# Wed, 11 May 2022 16:39:17 GMT
USER ContainerAdministrator
# Wed, 11 May 2022 16:39:33 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 11 May 2022 16:39:33 GMT
USER ContainerUser
# Wed, 11 May 2022 16:39:35 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 11 May 2022 16:50:59 GMT
ENV MONGO_VERSION=4.4.13
# Wed, 11 May 2022 16:51:21 GMT
COPY dir:cb2795f5b405c92d2e3366f5e962d386ae580b206db49ff53e53730c9b68815c in C:\mongodb 
# Wed, 11 May 2022 16:51:37 GMT
RUN mongo --version && mongod --version
# Wed, 11 May 2022 16:51:38 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 May 2022 16:51:39 GMT
EXPOSE 27017
# Wed, 11 May 2022 16:51:40 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2c74f0842c5a8e9b80b9e2cf64e1ab10a6fa67951f28cff5fee060b88128564c`  
		Size: 117.7 MB (117687017 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:617bb7e935bb4ca0ff934490b4a9f19a0bdedc2df4476ebd2784b3e63f7ec0eb`  
		Last Modified: Tue, 10 May 2022 22:56:44 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a76e790336cc4d64aaadb23a03a27f9f4352a880194898d465e6a82e7b9dd6a`  
		Last Modified: Wed, 11 May 2022 17:20:55 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b030784dcc6bf7a514f4644008557472c82550eadadd78af9809824614c3183`  
		Last Modified: Wed, 11 May 2022 17:20:53 GMT  
		Size: 77.9 KB (77875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ab77618c3aa83b86640181eb4fb79f1c00adee456bf2b314370fb54fa17cd5`  
		Last Modified: Wed, 11 May 2022 17:20:53 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6776d86c1e048f2ff9fcb9c0ee71fea4ea239bd9052c11ca2ed76c7b6b323919`  
		Last Modified: Wed, 11 May 2022 17:20:53 GMT  
		Size: 263.5 KB (263499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc863b95260ec3790e66388e09d674c91c14ee5b5702d934b41ef627a37c36f4`  
		Last Modified: Wed, 11 May 2022 17:49:37 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b696925ba9c5eca9c49acc51e82470f7ecfcd40b5aa63e5bbaab2e7c4c573a85`  
		Last Modified: Wed, 11 May 2022 17:53:47 GMT  
		Size: 241.6 MB (241620367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74764004ca939ea56b08c33402e75798ebc5891b1690c776b9299e0fc04135c2`  
		Last Modified: Wed, 11 May 2022 17:49:34 GMT  
		Size: 52.4 KB (52363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5936aa1d4ff6bcc297f6fa4620ca584dcafa62f78cab4775084dda5b77f7f993`  
		Last Modified: Wed, 11 May 2022 17:49:34 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e6b3d9d205a9f041bf4032435d4d3abc3f949a2afc72edb7e2375e28a467a4`  
		Last Modified: Wed, 11 May 2022 17:49:34 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34590e124021afd2feb30fc02f02dc1be65db0ea9f7676aa7f1c38bc126bd5a`  
		Last Modified: Wed, 11 May 2022 17:49:34 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-nanoserver` - windows version 10.0.17763.2928; amd64

```console
$ docker pull mongo@sha256:2a1b6ff39fe8fae6c2b518e22b706e6189ae30b84505c5239d160d77a37cd7ed
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345165923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86bf6131e8bf7e914dcce8c569feb6d3fe652ba276e311a0fa895335a663ca32`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Tue, 10 May 2022 22:32:24 GMT
SHELL [cmd /S /C]
# Wed, 11 May 2022 16:40:31 GMT
USER ContainerAdministrator
# Wed, 11 May 2022 16:40:44 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 11 May 2022 16:40:45 GMT
USER ContainerUser
# Wed, 11 May 2022 16:40:46 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 11 May 2022 16:51:51 GMT
ENV MONGO_VERSION=4.4.13
# Wed, 11 May 2022 16:52:14 GMT
COPY dir:cb2795f5b405c92d2e3366f5e962d386ae580b206db49ff53e53730c9b68815c in C:\mongodb 
# Wed, 11 May 2022 16:52:28 GMT
RUN mongo --version && mongod --version
# Wed, 11 May 2022 16:52:28 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 May 2022 16:52:29 GMT
EXPOSE 27017
# Wed, 11 May 2022 16:52:30 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d7d4dec608f59eb9166ff96f59e4f4fcbda08a55e78d630ba39e558b23b3e475`  
		Last Modified: Tue, 10 May 2022 22:59:35 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987cbdd0546a925a5277fca5911acd2464f2d239476fc117cd8a3011bd985189`  
		Last Modified: Wed, 11 May 2022 17:27:18 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded12f0f392c537c7ff213a868a7db1e71d13284232bf441fb1b18802cc2c58a`  
		Last Modified: Wed, 11 May 2022 17:27:16 GMT  
		Size: 67.6 KB (67566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4a2b90ac4cd5ddd91d660cc65ee02c9cb8c76798bcfcf2f2659c9392279c54`  
		Last Modified: Wed, 11 May 2022 17:27:16 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010bcf23b940f6ea8fc6a008db1ca8b75afaf2fbcf10edac831c4ea75c2d9146`  
		Last Modified: Wed, 11 May 2022 17:27:16 GMT  
		Size: 263.5 KB (263496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b2e35d364a37edd8ddcf2a11165abd727f007d317dd1e3efa81366bc32c97`  
		Last Modified: Wed, 11 May 2022 17:54:04 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a91a87587608b7b88ae7bab06666fbf78c72343830cec033a7ef75b836ce5b`  
		Last Modified: Wed, 11 May 2022 17:58:09 GMT  
		Size: 241.6 MB (241620417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b778787eda6ac0b9dcdc7f82f87c3fa8c118daf9c9b7000749e5f02127a8d79`  
		Last Modified: Wed, 11 May 2022 17:54:02 GMT  
		Size: 72.4 KB (72432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ecda082b4a9feaf59cfd152fa195a72fd30d5aaed9e9508296b1e75ee237bc`  
		Last Modified: Wed, 11 May 2022 17:54:01 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea49c3f80f7c4f8ec1fec5f42d3ba6a4b40015da4ebe2de423234f3468c45ab5`  
		Last Modified: Wed, 11 May 2022 17:54:01 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e2fd771dd1a9faf5eddb96d281127cebb256a9cd997962dd59824c5262fff1`  
		Last Modified: Wed, 11 May 2022 17:54:02 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
