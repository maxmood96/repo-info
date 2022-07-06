## `mongo:4-nanoserver-1809`

```console
$ docker pull mongo@sha256:7da736861172f81e071cb9d7626ff85ba2269285b3bd65b12429060a7011b209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `mongo:4-nanoserver-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull mongo@sha256:329f2498f0e78909dc1bec0cc7c667df728cc6d8e2cdd396e936dcfb7ff2e691
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.7 MB (345659673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdd046bf29b5980f7761668286df6d427a335faaada7f16296270f35c11b63d0`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Jun 2022 19:20:11 GMT
RUN Apply image 10.0.17763.3046
# Wed, 15 Jun 2022 13:18:02 GMT
SHELL [cmd /S /C]
# Wed, 15 Jun 2022 21:09:01 GMT
USER ContainerAdministrator
# Wed, 15 Jun 2022 21:09:31 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 15 Jun 2022 21:09:32 GMT
USER ContainerUser
# Wed, 15 Jun 2022 21:09:33 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Tue, 05 Jul 2022 23:22:01 GMT
ENV MONGO_VERSION=4.4.15
# Tue, 05 Jul 2022 23:22:22 GMT
COPY dir:11442d39c1a8be57a2edf36307e3c0f90a74de72a5c1c7d47a958b8e789a5794 in C:\mongodb 
# Tue, 05 Jul 2022 23:22:42 GMT
RUN mongo --version && mongod --version
# Tue, 05 Jul 2022 23:22:43 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 05 Jul 2022 23:22:44 GMT
EXPOSE 27017
# Tue, 05 Jul 2022 23:22:45 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:d555a7e4de4dd775379d5c43c1419374bff7908670dc7444be5e8e8f386f3d26`  
		Size: 103.2 MB (103153235 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ec2e0a40359897e8d5f91d9806e952d9783f2bc30dd279b63a217ee6985ef3c`  
		Last Modified: Wed, 15 Jun 2022 14:07:45 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d19bba12342216b396550bee0fd1ec81490efee021917ee03cd358c63f84ba8`  
		Last Modified: Wed, 15 Jun 2022 21:54:02 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1482fe090238b0a466d117555441f2f20f684020b14f8c6ab297c5e213d39b5e`  
		Last Modified: Wed, 15 Jun 2022 21:53:57 GMT  
		Size: 70.5 KB (70534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8a70e7a7c337b61c46d7d53947831d7a343ec9b3afc2f1ac6909de090c0e88`  
		Last Modified: Wed, 15 Jun 2022 21:53:56 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7c468f9b42d6946f0bee90ae8ef2b05161d9e5f7f6de932d1e31ae7a9728dc`  
		Last Modified: Wed, 15 Jun 2022 21:53:48 GMT  
		Size: 263.5 KB (263496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d1577a65e813765106d36ad45ac4474b9e08ef05f26311f60463942526f0ab`  
		Last Modified: Wed, 06 Jul 2022 00:22:02 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d1de0e73e1fd22a16f1f50c1370ce0b545c4bfe5a2f41ddab45795e13b2078`  
		Last Modified: Wed, 06 Jul 2022 00:22:46 GMT  
		Size: 242.1 MB (242081587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61f653fb7ce022e9272efe66ad8c862ab3da3c6a0ceae7fd1ded35dd76224c5`  
		Last Modified: Wed, 06 Jul 2022 00:21:59 GMT  
		Size: 82.7 KB (82658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80f891ca076f1cf793780b2a07e58ae2c8918989175e7875b985a79151aa39d`  
		Last Modified: Wed, 06 Jul 2022 00:21:59 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2294151f48d4d2e03af7ea01f1fc45d2b34a022cd49fc11d2735025811808a71`  
		Last Modified: Wed, 06 Jul 2022 00:21:59 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92af75d33dc77247867b8dd5e7b78e87a31c1844480dfa0bf6a2934c3cb5479d`  
		Last Modified: Wed, 06 Jul 2022 00:21:59 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
