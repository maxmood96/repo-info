## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:770b00e2b481e472b4d08dd271130ba4c9a5c639317275c4a2019bb10c51dcde
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:f1613b21a930f6032e7d67ebe5a2fe21fc68b54a1f068d7ce2eaf476b461def4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.2 MB (622194505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce68bd75e78cd40df068865833307626f066e74634bd2646b1a72b700f962a0c`
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
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
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
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08803d401c081fc3d12416d99b187a634698db36a10df80f4cef29170ef83e5b`  
		Last Modified: Fri, 05 Jul 2024 19:57:30 GMT  
		Size: 681.8 KB (681844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f68a5436d21a97e82cf7e242efe03dde4f5b729ed2dbaf097fa8087d993f1c`  
		Last Modified: Fri, 05 Jul 2024 19:57:31 GMT  
		Size: 3.6 MB (3558040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36adc7815cbb0b60279e15f0898d1f5d3880e45c336e2d37b6e55f3c19a7d41`  
		Last Modified: Fri, 05 Jul 2024 19:57:30 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dd0181ad8621c2a9206894fa0ac8823b0e7b0c1e07f8700418d53b93a2fa76`  
		Last Modified: Fri, 05 Jul 2024 19:57:30 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b76af7af5fdf91bcc77e8167917c7c9febf10158f328daafe713d29813881e`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 122.5 MB (122459142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79ae2ca4e9abcb78cdac5210d4cbcc57bb261e4fd8cca1695e8606c8e4193be`  
		Last Modified: Fri, 05 Jul 2024 19:57:31 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5321657307942f41a64bc471813d51df34d29ad63ad10c3d793023b9021fe79`  
		Last Modified: Fri, 05 Jul 2024 20:52:58 GMT  
		Size: 114.1 MB (114108837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86be0739349eff42b0a8e0e345e9e9a8aa166f249d7f6ef37b687d356f47b3b6`  
		Last Modified: Fri, 05 Jul 2024 20:52:56 GMT  
		Size: 320.7 KB (320664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cb43da572f51f6a10a289760b4f513838dcd8847ee4d4f6192252fc22c8ea4`  
		Last Modified: Fri, 05 Jul 2024 20:52:56 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8529e63f95c2d883fe2a372f6ab67e93846ac82959ffd623ca33286548c9db`  
		Last Modified: Fri, 05 Jul 2024 20:52:56 GMT  
		Size: 27.5 MB (27525587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e6cb64aa8a32ee5c16ba6db45d611d37f53952605f2841fad98cd87525ff7d`  
		Last Modified: Fri, 05 Jul 2024 22:58:51 GMT  
		Size: 323.8 MB (323830314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:a01192c1d4c75991cf3b46b79291592b7f265a0eaa4e99c5db05f057fb260556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41862974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa14338b46b978bd9c78205014df5139ddd1f22d20dcee24bb4827b06dfbb15`

```dockerfile
```

-	Layers:
	-	`sha256:c6ebfa1e97cf1eda86b20f887ff636f38ee9246c9ca89ed90f960c854b793733`  
		Last Modified: Fri, 05 Jul 2024 22:58:45 GMT  
		Size: 41.9 MB (41853320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5a84a6671a73a4dbac4ba3d4eabaeb74153fe4d17aca385efa740c30f395b4c`  
		Last Modified: Fri, 05 Jul 2024 22:58:44 GMT  
		Size: 9.7 KB (9654 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:64e6ec792eff7c3d11f24baf60fb0eba99c3a7f093a70b8ea40bb35301cd1c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.3 MB (565254776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccff6588f7c05f70d285128536b8912d546e14653184acae07d04443318b33d9`
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
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
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
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00b51afdfa888108b5327eaa25f853a74f2c27da7625d948bc55801e64f6ca7`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 682.9 KB (682859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52f820b5d2d06b509882a9cc403aeb5252f4c3f607b1f19440dfad83e210a4c`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 3.6 MB (3557860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44530f29d7b23d361456650ea1c47949c67bb960670945ab3965c4a0343ecd4e`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa6a1ba10484c96c3d670c92fa3def01f5a86f8625fc602e8c98deb062a7a64`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2bcc4261342272a0b424b2401e4e9c1ea3ea48e2a0be3cb37d3d60ce914fda`  
		Last Modified: Fri, 05 Jul 2024 20:47:53 GMT  
		Size: 117.3 MB (117265893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64869f6a58555ee8828021c2ebca140ab2ebc780b737e8bcf35b2779cba239`  
		Last Modified: Fri, 05 Jul 2024 20:47:51 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04377fa51164b0ddeff26326acbec8bcf286902f25984a00ad5b9770309eaa5c`  
		Last Modified: Fri, 05 Jul 2024 21:19:13 GMT  
		Size: 111.0 MB (110952468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de20866bb5b0e8c5cd02eb7bdafdbf97e9d2c76e843c86834718b03e927523a7`  
		Last Modified: Fri, 05 Jul 2024 21:19:10 GMT  
		Size: 320.7 KB (320662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d5b3fd79a1b761f8269b08686ff60c0d760bed1b9e7081c0572fbc0314c0d8`  
		Last Modified: Fri, 05 Jul 2024 21:19:11 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18ee15bddfe47248908eaa975ae8811c53faa743b28e8556d61b5a7bf116436`  
		Last Modified: Fri, 05 Jul 2024 21:19:11 GMT  
		Size: 26.7 MB (26671682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f292cc5e2c1d0ccbfad936c8fff806ac8f3c83d0f44fe829959695f7c85aa114`  
		Last Modified: Fri, 05 Jul 2024 23:53:01 GMT  
		Size: 277.0 MB (276955400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:e405f8232bd606164745daf0a13194b463000d9f73fd49adc7e7bfc53d820977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41863716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2c2b8f2ba753e63be83d21547cf8aa3ceada6608e6b30a6f366d597e6f53e9`

```dockerfile
```

-	Layers:
	-	`sha256:726cc8db93af593d08fdec232f81afc286061c7296a3e4cda432fbf27531f650`  
		Last Modified: Fri, 05 Jul 2024 23:52:56 GMT  
		Size: 41.9 MB (41853701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7caadde2ffb44d7d9da6c08b609e069bf4b6b76a5584d3e68679bb422484c28`  
		Last Modified: Fri, 05 Jul 2024 23:52:54 GMT  
		Size: 10.0 KB (10015 bytes)  
		MIME: application/vnd.in-toto+json
