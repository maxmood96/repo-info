## `gazebo:libgazebo11`

```console
$ docker pull gazebo@sha256:4b46fed5f7f804d05dad8af6d3b7af4a0a22f077f975a467151a26a16b980ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo11` - linux; amd64

```console
$ docker pull gazebo@sha256:2c20769db1d60f9dae20c40a11ae7be17409b7429b40e86cf4014541494e9c27
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.1 MB (618137821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37044fd400dd8c2bdb7c753f9e5fcf1f26f3f25daa73d74f4996075e3bd40720`
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
# Mon, 30 May 2022 18:35:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 30 May 2022 18:35:08 GMT
EXPOSE 11345
# Mon, 30 May 2022 18:35:08 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Mon, 30 May 2022 18:35:09 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Mon, 30 May 2022 18:35:09 GMT
CMD ["gzserver"]
# Mon, 30 May 2022 18:39:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.11.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:af80aceddebfeba37d40029780905d68a3794791cd885bcc9ef359b222f3e2ed`  
		Last Modified: Mon, 30 May 2022 18:42:13 GMT  
		Size: 275.9 MB (275927009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309af15bc351b407876041a9208d8512fb6787a2ae6e3914aee3aa2d1e8f527f`  
		Last Modified: Mon, 30 May 2022 18:41:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c50c8df04bae5ffb6b69322e38cf6f33ce41d1a499692327b60fa74dedd582f`  
		Last Modified: Mon, 30 May 2022 18:43:11 GMT  
		Size: 296.3 MB (296286620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
