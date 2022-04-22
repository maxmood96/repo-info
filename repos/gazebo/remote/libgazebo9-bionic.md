## `gazebo:libgazebo9-bionic`

```console
$ docker pull gazebo@sha256:904dad15c45fe12feda64c1aec1719757d64d7bab70fb43818eefa476351a7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo9-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:aac4b8808b3a347f455159418613f1100b23cda444a4a183198a6d8630979450
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.7 MB (413696360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8212c0ba0e76091bb5a93b6ac4720a5478a0647951d9fc534c430d13f5abb98d`
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
# Fri, 22 Apr 2022 02:15:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.19.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:15:34 GMT
EXPOSE 11345
# Fri, 22 Apr 2022 02:15:34 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Fri, 22 Apr 2022 02:15:34 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Fri, 22 Apr 2022 02:15:34 GMT
CMD ["gzserver"]
# Fri, 22 Apr 2022 02:18:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo9-dev=9.19.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:451045a2f640235505958342c7548c22de23eb3deb95d93d8f27d165afcafabf`  
		Last Modified: Fri, 22 Apr 2022 02:31:02 GMT  
		Size: 226.2 MB (226163297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4225ad22bcfd061c8c1a1b4ca211190e271917d857fc330329514eee153c52c2`  
		Last Modified: Fri, 22 Apr 2022 02:30:35 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4654be747af344cb226632d70db99f26b6b943bb41aa11e124a11f3bc31abd`  
		Last Modified: Fri, 22 Apr 2022 02:31:37 GMT  
		Size: 145.3 MB (145270816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
