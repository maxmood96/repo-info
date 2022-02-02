## `gazebo:gzserver11-focal`

```console
$ docker pull gazebo@sha256:a66e0b89266b7b4cfbdcb11495d319e188c4d28d94966632147ce39fdfc0b634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:gzserver11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:2787dcee50b744914a866a5dde15edf4174a2ab329d5143969ad590d8cb85a76
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320941270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87baf064e031d9efbc2d50e06558842a6fbe30082d964e583ce9df71baefeffc`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:18:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:18:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:19:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Wed, 02 Feb 2022 03:19:28 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Wed, 02 Feb 2022 03:25:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.10.1-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:26:00 GMT
EXPOSE 11345
# Wed, 02 Feb 2022 03:26:01 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Wed, 02 Feb 2022 03:26:01 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Wed, 02 Feb 2022 03:26:01 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762bb72141f73c9f8d23d9bc2396670126e4d86b9784e31484c651effc425f91`  
		Last Modified: Wed, 02 Feb 2022 03:38:42 GMT  
		Size: 1.2 MB (1182237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3bf51d880257d1e11e84e7c58392ded9c12fd127035b14f24cd218dced9d1c`  
		Last Modified: Wed, 02 Feb 2022 03:38:41 GMT  
		Size: 16.2 MB (16169904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5846641b386e17d8cb333e1128a068702afb1934299917c42549885410b446`  
		Last Modified: Wed, 02 Feb 2022 03:38:39 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fee29037ff6852a7b77dc70e48f4f2b1b36937e0afb33e5a98745e2f85957e`  
		Last Modified: Wed, 02 Feb 2022 03:38:39 GMT  
		Size: 5.5 KB (5502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efc09bc10499c0b0dda442ace467602452bbf540bd976e979909d165c0c8e1c`  
		Last Modified: Wed, 02 Feb 2022 03:39:11 GMT  
		Size: 275.0 MB (275017900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6bce17d9e4eea3c6505df81cba0093ecadcc98fe1a2ca760b9e9b934e93bfc`  
		Last Modified: Wed, 02 Feb 2022 03:38:39 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
