## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:6dd33cde266a512e91cec291e03e55bf85cd3a0d2df163abd79a1331c2f741a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:66de3f92af7e95fcfac129e90bc5cb1da1f421cb2c78612a3ee1542e9f325fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310400054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677bde48799b4aaefce220d8b3d1fcf2284d96e88f04456c6b0594cacfda0c18`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a37d70e90a7d664105dea1987b320d87a2f03f888a701e8c119b5ff2f38763e`  
		Last Modified: Mon, 01 Sep 2025 23:41:21 GMT  
		Size: 683.9 KB (683852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683da3131eb22696ee1fafcb5f2eaf8378dc9d26956bce0f0444b6da44efebe4`  
		Last Modified: Tue, 02 Sep 2025 00:13:59 GMT  
		Size: 6.7 MB (6746730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd06cb60726529ab14c33cd0e549e60ff60afd5cbfb5e3c025eddb450bc7a8d1`  
		Last Modified: Mon, 01 Sep 2025 23:41:20 GMT  
		Size: 94.1 KB (94066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8007cbb38796d10e52a782b6ca676f15631b28b4af68e7bd4feae2f16fa8b58c`  
		Last Modified: Tue, 02 Sep 2025 00:14:08 GMT  
		Size: 134.6 MB (134573911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a886e9df23356de168fcfac31a587b1c0a6e9e6f85e9348f2f06959e818123`  
		Last Modified: Mon, 01 Sep 2025 23:41:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890398f342aa88c778c4f5ec79b47e448e4be344d76bfe12abcb5525c8dceb2a`  
		Last Modified: Tue, 02 Sep 2025 01:12:19 GMT  
		Size: 110.2 MB (110184026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a000dae7914aa2f9240b525d7ace99c6aeb786ed92d156beaa2e7db638db61`  
		Last Modified: Tue, 02 Sep 2025 00:49:53 GMT  
		Size: 353.1 KB (353120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54fcea91659938ec9ac4eaba7bed60e4ea22031e9869f9441a2d988b9f167e`  
		Last Modified: Tue, 02 Sep 2025 00:49:52 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4f25e282b9e272bff5eb5fad06859e7ea0a1568ef3b4e8a7a21007e3055071`  
		Last Modified: Tue, 02 Sep 2025 01:12:12 GMT  
		Size: 28.0 MB (28038618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:bdde48fcba1de559a19420e232f9ac7c10fc1a5cea882cb0653a1645d6713166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24534893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b590eceb7c41e911fe0f29f1a731bc736b661d53fc1a696a3d0c49ea4cdf7b3`

```dockerfile
```

-	Layers:
	-	`sha256:dee4d445b04a216b5463f19c9304f051dad012ed4cc9112430267cf11384e360`  
		Last Modified: Tue, 02 Sep 2025 04:18:13 GMT  
		Size: 24.5 MB (24518486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faed8d5fbfeddf67ce010f205687d8c782ca6198a96fd8ebbdee3c280d7cd4c1`  
		Last Modified: Tue, 02 Sep 2025 04:18:14 GMT  
		Size: 16.4 KB (16407 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3cdb3b47f150d2efe2b3df4388fd8bb69b2eefd4701edd48f3e7a2a4c87adaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298763393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97dd025cc9218f0b003a62b1068b43b2275120444918d46af3180bcd93bd5657`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a1aeeb021ff56f6549713871ea035936891c67787fb388f08e69e57ccaa5f2`  
		Last Modified: Tue, 02 Sep 2025 02:55:39 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ffa2a8671f1746a19c7af89127b62a1f22836df01caa93a61d61b0d2574661`  
		Last Modified: Tue, 02 Sep 2025 02:55:39 GMT  
		Size: 6.8 MB (6759788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290a01a08d6a7cb15e63953b7781299b8e80e32583b1030aa55d13094df1d2d7`  
		Last Modified: Tue, 02 Sep 2025 02:55:38 GMT  
		Size: 94.2 KB (94161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87da0cff68a8427331fbfc105444a2e3a301c84d89d6502ffcc7d286d9ca936b`  
		Last Modified: Tue, 02 Sep 2025 03:24:20 GMT  
		Size: 129.3 MB (129296622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cefd946668c189566a6003b610072156abfde5c7d1e40317d71a12b10e18967`  
		Last Modified: Tue, 02 Sep 2025 02:57:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f608379c04dd18338fd5de33da4f28ebeeff6fcdaf46dda6b373574a988f10`  
		Last Modified: Tue, 02 Sep 2025 05:42:04 GMT  
		Size: 105.6 MB (105593088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98a9941ab91082ddeb82f35bdf997faf5f763710817de6692aa301d3ff8a8f9`  
		Last Modified: Tue, 02 Sep 2025 05:41:53 GMT  
		Size: 353.1 KB (353122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a97c4b2e3063f919b0777c135cbd16ad3cc438c95c13ac286a95c8a645b6d59`  
		Last Modified: Tue, 02 Sep 2025 05:41:53 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7240163a446ca92d4d3c0e12f6597f79838a505a2dbd30bd5bd9720ae9a1b78`  
		Last Modified: Tue, 02 Sep 2025 05:41:55 GMT  
		Size: 27.1 MB (27119796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:2d3435ef07b4e9bc5fd506ec9a9d1bb2a3426435041fefb44f5998d2300798ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24557291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdb2b8e155064460d77a691f04831758db4b0c462307b122d4fffd403d0c178`

```dockerfile
```

-	Layers:
	-	`sha256:0a673fcb1307f1826a3077ecf65d10362d98bd5461bcb719334af1374d286d0f`  
		Last Modified: Tue, 02 Sep 2025 07:18:10 GMT  
		Size: 24.5 MB (24540746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42c38767ecc3afae7164515a729e7e9188a8f67f1d471251b41458e2228b56d1`  
		Last Modified: Tue, 02 Sep 2025 07:18:11 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json
