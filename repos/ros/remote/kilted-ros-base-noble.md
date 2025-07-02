## `ros:kilted-ros-base-noble`

```console
$ docker pull ros@sha256:ff35b75fc35505ede9607df277b24cdef86d3c082bcd052e8164ef6170923e96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:d1731a84608298b7f9f3fc44a8a1353fe606a84c37d45fc6b68b728027e004da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308239796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fcfdc00a096c70701d65348ff2df89721886af9a97465f38aa7555c54f620e`
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

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:56d8757abb7bd23f0b728f08b8a755058cea330b1a606b3f1a48ad4f8d61950e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24652798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd1416d76e876a1ba870e664e0c4f11df9a0071aa1f5d29c6b85b70ce8712d3`

```dockerfile
```

-	Layers:
	-	`sha256:efbd9ad746fa0f176367a3bb5d6e282eaa4961549e2f032b87020bb0a651a9b0`  
		Last Modified: Wed, 02 Jul 2025 07:18:01 GMT  
		Size: 24.6 MB (24636408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90eb727f87e7370c4afad7493905205e3ada84dfacab887fb7693bc0dc33796d`  
		Last Modified: Wed, 02 Jul 2025 07:18:02 GMT  
		Size: 16.4 KB (16390 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:87260e8b0f77e8183629f6e5a4b941306bc9d5e5d01c0e973cf0ec47ccd62455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296584050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51dd28410a8cd6823800155dfabe062d03afe081337cfae7c4145458d0b2f42`
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

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:c5d49a60f3d8a21b64f0a6cca3d2a2c3a01d0fc85089e53d319f1beb55784a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24675196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd06b388bfacd51354ff4652dccc92dc593e5129ddead6df4b98172f9a41742f`

```dockerfile
```

-	Layers:
	-	`sha256:43bf9269c2eae35bccdccce11f98d160b9312c872d39ccdaaebaacc3b053df78`  
		Last Modified: Wed, 02 Jul 2025 10:17:57 GMT  
		Size: 24.7 MB (24658669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e70d138ae4a633ac50de1359477ed9b134136250430003ef3a2eedfb3cbe88a9`  
		Last Modified: Wed, 02 Jul 2025 10:17:58 GMT  
		Size: 16.5 KB (16527 bytes)  
		MIME: application/vnd.in-toto+json
