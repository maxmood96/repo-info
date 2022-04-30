## `gazebo:libgazebo9-bionic`

```console
$ docker pull gazebo@sha256:cd712649835e683b6f4a803d9e6f82e191266d5cce70bd8167e6774ada4da685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo9-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:847f8f402c956bca8eccaa9a15fdbbbfaa9d0daa4f739ce79283e5581ac8160d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.7 MB (413695400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cf14bfbe696d4c2496e62990b319e3516ad9df1be028e69df64807e153a259`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:51 GMT
ADD file:f657a56a18426c3a88d620a7024e7b91424d926e7b47faa6a97c2369c4c4a228 in / 
# Fri, 29 Apr 2022 23:20:51 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:29:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:29:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:29:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Sat, 30 Apr 2022 00:30:00 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Sat, 30 Apr 2022 00:32:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.19.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:32:55 GMT
EXPOSE 11345
# Sat, 30 Apr 2022 00:32:55 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Sat, 30 Apr 2022 00:32:55 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Sat, 30 Apr 2022 00:32:55 GMT
CMD ["gzserver"]
# Sat, 30 Apr 2022 00:35:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo9-dev=9.19.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:40dd5be53814ae70b2898558673b7ea18d58bf7ab3433560b9ce3cb76d9ff0b1`  
		Last Modified: Fri, 29 Apr 2022 23:22:07 GMT  
		Size: 26.7 MB (26709108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c6e4dbac2549834f9ff8126148bc819d27a613ba3783701cdafd265b966467`  
		Last Modified: Sat, 30 Apr 2022 00:47:48 GMT  
		Size: 839.0 KB (839025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc6139aa6bacaa2124240380fcb17a6deae2ad085841b79567e4b59b5076c3d`  
		Last Modified: Sat, 30 Apr 2022 00:47:48 GMT  
		Size: 14.7 MB (14706444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ef827375b3bc57c0b4b6d560815b0675b8828d7fdb11ea6fc8b70a6ed088bd`  
		Last Modified: Sat, 30 Apr 2022 00:47:46 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e416be6a5bd50cd1188ce0b6b0adc86194d21e5aa8fe2968053d87215f8ed810`  
		Last Modified: Sat, 30 Apr 2022 00:47:46 GMT  
		Size: 5.5 KB (5461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a73c0842ee2382f0de5056f258e3bfafbee314a522f55436b29cb70b4fe6da8`  
		Last Modified: Sat, 30 Apr 2022 00:48:13 GMT  
		Size: 226.2 MB (226161531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699fd6172d31f0e3ced534877ac8da96a17aa9e5505df7c0df7729b667fb2251`  
		Last Modified: Sat, 30 Apr 2022 00:47:46 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c0cfe0884a3b1b76971a88c73beaab5049279ffa2fca8ae82e8254001b6ae2`  
		Last Modified: Sat, 30 Apr 2022 00:48:48 GMT  
		Size: 145.3 MB (145272205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
