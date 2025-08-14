## `mongo:6-nanoserver`

```console
$ docker pull mongo@sha256:2a3aae052dfc95279d742ccab55577905e030cf9aae06b0e27efd3859fb8416e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `mongo:6-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull mongo@sha256:3c7306ac7bbf9e848714f735c6c5a4b6023f5760457dc10ca71c6a75a1f5724d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.4 MB (649436467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468486a9adea0fb95482d8a922dff83c0074f286b00d16c82a6ae3d3a0cdd662`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:50:12 GMT
SHELL [cmd /S /C]
# Tue, 12 Aug 2025 20:50:13 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:50:18 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 12 Aug 2025 20:50:19 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:50:21 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Tue, 12 Aug 2025 20:50:22 GMT
ENV MONGO_VERSION=6.0.25
# Tue, 12 Aug 2025 20:50:40 GMT
COPY dir:eb82384afd608dadf39505c4064899b94d4e427c69fe141a2bddd227b5df956b in C:\mongodb 
# Tue, 12 Aug 2025 20:50:51 GMT
RUN mongod --version
# Tue, 12 Aug 2025 20:50:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 12 Aug 2025 20:50:53 GMT
EXPOSE 27017
# Tue, 12 Aug 2025 20:50:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440640ce7fab101865896ebdc7fca7f1ea7fb4f42d346a4931a4e738bd81e6ea`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f634d46c990c8e705082252119a1c02dc0f5b51fd7597a6a08dce46cc6f37260`  
		Last Modified: Tue, 12 Aug 2025 20:52:09 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffd10a044568de0cbb95e4fd18f876932851663c2e90a76d223f01cf9650802`  
		Last Modified: Tue, 12 Aug 2025 20:52:09 GMT  
		Size: 78.6 KB (78642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb40b6f99656d912caa6f659d43fe69ad18cd6de2049e7ac4eb06f9188fde210`  
		Last Modified: Tue, 12 Aug 2025 20:52:09 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8dacb5de687eb1b335796b431240c6b225b2937a9cc89ed2c440364e5a4aa8`  
		Last Modified: Tue, 12 Aug 2025 20:52:09 GMT  
		Size: 275.2 KB (275161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03b31cab7fe5c30ebbb77111b962407253d71c669c98bd96f834a90d36c0e73`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce33c373ff4ec9eb2d23a933dcc707933d4caa9af37c4a0c4d9986ea93cb8327`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 526.3 MB (526333023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9ca3d6e971ac381e67c57fa01b48112952b7a283bd057a4c84a663da84fe68`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 82.1 KB (82090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d994b003de2822d1bb481d2b28169a83bfa2fe49b9940ab69b252d76c38e23`  
		Last Modified: Tue, 12 Aug 2025 20:52:11 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fd5464dd112cb8eac9ccfcc5e3ecc8212b8067197ab86190500fe593323cdb`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9132380dead785f88648b0624df8e4a2222e0404ccbfdaee75f2f6ba9d8170`  
		Last Modified: Tue, 12 Aug 2025 20:52:11 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
