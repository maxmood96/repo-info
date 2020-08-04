## `gazebo:libgazebo9-stretch`

```console
$ docker pull gazebo@sha256:f69b5240be0aa7267bcadb19601cacfda718055ed4b80d232c29f64521621f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9-stretch` - linux; amd64

```console
$ docker pull gazebo@sha256:2863af9122312c568a1e5392dc7191f852594b25c20a3675d79095c316b04678
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.8 MB (569757274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f052838daace089f1d71be8bd4272a92316107b21038caf778403edd10614a`
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
# Tue, 04 Aug 2020 22:47:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     libgazebo9-dev=9.13.2-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:12a384cc22cc1c5be94ef37e561f5ea36ab9cfee66ff72f25ce60476cf13a723`  
		Last Modified: Tue, 04 Aug 2020 22:51:56 GMT  
		Size: 303.8 MB (303839848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
