## `gazebo:gzserver11-bionic`

```console
$ docker pull gazebo@sha256:1c32cd7b19020fad0e76cbf13351a922cf5a824547c0ca12a84c65a975f756db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:gzserver11-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:2be7f544134f12c757b9ad4f73ffa0cbb5c4a4e89aaa7539841afb7c41ef8d1b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277461734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552e0b2bc3fc4a7d235c26314ee94882adec0c6209ce3c50508ddc5db839acee`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:38:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:38:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:38:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Mon, 26 Jul 2021 23:38:30 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Mon, 26 Jul 2021 23:45:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.7.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:46:00 GMT
EXPOSE 11345
# Mon, 26 Jul 2021 23:46:00 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Mon, 26 Jul 2021 23:46:00 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Mon, 26 Jul 2021 23:46:01 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1186553e47569a52e52d0ff6702d24c183760ccfa8f0865f5cd805b6a834f02a`  
		Last Modified: Tue, 27 Jul 2021 00:00:30 GMT  
		Size: 840.6 KB (840558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22f29e22c5b4a7dee45885c7fd1060bc20504f6892f2f6e8a690fdd85e38e84`  
		Last Modified: Tue, 27 Jul 2021 00:00:30 GMT  
		Size: 14.7 MB (14701891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04465fc9eba13e0a1075f49af13a2d31edd33cc93f6df820d7d2344820a54d8e`  
		Last Modified: Tue, 27 Jul 2021 00:00:27 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c79e23b14d43c0f1df7721489416a5aaf8909970db213f9bee4d925741fef7`  
		Last Modified: Tue, 27 Jul 2021 00:00:27 GMT  
		Size: 5.5 KB (5457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ccca16f7278d826135d05503fccbb867997aca010639d682ed04d94dfb23bf`  
		Last Modified: Tue, 27 Jul 2021 00:02:16 GMT  
		Size: 235.2 MB (235203162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fd253f2a427e01cb270b8874359cb07e9a7f69bd394341963bef8cf9eafd43`  
		Last Modified: Tue, 27 Jul 2021 00:01:45 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
