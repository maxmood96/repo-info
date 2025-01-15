## `mongo:6-nanoserver-1809`

```console
$ docker pull mongo@sha256:4da70c4a45bbad641b9de819c2d302ef66a58e0e762a2831cabcec8370d4cca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `mongo:6-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull mongo@sha256:3c4429b7114545a1b1eb812a9f380705ae922ca6f6bb1623a1838a0575769342
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.4 MB (681375598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3cc8b31782a3da4137a321fc2449dbb4de30e6ea84fdc358583c5c7edffac3`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 17:57:01 GMT
SHELL [cmd /S /C]
# Wed, 15 Jan 2025 17:57:01 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 17:57:03 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 15 Jan 2025 17:57:04 GMT
USER ContainerUser
# Wed, 15 Jan 2025 17:57:05 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 15 Jan 2025 17:57:06 GMT
ENV MONGO_VERSION=6.0.19
# Wed, 15 Jan 2025 17:57:36 GMT
COPY dir:f97029ff7a52e12f6b8e5522b58ebccd35083615a35a3126b84db5898f526c7b in C:\mongodb 
# Wed, 15 Jan 2025 17:57:43 GMT
RUN mongod --version
# Wed, 15 Jan 2025 17:57:44 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jan 2025 17:57:44 GMT
EXPOSE 27017
# Wed, 15 Jan 2025 17:57:45 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24da20a1dec421e4af13c22250ad747e6b0be6f4d49318c3d865f04c3d2575c7`  
		Last Modified: Wed, 15 Jan 2025 17:57:53 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36dc566f57e191b8ae5ed193dc6dae8cd1477dfc012aac8f9d145f2d3981db94`  
		Last Modified: Wed, 15 Jan 2025 17:57:53 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5aab54edc1031a03ff77fa0cbe6ed19ebff6c7c584f1169ad318b05bc8122e6`  
		Last Modified: Wed, 15 Jan 2025 17:57:51 GMT  
		Size: 72.6 KB (72641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b4d02a2669f02d20cf6d22a68e5c9d67eac580db1cc20070724a544fa97263`  
		Last Modified: Wed, 15 Jan 2025 17:57:51 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c2a4a5f1c134a7d81f5701848cf677e71f59ee344f1ef772318a214d16e271`  
		Last Modified: Wed, 15 Jan 2025 17:57:52 GMT  
		Size: 275.2 KB (275167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ecb54db7faf56dfdda46327353f0bf230203c9ceb168a2c68b1759b61b7b50f`  
		Last Modified: Wed, 15 Jan 2025 17:57:51 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901809b8105fb1bed1e06c565ff5986f07d1eec6cb6fe49311148d471a38e0d6`  
		Last Modified: Wed, 15 Jan 2025 17:58:31 GMT  
		Size: 525.7 MB (525676983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0777362a1a406073449a5d0052b7de32fa93964221702e643b95739195f8282a`  
		Last Modified: Wed, 15 Jan 2025 17:57:49 GMT  
		Size: 76.0 KB (75952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56899841fa6d5005d4c0a7aed2c764e892fd5a2b8c55ac9052f4e233b912c4ed`  
		Last Modified: Wed, 15 Jan 2025 17:57:49 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e3a196da08fb3c035f4e8a905d7a8e28567e8d6319f3e64317ffc17f01883f`  
		Last Modified: Wed, 15 Jan 2025 17:57:49 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df33b08df0ca4213335c57bf1e3a3b1dba71ebe8f9620430786c8a72dee090b0`  
		Last Modified: Wed, 15 Jan 2025 17:57:49 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
