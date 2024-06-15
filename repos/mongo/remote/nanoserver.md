## `mongo:nanoserver`

```console
$ docker pull mongo@sha256:9a3b2240c0e8d29a83a57ede4a6081d1886ee2cec52d4b2b65e7e46b3559a63b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2527; amd64
	-	windows version 10.0.17763.5936; amd64

### `mongo:nanoserver` - windows version 10.0.20348.2527; amd64

```console
$ docker pull mongo@sha256:aed307ba454962284f0b8077226446606b4bbc42b662d78cd96a2326d4ef37af
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **739.1 MB (739131300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c63520107f961fd14b21d9b809af84d87e59834df0746643c2381c985b825c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Jun 2024 08:41:16 GMT
RUN Apply image 10.0.20348.2527
# Sat, 15 Jun 2024 00:03:31 GMT
SHELL [cmd /S /C]
# Sat, 15 Jun 2024 00:03:32 GMT
USER ContainerAdministrator
# Sat, 15 Jun 2024 00:03:35 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 15 Jun 2024 00:03:35 GMT
USER ContainerUser
# Sat, 15 Jun 2024 00:03:37 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Sat, 15 Jun 2024 00:03:38 GMT
ENV MONGO_VERSION=7.0.11
# Sat, 15 Jun 2024 00:04:01 GMT
COPY dir:19a9c5e7b92e67df364a58952a43fa9635a4cea236c07894dad5b3a27bc56ae4 in C:\mongodb 
# Sat, 15 Jun 2024 00:04:13 GMT
RUN mongod --version
# Sat, 15 Jun 2024 00:04:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 15 Jun 2024 00:04:15 GMT
EXPOSE 27017
# Sat, 15 Jun 2024 00:04:16 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:f9825bcd6f9509654677a23b5fa1d32b32e1e32ff51914ebfaa76d5e79c22b50`  
		Last Modified: Wed, 12 Jun 2024 02:27:19 GMT  
		Size: 120.5 MB (120488969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50448bbd2e59af044bbd8a137abf0de770434b8293096c211b1626bb9aaf14e0`  
		Last Modified: Sat, 15 Jun 2024 00:04:23 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ab5e4097b7f9fa5756bd33f5baad93a61338b22162c448d53171eb061acd32`  
		Last Modified: Sat, 15 Jun 2024 00:04:23 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99152e74d55afeb8f6631799a71d69ff18627e19cb6d9199e846e70e1c19599f`  
		Last Modified: Sat, 15 Jun 2024 00:04:22 GMT  
		Size: 80.5 KB (80472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0b08a4d1c361b36b0445911e5b2dfc541951dafeafd77d024060be04ac4ef7`  
		Last Modified: Sat, 15 Jun 2024 00:04:21 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02983190c8c1ce5a10001eab85642822348e6411185fcc29291575be1218801e`  
		Last Modified: Sat, 15 Jun 2024 00:04:22 GMT  
		Size: 275.1 KB (275149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1d5ce9f5c21fc93031085b3ee08545c9178739d8b71a1862342036fbcadda4`  
		Last Modified: Sat, 15 Jun 2024 00:04:22 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa378aa1dd69f33d04b704c2776e03e0f856fbed598ba641d3b32942bd2a437`  
		Last Modified: Sat, 15 Jun 2024 00:05:08 GMT  
		Size: 618.2 MB (618172234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0579a9b0b46419187f6a8b41b0b2a49da9a34373b83c7851de45d0856254ce90`  
		Last Modified: Sat, 15 Jun 2024 00:04:20 GMT  
		Size: 107.3 KB (107251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cd28ea6181525ad708736c64506c97f4af0f425ac4f5c4ae51b5b5e446a641`  
		Last Modified: Sat, 15 Jun 2024 00:04:20 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d4ba8a5f27966225a4189747963e0fe377a78ac94a7d7914d4c4826852f1e9`  
		Last Modified: Sat, 15 Jun 2024 00:04:20 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed38f6179a0aa07b65560b3d11c2be772a9a1eac6b807854c88d0c5c02cd4a17`  
		Last Modified: Sat, 15 Jun 2024 00:04:20 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull mongo@sha256:391ee22cc5b1d631ed90d46739c68ac4bc31a36ba32d40b3092619880ea25479
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **773.6 MB (773638521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e99b80fa18bab947d84e36fac3ab13621a3034c60f88315bf76d77c31e14353`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Sat, 15 Jun 2024 00:08:37 GMT
SHELL [cmd /S /C]
# Sat, 15 Jun 2024 00:08:39 GMT
USER ContainerAdministrator
# Sat, 15 Jun 2024 00:08:42 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 15 Jun 2024 00:08:43 GMT
USER ContainerUser
# Sat, 15 Jun 2024 00:08:44 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Sat, 15 Jun 2024 00:08:45 GMT
ENV MONGO_VERSION=7.0.11
# Sat, 15 Jun 2024 00:09:14 GMT
COPY dir:19a9c5e7b92e67df364a58952a43fa9635a4cea236c07894dad5b3a27bc56ae4 in C:\mongodb 
# Sat, 15 Jun 2024 00:09:27 GMT
RUN mongod --version
# Sat, 15 Jun 2024 00:09:28 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 15 Jun 2024 00:09:29 GMT
EXPOSE 27017
# Sat, 15 Jun 2024 00:09:30 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4742bd58662fc89fb1254b00b2def1fd2296c14f30a44f14f8fe8ee613231d`  
		Last Modified: Sat, 15 Jun 2024 00:09:35 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1d0348fbae88877a2b3244e3b9a6b1c2e3ef663648e099fbd4b6f151d418e92`  
		Last Modified: Sat, 15 Jun 2024 00:09:35 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347ad1da7b8ac6af1559e7fe346c9bf48f01b2e4efab6676038a0a910623693e`  
		Last Modified: Sat, 15 Jun 2024 00:09:34 GMT  
		Size: 73.7 KB (73658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b11c5a4132560c4de91bf40f97a1b34c5ffec9a3ebdcf82fef2db4676c3f43f`  
		Last Modified: Sat, 15 Jun 2024 00:09:34 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c87bfe5ea3427c37ad297e3b1c0cb9ec19e17bfbaec98dde896194e4108360d`  
		Last Modified: Sat, 15 Jun 2024 00:09:34 GMT  
		Size: 275.2 KB (275167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141f36378e7737369c3ac760bb895b0d7ee1288222467de309b54d07f0cf762e`  
		Last Modified: Sat, 15 Jun 2024 00:09:33 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35f88ede34106c1b25bc280def31938ec382eb3b5d599723b549093b2b7aa63`  
		Last Modified: Sat, 15 Jun 2024 00:10:22 GMT  
		Size: 618.2 MB (618172347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cdb5e3db09ee5af904c6f2bc2f60570976e1e16f0038b4c707f2e3af22cf7c`  
		Last Modified: Sat, 15 Jun 2024 00:09:33 GMT  
		Size: 76.9 KB (76868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fecbb055d191bf7ccc173016900231658b9732cd5261ab7332de84a3f3a9af8`  
		Last Modified: Sat, 15 Jun 2024 00:09:32 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd93b2968a764602d3091d4ad8d9a92f53f37652088c11761b1040d67794c27f`  
		Last Modified: Sat, 15 Jun 2024 00:09:32 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9709ee4e6ec7683782b82c6e8ccfb234ba3dc6cc82da9007827a886d8b0b86`  
		Last Modified: Sat, 15 Jun 2024 00:09:33 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
