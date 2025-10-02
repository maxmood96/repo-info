## `ros:humble-perception`

```console
$ docker pull ros@sha256:b28e43e044e231ed2f13f6d351586191037e6ff4de8dfd49c8bba7c4ef59575b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:cd95809fb5038fd44edf79e271b48038a9f54c803dd057cfab4ada139d4da977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.2 MB (955165950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c38c757f5c9847defc2c884ec0dea713341a46d4c57f4085f9af2de9f437edd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3acafe09bcaac051ef6d1f97c0d2d173c28b505278e8f1e352a4a38b3e6d53`  
		Last Modified: Thu, 02 Oct 2025 05:18:00 GMT  
		Size: 1.2 MB (1214024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb63b1a7685a896ac7f919e64c1bb1c2f836892f3b8d0b2d150496a95cdd84e`  
		Last Modified: Thu, 02 Oct 2025 05:18:03 GMT  
		Size: 6.0 MB (5995057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d979177940451251cb1465ddc2a4d20b9165b080ce72028029a0972462d2687`  
		Last Modified: Thu, 02 Oct 2025 05:17:56 GMT  
		Size: 97.1 KB (97120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79595a0d502923d1f8007afd19da2017254078ed965e44ae4494abeb5ae95275`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 104.6 MB (104600746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8627d2f078576b7acfca765aa3f0dc5295ae62399615969ca25316ff869c80b1`  
		Last Modified: Thu, 02 Oct 2025 05:17:56 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8921fc85add6643dfaca09b6d4648b9a390d9c25a0a7b76a339eddd1abbce10a`  
		Last Modified: Thu, 02 Oct 2025 08:42:30 GMT  
		Size: 98.0 MB (97961155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fff84f73176326d41acddc485f9bb72d1fb4023657107c3be33f1cc35bf9967`  
		Last Modified: Thu, 02 Oct 2025 08:42:23 GMT  
		Size: 374.3 KB (374273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077021ac2104c3764dc0ea75f26afc46bc0ff43df66f57352f9984201ac3b88d`  
		Last Modified: Thu, 02 Oct 2025 08:42:22 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94f36953130fd4527f52aa6fb545f561ac1a6ced8e51eb6bdc3245648a772f9`  
		Last Modified: Thu, 02 Oct 2025 08:42:26 GMT  
		Size: 23.3 MB (23318499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ec12be7f73945dd776113708f0deb24b26153cebc4a2cfbfb92753be821195`  
		Last Modified: Thu, 02 Oct 2025 13:18:33 GMT  
		Size: 692.1 MB (692065609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:3abbef0fd6d5fd5a1af78a6568be69ccde5283c27d7e6c56b0c8ca00d1f66c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58777209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b97d9adebcc2f4b35c1c7f94788fd4d2191fca9d9801f63466c41828f8ed11`

```dockerfile
```

-	Layers:
	-	`sha256:c4dc946f3e88502c233637ff403efcca49da9f493ba42cb19ea6ec5c40d70b3a`  
		Last Modified: Thu, 02 Oct 2025 13:17:21 GMT  
		Size: 58.8 MB (58767814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ad2bd5128e7058c90801145de9f9fa359dfe880c2a2290bb8ca0a4b1f1fd1d1`  
		Last Modified: Thu, 02 Oct 2025 13:17:22 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c3b3b6ff97b4b53dd43e628fafbb647a88f6f51221d42d95c2bdf2223357f6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.6 MB (915609144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a0d501c7ddfa99ac60b138d72d94f81ea235108131d6732a35a4f3f8011ab2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91acf2e35d271b16f5560e89ab696b0b3860e769bdd01a98be8d27f2b303af9b`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 1.2 MB (1214273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc15a8d1c24650e7b013c9200269a76754b2ebe61c4c0c7c702ce9f71ffa1f0`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 5.9 MB (5940017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ee1af528a3785d2b72ab104c943f6ca6d0139eff238112c82bf3a9ddb6d098`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 97.3 KB (97302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1903d03b380fc6eff49a30428f62cd153e71d401b3121f93b65c9b42a9495b`  
		Last Modified: Thu, 02 Oct 2025 01:33:09 GMT  
		Size: 102.3 MB (102341319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff1d9c6fb2a0e50f3f08713eb4a2f3474bd3246332d422e24690b33c09309f4`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ed460bd7610e695293d4aad069edacd2754484b0f55e8dfc4e3a8975b61299`  
		Last Modified: Thu, 02 Oct 2025 03:14:51 GMT  
		Size: 95.5 MB (95536513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee4a893c7ab244785cc16456c334bb289d0f040a1c336fbd113a913a0eb8a33`  
		Last Modified: Thu, 02 Oct 2025 03:14:45 GMT  
		Size: 374.3 KB (374273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e433a4c2230dce1a5c2cd4a3f00afd6ad4255d21ceffab538d491b369a751d`  
		Last Modified: Thu, 02 Oct 2025 03:14:45 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f4bf5c7c27cec9add8df7118cd31c934b55e265db6bb75c5d7da8b912340ad`  
		Last Modified: Thu, 02 Oct 2025 02:28:56 GMT  
		Size: 22.7 MB (22715620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5e2cb20c1dc183518b13ed55eccd22d11d50b212a21d414606337cc6c9dfa8`  
		Last Modified: Thu, 02 Oct 2025 04:21:25 GMT  
		Size: 660.0 MB (660004040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:95b26e59188683835237e4192a1143316b84eaff8fe03e7b9c33c92e1101a8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58761610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd567ee08a59ee70095b9e58ed96d33edd2ddf1154a0ca31f825d9da5e75bd3`

```dockerfile
```

-	Layers:
	-	`sha256:919c156d38ce0596b3d6b68493b917d2213f9ac75124f2e6c45cf24ab74b5e9f`  
		Last Modified: Thu, 02 Oct 2025 04:19:12 GMT  
		Size: 58.8 MB (58752135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a37e5fdd450e9e532057f7bb383c800c970154102b4dabb6d8170b92d8bbb5`  
		Last Modified: Thu, 02 Oct 2025 04:19:13 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
