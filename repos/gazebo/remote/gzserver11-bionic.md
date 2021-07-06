## `gazebo:gzserver11-bionic`

```console
$ docker pull gazebo@sha256:95a9cd0156c1edd9d7670940cc32660b47824b3691ebe0b64b81240a57d47bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver11-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:4954c4f37d926a896727bcea98f7bb46096969659da4d8dfdca17cfba0174af4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277452459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e96c36d1ca4caa06f3f8ded20e2f57081c9968c21beeaa9f43320a1b8e099c1`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 01:23:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:23:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:23:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 18 Jun 2021 01:23:35 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Tue, 06 Jul 2021 17:35:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.7.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Jul 2021 17:35:56 GMT
EXPOSE 11345
# Tue, 06 Jul 2021 17:35:56 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Tue, 06 Jul 2021 17:35:56 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 06 Jul 2021 17:35:56 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da448bd4f8f4db94a9b5039505342a7b53dd81b10fd374d2def1098fb0ac84d1`  
		Last Modified: Fri, 18 Jun 2021 02:24:11 GMT  
		Size: 841.3 KB (841252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c9bccca2de788969af6d6e387abb084c66ce0679c41ca4712bf3787173a3b8`  
		Last Modified: Thu, 24 Jun 2021 19:43:56 GMT  
		Size: 14.7 MB (14702322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97918488cc093177c1052f8a9ec4c7729f138fe79a40137d1a3198f8ac2de6e`  
		Last Modified: Thu, 24 Jun 2021 19:43:53 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389903f5c318711646c39cd700afeaea7d7beac2750a1953f8325917e500ffcb`  
		Last Modified: Thu, 24 Jun 2021 19:43:53 GMT  
		Size: 5.5 KB (5459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27021722adc2f8414bd9c1e664203052abd51d396a9bc161af4e25fd94586b70`  
		Last Modified: Tue, 06 Jul 2021 17:51:21 GMT  
		Size: 235.2 MB (235201093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050c77a065fef1685fed5c781331ede456463027ad9c5d782539e31efdb43d38`  
		Last Modified: Tue, 06 Jul 2021 17:50:48 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
