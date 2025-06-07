## `ros:lunar-perception-xenial`

```console
$ docker pull ros@sha256:ddf317fe97b08f9801d3c2e5be90e2a46b3e1c67768fb0885cae270a0b0f8958
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:lunar-perception-xenial` - linux; amd64

```console
$ docker pull ros@sha256:b784307437e20a53ee4650028ea1e563bac3c38a48642717c58a82b18503b341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.5 MB (719478621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d706e3b8fc45ad9255f141fe2bb0e28d0f93e3620f4bff3b5700b05421dc468`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Apr 2018 23:57:44 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Thu, 26 Apr 2018 23:57:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 26 Apr 2018 23:57:44 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 26 Apr 2018 23:57:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 26 Apr 2018 23:57:44 GMT
CMD ["/bin/bash"]
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN echo "deb http://snapshots.ros.org/lunar/final/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
ENV LANG=C.UTF-8
# Thu, 26 Apr 2018 23:57:44 GMT
ENV LC_ALL=C.UTF-8
# Thu, 26 Apr 2018 23:57:44 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
ENV ROS_DISTRO=lunar
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 26 Apr 2018 23:57:44 GMT
CMD ["bash"]
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -y     ros-lunar-perception=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:58690f9b18fca6469a14da4e212c96849469f9b1be6661d2342a4bf01774aa50`  
		Last Modified: Fri, 13 Dec 2024 13:12:07 GMT  
		Size: 46.5 MB (46497548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51569e7c50720acf6860327847fe342a1afbe148d24c529fb81df105e3eed01`  
		Last Modified: Fri, 13 Dec 2024 13:09:14 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8ef40b9ecabc2679fe2419957220c0272a965c5cf7e0269fa1aeeb8c56f2e1`  
		Last Modified: Fri, 13 Dec 2024 13:10:06 GMT  
		Size: 528.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb15d46c38dcd1ea0b1990006c3366ecd10c79d374f341687eb2cb23a2c8672e`  
		Last Modified: Fri, 13 Dec 2024 13:08:51 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88ab159a07291d742304920b79c14160def8f59b0960a09de2153cbf3a713fd`  
		Last Modified: Fri, 06 Jun 2025 22:49:42 GMT  
		Size: 6.9 MB (6939367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666f4344c057c7c79a8c767c35606fe7237d0cd03cd578070204607a24e0e571`  
		Last Modified: Fri, 06 Jun 2025 22:49:42 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadeec5d2aa49358a0c95bd28186e5e1870a47b03258f31b31473b785d42b9de`  
		Last Modified: Fri, 06 Jun 2025 22:49:42 GMT  
		Size: 17.3 KB (17334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fec28c4ac90e93fc866c6a9b249cb5f4010680060934e03a1aff4f744c9a9e`  
		Last Modified: Fri, 06 Jun 2025 22:49:45 GMT  
		Size: 54.3 MB (54251263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab75082b9a09a85d411d21349d8ff5f1dddcca35b0c3839e40debbd3dd3f5f8`  
		Last Modified: Fri, 06 Jun 2025 22:49:43 GMT  
		Size: 1.9 MB (1907618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340f6e124e3717740ec2bf06672e9200ec6bfe1fcc81a965c1df1b909a4f48b4`  
		Last Modified: Fri, 06 Jun 2025 23:07:36 GMT  
		Size: 193.4 MB (193351670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5957640ad151f4165dfcde4c0b4fb8e9b288ea790956b366caae5e98cfd354`  
		Last Modified: Fri, 06 Jun 2025 22:49:43 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e953e55cf55f11499636b0be8fdb31b2d51399d7215f3a67ef02a7375f7d3e`  
		Last Modified: Fri, 06 Jun 2025 23:09:41 GMT  
		Size: 85.5 MB (85456298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3547bca6a3bf8237e9579e0f2715205d242b7301fafea20169606993268b4e44`  
		Last Modified: Sat, 07 Jun 2025 07:47:39 GMT  
		Size: 331.1 MB (331055540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lunar-perception-xenial` - unknown; unknown

```console
$ docker pull ros@sha256:1164bd550d073e0471d18ec5886c91be4e709b86130548ee07719c8d1d222682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54167426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118fe5765037fc0a40c1b88ab2b2b7e171d36c5af2e37a8edff5a1ad5372af49`

```dockerfile
```

-	Layers:
	-	`sha256:beb1a2b1b72184ad725787e923d5696b1a82e11c9d9ae16ad84d98963718d007`  
		Last Modified: Sat, 07 Jun 2025 01:22:57 GMT  
		Size: 54.2 MB (54157496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f6af2a6183153debab580d080b3056ae28ef4185ceb75e43bbb3cc9acf00ff`  
		Last Modified: Sat, 07 Jun 2025 01:22:59 GMT  
		Size: 9.9 KB (9930 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lunar-perception-xenial` - linux; arm variant v7

```console
$ docker pull ros@sha256:8596c7d68eccf29fcaa64d737cb5c6e6f074aff69d0f5c67fcfa58c24fc2596a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.8 MB (610789234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257e9dbd02627b3aeb99a8f8344e58eda215efba830798c797a8c17e562bd2b6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Apr 2018 23:57:44 GMT
ADD file:294a94a081de785c730003a440a0530a85add2bcb60c0f5bc4ce7ee17867ac4e in / 
# Thu, 26 Apr 2018 23:57:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 26 Apr 2018 23:57:44 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 26 Apr 2018 23:57:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 26 Apr 2018 23:57:44 GMT
CMD ["/bin/bash"]
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN echo "deb http://snapshots.ros.org/lunar/final/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
ENV LANG=C.UTF-8
# Thu, 26 Apr 2018 23:57:44 GMT
ENV LC_ALL=C.UTF-8
# Thu, 26 Apr 2018 23:57:44 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
ENV ROS_DISTRO=lunar
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 26 Apr 2018 23:57:44 GMT
CMD ["bash"]
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -y     ros-lunar-perception=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b95ba076a26b98e98eac4b43596b59c20d1e61a36bcaf2afae3aeebadc8844cf`  
		Last Modified: Tue, 17 Dec 2024 15:12:14 GMT  
		Size: 40.3 MB (40312250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67de3a011d085fbb829ef04d78536904c6ead23dbc82dd5facff2488d6398672`  
		Last Modified: Sat, 14 Dec 2024 10:56:05 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1202719f1ed95c66ca12784e9dd1983de008b6871eb2cb324c3a3f1a98836af`  
		Last Modified: Sat, 14 Dec 2024 08:45:37 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1764d93e99e79b6b91814768fa379cc5ce0dce26c71ecfe2f5fc6b3f38212b`  
		Last Modified: Sat, 14 Dec 2024 13:56:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8a9efacdb733c2fb39076b37dded86a88cd62fb1c74b5515c47335180243e4`  
		Last Modified: Fri, 06 Jun 2025 23:03:39 GMT  
		Size: 5.7 MB (5701655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03abd5568e0f21ac1a88810d2f1a7440e11e213f902e4c43890cbedfb489fdfd`  
		Last Modified: Fri, 06 Jun 2025 23:03:38 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9306ee55967f6fad73271d8e982eca09e95cb37c8eea8b50f0f6c54add2989a1`  
		Last Modified: Fri, 06 Jun 2025 23:03:39 GMT  
		Size: 17.3 KB (17334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c057727f274d15046b615f58bb89163e07f83ea6fd3943da66919914bd1513bf`  
		Last Modified: Fri, 06 Jun 2025 23:03:43 GMT  
		Size: 49.8 MB (49808908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abc840338cf675e9a2e2c82f4582a509063786f887976fea9b34241b922ada4`  
		Last Modified: Fri, 06 Jun 2025 23:03:41 GMT  
		Size: 1.9 MB (1907403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251c334d8191461a21685b6aa412beb8445bba6aca0e123bcb18395b350b72a6`  
		Last Modified: Fri, 06 Jun 2025 23:03:19 GMT  
		Size: 164.7 MB (164735620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6038d0131f890f5cd0d702c5171fef1b8c3599a0a363c4d8cc840646cedae7a0`  
		Last Modified: Fri, 06 Jun 2025 23:03:40 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c5ca64cbbcd8d0a7a1aabee0d47ef2c86d1e78456a0039fbe20d076370bb96`  
		Last Modified: Fri, 06 Jun 2025 23:20:38 GMT  
		Size: 76.2 MB (76230375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd53ae0b43302d61adb9538e5db3c50d659e7122300892bd9bca89f9ce4ecda`  
		Last Modified: Sat, 07 Jun 2025 00:37:11 GMT  
		Size: 272.1 MB (272073716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lunar-perception-xenial` - unknown; unknown

```console
$ docker pull ros@sha256:d45cacb59ec0319199664fbd6e221fd6dd291d7ab662be03cc2bd06a2c19d5cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53919686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ece2fae8d979a37ac10475bd502e43faaa4a4d03799c7fec5e1500caf2a77e`

```dockerfile
```

-	Layers:
	-	`sha256:4d7b88fb4b7b52da5d8e56b73f94121c45de968651d2f95ca8dbaf40455d28cd`  
		Last Modified: Sat, 07 Jun 2025 01:24:15 GMT  
		Size: 53.9 MB (53909648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c662a1be7f0389a9d715e23ce614c23c52a4cc8f6b4941e60d67cf05460fb5a`  
		Last Modified: Sat, 07 Jun 2025 01:24:16 GMT  
		Size: 10.0 KB (10038 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lunar-perception-xenial` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0470de9bc5ecc83e747eca1ba35ad6a30641f06f5953b061e5cdf01ee99edbc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.6 MB (633592846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00ac3d8698639e9be853f9f36b7b4222e9d81f545be063b55c00784bd12da72`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Apr 2018 23:57:44 GMT
ADD file:3c6dc937cb7b4c81b42126f377d23320ec1d0a8ca34d38e7c45871f1d08dac43 in / 
# Thu, 26 Apr 2018 23:57:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 26 Apr 2018 23:57:44 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 26 Apr 2018 23:57:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 26 Apr 2018 23:57:44 GMT
CMD ["/bin/bash"]
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN echo "deb http://snapshots.ros.org/lunar/final/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
ENV LANG=C.UTF-8
# Thu, 26 Apr 2018 23:57:44 GMT
ENV LC_ALL=C.UTF-8
# Thu, 26 Apr 2018 23:57:44 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
ENV ROS_DISTRO=lunar
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 26 Apr 2018 23:57:44 GMT
CMD ["bash"]
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -y     ros-lunar-perception=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:828b35a09f0b2f3d1dead43aa2468ff5eba6c463423b3fff7ee6d150f6fd1b6b`  
		Last Modified: Fri, 13 Dec 2024 17:43:40 GMT  
		Size: 41.2 MB (41239253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66927c6d1d3d2e9321c4893f7f2105b7cd23dfb082853d97ec08f188e271e612`  
		Last Modified: Fri, 13 Dec 2024 20:27:34 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000560be91651dcbf476ebacb8bf1f1339694a3327f8e6da2519e0b29b33eb5d`  
		Last Modified: Fri, 13 Dec 2024 18:38:28 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6225a0253717abdc2ee23ea211c1c439c93b84231ec0a4f1c74762a205ba7234`  
		Last Modified: Fri, 13 Dec 2024 13:19:32 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c3c7fa1dbf39c02c8e143a34d21d21ae8a213708dfa93636973101fbe6dfb4`  
		Last Modified: Fri, 06 Jun 2025 22:54:04 GMT  
		Size: 6.0 MB (5958484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9af9636c74800d8fb80c3b306c34b804106f114cf8e2a716011bb8f623d680`  
		Last Modified: Fri, 06 Jun 2025 22:54:03 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823d15c61da62ded6603fed3d8bd7c3ee85b7d90d7ab2c255a2623657a583a39`  
		Last Modified: Fri, 06 Jun 2025 22:54:03 GMT  
		Size: 17.3 KB (17334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62e0a751f3a49a05f6cdbfe23f772012565e57c354bf85df6155cfc3337bd87`  
		Last Modified: Fri, 06 Jun 2025 22:54:06 GMT  
		Size: 51.6 MB (51559430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf119c02c68eda54d4cf53ec3a4606e3ae7771e1b917dcd7cb8788b81f6c9859`  
		Last Modified: Fri, 06 Jun 2025 22:54:05 GMT  
		Size: 1.9 MB (1907544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0456cf71714a073a4eb9bbc79b5b3f3d4b08efc0069182646fcbd0d31547d7a4`  
		Last Modified: Fri, 06 Jun 2025 22:53:40 GMT  
		Size: 174.0 MB (173995768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58de28b75411d2e198fcf0f41d3b67eeb48b62ece3bcdb053a8239534cc6a91b`  
		Last Modified: Fri, 06 Jun 2025 22:54:05 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29828e69108e5f7e56f0bae6be5e4b62fd37bbe48356fe19ebba33d7e56f3f6`  
		Last Modified: Fri, 06 Jun 2025 23:21:31 GMT  
		Size: 77.7 MB (77711863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da12ce6ec2931b847cbc9ca710ef9e4ffd32a872b7b0d0379248cf92584c70fc`  
		Last Modified: Sat, 07 Jun 2025 00:20:47 GMT  
		Size: 281.2 MB (281201236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lunar-perception-xenial` - unknown; unknown

```console
$ docker pull ros@sha256:0c25c86f69d71098ab06df836e9f58cb9b6169a3d75f1b39644399ec00bcf83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53809333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e54a45eb5b284039970ff236c029f8e521f7f9a4ea748322c7ba31fca7e423`

```dockerfile
```

-	Layers:
	-	`sha256:f44439ca37a1291b6588e831ed9005e85ce83d48ff796df6adb8783c5d74e1ca`  
		Last Modified: Sat, 07 Jun 2025 01:25:25 GMT  
		Size: 53.8 MB (53799275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae0bd69abdee152515a9e22b1e20053d7cb20483bec163a9eca9c4c7fafe065`  
		Last Modified: Sat, 07 Jun 2025 01:25:26 GMT  
		Size: 10.1 KB (10058 bytes)  
		MIME: application/vnd.in-toto+json
