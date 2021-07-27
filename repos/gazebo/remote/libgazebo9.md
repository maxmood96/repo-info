## `gazebo:libgazebo9`

```console
$ docker pull gazebo@sha256:e93c433817fb65bc0377c8fc5e51abb8ff3532a071c94ef9a87ea1d6c435df28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo9` - linux; amd64

```console
$ docker pull gazebo@sha256:f13f9362dac4ceb082a5c4be440558d8bfe8d452fb51dedcd9e1cf6b535fc4c1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.7 MB (413698281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0415cf24b1edea2813bf86ddc422b92727d2b76a055a70f4031b8776e119b611`
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
# Mon, 26 Jul 2021 23:41:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.19.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:41:45 GMT
EXPOSE 11345
# Mon, 26 Jul 2021 23:41:46 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Mon, 26 Jul 2021 23:41:46 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Mon, 26 Jul 2021 23:41:46 GMT
CMD ["gzserver"]
# Mon, 26 Jul 2021 23:44:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo9-dev=9.19.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:3848ee88717220f4b5d63f1c0e65c6faf62965d57b4ac0790df14eb8d9b9d876`  
		Last Modified: Tue, 27 Jul 2021 00:00:54 GMT  
		Size: 226.2 MB (226163778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d712471081867811b8f91d7e802b55f2e02513cc40df28badeb381b3759c5e`  
		Last Modified: Tue, 27 Jul 2021 00:00:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764382cb1edbd5776cacf4ec7d81386930df4981cc1635683982c8ffeb1e5968`  
		Last Modified: Tue, 27 Jul 2021 00:01:34 GMT  
		Size: 145.3 MB (145275930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
