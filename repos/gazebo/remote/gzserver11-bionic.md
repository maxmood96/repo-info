## `gazebo:gzserver11-bionic`

```console
$ docker pull gazebo@sha256:b55b7ce43dfdfceeec8ec5805b5477939a3dd89f3c7a9654c1fc28b6ec9f1488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:gzserver11-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:2c378fe3f90337063dca8366391c93c9a0763502839c9347083c82b56f7eb6f4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277456903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a06712245da1aece14598d8646a1936ae48252a9b81fee55aabeca26708e9d0`
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
# Tue, 13 Jul 2021 23:01:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.7.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:01:34 GMT
EXPOSE 11345
# Tue, 13 Jul 2021 23:01:34 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Tue, 13 Jul 2021 23:01:34 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 13 Jul 2021 23:01:35 GMT
CMD ["gzserver"]
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
	-	`sha256:f7e8543e7bede531b5873ffb1fbaa3260ab851649c2c9dfd7df1a3a28f35377f`  
		Last Modified: Tue, 13 Jul 2021 23:16:15 GMT  
		Size: 235.2 MB (235200890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74fa6bf8986a6b5543f2ff6b1e2d3a4d04a76a2bbe0cb9ac1a67aa1596ff06fd`  
		Last Modified: Tue, 13 Jul 2021 23:15:46 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
