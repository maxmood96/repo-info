## `ros:kilted-ros-core-noble`

```console
$ docker pull ros@sha256:da1f5b694e3d822a4a0eafe449c386971058df34aa2f3df3f0b23a7ea9f9ac76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:16ca259c8b256c79331a241e758f5b0eb8b64fe5a5953ba97e2b499e1c6725b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158053388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5f3dfb8bfbd589e1910cbaaddd8e71937ef9cf96da241049362ab22e3e22fd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:13 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:53 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:53 GMT
ENV ROS_DISTRO=kilted
# Tue, 02 Jun 2026 08:21:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685092803da43ca941292a896dd8f48ce1a8d91790f69c2b1c79155b9a69b145`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 684.1 KB (684100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfe1f8d3291d469cb43e34c42805d2fc2b1c783dcf66f4ee0525af8f9949005`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 6.8 MB (6752403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ad6cfd35f7eb6e09d5e6988027d6d14d4616a251e4b6f7b15d46610e5da6bf`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 94.3 KB (94312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16adb782f56ae8a50f40642754bde93ad1b585f0ec4ad386db098320f795644c`  
		Last Modified: Tue, 02 Jun 2026 08:22:24 GMT  
		Size: 120.8 MB (120789572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd387be3eedd271dde548d6e8d372f2d0df9203a335b5a07277419fd3a25c6f5`  
		Last Modified: Tue, 02 Jun 2026 08:22:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:1efe88ba089cfaa34054428a27aa7b92a4fcf015bb48555e12377f423ee2fe4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18504623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e8eab4cdf2f92c7a58a22c5d48e283779ffac26f110b372020241ab860dfb5`

```dockerfile
```

-	Layers:
	-	`sha256:283e9a91fd543500db6f4166861bcc107ea492e1bbd4447973d5898863669602`  
		Last Modified: Tue, 02 Jun 2026 08:22:22 GMT  
		Size: 18.5 MB (18490003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c346c041e403bac4b96cdd9e50f338d2d089267c98d06d5dd49275bb5da5c9a`  
		Last Modified: Tue, 02 Jun 2026 08:22:20 GMT  
		Size: 14.6 KB (14620 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4ff4f51647af6550b50fd6b2b88f2fb5bc32dffea3c298621c827a09ba784662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151938571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04be7631f6d56364f18a6f673429599154c2d9f5ded653d474fdd416dfdc02fa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:30 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:09 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:09 GMT
ENV ROS_DISTRO=kilted
# Tue, 02 Jun 2026 08:22:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b416145b2d0ffb7ae21a537e749877dcd599e74b4d9f478ff90dc7ca53b9bd61`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 684.2 KB (684232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6875267f1b9da5a58d88bcee0d575c2e293237fb4742314202eabbc1d1df8`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 6.8 MB (6765733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42269c28912bc00b80ac1cd7f69237e55b1853486f06e98f684b3b531cad7572`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 94.4 KB (94402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e07f457aff02417cb213909621dc479df8474c419987ecb0627cd88fd7bc2a6`  
		Last Modified: Tue, 02 Jun 2026 08:22:40 GMT  
		Size: 115.5 MB (115517604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930c855c40a83380b5b946026099a869c99e32021af8b48e3604c5218a4e9c70`  
		Last Modified: Tue, 02 Jun 2026 08:22:38 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:33479e56baf77ae896f4dcb0e85f121257d5d4eb1c6b3c8a38b98b9974250f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18478759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5675d24016197ece0e28f5846899340eea58c5c55467715f09076f1da44f34f0`

```dockerfile
```

-	Layers:
	-	`sha256:c37182ae41b7488ef98ac163d48a495daa33583e2794a7da3c365118057188d0`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 18.5 MB (18464014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb28c3002411c873a47ce179ea222358d467c82e4938378f47d5590a356f8869`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 14.7 KB (14745 bytes)  
		MIME: application/vnd.in-toto+json
