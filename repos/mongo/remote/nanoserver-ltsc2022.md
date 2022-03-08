## `mongo:nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:28b9079c157d0f2c23fec6352a37d85e2c20947c721214024b3aea6338341ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.587; amd64

### `mongo:nanoserver-ltsc2022` - windows version 10.0.20348.587; amd64

```console
$ docker pull mongo@sha256:72584bdb9a965ae6342c7bb72192e3b1d032e86a3b3876ece1f2683f2fa9ad05
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.3 MB (420274194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79864eee8f4d827a52323772cd190d04ca16d4c1bbf6e0c2b38ec730899054f2`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 03 Mar 2022 04:50:34 GMT
RUN Apply image ltsc2022-amd64
# Tue, 08 Mar 2022 20:12:59 GMT
SHELL [cmd /S /C]
# Tue, 08 Mar 2022 20:13:00 GMT
USER ContainerAdministrator
# Tue, 08 Mar 2022 20:13:22 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 08 Mar 2022 20:13:23 GMT
USER ContainerUser
# Tue, 08 Mar 2022 20:13:24 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Tue, 08 Mar 2022 20:13:25 GMT
ENV MONGO_VERSION=5.0.6
# Tue, 08 Mar 2022 20:14:04 GMT
COPY dir:8054396aef21c43e8eb1e82c0d52daca301fb548900656fb893eece57b5d6e88 in C:\mongodb 
# Tue, 08 Mar 2022 20:14:34 GMT
RUN mongo --version && mongod --version
# Tue, 08 Mar 2022 20:14:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 08 Mar 2022 20:14:36 GMT
EXPOSE 27017
# Tue, 08 Mar 2022 20:14:37 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:dad81795ce109a7e20ebf80ad31925797ed97f9ba2a559f13f96ce3be5ea712b`  
		Size: 117.5 MB (117485491 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1c729ab19fa1794c04e2296ab2468daa560c676da6b333af3a86d94c1dc68b9`  
		Last Modified: Tue, 08 Mar 2022 20:39:41 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f61b1893147a039d62fd4276d6cee74f0622039d39ed0e5027afbfe44bcda3f`  
		Last Modified: Tue, 08 Mar 2022 20:39:41 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ac4092d7ed9fea813a3de075af51547d693d898dcb94e9b3417d59269dfc63`  
		Last Modified: Tue, 08 Mar 2022 20:39:39 GMT  
		Size: 77.5 KB (77460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674a85a799efa796f60cf92518b6d18b3bb81d145fef57569bbf63d6f660a52b`  
		Last Modified: Tue, 08 Mar 2022 20:39:39 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8faf98d39c89d56a78fe9cedf415d3a0f709d9abd2b63601cf66246f7600c0`  
		Last Modified: Tue, 08 Mar 2022 20:39:39 GMT  
		Size: 263.5 KB (263501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61b618311e4178acb6e497ab57d48bb23682a713b269c54c3c4b8def9685151`  
		Last Modified: Tue, 08 Mar 2022 20:39:39 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933b6055c0b3380d34ea59ce3aa51bc2e922b6177a5574640a7739168dd692d1`  
		Last Modified: Tue, 08 Mar 2022 20:45:36 GMT  
		Size: 302.4 MB (302387766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c110dbb3c7f5d085b2437cf6918837a2ccfd1220186bfda4878966a8f78fd8`  
		Last Modified: Tue, 08 Mar 2022 20:39:37 GMT  
		Size: 52.1 KB (52150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd10632f535b2a6d850ec150dd36675880d2e87b60a41683898592c564d4bad7`  
		Last Modified: Tue, 08 Mar 2022 20:39:37 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09390ce6bc00c98ac8326398295a98ec604b19d49ed1e36b2799ff0304876b2f`  
		Last Modified: Tue, 08 Mar 2022 20:39:37 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5761df2ffa56be3ff78d0bb90dbb44085fccdb5cd397707fbb528f25c57f59f4`  
		Last Modified: Tue, 08 Mar 2022 20:39:37 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
