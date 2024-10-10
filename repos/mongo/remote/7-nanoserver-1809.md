## `mongo:7-nanoserver-1809`

```console
$ docker pull mongo@sha256:0682d9bbb5cd9f5407dac2d8ff1cc90b27494ae2d9569c8b18d05fbd77fc4c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `mongo:7-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull mongo@sha256:63619a6862ce8294cc05f0fee2712f3bb43e116444487896b7332eab97bb0617
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **764.0 MB (763983796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ecd58660542a184a7f92a95ce4963700bc10464a81e1d4565c801650428403`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 10 Oct 2024 00:03:45 GMT
SHELL [cmd /S /C]
# Thu, 10 Oct 2024 00:03:46 GMT
USER ContainerAdministrator
# Thu, 10 Oct 2024 00:03:49 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 10 Oct 2024 00:03:49 GMT
USER ContainerUser
# Thu, 10 Oct 2024 00:03:50 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Thu, 10 Oct 2024 00:03:51 GMT
ENV MONGO_VERSION=7.0.14
# Thu, 10 Oct 2024 00:04:24 GMT
COPY dir:569dc595e568429f713bfa17916f5a0425b14e2551565b8dcffbac1d9a45d806 in C:\mongodb 
# Thu, 10 Oct 2024 00:04:30 GMT
RUN mongod --version
# Thu, 10 Oct 2024 00:04:31 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 10 Oct 2024 00:04:32 GMT
EXPOSE 27017
# Thu, 10 Oct 2024 00:04:32 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f8a0e3e25e94bfb87b909301f5f0cbe9ec8baa60c8ecef792558c8c46f871d`  
		Last Modified: Thu, 10 Oct 2024 00:04:39 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73626085e953e4263af16eb21fa1e03cec2acf5c3c26e407ee8f5732c669040a`  
		Last Modified: Thu, 10 Oct 2024 00:04:39 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7411af26c60b585cf41916db3fa0d6ea8130b958153e02dbd7280e120b3ed4d1`  
		Last Modified: Thu, 10 Oct 2024 00:04:38 GMT  
		Size: 76.2 KB (76226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389175cd1eeef2b35bb560a09b0e62b5437f79bffb3ab3caeb2b75e8d863856b`  
		Last Modified: Thu, 10 Oct 2024 00:04:38 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de479ad80d0aad1a0cd7064aa6923703859838019ca579f5f6c274d84394ea30`  
		Last Modified: Thu, 10 Oct 2024 00:04:38 GMT  
		Size: 275.2 KB (275195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95604cd3de9e26193b31a684ce8c7c5469d40be992ca1b2cfa1fc18e5c075530`  
		Last Modified: Thu, 10 Oct 2024 00:04:38 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984a55b0653bf6a8d9bc4c3f484f9586ce7d5cb026b8be42b07d866cedc79a11`  
		Last Modified: Thu, 10 Oct 2024 00:05:27 GMT  
		Size: 608.5 MB (608452855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcda023eaf28c6703fc93f4fefaf519cb0a4d36fba62de2159a751ff8b0e96b`  
		Last Modified: Thu, 10 Oct 2024 00:04:36 GMT  
		Size: 78.7 KB (78680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8941571aeaaf2b135a6246ab9cf951d45d55acc10a027b3ea574463d5d0629`  
		Last Modified: Thu, 10 Oct 2024 00:04:36 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de2f9e5a9248c9ce70c323d2fd8e0f8fabaafc1fcac18230a2524e6a2ebac6f`  
		Last Modified: Thu, 10 Oct 2024 00:04:36 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a338699ba210f23cdb5c78a1d54bb6f6a923441b31778e2294713bb2c4a38bf8`  
		Last Modified: Thu, 10 Oct 2024 00:04:36 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
