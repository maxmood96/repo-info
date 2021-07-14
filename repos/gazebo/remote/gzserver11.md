## `gazebo:gzserver11`

```console
$ docker pull gazebo@sha256:a875480fcffa3f731ea4e00312287698916bf4dc6f69242303434dbf00c9fbda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver11` - linux; amd64

```console
$ docker pull gazebo@sha256:b4d1edd4177d316ec141248dfac78f001097eb46d145dd3a800f4531a1a6a91b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318358017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e204633d2b7ae5edb36ad288b07ab89cf4fc749fd51ce0897ac4fb5a94e85493`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:04:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:04:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Tue, 13 Jul 2021 23:04:56 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Tue, 13 Jul 2021 23:08:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.7.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:08:45 GMT
EXPOSE 11345
# Tue, 13 Jul 2021 23:08:45 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Tue, 13 Jul 2021 23:08:45 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 13 Jul 2021 23:08:45 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ac0af9608ebe50db5c9883ba2cc0fb4d341457cd84787a41bcf8a4a1559fed`  
		Last Modified: Tue, 13 Jul 2021 23:17:15 GMT  
		Size: 1.2 MB (1182378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e24c8e58e8995813e977d84d9b4b70f59ea1fd8685a16376a7aef93227de640`  
		Last Modified: Tue, 13 Jul 2021 23:17:15 GMT  
		Size: 16.2 MB (16166747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99af40a43aae3a339cdf4db15d28f29676d5aa0e759e39c7ab29035fda693deb`  
		Last Modified: Tue, 13 Jul 2021 23:17:12 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf233bacae35f81d68116020486b6c8da1e29af39321a000f180e87953a8eee`  
		Last Modified: Tue, 13 Jul 2021 23:17:12 GMT  
		Size: 5.5 KB (5496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6791d5cd77db81c310f568ada8538db2552d8369c10a350f276a4f515a39a076`  
		Last Modified: Tue, 13 Jul 2021 23:17:45 GMT  
		Size: 272.4 MB (272435908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2a479f3f097d9bd55e44da4c3fd7f6c7c2db8ce3ee6449264c87a11670d04e`  
		Last Modified: Tue, 13 Jul 2021 23:17:12 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
