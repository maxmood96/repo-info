## `mongo:nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:adf0e217baa187bc37ad9c8a32a2ff63db369e9a3a8aa57fe3aa9f2a2c25162a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.587; amd64

### `mongo:nanoserver-ltsc2022` - windows version 10.0.20348.587; amd64

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
