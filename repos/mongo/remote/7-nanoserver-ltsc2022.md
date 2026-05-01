## `mongo:7-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:044df9b61d635537b87aa02aedb91ca9558ce130ba0edbdac9326281a187d16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `mongo:7-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull mongo@sha256:07f04188970aaa061aae1ec5688934f85e9270635af69c2469bc5be579145801
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **750.2 MB (750166242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b39987dede409ebe8c86d173ab62afa83b899428aa9b5cbf25d55feef56e5ad`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Fri, 01 May 2026 07:13:01 GMT
SHELL [cmd /S /C]
# Fri, 01 May 2026 07:13:02 GMT
USER ContainerAdministrator
# Fri, 01 May 2026 07:13:15 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 01 May 2026 07:13:15 GMT
USER ContainerUser
# Fri, 01 May 2026 07:13:18 GMT
COPY multi:540d6dd70b1e7484f1958dc08b337aeb56cf8a92fe38be4c279dd406990d6935 in C:\Windows\System32\ 
# Fri, 01 May 2026 07:16:43 GMT
ENV MONGO_VERSION=7.0.32
# Fri, 01 May 2026 07:17:22 GMT
COPY dir:4eb584d0065c027dc88cadff0fd41a9f9c7265491130ff3967d737dd934ff24d in C:\mongodb 
# Fri, 01 May 2026 07:17:41 GMT
RUN mongod --version
# Fri, 01 May 2026 07:17:41 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 01 May 2026 07:17:42 GMT
EXPOSE 27017
# Fri, 01 May 2026 07:17:42 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3097855dfabc274b11e568ad24c2e1ade02688c7f713f4c5fbafd9f15bf1f76`  
		Last Modified: Fri, 01 May 2026 07:14:34 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4681be515aa241e2556a0e01c9b4af9101ea57d27eff49a755753ae65a36d2`  
		Last Modified: Fri, 01 May 2026 07:14:34 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1fc52a9b0da4df6afcc99605073807117534d5ae3969de52c2eeee8cd93a81`  
		Last Modified: Fri, 01 May 2026 07:14:32 GMT  
		Size: 74.2 KB (74220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977475972182b966955f03a4e3c9e625cbd58078e49d51158d7f27d0a267f724`  
		Last Modified: Fri, 01 May 2026 07:14:32 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf875ac859a86f36abfec1b75edbd76d3a5fe98033248b8575a3b72fa718730`  
		Last Modified: Fri, 01 May 2026 07:14:32 GMT  
		Size: 275.2 KB (275202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d405aefe1dc1a62a024a9844cc18ab3205e4d00df8cc30259dd156cf15e9c6bb`  
		Last Modified: Fri, 01 May 2026 07:17:48 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768dd3063eef3955ed1628d4b90cda8dc871ca2c1885bc9bff9e82e541cff592`  
		Last Modified: Fri, 01 May 2026 07:18:45 GMT  
		Size: 622.8 MB (622765859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ce138539efa57400a7ad59585e08f81e49f0bc26b1df427a8d49dceca621be`  
		Last Modified: Fri, 01 May 2026 07:17:46 GMT  
		Size: 87.6 KB (87556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cb547c234617e374ed12a80bb769aa4955080f39be26eba9afe7bbb2da4982`  
		Last Modified: Fri, 01 May 2026 07:17:46 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21abb6c3d929b6f6840a06a9a1ec5137d2f39b30746c77a4427d068ed11915a5`  
		Last Modified: Fri, 01 May 2026 07:17:46 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e809e060a9ae82c8eec7c9b193b8421bdc06640746445c42edd5edc56bf84454`  
		Last Modified: Fri, 01 May 2026 07:17:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
