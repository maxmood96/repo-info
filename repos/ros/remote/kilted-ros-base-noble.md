## `ros:kilted-ros-base-noble`

```console
$ docker pull ros@sha256:3628002efd5316b98d9bbd655000e3826a01c0c2e38b03ff0f468b65da67faed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:26b110983b90a6da84576b041d8a7be6b0e91a6d1b76af0f31b513def92d5f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310817113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6e28b2155633ba56e0d7b6fba89282bfa8fc436ae3bfd843ece3ea6985cc0a`
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
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
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
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80df8e2597bb5081a304f28b13049febe272f2c6d03097adb5bf569346c6a5f5`  
		Last Modified: Mon, 15 Sep 2025 22:26:53 GMT  
		Size: 683.9 KB (683859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a1827b068556f57886cad395350cded398b71c780dad810d9cb5f48aeb1bd5`  
		Last Modified: Mon, 15 Sep 2025 22:26:53 GMT  
		Size: 6.7 MB (6746894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251ab4ea82f37711412e2ce34dff17f73d11caef6a5cb3c8f4a23bb24242ff66`  
		Last Modified: Mon, 15 Sep 2025 22:26:52 GMT  
		Size: 94.1 KB (94080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c92407c0c99f8ce4496a5f8ab4a6883930dd204426676dc03f36394b96ef20c`  
		Last Modified: Mon, 15 Sep 2025 23:19:20 GMT  
		Size: 135.0 MB (134968079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fb84c0ca29118539fdb1987693ba26bbb7fef03bad6c1349885f8189f99491`  
		Last Modified: Mon, 15 Sep 2025 22:26:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ad4e0967c4f2fc54b1fc8c9371361914af0419279ef3a09f8f9ecbc3e17f3f`  
		Last Modified: Mon, 15 Sep 2025 23:21:05 GMT  
		Size: 110.2 MB (110185503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c3dabe47646cba938ba7076a97e47b843b10a81d035548e0c5ae09767aa456`  
		Last Modified: Mon, 15 Sep 2025 23:21:00 GMT  
		Size: 362.0 KB (361999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f256a20a09d470c8e0eb81166c3ecc100e308702d21403458d3e9acb78178d`  
		Last Modified: Mon, 15 Sep 2025 23:21:00 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428752ea94da6d6c5f53cfad376970875b81973b8f3c9bc747f9a9e63e679329`  
		Last Modified: Mon, 15 Sep 2025 23:21:05 GMT  
		Size: 28.1 MB (28050584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:3a9b3c6399726cdea354cf16b97f32f5bfa561185159a7fa206e7fd223f6f637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24666686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd7d7ff410f6eee0865a03e23d397f9bae2d27bc11a25f93b107978b525ef520`

```dockerfile
```

-	Layers:
	-	`sha256:d485c22b091c5ec0658d5a374041b8f64f862cd9ce77942180ba2c349ef97a43`  
		Last Modified: Tue, 16 Sep 2025 01:17:59 GMT  
		Size: 24.7 MB (24650296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe5b68568ebb732cc32df44df48f5fd52588ca9bc343f1a975dca482d9d6414b`  
		Last Modified: Tue, 16 Sep 2025 01:18:00 GMT  
		Size: 16.4 KB (16390 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b35fc8a894c495bcf8272f81fd58405a84e6a4d9b76c5ff2eba8d7596998ff05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301412796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd65f1dab0c81523927fc539ceec4bf3d110827c2c09c5e4bdae3ed6b8a1ace5`
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
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
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
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd86736f5c635c3f5b8beef3efae36f38495b548069192ed89cac1cf4d6f934d`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 684.0 KB (683979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfbb087113ae53a3e90cb85b5963ad48e6ec8532d44321eefe684834cfc497a`  
		Last Modified: Thu, 02 Oct 2025 01:33:57 GMT  
		Size: 9.0 MB (8973926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbd17857154a30cddea03ad031105494a674f1db252bb895b5c4a81ca05fb03`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 94.3 KB (94284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9968f8f03edaf427d0a41dcda7f3a9a8b145be55f1ea067ed842bf92d5e2744a`  
		Last Modified: Thu, 02 Oct 2025 02:27:13 GMT  
		Size: 129.7 MB (129702693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327223fa4a35fd1f26458825de95cb7d529d4954db71112bfb124d0d7dcf04ae`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5dc83680276732c62d2982905f12cebedd44317e978e6d78085b929089fdf0`  
		Last Modified: Thu, 02 Oct 2025 02:29:06 GMT  
		Size: 105.6 MB (105593985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70058fa606338201849e6038a5e65ed4a30257067d38892931c54bcc0f06761`  
		Last Modified: Thu, 02 Oct 2025 02:28:56 GMT  
		Size: 362.5 KB (362513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029c1a9952b890d778e8ebee58be510e51bbbe5a70553e39094c3566884feaa0`  
		Last Modified: Thu, 02 Oct 2025 02:28:57 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac005d2fde08e254e758d6d7e2564b3a75cf637e9d90df6894fef093d88310f`  
		Last Modified: Thu, 02 Oct 2025 02:28:58 GMT  
		Size: 27.1 MB (27137188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:6143c729057d88972ef32743622fc7039aa28ec23054b4b93fff4e2c74e3d0a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24689083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4c790cb1b8298ff2fa1073c9e44999f84d254b87837aebd9117f973b9af2af`

```dockerfile
```

-	Layers:
	-	`sha256:ba3c600f8b51ff0cd430170467790fd36d876d4cec25414b9d2e1f3d53858214`  
		Last Modified: Thu, 02 Oct 2025 04:18:32 GMT  
		Size: 24.7 MB (24672557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e26b84d59d2f219bdc05e27305409e4821e848d7990978b2313b97ba9ce584`  
		Last Modified: Thu, 02 Oct 2025 04:18:33 GMT  
		Size: 16.5 KB (16526 bytes)  
		MIME: application/vnd.in-toto+json
