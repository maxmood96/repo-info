## `mongo:nanoserver`

```console
$ docker pull mongo@sha256:62de425825bf18a46a8e848baf353ac789bcfbc3579e6fa8109a1919cbd3f788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `mongo:nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull mongo@sha256:66bb5071c38d37d4942fbd061e1f2d8049c5144241d03f3e149d1560fcbe0a26
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **943.8 MB (943825742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7522b4ce8a4e2f43ad1ffce699fffbb2902ab806f49ae24ee42cce77a346cb6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 19:01:36 GMT
SHELL [cmd /S /C]
# Wed, 13 May 2026 19:01:36 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 19:01:43 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 13 May 2026 19:01:43 GMT
USER ContainerUser
# Wed, 13 May 2026 19:06:00 GMT
COPY multi:540d6dd70b1e7484f1958dc08b337aeb56cf8a92fe38be4c279dd406990d6935 in C:\Windows\System32\ 
# Wed, 13 May 2026 19:06:01 GMT
ENV MONGO_VERSION=8.2.9
# Wed, 13 May 2026 19:06:34 GMT
COPY dir:797d5456de657bf5ef433bde260feca63731b9a6c546ad4fcacd6eeaee1bc8aa in C:\mongodb 
# Wed, 13 May 2026 19:07:02 GMT
RUN mongod --version
# Wed, 13 May 2026 19:07:03 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 May 2026 19:07:03 GMT
EXPOSE 27017
# Wed, 13 May 2026 19:07:03 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78566578c202e9f9d25b1345b401a1c83428e3838b24d55904c19b26d467cd1d`  
		Last Modified: Wed, 13 May 2026 19:03:13 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9cb3b8020887c5de6ef885b31bebac91d8dadf15deb43b036fb3dd867e95c8`  
		Last Modified: Wed, 13 May 2026 19:03:13 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56945527616a97a47b1927c0fb3694e9e49ee58e14e60e644f3215cb95493e44`  
		Last Modified: Wed, 13 May 2026 19:03:12 GMT  
		Size: 77.9 KB (77866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3904a27d2beace3e46b5488d160441425db98b7e9ca84a82b29bf1d154fb9c9`  
		Last Modified: Wed, 13 May 2026 19:03:12 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e0ab4faade76d78ceda9abe20f1ca305d31d1b7fd203b8d48ba5a16f62226a`  
		Last Modified: Wed, 13 May 2026 19:07:14 GMT  
		Size: 275.2 KB (275207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08dc5b99236e3526fa2c4d3163636b5c9c4ccf32c0fcb22f9fdb84888baf097c`  
		Last Modified: Wed, 13 May 2026 19:07:14 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5d9c833138dc1419fab88cc10c74d4ed2031561d0508416f5c1288c448ee77`  
		Last Modified: Wed, 13 May 2026 19:08:13 GMT  
		Size: 816.3 MB (816340271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78e6d09bf0e6a3d10a3ac5317cace779d2320fa974939375a99bdfc81851579`  
		Last Modified: Wed, 13 May 2026 19:07:13 GMT  
		Size: 86.2 KB (86229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d10af691c5c9a640eb03be04e5505e20a9fe1ec4ec811a03192102a3e9b6acb`  
		Last Modified: Wed, 13 May 2026 19:07:12 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0a08fc80d37b617420566cb1a85333a6049485e93ef7825636f1dbca2ad402`  
		Last Modified: Wed, 13 May 2026 19:07:12 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ed99ea27c03db5ed46ad3a5555bacc64988215ce81d036ab584e4e3c84a720`  
		Last Modified: Wed, 13 May 2026 19:07:12 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
