## `mongo:5-nanoserver`

```console
$ docker pull mongo@sha256:244d2989338fd655bbe856f8ec25a74f774f4eaa49f4d3e6bb786ceb2ecfb752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2113; amd64
	-	windows version 10.0.17763.5122; amd64

### `mongo:5-nanoserver` - windows version 10.0.20348.2113; amd64

```console
$ docker pull mongo@sha256:50663cc9723d8d58fc360616c7dc5fbea4286defb979889a0159fd90756f9957
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.0 MB (433976222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614ee1923b030180a9564fb9f483b974a148ba58a1adcc4274a34f79fd804ecb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Nov 2023 06:09:19 GMT
RUN Apply image 10.0.20348.2113
# Thu, 16 Nov 2023 02:53:08 GMT
SHELL [cmd /S /C]
# Thu, 16 Nov 2023 03:24:54 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 03:25:04 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 16 Nov 2023 03:25:05 GMT
USER ContainerUser
# Thu, 16 Nov 2023 03:57:01 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 29 Nov 2023 01:38:43 GMT
ENV MONGO_VERSION=5.0.23
# Wed, 29 Nov 2023 01:39:10 GMT
COPY dir:0018708e8eafae2e730cc7effdd40df3393db3f93570d01d6f7fc8a53b6c51f3 in C:\mongodb 
# Wed, 29 Nov 2023 01:39:24 GMT
RUN mongo --version && mongod --version
# Wed, 29 Nov 2023 01:39:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 29 Nov 2023 01:39:26 GMT
EXPOSE 27017
# Wed, 29 Nov 2023 01:39:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1ca4fbe907f22e883670decfa8d7f4490a79a995bb83a6c286248c21d61a62f5`  
		Last Modified: Tue, 14 Nov 2023 21:13:36 GMT  
		Size: 120.8 MB (120753560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc13ac2d02de25aafaa5c365411a34535ba58cc30cea6c804138bd620ee8c2ce`  
		Last Modified: Thu, 16 Nov 2023 03:12:33 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d474837d2cc6525aa5f583af9ac4b8295cfeda4968a5d72c5ca8d5d2b8ce0793`  
		Last Modified: Thu, 16 Nov 2023 04:22:53 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99315a52328e8cacc6b2209db2f8e22a758f85b3ab693adc992c634d89983122`  
		Last Modified: Thu, 16 Nov 2023 04:22:52 GMT  
		Size: 82.1 KB (82119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143fdbc2782bf8a5ad2348a0ba16a1fe641848670d929b10864294ba1ac342d1`  
		Last Modified: Thu, 16 Nov 2023 04:22:51 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341f241b24b10b19234e2efc59e77b7d11de694e8166145dd6c66b61e8fdd901`  
		Last Modified: Thu, 16 Nov 2023 04:47:51 GMT  
		Size: 263.4 KB (263375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc35fb24aca5fa80263dd3492367ac116f0db41ab99ac49b046d401ce37dcc27`  
		Last Modified: Wed, 29 Nov 2023 02:04:13 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a948197999dc78a7ec0688fdb6dddd1fa88790740271851511c6025dfad97d`  
		Last Modified: Wed, 29 Nov 2023 02:05:08 GMT  
		Size: 312.8 MB (312795683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6420aa6d325551498a71e895dc1415a2a7c07b7e4e02287a9da27f1a5341568`  
		Last Modified: Wed, 29 Nov 2023 02:04:11 GMT  
		Size: 73.8 KB (73834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe84acab6f974b931121be005096076285d496116389014bb4a96177dba29f30`  
		Last Modified: Wed, 29 Nov 2023 02:04:11 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db69ef8ed664824f7825eb97b9941723c4cd4d91be5da6ce7eaaa0ff8072682`  
		Last Modified: Wed, 29 Nov 2023 02:04:11 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213d8a54230aca8885e84ed3d00efe792336b84c8ca1383acc577c84e5caa9cf`  
		Last Modified: Wed, 29 Nov 2023 02:04:11 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-nanoserver` - windows version 10.0.17763.5122; amd64

```console
$ docker pull mongo@sha256:63affdcfbba0b0791c581f4f6683d21fd924bdff8db524e8e06d60cd76bcfd0b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.7 MB (417711196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a9aac5bcc4a31fa1b7df65d2a2a45f6beac17de7c6e0c23f351caf6e0b99d7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 02:55:52 GMT
SHELL [cmd /S /C]
# Thu, 16 Nov 2023 03:26:22 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 03:26:36 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 16 Nov 2023 03:26:36 GMT
USER ContainerUser
# Thu, 16 Nov 2023 03:57:55 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 29 Nov 2023 01:39:37 GMT
ENV MONGO_VERSION=5.0.23
# Wed, 29 Nov 2023 01:40:07 GMT
COPY dir:0018708e8eafae2e730cc7effdd40df3393db3f93570d01d6f7fc8a53b6c51f3 in C:\mongodb 
# Wed, 29 Nov 2023 01:40:19 GMT
RUN mongo --version && mongod --version
# Wed, 29 Nov 2023 01:40:20 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 29 Nov 2023 01:40:21 GMT
EXPOSE 27017
# Wed, 29 Nov 2023 01:40:22 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26eb16ff47ed3c1f3ff64a9920a3407afa035ee398f803b948326dc0e5e4e79e`  
		Last Modified: Thu, 16 Nov 2023 03:13:07 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e02f563a12fbc6846cdd83dd195b52331a6b956d0cadd546aac9d48eafc857c`  
		Last Modified: Thu, 16 Nov 2023 04:24:41 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a67c125c9a773e11ea7d5d4837aab6edb57a3542f5d40eb33917ff54a1764254`  
		Last Modified: Thu, 16 Nov 2023 04:24:39 GMT  
		Size: 68.4 KB (68440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ebb2a529df887c3f03501c0eb37994d3377f525a469a8ec60551d78b6fa67f`  
		Last Modified: Thu, 16 Nov 2023 04:24:38 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3c7cbc119978d3d4f1dea0cf8fa98065d456932d1c14d27637e965347f8383`  
		Last Modified: Thu, 16 Nov 2023 04:48:59 GMT  
		Size: 263.4 KB (263376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4677eb41c1f9b5cb02cdf22b74bfc27e09399f1dcc65f6b967b00fd1d26e74`  
		Last Modified: Wed, 29 Nov 2023 02:05:23 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83475ed23d315a17da79705f6794c546ce8983ebc398c4e5865d36ea4882fc44`  
		Last Modified: Wed, 29 Nov 2023 02:06:16 GMT  
		Size: 312.8 MB (312796678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd985a7a04f2a1d00b28c3960b8ca99e042790c2cdcb89b740ecc763df57585c`  
		Last Modified: Wed, 29 Nov 2023 02:05:21 GMT  
		Size: 77.4 KB (77391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d615fc3f527cbf3a4a4063fdb39b298d562da51b0bac2afbba45780545136a9`  
		Last Modified: Wed, 29 Nov 2023 02:05:20 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93d62ab0280d64f652cd6495fa9b88a63bd635e0186c493d84566636af8f32e`  
		Last Modified: Wed, 29 Nov 2023 02:05:20 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c39dce626c5a004cde6bea36e11f5e89bc15fe194c77cdd1c115d7c76738629`  
		Last Modified: Wed, 29 Nov 2023 02:05:20 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
