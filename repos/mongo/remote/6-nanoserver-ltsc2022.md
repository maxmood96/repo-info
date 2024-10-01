## `mongo:6-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:59ac771a342a01d90bd7576981c4bc1b30cf2e81a59fdd1d203e8a4a5f9771e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `mongo:6-nanoserver-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull mongo@sha256:067a30bc727503f8b5e6e307297d14b535ea383a69e84f3291ff5090dc864aff
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.6 MB (644600062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986a7b9caa9c3ba4009cfe89c3d1185ba921aaead946402fc7a95cf70cf88590`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 05 Sep 2024 23:48:03 GMT
RUN Apply image 10.0.20348.2700
# Tue, 01 Oct 2024 01:51:26 GMT
SHELL [cmd /S /C]
# Tue, 01 Oct 2024 01:51:27 GMT
USER ContainerAdministrator
# Tue, 01 Oct 2024 01:51:42 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 01 Oct 2024 01:51:43 GMT
USER ContainerUser
# Tue, 01 Oct 2024 01:51:44 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Tue, 01 Oct 2024 01:51:45 GMT
ENV MONGO_VERSION=6.0.18
# Tue, 01 Oct 2024 01:52:06 GMT
COPY dir:340f26541b74bac93fbc0306b4a24bb66227c5b0b1968f013d1e5b14ef125ee7 in C:\mongodb 
# Tue, 01 Oct 2024 01:52:21 GMT
RUN mongod --version
# Tue, 01 Oct 2024 01:52:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 01 Oct 2024 01:52:22 GMT
EXPOSE 27017
# Tue, 01 Oct 2024 01:52:23 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a447243899be39b01c34fc7e1bcecb47ce42b14668876fdd121f8b5e2d4d4a86`  
		Last Modified: Tue, 10 Sep 2024 22:28:02 GMT  
		Size: 120.5 MB (120509521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f26e73ca9af0bf3ec004846f3506d08c01aaf43e3419f8ff4391d5283a286b`  
		Last Modified: Tue, 01 Oct 2024 01:52:28 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7bdf49cc396aac2155e0b5766e7b2035aade7029fdde03a76b19b49134bf60`  
		Last Modified: Tue, 01 Oct 2024 01:52:28 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c8a98b2283e0051ccebbfc6e5d75c45398dac89dae745fd65c44da6dc78f80`  
		Last Modified: Tue, 01 Oct 2024 01:52:27 GMT  
		Size: 74.2 KB (74183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689379ed2446705a0ed261b0cb6983fc883e514229e36b0b6356490df02e3a63`  
		Last Modified: Tue, 01 Oct 2024 01:52:27 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50ed25ce275820a2c2cac09fd36bae925a324ca4323894320e0407e56344cd3`  
		Last Modified: Tue, 01 Oct 2024 01:52:27 GMT  
		Size: 275.2 KB (275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba22e919323b79a97d191d774e8f65e8f5e3a87ba26652d3adff681dfd4883a`  
		Last Modified: Tue, 01 Oct 2024 01:52:27 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1413802793976386d7d102afacd46b5231d0c71604c7b4a97bc6274827dcdfb`  
		Last Modified: Tue, 01 Oct 2024 01:53:09 GMT  
		Size: 523.6 MB (523631555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67a2baa67e98306f8786414d71172a923415f49d7d81b23cef72292854406ed`  
		Last Modified: Tue, 01 Oct 2024 01:52:26 GMT  
		Size: 102.1 KB (102130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966b704c54b4d6687e26a1518ab50c8efdd79973758e6f6cd4c9a225d03344b1`  
		Last Modified: Tue, 01 Oct 2024 01:52:26 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5780b29cbe51aa5ac9b12898dd2e2474803be0cf4ae422608c26a49718301a7`  
		Last Modified: Tue, 01 Oct 2024 01:52:26 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca48964661dc791cad667a1ae009bc334dabced6e7a170e49d564870eb898e1f`  
		Last Modified: Tue, 01 Oct 2024 01:52:26 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
