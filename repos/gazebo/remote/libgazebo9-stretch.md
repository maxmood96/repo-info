## `gazebo:libgazebo9-stretch`

```console
$ docker pull gazebo@sha256:20a2cfd8188bdd63f924fe38d5980b201605fdf9ef3af54582e74cdc0dafdbf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9-stretch` - linux; amd64

```console
$ docker pull gazebo@sha256:df3d52b9d2979760c41e9dad31bbdab765c319c2500aedae1cd6a2568b8ec72b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.2 MB (570181339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74df9839b29da66d1b1c27692e4bce45219dc62456fa368d049f2dd8e56cd147`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:50:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 05:51:02 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Tue, 09 Feb 2021 05:51:04 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Tue, 09 Feb 2021 05:51:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.16.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 05:51:56 GMT
EXPOSE 11345
# Tue, 09 Feb 2021 05:51:56 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Tue, 09 Feb 2021 05:51:57 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 09 Feb 2021 05:51:57 GMT
CMD ["gzserver"]
# Tue, 09 Feb 2021 05:53:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo9-dev=9.16.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d04da106e9d8decd06fcae16919ea213b53cb7d5cb11b8ae89ba23f8de520f`  
		Last Modified: Tue, 09 Feb 2021 05:55:01 GMT  
		Size: 18.5 MB (18510153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb27a07071cedc4afa32c43e5d8b2f88c01823bbaac433a582c14f7653d07070`  
		Last Modified: Tue, 09 Feb 2021 05:54:54 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a63a19aca85323515410a8b69b99d8755c6fcf2ab40928b157064bbed8b6df1`  
		Last Modified: Tue, 09 Feb 2021 05:54:54 GMT  
		Size: 5.0 KB (4983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340534c7d3270cf1864dbe33bd8d3c5366247424abf6fd9a18ecf86f067708c9`  
		Last Modified: Tue, 09 Feb 2021 05:55:35 GMT  
		Size: 202.3 MB (202278200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5d1a164683b13cace62a43ac21634c54ed3b6dd3b8b63a22afa21bfb2bc318`  
		Last Modified: Tue, 09 Feb 2021 05:54:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3affd38e09b9da42cc8adc6cca2f1fcd2a475e97bb864f7edaf707bdb78df95b`  
		Last Modified: Tue, 09 Feb 2021 05:56:55 GMT  
		Size: 304.0 MB (304006510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
