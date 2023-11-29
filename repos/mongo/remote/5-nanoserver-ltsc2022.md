## `mongo:5-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:fa6b709aad0c657e8476003395b782223d31d9819f5b6b705adfa8531e523188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `mongo:5-nanoserver-ltsc2022` - windows version 10.0.20348.2113; amd64

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
