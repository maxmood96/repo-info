## `ros:kilted`

```console
$ docker pull ros@sha256:306ad5bf3afdf39ed07461e327c6cd27fd5b9d77a70650ffb8e5d0f016bc20d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted` - linux; amd64

```console
$ docker pull ros@sha256:59d929672dc6583eeecfb542da5916dbbaf1987f22febc0c9de9cf68afc29d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.4 MB (308366915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a8ccf0d1864f1390687cc50dba3d2b37199370f9940e9685b9ba622079bb3e`
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

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:adc0d7a760d61b5b388ee1cd77e9e237741182a975b5c321c93de22759d456e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24658251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81c36898977f57351bec0987eda50f25cd50c7d10b82a0b55f8416b375db756`

```dockerfile
```

-	Layers:
	-	`sha256:e7ff89575b3f27bef5b06e7567a9797f386b648a4a25639cb4b285b2b2e17cd9`  
		Last Modified: Tue, 12 Aug 2025 19:18:05 GMT  
		Size: 24.6 MB (24641861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dbc0142fe328f00d02328bb719c8a4a3aa1b00062e26c9d93b163ef456145b6`  
		Last Modified: Tue, 12 Aug 2025 19:18:06 GMT  
		Size: 16.4 KB (16390 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b5683dbcc5b8e02abc01297d089220cbc0cd982fd4391a32dccf8c0022d2ed16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296723633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daac489745449a0fc4ad57b3ed5cf2ba0f3e3a4dce814b2e66fc488ecff78ee7`
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

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:40323ae39a214425c6c5a19eece498a292e8e2ed328d2774371e0770e0d3afb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24680649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d13b6b42925bc6494862fd78002eec9f576f001692065204713d10e477a059`

```dockerfile
```

-	Layers:
	-	`sha256:e8a805d18d8d3effe79bb3f3a13b485146a15f8779d58081d1044fcf9e235848`  
		Last Modified: Wed, 13 Aug 2025 01:18:03 GMT  
		Size: 24.7 MB (24664122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0dd7b7bfa5a9407334422f9e0343f09fc94478c64866e753138fa70206b654`  
		Last Modified: Wed, 13 Aug 2025 01:18:04 GMT  
		Size: 16.5 KB (16527 bytes)  
		MIME: application/vnd.in-toto+json
