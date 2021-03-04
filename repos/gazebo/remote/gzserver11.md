## `gazebo:gzserver11`

```console
$ docker pull gazebo@sha256:446082d5fc8a1db994499884a49c8448e02f3406d29216ad1286ada441af1195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver11` - linux; amd64

```console
$ docker pull gazebo@sha256:b14dcfd42081207dd3d37b3903da74a69134c603200d1413ae69b65815d1c09e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318606681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9db29628c66c5aadd66a400faad75332fe9160f6b851892c4d3a170a4505289`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:11:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:11:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:12:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 04 Mar 2021 04:12:02 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 04 Mar 2021 04:14:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.3.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:14:14 GMT
EXPOSE 11345
# Thu, 04 Mar 2021 04:14:15 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 04 Mar 2021 04:14:15 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 04 Mar 2021 04:14:15 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6feb7b35b48a6d7b9001d90f52185993d6984828fb9c5eb938874fe345fab7d`  
		Last Modified: Thu, 04 Mar 2021 04:22:47 GMT  
		Size: 1.2 MB (1182675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c853d2c4ffee69978054a176e77e8291024992e917d83428d5a5edb1b89ba43a`  
		Last Modified: Thu, 04 Mar 2021 04:22:49 GMT  
		Size: 16.1 MB (16147927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5984595a6c793e11621cfb81d492c34889df12e312e22f65f434e627ac62c1a`  
		Last Modified: Thu, 04 Mar 2021 04:22:46 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f498dca1a259e8ce35a3e98981a85038e8c7b651b1b646209014cb6b41fe456`  
		Last Modified: Thu, 04 Mar 2021 04:22:46 GMT  
		Size: 5.5 KB (5467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c4bd9ce9f5d6bf9474f5ff72468be5a9e1462094bc6d5f6454f5e3c89311de`  
		Last Modified: Thu, 04 Mar 2021 04:23:24 GMT  
		Size: 272.7 MB (272700186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9acd4e790058155c9721c0b77b961fc5d4989c9c948ae1be62e2a602a609e6f`  
		Last Modified: Thu, 04 Mar 2021 04:22:46 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
