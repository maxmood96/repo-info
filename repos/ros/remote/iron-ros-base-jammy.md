## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:97579ce6c48f11753f783ad71ff4d4f2888fb66c879bc1ea78ff04914f9840e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:3b35abb12383053d56d083c71a79a00008591aba52e3244f07ac48c5b9c5bb3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268962226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b8b248050243f7430ea86fe37ebb761450a9a8e3f84d781ea05ef08c76411b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:42:07 GMT
ENV ROS_DISTRO=iron
# Fri, 16 Feb 2024 02:42:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:43:01 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:43:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:43:01 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 02:43:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:43:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 02:43:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 02:43:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64116f613b23c02909000a42e67e9be2cd684886af17a609ab67bc5d1a8190b8`  
		Last Modified: Fri, 16 Feb 2024 02:52:48 GMT  
		Size: 124.3 MB (124264870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943b642bdfd3e9e1483069ffba4a7090e364f2d29606904fbb9a26d3925c2964`  
		Last Modified: Fri, 16 Feb 2024 02:52:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177e592df8efe0984926f743e834f7746effd90d514f3d3851abe3044c8a61c0`  
		Last Modified: Fri, 16 Feb 2024 02:53:07 GMT  
		Size: 85.2 MB (85170370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82907e5ee200d3fc665288fc89fc9cf64841db34917726251c720cd2178de28`  
		Last Modified: Fri, 16 Feb 2024 02:52:57 GMT  
		Size: 295.4 KB (295426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62501b0855f8ce6c24c8e4011b811b0a788aa94b6bf9a2a64c672fb2dee59828`  
		Last Modified: Fri, 16 Feb 2024 02:52:57 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6846f1670ef3d1bc2c2f4ac35db04c584f6230744c631aac1531732b9eb6b3`  
		Last Modified: Fri, 16 Feb 2024 02:53:01 GMT  
		Size: 23.7 MB (23731179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3bf0a98ec473072e37b88cb0cb856d4c83293c7f253b226e42321db8268d08ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261373157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eaf42cc0adadf5631a4e94d35ec33bb98350af8e126a592d69f658c9bce30a0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:52:09 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:52:16 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:52:17 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:52:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Feb 2024 02:52:17 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:52:17 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 03:04:26 GMT
ENV ROS_DISTRO=iron
# Fri, 02 Feb 2024 03:05:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 03:05:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Feb 2024 03:05:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 03:05:19 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 03:05:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 03:05:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 03:05:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Feb 2024 03:06:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5992f730822fa824cbf7d3f44bbe42d9e0a430ee802ff3b881740b95fe753e`  
		Last Modified: Fri, 02 Feb 2024 03:14:29 GMT  
		Size: 1.2 MB (1216340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74aa8ec77518d8d3ea5f4a848375f3a742074922bc1107a763144500d58322d2`  
		Last Modified: Fri, 02 Feb 2024 03:14:27 GMT  
		Size: 3.8 MB (3800535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1be5561e0e858afd3baefdb8b8ae673b68af4125f6bf3c705d953f6e46b12ac`  
		Last Modified: Fri, 02 Feb 2024 03:14:26 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944f99a3fc10280d08753ebc4cf1abcaa38717a8225d899c28c136c8b0cce61e`  
		Last Modified: Fri, 02 Feb 2024 03:14:26 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715c4189808204d3729098a02f763d793d5af5b6b3f46b7b186b0e4c085bef6c`  
		Last Modified: Fri, 02 Feb 2024 03:17:24 GMT  
		Size: 121.7 MB (121675421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fa51c266356fb6ed44ee3d5d00b59bc8730835aa9d882e2392db2cbd4e3885`  
		Last Modified: Fri, 02 Feb 2024 03:17:04 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c96e5a6ff70282af7861ace64b36c3908f601b86ede40e2af151e74fd427de4`  
		Last Modified: Fri, 02 Feb 2024 03:17:42 GMT  
		Size: 82.8 MB (82844022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc517bd6dbf86a55ad10bdfc76d9859f17ae5dd338937bcc89a21e49c1a5fdd`  
		Last Modified: Fri, 02 Feb 2024 03:17:33 GMT  
		Size: 311.8 KB (311835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d1b97b220686d3e3741018a1ae5870c77f4034fc0397568b25b4320f9858a6`  
		Last Modified: Fri, 02 Feb 2024 03:17:33 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52f37361bf94be965d42f0c1abdaf07943071e3d188c85265199b458779d3a1`  
		Last Modified: Fri, 02 Feb 2024 03:17:37 GMT  
		Size: 23.1 MB (23119927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
