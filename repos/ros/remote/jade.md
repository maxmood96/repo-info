## `ros:jade`

```console
$ docker pull ros@sha256:5ddde26e2e8f56f52fdc459ea0dc109fe99f540969ec11bcaf9a9689a29c5fa1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown

### `ros:jade` - linux; amd64

```console
$ docker pull ros@sha256:93726369bb5adcfd2fa9eea6c9e5a4f51c95f2d444ec340e12395410c59be988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.8 MB (270846398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0343c51803f3436a8cf2c8324d0b8ce1864576abc4634bb6dd7c677d23ad3982`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Sep 2017 19:26:55 GMT
ADD file:276b5d943a4d284f8a7b249176a31f93d95e852480c2b851de287e53ff622bba in / 
# Mon, 11 Sep 2017 19:26:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 11 Sep 2017 19:26:55 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 11 Sep 2017 19:26:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 11 Sep 2017 19:26:55 GMT
CMD ["/bin/bash"]
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
RUN echo "deb http://snapshots.ros.org/jade/final/ubuntu trusty main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
ENV LANG=C.UTF-8
# Mon, 11 Sep 2017 19:26:55 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 Sep 2017 19:26:55 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
ENV ROS_DISTRO=jade
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-get update && apt-get install -y     ros-jade-ros-core=1.2.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Sep 2017 19:26:55 GMT
CMD ["bash"]
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-get update && apt-get install -y     ros-jade-ros-base=1.2.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:eca7947e2e80596bd2dd6aa721c50543b02d859c18c479e6fee7974186341fbf`  
		Last Modified: Fri, 06 Jun 2025 22:50:20 GMT  
		Size: 14.0 MB (13999678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53493d080ac5b1dcf02f0544ab568f501bbd0cd25d5a3d4c090f79cfade15863`  
		Last Modified: Fri, 06 Jun 2025 22:50:19 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04b7382600e2675b92184b3c9e606962fb3a31d0fcc797c9718d86c5aeb77e1`  
		Last Modified: Fri, 06 Jun 2025 22:50:19 GMT  
		Size: 15.7 KB (15689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0540af077fd693d6d887b2c1377227d8aca763ac4abce016145113d53735c2`  
		Last Modified: Fri, 06 Jun 2025 22:50:21 GMT  
		Size: 30.9 MB (30903820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a90e857d50dc2639933dc58909049bb48dc5e49480f0b333cf30fd28555667d`  
		Last Modified: Fri, 06 Jun 2025 22:50:37 GMT  
		Size: 1.9 MB (1907624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d6930123b937d48d4d52a308e963df7fcdc06810cc42be7feaafbc10e10241`  
		Last Modified: Fri, 06 Jun 2025 23:07:49 GMT  
		Size: 149.7 MB (149666410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844a118e840e02939fac45745192b1b0256e7a176b68dd4d15b726e57f220d86`  
		Last Modified: Fri, 06 Jun 2025 22:50:20 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b08e9e2a9e663ee9d05790e491d44762dc6ef429870e731c93a8d91ad0ff0d`  
		Last Modified: Sat, 07 Jun 2025 00:07:53 GMT  
		Size: 3.6 MB (3588314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jade` - unknown; unknown

```console
$ docker pull ros@sha256:62a80a6aaefdd5c8c74750beba2418e32a836abd0a884df8064d7d52e5e99b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28833282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db28997a7f133db2b24d4043850653a713bf8514bd82ac0690ade929e4247752`

```dockerfile
```

-	Layers:
	-	`sha256:1da380a37a25906d4a8d673dea7b305148dd0004988b69e65abd519e9bee381c`  
		Last Modified: Sat, 07 Jun 2025 01:21:04 GMT  
		Size: 28.8 MB (28823717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b74196e0e5cbb6781a512fa1dfa87e202436142050e83f3b86f3c634e15b6956`  
		Last Modified: Sat, 07 Jun 2025 01:21:05 GMT  
		Size: 9.6 KB (9565 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jade` - linux; arm variant v7

```console
$ docker pull ros@sha256:35b7a62dbcf3248cc30d36bda667460c48230b99cbc17df6f71ae42cf884565c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 MB (247875405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddc7795cf2ea17157d9e873b2d1da994ca3ef2dc0d3959cbf2f1b23617d3b1c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Sep 2017 19:26:55 GMT
ADD file:e9d55e059869915743a8ca8e64582d23c48fe7e90e439daccd56d3e08e8673b4 in / 
# Mon, 11 Sep 2017 19:26:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 11 Sep 2017 19:26:55 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 11 Sep 2017 19:26:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 11 Sep 2017 19:26:55 GMT
CMD ["/bin/bash"]
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
RUN echo "deb http://snapshots.ros.org/jade/final/ubuntu trusty main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
ENV LANG=C.UTF-8
# Mon, 11 Sep 2017 19:26:55 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 Sep 2017 19:26:55 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
ENV ROS_DISTRO=jade
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-get update && apt-get install -y     ros-jade-ros-core=1.2.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Sep 2017 19:26:55 GMT
CMD ["bash"]
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-get update && apt-get install -y     ros-jade-ros-base=1.2.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:8c3a1499d5668b6eeb89a9466248af62e9ca582a05b6194ab6e3d02eee5dc26e`  
		Last Modified: Fri, 06 Jun 2025 22:55:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8938a18f64a189658ee8f48b5e9f7a626ff41fcf30c5f874cb2abb63d68ef65f`  
		Last Modified: Fri, 06 Jun 2025 22:55:37 GMT  
		Size: 15.7 KB (15690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263cbdaf4bc7d3a241568d22257a71f9904927c34f31958e9158bce6ef124d42`  
		Last Modified: Fri, 06 Jun 2025 22:55:39 GMT  
		Size: 28.4 MB (28374521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a92fe5263a2bc487b090e21e20f621403dbf2bbe128fd8708aba520322cceda`  
		Last Modified: Fri, 06 Jun 2025 22:55:39 GMT  
		Size: 1.9 MB (1907400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e4d6c3244eb00fe78adf5d790629099bc764bb9edc1c0c19c2e6e30a138bfe`  
		Last Modified: Fri, 06 Jun 2025 22:55:14 GMT  
		Size: 137.3 MB (137281787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f438e1a65e86df020def93be8ab1a263a07888112d72daaf1891da6b229ace`  
		Last Modified: Fri, 06 Jun 2025 22:55:38 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a3b5e16317ffd998270388053df05039b291855511acb39b0134904a2a00ae`  
		Last Modified: Fri, 06 Jun 2025 23:15:34 GMT  
		Size: 3.2 MB (3239276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jade` - unknown; unknown

```console
$ docker pull ros@sha256:9ad36d0e0394850b62eee2e2bf26eb505ae27ed82cf5611e9e05245a13750109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.7 MB (28715521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd37edc96ddb4dd3b6ec0197a3d4e984f83373608e59867e5f612ed30c3f4bb8`

```dockerfile
```

-	Layers:
	-	`sha256:fac6500ce65227bda2468289f2e0fdae190c593042872f3048e072963e61d52d`  
		Last Modified: Sat, 07 Jun 2025 01:21:34 GMT  
		Size: 28.7 MB (28705852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b604ce4ebaf4b7ea6ee2046f01234475ae7e224d71ac0136fcf50937753b3431`  
		Last Modified: Sat, 07 Jun 2025 01:21:35 GMT  
		Size: 9.7 KB (9669 bytes)  
		MIME: application/vnd.in-toto+json
