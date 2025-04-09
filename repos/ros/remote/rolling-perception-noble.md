## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:b8b6d94c9005333974fc990e18fdb81f8df7f62f307d1e5c01ea20cf203c913b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:356929b6d36543977d1339667e0d85478b4ec7bfd26bf4c4147366c5e68517be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.5 MB (661475842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49319845efbee64b4bfe8730cc4ec94c16117ed90721e658d2e1bc99bfc3dfa2`
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
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:fa100ae83b33f4a00647f4b3dc436a7eed071ab68f18a6142f712d0c9494f234`  
		Last Modified: Wed, 09 Apr 2025 02:48:53 GMT  
		Size: 110.2 MB (110171845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666490107601b7f396f20994e344057fd40294b1dd92231b664ee7c1891c960`  
		Last Modified: Wed, 09 Apr 2025 02:48:49 GMT  
		Size: 338.1 KB (338060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785cc6e2f10ee0b8f089cc0aa88c5953ea75ba381b07211777ce66d9dd2231ed`  
		Last Modified: Wed, 09 Apr 2025 02:48:49 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc80d84363dd2e6e993857b7b92a78ab887b160a51889507644e5631a9ae4d90`  
		Last Modified: Wed, 09 Apr 2025 02:48:50 GMT  
		Size: 28.0 MB (27971330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd86e13bdf954f20585bde2ebc36397f6ed75124ad70f65a8f0c5354df402b4`  
		Last Modified: Wed, 09 Apr 2025 03:13:11 GMT  
		Size: 366.2 MB (366230339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:6a977f3fc06ed4d524f31fbddd6484deb1c23873d606a320eedcf710c51117ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42151158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642c307e24a559a7393027bdd8b81f52135c1c34470942e93cd9f5364f64a09d`

```dockerfile
```

-	Layers:
	-	`sha256:7422534f18797de1f55698c82e457834537c28ec8c755a28f8f04ef9b39c35a9`  
		Last Modified: Wed, 09 Apr 2025 03:13:05 GMT  
		Size: 42.1 MB (42141448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1c660d473c97b348755a2e4866c34de5605703829aac164ad3af1381ec17604`  
		Last Modified: Wed, 09 Apr 2025 03:13:05 GMT  
		Size: 9.7 KB (9710 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fafd9cd4308ddd79ed1323d1a84dde345bc13106493568791f39659ad307d4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.5 MB (565488023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad78f33d3b7a2811e7a6c33bbc58e8cc2a40931ab86cd56cfe7d65ccbe07868f`
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
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:13f9af466fad2f65e605b90e86db4c3ddcc8167fe2a0eafabfe3be94dfbfaa7f`  
		Last Modified: Wed, 09 Apr 2025 15:54:53 GMT  
		Size: 105.6 MB (105595325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e5c94d4c8356be193c6875cb17e4c4820fcba1569c0569a48c7dbd73b8f9ac`  
		Last Modified: Wed, 09 Apr 2025 15:54:51 GMT  
		Size: 338.1 KB (338058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d33a92e1576144cea07ccfea2ddf7551cef8851883f7b4632198fa3d8db85c`  
		Last Modified: Wed, 09 Apr 2025 15:54:50 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42682e414427c952a849a517769a2a9330a32f2a861c581ed4ef05222f31dc83`  
		Last Modified: Wed, 09 Apr 2025 15:54:52 GMT  
		Size: 27.1 MB (27057105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea356f9edcf6e694ad6624c072d922ab308705826095e2073152e563c3e756b7`  
		Last Modified: Wed, 09 Apr 2025 19:28:06 GMT  
		Size: 281.8 MB (281761831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:0394ccc9635e113138dd46f3439441d672fd431374e406123fdfff42e52fd601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42111567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c571ff87d50a98aa5a84b07c72993fd9bf6075faed443c5893da5f2f707f89e`

```dockerfile
```

-	Layers:
	-	`sha256:f75eae50ba65e3fee2a30d0d36545d04cd147aca05c2ea45a4b10672a54a5ed5`  
		Last Modified: Wed, 09 Apr 2025 19:27:59 GMT  
		Size: 42.1 MB (42101778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edfc2de666dca547c880347d0fd5f43515e024765480c7fe9aee909b3d01a039`  
		Last Modified: Wed, 09 Apr 2025 19:27:58 GMT  
		Size: 9.8 KB (9789 bytes)  
		MIME: application/vnd.in-toto+json
