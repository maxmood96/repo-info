## `ros:kilted-ros-core`

```console
$ docker pull ros@sha256:2a5a0f80fb950bcd79720f1f3e3ae91e38487b5ac18ac168e5a5c34c40263215
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:f350c3d4f507a87bfb1fd30642463de061c33438dd8dc43b75e8a4da324ae198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172229902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13c7776c6db86aec9718e0b74f098f733da05df0710da9368fc38093b170b75`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1093e90b494a8cf5c26d88b9121c20432cfed972a3596da60382e67ff19b37ab`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 683.9 KB (683927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc95d893b22a2295a2886c6467a97ee5dade130bea11f8994e4f764607dc781`  
		Last Modified: Thu, 09 Oct 2025 21:24:02 GMT  
		Size: 6.7 MB (6746996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7aee44d69d92942ce7f9b6acc7104f12ee9caef6adadcb1a39d72cfde21076f`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 94.2 KB (94157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ad95cd04f77e0c5e96a8b537442f4b5d8be45febd447202f388d3a44663a30`  
		Last Modified: Thu, 09 Oct 2025 22:19:29 GMT  
		Size: 135.0 MB (134981480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b48f84fffbd5e61ea1d7e61e4143c8c98c1f4a0bff60b9411fd58aa4c63864`  
		Last Modified: Thu, 09 Oct 2025 21:25:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:9692c447c8b825099c0f96f6e365aaf59d03f9520bea79788d79a402f532d498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18414503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638bacd1f7a9b35ee59e98b486fa0b1dcfaf1f41087720db20c112b4659b6148`

```dockerfile
```

-	Layers:
	-	`sha256:9891b8f45133f25976c97df9943ea97919ff5420853d6f8387a250dd82a73aa4`  
		Last Modified: Fri, 10 Oct 2025 01:17:38 GMT  
		Size: 18.4 MB (18399851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc0c206e706d0a968c019d924567c807b85c5061d4776bd641b7d729025ab66e`  
		Last Modified: Fri, 10 Oct 2025 01:17:39 GMT  
		Size: 14.7 KB (14652 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a002c12d96b706ffbc2430ad3d0a8e5562b8507d9cc3f1acc3d7044ad80ffd58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.1 MB (166104217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dce02b7ce5c48a46e237aeede4ccb8dbb113a66f7999ee2fc0303c9e2f716f`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001f2e5bdb9ebc2dd1e4a97e4c4f8f6a4caa1a8d2b8c88779e314bfedf21b5eb`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 684.2 KB (684174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b431df98e5fde48f4218abb39181387c9329df717368142b9f365818c84a2731`  
		Last Modified: Thu, 09 Oct 2025 21:26:01 GMT  
		Size: 6.8 MB (6760140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283f352fd757879170ef433d2bc7b2b87844a7e64a56c215fd7e8bcf52511b33`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 94.4 KB (94397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcf903136d1425abdcfe45e487f28e07cfa1010e029bb0e9ea8ac6096c30939`  
		Last Modified: Thu, 09 Oct 2025 22:19:34 GMT  
		Size: 129.7 MB (129703599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680295d190e67764ff4359841a9d2f64ece12ca1088d22d70f40d69e908a05fc`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:8b2860c1621b703d8ce45eb6fc0e6f79f365f14ba2eabc712ebea7ce14568400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18388634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89b421b8535aba4924b4910e4b2800e3600538d6bb91f2ffe9bcba4b12f4c8`

```dockerfile
```

-	Layers:
	-	`sha256:17a970e5b5e850925606b2669971db1122a3a88e6b420328a58e045438ad354d`  
		Last Modified: Fri, 10 Oct 2025 01:17:56 GMT  
		Size: 18.4 MB (18373857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60eec2f4ecfdb667a440a1de8e5abc0871e69aed85644eca4084504fce0847c8`  
		Last Modified: Fri, 10 Oct 2025 01:17:57 GMT  
		Size: 14.8 KB (14777 bytes)  
		MIME: application/vnd.in-toto+json
