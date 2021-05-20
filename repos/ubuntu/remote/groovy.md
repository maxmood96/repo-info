## `ubuntu:groovy`

```console
$ docker pull ubuntu@sha256:665723ebde552a334e7cda35161c4985d327860e4c5657a4a84a25a2a456c3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:groovy` - linux; amd64

```console
$ docker pull ubuntu@sha256:6166dad89a1e4448f25a59ddd763bdc2ce95f784edc8bd5744562529134ce652
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31329155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5645187c49fdab7685ce24360cc17cb8bd7d740dc5de989f54f1d65c39d0548c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 May 2021 19:44:47 GMT
ADD file:50e56682329ac9b5b81321252a40154457a3f54c6972fce6c9755e513b4c8955 in / 
# Wed, 19 May 2021 19:44:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:44:49 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 19:44:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:44:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:abbb6e7817965b3a1b696d2d3393724dcba223f50e3be0fae33410c50a67db78`  
		Last Modified: Wed, 19 May 2021 19:46:05 GMT  
		Size: 31.3 MB (31328117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ac6b0850ddfacd14d25844827637a38cf1bc3b9350ded94f9f6c7533765c73`  
		Last Modified: Wed, 19 May 2021 19:46:01 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b666bf17853adc7e13292d64bed15e1e5c32888a27d3853b99a65b822a1bf62b`  
		Last Modified: Wed, 19 May 2021 19:46:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:groovy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:6c6739fc427893da3110e2f2c631f34e1146dc28f99b08ef8de367ba6c389159
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26302837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80239021fb9fa8a4c61c6e01eddbd4be06026a0545fff726543d44f18fbda922`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 May 2021 20:22:24 GMT
ADD file:acda6861dee730077731d36484af6c3fa51a7ea2bcdbab39a88f53cb3276509e in / 
# Wed, 19 May 2021 20:22:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 20:22:30 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 20:22:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 20:22:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ec376efdd72c4146827ffa866153a4452541beae9106def5a3afb4e858023939`  
		Last Modified: Wed, 19 May 2021 20:24:15 GMT  
		Size: 26.3 MB (26301801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065457da20bed844ec32f63c2c352d39da0d9cf58fd9fcdd710a8c2fe01e0ec`  
		Last Modified: Wed, 19 May 2021 20:24:08 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acffea83b1b3aaf9f535176139002bf18809b84cc711fddf2a83206c09194c8c`  
		Last Modified: Wed, 19 May 2021 20:24:08 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:groovy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:15507ed695229e52b84dbf79ab052b9c738917442244376d136ab0d99478c1c0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.9 MB (29859198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae42a2f69b62859661cbea2a3c44cf7523fb015a05e5d3501223c3f767baf585`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Apr 2021 22:48:13 GMT
ADD file:3b909e405de304d3529a43650aa6812b726dbfe24e2f2a9c163818ab5c206cf1 in / 
# Fri, 23 Apr 2021 22:48:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:48:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:48:20 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:48:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0312c280f333ebad21d92c6554a1f0b81a5d7de275f2f1fe29c960721e40cb28`  
		Last Modified: Fri, 23 Apr 2021 22:50:26 GMT  
		Size: 29.9 MB (29858157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fedfba085a0c1226682c17f7966295deb654a557860da25aedabd09c96edf6`  
		Last Modified: Fri, 23 Apr 2021 22:50:19 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d5a4de4889c6c2db1938b8170a1a427483a6b6ab113ceeae3e4b02819d54cf`  
		Last Modified: Fri, 23 Apr 2021 22:50:19 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:groovy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:328a4beb0442f2d7200c4a26bee07bdbdc4b249707d933967d3400d552db72e8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36529135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e89f68796380d91969dfc88742e1428be2b514424b750ff4ec8a85a97a7f531`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 May 2021 21:29:23 GMT
ADD file:e02a256acc936ce1e2fa7aca9307c60cd51693e4364c4d24cc107d2be40f37a0 in / 
# Wed, 19 May 2021 21:29:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 21:29:52 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 21:30:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 21:30:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c2eddaed5855ee2d3cec1b9f41f0937d8a74b9c2fe3d7da32d4539c7c0f7cdff`  
		Last Modified: Wed, 19 May 2021 21:34:22 GMT  
		Size: 36.5 MB (36528099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19b2b6c22e01fb1738990a7c11f30fd92a5e67e9496e82617dbb2c51f2974e8`  
		Last Modified: Wed, 19 May 2021 21:34:15 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb92cae7f4a2c1c2e37f248aea80ea800f4530338185b84410c36fc841a6c22`  
		Last Modified: Wed, 19 May 2021 21:34:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:groovy` - linux; s390x

```console
$ docker pull ubuntu@sha256:eab164a5a7f3991a7e2247b47ba4edf047c8e7cbf0e6ab99665b964deb96e2b0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31550556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466085af4ac5351b58f8a1b8ce42eeccd5aaae53d578459fa02c802a7723ad95`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 May 2021 23:28:59 GMT
ADD file:03a8898be40d65406ce1fa2226e61ca1176cda39f2eabf6cd8161c012630a3cb in / 
# Wed, 19 May 2021 23:29:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 23:29:08 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 23:29:10 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 23:29:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:147bdf237ff640c8d8e1f1d98a1660723eb59f9301ebfb588e12bf1835aa46dc`  
		Last Modified: Wed, 19 May 2021 23:30:49 GMT  
		Size: 31.5 MB (31549521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13093602d8efdcb973efdf2bbfb8d32b6e1498dd521ddd22d2dc8ef8450d2e5`  
		Last Modified: Wed, 19 May 2021 23:30:45 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c8cb1f72b71c4f8333c96b783bf5949a4e538652d011362cfa49108e19455e`  
		Last Modified: Wed, 19 May 2021 23:30:45 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
