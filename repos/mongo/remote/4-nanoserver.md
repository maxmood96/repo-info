## `mongo:4-nanoserver`

```console
$ docker pull mongo@sha256:1fbc1808fa498a867f8cd0351d20fd7c00d80f21579177b1f8cbdd131c32cce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.768; amd64
	-	windows version 10.0.17763.3046; amd64

### `mongo:4-nanoserver` - windows version 10.0.20348.768; amd64

```console
$ docker pull mongo@sha256:5527f0902e3decf9698bf63e35cbd1f5a10c812e6942462d02426c0fc3cd85c7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359887271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07354b7425a93f95a4d6c15bd106e102954fc4b470ba80ea858a3381a3fe05c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Jun 2022 04:10:14 GMT
RUN Apply image 10.0.20348.768
# Wed, 15 Jun 2022 13:13:03 GMT
SHELL [cmd /S /C]
# Wed, 15 Jun 2022 21:07:33 GMT
USER ContainerAdministrator
# Wed, 15 Jun 2022 21:07:49 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 15 Jun 2022 21:07:50 GMT
USER ContainerUser
# Wed, 15 Jun 2022 21:07:51 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 15 Jun 2022 21:14:45 GMT
ENV MONGO_VERSION=4.4.14
# Wed, 15 Jun 2022 21:15:09 GMT
COPY dir:5db4d92801abb4c6b6f16e80c283eda3a5fdc6431914dfb8699f556acea891c1 in C:\mongodb 
# Wed, 15 Jun 2022 21:15:24 GMT
RUN mongo --version && mongod --version
# Wed, 15 Jun 2022 21:15:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jun 2022 21:15:26 GMT
EXPOSE 27017
# Wed, 15 Jun 2022 21:15:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:fca88290e1b048d74ec4e9d1548c4ec09dc3921f80285f39a186278fcaf2d86f`  
		Size: 118.0 MB (117976537 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:52ea757d4cfd57a7819ffb3a397488867081bb0341fe10346d64443842ef882a`  
		Last Modified: Wed, 15 Jun 2022 14:06:26 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d080cea65d065b27b84a0c594cb12010c9ccca5823ecafa6eac5ec57317d9df`  
		Last Modified: Wed, 15 Jun 2022 21:47:41 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd63edee03f035f3cfb58666e80cbb4d84af480adce8fe2ed2bd5b76c51006e`  
		Last Modified: Wed, 15 Jun 2022 21:47:38 GMT  
		Size: 86.8 KB (86778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7db326850d2b42499eea1a0f505ff09671b98a4b106c795df4d1ceac799ec0d`  
		Last Modified: Wed, 15 Jun 2022 21:47:38 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cea24d3d6cb168c05a90004e4d96708c2ee7e46f43a50bbdd82f1479bcded8`  
		Last Modified: Wed, 15 Jun 2022 21:47:38 GMT  
		Size: 263.5 KB (263517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9f441a9862db509a77cf61d916fe3333731a8f4c5c54fcb8c6b4309d493e59`  
		Last Modified: Wed, 15 Jun 2022 22:01:05 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac626eaa32df743bc7891565c18370bc90ce2b54fe7e03588d139dd4ddc7a8d`  
		Last Modified: Wed, 15 Jun 2022 22:05:14 GMT  
		Size: 241.5 MB (241502322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a353db3dc058cd30a91c17aa82d85dfb28d307cfc6caa4876079062dbeaba8b`  
		Last Modified: Wed, 15 Jun 2022 22:01:02 GMT  
		Size: 49.9 KB (49945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8f944cc1960b532260bfc890a9482597484e317808c1d9ff4a6ceb5bedd8e8`  
		Last Modified: Wed, 15 Jun 2022 22:01:02 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d57cb6ce6193bc927a7a92a161dd946a410ea5cc3475335a2013c135b238048`  
		Last Modified: Wed, 15 Jun 2022 22:01:02 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96905d03c480803f312c86042e49173a5bd36434acc2bb3c25877f4ea7bfe4f2`  
		Last Modified: Wed, 15 Jun 2022 22:01:02 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-nanoserver` - windows version 10.0.17763.3046; amd64

```console
$ docker pull mongo@sha256:cc2aed3a1a2a9129e6d04f5e45fbae2d793c37a58e6cffc9b062b291ebb5c37c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345074164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc86a766a1f06dd046b51ae3ee4b4467e29f3ae5711589b31612147c049f2e1`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Jun 2022 19:20:11 GMT
RUN Apply image 10.0.17763.3046
# Wed, 15 Jun 2022 13:18:02 GMT
SHELL [cmd /S /C]
# Wed, 15 Jun 2022 21:09:01 GMT
USER ContainerAdministrator
# Wed, 15 Jun 2022 21:09:31 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 15 Jun 2022 21:09:32 GMT
USER ContainerUser
# Wed, 15 Jun 2022 21:09:33 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 15 Jun 2022 21:15:38 GMT
ENV MONGO_VERSION=4.4.14
# Wed, 15 Jun 2022 21:16:03 GMT
COPY dir:5db4d92801abb4c6b6f16e80c283eda3a5fdc6431914dfb8699f556acea891c1 in C:\mongodb 
# Wed, 15 Jun 2022 21:16:18 GMT
RUN mongo --version && mongod --version
# Wed, 15 Jun 2022 21:16:19 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jun 2022 21:16:20 GMT
EXPOSE 27017
# Wed, 15 Jun 2022 21:16:21 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:d555a7e4de4dd775379d5c43c1419374bff7908670dc7444be5e8e8f386f3d26`  
		Size: 103.2 MB (103153235 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ec2e0a40359897e8d5f91d9806e952d9783f2bc30dd279b63a217ee6985ef3c`  
		Last Modified: Wed, 15 Jun 2022 14:07:45 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d19bba12342216b396550bee0fd1ec81490efee021917ee03cd358c63f84ba8`  
		Last Modified: Wed, 15 Jun 2022 21:54:02 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1482fe090238b0a466d117555441f2f20f684020b14f8c6ab297c5e213d39b5e`  
		Last Modified: Wed, 15 Jun 2022 21:53:57 GMT  
		Size: 70.5 KB (70534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8a70e7a7c337b61c46d7d53947831d7a343ec9b3afc2f1ac6909de090c0e88`  
		Last Modified: Wed, 15 Jun 2022 21:53:56 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7c468f9b42d6946f0bee90ae8ef2b05161d9e5f7f6de932d1e31ae7a9728dc`  
		Last Modified: Wed, 15 Jun 2022 21:53:48 GMT  
		Size: 263.5 KB (263496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43bc191f9795894f8120276f3951c4e2a7b60223827e2212e1b5585e8654956`  
		Last Modified: Wed, 15 Jun 2022 22:05:30 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4edad4578563bb6d488e73df31d3f1ffb95d8d97096bb1ba9e3002725bdb8ac`  
		Last Modified: Wed, 15 Jun 2022 22:06:15 GMT  
		Size: 241.5 MB (241502321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcb2674f37712ba369d220b2b2f4a740550bb953e202e71daa5192313073178`  
		Last Modified: Wed, 15 Jun 2022 22:05:27 GMT  
		Size: 76.4 KB (76386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8ff006b2815babd4c15de129ed6949d0260177d2474cbcc4e4ef21015d7747`  
		Last Modified: Wed, 15 Jun 2022 22:05:27 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0fc1841075c90c2e10e37e16071ea1743b01c92a22de4396fef481f8193b62`  
		Last Modified: Wed, 15 Jun 2022 22:05:27 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2347e7dda916034e6a039e1ff9e816c65d0065cbab8ea1d423674fa205f169c`  
		Last Modified: Wed, 15 Jun 2022 22:05:27 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
