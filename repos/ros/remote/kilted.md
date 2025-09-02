## `ros:kilted`

```console
$ docker pull ros@sha256:c3b75d93080fa6127970f0d3b504674d9589e6bfb1daf1e68c11aeb44afa2671
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted` - linux; amd64

```console
$ docker pull ros@sha256:54847fffcaa8d1835bb5873bbdff3901de7dd775eecc98e8b6f1edb35ca238e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.4 MB (308382915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a266a76c926d2e37dbb17cd494a9c7b590d8eca026a21a4ee1e4af9ae3b36a9a`
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
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
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
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd02e97176c14eaa03f006fa54720bebeb708a83da54b668393efacf60573aae`  
		Last Modified: Tue, 02 Sep 2025 00:14:03 GMT  
		Size: 683.9 KB (683853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e028516e18628be8eb08e294a5a25f6154a69ebe540760b2abbea1fab96e3c7e`  
		Last Modified: Tue, 02 Sep 2025 00:14:03 GMT  
		Size: 6.7 MB (6746878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61da2aa9e2eacc0ff37e770afa4a0c40340697d1539408d5835baef2525f8124`  
		Last Modified: Tue, 02 Sep 2025 00:14:02 GMT  
		Size: 94.1 KB (94089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7a1886e59be020ece22b65154311fc45c3ad00572b966b017911d3fda27786`  
		Last Modified: Tue, 02 Sep 2025 00:14:28 GMT  
		Size: 132.5 MB (132537439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5cc470f41ac59ab3cf82150a32fea1c3ed42c33f8a446266493e528df33b7b`  
		Last Modified: Tue, 02 Sep 2025 00:14:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b9188915348bcd8cdb3cb8ab0f505d4b76bf56f72a81daa89fa450fdbc9932`  
		Last Modified: Tue, 02 Sep 2025 01:12:18 GMT  
		Size: 110.2 MB (110185157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a9912391768d1265229acda885b40746e60a4a026e38e6f5eb929022b4f3ef`  
		Last Modified: Tue, 02 Sep 2025 01:12:12 GMT  
		Size: 359.7 KB (359687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5132c1aeba0be5bc96c6267e0a5df4c314dd1700459cd549e25693ffecd4f2`  
		Last Modified: Tue, 02 Sep 2025 01:12:11 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11432e30b2351d069389aa35e3973c7c30dfb96164c0a331119152b3cb96f17b`  
		Last Modified: Tue, 02 Sep 2025 01:12:13 GMT  
		Size: 28.1 MB (28050090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:43ae18b8a46ba4f19bbd006777f45e67ea8d45a0cb88f589061082e95375dba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24666679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28cb44b84ee703b2a28f2b340842f7ee998c0e48f8860134a8f4765bbdd5a61`

```dockerfile
```

-	Layers:
	-	`sha256:0a90b9eecc942bb72841e508029023b3a34217773fb0aec5b02774293d7a040b`  
		Last Modified: Tue, 02 Sep 2025 04:17:54 GMT  
		Size: 24.7 MB (24650292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bea094d47d974da79bbeaf6b5e35152499efcc792484fbb2fffb3d38f0354ae`  
		Last Modified: Tue, 02 Sep 2025 04:17:55 GMT  
		Size: 16.4 KB (16387 bytes)  
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
