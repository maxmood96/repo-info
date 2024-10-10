## `mongo:nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:c017b2d853845e179a7cd4c3d89fcc9135db27783e7d48ce8bac135978d1d9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `mongo:nanoserver-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull mongo@sha256:cf905bf1ea22787f36a9adbf34c558ee22a1d67385450e375b42da8a5125aec3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **885.8 MB (885765441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224da143442a84b82c1296d76cde380fed6716dcb0aa27f0e1dfffa3dde06833`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 10 Oct 2024 00:00:01 GMT
SHELL [cmd /S /C]
# Thu, 10 Oct 2024 00:00:02 GMT
USER ContainerAdministrator
# Thu, 10 Oct 2024 00:00:04 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 10 Oct 2024 00:00:05 GMT
USER ContainerUser
# Thu, 10 Oct 2024 00:00:06 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Thu, 10 Oct 2024 00:00:07 GMT
ENV MONGO_VERSION=8.0.1
# Thu, 10 Oct 2024 00:00:34 GMT
COPY dir:51be3647b815c20429813a5d3bc4dda902965341b9140467cfcf228524b19b00 in C:\mongodb 
# Thu, 10 Oct 2024 00:00:57 GMT
RUN mongod --version
# Thu, 10 Oct 2024 00:00:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 10 Oct 2024 00:00:58 GMT
EXPOSE 27017
# Thu, 10 Oct 2024 00:00:58 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af1aa3b387b371cf454eef277ba08b58fc750129fa24c5e18427512e06166a8`  
		Last Modified: Thu, 10 Oct 2024 00:01:07 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36eb3b7cf6e677ab986ef2915ea065e7ff086d2687e253c8bdbb98c5fe97441`  
		Last Modified: Thu, 10 Oct 2024 00:01:06 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3292a77b61d790cd2e6fe212414618b9ef396225a202dba11931a902d7059368`  
		Last Modified: Thu, 10 Oct 2024 00:01:05 GMT  
		Size: 78.9 KB (78913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836a95d29ea22eb95601db6ef6676629e50bb77279e92343ed389c42448b732c`  
		Last Modified: Thu, 10 Oct 2024 00:01:05 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d190664e3200096194e05fb4be35c8c307d72a6519825f1e3e54d3470317220`  
		Last Modified: Thu, 10 Oct 2024 00:01:05 GMT  
		Size: 275.2 KB (275163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7b671cb015d7c24da9fe709e00470f437734b0f5235e37254c2f736ddf321a`  
		Last Modified: Thu, 10 Oct 2024 00:01:04 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e08bf1b31ef479c958def42a2174794dd54cefa2fc5f792c736f21828191e5b`  
		Last Modified: Thu, 10 Oct 2024 00:02:08 GMT  
		Size: 764.8 MB (764795420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585b0a2d9eac176f63668a04511d6bae5b493a7ea837d0dd2abc8a84a3ced3be`  
		Last Modified: Thu, 10 Oct 2024 00:01:03 GMT  
		Size: 97.7 KB (97749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a0df6bfae19c205903e027f34b39cb89484a1ee335c3a4ba987019465f01b0`  
		Last Modified: Thu, 10 Oct 2024 00:01:02 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302f5f8a726ed4a3df36d0651aa75f410bc4bd4196c6dbba5a81ce4ac1feda87`  
		Last Modified: Thu, 10 Oct 2024 00:01:03 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2509bfde47f7e086b2f0dc7cd5c41124d0b6e41cd3095537b13e14ae91d3e81`  
		Last Modified: Thu, 10 Oct 2024 00:01:02 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
