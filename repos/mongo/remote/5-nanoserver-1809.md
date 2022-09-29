## `mongo:5-nanoserver-1809`

```console
$ docker pull mongo@sha256:323a078d271933c99eaf2613ee024ce0de1690489ae859822e856ebf8cf47b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `mongo:5-nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull mongo@sha256:6745996bde167a37ce3d57201225ebd613262065029044e1408941496c1f4851
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.7 MB (413725915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f412b62bd2a6bbd5d9d81b8745982df23532ee715e95594ba02d98c9570f2db5`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 13:03:35 GMT
SHELL [cmd /S /C]
# Wed, 14 Sep 2022 18:18:09 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 18:18:21 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 14 Sep 2022 18:18:22 GMT
USER ContainerUser
# Wed, 14 Sep 2022 18:24:40 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Thu, 29 Sep 2022 20:30:13 GMT
ENV MONGO_VERSION=5.0.13
# Thu, 29 Sep 2022 20:30:47 GMT
COPY dir:644971c5551a7576841d7084c8a9e1086a2329d8484b2783b73ea3b245ca1a2f in C:\mongodb 
# Thu, 29 Sep 2022 20:31:02 GMT
RUN mongo --version && mongod --version
# Thu, 29 Sep 2022 20:31:03 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 29 Sep 2022 20:31:04 GMT
EXPOSE 27017
# Thu, 29 Sep 2022 20:31:05 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0668477bacdfc2e7df1cd4268b246175ed9b30cf07ccb4bcfcb258d8bee830e`  
		Last Modified: Wed, 14 Sep 2022 13:26:19 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ada06039b3dceb53c91ed6d7bd2d77d0abd90acba1883744d947d1ccee8349`  
		Last Modified: Wed, 14 Sep 2022 19:03:38 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d170c6bf2fd2a53a952e69b17f97ce92dd39dd7294e4b1c6ae6e11adc613210`  
		Last Modified: Wed, 14 Sep 2022 19:03:36 GMT  
		Size: 69.7 KB (69673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d16b6830f5e893640af2e263523f5ff88334d46d1a2d69d91cddf1f70f62790`  
		Last Modified: Wed, 14 Sep 2022 19:03:36 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98574a2f866f60f51f05d43d7e4e9d7e62e346b27ff83266400261170b141e2b`  
		Last Modified: Wed, 14 Sep 2022 19:08:41 GMT  
		Size: 263.5 KB (263502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3d106e5ff5c20637254ae978d378085d83fb130d7838f0318d2c592d13d134`  
		Last Modified: Thu, 29 Sep 2022 20:50:34 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6181cb9c733d21f9815721a0acdab91c9f7ffa840b2ad96489cc1e6ad4736f3d`  
		Last Modified: Thu, 29 Sep 2022 20:51:26 GMT  
		Size: 310.0 MB (309969698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88d5a0e5922c0308283127f2b28fa4811d95f3e61df078901b0cde626bf1089`  
		Last Modified: Thu, 29 Sep 2022 20:50:32 GMT  
		Size: 80.9 KB (80940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cee29e3e8e63ebddaa4fb39f7c973919876c7ef811ea31f6ff955262a10abf7`  
		Last Modified: Thu, 29 Sep 2022 20:50:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e76a899df7b97dc77c6ef6a76e87e7416c139b36ff8a8806e97eca59cd1ea2a`  
		Last Modified: Thu, 29 Sep 2022 20:50:32 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182e312d9b23e0b8dd9bfd81a33d9400b3b6b73db4404baa94a4c928fb25b86f`  
		Last Modified: Thu, 29 Sep 2022 20:50:32 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
