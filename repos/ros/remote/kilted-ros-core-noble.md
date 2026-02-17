## `ros:kilted-ros-core-noble`

```console
$ docker pull ros@sha256:9df9a73dfb4529e331c651c51eb2c5e53d26d38eced642a6176fb8b08bf63ddd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:aa9d0e7a5a0de93b6c9639949b0448387007ac020074a28697d383a19bbbb8e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.5 MB (159507664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a637fac4a1da4fd447c291397705f10770529044ada5c1daa8b62addb3f0e732`
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

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:f3da8efb9a5a6b1f055cb68405604c87d44ea58741eff33da3035c3404990841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18348767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7537f06471990282961fb3916c96d7d41651d8e17cee33f80cc9de626713e22`

```dockerfile
```

-	Layers:
	-	`sha256:28e18b2dc20ebed812c25b487b3ec251072847ab7fcd13a790aa89b38edcbcbe`  
		Last Modified: Tue, 17 Feb 2026 20:31:51 GMT  
		Size: 18.3 MB (18334158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b2ceb9fbb63c9584290a7c001300912a49e2289cf303a9188e2619aa320340`  
		Last Modified: Tue, 17 Feb 2026 20:31:49 GMT  
		Size: 14.6 KB (14609 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3b5278f418762522ab382851cd30051434c89a906a27d52c31c57428507db81e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153339167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10e29ed1dabff989082530269b5cfb6ac7c965601eb7b7f1d58d5d1c5c213e0`
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

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:0d96006a3656489e4fbbc326e2951be49e3259ee934af69813f5cf31f46d4c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18322898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f2be7b312b6953c99ac3fe94e7c7075d10e3725bea4eaef7d60ced53078155`

```dockerfile
```

-	Layers:
	-	`sha256:cff3b0d81aa847b8b80f981ab060fad729b96add29e8c0af818cadfadd604c53`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 18.3 MB (18308164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49f6184b90f992241505423cab8b7277ed17eb36725fc217a0e32c90171abd36`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json
