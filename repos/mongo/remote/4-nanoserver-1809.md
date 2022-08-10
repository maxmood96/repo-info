## `mongo:4-nanoserver-1809`

```console
$ docker pull mongo@sha256:580e9c92bcca8e01d255cf1380ee7f6a4ca28b444c6cebd8bf7ed6555de57433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `mongo:4-nanoserver-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull mongo@sha256:a5cd605490b7b7889d2a344e7f711290c5e2f6d3390f14460d5c47f155ed78ed
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.7 MB (345718660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c85185e5ab065544291348adba78f5c51f3459f4f11bbd9cf7938edbe21d74`
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
# Wed, 10 Aug 2022 18:28:58 GMT
ENV MONGO_VERSION=4.4.15
# Wed, 10 Aug 2022 18:29:25 GMT
COPY dir:11442d39c1a8be57a2edf36307e3c0f90a74de72a5c1c7d47a958b8e789a5794 in C:\mongodb 
# Wed, 10 Aug 2022 18:29:38 GMT
RUN mongo --version && mongod --version
# Wed, 10 Aug 2022 18:29:39 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Aug 2022 18:29:40 GMT
EXPOSE 27017
# Wed, 10 Aug 2022 18:29:40 GMT
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
	-	`sha256:ad072dd5e15cee6044366249daf04b4a8ffb0172f46372ad927f38a573316af9`  
		Last Modified: Wed, 10 Aug 2022 18:59:23 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226f28238b2522f12d5e240050ca2973e90f332cf4cbb2e52c77c0a5746a692d`  
		Last Modified: Wed, 10 Aug 2022 19:00:05 GMT  
		Size: 242.1 MB (242081689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92251457b3f1e748b496d142f0edefb1f38c3a6217b186363e17b47c1c53f681`  
		Last Modified: Wed, 10 Aug 2022 18:59:21 GMT  
		Size: 83.4 KB (83394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9ee0e16c9b588b3fea3106e74265e38c7582cb723f03a7ced2c3d2054c54f4`  
		Last Modified: Wed, 10 Aug 2022 18:59:20 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40244dc02d2ac1073a53406797d316f0326f81855bf0b95daca387b43705237f`  
		Last Modified: Wed, 10 Aug 2022 18:59:20 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7b9951bd4a64393168a2320967c1b8c8d756823bc6e3c1c62f8c2177d6229e`  
		Last Modified: Wed, 10 Aug 2022 18:59:20 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
