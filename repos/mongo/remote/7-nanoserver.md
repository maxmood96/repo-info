## `mongo:7-nanoserver`

```console
$ docker pull mongo@sha256:dda6d1bd062461bb7c68e88de96dd9ea6887d1fe26830952fe6dfdbc85215905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `mongo:7-nanoserver` - windows version 10.0.20348.4529; amd64

```console
$ docker pull mongo@sha256:b286439a37340e74ed281fa08372e04ef1910899050453054d417ddc8fe2d409
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.3 MB (744329102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a387aaf847f12d34f1ad82be0b69523cff7e15ac3eb717408c88241e60205985`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Fri, 19 Dec 2025 20:12:34 GMT
SHELL [cmd /S /C]
# Fri, 19 Dec 2025 20:12:35 GMT
USER ContainerAdministrator
# Fri, 19 Dec 2025 20:12:43 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 19 Dec 2025 20:12:44 GMT
USER ContainerUser
# Fri, 19 Dec 2025 20:12:46 GMT
COPY multi:540d6dd70b1e7484f1958dc08b337aeb56cf8a92fe38be4c279dd406990d6935 in C:\Windows\System32\ 
# Fri, 19 Dec 2025 20:17:38 GMT
ENV MONGO_VERSION=7.0.28
# Fri, 19 Dec 2025 20:18:23 GMT
COPY dir:a1ad2752e47279d3bb4839cb7b8eb5af635ef6fb54f82ba6bd2e3c7473ec3fc6 in C:\mongodb 
# Fri, 19 Dec 2025 20:18:40 GMT
RUN mongod --version
# Fri, 19 Dec 2025 20:18:41 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 19 Dec 2025 20:18:41 GMT
EXPOSE 27017
# Fri, 19 Dec 2025 20:18:42 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5da9d404d4b5c1d96e1676d163d271c25539436df2613e02c9950ba7b157ac5`  
		Last Modified: Fri, 19 Dec 2025 20:16:36 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e0d2cfd58f6b0c8ad1a4b13a109e9439080495a28d14ce29a50d61e715d6c9`  
		Last Modified: Fri, 19 Dec 2025 20:16:36 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737e48be1f172603677e7dc22e18a3cb2c08aebdc210a8cfb4e497b65b878dc9`  
		Last Modified: Fri, 19 Dec 2025 20:16:36 GMT  
		Size: 71.2 KB (71250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf310a71b78ce7f3eb2d13f2fd773f7280d02162e9c6e7caac9d250a219069d`  
		Last Modified: Fri, 19 Dec 2025 20:16:36 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0fda14cea78e1aa20602db25383546c89d8092cf2b0cd9ecdacc1adaa5a3e8`  
		Last Modified: Fri, 19 Dec 2025 20:16:36 GMT  
		Size: 275.2 KB (275215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7e1bea252d7b686026e9a45de82c24f9f31f78731abcb1844a39b9f3267fdc`  
		Last Modified: Fri, 19 Dec 2025 20:19:56 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94dec5136c4ff5b2316a413fa01fb8d4dc30b994befe4c5b5da48c7e355361e3`  
		Last Modified: Fri, 19 Dec 2025 20:20:13 GMT  
		Size: 617.5 MB (617528463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4630be656ac25eec0bb8e3283dc0940efa54e620bc22af898452fb27e8818253`  
		Last Modified: Fri, 19 Dec 2025 20:19:56 GMT  
		Size: 88.4 KB (88404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5b6340a703fa1f6b18fd49d13e6746073e149362c77fb3854a41352c48f9e`  
		Last Modified: Fri, 19 Dec 2025 20:19:56 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcce67b926e094534169e74bc1462af967b5e98e8d5c3f9e3540ad6ad66903b`  
		Last Modified: Fri, 19 Dec 2025 20:19:56 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366239cac20ced076dff1a812499bc0b55d880c452841980d3acc4325f836521`  
		Last Modified: Fri, 19 Dec 2025 20:19:56 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
