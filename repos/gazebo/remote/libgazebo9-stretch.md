## `gazebo:libgazebo9-stretch`

```console
$ docker pull gazebo@sha256:7666b00e5c24390bc87ae4203243b6a711aec1f535cb8f4336ee12c845d5f7b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9-stretch` - linux; amd64

```console
$ docker pull gazebo@sha256:be29771d12824fd0b4c324f8a544cdfb401560f08780692e79611c6b0ea0b3e7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.3 MB (570250040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8f5fb249dfecbad976a15783a24438dc4e4688a39b46ac14d19baf22fb58c6`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:36 GMT
ADD file:5f8ab4280b54d91475c84e497163ec05aabb5a9f9b9de687d38fda535ddc29b2 in / 
# Fri, 12 Mar 2021 02:22:36 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 09:52:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 09:52:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 12 Mar 2021 09:52:47 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Fri, 12 Mar 2021 09:53:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.16.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 09:53:54 GMT
EXPOSE 11345
# Fri, 12 Mar 2021 09:53:55 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Fri, 12 Mar 2021 09:53:55 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Fri, 12 Mar 2021 09:53:55 GMT
CMD ["gzserver"]
# Fri, 12 Mar 2021 09:55:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo9-dev=9.16.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16cf3fa6cb1190b4dfd82a5319faa13e2eb6e69b7b4828d4d98ba1c0b216e446`  
		Last Modified: Fri, 12 Mar 2021 02:29:57 GMT  
		Size: 45.4 MB (45380216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e059a7b3517c1d53a9c77e6e315800a8543ad1bf60b317dadb13965a5b462c07`  
		Last Modified: Fri, 12 Mar 2021 10:21:48 GMT  
		Size: 18.5 MB (18512387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e06efaf60aeb5e99279cd20097541b0ceeaf36651c1ff19f46c86b2f2bcd84e`  
		Last Modified: Fri, 12 Mar 2021 10:21:42 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927fa66d613d0f87d97f9c3919a163f60764c5d6e43c47600da195fe0fa325c5`  
		Last Modified: Fri, 12 Mar 2021 10:21:42 GMT  
		Size: 5.0 KB (5013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcde7efca5521588a2a9b709cdbb26f7fe672a1aff0375fd75ee90592d1279e`  
		Last Modified: Fri, 12 Mar 2021 10:22:21 GMT  
		Size: 202.3 MB (202283517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b402931f9fbccb4439e64b8caaff73931592a370efeab3d700b1deed42a7a1e`  
		Last Modified: Fri, 12 Mar 2021 10:21:42 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655c2ad489bafc361b1d87d63b208126a0db4cffb0d5212f1edc9997303da9ce`  
		Last Modified: Fri, 12 Mar 2021 10:23:49 GMT  
		Size: 304.1 MB (304067299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
