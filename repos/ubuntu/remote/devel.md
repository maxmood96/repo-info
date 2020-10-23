## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:d9d20b1c3a5a21074707a53123bc7dd5a93adb6d7db929eebd37cc1de11235c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:devel` - linux; amd64

```console
$ docker pull ubuntu@sha256:a569d854594dae4c70f0efef5f5857eaa3b97cdb1649ce596b113408a0ad5f7f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31338945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5958a2de8e69f762888ac8df90e995c74b5643f0a72ae09176f178de25b67c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Oct 2020 17:32:46 GMT
ADD file:6099585856c27a9f8dd40d7e679184a6d1bb58133acf73d5d3c9904932def005 in / 
# Fri, 23 Oct 2020 17:32:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 17:32:47 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 17:32:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 17:32:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7a14fb4cd302ea60d4b208f17bb50098b52a17183a2137c08299a3b915d7cbae`  
		Last Modified: Fri, 23 Oct 2020 17:33:40 GMT  
		Size: 31.3 MB (31337938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b1fecc905c746712dc231f73c5d630927892af991ce140673eb77dd9b697cd`  
		Last Modified: Fri, 23 Oct 2020 17:33:35 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ac8019c9736cea870759cf87bf752344fd3fb2dbf7a3921e9c60e140213900`  
		Last Modified: Fri, 23 Oct 2020 17:33:35 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:a0a7acfca9ff35115f91e05123f61a7e51adecca54599c01a4e6ba5de7c998f2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26299606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e22a489beb7ba89241a529f2cb9d0fa33c910f195f49c5c2a3c4f069b6a406`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Oct 2020 18:16:42 GMT
ADD file:0eeb4202bc0d9b7d0c78bff294ff6015f21c8fb8e9ca0ff983ff6c78d5897235 in / 
# Fri, 23 Oct 2020 18:16:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 18:16:46 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 18:16:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 18:16:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f17eabb5dfcad75fa1be363632f687064e41500f8c6fe95ae2ef3bcdf7c32c0c`  
		Last Modified: Fri, 23 Oct 2020 18:18:04 GMT  
		Size: 26.3 MB (26298569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d196182becee925f94a0471151ee4e042efe951ee13958f732f1b7c094aa6619`  
		Last Modified: Fri, 23 Oct 2020 18:17:57 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06172a7b7f85373b7794e70e99b64be5361635df132bbde4a4773b41f054659f`  
		Last Modified: Fri, 23 Oct 2020 18:17:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:7415c11a86fc9f42493000262437669bb5fb210953062f9e1f3f6979dea54f7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.9 MB (29885741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81ef668fd833f777a17a51581bdbc8d5c7ea266d8311e4bda01084763042df4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Oct 2020 18:19:57 GMT
ADD file:eba1bf343f462dff24cd8570c557a24680d651c0accfaed36f4d3845e30f92de in / 
# Fri, 23 Oct 2020 18:19:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 18:20:01 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 18:20:03 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 18:20:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:52b0f1f415e4765da3991a8d5e5c3d6bdf45adde4a31fe000210c37e09281ad4`  
		Last Modified: Fri, 23 Oct 2020 18:21:16 GMT  
		Size: 29.9 MB (29884705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7b4c42c4aa2ad2610ea0264f0a465ac8caecaebf3f6126595042adb7ab1616`  
		Last Modified: Fri, 23 Oct 2020 18:21:09 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566e53edfb1c98cf8ccea2ad6fdf8e3c67d3876df1d842cc33b5e373551af235`  
		Last Modified: Fri, 23 Oct 2020 18:21:09 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:1f06554e63cdcaef8637ee6009b041866c094dcf73dde9bc30fb00b9b6e8fdce
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36549526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d6b6b4abdfcf0394d3ea80f705e238a54b192658a94037b2043a0822e2e6f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Oct 2020 19:27:22 GMT
ADD file:3cceb8288ea4091c4fb6670e395f7391741cb6aaa44a1f5e6a2085df56ecba62 in / 
# Fri, 23 Oct 2020 19:27:45 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 19:28:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 19:28:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 19:28:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a69afe95a22d68414fa1ac1b89258d7d482624063e15ae9202ea3fa7649709e8`  
		Last Modified: Fri, 23 Oct 2020 19:32:07 GMT  
		Size: 36.5 MB (36548485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80643583a935ac0edf00defeb0107c6483073a7c2dddd14e5dfad2a4699b178`  
		Last Modified: Fri, 23 Oct 2020 19:31:58 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49aeb38173a94db987f5d84e1a11177492fa369f214626d961156443b10f1571`  
		Last Modified: Fri, 23 Oct 2020 19:31:58 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:17a743ebd0cf5056f2c66641e6b2dc1c20211ebf15494b119a8c5072369a41a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31362896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec25c45b5dd7cfc76b2ae926ad928a6be5b0c5cd4c9f707d671abc3cbf6a43a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Oct 2020 19:09:36 GMT
ADD file:48a4e577acc64b1b327a3319475c944be8287157a3c29f92b870c9dc36d77a4f in / 
# Fri, 23 Oct 2020 19:09:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 19:09:44 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 19:09:45 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 19:09:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9a0516eb4850a8432c465fe497cc8786c555cfc9ef04bfff7cb346e668dd51d9`  
		Last Modified: Fri, 23 Oct 2020 19:10:36 GMT  
		Size: 31.4 MB (31361864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cbebe3cbcbb775ec7522ca380dacda8bd8d73075b208366784ee1394410693`  
		Last Modified: Fri, 23 Oct 2020 19:10:33 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c089d98c2f3be8a4b0ea0a3158009c537906d5f7d069535d5a15c0e4298e384`  
		Last Modified: Fri, 23 Oct 2020 19:10:31 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
