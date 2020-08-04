## `gazebo:gzserver9-stretch`

```console
$ docker pull gazebo@sha256:ca94a17f0d4731b6f88679989cb9bc0a326b3c6aa3715f9af95514b666de6903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver9-stretch` - linux; amd64

```console
$ docker pull gazebo@sha256:010c8e23e351cc12d2c1682f18caab61a99e55488663f4716acc8586002d6d6c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.9 MB (265917426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c0ecda8b0f19b77dda3b2d6c6dbb1ddcf9b397c60bf177cbc2906e95098184`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:32 GMT
ADD file:a28d8a949b7577768d87fcbac346797fc5f7bad0539625339edcd09a32d6bf77 in / 
# Tue, 04 Aug 2020 15:45:33 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 22:45:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 22:45:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Tue, 04 Aug 2020 22:45:32 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Tue, 04 Aug 2020 22:46:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo9=9.13.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 22:46:22 GMT
EXPOSE 11345
# Tue, 04 Aug 2020 22:46:22 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Tue, 04 Aug 2020 22:46:22 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 04 Aug 2020 22:46:23 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:419e7ae5bb1e4875c367f3249b7bb7f8f39dd27dfceb4ee9d6a92191ed1c452f`  
		Last Modified: Tue, 04 Aug 2020 15:52:05 GMT  
		Size: 45.4 MB (45366706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9362859687a2d84c177a1f5dced4161a8c7c4b26ba928f113d95d153b24ea13`  
		Last Modified: Tue, 04 Aug 2020 22:50:24 GMT  
		Size: 18.5 MB (18514064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5637391b288d62be110136b1be071741c95edb378755e4401b398b826b9f718`  
		Last Modified: Tue, 04 Aug 2020 22:50:19 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce69c2f0891ae2abe2f10f2eab367c3f4aaa94179a17575962179b9c4e67e62`  
		Last Modified: Tue, 04 Aug 2020 22:50:19 GMT  
		Size: 5.0 KB (4982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc877507a62ff41bd4afb37e6a8e2af2fd397c7a905bf1d35969ad267206ab5`  
		Last Modified: Tue, 04 Aug 2020 22:50:58 GMT  
		Size: 202.0 MB (202030068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82a93d3d0106e86f76eddecaf44723dccd2df48786af3d677183c61ba21edd3`  
		Last Modified: Tue, 04 Aug 2020 22:50:19 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
