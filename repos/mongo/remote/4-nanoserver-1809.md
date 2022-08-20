## `mongo:4-nanoserver-1809`

```console
$ docker pull mongo@sha256:dc9936938b65b26921f89a2893409a2d31208550e1fd56e1c5e3fe75ebfb233d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `mongo:4-nanoserver-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull mongo@sha256:63b4ab5b51c7dd988b8005c3b8496cacb97b2673bbbc77002c4709438f30342c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.6 MB (346618172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1549daf044e37775dbcbd1e5b6b828ec9f9b65f90968a4baa5abb726de1f0cf6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 13:04:30 GMT
SHELL [cmd /S /C]
# Wed, 10 Aug 2022 18:22:41 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 18:22:55 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 10 Aug 2022 18:22:56 GMT
USER ContainerUser
# Wed, 10 Aug 2022 18:22:57 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Sat, 20 Aug 2022 01:28:02 GMT
ENV MONGO_VERSION=4.4.16
# Sat, 20 Aug 2022 01:28:29 GMT
COPY dir:ffbeec6bd323929cd73de85592d4f6ca731152ee6be82baf8e4514fb53642dc6 in C:\mongodb 
# Sat, 20 Aug 2022 01:28:44 GMT
RUN mongo --version && mongod --version
# Sat, 20 Aug 2022 01:28:45 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 20 Aug 2022 01:28:45 GMT
EXPOSE 27017
# Sat, 20 Aug 2022 01:28:46 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9982991b820814ad737b2a161e973194e66b8d7b0a9890bee49cd158d7e77dec`  
		Last Modified: Wed, 10 Aug 2022 13:27:27 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7180e2213de155098394f0dbf886f68478c49bc5ef2c0977d6e28da9593090df`  
		Last Modified: Wed, 10 Aug 2022 18:55:17 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0b5eb91e7b8da02b963c0e45697ecd1e88fdea8a134974bf17366b2dc3a68e`  
		Last Modified: Wed, 10 Aug 2022 18:55:15 GMT  
		Size: 77.8 KB (77802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c59fe6b6f7e47222898a3f00c7f02b87dcb9f4480cf874d6f00b55cbcede826`  
		Last Modified: Wed, 10 Aug 2022 18:55:14 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ccf06a99cd0032feb37c8d5a167ba6372e41687f302366e20b947fe83bafe`  
		Last Modified: Wed, 10 Aug 2022 18:55:14 GMT  
		Size: 263.5 KB (263523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322fb93387046a2fb7625ae3243e836cd00a2cb9951c3ab314c744d2fbe56f16`  
		Last Modified: Sat, 20 Aug 2022 01:45:58 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a246af17e47e6007c6154f6bb050adc713522543b39be67cc2d77f0b0e23d014`  
		Last Modified: Sat, 20 Aug 2022 01:46:42 GMT  
		Size: 243.0 MB (242976076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8a8bf5559b4f288717b92a4dd975b36e71dfdf5209e9d00fb2fa13ca3a6cdc`  
		Last Modified: Sat, 20 Aug 2022 01:45:55 GMT  
		Size: 88.6 KB (88556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a680e4d8d1063a6b174dc805bb8cea010c498bfa4487424e2a015ca6d23cfcb7`  
		Last Modified: Sat, 20 Aug 2022 01:45:55 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d956339b264d8aa6e42fb123727d1e104d43f8bd0c5d07ac7c13eec353d84225`  
		Last Modified: Sat, 20 Aug 2022 01:45:55 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e084988e760fc398d0c79810a25727ea07c6fa89a467fc5605a4ebbae19eff2`  
		Last Modified: Sat, 20 Aug 2022 01:45:55 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
