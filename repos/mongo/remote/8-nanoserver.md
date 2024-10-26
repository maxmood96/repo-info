## `mongo:8-nanoserver`

```console
$ docker pull mongo@sha256:719598e1741b880e427e680b5ee9b9c2f68d8043ae0a059135b6d671ac2bfe67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `mongo:8-nanoserver` - windows version 10.0.20348.2762; amd64

```console
$ docker pull mongo@sha256:5f3d253070894b17c7475070cda72eb5a8d0700bee7054d1c0c25deeee27609c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **888.5 MB (888458595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddf9730fd79a800025f1a5fc92af6300a2aa77ccad0b12bdc36dc52fb45c04e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Sat, 26 Oct 2024 00:49:48 GMT
SHELL [cmd /S /C]
# Sat, 26 Oct 2024 00:49:49 GMT
USER ContainerAdministrator
# Sat, 26 Oct 2024 00:50:06 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 26 Oct 2024 00:50:07 GMT
USER ContainerUser
# Sat, 26 Oct 2024 00:50:09 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Sat, 26 Oct 2024 00:50:09 GMT
ENV MONGO_VERSION=8.0.3
# Sat, 26 Oct 2024 00:50:40 GMT
COPY dir:cb547c7cfad49a94afae01b9d93519b13ae3ba80c3c346f206c2035105895991 in C:\mongodb 
# Sat, 26 Oct 2024 00:51:11 GMT
RUN mongod --version
# Sat, 26 Oct 2024 00:51:13 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 26 Oct 2024 00:51:14 GMT
EXPOSE 27017
# Sat, 26 Oct 2024 00:51:16 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a1b981245acddf14bdbe2920c0908e938f028e2e90c58147a3902f4f45f89e`  
		Last Modified: Sat, 26 Oct 2024 00:51:21 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165833b4986ded729d48baa48113b01928d2932c157a4639a2cd69be25d36eb6`  
		Last Modified: Sat, 26 Oct 2024 00:51:20 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746c38db1b6f93d404913c89940fd80b7d1421c29b65b88f6f0c3782ddd410b8`  
		Last Modified: Sat, 26 Oct 2024 00:51:20 GMT  
		Size: 72.5 KB (72474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec8f4c6c775ff1bd78ee6a1993ebf6dfa65de23607338daaa10f8c72e8123ba`  
		Last Modified: Sat, 26 Oct 2024 00:51:20 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eb327bde2a13bb6f4a026c80842b1fb67e8faa2390e3cfb1628c4dd065986c`  
		Last Modified: Sat, 26 Oct 2024 00:51:20 GMT  
		Size: 275.2 KB (275154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28f32cb3f1094b29514262cb7c984985d6b67d732ba0873664645794120ed86`  
		Last Modified: Sat, 26 Oct 2024 00:51:20 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3227cfe24e38006b13c4a74e4f6ede5169b14976962403ac77a84f41f466d08`  
		Last Modified: Sat, 26 Oct 2024 00:52:19 GMT  
		Size: 767.5 MB (767502470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117155b081e7aa41232d317bc77e543e521b4c42a2360342505b38db2988c374`  
		Last Modified: Sat, 26 Oct 2024 00:51:19 GMT  
		Size: 90.2 KB (90223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159023f3b30df6b3ca914fd33900fa1b0c7fa8ee9b91764b2aa5113f943ff742`  
		Last Modified: Sat, 26 Oct 2024 00:51:19 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013d9b1c9554873d4345cc39bd6fd63e8216d7ba456570294e325dcd80d35fe5`  
		Last Modified: Sat, 26 Oct 2024 00:51:19 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d83c9feeb39ee5a53f6349e583ee7c0afa46bc87645a447c44ca51ceb131d0d`  
		Last Modified: Sat, 26 Oct 2024 00:51:19 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:8-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull mongo@sha256:6e52f5858c8934887ee3d9014d69629c4c0aeb7fab3ad70733b34c34368d84f5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **923.0 MB (923009830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de017e60c814181e580a5bbeff2ffb1defd950015ea66a83c9567f5915284246`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Sat, 26 Oct 2024 00:49:54 GMT
SHELL [cmd /S /C]
# Sat, 26 Oct 2024 00:49:55 GMT
USER ContainerAdministrator
# Sat, 26 Oct 2024 00:50:08 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 26 Oct 2024 00:50:08 GMT
USER ContainerUser
# Sat, 26 Oct 2024 00:50:10 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Sat, 26 Oct 2024 00:50:11 GMT
ENV MONGO_VERSION=8.0.3
# Sat, 26 Oct 2024 00:51:14 GMT
COPY dir:cb547c7cfad49a94afae01b9d93519b13ae3ba80c3c346f206c2035105895991 in C:\mongodb 
# Sat, 26 Oct 2024 00:51:23 GMT
RUN mongod --version
# Sat, 26 Oct 2024 00:51:23 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 26 Oct 2024 00:51:24 GMT
EXPOSE 27017
# Sat, 26 Oct 2024 00:51:25 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32be485dfae6db386bbc7ed66034a15f2498fd136935a9af0781660c279645b2`  
		Last Modified: Sat, 26 Oct 2024 00:51:32 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b751935b863c86c50e6212df383fc34157a4f86b0ba316c2ce7e582a69a29e`  
		Last Modified: Sat, 26 Oct 2024 00:51:32 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb75f6931af10933db13245735b36d4c5cca35c3c7cadf2e3388445335ecd1f`  
		Last Modified: Sat, 26 Oct 2024 00:51:31 GMT  
		Size: 65.2 KB (65166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09613b0a187841fc0ac29efde7ae47dbbd2bb6f8f66108fa28a63d1c8b8fb129`  
		Last Modified: Sat, 26 Oct 2024 00:51:30 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6305d5251755376b6ca3b133e5260a4f17aca9078e276dad1291291c419c69`  
		Last Modified: Sat, 26 Oct 2024 00:51:31 GMT  
		Size: 275.2 KB (275171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aed4fcb948de76ecd9bbd61c56abdebfa37ff06212e39d5ad903f50bd3b6f87`  
		Last Modified: Sat, 26 Oct 2024 00:51:30 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100c8b9d09c631c9ee126a655a71b5712aa3128ab0d995d6e8b4bc71c4166df4`  
		Last Modified: Sat, 26 Oct 2024 00:52:30 GMT  
		Size: 767.5 MB (767502221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373cbaf703f570effde5f24fe4d2c3c6e8913b258aa4dbc65769c9ae0b5b6082`  
		Last Modified: Sat, 26 Oct 2024 00:51:29 GMT  
		Size: 66.4 KB (66427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd06388e638de9490fb04c80249af19bc054501ba18aad0b17499ce0ed18b309`  
		Last Modified: Sat, 26 Oct 2024 00:51:29 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b9e131b8f2a9face22df012576696444d780b240c9d3a0e3c720d27aa4acc15`  
		Last Modified: Sat, 26 Oct 2024 00:51:29 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267980f52e50c852df493b62235be381317854772cd559fe0b9905a2a736ecbe`  
		Last Modified: Sat, 26 Oct 2024 00:51:29 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
