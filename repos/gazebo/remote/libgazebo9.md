## `gazebo:libgazebo9`

```console
$ docker pull gazebo@sha256:743e5523b651468aff4e4b3fda72116aecdc30998c9f0a7a33331e45cb6c8e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo9` - linux; amd64

```console
$ docker pull gazebo@sha256:795ae5de0784a6514219497488ed026ea4987d3ca5cfc5a0cea92206b4850f11
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.8 MB (413804733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6f0308cfcdf4058467ba92941d9bb71f5384756fa7cf8ef3f610c1a72c8889`
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
# Wed, 05 Oct 2022 17:43:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.19.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:43:53 GMT
EXPOSE 11345
# Wed, 05 Oct 2022 17:43:53 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Wed, 05 Oct 2022 17:43:53 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Wed, 05 Oct 2022 17:43:53 GMT
CMD ["gzserver"]
# Wed, 05 Oct 2022 17:46:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo9-dev=9.19.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:b2bed6b37c3eddafa72add9b5886afc104bb5b1aa30ad217ca7cf5c9bd07db63`  
		Last Modified: Wed, 05 Oct 2022 17:59:26 GMT  
		Size: 226.2 MB (226198244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d9ae6b867532b82f90a915b82744ca6fe4818af83c36fcd80e632b6c360a5d`  
		Last Modified: Wed, 05 Oct 2022 17:58:59 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbe425022e2225ca63dc468672091d949459faf03e57045b14ed06fedb15ff1`  
		Last Modified: Wed, 05 Oct 2022 18:00:01 GMT  
		Size: 145.3 MB (145347770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
