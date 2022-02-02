## `gazebo:libgazebo9-bionic`

```console
$ docker pull gazebo@sha256:71a5aa8df9e96cced511f11f65f660a11c51c1ae8ad42ddbfcaaa4863e781fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo9-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:668c31564a3b2aef92b1d081a8ae821f9f05353fa94d521fa47dbfe7cb240a49
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.7 MB (413693053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bececb31cd0e3f04d67a18df248f3cb7d08c5e227764dc6392ef06148e0b627`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:05:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:05:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:06:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Wed, 02 Feb 2022 03:06:22 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Wed, 02 Feb 2022 03:10:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.19.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:10:28 GMT
EXPOSE 11345
# Wed, 02 Feb 2022 03:10:28 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Wed, 02 Feb 2022 03:10:28 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Wed, 02 Feb 2022 03:10:28 GMT
CMD ["gzserver"]
# Wed, 02 Feb 2022 03:14:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo9-dev=9.19.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a04d20dede38fb80c5555e5e471ed360ab6d41bc011f0af2d6ec62357562b8d`  
		Last Modified: Wed, 02 Feb 2022 03:36:03 GMT  
		Size: 838.9 KB (838901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99e58c80c83c12a27618ac972e278f1bdb1328623ce6554f47e3ca77fd17d33`  
		Last Modified: Wed, 02 Feb 2022 03:36:03 GMT  
		Size: 14.7 MB (14702920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36462e0cb726a06c051fa59a60f42c1c4aa926cbe67069365171e9c4ddcee414`  
		Last Modified: Wed, 02 Feb 2022 03:36:00 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68c1d049fc00e752039f75c595d0570cbc72a697b768913e3717ba982565e23`  
		Last Modified: Wed, 02 Feb 2022 03:36:00 GMT  
		Size: 5.5 KB (5457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6632643a63b165081ecbe39f1cc8699162b6b0863823b5bb6a16912a805e3e`  
		Last Modified: Wed, 02 Feb 2022 03:36:27 GMT  
		Size: 226.2 MB (226163320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c6bc3cdbbebf818142bb8d8f0cd1a7290a3a05bb70f78946f4284e538a87c7`  
		Last Modified: Wed, 02 Feb 2022 03:36:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9761aa33f692764a8db67c019dfefa0031a84d848f4488e9d906a4318699d12`  
		Last Modified: Wed, 02 Feb 2022 03:37:02 GMT  
		Size: 145.3 MB (145272760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
