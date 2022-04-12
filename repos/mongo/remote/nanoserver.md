## `mongo:nanoserver`

```console
$ docker pull mongo@sha256:43bc496f09d55e7884ad4d5b6925cfb48daaa4421d896f9b2b488c5d08c35bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.587; amd64
	-	windows version 10.0.17763.2686; amd64

### `mongo:nanoserver` - windows version 10.0.20348.587; amd64

```console
$ docker pull mongo@sha256:879003f8c5ad15e8bb62f88fb51a2a8f4bd7e0531fcad5313108d4d327d65913
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.5 MB (423488966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d49d46fe5c1458d170356b65503490594967ec2e0722170f04ead36af4a191`
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
# Mon, 11 Apr 2022 21:19:21 GMT
ENV MONGO_VERSION=5.0.7
# Mon, 11 Apr 2022 21:19:55 GMT
COPY dir:fb35459f874a32c339bad763a07251484cc13f01f904e8d607c367bab2629f9a in C:\mongodb 
# Mon, 11 Apr 2022 21:20:21 GMT
RUN mongo --version && mongod --version
# Mon, 11 Apr 2022 21:20:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 11 Apr 2022 21:20:23 GMT
EXPOSE 27017
# Mon, 11 Apr 2022 21:20:24 GMT
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
	-	`sha256:a1d4ccfd35e0e6c5c37126f284fb302bea07ffe78c92db8a07551763bdd7328c`  
		Last Modified: Mon, 11 Apr 2022 21:26:10 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2be8631bdc6a807592aa6de01a55665f292840203bb065d30691de743ac5b6`  
		Last Modified: Mon, 11 Apr 2022 21:27:01 GMT  
		Size: 305.6 MB (305593945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d45160515b00eb9da683256469947c9948b396b87eaa066af9a814efaab3ec`  
		Last Modified: Mon, 11 Apr 2022 21:26:08 GMT  
		Size: 60.5 KB (60510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9564baf8325895c37bc29ec6bd461e982c5510ddc93a835a812fc8cd502b48b9`  
		Last Modified: Mon, 11 Apr 2022 21:26:08 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b911ec1c0adec939ecc795f414e20970c67db17974026467c91967185026eacf`  
		Last Modified: Mon, 11 Apr 2022 21:26:07 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d76b0bd6f48c788dba81ad9461542cbfcd5ae10f1caec5728196001aeba34b`  
		Last Modified: Mon, 11 Apr 2022 21:26:07 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull mongo@sha256:f5255a87124505e79a4fad84f02ea44bb65b927ce2cca2747a365f0fa2ac48bb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.1 MB (409084795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90277e11ac854e90cb897bbef910fc9e5d1460290929e670ce8c6fdfb0a014db`
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
# Mon, 11 Apr 2022 21:20:34 GMT
ENV MONGO_VERSION=5.0.7
# Mon, 11 Apr 2022 21:21:06 GMT
COPY dir:fb35459f874a32c339bad763a07251484cc13f01f904e8d607c367bab2629f9a in C:\mongodb 
# Mon, 11 Apr 2022 21:21:20 GMT
RUN mongo --version && mongod --version
# Mon, 11 Apr 2022 21:21:21 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 11 Apr 2022 21:21:22 GMT
EXPOSE 27017
# Mon, 11 Apr 2022 21:21:22 GMT
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
	-	`sha256:ec7523e1bd8f43363f92b4e9f504ea5836e496ba19304da23eac1459289dbb18`  
		Last Modified: Mon, 11 Apr 2022 21:27:18 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b20ddcd7c8cd1d0887bf3af4aaaac9e157edb9daad776135215fd8d5a3bb2a8`  
		Last Modified: Mon, 11 Apr 2022 21:28:07 GMT  
		Size: 305.6 MB (305594502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4979303dc54ea49c446d7c66301d548a476e47d2019e76296392f1cfc6666de5`  
		Last Modified: Mon, 11 Apr 2022 21:27:16 GMT  
		Size: 85.7 KB (85676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c043903a7efcd965b0fc13facc46275ba4201b047aa1ac9fa6ab134aafd6db`  
		Last Modified: Mon, 11 Apr 2022 21:27:16 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e419b9d4d7a53206b4b58ac4f9659f92fa0e43d8c6a4620a2766b5d01e499f`  
		Last Modified: Mon, 11 Apr 2022 21:27:16 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f90b21be4e94db35fb31c05da9b77307b35b7c7b406c1ada9fe3f5c8bbab786`  
		Last Modified: Mon, 11 Apr 2022 21:27:16 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
