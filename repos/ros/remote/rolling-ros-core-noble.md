## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:dc578a780f969c27d4eca6b8a1ce0a482a11034012c9c20d377cfe9cf6b49335
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:a7f8504bc633056c364e3f6d99e5f7ff04e058526bb3d52fb032d3de8a9038a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169652594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a25ace67f66dacdb993f06f9e82370c801912f2d717f0797aa041f2f42b999c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d91b30c7ff9e55f538edeb417f53d4dfb70cc741627149d8b2bc11bb4c6d855`  
		Last Modified: Wed, 02 Jul 2025 04:13:14 GMT  
		Size: 683.8 KB (683757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d440c05e0c6d584917470bf0bc6bf509bcd76b9d9764f2423cb91dfa3e85246d`  
		Last Modified: Wed, 02 Jul 2025 04:13:14 GMT  
		Size: 6.7 MB (6745407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac55c4ebd36770b2e03164d34f70b12811197e63c53da6d33184e1f4971a1d76`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 94.0 KB (93995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa2e7ff368031161d10e8464ade9bd7caecbbe51f61c0c96f634858e2cbbe1c`  
		Last Modified: Wed, 02 Jul 2025 04:13:22 GMT  
		Size: 132.4 MB (132410874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280a3327298c7d6a49febab8e70915f0fc56946fe8468d9b8499c90f344e9f08`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:38a94f29cc7965911c3c9110b3bfa6b8860f25adfbb8508e0ca0a36be1fa37a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18312309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d26f79f09f7b72ab53ad2dd176573fadf7f4af07a13293f9053c42db7fb25af`

```dockerfile
```

-	Layers:
	-	`sha256:03919e412d7535fa4ee1db1b05bb40fe9968c40931079ed9cd9c4bce90277226`  
		Last Modified: Wed, 02 Jul 2025 07:18:33 GMT  
		Size: 18.3 MB (18297644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4065d67af5621efef8c1441e3088e6c0ff7576b9c18ade75fc1655afb22a1e6`  
		Last Modified: Wed, 02 Jul 2025 07:18:33 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:89d9724ded43eb34411b0cb602be12daeb99966c15b1e78f0a01ddd1415aa6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163485397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf4f60c551638a7621157a3ae03b6a5ed9659a983e64a54c2fdb093feed8446`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
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
	-	`sha256:ba80205a32428d80d47d738a520ae436ad7d1aaca7a54a3b8bc5b46b3fefc0b8`  
		Last Modified: Wed, 02 Jul 2025 06:30:50 GMT  
		Size: 127.1 MB (127092365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e416b86f6cb653b375173be75b902fa6b1fd9c4fd4e49908e63a7c2421b648`  
		Last Modified: Wed, 02 Jul 2025 06:30:42 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:88c6acb8d58ecca3506cfcee5e6cc152ddb2f1f3e204489de3042695c69298a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18286440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb45d223c5bec05a4d2da002eb8cb78939d445481b293e3bf3a0771de5b5d02`

```dockerfile
```

-	Layers:
	-	`sha256:a747702af18d6ff618a54d3f2fa07227a4717e1973974421e54f993bad3cd495`  
		Last Modified: Wed, 02 Jul 2025 07:18:46 GMT  
		Size: 18.3 MB (18271650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef2e29e55a91cc90b3d04da26d178dcacdae066c7e9f69cb18b3127fafca20ad`  
		Last Modified: Wed, 02 Jul 2025 07:18:47 GMT  
		Size: 14.8 KB (14790 bytes)  
		MIME: application/vnd.in-toto+json
