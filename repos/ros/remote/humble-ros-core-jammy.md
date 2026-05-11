## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:f17039028bce108afa2d173286a7d920bc515634f48b57b150938c4d0da3a7ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:131aee2f443d09950cc513045c94eb29e46749c22043e88f4eb93ab278a90c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141906957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ad7ca06347be90d4aff2f590b6c53bb989a6e9607f91c084da20d9619ec264`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 18:58:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:06 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.jammy_all.deb     && echo "767884cf4ed03116b9d64438930a832ed854147ae435279a7924dfdf60f94433 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:40 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 18:59:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 18:59:40 GMT
ENV ROS_DISTRO=humble
# Mon, 11 May 2026 18:59:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 18:59:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 18:59:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb80aca26f7323a4c05c7407144dbc29939fc8bed1f0eac2be917fe4a080f7fc`  
		Last Modified: Mon, 11 May 2026 19:00:09 GMT  
		Size: 1.2 MB (1215560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b22082ad8b9356a2dc5b871f9d097cdc16dd83fa3b8a005117663efd30385d5`  
		Last Modified: Mon, 11 May 2026 19:00:09 GMT  
		Size: 6.0 MB (5994781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444e673deaab41171f1d0b885f91abb5c46c069411710bb9875fdff17a5894f9`  
		Last Modified: Mon, 11 May 2026 19:00:09 GMT  
		Size: 97.2 KB (97243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572089fd39981cf3239cc207928f7dacc413065e75c598d50dad560a792da1a7`  
		Last Modified: Mon, 11 May 2026 19:00:12 GMT  
		Size: 104.9 MB (104862679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9278dcb40092814e1a4fdcddd11168813114ed14329d356db0f1c08b80734442`  
		Last Modified: Mon, 11 May 2026 19:00:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:40bd23bc04928571a437762be2c7b05e43025ba3396be806bd3b24d851d31a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17817515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47239fa44d7fc4d23310357a5e86803076c5373c45e9d565ea64744cf4b34770`

```dockerfile
```

-	Layers:
	-	`sha256:41d87f0c86ab547084984ca23bdd6ac2aa309dfa9aab838e3779b124bae87d93`  
		Last Modified: Mon, 11 May 2026 19:00:09 GMT  
		Size: 17.8 MB (17802889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2502ef0cd4c7431676a3e795c1b28e580c7709fd8260646cfa072db720951fe6`  
		Last Modified: Mon, 11 May 2026 19:00:09 GMT  
		Size: 14.6 KB (14626 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a0e852df46b0058e6ba57de2505e5c39d46f6c86e7b5ac4123633485b7dfd232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137485962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4321e7ec51b1249e3ed9629d88a2071c4903b3f41eff92ba1f6db339399292`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 18:58:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:18 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.jammy_all.deb     && echo "767884cf4ed03116b9d64438930a832ed854147ae435279a7924dfdf60f94433 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:58 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 18:59:58 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 18:59:58 GMT
ENV ROS_DISTRO=humble
# Mon, 11 May 2026 18:59:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:58 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 18:59:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 18:59:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21105286df146bcfee570e44f0c2084bab6a1650e301e96c71ea0c5b366164a`  
		Last Modified: Mon, 11 May 2026 19:00:24 GMT  
		Size: 1.2 MB (1215746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c730a6a208f443fefd548a8f3ba5e9897dd637a97eaadc5ad1e721c5327bca`  
		Last Modified: Mon, 11 May 2026 19:00:24 GMT  
		Size: 5.9 MB (5949231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d5c8cf6d70219c353d71b074227d00fbcaff0cd2f7a0778f99b4fc6d0d6819`  
		Last Modified: Mon, 11 May 2026 19:00:24 GMT  
		Size: 97.4 KB (97376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bf0daff854886510375744ab2162a5f99a2a1084da4730c0e0fcf1fa7d49a0`  
		Last Modified: Mon, 11 May 2026 19:00:28 GMT  
		Size: 102.6 MB (102616871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5430748a99c3d3af061e4180d3bb3188e758fa68689641a55b690c235300f66f`  
		Last Modified: Mon, 11 May 2026 19:00:26 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:d2978f3af1a768ddb560529c048fed2d086c1b12a1ba8319b7a6cca54c9c2547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17803985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000919b1ca5e7bedb97e8526a92adc6cec357f20e0361b18671b208f19c528a1`

```dockerfile
```

-	Layers:
	-	`sha256:48c34a82e6a2bb55395118afb9ac12291ae790094149b219f228f616a0238897`  
		Last Modified: Mon, 11 May 2026 19:00:24 GMT  
		Size: 17.8 MB (17789234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c251fd8365b28335a9f2ec12cdec1e6806e8fae36c677db7ad6b32bb623508`  
		Last Modified: Mon, 11 May 2026 19:00:24 GMT  
		Size: 14.8 KB (14751 bytes)  
		MIME: application/vnd.in-toto+json
