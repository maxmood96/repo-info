## `mongo:nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:b5b6b24b0aeb85e1ca1360c2fdbeae2327d4204573a14f2b827a356e89810e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `mongo:nanoserver-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull mongo@sha256:e84d15c33177dc425764f3ef53c434f2a02579dbaaf0dd1f587e3817c59fe2c6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.6 MB (738599116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e965aa60b2f07d24727fe1dd810179b5d082b01ec0eb5b7015bcf288d554e8d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Tue, 30 Apr 2024 00:53:03 GMT
SHELL [cmd /S /C]
# Tue, 30 Apr 2024 00:53:03 GMT
USER ContainerAdministrator
# Tue, 30 Apr 2024 00:53:21 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 30 Apr 2024 00:53:21 GMT
USER ContainerUser
# Tue, 30 Apr 2024 00:53:23 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Tue, 30 Apr 2024 00:53:23 GMT
ENV MONGO_VERSION=7.0.9
# Tue, 30 Apr 2024 00:53:51 GMT
COPY dir:c5adfa4f029ebda75c02b0a22ffb5e95f91770da0e60bc0d59f3d814db6f0d71 in C:\mongodb 
# Tue, 30 Apr 2024 00:54:10 GMT
RUN mongod --version
# Tue, 30 Apr 2024 00:54:11 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 30 Apr 2024 00:54:11 GMT
EXPOSE 27017
# Tue, 30 Apr 2024 00:54:12 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7aca7d546f3aeb542c760f25fa34556326354bddebe3e8cf7cb9eef89dd152`  
		Last Modified: Tue, 30 Apr 2024 00:54:20 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be5dd4521b26f575331663a1f05924c8af2162e0fcaf81087bcdcf39f1efc85`  
		Last Modified: Tue, 30 Apr 2024 00:54:20 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c78bc09f8e2e47954dd51a8494c79ed76f0b0c89732cef326264a221597d15`  
		Last Modified: Tue, 30 Apr 2024 00:54:18 GMT  
		Size: 106.7 KB (106740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bebb9e10c9b71b645f064fc871eff11c71822c056c57a5b401c931e4d68de1`  
		Last Modified: Tue, 30 Apr 2024 00:54:18 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c11ab6227b7affac4a9c8556aec7678e5f930b0c3a6c87b5570a09b271d863de`  
		Last Modified: Tue, 30 Apr 2024 00:54:18 GMT  
		Size: 267.1 KB (267111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c652041ab99f5354b88b239fa0203177d4a19c952e1bf67c314825a082e8da`  
		Last Modified: Tue, 30 Apr 2024 00:54:18 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e633ab745d25469d5a8ffe4b727745a87924e5cdcff94755db4471c99dc583`  
		Last Modified: Tue, 30 Apr 2024 00:55:08 GMT  
		Size: 617.1 MB (617115357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fb7a96530720921d111b95ecd329454a27a939bae7159cb2bef57567e7e0d9`  
		Last Modified: Tue, 30 Apr 2024 00:54:16 GMT  
		Size: 108.9 KB (108881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bd1c3a2fa18b076768c66e1331fb7e910c4392e1f73c76116cf29cfd1625c4`  
		Last Modified: Tue, 30 Apr 2024 00:54:16 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c6c38fc131d43a29b81f998afbe1710e6e5f30c43571770187bed832838ac0`  
		Last Modified: Tue, 30 Apr 2024 00:54:16 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0965ada1ea428c402e1875fbd0d40801ecec76845abdc851cd638607288fbba`  
		Last Modified: Tue, 30 Apr 2024 00:54:16 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
