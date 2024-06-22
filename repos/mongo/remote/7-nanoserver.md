## `mongo:7-nanoserver`

```console
$ docker pull mongo@sha256:5e8676973261220a8412ea9d13618fbf956c31df11e5c99cc86020a5860196f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `mongo:7-nanoserver` - windows version 10.0.20348.2529; amd64

```console
$ docker pull mongo@sha256:424cfad46e4b6657908fe1034d0a23813cb7619499bda8b3af44ec7aa4e2b10a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **739.1 MB (739120761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2539d5ceba093ac3ed9a5cdd1e4126c9c677d73c6b8c72e09031dc9caa9650c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 19 Jun 2024 19:27:30 GMT
RUN Apply image 10.0.20348.2529
# Sat, 22 Jun 2024 01:03:51 GMT
SHELL [cmd /S /C]
# Sat, 22 Jun 2024 01:03:52 GMT
USER ContainerAdministrator
# Sat, 22 Jun 2024 01:03:55 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 22 Jun 2024 01:03:56 GMT
USER ContainerUser
# Sat, 22 Jun 2024 01:03:57 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Sat, 22 Jun 2024 01:03:58 GMT
ENV MONGO_VERSION=7.0.11
# Sat, 22 Jun 2024 01:04:23 GMT
COPY dir:19a9c5e7b92e67df364a58952a43fa9635a4cea236c07894dad5b3a27bc56ae4 in C:\mongodb 
# Sat, 22 Jun 2024 01:04:41 GMT
RUN mongod --version
# Sat, 22 Jun 2024 01:04:42 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 22 Jun 2024 01:04:43 GMT
EXPOSE 27017
# Sat, 22 Jun 2024 01:04:43 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a8c295c425a912de308ded279124ae45fec44d55a451843fe5877155417f453c`  
		Last Modified: Fri, 21 Jun 2024 02:24:34 GMT  
		Size: 120.5 MB (120499549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e48357e8b1d5e2b06626d1fdfcebb0681bfe8e4afcf5bee99bbb0105d9b9d0`  
		Last Modified: Sat, 22 Jun 2024 01:04:48 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2643f62de6b291768f308d8d39d4fecee48830e263787fad9486e6bfbfc8130`  
		Last Modified: Sat, 22 Jun 2024 01:04:48 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3acaffe55db22e5e86884680fd8ff12769d8988e258c4bc87e26955697953a`  
		Last Modified: Sat, 22 Jun 2024 01:04:48 GMT  
		Size: 76.9 KB (76875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9942761d2228238545f4a89a89f40fddd21ced0d57340627a289db7bef94bef5`  
		Last Modified: Sat, 22 Jun 2024 01:04:47 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785fd70882c444fcde12e574bb254679c6fcb605625af43548ed221c0949e974`  
		Last Modified: Sat, 22 Jun 2024 01:04:47 GMT  
		Size: 275.2 KB (275170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039dc2ebb9a52612dcda0ecd34b0240b845cf33398939e593226375aa7b6093d`  
		Last Modified: Sat, 22 Jun 2024 01:04:47 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ead288cf6b2fe1c203ba23563a7d6160634521accc2c6885eb7b8eeaeabf3ee`  
		Last Modified: Sat, 22 Jun 2024 01:05:33 GMT  
		Size: 618.2 MB (618172305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cbc25a64340d8ae1c5e5411e22fee7c23684aad85de40b409088c1bec84968f`  
		Last Modified: Sat, 22 Jun 2024 01:04:47 GMT  
		Size: 89.7 KB (89653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4500665aeb287ff58cc4b0ed2708043a38465c5323293a824e53cd589ca6d6a3`  
		Last Modified: Sat, 22 Jun 2024 01:04:46 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2024a3daca065cea6d590f5154e95e83e020450169258da3bdaa4d85fb7e32d`  
		Last Modified: Sat, 22 Jun 2024 01:04:46 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07df0db133aed6dc729283a93ffbe9493aab49a2129a15733e987dc64bfed422`  
		Last Modified: Sat, 22 Jun 2024 01:04:46 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-nanoserver` - windows version 10.0.17763.5936; amd64

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
