## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:83ffbe8efc6b37f20e7cb4a4af0c9ec556f5222eb3eff0adc687ac2552b85589
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:abaf0d5b1c4272b021f9c12f23e267d1d7740c9a0716f74b6fd1c0b53ebaaabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157676277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b20c925c68bf455766410e82359ba652d4ffdec1b1abd553cbe062f8776a838`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:42 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:27 GMT
ENV ROS_DISTRO=jazzy
# Tue, 07 Apr 2026 02:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:27 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3f2df0147e83f87e8e0773aa75602bee1eb50ceec4c9f515f2f1182b82bcf9`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 684.1 KB (684098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d75d23a6c680dfa13a647dd3cf5db5f8ae9f87a17e3efb6e695fe061f9f6260`  
		Last Modified: Tue, 07 Apr 2026 02:28:56 GMT  
		Size: 6.8 MB (6751855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986f07e48752367934b73ae08576189a8e277ac5f37c4519c1f39ca5870b044e`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 94.3 KB (94253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5519a86acbf1f18e15faa4bf0be57e2da1e65732c6dbfbac0d9fb0ac44576a`  
		Last Modified: Tue, 07 Apr 2026 02:28:58 GMT  
		Size: 120.4 MB (120412417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9371cc9eed49f9903f8c0ebfb943d0dfef56e463785c84800dd55fbd6f9b40e3`  
		Last Modified: Tue, 07 Apr 2026 02:28:57 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:934253c51a14ba5879aa9f8c7795d888aaf31af4894ea8f93dd889dac2c49181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18342467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cdbd951b91babbb3678eb3ab6a84b8b41d96cc5ee7cc4851291ea3c1e661fce`

```dockerfile
```

-	Layers:
	-	`sha256:f4e38c3dec79902d1841ee4dc073b27d46479d2a4da84d721a9c6ed34219418f`  
		Last Modified: Tue, 07 Apr 2026 02:28:56 GMT  
		Size: 18.3 MB (18327867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c830ea8df1cff2451c7a44f9a286358a89eb9cb9bd0208dfe0b6487f22798c59`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 14.6 KB (14600 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0a1cc042e1611d8f2b9ecb7be39ba51715d33a1e9aa29d7dc38f8e9cd75ae9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151625197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf163ac9fa79261e25774d31c542e875759bcc789f9d7438c5e5e7e2174d3c9e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:32:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:45 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:33:45 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:33:45 GMT
ENV ROS_DISTRO=jazzy
# Tue, 07 Apr 2026 02:33:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:46 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:33:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:33:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d31541b1d8d1b3d218fba43000cb12270f551607798e615c32f5c659c019fb5`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 684.2 KB (684202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9db22f2cce3a01e224a54fd88e4b34db843b7b5ea6da1c036bd2b9ec317262c`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 6.8 MB (6765111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdc4a8210e22651b45d0b1d6ece27755ec3e5b2e07d4b23d461b295d2ba8f30`  
		Last Modified: Tue, 07 Apr 2026 02:34:15 GMT  
		Size: 94.3 KB (94328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21236c0dfc681ff5d94fac0319bd28d98dbc58bbfb85c9bec0d0e00c04cce8b`  
		Last Modified: Tue, 07 Apr 2026 02:34:19 GMT  
		Size: 115.2 MB (115207286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66d3a43b9d78c7f272dd8156356f6842d6031b8c267e016defaf96c1b7cb592`  
		Last Modified: Tue, 07 Apr 2026 02:34:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:6e1ea3944a0b3fb1c5be59ca8085fa1f155ff7014b89ae7a954efb8cf23635d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068cbb6a86aba99e6b013dac98bd091c904a230f8a73457fe47dd863bef88179`

```dockerfile
```

-	Layers:
	-	`sha256:4debb5b556b74709b6e1a5210eaab7b97136b7f646b396cb17422ec68be84f33`  
		Last Modified: Tue, 07 Apr 2026 02:34:17 GMT  
		Size: 18.3 MB (18301873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3a88731848c1ea876f483f7a4111728ed24ba7df599cce5e60df0cb2aeba403`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 14.7 KB (14725 bytes)  
		MIME: application/vnd.in-toto+json
