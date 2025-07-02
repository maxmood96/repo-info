## `ros:kilted-ros-core-noble`

```console
$ docker pull ros@sha256:1c98e9e217e46d7639dea565310d4d16bfa4344497d462f7eabc986dd540aaed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:66ebd667679864d6c3909cf0118fcf297c1637a5e6ac2130ee7975104f615dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169665930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9f3dd85b3b713e8b2a683701a16f694f940b6d5bb4fef68a3c02b0dc36ae54`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=kilted
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b35fcb4c72e4e1b576c9ad4eeb168575fdcd9f08aa9626159697d08f85f11d`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 683.8 KB (683766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a6ec29354bbb917479948bd512e7a37b5a78b548201e41ab844f5cd27b0a73`  
		Last Modified: Wed, 02 Jul 2025 04:13:15 GMT  
		Size: 6.7 MB (6745540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910605ef6993fba7a0021d6777f55c01af1f52d7fc5fcaaaefba86d25561efe4`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 94.0 KB (94001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47410432c7f18b2fef7279829cc16c86748b308925bb2b928a0d1f18b5a9faf0`  
		Last Modified: Wed, 02 Jul 2025 04:13:19 GMT  
		Size: 132.4 MB (132424061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e057fb5b5c66bd780fcacedc32a3c495cf63933eda6c5c80a9db3df9b484c53`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:0bb9aed55d0d4d06007bb8526d1be866c3f502747b9578c835a9fbeb3af129ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18409046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438abb225bc0c0a13743692b5efc63a9e9c99b84fcae261c26170c2ca4ff69c4`

```dockerfile
```

-	Layers:
	-	`sha256:235dd6d354142de573fa1971dd61c5d979b88f6f3e7bb04760c9d605003e407a`  
		Last Modified: Wed, 02 Jul 2025 07:18:14 GMT  
		Size: 18.4 MB (18394394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:991e63c05a19dbef16187b2618b81fe7733770759fe47e243a06adbe6dab412b`  
		Last Modified: Wed, 02 Jul 2025 07:18:15 GMT  
		Size: 14.7 KB (14652 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:065a8d4842aaa4c1847306c1b451169c37ea0603640b8df06ffb85a0cdb0c770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163508984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f8b581927a631c339f5005390b6410ba687042cd4674304e5fdcbde98b962e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=kilted
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d7528a0593a687366e793711eb7a036e8bf103509785a61913bf5858f83940`  
		Last Modified: Wed, 02 Jul 2025 06:29:33 GMT  
		Size: 127.1 MB (127115953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94731d288701fbac725cde2c66a4c866e7bc2a7e160fbd0f835eb50ae626e5a`  
		Last Modified: Wed, 02 Jul 2025 06:29:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:30f6ebe521d295e5a1f3b0203a711e2f36997c9ddfe68bb1de891faeec4be0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18383177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa94f2e5f0330b5935119de149195befce7f8a8586fc2a5a0d3ce6613b55fa62`

```dockerfile
```

-	Layers:
	-	`sha256:fa72359fc133638f37196f0dbe634d106a73ea75b9339ad16c09717620b9433d`  
		Last Modified: Wed, 02 Jul 2025 07:18:28 GMT  
		Size: 18.4 MB (18368400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25bf6a808bc8cf713ad8b0eb9e55102448fe77c5a4dc07b9edd75a50f636d386`  
		Last Modified: Wed, 02 Jul 2025 07:18:29 GMT  
		Size: 14.8 KB (14777 bytes)  
		MIME: application/vnd.in-toto+json
