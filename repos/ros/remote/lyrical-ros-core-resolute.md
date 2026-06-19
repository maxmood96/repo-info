## `ros:lyrical-ros-core-resolute`

```console
$ docker pull ros@sha256:35cd26774677a7d16d52ddf951945ec39249620a230a731867fbc1b2c5528a81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:lyrical-ros-core-resolute` - linux; amd64

```console
$ docker pull ros@sha256:b284cd8ad0e2fdbae28bc8b32763bcc51fa1bfa8d30dffa6907cac4c20e0a02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188678485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5896945d08856430f18c0e7592f41d0d68b18f3240bf6fd77bda4bb71cf6c7c0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.9106.tar --tag 26.04
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-10T03:30:57.931695+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-10T03:30:57.931695+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.control_data.9106.tar
# Fri, 19 Jun 2026 01:11:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:11:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:12:05 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:12:50 GMT
ENV LANG=C.UTF-8
# Fri, 19 Jun 2026 01:12:50 GMT
ENV LC_ALL=C.UTF-8
# Fri, 19 Jun 2026 01:12:50 GMT
ENV ROS_DISTRO=lyrical
# Fri, 19 Jun 2026 01:12:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:12:50 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 19 Jun 2026 01:12:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 19 Jun 2026 01:12:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:81e2f2053c8fa702b6863110b55c09e67f6adeb78b4672745958c4d8b3d056c5`  
		Last Modified: Wed, 10 Jun 2026 08:00:11 GMT  
		Size: 41.6 MB (41562239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f56e4c7f2f2a1415c59803638274d488a73b61a8e1f9cbd9cb280327e8d21e`  
		Last Modified: Wed, 10 Jun 2026 08:00:15 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b1770788335db7604bba0ceb7a41f3cc6c19bbd36127093ac28bace3e00d7`  
		Last Modified: Fri, 19 Jun 2026 01:13:32 GMT  
		Size: 740.8 KB (740786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e9c2cfcc02849b9506d2d29cb96f6ee38f7aebaf50ab1dc83d009eb71aabc`  
		Last Modified: Fri, 19 Jun 2026 01:13:33 GMT  
		Size: 9.8 MB (9784527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7de4965a0ddc323590e6e47b9a1c7c8543b5f4b15cbf6f8cb37582b4518e54a`  
		Last Modified: Fri, 19 Jun 2026 01:13:32 GMT  
		Size: 89.9 KB (89872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca11c3384c15abaac0e22d6c4ac49a8170e954811534a42084f875a7cf0e80f`  
		Last Modified: Fri, 19 Jun 2026 01:13:36 GMT  
		Size: 136.5 MB (136500477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9fc928349304d575f19e26e4713c0e9ab4159bb13cefa8129dfb1c2abe8c9`  
		Last Modified: Fri, 19 Jun 2026 01:13:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-core-resolute` - unknown; unknown

```console
$ docker pull ros@sha256:90772d8f5ad2144b3fd5499450aef23a8660776d73b8b19cea04fe1651c939bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22743715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e522b78fef8fb25982c60655ba79d5417bce136c92ebf23b45b6a4d34217a4a8`

```dockerfile
```

-	Layers:
	-	`sha256:1b42c20d4c4fa30bb56ce45aed546a5a99637193ba5bba1b55abf2a01929418f`  
		Last Modified: Fri, 19 Jun 2026 01:13:34 GMT  
		Size: 22.7 MB (22728132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64aa8640d790d8ad8db5e3d7c98d44f716d6b4b4143b3c9ec0b11c786d023141`  
		Last Modified: Fri, 19 Jun 2026 01:13:32 GMT  
		Size: 15.6 KB (15583 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lyrical-ros-core-resolute` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:04207016a6ef92ae044c153be5feef75fb6ad5b50f248b174250aacc2b6718d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.1 MB (181062230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab98f50882aebd1ebd543911a236c82fc8cb6288ca9dd6a353b903910e62f6e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 03:33:02 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.9196.tar --tag 26.04
# Wed, 10 Jun 2026 03:33:02 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-10T03:33:03.035505+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-10T03:33:03.035505+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.control_data.9196.tar
# Fri, 19 Jun 2026 01:11:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:11:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:11:57 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:12:55 GMT
ENV LANG=C.UTF-8
# Fri, 19 Jun 2026 01:12:55 GMT
ENV LC_ALL=C.UTF-8
# Fri, 19 Jun 2026 01:12:55 GMT
ENV ROS_DISTRO=lyrical
# Fri, 19 Jun 2026 01:12:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:12:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 19 Jun 2026 01:12:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 19 Jun 2026 01:12:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c572f291b2a0cc05a1d523f3dda4d3f1992c3e480debf2e1bc9278aeab115625`  
		Last Modified: Wed, 10 Jun 2026 08:00:25 GMT  
		Size: 40.7 MB (40709186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dda33820b52cf93fd5ff3808c770af252cf0565784b42e52e3dd74e2ebf5b2`  
		Last Modified: Wed, 10 Jun 2026 08:00:29 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4986530f0d3c75ff7820390034f5d3e027407a16c974996b5ded332599d708`  
		Last Modified: Fri, 19 Jun 2026 01:13:34 GMT  
		Size: 740.9 KB (740883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65791f49907d0570d76708a6b7fff49950ae25a376454d38f6777a932bacdfb`  
		Last Modified: Fri, 19 Jun 2026 01:13:35 GMT  
		Size: 9.6 MB (9605840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0681652efa697f65008a0c4209e2155b9e5cf57e320f77ceba5d9443b4cbd283`  
		Last Modified: Fri, 19 Jun 2026 01:13:34 GMT  
		Size: 90.0 KB (89997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b374f8a21b565bdf721c78327461dd298e6749b9b13b05d9f6cabfb073f7bc`  
		Last Modified: Fri, 19 Jun 2026 01:13:37 GMT  
		Size: 129.9 MB (129915744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da7d04141ffff77c744942b698c8f9e8a3641e745c138843a6922858ad57b69`  
		Last Modified: Fri, 19 Jun 2026 01:13:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-core-resolute` - unknown; unknown

```console
$ docker pull ros@sha256:6c584cb629c967825549a27f4bf7796a017f86f36d060821e08ca9e2861e2837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22716532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06e5e7c60935235d68affcba56428c89dfbbfb17c0560e188c8501a30b67112`

```dockerfile
```

-	Layers:
	-	`sha256:50cb1dd67369a2a06012835610c6f712223ecc272a3c36f568bb50701aafcf7a`  
		Last Modified: Fri, 19 Jun 2026 01:13:35 GMT  
		Size: 22.7 MB (22700824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:593bef670fc1f1f878df6670a546fec072d19ffe49f9796464d07b1941099d0e`  
		Last Modified: Fri, 19 Jun 2026 01:13:34 GMT  
		Size: 15.7 KB (15708 bytes)  
		MIME: application/vnd.in-toto+json
