## `mongo:nanoserver`

```console
$ docker pull mongo@sha256:81707ab6b3cd8423507986079cf8b253e601384cac1feb37c433e59b5847ab19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `mongo:nanoserver` - windows version 10.0.20348.3207; amd64

```console
$ docker pull mongo@sha256:6378079fa79d1366569f447554567aec87ea9c768bb00a449e07465e833946b4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **891.0 MB (891016096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24c40251be03998004d28e24f06ba73ecf77b65a3df3b89e932e40fa0412b0f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Mon, 24 Feb 2025 22:38:30 GMT
SHELL [cmd /S /C]
# Mon, 24 Feb 2025 22:38:31 GMT
USER ContainerAdministrator
# Mon, 24 Feb 2025 22:38:33 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Mon, 24 Feb 2025 22:38:34 GMT
USER ContainerUser
# Mon, 24 Feb 2025 22:38:35 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Mon, 24 Feb 2025 22:38:36 GMT
ENV MONGO_VERSION=8.0.5
# Mon, 24 Feb 2025 22:39:02 GMT
COPY dir:a57177c3820715e7790c25cd1624ad61fd2701fb2fd637d2847e81498bfa8394 in C:\mongodb 
# Mon, 24 Feb 2025 22:39:26 GMT
RUN mongod --version
# Mon, 24 Feb 2025 22:39:26 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Feb 2025 22:39:26 GMT
EXPOSE 27017
# Mon, 24 Feb 2025 22:39:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9f40abd3471b9f8c33f3203f4a58df1a9b7c6d6f5d45ccef73053e220b1477`  
		Last Modified: Mon, 24 Feb 2025 22:39:31 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbf12af2f425aab37f6ed148e4dadb5656a074e04d25dd3902d240f20110be5`  
		Last Modified: Mon, 24 Feb 2025 22:39:31 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62b96f78cbcfa81dfa06c1bb0739ecca09b8c6975beb3e8bcf8590a147ead10`  
		Last Modified: Mon, 24 Feb 2025 22:39:30 GMT  
		Size: 77.5 KB (77503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088722c1c92b9bae6b28eab83ee96899967287dfdae88f7c4fa685b86d39e6bf`  
		Last Modified: Mon, 24 Feb 2025 22:39:30 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4668a6f10d6c5d203fb7bb56b66ecdb5f2517323058bf17ca55918bb3950aa`  
		Last Modified: Mon, 24 Feb 2025 22:39:30 GMT  
		Size: 275.1 KB (275149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c386dcbfa9dee2e542ec1fe92a04350f3f6be2e5f09702a8830bec8eb62aaa3f`  
		Last Modified: Mon, 24 Feb 2025 22:39:30 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdb2137893cae8d4c167c54077019ed29d5f4b6f8e72fbb32ba94ebd5846ddb`  
		Last Modified: Mon, 24 Feb 2025 22:40:31 GMT  
		Size: 769.9 MB (769891057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5b3a43c4c5827f1fdc2756fdc8f677943bcd7575f83adb67e716b34ccc5aec`  
		Last Modified: Mon, 24 Feb 2025 22:39:29 GMT  
		Size: 98.6 KB (98565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99e24912ff1690323d32becaf14de8bd2605f6c0edef86b08789a4374660ab4`  
		Last Modified: Mon, 24 Feb 2025 22:39:29 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5227687a372511c250f55728f6a33901b657945283954b4b566020e450e81f`  
		Last Modified: Mon, 24 Feb 2025 22:39:29 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5609fdb2990812c3f8f09207b751ebad6d1de53decdeedd38eb06cbeeb3bd7d2`  
		Last Modified: Mon, 24 Feb 2025 22:39:29 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull mongo@sha256:86e60c6bd46172c52e2aa343c127158c15df1e197244a8b51498d605b1e01491
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **877.2 MB (877230788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc536d0c38bbb01a20bddd3a5b11f50c0712c208e73a6b8de08e4b1f2be2a064`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Mon, 24 Feb 2025 22:34:35 GMT
SHELL [cmd /S /C]
# Mon, 24 Feb 2025 22:34:37 GMT
USER ContainerAdministrator
# Mon, 24 Feb 2025 22:34:39 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Mon, 24 Feb 2025 22:34:39 GMT
USER ContainerUser
# Mon, 24 Feb 2025 22:34:40 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Mon, 24 Feb 2025 22:34:41 GMT
ENV MONGO_VERSION=8.0.5
# Mon, 24 Feb 2025 22:35:10 GMT
COPY dir:a57177c3820715e7790c25cd1624ad61fd2701fb2fd637d2847e81498bfa8394 in C:\mongodb 
# Mon, 24 Feb 2025 22:35:28 GMT
RUN mongod --version
# Mon, 24 Feb 2025 22:35:28 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Feb 2025 22:35:29 GMT
EXPOSE 27017
# Mon, 24 Feb 2025 22:35:30 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a60a5738eadcccc56bc21dc7801c550b8b4a75b8525582d41a16283ccbf82c`  
		Last Modified: Mon, 24 Feb 2025 22:35:37 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53133954722e26e3984644e5f952b7f153356b9d9720bfc6c3e62f21a0514a5e`  
		Last Modified: Mon, 24 Feb 2025 22:35:38 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6b87ea8d98df2070317a6420c8059b4047ba6f96ba5970749ecdd71c560164`  
		Last Modified: Mon, 24 Feb 2025 22:35:36 GMT  
		Size: 68.8 KB (68759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989595056d12d534d530b026c1cabbbe424d7efa0d23f84add858fd57ef60b28`  
		Last Modified: Mon, 24 Feb 2025 22:35:36 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc521303bff096ca42f91043b3945d2058cbf1054fcaa7d9aa68148d8e57615`  
		Last Modified: Mon, 24 Feb 2025 22:35:36 GMT  
		Size: 275.2 KB (275159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14e5e9fa9878ce354dd746a71de302cf9cd817d307f237d6ca036542c543202`  
		Last Modified: Mon, 24 Feb 2025 22:35:36 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53a4db218870516186e2cbb8e713e10986914290b5587ef3100f624df3f2069`  
		Last Modified: Mon, 24 Feb 2025 22:36:33 GMT  
		Size: 769.9 MB (769891013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc2e3546f232c7d3dfb439fed94f821f6b9f37188ff26d4fe861f21b0da81d9`  
		Last Modified: Mon, 24 Feb 2025 22:35:34 GMT  
		Size: 73.1 KB (73110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bb14a40ce11c13e437d358a6ca58840f6ae9943d52f00242f9878bdece2beb`  
		Last Modified: Mon, 24 Feb 2025 22:35:34 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f30f39a3abe93b4d5b6bd19916f70c6c432ed83166c6d45649395a8b385d5c6`  
		Last Modified: Mon, 24 Feb 2025 22:35:34 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f7518985cd2f98fb9318479c1922935e1af0b1a5080ea088a53d64b9b79f10`  
		Last Modified: Mon, 24 Feb 2025 22:35:34 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
