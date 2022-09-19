## `gazebo:gzserver11-bionic`

```console
$ docker pull gazebo@sha256:0ed71885129a2883e0f983eecec3a3ab9ef15b849a192cb5f8cce97702653539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:gzserver11-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:79ad94e66062f6876e27a492337067df01d4d25e4fc168c38a1a1372cb08b804
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.8 MB (277815717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d91773bf1a362f22a4e11e0e03966287887adb6dd041e8e853a0a1499c9bec`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 06 Sep 2022 19:38:36 GMT
ADD file:8733c7e8faf03d53cb2143ff6ac405362944cfa07422fccd21a3066cc2f42c83 in / 
# Tue, 06 Sep 2022 19:38:37 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 20:08:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 20:08:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 20:08:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Tue, 06 Sep 2022 20:08:14 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Mon, 19 Sep 2022 17:50:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.12.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 19 Sep 2022 17:50:25 GMT
EXPOSE 11345
# Mon, 19 Sep 2022 17:50:26 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Mon, 19 Sep 2022 17:50:26 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Mon, 19 Sep 2022 17:50:26 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:726b8a513d66e3585eb57389171d97fcd348e4914a415891e1da135b85ffa6c3`  
		Last Modified: Fri, 02 Sep 2022 15:41:13 GMT  
		Size: 26.7 MB (26710833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4768d9bcc163805ab5ecfee0d555df97a3b8eaadc5b4bf8e8b458c12e089102a`  
		Last Modified: Tue, 06 Sep 2022 20:16:26 GMT  
		Size: 831.0 KB (830982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d4d0f23e3d912c53609ab1be508ea52480495f1e93e47c5e2b107c4969b20f`  
		Last Modified: Tue, 06 Sep 2022 20:16:26 GMT  
		Size: 14.7 MB (14709179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf438ef6aac76bc018f4485e7292597740d514f8946170fe8b20ae459c909228`  
		Last Modified: Tue, 06 Sep 2022 20:16:24 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94106123bc7e51b0b61ac37d458ee8f95ec1b09e442f9c245cab9638803c3a5e`  
		Last Modified: Tue, 06 Sep 2022 20:16:24 GMT  
		Size: 5.5 KB (5460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1c8bc11a68c99a64df89b9f4c0b8193b751768fc8d020c5a3ec49f6ac27750`  
		Last Modified: Mon, 19 Sep 2022 18:04:07 GMT  
		Size: 235.6 MB (235557634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:490e421e2cc97d820799d8191b4c0b1558294fe116e960c737334c56e79b3667`  
		Last Modified: Mon, 19 Sep 2022 18:03:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
