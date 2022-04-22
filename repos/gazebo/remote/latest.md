## `gazebo:latest`

```console
$ docker pull gazebo@sha256:57ad38e1cc10b3eb1210ff1bc676a580187b6734a19b31f8c220b93ffd0f7d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:latest` - linux; amd64

```console
$ docker pull gazebo@sha256:c27d1554c139e56480146e5c4350b5f17cbd81a714ea2debb0342778f4f9818a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.1 MB (610095817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e36ef7608b518bb4094b487c5ebbaf5c4536766c5cc668d2436766472994f5c`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:22:16 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:22:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 22 Apr 2022 02:22:18 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Fri, 22 Apr 2022 02:25:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:25:24 GMT
EXPOSE 11345
# Fri, 22 Apr 2022 02:25:24 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Fri, 22 Apr 2022 02:25:24 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Fri, 22 Apr 2022 02:25:24 GMT
CMD ["gzserver"]
# Fri, 22 Apr 2022 02:30:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.10.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816a30ae3dab6930b855b8226d592bc58db82e5fe54b82a4e9a1992614c4f19e`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 16.2 MB (16169945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc3b22a268ef6ab29c620a5723ed914908b1178e3410b66f75d0967b8621b86`  
		Last Modified: Fri, 22 Apr 2022 02:33:09 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3267b1c54fddf890e9cea0b942bc2ad96dde55909b35df058b9a495cef6b666f`  
		Last Modified: Fri, 22 Apr 2022 02:33:09 GMT  
		Size: 5.5 KB (5500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a062a96e8bb3c9bb7caf3207933294694ab959c1f04615d71db3f7e657cc4f4`  
		Last Modified: Fri, 22 Apr 2022 02:33:42 GMT  
		Size: 275.9 MB (275858850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705719e4c5c3a030d0a489e71b4c9b35b82127d73b3e0d4cd43b7268e9558fc2`  
		Last Modified: Fri, 22 Apr 2022 02:33:09 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfaa1fe384125851b945298291594b8926c0e06fa43867e43b889e171254addb`  
		Last Modified: Fri, 22 Apr 2022 02:34:39 GMT  
		Size: 288.3 MB (288313022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
