## `mongo:nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:944c119405065fdf6c4d5011001165b22e0ef328a4a22cba350adb9f0a070bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `mongo:nanoserver-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull mongo@sha256:4124bacf69d49924c6d242263bca476c322172e25604aad70065f8f7fb04de60
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.0 MB (737966110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d1e948544e283d31594388a6e7d2b9e514330c6ef95c59c0486361d4f65b224`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 10 May 2024 20:16:48 GMT
RUN Apply image 10.0.20348.2461
# Wed, 15 May 2024 22:52:43 GMT
SHELL [cmd /S /C]
# Wed, 15 May 2024 22:52:43 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 22:53:14 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 15 May 2024 22:53:15 GMT
USER ContainerUser
# Wed, 15 May 2024 22:53:17 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Wed, 15 May 2024 22:53:18 GMT
ENV MONGO_VERSION=7.0.9
# Wed, 15 May 2024 22:53:46 GMT
COPY dir:c5adfa4f029ebda75c02b0a22ffb5e95f91770da0e60bc0d59f3d814db6f0d71 in C:\mongodb 
# Wed, 15 May 2024 22:54:06 GMT
RUN mongod --version
# Wed, 15 May 2024 22:54:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 May 2024 22:54:08 GMT
EXPOSE 27017
# Wed, 15 May 2024 22:54:08 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:90b3a5622f8d62905d0a3029df4f91b934558ad375bef25c596214df31acac88`  
		Last Modified: Tue, 14 May 2024 17:22:15 GMT  
		Size: 120.4 MB (120425316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d4fc5421c6de617379092fad8738bc94c009a465e43ad66b2f8e6285b28101`  
		Last Modified: Wed, 15 May 2024 22:54:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8a54f181eec98f9580c299c72fb350de710fdbd19c714b6a36c9f3c434dba8`  
		Last Modified: Wed, 15 May 2024 22:54:13 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28eb3a793e19fe5eb3c32eee5783bbb87474741d8fd10139a6bae8bf0fda30b2`  
		Last Modified: Wed, 15 May 2024 22:54:12 GMT  
		Size: 71.7 KB (71702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfdcf24154681aef0f67fba0215ca6664b732bdb86a09a916579ba58e721b21`  
		Last Modified: Wed, 15 May 2024 22:54:12 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3468db74dd871574bffd163f56faa41e6b21a1ac36013fda72a999f6b6535083`  
		Last Modified: Wed, 15 May 2024 22:54:12 GMT  
		Size: 267.1 KB (267085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14d7dde323f195908c62f4704cc6de121060d65b779177eefec026bb38f9b1a`  
		Last Modified: Wed, 15 May 2024 22:54:12 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c45b515c9ade7925f4d0fdb67a439dfe56dee7df95fd8f645978e3a48755c8`  
		Last Modified: Wed, 15 May 2024 22:55:01 GMT  
		Size: 617.1 MB (617115185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb55abe78c315388b29e365395e33be72aa55c8966845d598b9de539109c9700`  
		Last Modified: Wed, 15 May 2024 22:54:11 GMT  
		Size: 79.4 KB (79444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d0feab076c408d8bf0a56729e2de7a5cec2465a91b03119d658415e0ce0878`  
		Last Modified: Wed, 15 May 2024 22:54:11 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4289354f1888e4959bd4546946db7f1351f50d86f76eceed22a87b85bb0cb45`  
		Last Modified: Wed, 15 May 2024 22:54:11 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b7d05e3729907978b4cab2665cf7650bdad15c8fe80dd4df2c2160c1d0c270`  
		Last Modified: Wed, 15 May 2024 22:54:11 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
