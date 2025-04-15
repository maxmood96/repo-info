## `mongo:6-nanoserver-1809`

```console
$ docker pull mongo@sha256:1bde6d76d4959c1924d5d6d29fdc6ccc1b42720472561680a7e2a559f46ee2c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `mongo:6-nanoserver-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull mongo@sha256:2f7f724beccb63de2dea082c3bfdf3494c142eaf492cc45daf42d726af2e4968
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.2 MB (633218681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3a23fade8e6c4391f0039c7831a058624b1362ed75e77a539f531d5b7f14f8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Tue, 15 Apr 2025 00:08:56 GMT
SHELL [cmd /S /C]
# Tue, 15 Apr 2025 00:08:56 GMT
USER ContainerAdministrator
# Tue, 15 Apr 2025 00:08:58 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 15 Apr 2025 00:08:58 GMT
USER ContainerUser
# Tue, 15 Apr 2025 00:08:59 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Tue, 15 Apr 2025 00:09:00 GMT
ENV MONGO_VERSION=6.0.22
# Tue, 15 Apr 2025 00:09:29 GMT
COPY dir:4b15d5e4d896c710da0908054bfc1acda67a6afe024035e1b165242aea0e7d87 in C:\mongodb 
# Tue, 15 Apr 2025 00:09:35 GMT
RUN mongod --version
# Tue, 15 Apr 2025 00:09:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 15 Apr 2025 00:09:37 GMT
EXPOSE 27017
# Tue, 15 Apr 2025 00:09:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1561a9c99e18b5dd79e79fade726a060feb273a6538a92762d3f0600fbb709c7`  
		Last Modified: Tue, 15 Apr 2025 00:09:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038b6c690215678ddcd5f0bb4c8ae4446d6a8c9b14a144686a89cc3339c388d5`  
		Last Modified: Tue, 15 Apr 2025 00:09:45 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbb34d71948650ef0f34dfced223c95e2e1b2a22764bce42d45c396310fbd4f`  
		Last Modified: Tue, 15 Apr 2025 00:09:44 GMT  
		Size: 69.6 KB (69636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a0e8c18dd4087f5ac3602f475052ded641228ae7624276a342bc5e17d99a5f`  
		Last Modified: Tue, 15 Apr 2025 00:09:44 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9917967a3ead65bbc2dd0df824414479ce06fd245c9029e0043fd307c3bdbbec`  
		Last Modified: Tue, 15 Apr 2025 00:09:44 GMT  
		Size: 275.1 KB (275146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5b0c3a097b4e39283fd69ed8f6e3f1a1c666a0c34c99d279903b57eec0afd9`  
		Last Modified: Tue, 15 Apr 2025 00:09:44 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85100003d6a643f697e73cb5a3a9aca492246130a2a2f24e5ad282f4c08e29a1`  
		Last Modified: Tue, 15 Apr 2025 00:10:24 GMT  
		Size: 525.9 MB (525872340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46329e4cd15c5de2ff61566d0fb8c5b76f41d81149a83e047de37ee16fd095e1`  
		Last Modified: Tue, 15 Apr 2025 00:09:42 GMT  
		Size: 71.8 KB (71827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5731cb0bfad9755167750f0aaf820bb29f2b8a27439f5f991483b15c3531b73e`  
		Last Modified: Tue, 15 Apr 2025 00:09:42 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42cf3b1c126b6b8e23251d8b94eb00d7ea9e7439920da8e7fd51eb42ae28aa0f`  
		Last Modified: Tue, 15 Apr 2025 00:09:42 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a23433e8e226829b3dadea66c25b0b94d9e8f43de16b1d3c829e4bbadf1a00`  
		Last Modified: Tue, 15 Apr 2025 00:09:42 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
