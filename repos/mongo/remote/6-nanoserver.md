## `mongo:6-nanoserver`

```console
$ docker pull mongo@sha256:0aaaeb0619f43868e67559bb7e450f4ffa100acef73c05234d8e3f1ab246a6e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `mongo:6-nanoserver` - windows version 10.0.20348.2227; amd64

```console
$ docker pull mongo@sha256:99d75a384311e370653efc29a1215313d392788b5680b65fde4d6b8c6d2bdd0b
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.5 MB (639543647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6cd070924c9e423f965560a4c47525e283e9198c4332bfeb9ff2916f4ca60a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Fri, 19 Jan 2024 00:52:04 GMT
SHELL [cmd /S /C]
# Fri, 19 Jan 2024 00:52:05 GMT
USER ContainerAdministrator
# Fri, 19 Jan 2024 00:52:35 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 19 Jan 2024 00:52:36 GMT
USER ContainerUser
# Fri, 19 Jan 2024 00:52:38 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Fri, 19 Jan 2024 00:52:38 GMT
ENV MONGO_VERSION=6.0.13
# Fri, 19 Jan 2024 00:53:00 GMT
COPY dir:52c8844300bd1267892ff953bada283f10975ec77346ef3bec4c64101fde69fa in C:\mongodb 
# Fri, 19 Jan 2024 00:53:14 GMT
RUN mongod --version
# Fri, 19 Jan 2024 00:53:15 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 19 Jan 2024 00:53:16 GMT
EXPOSE 27017
# Fri, 19 Jan 2024 00:53:16 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:11d5cdc5eaac7bace3ae1ecd3c0df2a27ef5005ab296c56b7f83e24bf25c236c`  
		Last Modified: Tue, 09 Jan 2024 20:57:18 GMT  
		Size: 120.8 MB (120769267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975922d243cb3e3c27332e7aa449ee806913fcbd2c06d5a2182638d40d668ef2`  
		Last Modified: Fri, 19 Jan 2024 00:53:21 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e437e560ceecd609b6d2f2818f95cc8e743d3cee9013bb9e31d744670dc121e`  
		Last Modified: Fri, 19 Jan 2024 00:53:21 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec00f06b062f683df2915f66d63525b2d2ab6bf0426798bb32b9d273bf6f742`  
		Last Modified: Fri, 19 Jan 2024 00:53:21 GMT  
		Size: 104.2 KB (104247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4214e008817d9685409a29d43bd7909a3d3477b05aad971afe0fa79709caf2d`  
		Last Modified: Fri, 19 Jan 2024 00:53:20 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e43ba30f519a9895b5748d271b4087693ad594642ea09552574c1c66674c9b2`  
		Last Modified: Fri, 19 Jan 2024 00:53:20 GMT  
		Size: 267.1 KB (267089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf2d1083e81c7cf9288292f6e66b9c12bf3c45a2bdc3d2be054ba8f61ef7c8f`  
		Last Modified: Fri, 19 Jan 2024 00:53:20 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8570a1824708c698f0615156ddf6768e51ce8688d5bf880e076a2c1f812726`  
		Last Modified: Fri, 19 Jan 2024 00:54:02 GMT  
		Size: 518.3 MB (518294162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f85f4c02ceae76deb5609a1067cfd0eb1f8a09c7c14f190ef0840eb7565d2d`  
		Last Modified: Fri, 19 Jan 2024 00:53:19 GMT  
		Size: 101.6 KB (101578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5e8f1bb2e230fceaa3bd9b8ee14c6616a8c48c549e492d76eff685d826f219`  
		Last Modified: Fri, 19 Jan 2024 00:53:19 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cab4095b7199c3cf4569cdac7a23b7f4d0a3c29f6a7f6ac9190c3413c49e9b`  
		Last Modified: Fri, 19 Jan 2024 00:53:19 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699c06b5981a03720301fb7983a805796ce3548466d8a22910e9f68ae6bd8f69`  
		Last Modified: Fri, 19 Jan 2024 00:53:19 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull mongo@sha256:74a37284b2166e073d66fb73ebbbad5fa1d34981e548151cf06b78181f046c24
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.3 MB (623299762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4b5a6beec39808f1fc676e1bdb49fd17f03aa593f5e00c591de637e260d190`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Fri, 19 Jan 2024 00:51:38 GMT
SHELL [cmd /S /C]
# Fri, 19 Jan 2024 00:51:40 GMT
USER ContainerAdministrator
# Fri, 19 Jan 2024 00:51:46 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 19 Jan 2024 00:51:47 GMT
USER ContainerUser
# Fri, 19 Jan 2024 00:51:49 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Fri, 19 Jan 2024 00:51:50 GMT
ENV MONGO_VERSION=6.0.13
# Fri, 19 Jan 2024 00:52:23 GMT
COPY dir:52c8844300bd1267892ff953bada283f10975ec77346ef3bec4c64101fde69fa in C:\mongodb 
# Fri, 19 Jan 2024 00:52:30 GMT
RUN mongod --version
# Fri, 19 Jan 2024 00:52:31 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 19 Jan 2024 00:52:32 GMT
EXPOSE 27017
# Fri, 19 Jan 2024 00:52:34 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fa0f2d5d7efe5323a3dbce4c59236d5a7566b9eb9dbb4c83f8fa412a8f3a29`  
		Last Modified: Fri, 19 Jan 2024 00:52:43 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934c2c260ef9928f4911ed48096e3b541bca43245c4aae42aaa5afa834a80153`  
		Last Modified: Fri, 19 Jan 2024 00:52:43 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8acf197d8166e97185ed3c8b021c7019cd6f1753c755233087169adbf72e84`  
		Last Modified: Fri, 19 Jan 2024 00:52:41 GMT  
		Size: 69.2 KB (69185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0250a9ee65d848570216498f2545f543ba444dd07cba1a98850e3a94c05ab5`  
		Last Modified: Fri, 19 Jan 2024 00:52:41 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafc1a63786e21d60a9a9321c681bb0b3dbf624aa1c8b1cec59ea11969573b6f`  
		Last Modified: Fri, 19 Jan 2024 00:52:41 GMT  
		Size: 267.1 KB (267091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d170b34dcd85fb84fc3142d047c4daba5960db81051cc53940bcf1e398cc0eca`  
		Last Modified: Fri, 19 Jan 2024 00:52:40 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1b1a3d43ae536580adfedecbb5c0a02a3774b94cdd9c46125ac9ac987d8c7a`  
		Last Modified: Fri, 19 Jan 2024 00:53:21 GMT  
		Size: 518.3 MB (518294344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bedf00e8c882c3c4d94ac6e2c9bd08ac4901bbb512589c73497ec2113857306`  
		Last Modified: Fri, 19 Jan 2024 00:52:39 GMT  
		Size: 70.5 KB (70484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faeac13654d4819c01480feef8024f1117c32336bbbde1997bdd7a68579b74e`  
		Last Modified: Fri, 19 Jan 2024 00:52:38 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313b2980b8478af7bc8909b0e4f821a3bdf062b7d74eff6dc6c9f96cd58aba37`  
		Last Modified: Fri, 19 Jan 2024 00:52:38 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e491a1f607873672500837b04970700b743295b724136025c2d091971f239bec`  
		Last Modified: Fri, 19 Jan 2024 00:52:39 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
