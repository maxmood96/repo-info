## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:2725f05f3dcb0be4d7e0e5de8e5fd8543594e4ad955b1db08403f48662357d95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:1572554627d941b95dce4ffc8303a358bb9c3dd5102bf31db492a4d611154125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1079731337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901365dedcf2223e1f2b3cfab10464a3a401e424b72ab7d2c3a63d30043900dc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304b0a16a8c4686c1ae17356937b1b3bdaf0753b3311050abeb20562d0b3ec6`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 679.7 KB (679671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb30b279e5182888c1ce5be1be8b6ef62da8c7af113d92327c1b685afb4e2bc`  
		Last Modified: Tue, 04 Feb 2025 04:48:04 GMT  
		Size: 3.6 MB (3560942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac7cc1887f83d20d948f86dead37ce8706504781f9cfa1e2912f3db6419e7a7`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c4b7644d00b5e8121cbac43707d89d79b1578e713231dfe85d556a5c1b2e57`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb7850fddc977116096c2669bcd969bb3ddbc023b18e0828e31b7e1170b7ce6`  
		Last Modified: Tue, 04 Feb 2025 04:48:12 GMT  
		Size: 123.7 MB (123694054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb43dbf2da736a743b2be0e44c373dd969448b32853643bd272d4567cc9ebb7`  
		Last Modified: Tue, 04 Feb 2025 04:48:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f799811f78900d918566ae506e59f609131fc9aa2aadc0a20363c8431be72735`  
		Last Modified: Tue, 04 Feb 2025 05:27:05 GMT  
		Size: 112.5 MB (112548960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790abc014da9d08e679732b7bf93439b6e1c80b04e9389763566899abffe958f`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 348.3 KB (348305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17046dc54a215d05863c5f4578045d09e9165e2191a2689eaec75723fb8cb07a`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd799659eddfe3d7cb6e5fbf2cc059a3222acba665831b5b363d072093b4719`  
		Last Modified: Tue, 04 Feb 2025 05:27:04 GMT  
		Size: 28.0 MB (27963262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544ba78693a91ef0030d341fc55c6be950f1c82fbb25a3c279cf4f6120b4206f`  
		Last Modified: Tue, 04 Feb 2025 06:18:14 GMT  
		Size: 781.2 MB (781176958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:722788fbe3c9791c5e70652bf2defbc1c5ce352150987f8f8d2fc723e0a1b758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59572652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a59ee6e9738718605654bb9261f2e8c75f1deda0dcb0120437277756cf126a`

```dockerfile
```

-	Layers:
	-	`sha256:c21aad716a39812b49f3433961b0a6beec8f8de5ef19ad8cd10f24d840ac6c75`  
		Last Modified: Tue, 04 Feb 2025 06:18:03 GMT  
		Size: 59.6 MB (59562964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c834a428b6de21d4fe30efbb5e78642b82984cbe4afd27a86c5bc8f121c23ffd`  
		Last Modified: Tue, 04 Feb 2025 06:18:02 GMT  
		Size: 9.7 KB (9688 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:60ab3cec0a6e402ea164a516ca8f6cb6317e46306341a1154b5d4065e5629856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **974.9 MB (974946497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80815082200beedaea9dd164decf69becb82f386c98910fe3612312ec5a0a60`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828cafb5606bfc377030b11684ade4e9ef094c5c8866214772783aeefc65dd3e`  
		Last Modified: Tue, 03 Dec 2024 10:21:26 GMT  
		Size: 684.2 KB (684168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c673bfa5b508b4c5473b5d450e971cdb23a088fdd04c3bc04bc7016a57396a`  
		Last Modified: Tue, 03 Dec 2024 10:21:26 GMT  
		Size: 3.6 MB (3559491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75b4ec669cbefd2d68a727cdba4a382b80cd85f1930c4c17ea0f72808c33af2`  
		Last Modified: Tue, 03 Dec 2024 10:21:25 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb025d30ba4de809090f9a665f12e338cb143fc5b85c065932d10e06f6d155a`  
		Last Modified: Tue, 03 Dec 2024 10:21:26 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b494426cf0020c43838c91deb89a9ce6da60bcac380a766a5a3103053fc4a0de`  
		Last Modified: Tue, 03 Dec 2024 10:21:30 GMT  
		Size: 117.5 MB (117505391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c8974010aba9f0fb6ac664cee0cae14553b8820fc0de89028fb2488ebf0691`  
		Last Modified: Tue, 03 Dec 2024 10:21:27 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2b101ee11fe97dea9fb6db087d7e03417e50d6c827fa3b0081c59a7bfa4f9e`  
		Last Modified: Tue, 03 Dec 2024 14:37:53 GMT  
		Size: 111.0 MB (111007739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3cf1612d9d1fb2cd20d97d63dbb42923046c3bb1f7696caaff67cbcf8fc278`  
		Last Modified: Tue, 03 Dec 2024 14:37:50 GMT  
		Size: 342.4 KB (342353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6222ec72157e7abcd4ed22919ea0768fce7e1a2eacd878c2be5ba94c39cbc4`  
		Last Modified: Tue, 03 Dec 2024 14:37:50 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4564659199e87c69ffefaf3d047ec489aa6c03024ac1c21c3af3d9d92978bb1`  
		Last Modified: Tue, 03 Dec 2024 14:37:51 GMT  
		Size: 26.7 MB (26681514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e59b3175daf1deefffc486919f38b1beb07ca5423ae7060b77a76b743b5cb7`  
		Last Modified: Tue, 03 Dec 2024 17:33:54 GMT  
		Size: 686.3 MB (686268239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:38549375d57cce7193d1af5695b5cc258a0f8cace9a8422ceec8b93baa8ef19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59637414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a778389042bf0b03835f182cf1daa4bd6b086ac203d3ce327aad6d6e1af9a563`

```dockerfile
```

-	Layers:
	-	`sha256:5dd951732a50d4fd8c0545c0a5e25217a1592065ba21c5613a335d1da0848826`  
		Last Modified: Tue, 03 Dec 2024 17:33:39 GMT  
		Size: 59.6 MB (59627646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00965e6ee42767f47226885fc15c63bd6409b9685ab7ea40f6b37a2fcb866799`  
		Last Modified: Tue, 03 Dec 2024 17:33:37 GMT  
		Size: 9.8 KB (9768 bytes)  
		MIME: application/vnd.in-toto+json
