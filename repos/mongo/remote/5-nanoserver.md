## `mongo:5-nanoserver`

```console
$ docker pull mongo@sha256:d76e52a774374d2a1cd0e18bf96bc72b2bbddac7ac9b7f280966df94780e06f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.469; amd64
	-	windows version 10.0.17763.2452; amd64

### `mongo:5-nanoserver` - windows version 10.0.20348.469; amd64

```console
$ docker pull mongo@sha256:ed01a95e490be6bf715d4df0fc25b36389c33b82122b8dec59271cbbf989abf3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 MB (411698508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7afd91c7aabdc25dedb47db9654272407f764717d3c8bf126419f1e2697b6fc`
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
# Wed, 12 Jan 2022 03:50:32 GMT
ENV MONGO_VERSION=5.0.5
# Wed, 12 Jan 2022 03:51:31 GMT
COPY dir:97e0851993a8443e809dbfb982fa612becf2ad4c3b07d76c242613492af3987d in C:\mongodb 
# Wed, 12 Jan 2022 03:52:16 GMT
RUN mongo --version && mongod --version
# Wed, 12 Jan 2022 03:52:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Jan 2022 03:52:18 GMT
EXPOSE 27017
# Wed, 12 Jan 2022 03:52:19 GMT
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
	-	`sha256:5cf0d61f8561205c67ce6bc918e1f6bd8be58a109af91b4f7e0b12a5987bf4fb`  
		Last Modified: Wed, 12 Jan 2022 17:19:31 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50894e504ae0bd845c46886b1a71e1378465bef6e0072e91b735b32eb67dc13`  
		Last Modified: Wed, 12 Jan 2022 17:24:46 GMT  
		Size: 293.9 MB (293936065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc890bdd69de84c932d6dfedd8c37c1b8309f3ff01d347041310c7a214e51a46`  
		Last Modified: Wed, 12 Jan 2022 17:19:28 GMT  
		Size: 61.7 KB (61657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f026b563de3429f6010f35d5959ccb28f8f3467f6078938df2bd801a6e9ff6e`  
		Last Modified: Wed, 12 Jan 2022 17:19:28 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5edd04b4e6759daeabb00fddfbf7f6a6ea9d5de2ec4f25c39a2cb45607b80d8`  
		Last Modified: Wed, 12 Jan 2022 17:19:28 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbc91ad553cbccd3e1598ced0503c66b9078bb44aeace80827a221ba75127e9`  
		Last Modified: Wed, 12 Jan 2022 17:19:28 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-nanoserver` - windows version 10.0.17763.2452; amd64

```console
$ docker pull mongo@sha256:eebf90422ba916295734cdded5ee55922b3392d8bb799244b982fa4a1f802ad8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.4 MB (397383282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38315907dadb66386570c1e30cc34fc1c9c728c5397af3bfe951fa2359a1ec8a`
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
# Wed, 12 Jan 2022 16:41:52 GMT
ENV MONGO_VERSION=5.0.5
# Wed, 12 Jan 2022 16:42:54 GMT
COPY dir:97e0851993a8443e809dbfb982fa612becf2ad4c3b07d76c242613492af3987d in C:\mongodb 
# Wed, 12 Jan 2022 16:43:23 GMT
RUN mongo --version && mongod --version
# Wed, 12 Jan 2022 16:43:23 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Jan 2022 16:43:24 GMT
EXPOSE 27017
# Wed, 12 Jan 2022 16:43:25 GMT
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
	-	`sha256:f26ff52f41e6e5cf10bc32d02cf5b256313640fc2c63d393f15b155a659d54ab`  
		Last Modified: Wed, 12 Jan 2022 17:25:07 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2834e1812062ff311f8eac7e241e4f127e9f023e135b2b5e9ed1907469506e`  
		Last Modified: Wed, 12 Jan 2022 17:26:00 GMT  
		Size: 293.9 MB (293935599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e53ae1ba79385eef9fa16ae869c79f9e25bf58d4a93e3b083b5c903d541c92`  
		Last Modified: Wed, 12 Jan 2022 17:25:05 GMT  
		Size: 56.4 KB (56413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8606ce1d48e9b3480e78b4b04e60aa5feb204b1469da58a243ec42da400292ca`  
		Last Modified: Wed, 12 Jan 2022 17:25:05 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f57ae8dfa2915dc1d045cd82db139d00d2c8040bcd657ff4577de1f622e6e7`  
		Last Modified: Wed, 12 Jan 2022 17:25:05 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f91678718fc4bab28fe07ba582efc1a9e3aefd80518b70766726c19516cb4d`  
		Last Modified: Wed, 12 Jan 2022 17:25:05 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
