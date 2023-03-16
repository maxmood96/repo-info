## `mongo:6-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:34c61240e86fdb33f04d7c44826c2f2ea965d94ab8d027cbeb477c6ad31f4b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1607; amd64

### `mongo:6-nanoserver-ltsc2022` - windows version 10.0.20348.1607; amd64

```console
$ docker pull mongo@sha256:66f674ea896fce7c32aed4887ee77c9cdca600041240c29992fd5873e1cc7aba
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.9 MB (636889583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7432b45889eb7c97cedd81567c0020bd725960f5bc24b0c8f6d1170329cb54b9`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 10 Mar 2023 06:31:34 GMT
RUN Apply image 10.0.20348.1607
# Thu, 16 Mar 2023 02:15:36 GMT
SHELL [cmd /S /C]
# Thu, 16 Mar 2023 03:04:16 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 03:05:08 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 16 Mar 2023 03:05:08 GMT
USER ContainerUser
# Thu, 16 Mar 2023 03:05:10 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Thu, 16 Mar 2023 03:05:11 GMT
ENV MONGO_VERSION=6.0.5
# Thu, 16 Mar 2023 03:06:14 GMT
COPY dir:8cafabdc84824168ccb42f1fb38dd461d1f5833e45f22346735df9067c52e6a6 in C:\mongodb 
# Thu, 16 Mar 2023 03:07:01 GMT
RUN mongod --version
# Thu, 16 Mar 2023 03:07:02 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Mar 2023 03:07:03 GMT
EXPOSE 27017
# Thu, 16 Mar 2023 03:07:04 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7abf0a70d48bf65f3d985f5780d4bdaece36f1f4bb8be10d5a6aacce33dacc75`  
		Last Modified: Thu, 16 Mar 2023 01:54:24 GMT  
		Size: 122.2 MB (122171731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa68b8cf98c4e81d0a56e6860ff5347ca921b2991f0fca1a397b892e862ec97`  
		Last Modified: Thu, 16 Mar 2023 02:47:12 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38818021eafe80428d533486402f82f6a153761f59981c81574a3e0c2408dc5`  
		Last Modified: Thu, 16 Mar 2023 03:46:07 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65de860560f9b0e2f325b55686740703531054e4be4a3e58f40d88e3d9e969b`  
		Last Modified: Thu, 16 Mar 2023 03:46:05 GMT  
		Size: 84.6 KB (84635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7402b3f8ba1353ed1a390bc558b163d5c7f7c70f9889ab381b34e82d05cc0e9c`  
		Last Modified: Thu, 16 Mar 2023 03:46:05 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ae78c150482136567c45af704acfc534370b9ba2d665910eed3a5671a8c682`  
		Last Modified: Thu, 16 Mar 2023 03:46:05 GMT  
		Size: 267.2 KB (267181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f59abd5db51bf249d3423fad507af0d6699655b30f2e821eeaf7ead9f2fd95e`  
		Last Modified: Thu, 16 Mar 2023 03:46:04 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb578dfbe1eb56766881ea0c7c70d9938174f1a53d79075a02aa8251c77aba5`  
		Last Modified: Thu, 16 Mar 2023 03:47:33 GMT  
		Size: 514.3 MB (514297446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e91b1faf5209bef9b0d6964c50256db6b9b9ad6a46fd17e2dad732d17d19397`  
		Last Modified: Thu, 16 Mar 2023 03:46:03 GMT  
		Size: 60.5 KB (60473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3bc445292f72195a963656f5300d7cb3dffa705d66a8bc55bae4ae9293b335`  
		Last Modified: Thu, 16 Mar 2023 03:46:02 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b71fae966a42c96847c44a1df31ea4d10559862781d3b006e59891ea466107`  
		Last Modified: Thu, 16 Mar 2023 03:46:02 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cf430aaa46e1e46be8a84814a90384a1117b9b8fbc189a0289454261186ce3`  
		Last Modified: Thu, 16 Mar 2023 03:46:03 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
