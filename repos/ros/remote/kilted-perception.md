## `ros:kilted-perception`

```console
$ docker pull ros@sha256:02248d162c0810f7e8e253d1f0da81f62fb78d6d69e52aa1a42f0235d8ffdf9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:e1ad65669608fc7e11be058eb56a6e324ffe66dd92cb8431d7191941a72a7988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1089468164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2072229b981af9f439007905ef76b52bbd1f274c890b316f2b28820b2afdfa2c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b35fcb4c72e4e1b576c9ad4eeb168575fdcd9f08aa9626159697d08f85f11d`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 683.8 KB (683766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a6ec29354bbb917479948bd512e7a37b5a78b548201e41ab844f5cd27b0a73`  
		Last Modified: Wed, 02 Jul 2025 04:13:15 GMT  
		Size: 6.7 MB (6745540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910605ef6993fba7a0021d6777f55c01af1f52d7fc5fcaaaefba86d25561efe4`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 94.0 KB (94001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47410432c7f18b2fef7279829cc16c86748b308925bb2b928a0d1f18b5a9faf0`  
		Last Modified: Wed, 02 Jul 2025 04:13:19 GMT  
		Size: 132.4 MB (132424061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e057fb5b5c66bd780fcacedc32a3c495cf63933eda6c5c80a9db3df9b484c53`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7a35d9d6945cc374a7bbfe3995e6dbc6b123699603aaa8c7990a77a4dc1369`  
		Last Modified: Wed, 02 Jul 2025 05:11:27 GMT  
		Size: 110.2 MB (110186022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f65b252b4fd53b5ea6489534264475297a3f51a4fe0598b9ff93a0abfeab59d`  
		Last Modified: Wed, 02 Jul 2025 05:11:23 GMT  
		Size: 349.5 KB (349530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80acbf80c434da40993753a67a3ba8d7b3d0beab94fd257e6e037407515b0c7`  
		Last Modified: Wed, 02 Jul 2025 05:11:23 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdfa16ecda5fcc480a52ecea59a92cb7df654f4ec78d25471bde0870d708f60`  
		Last Modified: Wed, 02 Jul 2025 05:11:25 GMT  
		Size: 28.0 MB (28035850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a336c75d1a418190091c4dd0e9e617ee21f5a43d5e3250874545d0b86c099b16`  
		Last Modified: Wed, 02 Jul 2025 13:44:57 GMT  
		Size: 781.2 MB (781228368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:6c658b53db9e02743e60280034bcc96d1d188472e3a1bacf462e351196b1c6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60833904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94c686fa064203c6a40722524940d4765944afb88bbb9be17019ffb81aa8ae5`

```dockerfile
```

-	Layers:
	-	`sha256:9357acf14b760c0ab796add917ac7161f7e5ae3c9336bca24a055488ab8ae0cf`  
		Last Modified: Wed, 02 Jul 2025 07:18:07 GMT  
		Size: 60.8 MB (60824509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37cd757cdd55eab76c9f6182c3b6b9e201e0f8f743f5c4c0f29906258b593c22`  
		Last Modified: Wed, 02 Jul 2025 07:18:08 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:65dda2b1da4506a8ada257c74b91c8f916334b2fa6835c1931fdc6f4da27d77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **988.0 MB (988014104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19518177178a7218e20fd621d3233dead129dc27307e8269599c03ac7e1d6927`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d7528a0593a687366e793711eb7a036e8bf103509785a61913bf5858f83940`  
		Last Modified: Wed, 02 Jul 2025 06:29:33 GMT  
		Size: 127.1 MB (127115953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94731d288701fbac725cde2c66a4c866e7bc2a7e160fbd0f835eb50ae626e5a`  
		Last Modified: Wed, 02 Jul 2025 06:29:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245c50a57c3d0b1f339d0824f2a936f99bba2fe0eeabb7766b65f4098430a010`  
		Last Modified: Wed, 02 Jul 2025 09:17:49 GMT  
		Size: 105.6 MB (105594130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784cd5894385f601f510027e6896f3227810a6905fff4495333cd2a05ec3edda`  
		Last Modified: Wed, 02 Jul 2025 09:17:44 GMT  
		Size: 349.5 KB (349526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e758c429f764c8cd2ba3728865a6864d8ea589351940ceb59a0821349978a8`  
		Last Modified: Wed, 02 Jul 2025 09:17:44 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a14c6084c7ea506309951bfcf6196eeb524a3efd7b732fc211de2f4ef708527`  
		Last Modified: Wed, 02 Jul 2025 09:17:46 GMT  
		Size: 27.1 MB (27128913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a9b0bcbfb8e7f6162f026e2dd0a844f577c9ff623578aebbb7e00cae7f1eec`  
		Last Modified: Wed, 02 Jul 2025 20:04:04 GMT  
		Size: 691.4 MB (691430054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:9c30a5f79379181fb9031c34ebbbcefd454e372ca24f2fcd8051fa631b2864e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60764511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f461b5ac616f8b12e7247b7ccf5f72197e673bf76bdbd97897abff7f1304a901`

```dockerfile
```

-	Layers:
	-	`sha256:5a40692661b4b8a510b80b7ea80d44bd8935c37734fbd5cf83779030b4c730df`  
		Last Modified: Wed, 02 Jul 2025 16:19:27 GMT  
		Size: 60.8 MB (60755036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:107ed9ef037676b7b73d027b4a2edf7765585c61aadca17b188ecaa509a4bec0`  
		Last Modified: Wed, 02 Jul 2025 16:19:29 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
