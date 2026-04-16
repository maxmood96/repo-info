## `ros:kilted-ros-core-noble`

```console
$ docker pull ros@sha256:e98696af83cfd45f97ba9207bca4c7c126a98214411e7bde6d266bfccdc50f42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:3488a7a80106d067cc6c32ee8d1026c267fcd56fdbf0ab172d80216bb9b5e6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158171462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89b6088cc84722ffea57a901a9ad98f7384133340e7141f0700aed1782af5c6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:53:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:12 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:54 GMT
ENV ROS_DISTRO=kilted
# Wed, 15 Apr 2026 20:54:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b1e8c88b55de7bb95fc86629c092b8ee1185957ce194ca3e8c032521218d23`  
		Last Modified: Wed, 15 Apr 2026 20:55:19 GMT  
		Size: 684.0 KB (683970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fe78e730b0bc01704683bee8ea5c7144c34bc29d7f64e8f86e0fd3581c744d`  
		Last Modified: Wed, 15 Apr 2026 20:55:20 GMT  
		Size: 6.8 MB (6751659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05bcb8e9e38af2e16e36258cd57336a7d9f443d029737a994e0cbcde39dc7d8`  
		Last Modified: Wed, 15 Apr 2026 20:55:19 GMT  
		Size: 94.1 KB (94108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a8e25e7760a7f86e056446fe983fc96739a4cbc9010d4e8c16779f7f1ebb51`  
		Last Modified: Wed, 15 Apr 2026 20:55:23 GMT  
		Size: 120.9 MB (120908551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66fff459f77a979cc988155538d6cd842c44afec85e542f5659cee33be6ed7a`  
		Last Modified: Wed, 15 Apr 2026 20:55:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:f8b2359edb08a063032526bdfe786a4b14885a4736c5947bd785e66d6856a706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18503157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea32e6c73c6c625ec0ddf0c75ad0147650b36f36c3ce72f0e78610bdf5229c1`

```dockerfile
```

-	Layers:
	-	`sha256:48ae88e34d7373a715f5f5053b1f4bba51d637a5c47f8625146f6bd6d614fff0`  
		Last Modified: Wed, 15 Apr 2026 20:55:20 GMT  
		Size: 18.5 MB (18488549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:822a402c9fa80c9122edc35b5db34c5754fe7ae0a2aed1d55f79422af9416da1`  
		Last Modified: Wed, 15 Apr 2026 20:55:19 GMT  
		Size: 14.6 KB (14608 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e40ce479b9adc7185209dc8a2420185a27265eca9b4a507d5c657fc7f3c8bb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152052544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e613dfc912c54bd59ee4814483271f481ba23ab404e246f45a16e70fd066c079`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:01:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:03 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:53 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:53 GMT
ENV ROS_DISTRO=kilted
# Wed, 15 Apr 2026 21:02:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f0a2684d9babfb3177690b0c4a2b1ff0db4cf333b9a4f77b7eb9e6f53a0b5b`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 684.2 KB (684199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff337ea7733134af43106880ebb5e900603a2b5e4bd370721d73a7a25a8a3b86`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 6.8 MB (6765008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9c6d8e1bd0a4b9a42f8763d22cd8574e5086ed2804ba50f19de93f76d72e0b`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 94.3 KB (94323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca663cb32814a19e937ea07bd86b12869cbb41a47cc848ddf0559c75b785cfa3`  
		Last Modified: Wed, 15 Apr 2026 21:03:25 GMT  
		Size: 115.6 MB (115633032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb611bb0edd49e965a3a9b4f6c4c6dc8471d483595597dd92e232531e2c6d27`  
		Last Modified: Wed, 15 Apr 2026 21:03:23 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:86e282b8f99fdc46ffbe5f8b6cb5f24b751be8cd5686ee2d5a4e439afafcc13b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18477294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984ef693910bb0c21a914da8fa91e9808e838876e44fb082c3b7218e3ea6a709`

```dockerfile
```

-	Layers:
	-	`sha256:515c5647c5cc991e648b72b6fefa9f61b11b8df09a72b214b9a664bc3069b568`  
		Last Modified: Wed, 15 Apr 2026 21:03:23 GMT  
		Size: 18.5 MB (18462560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41f7042ad15560f90c32f39765cec73a3180aa68d8fd559c7b84da22b33cd37c`  
		Last Modified: Wed, 15 Apr 2026 21:03:21 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json
