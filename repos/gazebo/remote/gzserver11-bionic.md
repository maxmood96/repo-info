## `gazebo:gzserver11-bionic`

```console
$ docker pull gazebo@sha256:42b6a8d23e8d6fa19f82db0d3158f874bd7dc06b990f540370d5d323a44e9b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:gzserver11-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:fdeeba446f063bb35466b3045708f1dcbb43d2abbacbf044834fb6c1015569a9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277499389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cda3a63dc41c4110783afc21122b5db61e7021cfd4d523afb17816c69524782`
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
# Wed, 02 Feb 2022 03:15:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.10.1-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:15:28 GMT
EXPOSE 11345
# Wed, 02 Feb 2022 03:15:28 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Wed, 02 Feb 2022 03:15:29 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Wed, 02 Feb 2022 03:15:29 GMT
CMD ["gzserver"]
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
	-	`sha256:08a76d7536917d0c26a88b3dc9284b7441ff5a5b2d113fd88aae09515a119789`  
		Last Modified: Wed, 02 Feb 2022 03:37:40 GMT  
		Size: 235.2 MB (235242417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585c20aaa4197800150be742898e87c77991656034c541e01de78c2f6f7ffbf9`  
		Last Modified: Wed, 02 Feb 2022 03:37:12 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
