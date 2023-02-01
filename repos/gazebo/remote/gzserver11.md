## `gazebo:gzserver11`

```console
$ docker pull gazebo@sha256:7b039872bdd4ca00ed33f8e662d28a0fcb622f160a8c8a14cda3f3d8e4599fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:gzserver11` - linux; amd64

```console
$ docker pull gazebo@sha256:70c296947a231fbb3f17a6f448cfea5a98c6d73db6a6e339ad4ab18516767b36
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.9 MB (321938797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3c3e36904a0974c53f61dbc8c77242f475324fad1f13259e6839da44c7eb1f`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 18:45:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 18:45:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 18:45:35 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Wed, 01 Feb 2023 18:45:36 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Wed, 01 Feb 2023 18:51:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.12.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 18:51:47 GMT
EXPOSE 11345
# Wed, 01 Feb 2023 18:51:47 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Wed, 01 Feb 2023 18:51:47 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Wed, 01 Feb 2023 18:51:47 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db143da9f5a088b47cfbe87905f9e615f3b537f906257fc11ac7a38ffb0f236c`  
		Last Modified: Wed, 01 Feb 2023 18:58:42 GMT  
		Size: 1.2 MB (1154526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2930b93887660d25415790ec0cc4ab3c63026ea3dbc2def03b6620e17eb2c69`  
		Last Modified: Wed, 01 Feb 2023 18:58:43 GMT  
		Size: 16.2 MB (16176108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970ca3fa21611eee1c7922db8c9ea92c2277eebd390cef724c7b14a540787389`  
		Last Modified: Wed, 01 Feb 2023 18:58:40 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0708864b0ce5d27bdd1c40322948fe74da8edc904befa210e21b484679168317`  
		Last Modified: Wed, 01 Feb 2023 18:58:40 GMT  
		Size: 5.5 KB (5497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4def66b79ae6a92eb4f8512b798e7eb933caa3fefad2b8f18d87c38803f57263`  
		Last Modified: Wed, 01 Feb 2023 18:59:13 GMT  
		Size: 276.0 MB (276023154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5dca95fb4a76e8def6593aa8dd7981abad77edb514c48e62dc50a63aab4717`  
		Last Modified: Wed, 01 Feb 2023 18:58:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
