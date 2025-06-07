## `ros:lunar-ros-core-zesty`

```console
$ docker pull ros@sha256:94f216a6f4eb2ee3d392e82a46ae7511ec6ef8a86134b63003a49454d43a2f05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `ros:lunar-ros-core-zesty` - linux; amd64

```console
$ docker pull ros@sha256:21cd7b31bcc953c464242b933c898bad6f75756c02205b9603d187357fce5ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.0 MB (355022407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5862faab157c8afad7bebaf88836a75f626a29489e2d44d76574bd5bc5d4592`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 14 Dec 2017 21:00:08 GMT
ADD file:796db5dd87a82ef3448e235015cbe46f6e917199753ab9fa0a7fc03d14da91b0 in / 
# Thu, 14 Dec 2017 21:00:09 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 14 Dec 2017 21:00:09 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 14 Dec 2017 21:00:10 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Thu, 14 Dec 2017 21:00:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 14 Dec 2017 21:00:11 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:34 GMT
RUN find /etc/apt/ -name *.list -exec sed -i -e 's/archive.ubuntu.com\|security.ubuntu.com/old-releases.ubuntu.com/g' {} \; # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN echo "deb http://snapshots.ros.org/lunar/final/ubuntu zesty main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV ROS_DISTRO=lunar
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-core=1.3.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c2ca09a1934b951505ecc4d6b2e4ab7f9bf27bcdfb8999d0181deca74daf7683`  
		Last Modified: Sat, 14 Dec 2024 03:46:22 GMT  
		Size: 38.6 MB (38640200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c3619d2153ffdefa4a9c19f15c5d566ce271b397a84537baa9ee45b24178f2`  
		Last Modified: Sat, 14 Dec 2024 03:46:07 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efe07335a049e6afcd757db2d17ba37a12b717eb807acb03ddf3cd756b9fc2a`  
		Last Modified: Sat, 14 Dec 2024 03:46:07 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1bb01b3a3b72463ae8ac5666d57b28f1a21d5256271910ac8df841aa04ecd1`  
		Last Modified: Sat, 14 Dec 2024 05:44:11 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a98c1873995475a895f3d79f405232ef5230076b3f610c949c2e8341743af7`  
		Last Modified: Mon, 16 Dec 2024 03:45:41 GMT  
		Size: 163.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc37efbb469e8561f0c44efd5397dbb3422541bde867c738aa6de98695dddf3`  
		Last Modified: Fri, 06 Jun 2025 23:07:30 GMT  
		Size: 865.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ad09c0d6321127a19542ba1e423fd805f84ca229cce13fe0c1995dbd157a85`  
		Last Modified: Fri, 06 Jun 2025 23:07:30 GMT  
		Size: 5.0 MB (4978299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba92ced2324d9cf3036eb243e51bd1408bf93b87dbe3b63ede92123616361c89`  
		Last Modified: Fri, 06 Jun 2025 23:07:29 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede91a3b48718bd23660674457dff97823e2ec7ec2ab575bef81221f4c9dcfc2`  
		Last Modified: Fri, 06 Jun 2025 23:07:28 GMT  
		Size: 4.0 KB (3986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9346f16948021f99c4c9bf898a429461eb3749fa121fd3ae088db00909afcf7`  
		Last Modified: Fri, 06 Jun 2025 23:07:32 GMT  
		Size: 57.4 MB (57390018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b1c0f8e08d5581804b5706f222b98d5a30e4a047b476037f3d451544fa5040`  
		Last Modified: Fri, 06 Jun 2025 23:07:28 GMT  
		Size: 1.9 MB (1907616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bc69ede28004315ef4dacaf467657d528bc974a62e4f0f4048fb80b4abd84a`  
		Last Modified: Fri, 06 Jun 2025 23:07:55 GMT  
		Size: 252.1 MB (252098568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3677b8e9b08e94a57ddd05466876c6b32a9330811a37558f27125e8b0da1acb7`  
		Last Modified: Fri, 06 Jun 2025 23:07:27 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lunar-ros-core-zesty` - unknown; unknown

```console
$ docker pull ros@sha256:e299cdda5311ee2dbfed3b522c0289a59a53f961006586998a2cfae5e7a1cbaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (29969901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19aa8f4e2dc9ffdbe804844e0518e2fca3ef543c53d577c46b19d63fc103b2ce`

```dockerfile
```

-	Layers:
	-	`sha256:e24039435663709f3e80c9a758da277d86d8ec724ed04c162d835481f0509f62`  
		Last Modified: Sat, 07 Jun 2025 01:23:40 GMT  
		Size: 29.9 MB (29945338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eaf5c22c5eeef8cb484908d9e76abdb3f96c735760e33b2bf36f5aea3ddfab4`  
		Last Modified: Sat, 07 Jun 2025 01:23:41 GMT  
		Size: 24.6 KB (24563 bytes)  
		MIME: application/vnd.in-toto+json
