## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:9a3ad210f7d02295b4d8ac56cec23c254ec53c1d0f620acbea649d15b3ec45b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:da420d243a5f5deec5501a795dcec056be107d4080bac2cc62680fe413736331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.1 MB (186062757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e95bb3ab43d416620b526087706fea37c9724a7ad23d2c39aaf36e61cfce2c2`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2081cac45e5fb7bc52c7bf496d2ccc3433f84dd8702adc9fa84d467cc2be5543`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fb1361c757ec00d31a8c6c88058fd62b23da12af4290edf2d3b2c636f6da5a`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 6.7 MB (6746865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4540fb962b4d5de83708d3245134aac24f8adcb8d8457e317648dfe877db60`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 94.1 KB (94146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eebe16a8832263871186c0dda7eaada9cdcfd4f1a4bcc90feccdb47acfff940`  
		Last Modified: Thu, 09 Oct 2025 22:19:37 GMT  
		Size: 148.8 MB (148814487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cda935e56c9a4a7f7f77e60fc31b89aa8dc68da689983df8cab450bf7bace1b`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:583945997ea59965ad3f4c7af3755f49f3658da3a092fb6c7fa0256b5cce262a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19372017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde41f672c26b2756bcd8b10a33e18c6578776958d5d196d11efa808359a758d`

```dockerfile
```

-	Layers:
	-	`sha256:68c6611438f216e71285b4641824919748c76887cd70a29dc14cdb6c0499bea8`  
		Last Modified: Fri, 10 Oct 2025 01:17:51 GMT  
		Size: 19.4 MB (19357356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84946b9639aa950d309fda6bbfb20d1060f026e4f1e503028ec8f54814f3f48c`  
		Last Modified: Fri, 10 Oct 2025 01:17:52 GMT  
		Size: 14.7 KB (14661 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:34933f25fb92bffb2a6fbf696e48dc327811da2099ac14a6873c9594b44aa9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179543247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaf1df2b73e2d423b608f0b5d4763dcb58c0dd9e4673b7c64ecf64241947cf1`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea461ae627ab7b7cd6d4b25cdf53fffafc54e65b4ff6ff3a02d3d49b91d96071`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 684.2 KB (684173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a21bae08cf45f3689ecd30ecc6446aae60082c47632facd058cb8cd91a6915`  
		Last Modified: Thu, 09 Oct 2025 21:26:01 GMT  
		Size: 6.8 MB (6760158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28eb69984a6abb2f7a2c8c70a49497dbdac46d19f02c4ba45bfb8e65d1b52c7b`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 94.4 KB (94418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14560a455baad8eacfe612b059e56e9c5ca08dec61a49e2ca1d556759a08beea`  
		Last Modified: Thu, 09 Oct 2025 22:19:37 GMT  
		Size: 143.1 MB (143142590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc9bd3503415fa5eb2be4bb24bbf854e74951b39a17b36da6a34665776ee9ce`  
		Last Modified: Thu, 09 Oct 2025 22:19:27 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:ec7566968ec0b38f9fcd664c0a76788d6355570ff6a025ef3c3814c9d4a5f4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19346350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09fc1092b2dacdfd90aa9e7fc9dc2a390728b7adb66b4b6d0d246c3a7d349f6`

```dockerfile
```

-	Layers:
	-	`sha256:ba1feeaa24aa0edb1e0207d146fbf98ed07cf1c172df7832f9f75b0a2ec01b20`  
		Last Modified: Fri, 10 Oct 2025 01:18:08 GMT  
		Size: 19.3 MB (19331560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d077e9693178dac3d582e39314dfbd2bb0b43132683826bd3a3ef92708f84731`  
		Last Modified: Fri, 10 Oct 2025 01:18:09 GMT  
		Size: 14.8 KB (14790 bytes)  
		MIME: application/vnd.in-toto+json
