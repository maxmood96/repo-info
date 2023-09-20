## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:8a4d29e4a24a578c1aa02632ca77f81973b3aaa5d73ee614ce33dc7e2dea7989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:4a424d5ccb3ce81492d4a2aecc5bbe03a67a145345746a1d96c026d7956f33f2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110068714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c344b7589180b9b78bc248edaae3e05a72d7b3bd1240c9f0ecbc2bd8414643d3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 05:08:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 20 Sep 2023 00:18:51 GMT
RUN cmd /S /C #(nop) COPY file:82881a6eaae1fdef881aedd297eada2f8ec0fc40e73c31dbc83c116c9f282e11 in C:\nats-server.exe 
# Wed, 20 Sep 2023 00:18:52 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 20 Sep 2023 00:18:52 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 20 Sep 2023 00:18:53 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 Sep 2023 00:18:54 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9930674eb6676a1690e63a275d0da517ab8b8aeab7ccd20591f76f7c69a5`  
		Last Modified: Wed, 13 Sep 2023 05:08:48 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e311c6fa6640185d0147e86e5eee4ab6aac292985c5e1e0daeb8170482fd33d`  
		Last Modified: Wed, 20 Sep 2023 00:20:06 GMT  
		Size: 5.6 MB (5569723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b919469d50b165a5c87e445ee493dda4912cf2ad8db689c6d84a298c92e3b9`  
		Last Modified: Wed, 20 Sep 2023 00:20:05 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d34608f67091df8d80f28a392deb160738bbe00ec2a279d9edcfdd3b152eb8`  
		Last Modified: Wed, 20 Sep 2023 00:20:05 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c38e775b4dd4f949ccbee2cc13bc595e7ffad034c1ba158d7a8451c574cb98`  
		Last Modified: Wed, 20 Sep 2023 00:20:05 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc2e4e8b1ee6fac6ba0333ec74b715dc57449b31dc90cf5ad2315b8a962bc49`  
		Last Modified: Wed, 20 Sep 2023 00:20:05 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
