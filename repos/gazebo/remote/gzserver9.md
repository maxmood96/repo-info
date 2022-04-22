## `gazebo:gzserver9`

```console
$ docker pull gazebo@sha256:46279070bd28131a3567826cec1363d89e6a54be8253faec0595baf3ac3de73f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:gzserver9` - linux; amd64

```console
$ docker pull gazebo@sha256:9fed833b5a3294c3710c115ef9adf606f80e1008330d246d882805a9baab5562
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.4 MB (268425544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac14fd34ad53cc83c4aa775c8dc2f94afe64bb9e1697c438dd2bf19af17f698`
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
