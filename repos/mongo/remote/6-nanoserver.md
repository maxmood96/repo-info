## `mongo:6-nanoserver`

```console
$ docker pull mongo@sha256:0e67ee7005e59d30f1d6e4e061cda942d4de854b6e764c4ddbbac63596c7ae4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `mongo:6-nanoserver` - windows version 10.0.20348.4294; amd64

```console
$ docker pull mongo@sha256:b107f7f1aa6259ecf4b736ae624fc748c4c1c771a7c26c0440906db62c837ff4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.1 MB (649104708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb70d2c11a8bdd7e6caab9f53156e5861627993ae7d19c6d6eb430f7f50628e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Oct 2025 07:34:08 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 21:14:05 GMT
SHELL [cmd /S /C]
# Tue, 14 Oct 2025 21:14:06 GMT
USER ContainerAdministrator
# Tue, 14 Oct 2025 21:14:07 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 14 Oct 2025 21:14:08 GMT
USER ContainerUser
# Tue, 14 Oct 2025 21:14:09 GMT
COPY multi:540d6dd70b1e7484f1958dc08b337aeb56cf8a92fe38be4c279dd406990d6935 in C:\Windows\System32\ 
# Tue, 14 Oct 2025 21:14:09 GMT
ENV MONGO_VERSION=6.0.26
# Tue, 14 Oct 2025 21:14:34 GMT
COPY dir:0d00bc0d9c7727315b49b912b1a7cc29c8b089ecda32a37a554368213859ca20 in C:\mongodb 
# Tue, 14 Oct 2025 21:14:45 GMT
RUN mongod --version
# Tue, 14 Oct 2025 21:14:46 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 14 Oct 2025 21:14:46 GMT
EXPOSE 27017
# Tue, 14 Oct 2025 21:14:46 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:f68a3bbf3ee20b515c5b8b801e5627a9dac3782ef264e37060c34ed80e5d8874`  
		Last Modified: Tue, 14 Oct 2025 20:41:53 GMT  
		Size: 122.7 MB (122688886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34fff1adbceb320f029357ac6bc28d023f4b03a25c5b13b0e3b06a64e8e8d28`  
		Last Modified: Tue, 14 Oct 2025 21:56:53 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bca758b3461e3a7e976351066d290a094902f2fc2ef11eef7e561b2ccf4997`  
		Last Modified: Tue, 14 Oct 2025 21:56:53 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cbaea860541b1cb34d19d7bd0ae1cbf49b36ae236d5bdcfa1f24dd8e290869`  
		Last Modified: Tue, 14 Oct 2025 21:56:53 GMT  
		Size: 77.2 KB (77191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60638d2590f05fa8671bb3a4ebb55e3fc47efa4d975e8062a2a59cdee08db67f`  
		Last Modified: Tue, 14 Oct 2025 21:56:54 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b5a70b4ef75d629daa1ae1e4e3c2b93d825e9a221c3d8e73abdf3347c4c17d`  
		Last Modified: Tue, 14 Oct 2025 21:56:53 GMT  
		Size: 275.2 KB (275216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d91fe4287ed1f23e23992099bf8b1bdbaffe1dc948643709153dc7e63b8b8be`  
		Last Modified: Tue, 14 Oct 2025 21:56:53 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2a1d3f47cc922321ca76b877570af4e5d6dbf472d37d092144560bc303cdd3`  
		Last Modified: Wed, 15 Oct 2025 01:07:42 GMT  
		Size: 526.0 MB (525972070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4d7959183076ad12644ff0b0555df1581e27f0cf77bf6dd1f3c30c0ba1ad6c`  
		Last Modified: Tue, 14 Oct 2025 21:56:53 GMT  
		Size: 83.9 KB (83928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f615e65c650164bab58e67234882e0127600d17161631921ed0e141e89d4973`  
		Last Modified: Tue, 14 Oct 2025 21:56:53 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6d97a4e1fd1f94e79d1a919cb6c110072242ceb72ccd3ba832b755499ac9a9`  
		Last Modified: Tue, 14 Oct 2025 21:56:54 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7cad44052ce353cbfc325fe5c75cc4afa70941b6348d7111f082e2a6d2ee3d`  
		Last Modified: Tue, 14 Oct 2025 21:56:54 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
