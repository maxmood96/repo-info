## `mongo:nanoserver`

```console
$ docker pull mongo@sha256:7df6e6cd5b913adb567d7350544dc5eac8342a50332ff7d0225652f9968134d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `mongo:nanoserver` - windows version 10.0.20348.2966; amd64

```console
$ docker pull mongo@sha256:ed45f679c369dea24e1915955096988c4011d50ba4d6d2734328d8eee3479c01
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **888.7 MB (888658409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995a0d6e9e1f1b217e9d8f10ecad0ac05b770815a71883cf069e9901f71f86af`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 05 Dec 2024 01:18:54 GMT
RUN Apply image 10.0.20348.2966
# Wed, 11 Dec 2024 21:50:59 GMT
SHELL [cmd /S /C]
# Wed, 11 Dec 2024 21:51:01 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:51:05 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 11 Dec 2024 21:51:06 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:51:07 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 11 Dec 2024 21:51:08 GMT
ENV MONGO_VERSION=8.0.4
# Wed, 11 Dec 2024 21:51:37 GMT
COPY dir:0009924507cd67bb774ae279cf5a575db39e491af9c3c9f55c5a3622f7b63de5 in C:\mongodb 
# Wed, 11 Dec 2024 21:52:04 GMT
RUN mongod --version
# Wed, 11 Dec 2024 21:52:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2024 21:52:07 GMT
EXPOSE 27017
# Wed, 11 Dec 2024 21:52:07 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:f9d5d5ca3244fc2c429a892cbe6066394790f649f32d59acfdf012e490896378`  
		Last Modified: Tue, 10 Dec 2024 18:34:17 GMT  
		Size: 120.6 MB (120601318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecaee4e66d95de842811b5caa848520e9d752e5e85247e4ddd1c7ba45339c053`  
		Last Modified: Wed, 11 Dec 2024 21:52:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9277398e17bc477b283c58e96fb5b4b7b5687880739d1c37420984c277eea5e9`  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc47d9119c5b504bc69eca745d436b124d4676e4265e5392b8c073a9450b5215`  
		Last Modified: Wed, 11 Dec 2024 21:52:11 GMT  
		Size: 77.9 KB (77876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97df6a819eaf2d785bd11b0ee501843fc16712b125484ab160bd05b879f3fab9`  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943c0b3a3744d898f3e84837d6fa507b5b07b4c9b5b8a1cfd1546f0167e84c2b`  
		Size: 275.2 KB (275168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bce1cace186477b024a2e287892f38134257cb9c6729cb71da5838c84f062ee`  
		Last Modified: Wed, 11 Dec 2024 21:52:10 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faed4b2feb0d19ba63a0d89c3765763ba94dcf3810668a301b66ba884e3ac02`  
		Last Modified: Wed, 11 Dec 2024 21:53:08 GMT  
		Size: 767.6 MB (767598296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56436d310ae63deebfea056c16fb1ff693437b7bc7129e116948a76221957f5e`  
		Last Modified: Wed, 11 Dec 2024 21:52:09 GMT  
		Size: 98.5 KB (98452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:504f41d013e9da3776127b43408e6db400da1f18b2d7e6990808a22805bcff51`  
		Last Modified: Wed, 11 Dec 2024 21:52:09 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b07ecfc44dcde67e777e3f6526028d0d142f77e4560cb94da30afbe484638a1`  
		Last Modified: Wed, 11 Dec 2024 21:52:09 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e13b731cbec4c32cf07fa15fc7a92689912b0a3b3fe69d63743688094c9384`  
		Last Modified: Wed, 11 Dec 2024 21:52:09 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:nanoserver` - windows version 10.0.17763.6659; amd64

```console
$ docker pull mongo@sha256:ecad001d530c00bccc88013e0d7632c891fc5db14c39ae14510e3434b938c362
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **923.3 MB (923250638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73aee6dd6f9e1f07bfaa7ea78a41a5974fa73ec4eaea631280ccb2ef125ffa39`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Wed, 11 Dec 2024 21:48:04 GMT
SHELL [cmd /S /C]
# Wed, 11 Dec 2024 21:48:05 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:48:07 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 11 Dec 2024 21:48:07 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:48:09 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 11 Dec 2024 21:48:09 GMT
ENV MONGO_VERSION=8.0.4
# Wed, 11 Dec 2024 21:48:37 GMT
COPY dir:0009924507cd67bb774ae279cf5a575db39e491af9c3c9f55c5a3622f7b63de5 in C:\mongodb 
# Wed, 11 Dec 2024 21:48:58 GMT
RUN mongod --version
# Wed, 11 Dec 2024 21:48:59 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2024 21:49:00 GMT
EXPOSE 27017
# Wed, 11 Dec 2024 21:49:00 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56da3568049e293ca29748ba43bc5b90272cb073059165197ac6d6e7679863c4`  
		Last Modified: Wed, 11 Dec 2024 21:49:05 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59b03b08c516411d75bc65d53dd93f08bdb239e8865ecd83a4f317dfea10503`  
		Last Modified: Wed, 11 Dec 2024 21:49:05 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26efbcd312b11b91af6d31524c72bbd12a6ef7b3ccae7cd78f8a5f67f710fb08`  
		Last Modified: Wed, 11 Dec 2024 21:49:04 GMT  
		Size: 69.5 KB (69531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d29472bbeac7e98eec7ec515172ff93bc20e10d1a0eb942f8327be49886071`  
		Last Modified: Wed, 11 Dec 2024 21:49:04 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b44c8d70efbbc9410ffbc8dff08801b7e638ef7198ede201e5af539193ab917`  
		Last Modified: Wed, 11 Dec 2024 21:49:04 GMT  
		Size: 275.2 KB (275173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e909cf2bc311d50374fff8c808340505297453234eb5f3d6a5913aae043ab6f`  
		Last Modified: Wed, 11 Dec 2024 21:49:04 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2911261382fda13ebcd9cc83487abd743e93b8f45dbcabbe3cc726f4e763948`  
		Last Modified: Wed, 11 Dec 2024 21:50:03 GMT  
		Size: 767.6 MB (767598466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd570f9aa8de1ffc4056af61769c7e9d505199e13e2b5bfd0b29c1c73d1e5e9`  
		Last Modified: Wed, 11 Dec 2024 21:49:03 GMT  
		Size: 68.6 KB (68580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a51fecfa831820d39d72d946fb2664cc8ee1e5063eebfc4df49bed679b5f785`  
		Last Modified: Wed, 11 Dec 2024 21:49:03 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5149a8d5c25a90301d1b114f597139df8beb29fef1632444b1af24f755dc0d42`  
		Last Modified: Wed, 11 Dec 2024 21:49:03 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829f35777242d61e6d4536ce8a713c68323287b991f992b97783355ab3a8fbb4`  
		Last Modified: Wed, 11 Dec 2024 21:49:03 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
