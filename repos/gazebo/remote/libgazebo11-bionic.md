## `gazebo:libgazebo11-bionic`

```console
$ docker pull gazebo@sha256:6f44835c577c5a10b1db4ca3fe26bd202e56a125eb3a8fb18b168bc9d806ff4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo11-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:d52d9051842c0f20f9d66094a76a1e9f234ecd0c5fde9460c17dc3a283ba3670
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.7 MB (546705042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f37074c6416e89105c5f756fd6e2b3d4dc942f6f555b3af10eccad10ecc7d98`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 04:22:57 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 06:39:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 06:39:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Tue, 31 Aug 2021 06:39:14 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Tue, 31 Aug 2021 06:47:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.8.1-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 06:47:09 GMT
EXPOSE 11345
# Tue, 31 Aug 2021 06:47:09 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Tue, 31 Aug 2021 06:47:10 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 31 Aug 2021 06:47:10 GMT
CMD ["gzserver"]
# Tue, 31 Aug 2021 06:49:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.8.1-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cd3aa01fa8a2dad33dee176be919cf9e72b3b56c4289e1c823911634874027`  
		Last Modified: Tue, 31 Aug 2021 05:00:05 GMT  
		Size: 840.6 KB (840612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e05c50ab5c761da2419248fab70f5e9f08c46d2ef34cdff43c7906bc6f9a659`  
		Last Modified: Tue, 31 Aug 2021 07:01:30 GMT  
		Size: 14.7 MB (14702959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855ed3830ce0b2220e748c837c62382ae827bc93deb18930070be41ef1999781`  
		Last Modified: Tue, 31 Aug 2021 07:01:27 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b029e0b34632e03a59de48ba14e54b9014ebdbd516a59bae76b2443ea024df9`  
		Last Modified: Tue, 31 Aug 2021 07:01:27 GMT  
		Size: 5.5 KB (5458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8e7fa84f0232d2c9552c42262de4fcfbc6f22ea96957fea9d2df522f0301f8`  
		Last Modified: Tue, 31 Aug 2021 07:03:13 GMT  
		Size: 235.2 MB (235200772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302a1a0d92164b2f935b32ce8dee565cf13f149f6fe3d5243fa06a817708f4d7`  
		Last Modified: Tue, 31 Aug 2021 07:02:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38bc8cedb7710573b187e7d64036916a8aaad5b39b9978bcfdddb9514d50a44`  
		Last Modified: Tue, 31 Aug 2021 07:03:58 GMT  
		Size: 269.2 MB (269245103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
