## `ros:kilted-ros-base-noble`

```console
$ docker pull ros@sha256:5e3e2747312b94623a5dc179e183ff3b54d8bd07d83d6a2486357ee29137176f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base-noble` - linux; amd64

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

### `ros:kilted-ros-base-noble` - unknown; unknown

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

### `ros:kilted-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:05b5e7ce47eb5a584fdcea5438d644a231eba8c874dd565073365d85f26470a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296736710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c99015dc0f4b754794fc56706a4b501d740640ad3d3bb21218df9f050778d2`
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
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
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
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a1aeeb021ff56f6549713871ea035936891c67787fb388f08e69e57ccaa5f2`  
		Last Modified: Tue, 02 Sep 2025 02:55:39 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ffa2a8671f1746a19c7af89127b62a1f22836df01caa93a61d61b0d2574661`  
		Last Modified: Tue, 02 Sep 2025 02:55:39 GMT  
		Size: 6.8 MB (6759788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290a01a08d6a7cb15e63953b7781299b8e80e32583b1030aa55d13094df1d2d7`  
		Last Modified: Tue, 02 Sep 2025 02:55:38 GMT  
		Size: 94.2 KB (94161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2be0dca8d6f52d5f2c4ba3a0675233f0fe519dba60aa202556222a0e888f67`  
		Last Modified: Tue, 02 Sep 2025 02:56:54 GMT  
		Size: 127.2 MB (127245103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49b4e3787887556c9256034143b98c99e213f732b97da7a2fd8395a4b701679`  
		Last Modified: Tue, 02 Sep 2025 02:56:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e67f214adb5469f76e8003671cc870ef2d03407a87cf1fac62e2b6393ebbf8`  
		Last Modified: Tue, 02 Sep 2025 05:40:24 GMT  
		Size: 105.6 MB (105593915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda2941564e8029269473cbde954531b8a813a73176978b1cff4fa7531428dc4`  
		Last Modified: Tue, 02 Sep 2025 05:40:17 GMT  
		Size: 359.7 KB (359685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce602e6a7da8bb4c2153b0da7fda5a046b9c6d50ef59fd43c45fa829609f5e3`  
		Last Modified: Tue, 02 Sep 2025 05:40:17 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d752cca0552464bf76a6aaae299325cd518513536ab2502775b1723b88e088`  
		Last Modified: Tue, 02 Sep 2025 05:40:19 GMT  
		Size: 27.1 MB (27137243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:abe80e219f79672d594b93daa0afdab6ca50e504f749168e907220b635a4cfdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24689080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d326ec2ff3d1d399cc75653fa4452248aff42c90c2e0f379c5af13663d0fbd`

```dockerfile
```

-	Layers:
	-	`sha256:277bd05d35060c3477453dc69cf49501d067764c7d9d00f65510c0e0270211b4`  
		Last Modified: Tue, 02 Sep 2025 07:17:56 GMT  
		Size: 24.7 MB (24672553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd5088b1f39e0140575f8d28fc939f0fa59c3c08c1c7942a3ffaaf14aba0cf4`  
		Last Modified: Tue, 02 Sep 2025 07:17:57 GMT  
		Size: 16.5 KB (16527 bytes)  
		MIME: application/vnd.in-toto+json
