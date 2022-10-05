## `gazebo:libgazebo11`

```console
$ docker pull gazebo@sha256:a04601a527d4c39750c455a4a53b5b68636bac59cfc8dd50dcb905009873088d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo11` - linux; amd64

```console
$ docker pull gazebo@sha256:14aa5f99c5a2a357981d3afb338c493ac893153b8510e39464358d873b6f9fc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.4 MB (610438761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ece1154fa8590e25c3e2033e8be1fd13ca37e79f5a18d45fa3fac38e5909eab`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 10:02:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:50:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:50:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Wed, 05 Oct 2022 17:50:50 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Wed, 05 Oct 2022 17:53:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.12.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:53:57 GMT
EXPOSE 11345
# Wed, 05 Oct 2022 17:53:58 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Wed, 05 Oct 2022 17:53:58 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Wed, 05 Oct 2022 17:53:58 GMT
CMD ["gzserver"]
# Wed, 05 Oct 2022 17:58:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.12.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db398de1191a2231a78b6d5d54baa0f980aa763df67adb3394a7269111109671`  
		Last Modified: Wed, 05 Oct 2022 10:50:03 GMT  
		Size: 1.2 MB (1163849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca8c33c5296e4c69f417538eea6c604203cf271ccfc4faebd5df1aef30e30d8`  
		Last Modified: Wed, 05 Oct 2022 18:01:46 GMT  
		Size: 16.2 MB (16177421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0fcc706ab7b608c9d455d3172fda360a318b369274666207464896fdf0bba3`  
		Last Modified: Wed, 05 Oct 2022 18:01:44 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d515514d75fa295bca4d644698133f0dff17e267d730637fbf49b0c4dc2a1c`  
		Last Modified: Wed, 05 Oct 2022 18:01:43 GMT  
		Size: 5.5 KB (5503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16f7983d30aeb00ef0a769cf5b1a919605520610974804dbb38af28fef4d2ac`  
		Last Modified: Wed, 05 Oct 2022 18:02:21 GMT  
		Size: 276.0 MB (276020990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba5555afa5af071549a38bd8d8edc97d7f72057d3612568309c31a2ceac0dd3`  
		Last Modified: Wed, 05 Oct 2022 18:01:44 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ca23350175b9862e5971293573f85bad80bf1fb1c324ee008332f5c19d1246`  
		Last Modified: Wed, 05 Oct 2022 18:03:19 GMT  
		Size: 288.5 MB (288494920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
