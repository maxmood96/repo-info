## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:029b235468abbd489780a439ae35b739bd05a42edb5c5f10f3e1b3db30300f36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:f414f0f55ca18ecd31844deff5e7697d982790844e447b13a6450f6271592997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.7 MB (324675620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41af6baddc4abfe59e2d6f0cf880a9a9b36c18d8411d5ee7164aafada8498f01`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:41 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e859821e0442ece0b7c9f42ee8bcdfdad70f04374296a0341f99d1b376c5fa0`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 683.9 KB (683916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5287ecfab6903c1f04dc7eb19db93c17deaeea31b96bef58d717b45f2c1f381`  
		Last Modified: Thu, 13 Nov 2025 23:38:23 GMT  
		Size: 6.7 MB (6747192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1391505c3b5afdfe5141ea504ca465b721466073e736110bbae8d00f5277076`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 94.1 KB (94107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b150d605cbf49762e7160bf96073e12929d3fd3225eaee62cfa1277c65c988`  
		Last Modified: Fri, 14 Nov 2025 00:35:10 GMT  
		Size: 149.1 MB (149072998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711191b04df06da29609c7f663aca5b507baf432896470fb9544ddc7f887c1c8`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38ce9f7a316883bfc98e61ca8daa6375c6da50cafdfa85179993462ccdd487b`  
		Last Modified: Fri, 14 Nov 2025 00:36:58 GMT  
		Size: 110.2 MB (110187245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aedd5e5070fd29a8c753b2de8d407a4abde0375c9b87f0e6d79b5eaac109ec7`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 360.6 KB (360566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ecebcb6d8e697b2f3a67cae5173e1720c301480051226726d5e49cd344bcac`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eebc0c9343354909e51a450637213bc65cd5c91d45e429df1276e62c143dee5`  
		Last Modified: Fri, 14 Nov 2025 00:36:51 GMT  
		Size: 27.8 MB (27802204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:66ddeffd7daf51f32eabea4b4f291a53e86fc95d72aa6df4af2dd0ca9a76ed6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25740803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03df47cab50819f0c219786a9e845ce6ac771bb36997070a09d31f320b6e5b60`

```dockerfile
```

-	Layers:
	-	`sha256:71c54244bdb403b3d6b44098fafb232e6f53cbbb40ade9e8486caab58fa02dc0`  
		Last Modified: Fri, 14 Nov 2025 02:19:02 GMT  
		Size: 25.7 MB (25724438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a74c9352a53a21487108f4767012a0672567fca97fed315ee748096c737db26b`  
		Last Modified: Fri, 14 Nov 2025 02:19:03 GMT  
		Size: 16.4 KB (16365 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:28fd4ade8c7eeceef74187f01cf26800f5d7c67ff22f62fa27a16b65746aaf1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312650455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdf90b6fa04814069b7cc74317cdd9f3421e7b712843f32141043c5a76571cc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:11 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a2cea4c13e33edea2b72ed3f9d4748ba6dc241cee0acd04c241e80435bc823`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 684.0 KB (684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc69d87f518d8d7ac1084d666faf5003052bd6348dfeb6767064dd5c8442de`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 6.8 MB (6759913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d8b3301cd177c6ecf92c07deffe541461e7bc3543f8757723651628c28cf02`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 94.2 KB (94204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3a3e81481b556e57eef37b150639372f8d46f43b27b5097e8d669ff949ebff`  
		Last Modified: Fri, 14 Nov 2025 00:35:58 GMT  
		Size: 143.4 MB (143399101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f535c7019fbee286fb2b8dc53062e4d553b2a26164163daa0eed14cea9867155`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae6091bd1596cc9c94b3cf84cb131436ea38de25e0618787e197518ed2db80f`  
		Last Modified: Fri, 14 Nov 2025 00:37:41 GMT  
		Size: 105.6 MB (105596555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b3a9ff141db5b9d69a0e41e760ca068e881815f7be18d25824ea2a0c1818f3`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 360.6 KB (360561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885cd29b3de7a5c35ea79ca53c67b77daf2a0dca29a89e827bb0eec950d914d2`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5b2ee5e669e6632fe1d194fc920793372c6aeeedd6313ee11622b66897930c`  
		Last Modified: Fri, 14 Nov 2025 00:37:37 GMT  
		Size: 26.9 MB (26891440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:fb6bccc15b557ab67edb1d332e3a80ade8893c2865d1fc4f5c4bceb31e487a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25763398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41117bc44e3f37051e031a19cc2981fd6dc98b44d7b0a5d736009df486bc0eb`

```dockerfile
```

-	Layers:
	-	`sha256:e94a7abd29f5ed0717d069409d1949ec6ce56cee5dea8dbc3aca8199a0894a25`  
		Last Modified: Fri, 14 Nov 2025 02:19:27 GMT  
		Size: 25.7 MB (25746896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6bfa8cb739cd81e1891288b2e14a5ec0f76cc16c406310bc7fc5d4f551b125`  
		Last Modified: Fri, 14 Nov 2025 02:19:28 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json
