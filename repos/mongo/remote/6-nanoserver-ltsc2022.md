## `mongo:6-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:2405e9d69d8636544f7138502a7ff74909c257d7f0e0efd87b4a8e87cda4b7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `mongo:6-nanoserver-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull mongo@sha256:ca84b6fc3ddaf526a7a70c15bbeea5bd9a23cd699c189b511dc0157f504a1955
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.3 MB (647302157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb77f47f0f93e0fcec4679633c6a11add452871d00c317afe4ce55ed3e9bc72c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 02:18:54 GMT
SHELL [cmd /S /C]
# Wed, 09 Apr 2025 02:18:55 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 02:18:57 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 09 Apr 2025 02:18:58 GMT
USER ContainerUser
# Wed, 09 Apr 2025 02:19:01 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 09 Apr 2025 02:19:01 GMT
ENV MONGO_VERSION=6.0.21
# Wed, 09 Apr 2025 02:19:19 GMT
COPY dir:3e58ecc6221c38d328e962765c65cbae4544929c28b4dc0b7bf576cc4212e36c in C:\mongodb 
# Wed, 09 Apr 2025 02:19:30 GMT
RUN mongod --version
# Wed, 09 Apr 2025 02:19:31 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Apr 2025 02:19:32 GMT
EXPOSE 27017
# Wed, 09 Apr 2025 02:19:33 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d378ee82b0a562dd5612f8faa15c9b95ee6f6870d0ad618fa9088f188c5f263`  
		Last Modified: Wed, 09 Apr 2025 02:19:41 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e112805d3f38b7f8383b65bcbbbb6c94d00a32c5f2457a8bf6cb5a7b14f092d`  
		Last Modified: Wed, 09 Apr 2025 02:19:41 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9193f57c17847cd59f7a44f9d0c0834bdd07f47143422caab7694a349b814ed6`  
		Last Modified: Wed, 09 Apr 2025 02:19:39 GMT  
		Size: 76.6 KB (76599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4228a28e425773f15e8b90d1a1e0c2569286c205afc1a281ee5b24ed276da17a`  
		Last Modified: Wed, 09 Apr 2025 02:19:39 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eacc4fbfa2344836b26db55d5985145064559be7fc35d5af4ee111d05d5ea26`  
		Last Modified: Wed, 09 Apr 2025 02:19:40 GMT  
		Size: 275.1 KB (275146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9432591e6a8ac69bfb1db30731066b4124be7bcd7997f1f0203a6a1a5fdc6e`  
		Last Modified: Wed, 09 Apr 2025 02:19:39 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ff768ac1b7758cd3dff62b932fbf3c86256f0ddd64fd28f9fb498d1d2358e7`  
		Last Modified: Wed, 09 Apr 2025 02:20:19 GMT  
		Size: 526.1 MB (526116354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aaaf33191986a251f04436f02df2455f8cfbe1c7a306021cecc7be51bb2a9b`  
		Last Modified: Wed, 09 Apr 2025 02:19:37 GMT  
		Size: 90.5 KB (90547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef44955036a56d00e9a37cbf9e026a750285f9a5f3d12bbce16961e0f670ba8`  
		Last Modified: Wed, 09 Apr 2025 02:19:37 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efeb4eeb061be13ccde15a02b85e75e143ecff6d76b6e1a42b0d57999ef44b52`  
		Last Modified: Wed, 09 Apr 2025 02:19:37 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5bfaa40a3fbb13cda5ee83830200ce8bff4e2d2ec1d9471f12c39ca9af197a`  
		Last Modified: Wed, 09 Apr 2025 02:19:37 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
