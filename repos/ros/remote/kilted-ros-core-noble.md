## `ros:kilted-ros-core-noble`

```console
$ docker pull ros@sha256:62a7ba27a48159e00d0e94661e216820810b5b15adb5d8e757f8ed79d96f1d05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:e50eee05e9060c826384bbdd9a82cc75bcd61ee8e5e77e1eaff72f25b08e507c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158198892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb045e003cdd6c6eb80a9052069c7c04b15e78a027a3b45541d54f292d73b4e3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:35 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:13 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:13 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:13 GMT
ENV ROS_DISTRO=kilted
# Mon, 11 May 2026 19:01:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:13 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203aa6346a00710093073ecb851e68546fe7d5c7a63cadd967ed2e0aa14710a3`  
		Last Modified: Mon, 11 May 2026 19:01:39 GMT  
		Size: 684.0 KB (683966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8297d1086b1f98cc9287380fd3692f52255afda0cdc36d3f71de8384e801f5c6`  
		Last Modified: Mon, 11 May 2026 19:01:40 GMT  
		Size: 6.8 MB (6752218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d4ff6313d42e457ed69085fdbdc948df6fb09eda1bce0ed0adc882aca17571`  
		Last Modified: Mon, 11 May 2026 19:01:39 GMT  
		Size: 94.2 KB (94167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83cec8ec35503c52817d061b1414b615de2561b55cb85f2e547c2a4f2498d16`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 120.9 MB (120935367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cbfd4d642fd8b6e0afa60c8511d6c0bc8eb8471fac315e352391383debe6f0`  
		Last Modified: Mon, 11 May 2026 19:01:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:174363aec632d507841cef9828cf98206efafe204f4159bf746f12f84520093c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18504606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50022f477cd3c8403c62e076f0821ab59e625d81980883f360abd050a76a2028`

```dockerfile
```

-	Layers:
	-	`sha256:24492611cd6397b462ea33a8224e6905f480fda5050ef5488fdef33e2ecdf50d`  
		Last Modified: Mon, 11 May 2026 19:01:40 GMT  
		Size: 18.5 MB (18489985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acc1721156701d2e894171b230c9ca05a79ff6274a7725616a309679149026e5`  
		Last Modified: Mon, 11 May 2026 19:01:39 GMT  
		Size: 14.6 KB (14621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8eea9a303d9e1ca63b81ab1b2e7ae8bf38f4589ca648230485599410ef614f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152081101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f802896a33854f12df469b46459247fef5e52ba9086aca664d48344f12abcc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:47 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:08 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:53 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:53 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:53 GMT
ENV ROS_DISTRO=kilted
# Mon, 11 May 2026 19:01:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc10796365a045f536d89d2fac057e52b1f2ac4ded2cd70e983c8d188e980099`  
		Last Modified: Mon, 11 May 2026 19:02:21 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cc3dfbf9593cf69afba801c78df1d39513c204943247037d87b6ffc686f2bd`  
		Last Modified: Mon, 11 May 2026 19:02:22 GMT  
		Size: 6.8 MB (6765719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0325aca0beeecd063d5b36f9d2b79c49f8b5285d68089393904bb78725a415c6`  
		Last Modified: Mon, 11 May 2026 19:02:21 GMT  
		Size: 94.4 KB (94387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03683ac42ce0d6085689c7560dccd52e485e8811e595a23298003750fed62592`  
		Last Modified: Mon, 11 May 2026 19:02:25 GMT  
		Size: 115.7 MB (115660823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0310fb8d7ab59c87909b9450d1df5d071d4e1796dd9aff7a3039b45a8807780b`  
		Last Modified: Mon, 11 May 2026 19:02:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:e3154051f38f23e86adad4d93bb0643e30818ad1502e96cf25f13ed2e323e546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18478742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2570de1c3e52fb0cfb6ad1223ea7cc5be34529ce7a973c7e1ff50f7199a982d5`

```dockerfile
```

-	Layers:
	-	`sha256:a67ef78cc77fe23e1b505b3ca3c07ceef240ac57ce65e8363a2a9abd297e34ff`  
		Last Modified: Mon, 11 May 2026 19:02:22 GMT  
		Size: 18.5 MB (18463996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513690a7783078c92f117ad75129d56de5f064b0a925f8319c613f72c6c031cf`  
		Last Modified: Mon, 11 May 2026 19:02:21 GMT  
		Size: 14.7 KB (14746 bytes)  
		MIME: application/vnd.in-toto+json
