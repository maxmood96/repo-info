## `gazebo:libgazebo11`

```console
$ docker pull gazebo@sha256:ad230faa4a5be83cab2c44809bd83f44ecebd0b22a0f3651764cfdaf5bdacbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo11` - linux; amd64

```console
$ docker pull gazebo@sha256:27828f832d6fce25c237599b6d444164d7e43813925d9e1c4c00c6db80adf401
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.2 MB (612153799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9278b21e74ef19f4756bfd6128ce67773ed19f7553e535887d25be39d248f12f`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 01:24:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:24:39 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:24:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 18 Jun 2021 01:24:42 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Tue, 06 Jul 2021 17:44:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.7.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Jul 2021 17:44:46 GMT
EXPOSE 11345
# Tue, 06 Jul 2021 17:44:46 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Tue, 06 Jul 2021 17:44:47 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 06 Jul 2021 17:44:47 GMT
CMD ["gzserver"]
# Tue, 06 Jul 2021 17:50:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.7.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7068ef4db9e492493ff87fbf9095d1e4880263be63a6f42639411a96d5ed57f8`  
		Last Modified: Fri, 18 Jun 2021 02:27:02 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de016a33ce4c52c358d5182933555f132ede796ba07843ea5c1bdb742d9e61a`  
		Last Modified: Thu, 24 Jun 2021 19:46:45 GMT  
		Size: 16.1 MB (16149077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25740ed17f0991dfd51590656554367fc63d82af01be6cad451d1aaa514ba73`  
		Last Modified: Thu, 24 Jun 2021 19:46:42 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8dc1db69196852d66ee41dc90ac9918848d69a11a7a38240dcaf96e3c99074d`  
		Last Modified: Thu, 24 Jun 2021 19:46:42 GMT  
		Size: 5.5 KB (5507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c93a0df9409739d4b55d7b8581b8a8d362ca7d6a9155524f0563351dc7324f`  
		Last Modified: Tue, 06 Jul 2021 17:52:57 GMT  
		Size: 273.2 MB (273221601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0fdd68ebd8cca63514e84acec94f896d4e9ff58cb0e2a161fb9651ee300d20`  
		Last Modified: Tue, 06 Jul 2021 17:52:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091f92eda8908d457421b45eb9d0d45fb162600131260629c42932a6983cf3d2`  
		Last Modified: Tue, 06 Jul 2021 17:54:04 GMT  
		Size: 293.0 MB (293039817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
