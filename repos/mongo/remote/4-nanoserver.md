## `mongo:4-nanoserver`

```console
$ docker pull mongo@sha256:6d680ad7c923758143af77e56593edd9f6d460a62b5b9bedef6433681847f43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.587; amd64
	-	windows version 10.0.17763.2686; amd64

### `mongo:4-nanoserver` - windows version 10.0.20348.587; amd64

```console
$ docker pull mongo@sha256:f1df35bd970982ed585dd829d317a3068551587504feae6587621d0af2ed18b1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.5 MB (359507255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31244bd291169dbd283f6ef7c0576b7384f3e7a805575dffc07a51ffd44e8a1f`
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
# Tue, 08 Mar 2022 20:20:24 GMT
ENV MONGO_VERSION=4.4.13
# Tue, 08 Mar 2022 20:20:49 GMT
COPY dir:cb2795f5b405c92d2e3366f5e962d386ae580b206db49ff53e53730c9b68815c in C:\mongodb 
# Tue, 08 Mar 2022 20:21:11 GMT
RUN mongo --version && mongod --version
# Tue, 08 Mar 2022 20:21:12 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 08 Mar 2022 20:21:12 GMT
EXPOSE 27017
# Tue, 08 Mar 2022 20:21:13 GMT
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
	-	`sha256:bd50cd5c7dd65358068a51c1421dedcd4dff66cd773e6fed432f34951b1f07de`  
		Last Modified: Tue, 08 Mar 2022 20:53:18 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c15442aed36a181a0a0f6fb8b9af08c62eebaae7ce1f41bf2b7196d65ddeb8`  
		Last Modified: Tue, 08 Mar 2022 20:53:58 GMT  
		Size: 241.6 MB (241620407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b834253bed3501eb7d7b4765653d8c1b67f6a3d0a66e82130c89c8e074f4e7e`  
		Last Modified: Tue, 08 Mar 2022 20:53:16 GMT  
		Size: 52.3 KB (52344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838145fa511a775e773e552494ac280f92e18c53c84a6063b151a5afd7e3a832`  
		Last Modified: Tue, 08 Mar 2022 20:53:16 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a7e18f4b41b5af408681745ac020c0c1bb473003274ede7225ed1b1491621b`  
		Last Modified: Tue, 08 Mar 2022 20:53:16 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f2b9c587c498abac02eeb594a6c5c609cc050eb849265ba1024e6813265c88`  
		Last Modified: Tue, 08 Mar 2022 20:53:16 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull mongo@sha256:dee618a62f7b5961d68fef639da572f56422464388993b377bedd115305a7ab9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345114036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfaf8dce869f96cd21a2fcf7361bbaede2f75696a8149e84151858c57d2fcde4`
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
# Tue, 08 Mar 2022 20:21:29 GMT
ENV MONGO_VERSION=4.4.13
# Tue, 08 Mar 2022 20:21:53 GMT
COPY dir:cb2795f5b405c92d2e3366f5e962d386ae580b206db49ff53e53730c9b68815c in C:\mongodb 
# Tue, 08 Mar 2022 20:22:07 GMT
RUN mongo --version && mongod --version
# Tue, 08 Mar 2022 20:22:08 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 08 Mar 2022 20:22:09 GMT
EXPOSE 27017
# Tue, 08 Mar 2022 20:22:10 GMT
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
	-	`sha256:4833fb384e9f514b629c70e3f4f4e4b326a171a378f4ed005fa11ef42e78dd00`  
		Last Modified: Tue, 08 Mar 2022 20:54:15 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c69696e510d48478c8a763ed3cc3f7d9e21dace92c7dab3d11e04ec97616825`  
		Last Modified: Tue, 08 Mar 2022 20:59:01 GMT  
		Size: 241.6 MB (241620396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7ccb1f4cdf2c0722afca874cb37a3876aa51b382fd964e4bce10725845f3ed`  
		Last Modified: Tue, 08 Mar 2022 20:54:13 GMT  
		Size: 89.1 KB (89053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb657c0e2b06eb3a789f0fdd1ef6ad0869d5f32d47b43e243a8f0fa48a66dc4`  
		Last Modified: Tue, 08 Mar 2022 20:54:12 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c730e6c74dfd8d6f096fe18b2334d7257b5e1975ddf1fd80db1fef08c05769`  
		Last Modified: Tue, 08 Mar 2022 20:54:12 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d316914c7b72074a075a9b0b36d9e77404ee9eefe516eb61e25fcf53136931d`  
		Last Modified: Tue, 08 Mar 2022 20:54:13 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
