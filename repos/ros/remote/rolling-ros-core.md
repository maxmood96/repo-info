## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:b1e8e7cec034dd09b179be382a6b5782aa78f55c207bd1e01fe061f5acfbdfc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:c383f64648dbdac701e1003a66ea110362396d92e4fe609def1d4d23e9e9c6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173792134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69edf43e6e0fff4dab5edcceb27e8e22d9d91e0cb6aeab958c6cfcf0de34b5df`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:19:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:21:02 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:21:02 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Mar 2026 02:21:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:21:02 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:21:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:21:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15463b82d632a1bc8cf0fa79f69d770edd9fcf2c7dc6fd90ff2bd17e055841a`  
		Last Modified: Tue, 17 Mar 2026 02:21:31 GMT  
		Size: 683.9 KB (683904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f8b81a23f03cb1f80996b1b31fd2dba3346f972b473e53a0e3698bbc5b0d03`  
		Last Modified: Tue, 17 Mar 2026 02:21:31 GMT  
		Size: 6.8 MB (6751746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe925611e40b8d95c593caef9f6ece9b81c61828373e4ac5694187a041abdb94`  
		Last Modified: Tue, 17 Mar 2026 02:21:30 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09240c2cd96a025739e67f40f2364f9385438562acbbdac5739bde6fe42e309a`  
		Last Modified: Tue, 17 Mar 2026 02:21:34 GMT  
		Size: 136.5 MB (136530193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f17b80019f4c578c4719a33fed7d89543c542dc0af18e9dbd35bd0f12926540`  
		Last Modified: Tue, 17 Mar 2026 02:21:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:5342dea70b71b20a33ba0edc2d9c5b4005570bda6808c462e7016ea89ea426c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19431994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d7256ba5081776b9a2943da90c29ca971962c8796832e3f094d12cffa37f80`

```dockerfile
```

-	Layers:
	-	`sha256:2668f1a3b46013ba0c9fa9432a15e712db3a9520d3666ac68fe68a189d49d3e3`  
		Last Modified: Tue, 17 Mar 2026 02:21:31 GMT  
		Size: 19.4 MB (19417372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d17af51955f4bda4f92e3e0fec6e7d6d38bb9d5cf7234718b3b3fdf1f07dba`  
		Last Modified: Tue, 17 Mar 2026 02:21:30 GMT  
		Size: 14.6 KB (14622 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a8e018a7e06260f245f22aec9d55d5c49a8106d39651293b97287bbec47fab44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167376535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d621d83bb7081037ad550e318741601de7214d820a82fa297e5aa5ca7292214`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:25:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:26:48 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:26:48 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:26:48 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Mar 2026 02:26:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:26:48 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:26:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:26:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656ce31aeaa29ac4e6452e3da1b22f70b50bef7b8fb4360d957c378666e3a1ea`  
		Last Modified: Tue, 17 Mar 2026 02:27:21 GMT  
		Size: 684.0 KB (684045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240ec1232177be2455f9a0dc247b5543e0b1a1197eeb970ad1ad08a3ceca3419`  
		Last Modified: Tue, 17 Mar 2026 02:27:21 GMT  
		Size: 6.8 MB (6764923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517ea7c6da9dda5a9d9bd7a79a74e38c3a3db8ed248109a7be2337d8aa0e0300`  
		Last Modified: Tue, 17 Mar 2026 02:27:21 GMT  
		Size: 94.2 KB (94239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465c0a6393d917b703e9eaadd7cecb66acc38ea8629230531e47694ef6af4f37`  
		Last Modified: Tue, 17 Mar 2026 02:27:25 GMT  
		Size: 131.0 MB (130963424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed02cf0331f23f1c9a6b54ba39118f8e8d77a71a77e5e9b735f5d44bd01e28b`  
		Last Modified: Tue, 17 Mar 2026 02:27:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:86759c8f002027b47d6986dafcb9fb7ae0b9f163fb08790937cce262b7fd4896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19406328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b349b47c175b53c136ec18e6ce4fa2927086d720f7e1b53de4de6295d72404a7`

```dockerfile
```

-	Layers:
	-	`sha256:e7cc09dec0d91b6505ca752c9c81434c9b093fdda14f0cbeea38818d47a3b849`  
		Last Modified: Tue, 17 Mar 2026 02:27:22 GMT  
		Size: 19.4 MB (19391581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cd67238c8d14a44be21455eff8f7ce69131b87b7407ed23209efa000511cd94`  
		Last Modified: Tue, 17 Mar 2026 02:27:21 GMT  
		Size: 14.7 KB (14747 bytes)  
		MIME: application/vnd.in-toto+json
