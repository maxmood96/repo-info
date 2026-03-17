## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:f166f8843c4e9d0daa6d3d46ddf94e2b9c24d4528ba23b670417c3612b21dcd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:c67e76f473f78c8a586514f42ff90cede4983817642ec2833c0c09a1c8a4811e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159141469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986e2984e1a898f636dd2836fc3b1cd12099e47fde1abb8828b4dee22e5674ad`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:19:09 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:20:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:20:05 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Mar 2026 02:20:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:20:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee4573c7be9d73705c0bb791e2cc7a3cdf038683b9864c37cacf1e7d37b35f8`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 683.9 KB (683886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2368d690de1e3b7bc830ed3cfcc7712dfbe68a7c08dacb836cbd611c9e4dc41a`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 6.8 MB (6751682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece1eb6223c5724538b469a1a0ab386a04f51a8415716356c2b58e64bfabda59`  
		Last Modified: Tue, 17 Mar 2026 02:20:31 GMT  
		Size: 94.1 KB (94091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c84744087b27b97a38f3a63730cb34997b7bd8897f443bd24cae94191cafc9`  
		Last Modified: Tue, 17 Mar 2026 02:20:34 GMT  
		Size: 121.9 MB (121879621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142b8a2170ee1435217998b618da53396cb6dd965ab36f53083e01c662b6bc00`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:532bc3aa23c4b1159c6e4496316f3f2cb6918232fc735cfcc523649ede27fe33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18342467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef83d24e317e67b9e2a9cf40e66e4e42d481994768ddf70314cf30f230b40e4`

```dockerfile
```

-	Layers:
	-	`sha256:e3d244e35056c2eac3feda388784e8e5707c4390dfdd6de4e16fc712fa71dfde`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 18.3 MB (18327867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4dd1af4adf9c39ca81af616e2012014d0472bdd068360ffd8d5ab8ffcdec2d2`  
		Last Modified: Tue, 17 Mar 2026 02:20:31 GMT  
		Size: 14.6 KB (14600 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ff3ca5af04319ebd01fdc0a8ca87bfc80e364bade419f540a5271ff61ab29b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153151364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5879234065016f688fe3de3e9ab8873ca0b8760662db642fcdf18825577b98`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:24:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:51 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:25:56 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:25:56 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Mar 2026 02:25:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:25:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fea7bb6a53c36da8c8f418e272e9aa6d2f438851fd6321f099a7c8181ee3f3`  
		Last Modified: Tue, 17 Mar 2026 02:26:26 GMT  
		Size: 684.0 KB (684042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd69bb424697dd6812c95d01160609a8beb614b0848e1b22409ce6a4607a3fb`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 6.8 MB (6765012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40e562919faf985671753e63630ed9813bd3e261af2ef9eef2f11771ef790ee`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 94.2 KB (94236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df34e90ecee635227f37e80530183d7ff158f9ee3601907cd9ed66555ff3bc`  
		Last Modified: Tue, 17 Mar 2026 02:26:30 GMT  
		Size: 116.7 MB (116738169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc9ccc54bee1d6b7b4d1660cb215140cbe5a8ddc85458e03d53bc3523406874`  
		Last Modified: Tue, 17 Mar 2026 02:26:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:ce04a2ff107f3e2886980db837743ca52691801f340c3aaf198e409fa4402cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052cdf281590b7e26e9d670d3a4b71dac9d33509d3252d0111bebcaaa5957eb7`

```dockerfile
```

-	Layers:
	-	`sha256:f02552ffdff761db0d91c235be596e2696ffbd6365c9bf49cf84a684b6c132dd`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 18.3 MB (18301873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b45c07c4ba308b8ae3a44ff25fdfd881349ad7298d112796b22c474555444508`  
		Last Modified: Tue, 17 Mar 2026 02:26:26 GMT  
		Size: 14.7 KB (14725 bytes)  
		MIME: application/vnd.in-toto+json
