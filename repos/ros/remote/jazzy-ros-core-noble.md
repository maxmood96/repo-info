## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:467a18374bb776485a1720fc68400b5ed1bac94defd59064e881f3f05f1631c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:c420ad6abf1e51f3fdf82a69e107601c4a9e0ef4433fb446cb0bcd829c2cc3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157370334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2944457b1a8ed0d61ede200277c61c7d8cee537cf0efebb74d5af34807313e1c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:35:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:36:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:36:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7599b009ea097aa778e0d1ff97f7ab0dad2381f4e6348b7885090cd5544bcc29`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 683.9 KB (683894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a34f0fc738d411b401c35a9622d233b029551d8ab2d349b1e7f7dd0a97936`  
		Last Modified: Thu, 13 Nov 2025 23:36:52 GMT  
		Size: 6.7 MB (6747169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f1e1be724939fb6a48ae8947ce67eb644f63e7eef7a28111f530d95e79a28`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130f554dc5131ca30bb3cca2803ec4a2d298833d60d8ffabe7a3cb4afea71c9`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 120.1 MB (120120282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172928eab2e2b55a426daa21320f98060ea4fd34cd2e8271d708edb2c3c951e3`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:aa6f6782fb8809d1bdc11cc0c39268ca1f92a4361dde84b2144d0f6d757bbe4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18315182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2aec48da4050c47322daa0c5d5b229e2dd930655ef7535791496ec90d58b25`

```dockerfile
```

-	Layers:
	-	`sha256:82536b918e41be2698e73a79e1d27e387ec53ce1fc2c9d80f9147f2deede39c8`  
		Last Modified: Fri, 14 Nov 2025 02:18:29 GMT  
		Size: 18.3 MB (18300584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dedbc50bfebc9bcdaa2e2ffde4d36995eea034731102d1d2c38550bf4ca41bd2`  
		Last Modified: Fri, 14 Nov 2025 02:18:31 GMT  
		Size: 14.6 KB (14598 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f89dfa391a2e2e87e7d9ece24fafd916df612422c1917fcd6db0cf9285e5d139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151307684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281158ddbed9d2ece10045e53849ad1a4014acfeaedd71e8596c82e203918f10`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:34:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:43 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:35:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:35:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9194fd0d9680db2205731529116eadbbbc8027cfff9aceb7487f9c934ad7bc3e`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 684.0 KB (684027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946995b31a424fe6ec0f5dd123c93a8bd1961e062bd418b5b057578e21c5c8bc`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 6.8 MB (6759933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d098b84a269afa0a803df77b1179a40e820a32854f590ab7ff373e8eb5ed5`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 94.2 KB (94197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b736617adc2c17f98e0578d4c8830f36185acd9d89bb802dd5a4a33f37f51cf2`  
		Last Modified: Thu, 13 Nov 2025 23:36:15 GMT  
		Size: 114.9 MB (114907375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6df2d828da46459a8d1d5b906a8ac82b3b7356bebc393ac95f13eb3448931ab`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:598a7a2553b79860a5e1507079e269b151f344672a5245e849678eb8148d808b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18289315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cbd7d7c2a1bec5bfedf88f6bc329b070c59adb966e6f536249e99e6ed7afe6`

```dockerfile
```

-	Layers:
	-	`sha256:76bd73b0f67cbb130195955194720d3f9ae34819328c3d09aa28ff0e95eb181a`  
		Last Modified: Fri, 14 Nov 2025 02:18:45 GMT  
		Size: 18.3 MB (18274590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:042300afc3122faebbb64fad817226bc3428cc12a33bec01b770a4136c6bedeb`  
		Last Modified: Fri, 14 Nov 2025 02:18:46 GMT  
		Size: 14.7 KB (14725 bytes)  
		MIME: application/vnd.in-toto+json
