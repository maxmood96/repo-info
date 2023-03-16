## `mongo:5-nanoserver`

```console
$ docker pull mongo@sha256:af96220e554928e3ee7b3ee7e9848e7c96ebf8fd1088ba6c83522330fc3a0d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1607; amd64
	-	windows version 10.0.17763.4131; amd64

### `mongo:5-nanoserver` - windows version 10.0.20348.1607; amd64

```console
$ docker pull mongo@sha256:bd5e6699995987a944f222503a3c646b00987eff2a1239eb5a8345e12737e416
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.7 MB (433719482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a29710c781646f03e94807bf1f4fdb524e018f5554d7a04fbf8faebaf3a1538`
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
# Thu, 16 Mar 2023 03:17:16 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Thu, 16 Mar 2023 03:17:17 GMT
ENV MONGO_VERSION=5.0.15
# Thu, 16 Mar 2023 03:17:54 GMT
COPY dir:fb2387548719c31821557ec72e326693578135a8ffa29c575b7481c4a733db86 in C:\mongodb 
# Thu, 16 Mar 2023 03:18:38 GMT
RUN mongo --version && mongod --version
# Thu, 16 Mar 2023 03:18:39 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Mar 2023 03:18:40 GMT
EXPOSE 27017
# Thu, 16 Mar 2023 03:18:40 GMT
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
	-	`sha256:b74d41f41e06a86d9900047685f97aca38309bc334a853ef39c6d49dd50321af`  
		Last Modified: Thu, 16 Mar 2023 03:51:56 GMT  
		Size: 263.4 KB (263383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8748b323623ec4b4c38c99eb612ff8ac58c6e1484d7883e3946a7e4e4c793854`  
		Last Modified: Thu, 16 Mar 2023 03:51:56 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e56396565e60ce5308df889f46e41053a3eee567b1b008b5831caa59390074d`  
		Last Modified: Thu, 16 Mar 2023 03:52:56 GMT  
		Size: 311.1 MB (311131385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fce3a93081322dd083cee5be6dde006a481c91612c7416829a2d87816270fc8`  
		Last Modified: Thu, 16 Mar 2023 03:51:54 GMT  
		Size: 60.5 KB (60480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7065a15f0dc4f24c00538b6c283dec418aa6fd9da05192dfc64c7ac57f58f89a`  
		Last Modified: Thu, 16 Mar 2023 03:51:54 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97304f8d959fbfb34e48dacdb9608849fbe53183f0138a4d71bcd5ac4c9cc94d`  
		Last Modified: Thu, 16 Mar 2023 03:51:54 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ef9fa56296adc7b46b9aa2d6ea44b32d8603c15de1eb2e92198c4652b9ddd1`  
		Last Modified: Thu, 16 Mar 2023 03:51:54 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-nanoserver` - windows version 10.0.17763.4131; amd64

```console
$ docker pull mongo@sha256:52afa3415d9094b59c5debd368c5d5a53fe1d667b91213bbe07241732de3c90c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.2 MB (418232113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678851f765da57161925aa86150f6d65cc4c14a650d9684380409bba7b3e8499`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 02:20:46 GMT
SHELL [cmd /S /C]
# Thu, 16 Mar 2023 03:07:20 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 03:08:00 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 16 Mar 2023 03:08:01 GMT
USER ContainerUser
# Thu, 16 Mar 2023 03:19:02 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Thu, 16 Mar 2023 03:19:02 GMT
ENV MONGO_VERSION=5.0.15
# Thu, 16 Mar 2023 03:19:41 GMT
COPY dir:fb2387548719c31821557ec72e326693578135a8ffa29c575b7481c4a733db86 in C:\mongodb 
# Thu, 16 Mar 2023 03:20:26 GMT
RUN mongo --version && mongod --version
# Thu, 16 Mar 2023 03:20:27 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Mar 2023 03:20:28 GMT
EXPOSE 27017
# Thu, 16 Mar 2023 03:20:29 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5cc414fce78380e134ec2315d713a8a9040bff5d1298887a2a68029cfc0922`  
		Last Modified: Thu, 16 Mar 2023 02:48:05 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1a233254ba5f14e1070a15977726a5b4df112b5b0262b272ea76a367494e42`  
		Last Modified: Thu, 16 Mar 2023 03:47:51 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3263ac1a13295ff69bbe88e22f0e3624eaac310642d5dcc0a5236ef526d1d4bd`  
		Last Modified: Thu, 16 Mar 2023 03:47:49 GMT  
		Size: 69.4 KB (69440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e43090cb5cef65a97ac19c1867ef724287872689f8abc9c92bdddefa56ea21`  
		Last Modified: Thu, 16 Mar 2023 03:47:49 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d627e884652ce7cc34439052c446c4167e28e502301e59a05a1f97f41eee4110`  
		Last Modified: Thu, 16 Mar 2023 03:53:09 GMT  
		Size: 263.4 KB (263397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2401806a697f9b53123369c619a3aeed2dd39b24ddabbc09f3c7595ca349c46d`  
		Last Modified: Thu, 16 Mar 2023 03:53:09 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef152450dfd28896c4d69d90a8aab140667a928b5c9d4af9c26a9eed98cf8785`  
		Last Modified: Thu, 16 Mar 2023 03:54:13 GMT  
		Size: 311.1 MB (311131417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c3d99b33657ef9b2858a3306a5aca0af12e1da4606e1ac755532f4fd6e9104`  
		Last Modified: Thu, 16 Mar 2023 03:53:07 GMT  
		Size: 75.8 KB (75816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd2da59d09b516a67b19268d7f7401b1e6619fc25bd5bd8fb0a1a5163432ca8`  
		Last Modified: Thu, 16 Mar 2023 03:53:07 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980b492346eacabc49034be8376d3bd5cb7a8ada1fc69cc3116c2e2df051b08b`  
		Last Modified: Thu, 16 Mar 2023 03:53:07 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0ace2b982bc422e8acc21e37c6e0a38e0f9dfc8d408c4d85102fb8c5eae161`  
		Last Modified: Thu, 16 Mar 2023 03:53:07 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
