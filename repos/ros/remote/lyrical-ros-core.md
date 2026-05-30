## `ros:lyrical-ros-core`

```console
$ docker pull ros@sha256:75dca9d8a0a8fbef65d67cc4beedd913b154e4f62a6dbb8011a96a1a85c67b95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:lyrical-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:46c620bed11404b2a3c940e1f8ffb82164d69b9bb73d807cf03dd2d6085e92c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188702043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd335e8262647966eea2855bbcc5856ee851d1c8c9a8b3095ebbac309ba988a2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 17:23:53 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4415.tar --tag 26.04
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4415.tar
# Sat, 30 May 2026 00:27:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:31 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:35 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:28:19 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 00:28:19 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 May 2026 00:28:19 GMT
ENV ROS_DISTRO=lyrical
# Sat, 30 May 2026 00:28:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:28:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 30 May 2026 00:28:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 May 2026 00:28:19 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6f5c5aa4e145204b113f983c003ff8ad6489394294ef95ec030bc94e3daded54`  
		Last Modified: Tue, 21 Apr 2026 18:49:33 GMT  
		Size: 41.6 MB (41554862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c24335ddd46023ff99bd665bd8ea6798464f7bbf501718edcf2eb4696e5f408`  
		Last Modified: Tue, 21 Apr 2026 18:49:35 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a66e0e4ba2827013cfdb6d7d0277845dd90d29cf5be6f6b1a2edb35b35b8f8f`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 740.5 KB (740466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d768bea23ca17d73373bced93b07f016d49dc73083020b677ca88820b6e206`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 9.8 MB (9817877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d56e888694023b5e25084b3279db49e8acf8dd01b333bc892018778ac0b6217`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 89.6 KB (89573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568aec1aaa0eab51b8b82e80be56f21f3b816a67df5322fffb3616f28e0eaa6d`  
		Last Modified: Sat, 30 May 2026 00:29:04 GMT  
		Size: 136.5 MB (136498683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27deaf91b06f9331b9e482842dd053ce65d106daab5a1476638159a380ccdeab`  
		Last Modified: Sat, 30 May 2026 00:29:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:bfd86737278ed7b00f2d49c136b47b865e1dafed688d304d210be5934c67a817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22758310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5fbda6178cad9b3e0702927fdd417b40027436968dd777250dcb33ff8399bd`

```dockerfile
```

-	Layers:
	-	`sha256:4a8b3562cd31d666080fc0f6c3a20525e0cff316849a7a89861f7da54ade44f8`  
		Last Modified: Sat, 30 May 2026 00:29:02 GMT  
		Size: 22.7 MB (22742728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec15194a5fee2b37a82400bbf73144850892484588e5996e0db079a5d23b1a6`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 15.6 KB (15582 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lyrical-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a8b32b5eb80081ed0ab06576b14dd5087c675e79fe3506278d4fa29a33e289f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.1 MB (181094025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2473339221f972c887c1de5d521549a07120a4cc9daee015164848171e9ff6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 15:27:25 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4553.tar --tag 26.04
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4553.tar
# Sat, 30 May 2026 00:26:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:26:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:26:57 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:46 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 00:27:46 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 May 2026 00:27:46 GMT
ENV ROS_DISTRO=lyrical
# Sat, 30 May 2026 00:27:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:47 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 30 May 2026 00:27:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 May 2026 00:27:47 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2113f8d7eb32748b14581824c1b94cea9ed9a08456312a2e94eddd522d01b927`  
		Last Modified: Tue, 21 Apr 2026 18:49:43 GMT  
		Size: 40.7 MB (40728955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7720058461eb4ae40ed203b9874ab3248bd34ffb9948193e99245229fdbd6f`  
		Last Modified: Tue, 21 Apr 2026 18:49:46 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc2ad364c506093b49a14399caae9c415d779931557582d1064c20883556f3a`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 741.2 KB (741165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f72c9d5baed137ff572cc6144d1b1c3ee48d9da3e8ec830a0a2b85445a8bf`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 9.6 MB (9641306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37666b6096b138cbf3a42a8c82ab2e084f00595ad4f69a0d0541a2255a450ce1`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 90.3 KB (90277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44192943d5ae755decbe581424aa597252ca509537720b2177b1dabb1ec588a9`  
		Last Modified: Sat, 30 May 2026 00:28:29 GMT  
		Size: 129.9 MB (129891737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f43a2870356aaff3f0fdef23de031b83b26a6a66afe29f02ed3cdaf6285b0ea`  
		Last Modified: Sat, 30 May 2026 00:28:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:998c7f65355d63555e7d70c1a5ebc5dcd58270b4f24e29d57a5f739218201fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22731128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41276bf6a1c5f1ff3dd0ab9efaf7c720783345bc0fcbf4ba03fc8e10f7c5e876`

```dockerfile
```

-	Layers:
	-	`sha256:7869e9c1067c1a97642f5db8f412b89b4c750d9b63253b854a1421095ea7d423`  
		Last Modified: Sat, 30 May 2026 00:28:27 GMT  
		Size: 22.7 MB (22715420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:931dd2af90ac34cceb907f7a10613789f9856d9302520739272a87a42b20ddf3`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 15.7 KB (15708 bytes)  
		MIME: application/vnd.in-toto+json
