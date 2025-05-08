## `mongo:6-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:06511af614034483b0d326043c9133e2436a5da582faada1add60db36ea967b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `mongo:6-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull mongo@sha256:d5112b99f9deff2c27b7182fc11fb21a70c8bca61abe7dae38a5e175f887c7f2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.9 MB (648876398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09bf5c9e8d6ca0c062d745993113e5d7356eb672bedb553b1f93a1613eb24e33`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Wed, 30 Apr 2025 18:09:26 GMT
SHELL [cmd /S /C]
# Wed, 30 Apr 2025 18:09:27 GMT
USER ContainerAdministrator
# Wed, 30 Apr 2025 18:09:47 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 30 Apr 2025 18:09:48 GMT
USER ContainerUser
# Wed, 30 Apr 2025 18:09:52 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 30 Apr 2025 18:09:53 GMT
ENV MONGO_VERSION=6.0.23
# Wed, 30 Apr 2025 18:10:11 GMT
COPY dir:61cfe29ccc038afb3fae0bca0d9d2a1c9c8488076e3e2305b0edb2748a3a7149 in C:\mongodb 
# Wed, 30 Apr 2025 18:10:32 GMT
RUN mongod --version
# Wed, 30 Apr 2025 18:10:32 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 30 Apr 2025 18:10:33 GMT
EXPOSE 27017
# Wed, 30 Apr 2025 18:10:35 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c51a302f2ed2e7a6c661f7781bde6eaafe93fe331d8d70a189a5e51a781b0a4`  
		Last Modified: Wed, 30 Apr 2025 18:10:39 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da375416f559681944c1f497ee45572b48c57fae4d476cb9dfb24c67fbedd363`  
		Last Modified: Wed, 30 Apr 2025 18:10:39 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf59fc0fd06e538a003f501c93248276d3115bdf9f431a936b6887446d307be`  
		Last Modified: Wed, 30 Apr 2025 18:10:39 GMT  
		Size: 72.0 KB (71988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1b541bbe129a1675de8a6fb3076dbe29f5f471f7e5c45283655971249d2073`  
		Last Modified: Wed, 30 Apr 2025 18:10:38 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cab06e8247554d27e7ddabcf74782e53cb184cf4ff1b39c73de374ce0b0acae`  
		Last Modified: Wed, 30 Apr 2025 18:10:38 GMT  
		Size: 275.2 KB (275160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030fc6ef70a14498a1eaff231a877a22fd31053de37473deb136c1fc47526435`  
		Last Modified: Wed, 30 Apr 2025 18:10:38 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74644f8f05ed9c3d4d8bb700f91476b80482baa56495668ac9109bc87fbc9bdb`  
		Last Modified: Wed, 30 Apr 2025 18:11:21 GMT  
		Size: 525.9 MB (525897257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41d25e6cd95825721441bc06bf4cfeea42cc6874f813d4c794d9ddcef23653a`  
		Last Modified: Wed, 30 Apr 2025 18:10:37 GMT  
		Size: 85.7 KB (85690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cfbeb7e66fa9f3a90a29dc730d9b071bdfd552b0e258eac82ae9968ac753f8`  
		Last Modified: Wed, 30 Apr 2025 18:10:37 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d30bcaf398e4e3235ada55d0d700156d11508c9b3d9b177efe35b3664bc4689`  
		Last Modified: Wed, 30 Apr 2025 18:10:37 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6471f56b17ae3d0822b30cec56345325f11fe6b6c5cef470e4c996a16ed2fe3`  
		Last Modified: Wed, 30 Apr 2025 18:10:37 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
