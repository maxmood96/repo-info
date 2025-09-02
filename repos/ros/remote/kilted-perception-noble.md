## `ros:kilted-perception-noble`

```console
$ docker pull ros@sha256:8f6991857fe9396c896625c177c1a7f36603c310f032b9342d217341c34ef33b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:ffa2dfe245866bc077e29c252600723321c280a0607693c496ecca1a5f475b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1090409822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af97839aa535fefd7c6fa7e65b410940b7ab08db0cfa7cdf427fc984e51c555`
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
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:1409f24755840a991f800d9e93118bcefbdcad9ee3650c1018d0409b27e8e4a7`  
		Last Modified: Tue, 02 Sep 2025 05:05:39 GMT  
		Size: 782.0 MB (782026907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:740777b47579cf026126668d1a7e325b85df6e95eec955876e9b28582ca37547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60831738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734ffb889f7581eefc32bc1b6cecf983b6903ea09d68c4d286cf827c13e74cf4`

```dockerfile
```

-	Layers:
	-	`sha256:d01cbf09d01bdb6fd04552fcac752cb41b8d3574ada3317142ee30730d52c399`  
		Last Modified: Tue, 02 Sep 2025 04:18:06 GMT  
		Size: 60.8 MB (60822343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5180c04a69fa3d0c076d2ab7c22e06f1fe10996633efe1d3df3d9c95edaafc02`  
		Last Modified: Tue, 02 Sep 2025 04:18:08 GMT  
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
