## `ros:kilted-perception`

```console
$ docker pull ros@sha256:df006176bdbb38a2f4c59f304ee32ac46bac54aa03dc4a0133d269baa49fc468
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:e6f91c3d34b47041c937a5daeb2f0a55c8479b8883b1d7c61252dd304dcaa279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1082902200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec818ea038b7bfb7815ab0c942fdd455cf6045c2fb73a15e3307d481bbcfab14`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:35 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:21 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Feb 2026 20:31:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:21 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:43 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:46 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:52:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe6258945f1d2a6e861a58388276d97ad9e277485239d40e851988410562ea7`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 684.0 KB (683954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d05fb7dae912dbe49e93ba6434ac0d6b402be813c0b373f2d69eb287cc8071e`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 6.7 MB (6749467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da204b536633a39ef76265eca1307eb09e44ce38040f08f2bff65c24fa1cf37`  
		Last Modified: Tue, 17 Feb 2026 20:31:49 GMT  
		Size: 94.2 KB (94151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6b6def36f07048480e9220add30ca3c423fb273e95213c76a049165ecbaaae`  
		Last Modified: Tue, 17 Feb 2026 20:31:52 GMT  
		Size: 122.3 MB (122252285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226eb2247de4862db4e76be01f1b2fea4af11588b4c4a7de5f41a3bc748198e`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7664201107a73be69a1fcc67abe7b8dfba9f08f8ac21cd6e6653ff31c72386`  
		Last Modified: Tue, 17 Feb 2026 21:30:45 GMT  
		Size: 110.2 MB (110187964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1ca4d412f7ba8e088e340e41db78e3af76477eef4de912442cad60baafe980`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 374.4 KB (374406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b84c226681e00ba22043272c1fd02b401bd4ef90eeb5d75340c924016701c0b`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f44533e62581038678d3c036cd8b357f29ecca65c9e45adeafa646d32244d7`  
		Last Modified: Tue, 17 Feb 2026 21:30:42 GMT  
		Size: 28.1 MB (28064217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71edfa12c0b2f586afbbc2dc086c98d0e4752d1791c77d6e829165d71b09b550`  
		Last Modified: Tue, 17 Feb 2026 21:55:26 GMT  
		Size: 784.8 MB (784765440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:15dec1e8c4da3c20147899d1139e71a89e23f20ec9c336275959c60cd3ac61a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60761103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909cf12fab19f06ec4c6305031a28fddb4bdb2f505e6dd041bcd116d630422f4`

```dockerfile
```

-	Layers:
	-	`sha256:d82a0845919bcfb8dd34f41e681ea13c14b6c107a5328896d2eba075d3837a1b`  
		Last Modified: Tue, 17 Feb 2026 21:55:14 GMT  
		Size: 60.8 MB (60751752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a4b33f28b99423ba94d636d48bb079cc4f6f733418cc852f68f1c0f21a268ac`  
		Last Modified: Tue, 17 Feb 2026 21:55:11 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ba057f2b9047d10eddf26a5644878e87b2230a07f5b7390634aefec782d96948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **985.4 MB (985445837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c5a8b7ca0950611f2b6ac14d4418fe70b141100460122e3161e2a793eb0421`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:29:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:27 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:13 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:13 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Feb 2026 20:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:13 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:30:00 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:53:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8f486837e1c7893b0d997d722c0b3124671ec83248346e7893f0ff21e8c276`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 684.1 KB (684090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed93d611be098da8ea0b2858e9f03622a1e3e5c8f43f2eeb97f878f6859c5f06`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 6.8 MB (6762611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ec439fca92fb8631158e3e3796842e521de2575d73ddec227c5a47d83635b6`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 94.3 KB (94269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdd84f029fa4b3abe15699eee427345f63d5c5ae19538d7edf00f2b788dfd5a`  
		Last Modified: Tue, 17 Feb 2026 20:30:45 GMT  
		Size: 116.9 MB (116932881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010f081aefa0ee68f583b4c56ea0ce5cdade0407823a2b92c89b1cd4b84161f`  
		Last Modified: Tue, 17 Feb 2026 20:30:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4448e37013cf9183e38cc9955d643924c43a7498cfc246fcbca68d2cd37ff696`  
		Last Modified: Tue, 17 Feb 2026 21:31:00 GMT  
		Size: 105.6 MB (105600489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5767953e8490b993e411a343f8bcff3b560c0ca2cbfe5175afe92ff040558a79`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 374.4 KB (374408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26ebc39380b97a2003e0ec3a56e4d2013953c1ad0bf4c68d2bc22d7c2a61e80`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c245d1be384cea3eebb42dfd710b8a80c899f2db13badd8d32df1fd718dc4d7a`  
		Last Modified: Tue, 17 Feb 2026 21:30:58 GMT  
		Size: 27.1 MB (27146333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427bf6b6cc768f90af14376514666a34e1726b5cdb30ce2503fa9afe353ed9e1`  
		Last Modified: Tue, 17 Feb 2026 21:56:14 GMT  
		Size: 699.0 MB (698982931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:750cf893050c09301049d9126bdd06b97686bf543468da9d8c577d1829b97249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60691700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e30d478cf9fe0d997c1002d421ac54a2677edefd8ae07927d8a3d0241206325`

```dockerfile
```

-	Layers:
	-	`sha256:f8677181204ff6c354021d415b10ea0fe48ccc47d3010644cc217a5ea35537c7`  
		Last Modified: Tue, 17 Feb 2026 21:55:58 GMT  
		Size: 60.7 MB (60682268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab58feac95b434cc6637c12fa0d38b78b357de8c42bcebbde3b6b782aa647c2`  
		Last Modified: Tue, 17 Feb 2026 21:55:55 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json
