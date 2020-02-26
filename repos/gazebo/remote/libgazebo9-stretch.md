## `gazebo:libgazebo9-stretch`

```console
$ docker pull gazebo@sha256:991631beceb7ebb8dc16b5c7847d7e62f6564a52307aefaa8901d634463b9267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9-stretch` - linux; amd64

```console
$ docker pull gazebo@sha256:2d3c8909a3d5e9a73073af42ddbfb13c242428beb84c8ac5804ac93544777cea
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.9 MB (650928603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fd42fd3985fd85fde51ead2d9ed7d6279816886b1fc77fb0111cee5260bcdb`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:14 GMT
ADD file:08c5ab7c53526da155d6be40a9795fc08afc9f47bd333c096e90185fe9fab2b1 in / 
# Wed, 26 Feb 2020 00:41:14 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:27:32 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Wed, 26 Feb 2020 01:27:37 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Wed, 26 Feb 2020 01:28:56 GMT
RUN apt-get update && apt-get install -q -y     gazebo9=9.12.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:28:57 GMT
EXPOSE 11345
# Wed, 26 Feb 2020 01:28:57 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Wed, 26 Feb 2020 01:28:57 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Wed, 26 Feb 2020 01:28:58 GMT
CMD ["gzserver"]
# Wed, 26 Feb 2020 01:30:52 GMT
RUN apt-get update && apt-get install -q -y     libgazebo9-dev=9.12.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c0c53f743a403d45480d026864d9611d6eb898e897d60c13ae854ad453d462a4`  
		Last Modified: Wed, 26 Feb 2020 00:47:05 GMT  
		Size: 45.4 MB (45375932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9206dbb9aeb9b048d4ae5913aa16cc110c51239db67e87e4b02ea4eba67968b`  
		Last Modified: Wed, 26 Feb 2020 01:31:37 GMT  
		Size: 21.1 MB (21095010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3235ffeaa37e1282caa0fed6342d71cab6e4f41271f33b3fea0cc3377bceb40a`  
		Last Modified: Wed, 26 Feb 2020 01:31:31 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c38001383936ac81de9c49be4ed614ad85380a866fcf47a449e7f3539add298`  
		Last Modified: Wed, 26 Feb 2020 01:31:31 GMT  
		Size: 5.0 KB (4975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28632871feba23c58d4f4f17f62f24dca1166aad3eda8ae0d773067f0e77ab26`  
		Last Modified: Wed, 26 Feb 2020 01:32:17 GMT  
		Size: 279.9 MB (279870974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8865eab45788c1afd17c34f8d988483093cbd1e8030184466068206192f937`  
		Last Modified: Wed, 26 Feb 2020 01:31:31 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28a1783e85d2dff781b60124bf57685ec02654be020bf3f1e45515c2e6b3dd8`  
		Last Modified: Wed, 26 Feb 2020 01:33:17 GMT  
		Size: 304.6 MB (304580103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
