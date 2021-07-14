## `gazebo:libgazebo9`

```console
$ docker pull gazebo@sha256:43e2c65cf567735f31957211ef21cdb64486232bbc850dfbcd12a27aee15a8b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9` - linux; amd64

```console
$ docker pull gazebo@sha256:fe1ed57bdb90f34782156906cb5bf2d314166d431a3c86d1ef934598490cfe0c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.7 MB (413691382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3763dc2766fab7306c782db2ac083c16dd81809b6c8c427c742d4e734912abe5`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 22:53:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 22:54:04 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 22:54:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Tue, 13 Jul 2021 22:54:07 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Tue, 13 Jul 2021 22:57:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.19.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 22:57:22 GMT
EXPOSE 11345
# Tue, 13 Jul 2021 22:57:22 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Tue, 13 Jul 2021 22:57:22 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 13 Jul 2021 22:57:22 GMT
CMD ["gzserver"]
# Tue, 13 Jul 2021 23:00:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo9-dev=9.19.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1107129de068a3615596b08dc61d39c6a7722d1f446096ae57c3f28769bfca39`  
		Last Modified: Tue, 13 Jul 2021 23:14:34 GMT  
		Size: 840.8 KB (840788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc35c0c59de4c823607e8f5602ad1738518fab84e3f56e0486061c35ee674ffb`  
		Last Modified: Tue, 13 Jul 2021 23:14:34 GMT  
		Size: 14.7 MB (14701992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63db980b8845e5d76f5727d0ab035a0e09bca0cee683161c27767ba4cb65b8d`  
		Last Modified: Tue, 13 Jul 2021 23:14:31 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcce1eb1ae7a73efed37001870f9d5dd2eb0260574dfd0c746201c7a9effd5f5`  
		Last Modified: Tue, 13 Jul 2021 23:14:31 GMT  
		Size: 5.5 KB (5462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e6d023eac1cae30a6d2617ac08a16cda3c22ca3970d9d0391fd7eb61d65994`  
		Last Modified: Tue, 13 Jul 2021 23:14:59 GMT  
		Size: 226.2 MB (226164582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f3305b87782cecf44caff7570493e7fa2fabf403c92dd348bc8b6651c07a2f`  
		Last Modified: Tue, 13 Jul 2021 23:14:31 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e960720ec3b398dc82b217283ab1402abe8a00d4751d35bc9b2e8a356bf5a1ec`  
		Last Modified: Tue, 13 Jul 2021 23:15:36 GMT  
		Size: 145.3 MB (145270787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
