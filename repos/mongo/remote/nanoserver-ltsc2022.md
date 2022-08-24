## `mongo:nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:6a929659f315b2577ae98af29b826cf91f1ab4836945ec82cc2fccd2987d2653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.887; amd64

### `mongo:nanoserver-ltsc2022` - windows version 10.0.20348.887; amd64

```console
$ docker pull mongo@sha256:6ae8926913dd2951e2d608b4ba2eee3f5943cdf39d5d7d31c2e6cb170802b283
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.7 MB (627717165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2557d47a1bbf7e7ac7d1fc638005d2dbfdc33df9398c316de358ad2adb31ea00`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 06 Aug 2022 18:05:23 GMT
RUN Apply image 10.0.20348.887
# Wed, 10 Aug 2022 13:00:01 GMT
SHELL [cmd /S /C]
# Wed, 10 Aug 2022 18:21:28 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 18:21:43 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 10 Aug 2022 18:21:43 GMT
USER ContainerUser
# Wed, 24 Aug 2022 22:26:27 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Wed, 24 Aug 2022 22:26:29 GMT
ENV MONGO_VERSION=6.0.1
# Wed, 24 Aug 2022 22:27:19 GMT
COPY dir:9bc3bf7ac427acc5da2a94db90fd2f879ea935b4a3cfd676cbd1fb49e16c8f3c in C:\mongodb 
# Wed, 24 Aug 2022 22:27:35 GMT
RUN mongod --version
# Wed, 24 Aug 2022 22:27:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 24 Aug 2022 22:27:38 GMT
EXPOSE 27017
# Wed, 24 Aug 2022 22:27:40 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2ebf439f800cd4c1fccaf4a0545e6bff60caa5141295c8ab81f6c525073c423d`  
		Size: 118.1 MB (118088450 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:28bba27fcdd9c2f008a9c22db6c16dece3a5c3a49f9fac9447924071999adf65`  
		Last Modified: Wed, 10 Aug 2022 13:26:19 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea577aa22b29cf1143b45e9c9507d3cb6afba550ab0e0f1d34cc0f3bc394fb8`  
		Last Modified: Wed, 10 Aug 2022 18:54:06 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573d7b3cd6a4597d6a752c3c5d397d443396335384d76305346cc9cd7d307fe8`  
		Last Modified: Wed, 10 Aug 2022 18:54:04 GMT  
		Size: 76.2 KB (76190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24136b33c2554c6e408883876b2a54dba6f355751bc713713bcf47ecaac222`  
		Last Modified: Wed, 10 Aug 2022 18:54:04 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680be7b0846097e61562a67c77963a165ce0a70fd0a6900aff0cd4698aa0a72d`  
		Last Modified: Wed, 24 Aug 2022 22:53:35 GMT  
		Size: 267.2 KB (267180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda8b8f8ff15ecfe9a9dc11f2cfdc91e2d4efe9a0c1c8983e7b241dbb1df6c51`  
		Last Modified: Wed, 24 Aug 2022 22:53:35 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d54d72cfac6a91b87fdee8fcf3229bd77374b467ed72c77eeb24d1152f00418`  
		Last Modified: Wed, 24 Aug 2022 22:54:52 GMT  
		Size: 509.2 MB (509224341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef9ef7f5425e6f80b6175064364741460a5f7f49973e7b564b2dcccd7b86570`  
		Last Modified: Wed, 24 Aug 2022 22:53:33 GMT  
		Size: 52.8 KB (52822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4e8d64b881747a2bda2aba2a7385411cf91ea5c25f6d7c089cf384f5c80571`  
		Last Modified: Wed, 24 Aug 2022 22:53:33 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb187887be6a67c7eaede99957167718f7bbeffc90ef29cee7e20c11d192ec6b`  
		Last Modified: Wed, 24 Aug 2022 22:53:33 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0baff8c2dc1b4d7e7e87f9864e9aa515b9c261705679f3a83eb1540e159252`  
		Last Modified: Wed, 24 Aug 2022 22:53:33 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
