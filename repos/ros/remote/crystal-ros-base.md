## `ros:crystal-ros-base`

```console
$ docker pull ros@sha256:97fee258096403cc7eba97148e86a3b5481b959b3c09b50d19c4bb3afdb5fca5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:crystal-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:88e5d68b53376674110cb84fc79d613e0cf8e7d008cc68cb14831b00dd68ff4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269190337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4cded9ace4393ffb76fd0914ab0f433e700d21be8e54d8ab8b3e587fea42649`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 29 Dec 2018 04:54:49 GMT
ARG RELEASE
# Sat, 29 Dec 2018 04:54:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 29 Dec 2018 04:54:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 29 Dec 2018 04:54:49 GMT
LABEL org.opencontainers.image.version=18.04
# Sat, 29 Dec 2018 04:54:49 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Sat, 29 Dec 2018 04:54:49 GMT
CMD ["/bin/bash"]
# Sat, 29 Dec 2018 04:54:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN echo "deb http://snapshots.ros.org/crystal/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
ENV LANG=C.UTF-8
# Sat, 29 Dec 2018 04:54:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 29 Dec 2018 04:54:49 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN pip3 install -U     argcomplete # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
ENV ROS_DISTRO=crystal
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-core=0.6.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 29 Dec 2018 04:54:49 GMT
CMD ["bash"]
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-base=0.6.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7c457f213c7634afb95a0fb2410a74b7b5bc0ba527033362c240c7a11bef4331`  
		Last Modified: Fri, 13 Dec 2024 13:10:33 GMT  
		Size: 25.7 MB (25691281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e847f9b0aad385ab77566a2ac923af0a15b2192907801f15b7b41f577985de10`  
		Last Modified: Fri, 06 Jun 2025 22:49:48 GMT  
		Size: 818.8 KB (818768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9ae40033f39f6a308b9384305f95efdd78e4899e4f4990ec75a69922571700`  
		Last Modified: Fri, 06 Jun 2025 23:07:52 GMT  
		Size: 159.1 MB (159062686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea2809a7d8d83c538d29214e4df6e5c7be0237eb3a0f6f57373c99f9b788329`  
		Last Modified: Fri, 06 Jun 2025 22:49:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d754330321e6127ddf98ea3d28f7c60dee76bec0880c75af15faaee93ed54ce`  
		Last Modified: Fri, 06 Jun 2025 22:49:48 GMT  
		Size: 2.4 KB (2367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26edd255e0df33ceacac45c44006e4788df63cf5d21a62a37033964a7b40d8f`  
		Last Modified: Fri, 06 Jun 2025 22:49:51 GMT  
		Size: 28.4 MB (28422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321a6c25b34e7cf48e493b2e684412ccd542e2e970da32b817beafff975cb823`  
		Last Modified: Fri, 06 Jun 2025 22:49:50 GMT  
		Size: 1.8 MB (1830601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dbdf3680df89f94e3e5da5eeb47deefbb9342a048ce3140178ff9a29f99a69`  
		Last Modified: Fri, 06 Jun 2025 22:49:49 GMT  
		Size: 2.5 KB (2475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8526c8b64ecd13db87db7dd1aff4da53b7f4863e621ad8e6967849bc8f940380`  
		Last Modified: Fri, 06 Jun 2025 22:49:50 GMT  
		Size: 344.4 KB (344389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9100a6beebfdd01f66a4f0815af11181e82599abc25ae62da2d42cf7cbb169`  
		Last Modified: Fri, 06 Jun 2025 22:49:52 GMT  
		Size: 50.0 MB (50047094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec4734dde9d09e64405a948efa46ef4e276c5c4fd623536c7f609e31a298f1d`  
		Last Modified: Fri, 06 Jun 2025 22:49:50 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bbfca2990942a96391339689128dea46309751247b0d39d87040a18c3335de`  
		Last Modified: Sat, 07 Jun 2025 00:21:09 GMT  
		Size: 3.0 MB (2967756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:crystal-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:5a475f84e339642a37bb9257a38b234cc6ae0187c9c75f3c097256e01bbf6d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21352259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a463836bbd43458b7918779c0deb724f2672b6a3f48a15e1b0d725eb21b10cbb`

```dockerfile
```

-	Layers:
	-	`sha256:e6183623e7ec7c0cf28c42995d69532a5c5bf2035c6cba4ec12cf808792c0b0f`  
		Last Modified: Sat, 07 Jun 2025 01:18:06 GMT  
		Size: 21.3 MB (21342329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1a3a02d7ddfec0e48ca2b1f727d26ccd7c450d6a8359a3964443b60173d75c3`  
		Last Modified: Sat, 07 Jun 2025 01:18:07 GMT  
		Size: 9.9 KB (9930 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:crystal-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1869298492d0dc581ae26ee80df48424d4dd0f2a3348a95f8e529b7f368f5045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.7 MB (245737222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f92b2bc47c4fd54950b2bd418d40fbf041e97f5203cef7fe238d545d990a68`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 29 Dec 2018 04:54:49 GMT
ARG RELEASE
# Sat, 29 Dec 2018 04:54:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 29 Dec 2018 04:54:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 29 Dec 2018 04:54:49 GMT
LABEL org.opencontainers.image.version=18.04
# Sat, 29 Dec 2018 04:54:49 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Sat, 29 Dec 2018 04:54:49 GMT
CMD ["/bin/bash"]
# Sat, 29 Dec 2018 04:54:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN echo "deb http://snapshots.ros.org/crystal/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
ENV LANG=C.UTF-8
# Sat, 29 Dec 2018 04:54:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 29 Dec 2018 04:54:49 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN pip3 install -U     argcomplete # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
ENV ROS_DISTRO=crystal
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-core=0.6.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 29 Dec 2018 04:54:49 GMT
CMD ["bash"]
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-base=0.6.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:064a9bb4736de1b2446f528e4eb37335378392cf9b95043d3e9970e253861702`  
		Last Modified: Fri, 13 Dec 2024 14:46:44 GMT  
		Size: 22.7 MB (22713516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da943fc9d36da891f643cb8846da026acaf282a4cd7307acd04f4d7d57030e1`  
		Last Modified: Fri, 06 Jun 2025 23:51:37 GMT  
		Size: 818.8 KB (818806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0387700f6cd8093562ae937213c0a814a6dc71f8797f21027defef5d9fb84ae5`  
		Last Modified: Sun, 08 Jun 2025 00:25:06 GMT  
		Size: 150.7 MB (150693162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d8037a33cdd60a95ce35e58a33133e51145469eba0818daabc04c2c55a72df`  
		Last Modified: Fri, 06 Jun 2025 23:35:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbbd60019031563bc9aa9b4f70361ccffcfbe9dc8b03d5d5955a0939a1aff0f`  
		Last Modified: Fri, 06 Jun 2025 23:35:02 GMT  
		Size: 2.4 KB (2369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d9fa45548d86929d143b92b098946da4edf5e8aa460d5f75646cbaed5185c4`  
		Last Modified: Fri, 06 Jun 2025 23:35:04 GMT  
		Size: 27.1 MB (27086166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a9e2533da06b130a85db5303768198da6f98d2d20d41609da408813905875e`  
		Last Modified: Fri, 06 Jun 2025 23:35:04 GMT  
		Size: 1.8 MB (1830758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01c9329681badb760ac27e64fb29a08687d444141aa330031e1e7102546419a`  
		Last Modified: Fri, 06 Jun 2025 23:35:03 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938132d1c6add11dadcef8872c77ce5370294989a672e01b7735373832284179`  
		Last Modified: Fri, 06 Jun 2025 23:35:04 GMT  
		Size: 344.5 KB (344482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc461c427408f497ab23fb2bdffc9069d2958e81d309e8cef5c6dab143cbe749`  
		Last Modified: Fri, 06 Jun 2025 23:35:07 GMT  
		Size: 39.5 MB (39515370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed664b88720c89363959ddbe9c6c889e01d0e1b2f446693104151abfbb9a2ec`  
		Last Modified: Fri, 06 Jun 2025 23:35:05 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00de986be5cd5d8488a2365676b59b4d7510580b504e1b7744c5d05b9a3f219d`  
		Last Modified: Sat, 07 Jun 2025 00:38:59 GMT  
		Size: 2.7 MB (2729677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:crystal-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:2d3db7ed11fce4678866ac52a70df95d1ac1cc4ba556744acc98384903729f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20155078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dead10c60a4f98b61e06bc045079f00317df72c5b5486ed5e0d17a81f202174e`

```dockerfile
```

-	Layers:
	-	`sha256:d418ed8acccfb32f4ef73c78d88ccd2a9a923ec18f06af9a299bf2c0b2357a25`  
		Last Modified: Sat, 07 Jun 2025 01:18:24 GMT  
		Size: 20.1 MB (20145056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:141f9d2c25c09963340255fd8fb0bd63f7c43f70a606b8c7eea83b35ece66a95`  
		Last Modified: Sat, 07 Jun 2025 01:18:25 GMT  
		Size: 10.0 KB (10022 bytes)  
		MIME: application/vnd.in-toto+json
