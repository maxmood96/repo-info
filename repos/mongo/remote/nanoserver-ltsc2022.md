## `mongo:nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:3b708686364ba3a9866cba8553abda4d81db003b84097c0867bcc20e349cec65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `mongo:nanoserver-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull mongo@sha256:739bfee66f74c585be8e3f66c96ea9449c5dff872c9c53c77f03d340a84c29a3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **732.1 MB (732085129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc361875f986c901a1d92cbc05768e269b1316ec06dbdcb765532b49638e67b0`
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
# Wed, 29 Nov 2023 01:22:53 GMT
ENV MONGO_VERSION=7.0.4
# Wed, 29 Nov 2023 01:23:43 GMT
COPY dir:1ed22a695d6759e945a6b79c9e5fbe1b8cd3b8404523cfde550085866fe7694e in C:\mongodb 
# Wed, 29 Nov 2023 01:24:05 GMT
RUN mongod --version
# Wed, 29 Nov 2023 01:24:06 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 29 Nov 2023 01:24:06 GMT
EXPOSE 27017
# Wed, 29 Nov 2023 01:24:07 GMT
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
	-	`sha256:f168f34244af64d92af88729af9800a6e47bb0734b1771b9e9d4710da410c167`  
		Last Modified: Wed, 29 Nov 2023 01:51:40 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c400162e30b95bbd322ca18a6c2c3b3370d19b91e297dc9871490b5ae1d50b17`  
		Last Modified: Wed, 29 Nov 2023 01:53:16 GMT  
		Size: 610.9 MB (610921105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93cf69b125e5c90043e81d15ed51c78494e3e626c8db5a6c1aeed71e7374b47`  
		Last Modified: Wed, 29 Nov 2023 01:51:38 GMT  
		Size: 53.5 KB (53453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32fac7191b11a35346acac8863d2e3085d7698223e8ab8a949f297215db82ce`  
		Last Modified: Wed, 29 Nov 2023 01:51:38 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19522b1822e53d750825654b9f39abc5e34082cb5a149503d466c326b50d4bb9`  
		Last Modified: Wed, 29 Nov 2023 01:51:38 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d06db121b08d6fdbf418004d7cb68085c3ef5e9d3bdd0b865423daec4e7b5d4`  
		Last Modified: Wed, 29 Nov 2023 01:51:38 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
