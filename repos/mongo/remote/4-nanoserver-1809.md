## `mongo:4-nanoserver-1809`

```console
$ docker pull mongo@sha256:e4d20dd61d922b705c7e73c87d5079fbcda50dd999a04e702a672e5adad611ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `mongo:4-nanoserver-1809` - windows version 10.0.17763.2452; amd64

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
