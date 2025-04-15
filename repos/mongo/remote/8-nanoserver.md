## `mongo:8-nanoserver`

```console
$ docker pull mongo@sha256:1f4eb57c9a833b94c9cb54d3c16105a4418b801d7d4fadd0e9cdd5f0a3c56bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `mongo:8-nanoserver` - windows version 10.0.20348.3453; amd64

```console
$ docker pull mongo@sha256:24f46d659308aeef03a4215462e9993a696d414e615b3b78fa6afe0e5ed065be
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **890.4 MB (890399800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3506c92466e8b309b34179ee32cb65dadd12ba036f0701357592307a9c1ac250`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Tue, 15 Apr 2025 00:10:19 GMT
SHELL [cmd /S /C]
# Tue, 15 Apr 2025 00:10:20 GMT
USER ContainerAdministrator
# Tue, 15 Apr 2025 00:10:23 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 15 Apr 2025 00:10:24 GMT
USER ContainerUser
# Tue, 15 Apr 2025 00:10:25 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Tue, 15 Apr 2025 00:10:26 GMT
ENV MONGO_VERSION=8.0.8
# Tue, 15 Apr 2025 00:10:55 GMT
COPY dir:72b416844fc933841484cbf4a72c928cbc4d580829e8d356764afc081e298d11 in C:\mongodb 
# Tue, 15 Apr 2025 00:11:15 GMT
RUN mongod --version
# Tue, 15 Apr 2025 00:11:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 15 Apr 2025 00:11:17 GMT
EXPOSE 27017
# Tue, 15 Apr 2025 00:11:18 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4e49cb58110b58afd8986041d90e0a447e3d24a6d2aed369a7064a152b02f1`  
		Last Modified: Tue, 15 Apr 2025 00:11:26 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6161c4a46194ab68c66e943153f32265132460338836b65ecbeff0cd8e9e707f`  
		Last Modified: Tue, 15 Apr 2025 00:11:26 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff50389f6e60cbbab606c2db40011c194d8081635c13ea96da5def026bf3efcb`  
		Last Modified: Tue, 15 Apr 2025 00:11:24 GMT  
		Size: 76.8 KB (76753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dab6eda93ac8dc7f0ab9083d39fff76935ddaed92f09af8b431dfa4e7db1e1b`  
		Last Modified: Tue, 15 Apr 2025 00:11:24 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0712906d94597be9398d3851b3b5c10e1003e6caef14cce4f1ef1992571ec445`  
		Last Modified: Tue, 15 Apr 2025 00:11:24 GMT  
		Size: 275.2 KB (275167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3552485b2aa54b8cfc993a0da96d986c177dc296c4fcbd859f35a5ace20f3ac7`  
		Last Modified: Tue, 15 Apr 2025 00:11:24 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa886b6529832183df0555fc1622e3c96c3ee5286c5fa8a81daea83648bab78e`  
		Last Modified: Tue, 15 Apr 2025 00:12:21 GMT  
		Size: 769.2 MB (769212396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2cce06f560106b64e45545cc388b1fb8d7e1274b280e1eae43fcb546274862`  
		Last Modified: Tue, 15 Apr 2025 00:11:22 GMT  
		Size: 91.9 KB (91897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3b34028ea6d3bbd42fde768c6bbd386a9343cd712c561d2320fa704a9c810f`  
		Last Modified: Tue, 15 Apr 2025 00:11:22 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fe1cad9ff2242ced0dbcdc7684cef9cacefff462e788882087e3402445048b`  
		Last Modified: Tue, 15 Apr 2025 00:11:22 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425dca41e4f617d040b24cd44b34b7d1d16657273a8834d10059d5a00d0a605e`  
		Last Modified: Tue, 15 Apr 2025 00:11:22 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:8-nanoserver` - windows version 10.0.17763.7136; amd64

```console
$ docker pull mongo@sha256:4afe5ac07a06043354e13e706ea4e4e5967a119ddea29e160d01c7f5293501c6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **876.6 MB (876554481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ed2d0a70e3d4b63861f2ffb64fe881abb1a6980a5e4e6f1a91869dff5cf7a9`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Tue, 15 Apr 2025 00:09:03 GMT
SHELL [cmd /S /C]
# Tue, 15 Apr 2025 00:09:04 GMT
USER ContainerAdministrator
# Tue, 15 Apr 2025 00:09:05 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 15 Apr 2025 00:09:06 GMT
USER ContainerUser
# Tue, 15 Apr 2025 00:09:07 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Tue, 15 Apr 2025 00:09:07 GMT
ENV MONGO_VERSION=8.0.8
# Tue, 15 Apr 2025 00:09:41 GMT
COPY dir:72b416844fc933841484cbf4a72c928cbc4d580829e8d356764afc081e298d11 in C:\mongodb 
# Tue, 15 Apr 2025 00:10:01 GMT
RUN mongod --version
# Tue, 15 Apr 2025 00:10:01 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 15 Apr 2025 00:10:02 GMT
EXPOSE 27017
# Tue, 15 Apr 2025 00:10:02 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2e3e5bb27ca35f0cd2c7a52eaf7fadca82aafe4e73486351f5a786ec22c2b8`  
		Last Modified: Tue, 15 Apr 2025 00:10:10 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b59974b22ba8f721042afec3bb9cd0f67836ed186e3d2506e983573bb4ddbf`  
		Last Modified: Tue, 15 Apr 2025 00:10:10 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af034ba57e315c66745e057c84b0f07ee6583288a0c85e2678257ea8083dfd1a`  
		Last Modified: Tue, 15 Apr 2025 00:10:08 GMT  
		Size: 68.8 KB (68805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98407ff05550f8646d0d85c914640b43f44b2d48a9b23b102b6ab3c341dfb3fc`  
		Last Modified: Tue, 15 Apr 2025 00:10:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2923bac23202cf52318510d338f5b0b900fde612cd0ce5ef42c2405e06be1a`  
		Last Modified: Tue, 15 Apr 2025 00:10:08 GMT  
		Size: 275.2 KB (275156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea3ab4c98427642f7d316919b1c3331b3a89c604ebbec031b46528d321c2be4`  
		Last Modified: Tue, 15 Apr 2025 00:10:08 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf77d0e6cc019b2509972ab4543ce63b9c225eb491eb7108f9bf181f1c9d4f6`  
		Last Modified: Tue, 15 Apr 2025 00:11:06 GMT  
		Size: 769.2 MB (769212481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6044ea01fd881b6b30f771706cd5e3d1d80d6b2f5084c46373c1a48f2a52dbbc`  
		Last Modified: Tue, 15 Apr 2025 00:10:06 GMT  
		Size: 68.3 KB (68317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b725ac0aeaf5d1c51f9866ab45fd4671e24e48ed848f4ad759ecd6fd6c7946ca`  
		Last Modified: Tue, 15 Apr 2025 00:10:06 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de3044ab2ed4c04666da1389ecfbe5d0b1b7d07b9c74de8951cdc37f2d79a8b`  
		Last Modified: Tue, 15 Apr 2025 00:10:06 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df272441af84dfdb0d728d699ead44fb037f384fe9fb82439eca334c1bfbe68b`  
		Last Modified: Tue, 15 Apr 2025 00:10:06 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
