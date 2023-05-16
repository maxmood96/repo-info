## `gazebo:gzserver11-bionic`

```console
$ docker pull gazebo@sha256:66f8ce922c0071bd289f8f223e434c3fcf7f4fb3653181a0370a0e6d70378879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:gzserver11-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:26af4ef5467cd9839c6b4d565c29adfb73b875d0d0bf295f11601d5bacb922d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.8 MB (277839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433fc504932b39714a1ec986790fab99e37704f0d54f8bbd1fa1337cf1a7bed7`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 12 May 2023 09:41:51 GMT
ARG RELEASE
# Fri, 12 May 2023 09:41:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 May 2023 09:41:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 May 2023 09:41:51 GMT
LABEL org.opencontainers.image.version=18.04
# Fri, 12 May 2023 09:41:52 GMT
ADD file:47682dd3869ca8e57ceb15f69a6ac7c9048d4d42c7a99a976e597cf072423c12 in / 
# Fri, 12 May 2023 09:41:53 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 01:04:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:27:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:27:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Tue, 16 May 2023 01:28:00 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Tue, 16 May 2023 01:29:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.12.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:29:12 GMT
EXPOSE 11345
# Tue, 16 May 2023 01:29:12 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Tue, 16 May 2023 01:29:12 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 16 May 2023 01:29:12 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:c67806d7e72dd941e600bad2eabe920a17ba1852b325b63900c819ffeae646fb`  
		Last Modified: Tue, 16 May 2023 01:01:48 GMT  
		Size: 26.7 MB (26715509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8112c7660661f5d395aac99b0d2403ccaaf47cfce01b40167688a866847d540`  
		Last Modified: Tue, 16 May 2023 01:17:48 GMT  
		Size: 819.1 KB (819098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af0f112a641a7dded1a88984b00a91588e94005222eeff72c7129e47da5d459`  
		Last Modified: Tue, 16 May 2023 01:31:16 GMT  
		Size: 14.7 MB (14714973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1424c132b637c9b241d1a15e87e4179e7944aeb54faea5226d25e13807383d`  
		Last Modified: Tue, 16 May 2023 01:31:13 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf505bb02aa45e02532816e9c00f3bca0eb1328f7422b250e79387318fc6123f`  
		Last Modified: Tue, 16 May 2023 01:31:14 GMT  
		Size: 5.5 KB (5459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009c28d8f09cb72e0548221671bdee67734ccce37a6fda4eedb2d1ffddbaed0e`  
		Last Modified: Tue, 16 May 2023 01:31:40 GMT  
		Size: 235.6 MB (235582511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa7a423553ceddf958206ca43710de0f0eaab7c27469045dad40ff413d72d2b`  
		Last Modified: Tue, 16 May 2023 01:31:14 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
