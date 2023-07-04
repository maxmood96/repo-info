## `gazebo:libgazebo11-focal`

```console
$ docker pull gazebo@sha256:82fc4ffb79cfd230def2fda4b0691cf98e24da8f24bd72ff9601606fdde8f636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:7ad81317a58dfeddbc5add06aefaf371eddcf4197a3d3f1c72058549ea03d0c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.5 MB (610513873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3765e10cb018a6c00a27924509eb9c8000d13450089da3ffe19956fce3aa49`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:38:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:44:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:44:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Tue, 04 Jul 2023 20:44:21 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Tue, 04 Jul 2023 20:47:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.13.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:47:28 GMT
EXPOSE 11345
# Tue, 04 Jul 2023 20:47:28 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Tue, 04 Jul 2023 20:47:28 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 04 Jul 2023 20:47:28 GMT
CMD ["gzserver"]
# Tue, 04 Jul 2023 20:51:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.13.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff84dd75ab0363da2809c202391ffc2d59534b4888fb855bfd3e21fba17c6fc`  
		Last Modified: Tue, 04 Jul 2023 20:06:54 GMT  
		Size: 1.2 MB (1198708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138900508d89d15fbba39a3eb1b15017ad986cddb3cb414ddfefdbcaa67f2bd4`  
		Last Modified: Tue, 04 Jul 2023 20:52:08 GMT  
		Size: 16.2 MB (16177153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414da1835970c9218256ae74326f55fe95627d370426249e90e14dbc81ff0b5e`  
		Last Modified: Tue, 04 Jul 2023 20:52:04 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4261e9dd1b459c29c59d9495c76e53a9f693f9a107efa249826c6424998babd4`  
		Last Modified: Tue, 04 Jul 2023 20:52:04 GMT  
		Size: 5.5 KB (5500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9a87760e7c134e957008e996b2b9bd4518bddbbe54df508271c754c9c75784`  
		Last Modified: Tue, 04 Jul 2023 20:52:34 GMT  
		Size: 276.0 MB (276024942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9380a249beca875add1df17ca99b1c6eb1f1d4eb87ee4b9d1e26c2d6e67025`  
		Last Modified: Tue, 04 Jul 2023 20:52:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82512c5c8e7727327e6f6177e65e65c25093c268160923cea71cb63867532781`  
		Last Modified: Tue, 04 Jul 2023 20:53:26 GMT  
		Size: 288.5 MB (288525925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
