## `mongo:nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:87107674a0e47c71ab648eb89e5f1d0ae647160c77054d1ce1ceea52cdd217ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `mongo:nanoserver-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull mongo@sha256:609941d0e8a754b1b09174ae08eef779f517cdad2279c62ac2933369cbff037b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **728.7 MB (728695286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad5f1536c0154bae54650ec344b1f8cdaaf94d03f8ebe2cb9f76e7086502c38`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 19 Jun 2024 19:27:30 GMT
RUN Apply image 10.0.20348.2529
# Sat, 29 Jun 2024 00:50:21 GMT
SHELL [cmd /S /C]
# Sat, 29 Jun 2024 00:50:22 GMT
USER ContainerAdministrator
# Sat, 29 Jun 2024 00:50:39 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 29 Jun 2024 00:50:40 GMT
USER ContainerUser
# Sat, 29 Jun 2024 00:50:42 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Sat, 29 Jun 2024 00:50:42 GMT
ENV MONGO_VERSION=7.0.12
# Sat, 29 Jun 2024 00:51:05 GMT
COPY dir:f0b5fa50aabc110faf03295e6346b9d39d589dd155d9a16877c392688d63cd36 in C:\mongodb 
# Sat, 29 Jun 2024 00:51:21 GMT
RUN mongod --version
# Sat, 29 Jun 2024 00:51:21 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 29 Jun 2024 00:51:22 GMT
EXPOSE 27017
# Sat, 29 Jun 2024 00:51:22 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a8c295c425a912de308ded279124ae45fec44d55a451843fe5877155417f453c`  
		Last Modified: Fri, 21 Jun 2024 02:24:34 GMT  
		Size: 120.5 MB (120499549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1743b6778bb15240a633c3fd0790d6a7dac6e1d7a049a78953ae9e7b046d2aa9`  
		Last Modified: Sat, 29 Jun 2024 00:51:27 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6c6deee11e456b21e1761225b009426832a2b187e1adb502e8dfd96cc7f6b6`  
		Last Modified: Sat, 29 Jun 2024 00:51:27 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2db8e92819479b45495df4ec2bf7df5167ab5a0992bb1f40046cdd390513f3d`  
		Last Modified: Sat, 29 Jun 2024 00:51:26 GMT  
		Size: 108.0 KB (108048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ea5321a1104dced4b8119c42deef250a3aafb37b55471dd4d3239fea9073df`  
		Last Modified: Sat, 29 Jun 2024 00:51:26 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd3352eed28c4009f8663bbf36a674c90465a407f52303e2db6fb52532174e2`  
		Last Modified: Sat, 29 Jun 2024 00:51:26 GMT  
		Size: 275.2 KB (275166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa1394456c6cf4fab57ec879d950af50e19615cf92748fd94b375128ec4c92f`  
		Last Modified: Sat, 29 Jun 2024 00:51:26 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8485f2727aa99868194c5f9e673cd826128c0fe853506f048c02fa0e7f4251`  
		Last Modified: Sat, 29 Jun 2024 00:52:13 GMT  
		Size: 607.7 MB (607714415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0de103876144de0d4b7a7f2d1f02615c69c2187ada24b47b892ea6514a79fb`  
		Last Modified: Sat, 29 Jun 2024 00:51:25 GMT  
		Size: 90.9 KB (90889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746c4bd69d6f8a59a7d86e65591ac49a6366d86ed9de528a7e9ddbe3361232e2`  
		Last Modified: Sat, 29 Jun 2024 00:51:25 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccdfe56d5195274c8f71977e4a56f6932823bf43aec9a8beaf69d260c0232c9`  
		Last Modified: Sat, 29 Jun 2024 00:51:25 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23977555776e2e3679cb15985e7de0c96c50713642250449ca1b3be6555d0d7`  
		Last Modified: Sat, 29 Jun 2024 00:51:25 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
