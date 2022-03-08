## `mongo:nanoserver-1809`

```console
$ docker pull mongo@sha256:89c4b070fbc207f5b28f69cff5dec9b841ace73c3c7baeb09b598c060f173699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `mongo:nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull mongo@sha256:e7932ebd996ae49012dbb093ce00f996678deca8652a49e196572c6f680d5a0a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.9 MB (405880836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4907a2387ee3401e9c160279a88ec8fa9bff2acf241c6e1af56b1bc1099fddcb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Tue, 08 Mar 2022 20:14:56 GMT
SHELL [cmd /S /C]
# Tue, 08 Mar 2022 20:14:57 GMT
USER ContainerAdministrator
# Tue, 08 Mar 2022 20:15:11 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 08 Mar 2022 20:15:12 GMT
USER ContainerUser
# Tue, 08 Mar 2022 20:15:13 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Tue, 08 Mar 2022 20:15:14 GMT
ENV MONGO_VERSION=5.0.6
# Tue, 08 Mar 2022 20:15:46 GMT
COPY dir:8054396aef21c43e8eb1e82c0d52daca301fb548900656fb893eece57b5d6e88 in C:\mongodb 
# Tue, 08 Mar 2022 20:15:57 GMT
RUN mongo --version && mongod --version
# Tue, 08 Mar 2022 20:15:58 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 08 Mar 2022 20:15:59 GMT
EXPOSE 27017
# Tue, 08 Mar 2022 20:16:00 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f64bdb56c2b15796c35e920619553b18bea7fbac60e4268edd3d421d55630a01`  
		Last Modified: Tue, 08 Mar 2022 20:46:00 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f69819a0d246198af24821727ce1b7c304c8339daf63d64bf2e033f97616aa5`  
		Last Modified: Tue, 08 Mar 2022 20:46:00 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a00d1f0eb495a45f73cb8d64998ad09d7cd3aa1a6809f603fa9489240223763`  
		Last Modified: Tue, 08 Mar 2022 20:45:58 GMT  
		Size: 78.9 KB (78883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20f536a21c2557c84c26fd67d38465b53e4350049a6d51ee6664f9362fb7413`  
		Last Modified: Tue, 08 Mar 2022 20:45:57 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df76cdee36ec126e213687dc2507f0bbee3b68b153a53ebd9305baa78eb1bf3`  
		Last Modified: Tue, 08 Mar 2022 20:45:58 GMT  
		Size: 263.3 KB (263349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c05f519a2fce2b3263d86fb348b27da75a024577e6990b610801f10750f05f8`  
		Last Modified: Tue, 08 Mar 2022 20:45:57 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965f1d8b618bc5e4290cbac67da4cbc06c927129aaac3e38c58d51f01316ac94`  
		Last Modified: Tue, 08 Mar 2022 20:46:58 GMT  
		Size: 302.4 MB (302387659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bcec1c5f7ccd3ffc19af0e3e16b3c515ba68a61e94bd7472b6191561af7d9c6`  
		Last Modified: Tue, 08 Mar 2022 20:45:55 GMT  
		Size: 89.0 KB (88963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f7002e1a287446cba2050e753df06a1791a897b8ceed0bbcc1fb4aa975bd92`  
		Last Modified: Tue, 08 Mar 2022 20:45:55 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9100f6c996de6d11c847d66e39df3ff1834f1afd545ff73af6e2e45a770ec5b`  
		Last Modified: Tue, 08 Mar 2022 20:45:55 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d78e80043066458e9b18a26ba4fd14c14a52f0e6b7258d8a7918d3939a9820`  
		Last Modified: Tue, 08 Mar 2022 20:45:55 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
