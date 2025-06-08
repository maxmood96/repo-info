## `ros:crystal-ros-core`

```console
$ docker pull ros@sha256:038249f735e7c1985ceef6824aefbcc798272aa8cd0b444c8e5df271b4d02214
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:crystal-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:8b003dd48a497cf809bb06ffb93067d93e47e94cb16aff59911cb344ea9c36b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266222581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bea3dd92f8965708e709ebea184da1709503016e392671dc34ee95f4e53800`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN echo "deb http://snapshots.ros.org/crystal/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN pip3 install -U     argcomplete # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV ROS_DISTRO=crystal
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-core=0.6.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:34 GMT
CMD ["bash"]
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

### `ros:crystal-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:016a01b76cf9c1158c9bb046d3b7529a3ed236583a3fc6eebac31567832d351d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20574651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991f81f0d9235592a405f3021fbfef8ccfcbabfe2966dbfb69e0181526ad0ec2`

```dockerfile
```

-	Layers:
	-	`sha256:15e58cdc1298060d0e9740e983660233d32212b22bee1bb057b5a4399f399fff`  
		Last Modified: Sat, 07 Jun 2025 01:18:17 GMT  
		Size: 20.5 MB (20549444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c9c7d9de46a5ca3808913cee9a99b47f0da8112bdb68a1760d205d7666854b5`  
		Last Modified: Sat, 07 Jun 2025 01:18:18 GMT  
		Size: 25.2 KB (25207 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:crystal-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9c0d99279c60cf06110c31e1df372a66aeb95a0c4fcf4f29b3637e505b9c86f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243007545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5a1048444cc4475ca1bca2c280114413fd6d2007d0547fd8e81d57b6a290cf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN echo "deb http://snapshots.ros.org/crystal/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN pip3 install -U     argcomplete # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV ROS_DISTRO=crystal
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-core=0.6.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:34 GMT
CMD ["bash"]
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

### `ros:crystal-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:38a0b32c32a5580c45369da5cbf665f91b2dc3a428a1f6d62a653db0f4bb32ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19405997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b766860b344887b19cf6e7db86bd2968eff6c16a19126caef20a5d05c53214a1`

```dockerfile
```

-	Layers:
	-	`sha256:fb58673792180587f7785db9ca69ad15d02282e29edaf5ce9f30ce637c6da9f2`  
		Last Modified: Sat, 07 Jun 2025 01:18:30 GMT  
		Size: 19.4 MB (19380596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1057357e0cb3269c6d28913a40fcbd688d704c8f1e8c111de8f41e77daff3ef`  
		Last Modified: Sat, 07 Jun 2025 01:18:31 GMT  
		Size: 25.4 KB (25401 bytes)  
		MIME: application/vnd.in-toto+json
