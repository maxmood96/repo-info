## `mongo:4-nanoserver`

```console
$ docker pull mongo@sha256:f4395b7dec8916a1b70d1331599ad9b05019d32de428e6e0ecb57bde34eebe53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.887; amd64
	-	windows version 10.0.17763.3287; amd64

### `mongo:4-nanoserver` - windows version 10.0.20348.887; amd64

```console
$ docker pull mongo@sha256:6c2ccfb41ee434abc3023fd754a4d8b392d22d9a0ad51401494e92a6f6fa9223
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.5 MB (361473272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac848a063d7270c78808569d7200fc90e77a7ccb80ef7a88e53b8fc0f936f3a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 06 Aug 2022 18:05:23 GMT
RUN Apply image 10.0.20348.887
# Wed, 10 Aug 2022 13:00:01 GMT
SHELL [cmd /S /C]
# Wed, 10 Aug 2022 18:21:28 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 18:21:43 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 10 Aug 2022 18:21:43 GMT
USER ContainerUser
# Wed, 10 Aug 2022 18:21:45 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Sat, 20 Aug 2022 01:26:59 GMT
ENV MONGO_VERSION=4.4.16
# Sat, 20 Aug 2022 01:27:25 GMT
COPY dir:ffbeec6bd323929cd73de85592d4f6ca731152ee6be82baf8e4514fb53642dc6 in C:\mongodb 
# Sat, 20 Aug 2022 01:27:45 GMT
RUN mongo --version && mongod --version
# Sat, 20 Aug 2022 01:27:45 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 20 Aug 2022 01:27:46 GMT
EXPOSE 27017
# Sat, 20 Aug 2022 01:27:47 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2ebf439f800cd4c1fccaf4a0545e6bff60caa5141295c8ab81f6c525073c423d`  
		Size: 118.1 MB (118088450 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:28bba27fcdd9c2f008a9c22db6c16dece3a5c3a49f9fac9447924071999adf65`  
		Last Modified: Wed, 10 Aug 2022 13:26:19 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea577aa22b29cf1143b45e9c9507d3cb6afba550ab0e0f1d34cc0f3bc394fb8`  
		Last Modified: Wed, 10 Aug 2022 18:54:06 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573d7b3cd6a4597d6a752c3c5d397d443396335384d76305346cc9cd7d307fe8`  
		Last Modified: Wed, 10 Aug 2022 18:54:04 GMT  
		Size: 76.2 KB (76190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24136b33c2554c6e408883876b2a54dba6f355751bc713713bcf47ecaac222`  
		Last Modified: Wed, 10 Aug 2022 18:54:04 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa7e2c4308c7bcabbfca14bc95b704c0077c76f9311295c08a306d000fc3c59`  
		Last Modified: Wed, 10 Aug 2022 18:54:04 GMT  
		Size: 263.5 KB (263480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e797d3e713ccce6def6ca4bb2a8b1eb997753877f8353927e37ba64a7df7e6c1`  
		Last Modified: Sat, 20 Aug 2022 01:44:56 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e7b2200d0efc3b01d0101eaa717eafec9da010255592471b1635611f7a3769`  
		Last Modified: Sat, 20 Aug 2022 01:45:42 GMT  
		Size: 243.0 MB (242976112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46bb0ea2fe6e16dda491a7f00c81bf9ef9cca76e44b21900142a00abf6ea110`  
		Last Modified: Sat, 20 Aug 2022 01:44:54 GMT  
		Size: 60.9 KB (60894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eab953c1f0f17af55b8edd0acd4e74a421d38de0f0705fe9b489f816f372129`  
		Last Modified: Sat, 20 Aug 2022 01:44:54 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70faba7b3fe001e9f866b40563d5138af13c27925f81aaf806a19873c0ee81e`  
		Last Modified: Sat, 20 Aug 2022 01:44:54 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba4d691a8537ac75816139575b8c90a8d1931f84e236ca2f8f380f78c2c7a32`  
		Last Modified: Sat, 20 Aug 2022 01:44:54 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-nanoserver` - windows version 10.0.17763.3287; amd64

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
