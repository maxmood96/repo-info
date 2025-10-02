## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:2d39dd63d078d71d0aac36df077abf01b581c5523297b00682ba8826e64fb4f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:c9129ccb9db17d0c557431feaba2dad7a6b7866648f71eaa5c17beaf1a0f64e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185938461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cc10a45a2f45a5e29cd724b6eed85a00753725b7d87dc3ce804d6e48ff1cf5`
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
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
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
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1090f035fbb3dc8bff3a56b524d81b9bff6d998a0a78d6e678503894be117f`  
		Last Modified: Mon, 15 Sep 2025 22:25:40 GMT  
		Size: 683.8 KB (683822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb53581a15804c55072740da9f13b016d0777a3634e94bab7a8a4df208f2b99`  
		Last Modified: Mon, 15 Sep 2025 22:25:40 GMT  
		Size: 6.7 MB (6746858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e479f0117c61cf443355a1be70fb06e043d70a323af3a3542f6940e3ac348b`  
		Last Modified: Mon, 15 Sep 2025 22:25:40 GMT  
		Size: 94.1 KB (94065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee7384dbecd35a0eab61a37ccb1544fe43b6e12df8bb82664f36d7f3c8f17c8`  
		Last Modified: Tue, 16 Sep 2025 01:47:21 GMT  
		Size: 148.7 MB (148690069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e689d29ebbdfe99b51ce27372da98ec09baee25a0bf94f58e7d77b7bb8dda948`  
		Last Modified: Mon, 15 Sep 2025 22:27:00 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:6f20c79e235faf3c1aebca501a979b22e8d26e7c5a786f3efd9d6e8801780bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19370012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640abe85be2af677904ac10258257fb5f8f150fc0ed98ac3da027596766dd2f7`

```dockerfile
```

-	Layers:
	-	`sha256:47eea2a763103dc58ef6c1da26c5151d525e7a46103b07d63ab0dbc7fb44a87b`  
		Last Modified: Tue, 16 Sep 2025 01:18:55 GMT  
		Size: 19.4 MB (19355347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e12d115adad90eacda78db9ef3cfdf919b51712d601182d7e9abf86bd819bb26`  
		Last Modified: Tue, 16 Sep 2025 01:18:57 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0fea03fc7e231ee8bd7a1efa5300ce2cb20bfe4902fb5055af4ec8b26a5ba742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181756348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ae1f48552e0eae7d2d7f9362b12d419cf82a31bf8f453fd9fde74a402ee814`
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
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
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
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c405d746b2e8e7ce7738b1e9aed7c013430edd37997e3df63cc1fcd07921b25d`  
		Last Modified: Thu, 02 Oct 2025 01:33:58 GMT  
		Size: 684.0 KB (683980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da54c7c4310afa97400aea2c20195b24269208ada7d53fe377f2ae01f75d193`  
		Last Modified: Thu, 02 Oct 2025 01:33:59 GMT  
		Size: 9.0 MB (8973936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675b7f405bed0152d1b27d7c72a2312d179c5ea0e0a8f0868682929ad1b0e1cd`  
		Last Modified: Thu, 02 Oct 2025 01:33:58 GMT  
		Size: 94.3 KB (94286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9267757f1f7c27d4e5765e789787f1c7ada31d6efab6d32714301347766dd9e`  
		Last Modified: Thu, 02 Oct 2025 02:27:18 GMT  
		Size: 143.1 MB (143142374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327223fa4a35fd1f26458825de95cb7d529d4954db71112bfb124d0d7dcf04ae`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:fd9b91642f55c1363c8d7c28ac603fe10b3cb749b602c83823a1c15069836562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19346350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f905600348388d8c66672a7f31c19c6a1320fcc1db37dacb81a980e1ebb69caf`

```dockerfile
```

-	Layers:
	-	`sha256:11b1e25fd11d263114736575ebcd74a31523dc516e98c9c1620002ce3cc888e5`  
		Last Modified: Thu, 02 Oct 2025 04:19:05 GMT  
		Size: 19.3 MB (19331560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce833414a630ec5c751c7fcf05e473587c5f5722c04089af3cd568a446021b77`  
		Last Modified: Thu, 02 Oct 2025 04:19:06 GMT  
		Size: 14.8 KB (14790 bytes)  
		MIME: application/vnd.in-toto+json
