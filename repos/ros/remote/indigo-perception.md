## `ros:indigo-perception`

```console
$ docker pull ros@sha256:ee6e17dbee97096a306d74a04a90c611cf712f1b176b1ed4b8104d573ef0681d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown

### `ros:indigo-perception` - linux; amd64

```console
$ docker pull ros@sha256:7f7985846051f92533db143814bf38f8a8f192f4e67633e5875b4aac843c2067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **550.2 MB (550158171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef71fc05308d46cbbab789b0dfd4a2b7c041577bffdd760c6d42d36476b0acf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Apr 2018 23:59:42 GMT
ADD file:276b5d943a4d284f8a7b249176a31f93d95e852480c2b851de287e53ff622bba in / 
# Thu, 26 Apr 2018 23:59:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 26 Apr 2018 23:59:42 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 26 Apr 2018 23:59:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 26 Apr 2018 23:59:42 GMT
CMD ["/bin/bash"]
# Thu, 26 Apr 2018 23:59:42 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:59:42 GMT
RUN echo "deb http://snapshots.ros.org/indigo/final/ubuntu trusty main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Thu, 26 Apr 2018 23:59:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Thu, 26 Apr 2018 23:59:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:59:42 GMT
ENV LANG=C.UTF-8
# Thu, 26 Apr 2018 23:59:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 26 Apr 2018 23:59:42 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Thu, 26 Apr 2018 23:59:42 GMT
ENV ROS_DISTRO=indigo
# Thu, 26 Apr 2018 23:59:42 GMT
RUN apt-get update && apt-get install -y     ros-indigo-ros-core=1.1.6-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:59:42 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 26 Apr 2018 23:59:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 26 Apr 2018 23:59:42 GMT
CMD ["bash"]
# Thu, 26 Apr 2018 23:59:42 GMT
RUN apt-get update && apt-get install -y     ros-indigo-ros-base=1.1.6-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:59:42 GMT
RUN apt-get update && apt-get install -y     ros-indigo-perception=1.1.6-0*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2e6e20c8e2e69fa5c3fcc310f419975cef5fbeb6f7f2fe1374071141281b6a06`  
		Last Modified: Fri, 13 Dec 2024 13:52:03 GMT  
		Size: 70.7 MB (70691577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0551a797c01db074ab0233ceb567e66b8ebdcb9de9a2e7baa36d57dfbca463a3`  
		Last Modified: Fri, 13 Dec 2024 14:33:56 GMT  
		Size: 72.7 KB (72664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512123a864da5e2a62949e65b67106292c5c704eff90cac2b949fc8d7ac1e58e`  
		Last Modified: Fri, 13 Dec 2024 13:28:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5aebcfad19ca429757c3e9e33e13cd202e1a9b5bd4a88a247e97e864dbc5ea`  
		Last Modified: Fri, 06 Jun 2025 22:50:35 GMT  
		Size: 14.0 MB (13999491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf966c9e4a21d11472c477852399d46e5d3271473caea3fb2bb5aa94faf291fd`  
		Last Modified: Fri, 06 Jun 2025 22:50:35 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f621077a1e29b4faedc75aeaf0a8a648102b0875ebab656b2e3e7a2b08726eb`  
		Last Modified: Fri, 06 Jun 2025 22:50:35 GMT  
		Size: 15.7 KB (15689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a921a880c1f080966c4e2608b7b368edaab025dcc3147367039270208a19335`  
		Last Modified: Fri, 06 Jun 2025 22:50:37 GMT  
		Size: 30.9 MB (30903890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80de1b0cd873740b71bb81884425c02295329124310e30df7d2de3d6b5100174`  
		Last Modified: Fri, 06 Jun 2025 22:50:37 GMT  
		Size: 1.9 MB (1907616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db15e1359a717eb3d0d757f27c753f8bc0bf13540f4d27e1739519769fc5880`  
		Last Modified: Fri, 06 Jun 2025 23:07:36 GMT  
		Size: 149.5 MB (149533670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5957640ad151f4165dfcde4c0b4fb8e9b288ea790956b366caae5e98cfd354`  
		Last Modified: Fri, 06 Jun 2025 22:49:43 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae9c4870418bcb2a5517b21446569e2c0b4a8f055d17088a90754dada06219b`  
		Last Modified: Sat, 07 Jun 2025 00:07:39 GMT  
		Size: 46.8 MB (46779770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d1ccdc5fcf2e1c349917d409fd21b658d9f942242383dbda2c499a02618f8c`  
		Last Modified: Sat, 07 Jun 2025 00:10:11 GMT  
		Size: 236.3 MB (236253184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:indigo-perception` - unknown; unknown

```console
$ docker pull ros@sha256:47046261d67ca34db6e08b9832a5e8da6cb6eea190106c15847361eb025a5169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46799181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219880f650eaf01297304438dc0b6d951904851619f011747b7c32c6ec861658`

```dockerfile
```

-	Layers:
	-	`sha256:bf34510c888e2768553c83f2c55e2f6851076583a2791d581c54efc3da045607`  
		Last Modified: Sat, 07 Jun 2025 01:20:12 GMT  
		Size: 46.8 MB (46789540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddc761e66bb6957a152b8572fd20384f0328b1ebcd43c5dcee02195240ae723c`  
		Last Modified: Sat, 07 Jun 2025 01:20:13 GMT  
		Size: 9.6 KB (9641 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:indigo-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:f4f910dddd868986498809c8f9992e6b6a88e4041f52ab590849d3ccc8c7f318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **496.7 MB (496735169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7b906d7c6d9745d0a5f39c4ed4503f8698fd06cc28de510307382024bd231d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Apr 2018 23:59:42 GMT
ADD file:e9d55e059869915743a8ca8e64582d23c48fe7e90e439daccd56d3e08e8673b4 in / 
# Thu, 26 Apr 2018 23:59:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 26 Apr 2018 23:59:42 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 26 Apr 2018 23:59:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 26 Apr 2018 23:59:42 GMT
CMD ["/bin/bash"]
# Thu, 26 Apr 2018 23:59:42 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:59:42 GMT
RUN echo "deb http://snapshots.ros.org/indigo/final/ubuntu trusty main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Thu, 26 Apr 2018 23:59:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Thu, 26 Apr 2018 23:59:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:59:42 GMT
ENV LANG=C.UTF-8
# Thu, 26 Apr 2018 23:59:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 26 Apr 2018 23:59:42 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Thu, 26 Apr 2018 23:59:42 GMT
ENV ROS_DISTRO=indigo
# Thu, 26 Apr 2018 23:59:42 GMT
RUN apt-get update && apt-get install -y     ros-indigo-ros-core=1.1.6-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:59:42 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 26 Apr 2018 23:59:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 26 Apr 2018 23:59:42 GMT
CMD ["bash"]
# Thu, 26 Apr 2018 23:59:42 GMT
RUN apt-get update && apt-get install -y     ros-indigo-ros-base=1.1.6-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:59:42 GMT
RUN apt-get update && apt-get install -y     ros-indigo-perception=1.1.6-0*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0db3a87a3d7959895fd860c8b924980adda6e77f5d315b6676a4ac0e12518978`  
		Last Modified: Tue, 14 Jan 2025 21:10:21 GMT  
		Size: 64.6 MB (64624015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a31831ce9fd9e38ad9d926286efdb85e400dc823da723d72cc676869c295fb0`  
		Last Modified: Sat, 14 Dec 2024 10:55:47 GMT  
		Size: 76.8 KB (76775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66373b79ee1bedb2a2bf237fb2a717660559ee8e3fec0aae52d9797c2b32b27c`  
		Last Modified: Tue, 14 Jan 2025 21:05:11 GMT  
		Size: 162.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca3ba35474a2e7add4548570538f01ba4e19ba476ef013e6894b61ee78fc57f`  
		Last Modified: Fri, 06 Jun 2025 22:52:08 GMT  
		Size: 12.4 MB (12355346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfaf8cb1603a4600a99cfa59bf1a8b39b0c7cbcee8439c28d97d711657d925b`  
		Last Modified: Fri, 06 Jun 2025 23:00:40 GMT  
		Size: 236.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c6bb7b47777cab0b903ed1fc357a1bb1eb4be758dbdc940072982539a4821d`  
		Last Modified: Fri, 06 Jun 2025 23:00:43 GMT  
		Size: 15.7 KB (15685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c6136e0a688e95f22d63fa0a498a343896836568fe4ad2bbe7ff9b945e68d2`  
		Last Modified: Fri, 06 Jun 2025 22:52:10 GMT  
		Size: 28.4 MB (28374474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e7b2fa168e2c9998082773d503d896424430d5428950e240b111c2602b8338`  
		Last Modified: Fri, 06 Jun 2025 23:00:48 GMT  
		Size: 1.9 MB (1907476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7281ef55bc653c13d875151fa38e4a640087d53c0f74537bc3c2f2f104b19f`  
		Last Modified: Fri, 06 Jun 2025 22:52:14 GMT  
		Size: 137.2 MB (137156042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00e0e15a4348df79ca586bb772c7eae34188f6cbca3d169abace8fd4407ddb3`  
		Last Modified: Fri, 06 Jun 2025 23:00:53 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee5d20acc66fe2d7a53e525eb7efcf6cd7187f6352a5a776b7e67100cea57e2`  
		Last Modified: Fri, 06 Jun 2025 23:14:02 GMT  
		Size: 40.4 MB (40389239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff868abe42394faeaccffd6621cd14e1582822df2d2fae0c7babfdd212ef9b6`  
		Last Modified: Sat, 07 Jun 2025 00:14:48 GMT  
		Size: 211.8 MB (211835525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:indigo-perception` - unknown; unknown

```console
$ docker pull ros@sha256:e4d157ac5f4b44868f7f3e952b7eeef7bdb64bf58473bc55df532ad725180b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46927656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646297394c55e466a586bf43263c717cedbce304efd87ef7adc9e41cd698882e`

```dockerfile
```

-	Layers:
	-	`sha256:2f73b667c944b00b17cd56b02c068ec391a0528a67868c00bb067f46b853ec04`  
		Last Modified: Sat, 07 Jun 2025 01:21:06 GMT  
		Size: 46.9 MB (46917920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:951936e0475e808d5e7c82c3e04d7bff0c5679f0ffdedad15c4fc8e3d272fc40`  
		Last Modified: Sat, 07 Jun 2025 01:21:07 GMT  
		Size: 9.7 KB (9736 bytes)  
		MIME: application/vnd.in-toto+json
