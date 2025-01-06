## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:857a29a6a58d83368da88ce938b033c593c66aa36e53ce83194bad62cbf64f5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:dd9aa8a30580ae18bc7fe5130c112d7f14a396c267f94f4e63067759a9fe743e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1036859926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684a77547bf02d57dfb990db1eb50bf05a8ec8dff7cb0b40456184813ab319f1`
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
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
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
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb9b5148ae557dba975bb84acfb09e3d5ecb3b30a6664c1b158038437ff864`  
		Last Modified: Tue, 03 Dec 2024 02:17:23 GMT  
		Size: 684.0 KB (684039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec79256506a8ed2c76d26fb5263d09a717a558dbad31f97bc79a412b71bc3d5`  
		Last Modified: Tue, 03 Dec 2024 02:17:23 GMT  
		Size: 3.6 MB (3560620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa924df05280940cb19b9e74ac5885a2f67622eab697a7433b583a120694239`  
		Last Modified: Tue, 03 Dec 2024 02:17:23 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98f3e08353bf8f53937fa7168cbad7d39df3214474bc9b07557880d6ff63b08`  
		Last Modified: Tue, 03 Dec 2024 02:17:23 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c01218c18dd3d57f0fd398836513b6b50fbe554ff4b460941357ebfb7289972`  
		Size: 122.7 MB (122691998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a4d000285c3d2a81b20a96c50372bd1cde9b88f7611ccaa417fea7a3c85459`  
		Last Modified: Tue, 03 Dec 2024 02:17:24 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17292e7638873b8383a8077c14d0b55cd66f74bc5428ac9cbfb5d353da8c8423`  
		Last Modified: Tue, 03 Dec 2024 03:25:07 GMT  
		Size: 114.1 MB (114147298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d15681af803fdb5522376544c8684b41f96b7302f381c439f144544ecee9777`  
		Size: 342.4 KB (342357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28e771bfd74e3604730bf79016216276d7f5a0ffa622e23f687b33b7f0baacc`  
		Last Modified: Tue, 03 Dec 2024 03:25:06 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401ff9aff2459f1c5d9ec5957ad0af8f8e54696b7d93bda3cdae79703db2adc5`  
		Last Modified: Tue, 03 Dec 2024 03:25:06 GMT  
		Size: 27.5 MB (27530745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3afa5dbc2b085fe55b153f9297601b3ed264ab949e6ea652a2ccdc92bf548`  
		Last Modified: Tue, 03 Dec 2024 04:35:36 GMT  
		Size: 738.1 MB (738146016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:2c6b6e47d90a19f47ac25ef635505c01992e8d334e82f6ebe0c8fb096b72b827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59646540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8014053ddfcadb0cdf53481241b72c66edcf62eac12f7e8945fc7464c7c1da`

```dockerfile
```

-	Layers:
	-	`sha256:5a5e4c78f159b0468bcec82e8c3034a485a0b90e77cd6b7690bd86f79265dfb0`  
		Last Modified: Tue, 03 Dec 2024 04:35:26 GMT  
		Size: 59.6 MB (59636853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3930749044ec8d702df96329c2e5639642de11118e33736b69fba4b12655a2fc`  
		Last Modified: Tue, 03 Dec 2024 04:35:25 GMT  
		Size: 9.7 KB (9687 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

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

### `ros:jazzy-perception-noble` - unknown; unknown

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
