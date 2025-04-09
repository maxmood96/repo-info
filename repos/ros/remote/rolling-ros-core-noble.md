## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:f2b4765659d16dd4f1f6b393dd83dae59fead9170d040fc1cf9decafac98cbd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:f189a8beab995fe6d4089037e6271b18a135f54e4c5419094ea5521654eedbf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156761814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4812ff35af762386f778c6dbac497fcb7e5e5e37f4867538d3bc93ba91e3742d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b9da1b5048f08150019e977d6e262db7577c0ddca858e147df7d9bf93f79da`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 683.6 KB (683556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05e54389289d908213d0e62f13c72b2001cc525190c511ba09dfad5c8b084fb`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 3.6 MB (3563161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f5382010868ddf658e88e6bffad5d0ce76a6a6a6b354b9cce80c97e508cb63`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01b64bc19922e1f6345f2b4e899c22ff3b9b37a905b50f5c6e0784ada292f34`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fee44a6aadcf0d84954979ffc4c8878dd6ea0ef9a78cb99a31bced6981ef5ed`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 122.8 MB (122794979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48198ad8c8df02f87473863271fe668e6d78defe02d55c43b7168acc66a4ecc2`  
		Last Modified: Wed, 09 Apr 2025 01:20:47 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:1b5482fe1e1507f49fe013bec9a5b1996e805753c0deb290c5c9939b8ce83695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17796623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727b0b800c933cc35c5239b6571e84eeadf2b87fb6a29d9d26655a2a6f8c8eea`

```dockerfile
```

-	Layers:
	-	`sha256:d41a9071eb7d8ecac362ae42915cdc2eaff4c34da8c42cd96c9125a509167f4e`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 17.8 MB (17780229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:245f7e10fcd0db42ea9e7f2ef2b0a51d1d3dbb59a050fee13607d17031cd83a8`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:039b42fb976a37a22f30d3bfc94c097eadf24c3bb2eee27c65e12891434e2c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150733271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0f09b2208f9cde4993678acbeb8729636c3665064cb42ba6e04fd9c6eda3a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46007cb290c9c61d3be471686a736ee17b9fac514d4a3ee75010c0ff00e86e0a`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 683.7 KB (683730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c743169635f1311f3b83c0db23367bb49da554ccc36aed60f0560db69fb31c`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 3.6 MB (3561575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d49b1f526488311879e130a8efc035c71e0bfc7b62c561004139c1a01340b1`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bdb94284e8bd83926f228dee3a3d21bee9da2bbbed34c32bd397c9fa0b5d90`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a60662d472c0013b6b8d0ea8420230ca63c5a5cc05908698fa85ce4d690d0c`  
		Last Modified: Wed, 09 Apr 2025 09:16:43 GMT  
		Size: 117.6 MB (117638537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c91896a405184701e3d8a7ccd13bb50b4678fd39d67f09c91da7542824b3c9`  
		Last Modified: Wed, 09 Apr 2025 09:16:39 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:06ba545c0b8c795b2a0ec3fecbe6b769cf1d5b4c8e73b90d605a448ef378f632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17770769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b543a87320a7b02c76e6f3c2fa8cdf0b359904c9187b660cded059bf5c37f845`

```dockerfile
```

-	Layers:
	-	`sha256:3a1208b322e6587034825646df2cdf09a099cefcb877bc438a58fa52e688fcf8`  
		Last Modified: Wed, 09 Apr 2025 09:16:39 GMT  
		Size: 17.8 MB (17754235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81c1de3b281c6ace12bb55b923a352190f112efc43cfe5dfb03b24d1b54373a2`  
		Last Modified: Wed, 09 Apr 2025 09:16:39 GMT  
		Size: 16.5 KB (16534 bytes)  
		MIME: application/vnd.in-toto+json
