## `mongo:6-nanoserver`

```console
$ docker pull mongo@sha256:90370fbd42b9b102bd8c7d9e0d17c565b98f92661bff8fa33d04a65177c6d6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `mongo:6-nanoserver` - windows version 10.0.20348.2402; amd64

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

### `mongo:6-nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull mongo@sha256:3a7e7ba05166fc1d7ab818794c368ed4a2b14d84a794081229fcf1d032cc9498
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.2 MB (626213628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d2ab77bcb38d0e7cd702339a63190f871af8bc152b030716f3c568f07402e4`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Wed, 10 Apr 2024 01:00:44 GMT
SHELL [cmd /S /C]
# Wed, 10 Apr 2024 01:00:45 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 01:00:47 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 10 Apr 2024 01:00:48 GMT
USER ContainerUser
# Wed, 10 Apr 2024 01:00:49 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Wed, 10 Apr 2024 01:00:50 GMT
ENV MONGO_VERSION=6.0.14
# Wed, 10 Apr 2024 01:01:24 GMT
COPY dir:254820e97691f1aa9249d91faf05efbef599ba0e97089379ceabe51f49c02c4a in C:\mongodb 
# Wed, 10 Apr 2024 01:01:33 GMT
RUN mongod --version
# Wed, 10 Apr 2024 01:01:34 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Apr 2024 01:01:34 GMT
EXPOSE 27017
# Wed, 10 Apr 2024 01:01:35 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c8042a2c0249b909abc2cbad3de179deac27a4408de0df459cb2d8194fed2e`  
		Last Modified: Wed, 10 Apr 2024 01:01:40 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a1567fdff13dd1e281292512e06b7fc2db153cb7bba991c5e0a5290ea0b7d0`  
		Last Modified: Wed, 10 Apr 2024 01:01:39 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd6465fd57fa2085d3b648764e66b016059c560fa26779ccc783a96c60d97eb`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 71.7 KB (71695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91657c8f6db32b605651901a143bd66dbe106b02c81a0be5bf1f2f17e43def5c`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e1cc4d1230907e74c8aad6a68283afb37a9ff3960beff3cf16daaff929a008`  
		Last Modified: Wed, 10 Apr 2024 01:01:39 GMT  
		Size: 267.1 KB (267062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:386bc9950fea20ee5eda726441a6508fa3ed91bea2dfff15001b51c3aa4e0d6e`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f3dd253cd5ee948c1a1346b2f081a7c34a14e43e0a49143bc42b2c3aa62112`  
		Last Modified: Wed, 10 Apr 2024 01:02:21 GMT  
		Size: 520.9 MB (520890916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6edb793114264d25de469acb466772e4de080c9ee2ab291b4e2b4423696d1e`  
		Last Modified: Wed, 10 Apr 2024 01:01:37 GMT  
		Size: 87.6 KB (87559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bf153868713925e0a0ff685a198c94d2166a082084ded8f832ee1b683e7c27`  
		Last Modified: Wed, 10 Apr 2024 01:01:37 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887f6956aa14b6c40ee9b24a73dfe2b1b007ce65e23866c6e7831131feeda4d0`  
		Last Modified: Wed, 10 Apr 2024 01:01:37 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f72cea48ee6e0aa6a0acbab6f6f32806b6f6ed65f422000ea94f9ac00e99b75`  
		Last Modified: Wed, 10 Apr 2024 01:01:37 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
