## `ros:kilted-perception-noble`

```console
$ docker pull ros@sha256:851d2e0f778cd746eecb2765fc1f554d9de032235028a2e180853373ae2b6e91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:f810ddca7b279158107574c6ce625f1d4eb80fb986b3cafe144c598acfbaa52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081681335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362ce0f64f6743d88da084c703212db1c944cc042e5258487472125f568459b2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:13 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:53 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:53 GMT
ENV ROS_DISTRO=kilted
# Tue, 02 Jun 2026 08:21:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:53 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:14:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:15:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:15:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:15:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:19:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685092803da43ca941292a896dd8f48ce1a8d91790f69c2b1c79155b9a69b145`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 684.1 KB (684100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfe1f8d3291d469cb43e34c42805d2fc2b1c783dcf66f4ee0525af8f9949005`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 6.8 MB (6752403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ad6cfd35f7eb6e09d5e6988027d6d14d4616a251e4b6f7b15d46610e5da6bf`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 94.3 KB (94312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16adb782f56ae8a50f40642754bde93ad1b585f0ec4ad386db098320f795644c`  
		Last Modified: Tue, 02 Jun 2026 08:22:24 GMT  
		Size: 120.8 MB (120789572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd387be3eedd271dde548d6e8d372f2d0df9203a335b5a07277419fd3a25c6f5`  
		Last Modified: Tue, 02 Jun 2026 08:22:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7591985e47a84095a344162d1c2db751bf489e751dcd4e74636cfe7ce1b56c32`  
		Last Modified: Tue, 02 Jun 2026 09:15:51 GMT  
		Size: 110.2 MB (110196246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a097140c3e1ce3192ceaafb4247254801b5536f5ff6e4e935df9b35d20218973`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 384.0 KB (383978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3112170637d27b54fc305ed87c92758f6cac238c074fe0c0e11226c3e22c94c3`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac36c7d12f9264e8c13e70c4be0a94ec42d19a7fa9ef2e9020fa697cb5aee914`  
		Last Modified: Tue, 02 Jun 2026 09:15:49 GMT  
		Size: 27.9 MB (27889252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b56b3d05a6b7440849c36aa784af3d0fb9bbb69f3a047146bfa034baad1c063`  
		Last Modified: Tue, 02 Jun 2026 10:22:07 GMT  
		Size: 785.2 MB (785155973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:4096d1734135679309b4c63ea1689e518902195faeaa2747a6471a1f549a4d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60934145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d23a71d829c2df822e0f1972c0656b583e757a0c403f31c67d50752c4c59a3`

```dockerfile
```

-	Layers:
	-	`sha256:caa64c2111d457cd75385ea1933663acd672b4b6c7b7dea3ddbf60fe2a9ebc8a`  
		Last Modified: Tue, 02 Jun 2026 10:21:54 GMT  
		Size: 60.9 MB (60924794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e86a8185b6ca87ea0caf5f2eb452203151125c577c4e22124d3aca0a53fa9ac9`  
		Last Modified: Tue, 02 Jun 2026 10:21:51 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:34d5046ade40a0d5efbdc98e2816fc521030db5bc7bc068176eb1016bf597d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.2 MB (984210995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e873546207eda37bb541c2fa4db2dee886491bb6a52a83a19720aa3361d9747a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:30 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:09 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:09 GMT
ENV ROS_DISTRO=kilted
# Tue, 02 Jun 2026 08:22:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:09 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:23:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:23:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:23:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:23:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:14:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b416145b2d0ffb7ae21a537e749877dcd599e74b4d9f478ff90dc7ca53b9bd61`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 684.2 KB (684232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6875267f1b9da5a58d88bcee0d575c2e293237fb4742314202eabbc1d1df8`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 6.8 MB (6765733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42269c28912bc00b80ac1cd7f69237e55b1853486f06e98f684b3b531cad7572`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 94.4 KB (94402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e07f457aff02417cb213909621dc479df8474c419987ecb0627cd88fd7bc2a6`  
		Last Modified: Tue, 02 Jun 2026 08:22:40 GMT  
		Size: 115.5 MB (115517604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930c855c40a83380b5b946026099a869c99e32021af8b48e3604c5218a4e9c70`  
		Last Modified: Tue, 02 Jun 2026 08:22:38 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf77bfb824aac72d5c1073df5f5acb6b7a3c20d107adec44a222da0c810d8c94`  
		Last Modified: Tue, 02 Jun 2026 09:24:11 GMT  
		Size: 105.6 MB (105609755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4428427f205c2c454f011d2825db888344ddc8501ace447a350671bfef15670a`  
		Last Modified: Tue, 02 Jun 2026 09:24:07 GMT  
		Size: 384.0 KB (383972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a251bc17a680222bf4f00827205fce57a7a1229a19ed87b70fb066f99a0c5910`  
		Last Modified: Tue, 02 Jun 2026 09:24:07 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c18e61574b544d7fd789fc4baed9d75abfd91e2912379743520d5aaf7a68bf6`  
		Last Modified: Tue, 02 Jun 2026 09:24:09 GMT  
		Size: 27.0 MB (26997482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da16fd02efd72c13d52b7df4a570eab94e827361785e920aed1158a42b058cb`  
		Last Modified: Tue, 02 Jun 2026 10:17:31 GMT  
		Size: 699.3 MB (699278719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:99a11441dddef0e0d1aad4f3301d21d75d445d331688b789cb9005bf42eca76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60864750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b87cc50a78cfaf607277e28bd310860f0ade68d9c615d5cda091c494f8631c`

```dockerfile
```

-	Layers:
	-	`sha256:f3a2670857037c0e44fb6c2eba9c9594c5631a0d606dcbd99a1c6536dc77dbd4`  
		Last Modified: Tue, 02 Jun 2026 10:17:19 GMT  
		Size: 60.9 MB (60855318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0af211f7f444ca4f62d4455ae96d0fb095012b14e105cc092e5ebeb557fefb`  
		Last Modified: Tue, 02 Jun 2026 10:17:16 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json
