## `gazebo:gzserver11-focal`

```console
$ docker pull gazebo@sha256:f0dfb1e44cf15599946b9ca5e1c2b0a4565aa21e6dd3f72f1a6c0dc4db3db480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:gzserver11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:717c5341160e5d91a8b7d1703367ec369d8886c6309c344127b55269ba4f1990
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.8 MB (320836076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c79390e7ee14c6fe9a89fdf13c2d4399625d06495fb2f09aaccbd044f7f6f3`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:55 GMT
ADD file:d2abf27fe2e8b0b5f4da68c018560c73e11c53098329246e3e6fe176698ef941 in / 
# Tue, 31 Aug 2021 01:20:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 04:36:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 06:50:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 06:50:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Tue, 31 Aug 2021 06:50:24 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Tue, 31 Aug 2021 06:54:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.8.1-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 06:54:18 GMT
EXPOSE 11345
# Tue, 31 Aug 2021 06:54:18 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Tue, 31 Aug 2021 06:54:18 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 31 Aug 2021 06:54:18 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:35807b77a593c1147d13dc926a91dcc3015616ff7307cc30442c5a8e07546283`  
		Last Modified: Sat, 28 Aug 2021 03:03:19 GMT  
		Size: 28.6 MB (28570074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a41ae3b013398d2c13b5bceb3338e9582560c6d0ffd908463d766628be0a9c`  
		Last Modified: Tue, 31 Aug 2021 05:02:39 GMT  
		Size: 1.2 MB (1182916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fb6198ceddff79ea060a3dcbf867b150789ab77f10bedecccb06928c02981c`  
		Last Modified: Tue, 31 Aug 2021 07:04:14 GMT  
		Size: 16.2 MB (16167873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06707dd13f9686d51caea69aa6b9aa42e025ced980d098f96ff8a644a33e8676`  
		Last Modified: Tue, 31 Aug 2021 07:04:11 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba95019c5f0b077d2e40c42932ce1f811f6fef077972cbe98b4ae0e3fa06279e`  
		Last Modified: Tue, 31 Aug 2021 07:04:11 GMT  
		Size: 5.5 KB (5501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d7ddcd1744b56e15c4ed6945bc7d361f40dff3e14eef620287c9fdfd911a59`  
		Last Modified: Tue, 31 Aug 2021 07:04:44 GMT  
		Size: 274.9 MB (274908085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a5d63aee8ad00a9d62ed9ac6cb2520c522c8b8e3499c80e41b97d47c91f62f`  
		Last Modified: Tue, 31 Aug 2021 07:04:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
