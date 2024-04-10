## `mongo:6-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:ead603790112798ba6eddb0b7434d31deb77fff023d3269c03592b05bb314125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `mongo:6-nanoserver-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull mongo@sha256:cea55226a5d8cad2052951e4881332105e825118a400a8e30772a9294f051ce5
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.3 MB (642332911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6b8ad63d4b295071c44bb194a9657df582b19a0d4ede147014f5716f99d750`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Wed, 10 Apr 2024 01:01:38 GMT
SHELL [cmd /S /C]
# Wed, 10 Apr 2024 01:01:38 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 01:01:41 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 10 Apr 2024 01:01:42 GMT
USER ContainerUser
# Wed, 10 Apr 2024 01:01:44 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Wed, 10 Apr 2024 01:01:44 GMT
ENV MONGO_VERSION=6.0.14
# Wed, 10 Apr 2024 01:02:07 GMT
COPY dir:254820e97691f1aa9249d91faf05efbef599ba0e97089379ceabe51f49c02c4a in C:\mongodb 
# Wed, 10 Apr 2024 01:02:21 GMT
RUN mongod --version
# Wed, 10 Apr 2024 01:02:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Apr 2024 01:02:23 GMT
EXPOSE 27017
# Wed, 10 Apr 2024 01:02:24 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe035322b97d323052df700eaf6ca1438ec22463789f1bca5a8553dbc265c9`  
		Last Modified: Wed, 10 Apr 2024 01:02:28 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6bb672b9b1dd86c8c2e36dda089c0212feee311747bf46accf18f39c543af91`  
		Last Modified: Wed, 10 Apr 2024 01:02:28 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3f645d9b3fdce3c0aeadb354a4eb37b0e0894912675cccf390c4a91614fd54`  
		Last Modified: Wed, 10 Apr 2024 01:02:27 GMT  
		Size: 75.5 KB (75458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbfc152902c3295a2737c95a29291a1431941b5c2d93cbf6f797c57dc94d8e6`  
		Last Modified: Wed, 10 Apr 2024 01:02:27 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4ceb47a8f84828c953ef0ee442b9107887316b0f6f5370033c7b0dbcd0542c`  
		Last Modified: Wed, 10 Apr 2024 01:02:27 GMT  
		Size: 267.1 KB (267079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9877e0319cf4bf28de3c00c990e61e95273a4dbd6720d6bc3339d36f4401406d`  
		Last Modified: Wed, 10 Apr 2024 01:02:27 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d4666823f98279e2b90815dadb0956d497587118949963cfac1546b3bce673`  
		Last Modified: Wed, 10 Apr 2024 01:03:10 GMT  
		Size: 520.9 MB (520890998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76abc9412939e55593eaab8ea67b3f1cf1859d25c4875e37b0a9f8eab8cbdb29`  
		Last Modified: Wed, 10 Apr 2024 01:02:26 GMT  
		Size: 98.3 KB (98335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28bdf94bcd2d71155546c9c8054521cc9fa7a6c9f8bc194f78976d834386065`  
		Last Modified: Wed, 10 Apr 2024 01:02:26 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb7ebc03b868ebd3e77d9aa7b3abe4919eb3c33c034d341361faf45f985085e`  
		Last Modified: Wed, 10 Apr 2024 01:02:26 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58db7b79fceec05d11312534298a35662e27bdbda615aedf0515fc2f060d39d`  
		Last Modified: Wed, 10 Apr 2024 01:02:26 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
