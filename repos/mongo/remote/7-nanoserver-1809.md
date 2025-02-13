## `mongo:7-nanoserver-1809`

```console
$ docker pull mongo@sha256:cf8dde2660e339b6bf1e5cdb15e18976552cd537d1ea8b8362bbd066fd1bf9f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `mongo:7-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull mongo@sha256:837f500f66e7a3fe85e87ac6b789d2d7432fb5b12b7778b113bf6bde947ec607
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **766.4 MB (766381300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f86bf245650f997e5a229c81081cb41b4a5fc328b41588eb7270e2f3663b445`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 18:08:22 GMT
SHELL [cmd /S /C]
# Wed, 15 Jan 2025 18:08:24 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:08:26 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 15 Jan 2025 18:08:26 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:08:28 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 15 Jan 2025 18:08:29 GMT
ENV MONGO_VERSION=7.0.16
# Wed, 15 Jan 2025 18:08:50 GMT
COPY dir:e2287a32285406d829d215fee89db1b9fbd999270c712cc0faadfea5bebebee9 in C:\mongodb 
# Wed, 15 Jan 2025 18:09:07 GMT
RUN mongod --version
# Wed, 15 Jan 2025 18:09:08 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jan 2025 18:09:08 GMT
EXPOSE 27017
# Wed, 15 Jan 2025 18:09:09 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Wed, 15 Jan 2025 07:23:16 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae20508ad1dba64c9a57a265e79b0b1927e9955bf9f3fa0aab4cb19e6a47c8b`  
		Last Modified: Wed, 05 Feb 2025 21:37:13 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b597b7b68a0ae5ae735d0eee427689b15995eb4602b3a111c05113b4ca586c5`  
		Last Modified: Wed, 05 Feb 2025 21:37:13 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecb5ce334f56b52dd0e76450bd081ffe939312578f78114210df54c826c80c6`  
		Last Modified: Wed, 05 Feb 2025 21:37:13 GMT  
		Size: 71.2 KB (71182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f615fa7c0e3a3e538faed69b46ee182e1793432a28ddda0b0e14610ab9854c`  
		Last Modified: Wed, 05 Feb 2025 21:37:14 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79085d45ec625fe066e00922b0a85876132913eca33ff8b9c45c9a62b2ca7ae`  
		Last Modified: Wed, 05 Feb 2025 21:37:14 GMT  
		Size: 275.2 KB (275234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57511cd0ee4cb8ff1901d8232410ad921c2486d362b767c941f5c4a8c7424f47`  
		Last Modified: Wed, 05 Feb 2025 21:37:15 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1860156e26a16671b439df71d94bc1bb2b129a4c12fd60511dd99eb3d0d943c`  
		Last Modified: Wed, 05 Feb 2025 21:37:32 GMT  
		Size: 610.7 MB (610683526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95de743771b8b2c0e89090f2ede8e641c7bbd1cc180ff8ac4625763d0cc19b9b`  
		Last Modified: Wed, 05 Feb 2025 21:37:15 GMT  
		Size: 76.2 KB (76215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa94e97d73be7d10a314f305f319f82509ab6e9791107d48be10de3d3b28b7d6`  
		Last Modified: Wed, 05 Feb 2025 21:51:52 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a447058c6fc45d8a35760338085ef13dfd199858b11c5ab66a35349d29b79bfb`  
		Last Modified: Wed, 05 Feb 2025 21:51:52 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef1a1d827584c4c5812367ec0b9fce7b5ea1479afa9b1b819348a6d96334ddd`  
		Last Modified: Wed, 05 Feb 2025 21:51:52 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
