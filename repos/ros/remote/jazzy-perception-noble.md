## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:8fca844ef649359c9e26795380f8084222f463467658aa03cd9f3801c7b64c27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

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

### `ros:jazzy-perception-noble` - unknown; unknown

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

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c3bd1a67280a5daf89a7800d9823e574b93b4c824ff6fe35af185677f9b9a994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **977.4 MB (977422326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5342fb846691467c02d438192cdee325edccc145312d00ad18c33a9c1eb690`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63319eccea3c72ab6d7d949469263856d4536e9cd706ea95737df417a0844d47`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 679.9 KB (679880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6398c28a986a6ad00e38d58018c1164a49f100005ed75bf86b35f690f439ea7e`  
		Last Modified: Tue, 04 Feb 2025 14:49:54 GMT  
		Size: 3.6 MB (3559788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df9da01336e4108fa26e6b36a069895325f27ba04a1fec9c91ff35c84097ae`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f58c34793503cf5ba16f4d4fc8ce2e5b169468c3ab1534db58be9aef1c8cfd`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f850ce01846867a763779ca58d7bcd68a406bcc06d83d5f336df9f1af04d89b`  
		Last Modified: Tue, 04 Feb 2025 14:49:58 GMT  
		Size: 117.6 MB (117595132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc74950aa3433684e07f35a319dae2d5b2c9194e38d014e3888c3c2c24bec843`  
		Last Modified: Tue, 04 Feb 2025 14:49:54 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b1b23617d0853ed5a82180013d21d276e99021dd317a022ba92434e181df22`  
		Last Modified: Tue, 04 Feb 2025 22:04:56 GMT  
		Size: 107.9 MB (107945853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea83452a074608a4c581e2d883714478c1bd0639a3c85b8b69e1d061f1d59baa`  
		Last Modified: Tue, 04 Feb 2025 22:04:53 GMT  
		Size: 349.1 KB (349149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7cf2b9d680488073e25fd14f7cc38713758bbf5c42e19eba260082becdef26`  
		Last Modified: Tue, 04 Feb 2025 22:04:53 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0ff6b4898d5f98f2fded332804af4b40d7b47c66907a152822cb5e2fd0db20`  
		Last Modified: Tue, 04 Feb 2025 22:04:54 GMT  
		Size: 27.1 MB (27055422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b0be361a73f37b76ff368119b44430ced2a6e53c5f223b293c9e58ca559e12`  
		Last Modified: Wed, 05 Feb 2025 03:54:51 GMT  
		Size: 691.3 MB (691338596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:90414b8d1a2fb77fa6d0c72f7d1a92478f21589e083e27f63fc630540547b77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59526735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b927f67b1b937a61bd21df1b0aa4f1bdc3a1b1431d10e3ae4efb21da42180625`

```dockerfile
```

-	Layers:
	-	`sha256:b32120b9351bdc8d942d72598151a4803098c15687909ebb8eead540f5b32089`  
		Last Modified: Wed, 05 Feb 2025 03:54:40 GMT  
		Size: 59.5 MB (59516968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b03ed190939014db04247f278a6ff24822dcab334853d5c73f2cdf882a9266`  
		Last Modified: Wed, 05 Feb 2025 03:54:38 GMT  
		Size: 9.8 KB (9767 bytes)  
		MIME: application/vnd.in-toto+json
