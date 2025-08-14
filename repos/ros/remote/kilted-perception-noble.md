## `ros:kilted-perception-noble`

```console
$ docker pull ros@sha256:c4d6b9e82dcd6b846051fe3d0446bff892d3677c75e4825f612a72a91772dd83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:4e34c0a244e6149daddc9709a91c958ff2abfca499944801ba9520d9c01c63ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1090392462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae0649b12b0023cb969e0e86933b7bb4ab916b16fd8c9bc0d1b0a0e3077375a`
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
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
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
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8458ba3c0b58143434c70cf4e6581f22fa56e20d61a6a1c84ffa7b84441273c`  
		Last Modified: Tue, 12 Aug 2025 17:56:24 GMT  
		Size: 683.8 KB (683839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10349b0da1d1089de393c57864e40dad15a76b1834f52cb2e9bae2abe6547f5`  
		Last Modified: Tue, 12 Aug 2025 17:56:24 GMT  
		Size: 6.7 MB (6746750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f415c2763c60c172d749238d5086495aea9b2123fff0c192f01ca941df418a2b`  
		Last Modified: Tue, 12 Aug 2025 17:56:23 GMT  
		Size: 94.1 KB (94071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f37eb9d7cabc674561bdb7db1f98e598c68d56c3fc7546c1b699dba8aee753`  
		Last Modified: Tue, 12 Aug 2025 17:56:39 GMT  
		Size: 132.5 MB (132527532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7bf79134a2385d994ca97451232d9fa112bca9db42258464d62d8841eba54a`  
		Last Modified: Tue, 12 Aug 2025 17:56:23 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797686f4a4316ef2e7f6977cc950dc51d33686adda2e72684f95cdc357d57ca0`  
		Last Modified: Tue, 12 Aug 2025 18:08:18 GMT  
		Size: 110.2 MB (110185393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd6abb9174e4f58f66c71a6e1b1d9836e7ac0b9c5d48e5e60ad3bdc67e08f6f`  
		Last Modified: Tue, 12 Aug 2025 18:08:04 GMT  
		Size: 358.7 KB (358724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58324f6cd4d04640ad5791366d2d47adf62dc4c4fbb1f1373fa81551143816c`  
		Last Modified: Tue, 12 Aug 2025 18:08:04 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8e163279e7f5ce816cf4aa8e39a93f61eff2364bce631b1508a1c5a24f028d`  
		Last Modified: Tue, 12 Aug 2025 18:08:10 GMT  
		Size: 28.0 MB (28044762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1860a038893a19bc5f867ca89a98dc2c3988faa011b4af14728290851ea44e`  
		Last Modified: Wed, 13 Aug 2025 13:33:02 GMT  
		Size: 782.0 MB (782025547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:8b0e53f4d4a4c0cfe8bfe0173d8d66e3c8a7d43fd1a55f1079e89f0cfb01104d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60823307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fad15915c5636d3fc61a6fcb90db5c4d9d4233d87596fe76467901617207237`

```dockerfile
```

-	Layers:
	-	`sha256:41d2a4b3e036f994802ba251ff2463334dbc80e9adc25f2b625815da4b2c632e`  
		Last Modified: Tue, 12 Aug 2025 19:18:21 GMT  
		Size: 60.8 MB (60813912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05b61ff6549e8af22de87c4f3b6065dae0507adb52574b967d9d79be603aed81`  
		Last Modified: Tue, 12 Aug 2025 19:18:23 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:10363d5b8c77adaab80c1c57cc9c8ba2db0171ce94b1d61851f94db0bcbd1daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **988.7 MB (988719534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c298be2e12c7ad18272b06a2b9b83e53d2d42a9055b77b49e55e02f02bb70480`
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
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
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
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4fca2469212f7c463fa14e87fe769d2a219fecf58125d538219a566e9b9ec9`  
		Last Modified: Tue, 12 Aug 2025 21:07:03 GMT  
		Size: 684.0 KB (683970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8101d7e467e40dcfb7a696c7d00d28a9434914ea87bae800f81106c8e471f29e`  
		Last Modified: Tue, 12 Aug 2025 21:07:03 GMT  
		Size: 6.8 MB (6759892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883862c530c4be898d18cd02b3b2123fa8a5ea159a5132eca0eef18580a0faa5`  
		Last Modified: Tue, 12 Aug 2025 21:07:02 GMT  
		Size: 94.2 KB (94211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87406253e2c43cf58eab2d463ce427f8d198773d0a1d58dd0177892cb64cd6d8`  
		Last Modified: Tue, 12 Aug 2025 21:08:52 GMT  
		Size: 127.2 MB (127233714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4419b22bff908fa5f652281aa2a2eda720ff5bc77dfc925235d36455b8d4cc`  
		Last Modified: Tue, 12 Aug 2025 21:08:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbe6023b9b69ca0bb94d591b8bcfacf7267a7fa3968a448d58cc00f1af66298`  
		Last Modified: Wed, 13 Aug 2025 00:13:23 GMT  
		Size: 105.6 MB (105594059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:decac5cda0036a2c8a8eebe79ce495eab2eaf9d1126af49c23ab05216cba04ef`  
		Last Modified: Wed, 13 Aug 2025 00:13:13 GMT  
		Size: 358.7 KB (358731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612f162ae6a274431adf24d3abad3b1787937b1829db7556b374141bb5f58ee5`  
		Last Modified: Wed, 13 Aug 2025 00:13:11 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1500bfaaeaee3ab2b01dd016de6502833ffd7cf5747aada32d7657296c12e87a`  
		Last Modified: Wed, 13 Aug 2025 00:13:18 GMT  
		Size: 27.1 MB (27136035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1e662446bfa87621738a8d1712c2c58e35c734eb0b0d9713d54bd819543b8c`  
		Last Modified: Thu, 14 Aug 2025 00:12:37 GMT  
		Size: 692.0 MB (691995901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:f4c4d688202733890231e8ae4ff710c24a9acf25ae7de5bf2009e5a0a0311c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60753912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5727f1ea7e0ad316413de24386efa55185c83cb7b3a33fddfaad4db0a4b2fddd`

```dockerfile
```

-	Layers:
	-	`sha256:fc33f1466f612c944333a7e21b2354a622b65fb08cc7db54b9c269c60cb9c7e7`  
		Last Modified: Wed, 13 Aug 2025 13:19:31 GMT  
		Size: 60.7 MB (60744437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:036869865b6b801703764075fe16935e944e35ed12a4f227a02ea0119ec0231b`  
		Last Modified: Wed, 13 Aug 2025 13:19:32 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
