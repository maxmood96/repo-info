## `ros:lyrical`

```console
$ docker pull ros@sha256:a3063ea4b3cca293c1697a4495e5961860d88a205dda0701f145a0eb252a624a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:lyrical` - linux; amd64

```console
$ docker pull ros@sha256:1a6db26d51251586c2c7206e16a7a8e7f678f8bf481c691aa62597ad93a272e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339630979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b91b18371dc470de8db3602ed01d848fa1bf8dba85894da4eaebc1c5d8bc41`
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
# Fri, 19 Jun 2026 02:14:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 02:14:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 19 Jun 2026 02:14:30 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 19 Jun 2026 02:14:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:1c455c6911eba72cf2336b92d219c6a90919a123e5121e5eb2cee4ffb530e410`  
		Last Modified: Fri, 19 Jun 2026 02:15:44 GMT  
		Size: 124.7 MB (124738757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ff568adefbbf749104149fce980c46cf8ac3e55a08efd058c979cdd22f0bb6`  
		Last Modified: Fri, 19 Jun 2026 02:15:40 GMT  
		Size: 372.9 KB (372868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9423cb87c7b667f632f63fc7640ddf5a745fea70eb774b4afaecbbbd9e4b920`  
		Last Modified: Fri, 19 Jun 2026 02:15:40 GMT  
		Size: 130.8 KB (130820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7213c5ae9089e77ccafbbdb25adf08f162ff74baaff34a595fbe98c59abc80`  
		Last Modified: Fri, 19 Jun 2026 02:15:42 GMT  
		Size: 25.7 MB (25710049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical` - unknown; unknown

```console
$ docker pull ros@sha256:7f4d05278aed57afa6f22f9dce1d9eb5d94ba82c4a9d085f1d0a3b4c83dd7711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29135674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d32dc260929465193d4a40397ab7223d5037fd846ef5b1477427b3b1cb835ef`

```dockerfile
```

-	Layers:
	-	`sha256:ebaa3aec1b267ae44cec9f4df5dd929704bb244de0361c6416a4f9e29cc72f23`  
		Last Modified: Fri, 19 Jun 2026 02:15:42 GMT  
		Size: 29.1 MB (29118226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62c385db96d94474e6a9080175872e17f7b97f68299439a90910d418bc274735`  
		Last Modified: Fri, 19 Jun 2026 02:15:40 GMT  
		Size: 17.4 KB (17448 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lyrical` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:698fba68b227ecdab4bd8bc3afde265f71de5e1a1812537e10ab40be4f8d2b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.4 MB (324377847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a500a45b42ec9258be2166c93661b5f5a67918d1107eda33423035d20dbe190`
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
# Fri, 19 Jun 2026 02:14:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 02:14:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 19 Jun 2026 02:14:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 19 Jun 2026 02:14:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:1757961943f2d6873e218d227b99aec637e34daaebad76220309ce26bd3cd285`  
		Last Modified: Fri, 19 Jun 2026 02:15:37 GMT  
		Size: 118.2 MB (118153811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5a9d8430525b04e0f4e53d32c19982a81767c850bb3155be5118c71fa64dd2`  
		Last Modified: Fri, 19 Jun 2026 02:15:33 GMT  
		Size: 372.9 KB (372871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e27ef8b50545cc0220a341b681b612673a8daaf05a7fc6446eccc66082bfea4`  
		Last Modified: Fri, 19 Jun 2026 02:15:33 GMT  
		Size: 130.9 KB (130851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40aa0e0d2e8defb2f1ef68d61ffa62295cf8a0359d555079fbee419c08149f24`  
		Last Modified: Fri, 19 Jun 2026 02:15:34 GMT  
		Size: 24.7 MB (24658084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical` - unknown; unknown

```console
$ docker pull ros@sha256:0aeef8769f4ece6cfa2ea7ac74e0f1ee0bb51ac083d213f991fd19c3daabd10e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29200454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb944e87b16393cb30ea8dbb12f9f171a396c0d28bbc03a4156f125f21b531b`

```dockerfile
```

-	Layers:
	-	`sha256:ffc446d1622f40dfd3940d7b54c1041b20c9f8abce641444c782e8b17134774c`  
		Last Modified: Fri, 19 Jun 2026 02:15:34 GMT  
		Size: 29.2 MB (29182856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b927a61ac8834b1114aa55db3d2558d4d13ec8e2065a182bb2b010bce83c7b30`  
		Last Modified: Fri, 19 Jun 2026 02:15:33 GMT  
		Size: 17.6 KB (17598 bytes)  
		MIME: application/vnd.in-toto+json
