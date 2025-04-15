## `mongo:6-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:193498f903b10ab1f6f032f047805187f97ded968252e0436aadfd0a05b756f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `mongo:6-nanoserver-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull mongo@sha256:c1d3624a5e9dc4a95fe80baa411c2ba500050c1d704858d927c083255f8a8a09
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.1 MB (647061044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad1ae50985626528ddca05cdc8f8ec2de67533c0258b7497cd32e2e668aae6f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Tue, 15 Apr 2025 00:09:56 GMT
SHELL [cmd /S /C]
# Tue, 15 Apr 2025 00:09:56 GMT
USER ContainerAdministrator
# Tue, 15 Apr 2025 00:09:58 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 15 Apr 2025 00:09:59 GMT
USER ContainerUser
# Tue, 15 Apr 2025 00:10:00 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Tue, 15 Apr 2025 00:10:01 GMT
ENV MONGO_VERSION=6.0.22
# Tue, 15 Apr 2025 00:10:18 GMT
COPY dir:4b15d5e4d896c710da0908054bfc1acda67a6afe024035e1b165242aea0e7d87 in C:\mongodb 
# Tue, 15 Apr 2025 00:10:30 GMT
RUN mongod --version
# Tue, 15 Apr 2025 00:10:31 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 15 Apr 2025 00:10:32 GMT
EXPOSE 27017
# Tue, 15 Apr 2025 00:10:32 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51818da93c1bddcca3dd0371c09b7fa4d775be1dc0a9cf6fe45209c1f3f4c0a5`  
		Last Modified: Tue, 15 Apr 2025 00:10:41 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0023ddf2ee1d71061857e9c91ae55a9e6c8742ef7ba127269ba1e84e3d0f6e92`  
		Last Modified: Tue, 15 Apr 2025 00:10:41 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f95a292b35b091d467b1174f7dd1c3f989722bcf5e5b0b0fef690fd1137b39d`  
		Last Modified: Tue, 15 Apr 2025 00:10:39 GMT  
		Size: 76.1 KB (76106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95f9cfc06fc3f37b3ee0b5882be6c221f5afdf887a7c63f9549df29df1f6e0f`  
		Last Modified: Tue, 15 Apr 2025 00:10:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0300e488245a66f95d83c710de30f8eb548ae2d9601780e3cbed5fa001df2516`  
		Last Modified: Tue, 15 Apr 2025 00:10:39 GMT  
		Size: 275.2 KB (275153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8de904d7c8a8bd2c2ad055dbedfcbc4aafe738c5cf83f6c441feb0596ee6866`  
		Last Modified: Tue, 15 Apr 2025 00:10:39 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b73f757f7d8b944d739e361892ae63872bb7d75592bfbd0f2521b31df31425`  
		Last Modified: Tue, 15 Apr 2025 00:11:21 GMT  
		Size: 525.9 MB (525872504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a57a485f7cceafc11f3d81ba5753f9388f245483281da68f833f177d0f1624`  
		Last Modified: Tue, 15 Apr 2025 00:10:37 GMT  
		Size: 93.8 KB (93773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289509437bb7b754bf5399d135b2a8698f3113302f91ed240062cc277ec9e65f`  
		Last Modified: Tue, 15 Apr 2025 00:10:37 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf775d6e2e1af60678ff29e1f1439c96c46b83d501f884bdb409c45aa6aecde4`  
		Last Modified: Tue, 15 Apr 2025 00:10:37 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9284446b29f42de9603e9ae7519111f3a9c101d2a286dcf2f62af1f51031cf95`  
		Last Modified: Tue, 15 Apr 2025 00:10:37 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
