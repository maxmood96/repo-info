## `gazebo:libgazebo11`

```console
$ docker pull gazebo@sha256:117ab8e5dde919d31c5bb5de75b4cc62db511e9156aff393dd142439c4121ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo11` - linux; amd64

```console
$ docker pull gazebo@sha256:67fb9ba8c009e87b1e55ff5342adbdd35dc1e2a1195d38b7e99a553a8f75b619
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.5 MB (610509134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27a5b21f5f10ee7b6559a5154b798a75d8edaaa434887c230a445ca893bd826`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:15:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:15:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:15:55 GMT
RUN set -eux; 	key='D2486D2DD83DB69272AFE98867170598AF249743'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /usr/share/keyrings; 	gpg --batch --export "$key" > /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 02:15:56 GMT
RUN . /etc/os-release     && echo "deb [ signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg ] http://packages.osrfoundation.org/gazebo/$ID-stable $VERSION_CODENAME main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 02 May 2024 02:18:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.14.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:18:54 GMT
EXPOSE 11345
# Thu, 02 May 2024 02:18:54 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 02 May 2024 02:18:54 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 02 May 2024 02:18:54 GMT
CMD ["gzserver"]
# Thu, 02 May 2024 02:23:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.14.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9f83335e3f34356129a65a46777f2c11b35558325643aeceb57ad34fcf26ae`  
		Last Modified: Thu, 02 May 2024 02:23:52 GMT  
		Size: 1.2 MB (1198590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9931bbbdc456888cafcfb45518f1f74377f7ded26c5caeba3779574b953c2f0`  
		Last Modified: Thu, 02 May 2024 02:23:51 GMT  
		Size: 5.6 MB (5553874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445ed4a941f51d554841f70799314b4ac5d5dc064767b75b05df1d86c17787e1`  
		Last Modified: Thu, 02 May 2024 02:23:49 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513072e5b65273f384bd838a524ca9d462f83e889c44385461419341a0ddb9a1`  
		Last Modified: Thu, 02 May 2024 02:23:49 GMT  
		Size: 289.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5747ed01a1195fcefb488c84b9f842bceedc716074f91ec8b3e5b3f85269d6`  
		Last Modified: Thu, 02 May 2024 02:24:20 GMT  
		Size: 278.1 MB (278056911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd608ca03f87defa0cc9c23a8bf9b75741e7287283a9e921305de20b1905d4eb`  
		Last Modified: Thu, 02 May 2024 02:23:49 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e64479743d6a37e4b5d8419494e9893d010542145161e62dc143ea5f9080f9f`  
		Last Modified: Thu, 02 May 2024 02:25:16 GMT  
		Size: 297.1 MB (297113509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
