## `mongo:5-nanoserver`

```console
$ docker pull mongo@sha256:a006cb11f9bb8ff9e0921e19e3e4dad2ee585035727415e96eee7337eeb9aa37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2031; amd64
	-	windows version 10.0.17763.4974; amd64

### `mongo:5-nanoserver` - windows version 10.0.20348.2031; amd64

```console
$ docker pull mongo@sha256:814502de4e26aa87391468e24bd2196d23da88475c82a5a3fbf2b206d1cf3f89
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.2 MB (433242596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e091ea9fc932bb8908da3fa3aac6dcb021b0b340fbf24d899b7b91eb9ae0730`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 06 Oct 2023 21:30:39 GMT
RUN Apply image 10.0.20348.2031
# Wed, 11 Oct 2023 02:28:41 GMT
SHELL [cmd /S /C]
# Wed, 11 Oct 2023 03:03:40 GMT
USER ContainerAdministrator
# Wed, 11 Oct 2023 03:04:28 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 11 Oct 2023 03:04:29 GMT
USER ContainerUser
# Wed, 11 Oct 2023 03:22:56 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 11 Oct 2023 03:22:56 GMT
ENV MONGO_VERSION=5.0.21
# Wed, 11 Oct 2023 03:23:23 GMT
COPY dir:7c782df2b40da2daccf2a126d1d94993a3ddaf542b20f3f16bea7641546b87ea in C:\mongodb 
# Wed, 11 Oct 2023 03:23:36 GMT
RUN mongo --version && mongod --version
# Wed, 11 Oct 2023 03:23:37 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Oct 2023 03:23:38 GMT
EXPOSE 27017
# Wed, 11 Oct 2023 03:23:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:fff54800e03713ba81736f43d985319592fc643a1a32b62dbd5c0ec36549de00`  
		Last Modified: Tue, 10 Oct 2023 17:30:43 GMT  
		Size: 120.6 MB (120604344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cd425f94dc5addd6f49003c495c9acbf2a61ab29ca68946c6cd056ed33c5f6`  
		Last Modified: Wed, 11 Oct 2023 02:48:05 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c5d8a4d1b8dd712544f618c2e6ee6be0146ea27a9e28326d8d91f8bd6fa8a0`  
		Last Modified: Wed, 11 Oct 2023 07:41:29 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2c9710a873f77c9b8cdf8f8359453db5ea2693415cdcd182e0478772b06b5f`  
		Last Modified: Wed, 11 Oct 2023 07:41:28 GMT  
		Size: 87.1 KB (87090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e705c53faad5aaf4367e374cfed21b9e0b718d308280d68adb51337227f65b`  
		Last Modified: Wed, 11 Oct 2023 07:41:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ea7423ef5c85bc963972b957ec3d2c304199cb73f633cb0ba6b514f5c9a0c0`  
		Last Modified: Wed, 11 Oct 2023 07:51:56 GMT  
		Size: 263.4 KB (263365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3617519ea906f6f1e68a90ed0017d0ab68e50ea46a9cb50444a1554e569b63b3`  
		Last Modified: Wed, 11 Oct 2023 07:51:55 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15f47d45a797291acc2900a2167c6308bdc61f9c5bfd9e737421d80c5e12508`  
		Last Modified: Wed, 11 Oct 2023 07:52:40 GMT  
		Size: 312.2 MB (312221481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a244b74e5e6f0366afe314ca9faad8129c17925b4a19b21e84e88f58cd186f60`  
		Last Modified: Wed, 11 Oct 2023 07:51:54 GMT  
		Size: 58.5 KB (58535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73e516c9eaf22bb72383482121e42bd8f3935867f945f10b61789567f0e202e`  
		Last Modified: Wed, 11 Oct 2023 07:51:54 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100b5e70571f70978799e916b173aedd1b46e88eeb465db0861fbb31cb84b2af`  
		Last Modified: Wed, 11 Oct 2023 07:51:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c5bdf90f37db69a5fc86495935f11815e5e970554d0b624fe7a3ff0abb9ed4`  
		Last Modified: Wed, 11 Oct 2023 07:51:54 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-nanoserver` - windows version 10.0.17763.4974; amd64

```console
$ docker pull mongo@sha256:e9d8e9528175948fde70655283f9af71068f7526009903087baac41ea539dcb4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.1 MB (417107780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd3183f3b3f4ec78ed87e33a1538b33cead2e8a2d062fc350707029bbcca488`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 02:31:25 GMT
SHELL [cmd /S /C]
# Wed, 11 Oct 2023 03:06:25 GMT
USER ContainerAdministrator
# Wed, 11 Oct 2023 03:06:58 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 11 Oct 2023 03:06:59 GMT
USER ContainerUser
# Wed, 11 Oct 2023 03:23:49 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 11 Oct 2023 03:23:50 GMT
ENV MONGO_VERSION=5.0.21
# Wed, 11 Oct 2023 03:24:15 GMT
COPY dir:7c782df2b40da2daccf2a126d1d94993a3ddaf542b20f3f16bea7641546b87ea in C:\mongodb 
# Wed, 11 Oct 2023 03:24:28 GMT
RUN mongo --version && mongod --version
# Wed, 11 Oct 2023 03:24:29 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Oct 2023 03:24:30 GMT
EXPOSE 27017
# Wed, 11 Oct 2023 03:24:31 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1d090bf86f6024502bc8f94ffdf6082818dc40adde892065acecc65617301f`  
		Last Modified: Wed, 11 Oct 2023 02:48:49 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884f2cb9b5edcbbf4b0b83f11a2ca9e93da04c86243865ff1f331445db9abcf3`  
		Last Modified: Wed, 11 Oct 2023 07:43:05 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7c6a1f7c9281c4d2be3cef0ad78603721509d8a2a8f6bc3411192f8112c273`  
		Last Modified: Wed, 11 Oct 2023 07:43:04 GMT  
		Size: 69.0 KB (69002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3529e287318b8e986a6ed2518bcd876b733f1577a5c44c2528bbc77778272a`  
		Last Modified: Wed, 11 Oct 2023 07:43:04 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77a817fbce4ee96b93831883b25e1627d9ddb429929338e362a0c881b44b383`  
		Last Modified: Wed, 11 Oct 2023 07:52:54 GMT  
		Size: 263.4 KB (263368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f345fed7701f8bd8cedbb026cc7b190ec99efc00f69aad5d4670101f1edae3`  
		Last Modified: Wed, 11 Oct 2023 07:52:54 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097618d9d6bb52c944a0d48b13f8f851c5bc90192fc87b4d59306833955b3750`  
		Last Modified: Wed, 11 Oct 2023 07:53:39 GMT  
		Size: 312.2 MB (312221441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ee943cc71730c394665202890962d6561fcfb4498e4d2483738a4b9ef37c82`  
		Last Modified: Wed, 11 Oct 2023 07:52:52 GMT  
		Size: 81.5 KB (81479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96eedb2d8db73094fb01477c90654cdeae4ba60f3c8f2a7dae667834aafe7728`  
		Last Modified: Wed, 11 Oct 2023 07:52:52 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a793ca68408c2cbea31ec9ac62eaa59ea6d2e642d7acf41bbe63ef023c1406a`  
		Last Modified: Wed, 11 Oct 2023 07:52:52 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea92e6740ad9c7f24033d0e66eb059a6ce132360c09b6d889bcf7c4d9980ab8`  
		Last Modified: Wed, 11 Oct 2023 07:52:52 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
