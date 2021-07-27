## `gazebo:libgazebo11-focal`

```console
$ docker pull gazebo@sha256:f13ee3b8d8d24ea79e809fc5ace9342d7693a3617a1f5a6bf85bcdb4d808781d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:8fe0e781922e6da95eb137e5b81f78e5d3d74cfd0135d2ce9895631f0add7f2e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.0 MB (602982256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c208ba343c7eff40c51c79983c04c69527a1fb8d392b916521c26c0733b6061a`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:49:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:49:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Mon, 26 Jul 2021 23:49:33 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Mon, 26 Jul 2021 23:53:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.7.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:53:15 GMT
EXPOSE 11345
# Mon, 26 Jul 2021 23:53:15 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Mon, 26 Jul 2021 23:53:15 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Mon, 26 Jul 2021 23:53:16 GMT
CMD ["gzserver"]
# Mon, 26 Jul 2021 23:58:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.7.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52fa7f2bbaf9fdabe2f4f44c9c14e354edb50cbf9d14d543c25068e3bac43f3`  
		Last Modified: Tue, 27 Jul 2021 00:03:13 GMT  
		Size: 16.2 MB (16166865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82b78dfba60e8c933ef391fb029a1696247906bdb721ab7b16f27384a190896`  
		Last Modified: Tue, 27 Jul 2021 00:03:11 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfc640b65e76d09c20486b01253367703fec36621d99d69308307a3e4d62531f`  
		Last Modified: Tue, 27 Jul 2021 00:03:10 GMT  
		Size: 5.5 KB (5500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7807d871ce1350463426d0396446fa3f2a160fb9a1935ffdf6627e8ce4625c45`  
		Last Modified: Tue, 27 Jul 2021 00:03:42 GMT  
		Size: 272.4 MB (272439593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466c60bfcb630aaaa1efbb65fe80ef1aba49357968f4e5b4a430e7ec6e199954`  
		Last Modified: Tue, 27 Jul 2021 00:03:10 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d9568099ae8b4c3b7201de85b8edd49d310d0e9481cfa43f3b77ff20b173c0`  
		Last Modified: Tue, 27 Jul 2021 00:04:40 GMT  
		Size: 284.6 MB (284618248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
