## `gazebo:latest`

```console
$ docker pull gazebo@sha256:639f50cf89edd04df3be43ebd97f730affad8e95d94969a8d212e622ee487d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:latest` - linux; amd64

```console
$ docker pull gazebo@sha256:0e5f8bc15c5bf8ba44aff16c66ad3e38f10ba92438ccc792f72c51d20cda1838
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.6 MB (610561013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9731a1b002100d4a83f546886a015183041c39dd4660ea8bd911828847eafafc`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:44:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 02:45:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 02:45:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 03 Aug 2023 02:45:34 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 03 Aug 2023 02:48:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.13.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 02:48:35 GMT
EXPOSE 11345
# Thu, 03 Aug 2023 02:48:35 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 03 Aug 2023 02:48:35 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 03 Aug 2023 02:48:35 GMT
CMD ["gzserver"]
# Thu, 03 Aug 2023 02:52:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.13.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aab22f0326d7d89686f4eebe2ba52f86ca4e83a4c69d66dfe4f2b1494eae439`  
		Last Modified: Thu, 03 Aug 2023 02:53:09 GMT  
		Size: 1.2 MB (1198625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7537a4633286752d5bbe02fb22f93fc43f5d85fab59ced7194b862896ac1d1d`  
		Last Modified: Thu, 03 Aug 2023 02:53:09 GMT  
		Size: 16.2 MB (16177045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fdbcba4b60e13428e996857b320b2f6c63e807e5a913ad4ec5d47030d42cfeb`  
		Last Modified: Thu, 03 Aug 2023 02:53:06 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1541c109b80ce27f2bc1c68b6a83cd6685c14be2db0cd37146cd4fcf03bffc3f`  
		Last Modified: Thu, 03 Aug 2023 02:53:06 GMT  
		Size: 5.5 KB (5493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301117e166f8042dc24af9bb2f6693876e9489c550a53d244296be7757d01a48`  
		Last Modified: Thu, 03 Aug 2023 02:53:36 GMT  
		Size: 276.1 MB (276087586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b31485c9538417622ded1135b1af744c7ca3a7a6d237b47390172f32b2c29ee`  
		Last Modified: Thu, 03 Aug 2023 02:53:06 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1fe1d26217df6c9882ad7100b79c4415d5867a26506e7ecdbb212fd9cfbc814`  
		Last Modified: Thu, 03 Aug 2023 02:54:27 GMT  
		Size: 288.5 MB (288509964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
