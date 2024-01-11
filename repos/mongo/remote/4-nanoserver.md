## `mongo:4-nanoserver`

```console
$ docker pull mongo@sha256:2d2fd0e938c657fed7dbc249672b5c3d87a6933a515a814ac43f4031062b4b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `mongo:4-nanoserver` - windows version 10.0.20348.2227; amd64

```console
$ docker pull mongo@sha256:7c4b1462dd2b8cf1b0e896ee8ac11ad6a8dceea3a75a6c335db5769d54e78aee
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.2 MB (366186689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b31e0cbd593f184958cc92b1db8a2f445008b0c8cc9a949a6ffeecb5da4f315`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Thu, 11 Jan 2024 00:55:08 GMT
SHELL [cmd /S /C]
# Thu, 11 Jan 2024 00:55:09 GMT
USER ContainerAdministrator
# Thu, 11 Jan 2024 00:55:12 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 11 Jan 2024 00:55:13 GMT
USER ContainerUser
# Thu, 11 Jan 2024 00:55:14 GMT
COPY multi:d83167ee7f0a01f519841410f1f031c3bdfa566af08cc1936efaf3b3f20e2b0f in C:\Windows\System32\ 
# Thu, 11 Jan 2024 00:55:15 GMT
ENV MONGO_VERSION=4.4.27
# Thu, 11 Jan 2024 00:55:26 GMT
COPY dir:9a4451ece440a57e287596f9b8b98884938e76dd62cf67441f8c60aeee0d3e41 in C:\mongodb 
# Thu, 11 Jan 2024 00:55:36 GMT
RUN mongo --version && mongod --version
# Thu, 11 Jan 2024 00:55:37 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jan 2024 00:55:37 GMT
EXPOSE 27017
# Thu, 11 Jan 2024 00:55:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:11d5cdc5eaac7bace3ae1ecd3c0df2a27ef5005ab296c56b7f83e24bf25c236c`  
		Last Modified: Tue, 09 Jan 2024 20:57:18 GMT  
		Size: 120.8 MB (120769267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c09cce440382d3db43120a7d72684069e427a7521ed44e8ed348b6f2947de1`  
		Last Modified: Thu, 11 Jan 2024 00:55:46 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280b8144948ae0cf4945cdeeb958eafb75d2ed659c9669768857848f6f4b8935`  
		Last Modified: Thu, 11 Jan 2024 00:55:45 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191793692a72809c37f04ec3fd48d981dc598e64c2505167f846dd1724093cf4`  
		Last Modified: Thu, 11 Jan 2024 00:55:44 GMT  
		Size: 84.9 KB (84916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011de084b2610f78d220738121f5752ab4a344396cea9998e32bde7be378b99f`  
		Last Modified: Thu, 11 Jan 2024 00:55:44 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66950599842ba98bc21e1cc5efe47ddc35ba64efc8daf5bbbff4727648134fa3`  
		Last Modified: Thu, 11 Jan 2024 00:55:44 GMT  
		Size: 263.4 KB (263371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bce3527e9e895adffdc0e3108941c014da163e3e7b21e5e197715ac3b535e62`  
		Last Modified: Thu, 11 Jan 2024 00:55:43 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ad53d9ccf88fd4501fa368d251d77503d45977324c3ecb463989cdac183def`  
		Last Modified: Thu, 11 Jan 2024 00:56:06 GMT  
		Size: 245.0 MB (244979230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e46e9cec72175db0d1504d36adaa6d4c3763c53b60ea6ae532291927d68d24d`  
		Last Modified: Thu, 11 Jan 2024 00:55:42 GMT  
		Size: 82.4 KB (82407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5bcad9f5955a04a02d986552a01a4544e2a62438ecb4ded4c7bb8dba1dd6ec`  
		Last Modified: Thu, 11 Jan 2024 00:55:42 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7d00ac660e5bcda1e20e3bf897dff95a4e4bacb526c94bb6a14cbe04ec3ad1`  
		Last Modified: Thu, 11 Jan 2024 00:55:42 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efa08e335c932b13eec90d0a7ec71f571e9b6676e377511ced7966ab37ca0f9`  
		Last Modified: Thu, 11 Jan 2024 00:55:42 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull mongo@sha256:1d9374b86810f140fe86c9c278399c8bf3e12bc5a2e9d150e1ceaa46a1209a56
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.0 MB (349983528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010a4e11cd023484798f7dbb4dc4c8021b8a806d3ba6b4f1bbc16119c4086c42`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:59:00 GMT
SHELL [cmd /S /C]
# Thu, 11 Jan 2024 00:59:02 GMT
USER ContainerAdministrator
# Thu, 11 Jan 2024 00:59:05 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 11 Jan 2024 00:59:05 GMT
USER ContainerUser
# Thu, 11 Jan 2024 00:59:07 GMT
COPY multi:d83167ee7f0a01f519841410f1f031c3bdfa566af08cc1936efaf3b3f20e2b0f in C:\Windows\System32\ 
# Thu, 11 Jan 2024 00:59:08 GMT
ENV MONGO_VERSION=4.4.27
# Thu, 11 Jan 2024 00:59:20 GMT
COPY dir:9a4451ece440a57e287596f9b8b98884938e76dd62cf67441f8c60aeee0d3e41 in C:\mongodb 
# Thu, 11 Jan 2024 00:59:25 GMT
RUN mongo --version && mongod --version
# Thu, 11 Jan 2024 00:59:26 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jan 2024 00:59:26 GMT
EXPOSE 27017
# Thu, 11 Jan 2024 00:59:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4a078746161fb95f7f1f47669b183b7ae83bc6b1641cd9c427e53543ae33f6`  
		Last Modified: Thu, 11 Jan 2024 00:59:31 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff7245646b7c4d53376c6f7c24c496948ce6a27c6ab3f391de7d2dfe857cf17`  
		Last Modified: Thu, 11 Jan 2024 00:59:31 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e72467ea07fb1d4cfbf3a3c13abe1f957793a46c3abdf985c5be02b6f31ac9`  
		Last Modified: Thu, 11 Jan 2024 00:59:31 GMT  
		Size: 69.2 KB (69157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a034dc53c7aa7d30957e91895427fa2aa76e637f9bdc11fe9113e1e8d08f1b3`  
		Last Modified: Thu, 11 Jan 2024 00:59:30 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2d32dcede1362cdc61a77b87bff4808f5cafa8b7d2849d659e94ad356c7bf`  
		Last Modified: Thu, 11 Jan 2024 00:59:30 GMT  
		Size: 263.4 KB (263376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a8731f576a2ad9ab07b5dd9c4dc0b4a49285784c297c33b41d0081b5414a1b`  
		Last Modified: Thu, 11 Jan 2024 00:59:30 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e361f9ee423e21098e2eed325424999ebf9fd08934bf6214db05c5ae613ade`  
		Last Modified: Thu, 11 Jan 2024 00:59:54 GMT  
		Size: 245.0 MB (244979376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3595a8b9c3877c808d66ecbb6be49d5d0e861d7fc3533e88b123ce65bc47139`  
		Last Modified: Thu, 11 Jan 2024 00:59:29 GMT  
		Size: 73.2 KB (73166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad27f21aa2081705ced4c05011fc53c1aa3689cafdafe9fde3f4aca8157293cc`  
		Last Modified: Thu, 11 Jan 2024 00:59:29 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a6fd8de01422f6c23c605572a39b2fc68dfea254a54e4990f15fb7bf262afb`  
		Last Modified: Thu, 11 Jan 2024 00:59:29 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cf366bb476d782d447419baf5cbf52d5addd8e602c1725fcc2fe5dfd5e346e`  
		Last Modified: Thu, 11 Jan 2024 00:59:29 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
