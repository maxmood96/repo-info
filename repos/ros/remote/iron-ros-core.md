## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:0bb3828a3573b261ee6b1cf3f11cc0200949f6c31fbfe861110ffa19074f87db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:70d5036081281c33d01b7a397d706c4b22c46ec7359659271ecb59469f24dc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158741608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cfc4cc1935f650cf5db05be31aeb394e8b0d15f829755db45adc5e293bf52a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 09 Mar 2025 12:07:58 GMT
ARG RELEASE
# Sun, 09 Mar 2025 12:07:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 09 Mar 2025 12:07:58 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["/bin/bash"]
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LANG=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LC_ALL=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV ROS_DISTRO=iron
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7846943e3d9298fdd9fe26a42e42bf98bc05af7261e8bd2b1733e389edfe59e`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 1.2 MB (1213915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2aa8586cf11825d7e10ae4444ca3b83648ae7dad28324ce38ae538e6180acb5`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 3.6 MB (3625561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f1565c7e7e6ff4f87e7d2b009d611e56267bddf3c32d322fe724e0916272e9`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bad7354d3b595af2bed14f27f06908e2caf0eac957613e4b27ef1509f3ee10`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161e718750b0e9b02bd3475720412d93698bee5511db8ddae1cd3d9bf39339b3`  
		Last Modified: Wed, 09 Apr 2025 01:20:53 GMT  
		Size: 124.4 MB (124365656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36620f46180918624c7173c874dcab6859508f3d0078919cf838dfe86210069f`  
		Last Modified: Wed, 09 Apr 2025 01:20:50 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:2f7300f6a28bfafc568dc6d4f92e704241cf6bb3dc9f8ef14f7cd7a8d839c8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19242256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccb440c2f41b957fb6f869ec764c58c788fca64854ff84da0fdc34e232a3932`

```dockerfile
```

-	Layers:
	-	`sha256:8512acde24b888671239fd31dbe59d9654128f22ea970edf0167c2be6b521c29`  
		Last Modified: Wed, 09 Apr 2025 01:20:50 GMT  
		Size: 19.2 MB (19225851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7e671102472b9cf10097bf426a18c9c5771e38544b7bd98f02c5a6b98c2c0c9`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 16.4 KB (16405 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:395e82bac03665e95ce2fc4e0fbdd7309d934c49a6b32df758be968b27d12311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160174087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baaa32b146bf75ca5682fffccc3e4c942bcb4b6e33951eb9d5a2b503e25f5e08`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LANG=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LC_ALL=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV ROS_DISTRO=iron
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1926f36c9b7b151d496c801225ee7599eb5a8b9b724136c3f5e16b117476669d`  
		Last Modified: Mon, 10 Mar 2025 18:23:24 GMT  
		Size: 1.2 MB (1208081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d6a4a0853d9c07e7a7b7e748902799150df963c6d6c838f9689a1221332395`  
		Last Modified: Mon, 10 Mar 2025 18:23:24 GMT  
		Size: 3.6 MB (3596329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92d7b8158f3e4d0bc00f0b83b4f7652632ca53aa97593b50614e361a8057b00`  
		Last Modified: Mon, 10 Mar 2025 18:23:23 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb95bfa72cbcd78f679175ba71dd1855fc3b7d01686c288428c1ad9a99e928d5`  
		Last Modified: Mon, 10 Mar 2025 18:23:24 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ad630b2a2b3a1b904d5d02d598bffc5bf6b3a0f69e400bc074b2aab1de0843`  
		Last Modified: Mon, 10 Mar 2025 18:23:28 GMT  
		Size: 128.0 MB (128007383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18262b00390f040cf294eaa509d4f779a9ffbf41db0b492fe510f0f29a3f3e4c`  
		Last Modified: Mon, 10 Mar 2025 18:23:25 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:1b1a26de1f9fd0065cb8c9fe0444c34f0af9a2bdadc0629ad8594853432b3330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19233947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666d8589c7edea49e23cd3e3944491b72e377037e97e33cbf546a634471d63d5`

```dockerfile
```

-	Layers:
	-	`sha256:51173e6e9a615c6eec568c02d61d5d82bc81f464c5f841a7be1e214c790e4bd4`  
		Last Modified: Mon, 10 Mar 2025 18:23:25 GMT  
		Size: 19.2 MB (19217402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1898f397cd64e25737f39a5c39bee7febdf3176972f7e11f5c028f72b30077c8`  
		Last Modified: Mon, 10 Mar 2025 18:23:23 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json
