## `gazebo:gzserver11-focal`

```console
$ docker pull gazebo@sha256:1bb18e02b9dd0d9e9c77fb73fdfbc0b1e58795198615c4f49e3eac2f5ccd9a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:gzserver11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:9f6755b586c9c5edca169d734e5507f5b5c67218e79ecb27fc6350715c5d40d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.8 MB (321848877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dcb5504c25f090c962f0a7876c6cdcd8af38100a58610b8c36c815ef629ed1c`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:59 GMT
ADD file:7009ad0ee0bbe5ed7f381792e07347e260e6896aeee0d80597808065120fa96b in / 
# Fri, 29 Apr 2022 23:20:59 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:39:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Sat, 30 Apr 2022 00:39:28 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Sat, 30 Apr 2022 00:42:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:42:35 GMT
EXPOSE 11345
# Sat, 30 Apr 2022 00:42:35 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Sat, 30 Apr 2022 00:42:35 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Sat, 30 Apr 2022 00:42:36 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:d5fd17ec1767521cf97f61568096bfc9a7cd9c2d149576a7b43930c5a97062b0`  
		Last Modified: Thu, 28 Apr 2022 03:03:21 GMT  
		Size: 28.6 MB (28566230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca43c78a9071a3a99b9aa1fe030cf8ba61c96fbf0b12adc1a85163d395cc10a1`  
		Last Modified: Sat, 30 Apr 2022 00:50:22 GMT  
		Size: 1.2 MB (1180884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462149346c979b524cdc491e48ec6fd9603354ed6e3f3d3c1f718d7db350f043`  
		Last Modified: Sat, 30 Apr 2022 00:50:22 GMT  
		Size: 16.2 MB (16169955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9e2b8c8e7a35ccd27627a96b08bc1d4d52de5cd628966e1b4a08e608b791fa`  
		Last Modified: Sat, 30 Apr 2022 00:50:19 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bb6723ad2e367ee890e62f09a9abb2abb9e0fc24ff74052835b1a893726224`  
		Last Modified: Sat, 30 Apr 2022 00:50:20 GMT  
		Size: 5.5 KB (5494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591e2c9abb74cbee22b19cbd8d58a627ff4b76910590ea343df95ae43742eb2c`  
		Last Modified: Sat, 30 Apr 2022 00:50:52 GMT  
		Size: 275.9 MB (275924686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce1949a815fcc7e80999b254c38c44561907a3033904a5e34cb46c25f427dff`  
		Last Modified: Sat, 30 Apr 2022 00:50:19 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
