## `mongo:6-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:3d5135a621397a9b64313dc05cba0ac41adf707360e183944ac2c2325494ad9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `mongo:6-nanoserver-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull mongo@sha256:193d763be0fdc90d0c1a68f1a40ff302f69b69f324e46afdaaf9f54604ccc59f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.6 MB (638564740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915cec4b2a2ae652bd4b408b79b000ac3ac286640a884f2c769ffb1a50f65889`
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
# Thu, 16 Nov 2023 03:25:06 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Wed, 29 Nov 2023 01:31:18 GMT
ENV MONGO_VERSION=6.0.12
# Wed, 29 Nov 2023 01:32:41 GMT
COPY dir:8559148497dc768ddd11c21dfa76fba54aa7fe60a1051bc30a5cf71e7f4f107f in C:\mongodb 
# Wed, 29 Nov 2023 01:32:55 GMT
RUN mongod --version
# Wed, 29 Nov 2023 01:32:56 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 29 Nov 2023 01:32:57 GMT
EXPOSE 27017
# Wed, 29 Nov 2023 01:32:58 GMT
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
	-	`sha256:7ba7dcc051c7c2f58503f152324d54cae0121e59f9195f52369107fc1a818f71`  
		Last Modified: Thu, 16 Nov 2023 04:22:52 GMT  
		Size: 267.1 KB (267130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0f81a00a779ff412230f431daf428d9b02e2b7c2dde99f068bcab1f07a5b1a`  
		Last Modified: Wed, 29 Nov 2023 01:58:39 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29375288a41ec1489c933e5f1ea5f2dda15505f9e6440d276c7a955f336396ff`  
		Last Modified: Wed, 29 Nov 2023 01:59:59 GMT  
		Size: 517.4 MB (517400123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fccd002eddea23138ff4040cb158e5dec3aa24fb233a453c7344dd3d82f6b5e`  
		Last Modified: Wed, 29 Nov 2023 01:58:37 GMT  
		Size: 53.7 KB (53699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f82445af3442f9bd776708a6c7b5e950a38619a15e51c58989017c1c644afd6`  
		Last Modified: Wed, 29 Nov 2023 01:58:37 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ab53b774b3f66400b56ecd1325deb07882068e7d6dffd441e4551faf9ab105`  
		Last Modified: Wed, 29 Nov 2023 01:58:37 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87362a42c66dcfcd0b665be56442a57f40cbadb81e57a0a83003db01a14f438e`  
		Last Modified: Wed, 29 Nov 2023 01:58:37 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
