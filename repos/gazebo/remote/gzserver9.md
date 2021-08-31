## `gazebo:gzserver9`

```console
$ docker pull gazebo@sha256:0d70a7d9bbfdd8e10ece6a13eb1b40fd50f8b2a0827f301c587478a389120ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:gzserver9` - linux; amd64

```console
$ docker pull gazebo@sha256:e2e309ef20f4c2369c80a3b3ef4904fb9eaa010959aa5d7b69eb5d056aef1852
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.4 MB (268422511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84921e5caf1eda293e7c0916d12847ddeca03e632533aba503946f611620698b`
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
# Tue, 31 Aug 2021 06:42:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.19.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 06:42:54 GMT
EXPOSE 11345
# Tue, 31 Aug 2021 06:42:54 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Tue, 31 Aug 2021 06:42:54 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 31 Aug 2021 06:42:55 GMT
CMD ["gzserver"]
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
	-	`sha256:bd63f3eced698338918dd982d78afe1b3b96aa4b155833440e22a1e53a414412`  
		Last Modified: Tue, 31 Aug 2021 07:01:54 GMT  
		Size: 226.2 MB (226163342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1442d2f5db987e8bc5f31703b6f91234ad541c44a2f33f523ab1634c4ef410e`  
		Last Modified: Tue, 31 Aug 2021 07:01:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
