## `gazebo:gzserver11-bionic`

```console
$ docker pull gazebo@sha256:9afa8eb1e0e30a22a1defee661d143c5a9403ffe6d8ac2fcce21be941e4055ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:gzserver11-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:e1b65b90e3f164846a2c90b1929fcefe39b2279699dc66d9eb674a8a7a4d9428
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277723728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f67eb409846a0fc7b74d6247c18ad21dda4709c3b08a597bd33e5d7b6fb42a7`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:12:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:12:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:12:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 22 Apr 2022 02:12:42 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Fri, 22 Apr 2022 02:19:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:19:32 GMT
EXPOSE 11345
# Fri, 22 Apr 2022 02:19:32 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Fri, 22 Apr 2022 02:19:32 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Fri, 22 Apr 2022 02:19:32 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d08ae4a50ec7a4071fcd259c6dc2b8f3219e66e5206c2f15ee781c4691a7699`  
		Last Modified: Fri, 22 Apr 2022 02:30:38 GMT  
		Size: 839.0 KB (838982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598c7766b18d877e1a59d1316798474fde98be625c8a0d61231ae22574ca4696`  
		Last Modified: Fri, 22 Apr 2022 02:30:38 GMT  
		Size: 14.7 MB (14706301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108a98dbb6e7c0b2478d6b00e6653f779c21a71914253e8f8c8b236ee33eac7`  
		Last Modified: Fri, 22 Apr 2022 02:30:35 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70fea14618112c5849f54d05aab7519af9061763e935e2d3b2028c1142da7b2e`  
		Last Modified: Fri, 22 Apr 2022 02:30:35 GMT  
		Size: 5.5 KB (5456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe6719d99e969837cd6c4c7fbddba9f7b2efa5d76c2d67a7f541237edb7ba86`  
		Last Modified: Fri, 22 Apr 2022 02:32:16 GMT  
		Size: 235.5 MB (235461482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f374eef7c8ee37ac82fd0e700f3eb8a53c4557feb5fd7f3fda3cfc4b96a8300`  
		Last Modified: Fri, 22 Apr 2022 02:31:47 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
