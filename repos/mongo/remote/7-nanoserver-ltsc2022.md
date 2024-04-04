## `mongo:7-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:a4372a8301b636a9254a3675c66da96111d6cf9c7423edb110e54e1ce5825be5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `mongo:7-nanoserver-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull mongo@sha256:5623c8cd57549465794442099ddda3237e5043a6d21af96128dcef4bae2d6f5f
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **737.7 MB (737738254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03aeb1dbeff2ca6d339280b1f1b54c4aba8c334bdeddf5cdb6fc430bdd0dca40`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 05 Mar 2024 19:20:30 GMT
RUN Apply image 10.0.20348.2340
# Wed, 03 Apr 2024 21:51:10 GMT
SHELL [cmd /S /C]
# Wed, 03 Apr 2024 21:51:11 GMT
USER ContainerAdministrator
# Wed, 03 Apr 2024 21:51:33 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 03 Apr 2024 21:51:33 GMT
USER ContainerUser
# Wed, 03 Apr 2024 21:51:35 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Wed, 03 Apr 2024 21:51:35 GMT
ENV MONGO_VERSION=7.0.8
# Wed, 03 Apr 2024 21:52:01 GMT
COPY dir:4a345f3390b35b1b56d808fec53236340ce99accef71314ef04d72a18e5c5b17 in C:\mongodb 
# Wed, 03 Apr 2024 21:52:17 GMT
RUN mongod --version
# Wed, 03 Apr 2024 21:52:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 03 Apr 2024 21:52:18 GMT
EXPOSE 27017
# Wed, 03 Apr 2024 21:52:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:94ec3b200bababb5c0b6605ad82c23779d8f918fbfe1ef5d1cf51be6f12fa749`  
		Last Modified: Tue, 12 Mar 2024 19:42:37 GMT  
		Size: 120.7 MB (120702694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c31f05dd83a365212e3eccdf7ed24ebb4638fb1e7f92f723265ba10d0f184e`  
		Last Modified: Wed, 03 Apr 2024 21:52:23 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815d60597321cada9cae7fbcdcc095e40a5066f595cf8a921b0187f62bf7500c`  
		Last Modified: Wed, 03 Apr 2024 21:52:23 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cee37cc6b58254f8a063c35b343533f1f89d34e106d81eddc85d4b259c36132`  
		Last Modified: Wed, 03 Apr 2024 21:52:23 GMT  
		Size: 89.2 KB (89189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f39236ef75d06b6459750453d8578b65ace5ddb87e069f61aeb537855a3a1fa`  
		Last Modified: Wed, 03 Apr 2024 21:52:22 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2048fb10020a27ba5757f47377cec817ac6ab31877249f08fca4df6273c4a0c2`  
		Last Modified: Wed, 03 Apr 2024 21:52:22 GMT  
		Size: 267.1 KB (267085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f47a3d17eccbd5552c956ec67d51a524e5a66860ec477f3024b266244a1526`  
		Last Modified: Wed, 03 Apr 2024 21:52:22 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f6e046fca144ea754e28a33bf5a3cf529210e1ce621d45c093fe09dc5b5a43`  
		Last Modified: Wed, 03 Apr 2024 21:53:11 GMT  
		Size: 616.6 MB (616579556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780bf9339304b284d6de9165a27ec1de9a6315a46c21e54655fe25833e8d2f9a`  
		Last Modified: Wed, 03 Apr 2024 21:52:21 GMT  
		Size: 92.4 KB (92435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f36e7f9329dda1717c86f2a6229e3a08d216c12ed4236b332fabe191e47056`  
		Last Modified: Wed, 03 Apr 2024 21:52:21 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57b64b0384fc9f35c6578a936c52a9977bd5923d55c07b3335beaa80bca8ae8`  
		Last Modified: Wed, 03 Apr 2024 21:52:21 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362343bb756c9f2daf8b30328ae20fdf90cf7c4a6e46861f5d702222bb3f54ba`  
		Last Modified: Wed, 03 Apr 2024 21:52:21 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
