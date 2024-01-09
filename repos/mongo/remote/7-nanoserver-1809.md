## `mongo:7-nanoserver-1809`

```console
$ docker pull mongo@sha256:4388e6cb6a997acafe43897190c491d60a0e5a5a22fa1c5c81b3bef4579d7340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `mongo:7-nanoserver-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull mongo@sha256:6abbba7c3487dd6fd77e1054e09442ffe288c16dcfc799b0cdbf0a7dda6bdf5a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.6 MB (716589613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1a73b9cd99eb3a087aba103b3edefd641a96e01d21166ea086917d72e6a797`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 04 Dec 2023 10:54:04 GMT
RUN Apply image 10.0.17763.5206
# Tue, 09 Jan 2024 02:48:48 GMT
SHELL [cmd /S /C]
# Tue, 09 Jan 2024 02:48:50 GMT
USER ContainerAdministrator
# Tue, 09 Jan 2024 02:49:05 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 09 Jan 2024 02:49:05 GMT
USER ContainerUser
# Tue, 09 Jan 2024 02:49:06 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Tue, 09 Jan 2024 02:49:07 GMT
ENV MONGO_VERSION=7.0.5
# Tue, 09 Jan 2024 02:49:50 GMT
COPY dir:e35779bad98800653cfb4a4e0e8010143d34591b7f537faf64c0de91cf35eb83 in C:\mongodb 
# Tue, 09 Jan 2024 02:49:59 GMT
RUN mongod --version
# Tue, 09 Jan 2024 02:50:00 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 09 Jan 2024 02:50:01 GMT
EXPOSE 27017
# Tue, 09 Jan 2024 02:50:02 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:424f13a93a185a5defe848e7d270655e05233555f51328c0af24b9e70677d037`  
		Last Modified: Tue, 12 Dec 2023 20:02:40 GMT  
		Size: 104.5 MB (104510104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8e59e507e878d5b775488c813ee8ce41707cd7a813a1885bd902a22a4fc426`  
		Last Modified: Tue, 09 Jan 2024 02:50:11 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee3653e028ef704a558eb5a291363d342949d1277d94fe9a3fb42eaff9edef1`  
		Last Modified: Tue, 09 Jan 2024 02:50:11 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf748df14a4adf9288e6a69d6e27eca9b5f02c7f6b4027bac6c5e9b77ed537c`  
		Last Modified: Tue, 09 Jan 2024 02:50:10 GMT  
		Size: 66.3 KB (66261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78ea4aa4148ad53c7e51aaf16f04cd81cd369c36534c28467f2d75e9526d5c6`  
		Last Modified: Tue, 09 Jan 2024 02:50:09 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5112cc0e092e7a50e63c6ee926376a5cc433c48e8ffc3cede2c395a944ecaae7`  
		Last Modified: Tue, 09 Jan 2024 02:50:09 GMT  
		Size: 267.1 KB (267077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85da0edd7f900355d1a7ca90c74ab10edca384a18c3c45f715c7be6a5830730`  
		Last Modified: Tue, 09 Jan 2024 02:50:08 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24367a0e9e2e36d47f3f2ea30ad9e922e52c77bcd1f3a9b390145616be9ab44e`  
		Last Modified: Tue, 09 Jan 2024 02:50:56 GMT  
		Size: 611.7 MB (611671784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9372b60179f31b3718d239edd4217769e4161ef4e68fa550637ee1f2c810cd`  
		Last Modified: Tue, 09 Jan 2024 02:50:06 GMT  
		Size: 67.0 KB (67003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c806f319675aeb50315e265e148b67bc3886816b7e0443e5720ecffa3921e2`  
		Last Modified: Tue, 09 Jan 2024 02:50:06 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c32b93972673c2a603cde615656d55f4ab9626c9dee98edf40bf7efaf2291f8`  
		Last Modified: Tue, 09 Jan 2024 02:50:06 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18c2b79c7b6782c3410cc407e19d2e88317f657e5c73cdadc901a562c79982f`  
		Last Modified: Tue, 09 Jan 2024 02:50:06 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
