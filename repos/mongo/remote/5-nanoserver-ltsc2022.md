## `mongo:5-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:fa93c659719e7e06c5bf8b86c4b6eeb56d68bba2ea8205f31ac47da687811e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2031; amd64

### `mongo:5-nanoserver-ltsc2022` - windows version 10.0.20348.2031; amd64

```console
$ docker pull mongo@sha256:b6ed83e522e591074629e2c0a82b72089be8f9b5298eeb41d74d484dca37bfc8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.7 MB (433718446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7574c101eddd5197acc833684865cf3697f1d9c6f3c6bc8a136751bde0f70d`
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
# Thu, 26 Oct 2023 23:27:42 GMT
ENV MONGO_VERSION=5.0.22
# Thu, 26 Oct 2023 23:28:06 GMT
COPY dir:5301d798ae71e503900361fe1355b6f3d344b80ef6d1feeca771e6bc301bbcc9 in C:\mongodb 
# Thu, 26 Oct 2023 23:28:19 GMT
RUN mongo --version && mongod --version
# Thu, 26 Oct 2023 23:28:19 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 26 Oct 2023 23:28:20 GMT
EXPOSE 27017
# Thu, 26 Oct 2023 23:28:21 GMT
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
	-	`sha256:56e641cc27f7d3890f32dd35ce399ea71a255590bb4690eaf1f990b692447ee0`  
		Last Modified: Thu, 26 Oct 2023 23:39:06 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf10e01064a05bddb97099339aaf8356a1be752f57a1634b8db351fa1ee10d5`  
		Last Modified: Thu, 26 Oct 2023 23:39:49 GMT  
		Size: 312.7 MB (312704818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f72c8d6736a7b82b4c4b5da1596a7ce851c132aba41b663316aef08520e030`  
		Last Modified: Thu, 26 Oct 2023 23:39:04 GMT  
		Size: 50.8 KB (50771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab58efdd32bb5df69abfa5cf8413baea4676a28d5aae39a538d77b4471ee8a24`  
		Last Modified: Thu, 26 Oct 2023 23:39:04 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c776a0f25dcaad253966bbbe9ba6e2fed3417a8b67fb039a5f2fcb54692cae`  
		Last Modified: Thu, 26 Oct 2023 23:39:04 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3671fe27b42154def621f7978b84e394e9a48f24627643ee9832d9390a932708`  
		Last Modified: Thu, 26 Oct 2023 23:39:04 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
