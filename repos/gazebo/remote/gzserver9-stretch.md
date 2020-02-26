## `gazebo:gzserver9-stretch`

```console
$ docker pull gazebo@sha256:84b27732a0f4937b36fc4b8c19e8e5b12f6bd6ee9b487d597e9e4f3fb9e7eb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver9-stretch` - linux; amd64

```console
$ docker pull gazebo@sha256:78b07bd5e8170f067f196cf5f81e5a128332f48176efda9745697f6e630b6152
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.3 MB (346348500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2362b6c07dd52fcfdf0bf0479d5f04ea994c6624a03c5e41c575970d793ec572`
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
