## `ros:humble-perception`

```console
$ docker pull ros@sha256:d6e9743edd6c9326608254ca8352f0ba5e7455b5ef7c731fab6d1417bf56d52d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:9803211d5c18da4662d15dd577fb9fe1d7d90675739d912a2aac8ef0d113e947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.8 MB (961842264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6a041c20890e6afd3f5bad4c59e2ebddf354bd2a90b5e48196039886342a0a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6a79aeb6571349bd0ed39d022974bd75ce6cd8a8fb16abc081979f49eb047c`  
		Last Modified: Mon, 10 Mar 2025 18:13:43 GMT  
		Size: 1.2 MB (1208095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad511e33582dd506cff877292e878fa641e74fc75c6b05d646f02a8591ff6375`  
		Last Modified: Mon, 10 Mar 2025 18:13:44 GMT  
		Size: 3.6 MB (3625056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cae3cbe2ca7852f81be5faded91257ec73279265656d13ab374d2b575abf05`  
		Last Modified: Mon, 10 Mar 2025 18:13:43 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea7840eaa99bd262f11e2fa84632a1f7ba2a6fba94652d5e4272e9a11794793`  
		Last Modified: Mon, 10 Mar 2025 18:13:43 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad57cd4eadaac8aeec4e7509e5fd14d30569d2e25cdba0bb834a763bf11cb3`  
		Last Modified: Mon, 10 Mar 2025 18:13:47 GMT  
		Size: 114.1 MB (114061990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82474f94165ca84f75e2d760c63690d4ca308855187afbce52058b83f50ffa2`  
		Last Modified: Mon, 10 Mar 2025 18:13:44 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089ca1bc1a1b15b540b30569f018bf20eb06e2d53692e9ebeb5d9450ff6ec4f9`  
		Last Modified: Mon, 10 Mar 2025 19:11:41 GMT  
		Size: 98.0 MB (97955411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72787a0c5c86d2f3d46b79cba33f298d9b823560c589f46137ced804446c8605`  
		Last Modified: Mon, 10 Mar 2025 19:11:40 GMT  
		Size: 353.9 KB (353949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83b85f22d836da075cbfedecd3b724760d7d3c69d7a09a90aeb76e9f6bcc2eb`  
		Last Modified: Mon, 10 Mar 2025 19:11:40 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317a32ed63c738b388aa2ea26d69edfa67bf726ca002076f6f3d92dfd889c12a`  
		Last Modified: Mon, 10 Mar 2025 19:11:40 GMT  
		Size: 23.3 MB (23289692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0536bcd16cf9de22f3b7f833be0c1563edfb49da8b025b8d279b9682068ef990`  
		Last Modified: Mon, 10 Mar 2025 20:13:56 GMT  
		Size: 691.8 MB (691807193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:c8b3991c93269a294e97e940a5360e8c53cf66155f380257775b9fd894b57618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57536008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed8574ed6fe42aec8987dab7326b23b4901d42901a2f692630999a2a75bdf66`

```dockerfile
```

-	Layers:
	-	`sha256:b128338e0d659283ddefb4aeb1bdea3ec04b047c07bff2603970f1b84200c181`  
		Last Modified: Mon, 10 Mar 2025 20:13:45 GMT  
		Size: 57.5 MB (57526310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:622bac1d1a879f9375f8a31f65a69c8f655537eee672125e15ba2e2669ab0532`  
		Last Modified: Mon, 10 Mar 2025 20:13:44 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f20ff5afd5447ffedbf85aac8d1e759228160e6dc3e5b463e6d4e7e9597deecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.9 MB (920930825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66015e6af6cb96aa05f610c74b7c52dde9baadd558a846d2bbbf784c0adc8a7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:4aeeed08a57b27403fa9fe9538ce4160740d4ec04e65be4ed90fbb9ac2bb25df`  
		Last Modified: Mon, 10 Mar 2025 18:24:52 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bf01b92f5fca1f33ea542127260bc8758f57c788ac4d6d9346acea13a47675`  
		Last Modified: Mon, 10 Mar 2025 18:24:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a8e209955f92010bb513e324647114f2359e3b4f0c03936550a6734d9f53e4`  
		Last Modified: Mon, 10 Mar 2025 18:24:56 GMT  
		Size: 110.5 MB (110522121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804f4e59511abf9df55102f7c8e0af1ed796adc901b8d302319e1239f269c737`  
		Last Modified: Mon, 10 Mar 2025 18:24:53 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7508b4e2599475e76914a14ddd797e71dda721ec44f4eaab8bce1a7fb39c0419`  
		Last Modified: Mon, 10 Mar 2025 19:14:23 GMT  
		Size: 95.5 MB (95504266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f37179274d39275f985eb073fab1065c89de9eed79fe218a81beda489d967c`  
		Last Modified: Mon, 10 Mar 2025 19:14:20 GMT  
		Size: 353.9 KB (353944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0ff50873b42f1e7360840ce1eb3222c691b624aa3b0c67897c9454dd6c7639`  
		Last Modified: Mon, 10 Mar 2025 19:14:20 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638a7b530f1173d3c0eeb841d87100ae95325f1fb5d39bb878125ccd0c01fac3`  
		Last Modified: Mon, 10 Mar 2025 19:14:21 GMT  
		Size: 22.7 MB (22676455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf28ea9806567b9aeb3b1968e7643fc307f6dcf5f5b082897fc88e4b44aaa35`  
		Last Modified: Mon, 10 Mar 2025 20:44:58 GMT  
		Size: 659.7 MB (659706533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:2262f6a3e8850a1fd68cc87528619d79de20591a462e199c4acd30ee0885c1c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57531927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc17ce53fe7f7ae521ad02b76a4d02c43e492be56b75fa892f3bd6de8d1e2e32`

```dockerfile
```

-	Layers:
	-	`sha256:a8ddcf8c052cf0372099ef2cd47a09fc2d2466ffb36f34347ac944288daf23c2`  
		Last Modified: Mon, 10 Mar 2025 20:44:44 GMT  
		Size: 57.5 MB (57522146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dc1ff8899b4756071e729e5353b523c64fe9bdbc0a518415e26dddc955b3a75`  
		Last Modified: Mon, 10 Mar 2025 20:44:42 GMT  
		Size: 9.8 KB (9781 bytes)  
		MIME: application/vnd.in-toto+json
