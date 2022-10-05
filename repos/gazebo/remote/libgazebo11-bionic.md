## `gazebo:libgazebo11-bionic`

```console
$ docker pull gazebo@sha256:b07c550ff00bc3df2f54aa5ba365c224b39a15769a2e5c3f16e08c368aaf80a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo11-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:439bcb445ff97dd5aeeb8fde296be643194f68d0804ec759e478dcfeb902d598
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.2 MB (547225421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48185b92c48f4d66febf1b90802f82d0b649f88d475de14878ce549b21f501c4`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:04 GMT
ADD file:ed601c56cf74241eeb1971b24ed969fb855cd2b9330276d3c5779ecdb0b28364 in / 
# Tue, 04 Oct 2022 23:35:04 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 09:49:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:40:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:40:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Wed, 05 Oct 2022 17:40:56 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Wed, 05 Oct 2022 17:47:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.12.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:47:55 GMT
EXPOSE 11345
# Wed, 05 Oct 2022 17:47:56 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Wed, 05 Oct 2022 17:47:56 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Wed, 05 Oct 2022 17:47:56 GMT
CMD ["gzserver"]
# Wed, 05 Oct 2022 17:50:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.12.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e706e0a9f42365312b366bf4caa22f3cdd8fc7fd8f6f49b4dd3782711f66aca7`  
		Last Modified: Tue, 04 Oct 2022 11:37:26 GMT  
		Size: 26.7 MB (26711852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ec163f2e73ca4c7df5142df330fb9169325367e235b65c457afcc3bf320f35`  
		Last Modified: Wed, 05 Oct 2022 10:47:14 GMT  
		Size: 831.0 KB (831002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb5832fa364dd6f03f1b99838bac548d5b8d7a2395a33221fa20b20cfc558d1`  
		Last Modified: Wed, 05 Oct 2022 17:59:01 GMT  
		Size: 14.7 MB (14708778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069daecaba9808a64427fdf457e9a7f2d0848e1a852a163310d4a8dcd516ea76`  
		Last Modified: Wed, 05 Oct 2022 17:58:59 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230b1fb259b86f90a7d2392ca30e5dc724a0bdac449f7e3d2e540ae20a1958db`  
		Last Modified: Wed, 05 Oct 2022 17:58:59 GMT  
		Size: 5.5 KB (5460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b222699ea7083b4eaaf8a547797a2b0ec7f085af64ce323eb97eef79fcc9ca7`  
		Last Modified: Wed, 05 Oct 2022 18:00:40 GMT  
		Size: 235.6 MB (235567963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4564136c02b996afab633035341614a90ea45c7dfa0a8631e6edb501e4a5db22`  
		Last Modified: Wed, 05 Oct 2022 18:00:12 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d46c25df459f9f9b3253cba9f1fc2696accd83f88ae112ce7e4ad2fe08f117`  
		Last Modified: Wed, 05 Oct 2022 18:01:32 GMT  
		Size: 269.4 MB (269398738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
