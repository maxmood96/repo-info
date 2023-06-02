## `gazebo:libgazebo11-bionic`

```console
$ docker pull gazebo@sha256:c0bc17d5cb72d98c58a862c3b9b2de281538c725c2fa925280588c97176edc3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo11-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:7a4e450f2f5ef614ea24c3611668895119863554578a8bd0d917e44373e8a200
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.3 MB (547331363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644ddabb1b9404d428e9dceb169a089c09c5962fe5d304b46c33c90470e8be6c`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 00:55:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:55:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:55:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 02 Jun 2023 00:55:39 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Fri, 02 Jun 2023 00:58:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.13.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:58:17 GMT
EXPOSE 11345
# Fri, 02 Jun 2023 00:58:17 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Fri, 02 Jun 2023 00:58:17 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Fri, 02 Jun 2023 00:58:18 GMT
CMD ["gzserver"]
# Fri, 02 Jun 2023 01:01:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.13.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27456075680427d55e79ddce0ccec278d1f81ab5181d13386de5ac3f085b90`  
		Last Modified: Fri, 02 Jun 2023 01:02:13 GMT  
		Size: 818.9 KB (818915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208a5fc38d6686d09afe4c36d24561e6952f5e2a37e4fe3aed10fc679393e454`  
		Last Modified: Fri, 02 Jun 2023 01:02:13 GMT  
		Size: 14.7 MB (14714619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f1c4414805c51da59d1c81cf6d3cdb4a6416e4b1523359595d62645908563b`  
		Last Modified: Fri, 02 Jun 2023 01:02:10 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7c470423b35bccea898315bb522fff6efe67c1fa66231d3d86719a7f7a9863`  
		Last Modified: Fri, 02 Jun 2023 01:02:10 GMT  
		Size: 5.5 KB (5457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb88345d023b392cd3408b3c810acc86f53c792051de6fd2e9069e9de312a81`  
		Last Modified: Fri, 02 Jun 2023 01:02:37 GMT  
		Size: 235.6 MB (235581256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827441c984c9f0878ee0294f1cf4e8de836c7d902ecb38d232d8b671a480e4f1`  
		Last Modified: Fri, 02 Jun 2023 01:02:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a17b0d2225097785cfc72ac1e963298ac0625f0343f97f0f420f2d4b7f8336d`  
		Last Modified: Fri, 02 Jun 2023 01:03:18 GMT  
		Size: 269.5 MB (269492128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
