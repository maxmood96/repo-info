## `ros:kilted-perception`

```console
$ docker pull ros@sha256:f10f0ca39f932a1a3a0d9320b5a553af3ba499fd9e6b316ac20ea4709a7629ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:ec16d6322313300194810b4f79bf9a7171907e45afc78a2f3b6eec96d245375d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1082003503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235dfd1749dc7a25b40c277ca5b8553a9e9326a49ecef19aa5f4d0b87d03f198`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:35 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:13 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:13 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:13 GMT
ENV ROS_DISTRO=kilted
# Mon, 11 May 2026 19:01:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:13 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:13 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:13:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:14:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:14:06 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:14:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 20:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203aa6346a00710093073ecb851e68546fe7d5c7a63cadd967ed2e0aa14710a3`  
		Last Modified: Mon, 11 May 2026 19:01:39 GMT  
		Size: 684.0 KB (683966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8297d1086b1f98cc9287380fd3692f52255afda0cdc36d3f71de8384e801f5c6`  
		Last Modified: Mon, 11 May 2026 19:01:40 GMT  
		Size: 6.8 MB (6752218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d4ff6313d42e457ed69085fdbdc948df6fb09eda1bce0ed0adc882aca17571`  
		Last Modified: Mon, 11 May 2026 19:01:39 GMT  
		Size: 94.2 KB (94167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83cec8ec35503c52817d061b1414b615de2561b55cb85f2e547c2a4f2498d16`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 120.9 MB (120935367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cbfd4d642fd8b6e0afa60c8511d6c0bc8eb8471fac315e352391383debe6f0`  
		Last Modified: Mon, 11 May 2026 19:01:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6dd392dbff6d7b6d67519ea916b13cc6925d0f92d2307dbd82948acdad262e`  
		Last Modified: Mon, 11 May 2026 19:14:56 GMT  
		Size: 110.7 MB (110663798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1181bd112c159be737e19d577fcc94d397c7a43df3b628032eba0cd6d04aaf1`  
		Last Modified: Mon, 11 May 2026 19:14:53 GMT  
		Size: 382.2 KB (382206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74b2253a336265af7d54719c96a7b7657acd02bdb998b134763b3d84a72ba52`  
		Last Modified: Mon, 11 May 2026 19:14:53 GMT  
		Size: 2.5 KB (2517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3324873c74ee6b185565d669a1ea23f5580faf99788e41da860250d9c7599abb`  
		Last Modified: Mon, 11 May 2026 19:14:54 GMT  
		Size: 27.9 MB (27889131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518a8710847f07c6cec235443e0164daabd110ed01aeb7b20f3e3d93ff7904f8`  
		Last Modified: Mon, 11 May 2026 20:18:23 GMT  
		Size: 784.9 MB (784866959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:dd76c06623afe43413fcc8540211d56baa06acd2a94d6565c7728926a89b0953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60933291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde38d31ed2fb10170c58e325e7c6a20ee4069de1e7ce7755c4927c022fcc950`

```dockerfile
```

-	Layers:
	-	`sha256:8a6d00c1b4470dce7c2f7e688520b0d8a2f526fa39e2ab8fb83d0545d0992f05`  
		Last Modified: Mon, 11 May 2026 20:18:08 GMT  
		Size: 60.9 MB (60923940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50b7d7b496637da95284a2b0eab577946a256a2bcbe9b6f9d34074aa7e7e1239`  
		Last Modified: Mon, 11 May 2026 20:18:04 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6d434861071c4ad6eda1f362305ad288a40c10577d68704cb2989068639c4639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.5 MB (984517104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212429b520a084e1922ecb666e3cfd89b325e308d00a7552d238b50752020703`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:47 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:08 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:53 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:53 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:53 GMT
ENV ROS_DISTRO=kilted
# Mon, 11 May 2026 19:01:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:53 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:12:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:12:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:12:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:12:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 20:16:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc10796365a045f536d89d2fac057e52b1f2ac4ded2cd70e983c8d188e980099`  
		Last Modified: Mon, 11 May 2026 19:02:21 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cc3dfbf9593cf69afba801c78df1d39513c204943247037d87b6ffc686f2bd`  
		Last Modified: Mon, 11 May 2026 19:02:22 GMT  
		Size: 6.8 MB (6765719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0325aca0beeecd063d5b36f9d2b79c49f8b5285d68089393904bb78725a415c6`  
		Last Modified: Mon, 11 May 2026 19:02:21 GMT  
		Size: 94.4 KB (94387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03683ac42ce0d6085689c7560dccd52e485e8811e595a23298003750fed62592`  
		Last Modified: Mon, 11 May 2026 19:02:25 GMT  
		Size: 115.7 MB (115660823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0310fb8d7ab59c87909b9450d1df5d071d4e1796dd9aff7a3039b45a8807780b`  
		Last Modified: Mon, 11 May 2026 19:02:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27109cc6f2f4ce1d42bfbc092c0beee92d9717649e91b7bd9673e2fcbd075cbd`  
		Last Modified: Mon, 11 May 2026 19:13:10 GMT  
		Size: 106.1 MB (106090308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d522455a5a2e6e8a9311ac13057aa690b6d1ebf53c75b456e1cafc24bf8f9f27`  
		Last Modified: Mon, 11 May 2026 19:13:07 GMT  
		Size: 382.2 KB (382192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834d76cc9a9d526bd2365c7b6dc88a52aaf996f604271a069a01abc4cc2f0141`  
		Last Modified: Mon, 11 May 2026 19:13:07 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bbcab63cba92ef478797b62881851c9f78d63434813a411a979a749f7fac07`  
		Last Modified: Mon, 11 May 2026 19:13:08 GMT  
		Size: 27.0 MB (26997534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e42a24d7148ad851d01b0f14a34e0adbe6ce1a671ebfe649f5fc69e3a4e61cc`  
		Last Modified: Mon, 11 May 2026 20:19:04 GMT  
		Size: 699.0 MB (698963453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:9fff4e271c674c4ba2f760ac32dac6b529720bbe9a5e890d1e3a77fa75688b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60863892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1feaadbb76f92ca542e7a4d7100d9123dfe44f49e5f45915fd5cafb3ece86b3`

```dockerfile
```

-	Layers:
	-	`sha256:03db9e2d0a4f6ebb2b9e15398f95d336bb273e9764942dfa87fbb79ce163e996`  
		Last Modified: Mon, 11 May 2026 20:18:52 GMT  
		Size: 60.9 MB (60854460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccafddf35aeedcd1b9de7a4099e1ca2829418353116ab4243d0d9df91797e22d`  
		Last Modified: Mon, 11 May 2026 20:18:50 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json
