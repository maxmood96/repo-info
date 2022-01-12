## `mongo:4-nanoserver`

```console
$ docker pull mongo@sha256:61604a3306fb650c1acf8e3f99568946f22ab42f8666b82882d935f5469e3e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.469; amd64
	-	windows version 10.0.17763.2452; amd64

### `mongo:4-nanoserver` - windows version 10.0.20348.469; amd64

```console
$ docker pull mongo@sha256:112e0de940582c680b1e393d0a905ee36637fb05582cfbadfe61af467d6afd7d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351125963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f9c0a0fac33a99fb05043cd19c14a22ab2a0d1c6b342ac0170582020064e9a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 06 Jan 2022 03:34:42 GMT
RUN Apply image ltsc2022-amd64
# Tue, 11 Jan 2022 23:41:02 GMT
SHELL [cmd /S /C]
# Wed, 12 Jan 2022 03:49:41 GMT
USER ContainerAdministrator
# Wed, 12 Jan 2022 03:50:28 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 12 Jan 2022 03:50:29 GMT
USER ContainerUser
# Wed, 12 Jan 2022 03:50:31 GMT
COPY multi:0196f9e96f60ad3e2b92fd0773f8d0fe3a8235e1eefbb9ef1a1f0d672e6a711c in C:\Windows\System32\ 
# Wed, 12 Jan 2022 04:19:05 GMT
ENV MONGO_VERSION=4.4.11
# Wed, 12 Jan 2022 04:19:41 GMT
COPY dir:ac3dcf0e6bbeecc23af1858c2ccb3c1b4355678709a4966921cec081dbebc530 in C:\mongodb 
# Wed, 12 Jan 2022 04:20:06 GMT
RUN mongo --version && mongod --version
# Wed, 12 Jan 2022 04:20:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Jan 2022 04:20:08 GMT
EXPOSE 27017
# Wed, 12 Jan 2022 04:20:08 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:b2bb136f79c12b0a42720d7bb83469bce3f7bf2ca5c8bc68a36228796311fc6b`  
		Size: 117.3 MB (117334348 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:84b025a23a2f3c592a35a160efcc06650fd18dc74fa4fbd5e7fbab2861137597`  
		Last Modified: Wed, 12 Jan 2022 00:36:05 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d530c5dcdde9ccc187c814e1c756a5954a2b2234e57c33573cc7a722390ad14`  
		Last Modified: Wed, 12 Jan 2022 17:19:33 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413cefb3d6a1e3f810ef6a7b7b735827aa4340e30ec20bc7dd007e0650671534`  
		Last Modified: Wed, 12 Jan 2022 17:19:31 GMT  
		Size: 84.2 KB (84202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6da08c86901749341212927c40cdffa01fcb5fb9d38741ab1239cba6c783b8`  
		Last Modified: Wed, 12 Jan 2022 17:19:31 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899b12b3ff3c6626620bff4e712fd0e7e2cee8326812cea0ff96b0722f635098`  
		Last Modified: Wed, 12 Jan 2022 17:19:31 GMT  
		Size: 274.1 KB (274113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99e4f8b3dc2428e967af8c4824b96a05bb145b64d8fc42d3209570245926761`  
		Last Modified: Wed, 12 Jan 2022 17:48:53 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2dbb590f405b9536fd13cee51e28e2ab81d32978c38fd0538d4d381d79fdef`  
		Last Modified: Wed, 12 Jan 2022 17:49:34 GMT  
		Size: 233.4 MB (233371623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2558a056eccb08cc2e2113f2be1fb0bfb881e2ab5754be8fe204ab953f90fe6d`  
		Last Modified: Wed, 12 Jan 2022 17:48:50 GMT  
		Size: 53.5 KB (53518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5526a503979dc7fa15356976079f91af913df789b8d809afc48278546aaa1cb5`  
		Last Modified: Wed, 12 Jan 2022 17:48:50 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5cbf5bd671c997d4f06c2670f553baa6fb15dc516259c596374a3e99d8c345`  
		Last Modified: Wed, 12 Jan 2022 17:48:50 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85ecc8c5fcfed3999e247840fef3f8195b3897bf25b6ed473bf0817fe5ce472`  
		Last Modified: Wed, 12 Jan 2022 17:48:50 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-nanoserver` - windows version 10.0.17763.2452; amd64

```console
$ docker pull mongo@sha256:3565184aae4281750f8d9bb23854432f0e95b99f1f2a22e4fd333f0c39eb95ac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336819453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6330ad1f2a581809c3e236ae884a4ce3b24d6d01592e00e7e7e56fef29cb804d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 13:19:53 GMT
SHELL [cmd /S /C]
# Wed, 12 Jan 2022 16:41:35 GMT
USER ContainerAdministrator
# Wed, 12 Jan 2022 16:41:49 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 12 Jan 2022 16:41:50 GMT
USER ContainerUser
# Wed, 12 Jan 2022 16:41:51 GMT
COPY multi:0196f9e96f60ad3e2b92fd0773f8d0fe3a8235e1eefbb9ef1a1f0d672e6a711c in C:\Windows\System32\ 
# Wed, 12 Jan 2022 16:52:34 GMT
ENV MONGO_VERSION=4.4.11
# Wed, 12 Jan 2022 16:53:38 GMT
COPY dir:ac3dcf0e6bbeecc23af1858c2ccb3c1b4355678709a4966921cec081dbebc530 in C:\mongodb 
# Wed, 12 Jan 2022 16:53:50 GMT
RUN mongo --version && mongod --version
# Wed, 12 Jan 2022 16:53:51 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Jan 2022 16:53:52 GMT
EXPOSE 27017
# Wed, 12 Jan 2022 16:53:53 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2e33ce14c030f51993f87b8caf6fcbc38d7e0c720e938c28109df0cc1fcecc69`  
		Last Modified: Wed, 12 Jan 2022 13:45:07 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8939f342fed44c2788bbad268cc1694d0f7847a41cfe6de812fcddbe3bfa5b1d`  
		Last Modified: Wed, 12 Jan 2022 17:25:09 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63721e629e6b8e03acc500ea84ead467fb1d34524b70a07e8f1aee67bc571055`  
		Last Modified: Wed, 12 Jan 2022 17:25:07 GMT  
		Size: 78.0 KB (78013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fc02788fb3893cd4e6cde670b7e4bb3af946e8912d384ebf2ed584cdd09e50`  
		Last Modified: Wed, 12 Jan 2022 17:25:07 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a88a4399879d6cc0c2bab8adf64257dde87a874c8af0abefeaf548b55d55c0`  
		Last Modified: Wed, 12 Jan 2022 17:25:08 GMT  
		Size: 274.1 KB (274092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a16e2bec3385ef13274dd891527ad20127fe919ce4f13794ec737d2109947cf`  
		Last Modified: Wed, 12 Jan 2022 17:49:51 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6e1628b77c8f65f8dd1a2884cf1293d598cbe7e91f6dfcc6f50c2c5a845131`  
		Last Modified: Wed, 12 Jan 2022 17:54:05 GMT  
		Size: 233.4 MB (233371567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37d68b398b35476f6a5d7b9f58f480b45ad754ceefbdaf73aeb62d8a7cebba7`  
		Last Modified: Wed, 12 Jan 2022 17:49:49 GMT  
		Size: 56.7 KB (56652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69bd6183254674ca145b7541e2d21f18295c078ec776d30f675b7b196e350dd8`  
		Last Modified: Wed, 12 Jan 2022 17:49:49 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a3df18e2d7b0d65f0ae820984c7d8127ab00a455c7f748800db9b3342fe69d`  
		Last Modified: Wed, 12 Jan 2022 17:49:49 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faed5261ca50cccf33a90d380a4a3609150e0f270cfe545ce4e4ebf3e20c5fd`  
		Last Modified: Wed, 12 Jan 2022 17:49:48 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
