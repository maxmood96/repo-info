## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:180a16bf0752b5d573d8b20fe003237c40963832f49b6a2e2b4667e9f90efe2d
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
$ docker pull ubuntu@sha256:bb03a3e24da9704fc94ff11adbbfd9c93bb84bfab6fd57c9bab3168431a1d1ff
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28841348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1aa655de821c2761b4dec437fbb5a52429b029141f687b38cdff4cd0d50d32`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:15:22 GMT
ADD file:53ca8a3f446b0751019d522066ce844f6281ffb5b15e9605cd8940176abf4c76 in / 
# Wed, 19 Aug 2020 21:15:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:15:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:15:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:15:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d94cf711eb1df9e05b5ab9c367f7417c481e9b5deee1724f93b96c77bff11c8f`  
		Last Modified: Mon, 17 Aug 2020 15:53:01 GMT  
		Size: 28.8 MB (28809294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc1ea4c1ef986e00d114cccc9e5fbbe6bd5b8f35145cacb0f12ae3389c4e0a2`  
		Last Modified: Wed, 19 Aug 2020 21:17:10 GMT  
		Size: 31.0 KB (31042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2147ebd301d69260017329191f4072fbb193e2c1c092542270947091c6eaa60c`  
		Last Modified: Wed, 19 Aug 2020 21:17:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2955d4b7554096a19ae03fac9a539a3106b871165d9beef32fb6f3b16bed6c4a`  
		Last Modified: Wed, 19 Aug 2020 21:17:10 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:eb1e82d1e85283abb47d328cb838e8adff126ec4f44398a0e4b7f66dbad3fcb3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24225677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da198324477aac913e0edc38e27352d36c5b9dbc1c4853faa79e2349f8dac21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:46:00 GMT
ADD file:0bf418503e730b1c07a5f7cfa6bb46ee5632cc7b373b62ee6dd516fd9ac74a74 in / 
# Wed, 19 Aug 2020 21:46:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:46:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:46:08 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:46:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:51f59682918cc084f352717f5c3396b728b9330e743eeb2b4e68dfb462af45d7`  
		Last Modified: Mon, 17 Aug 2020 15:53:50 GMT  
		Size: 24.2 MB (24193556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b1422315ef362739026a4ca046b2e2d8c997dd3e3abb96a1be02059d277f54`  
		Last Modified: Wed, 19 Aug 2020 21:47:41 GMT  
		Size: 31.1 KB (31088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5e75f32a143c512dd9eac32b387a755f89cce7c5ba380f97e7925c151578cc`  
		Last Modified: Wed, 19 Aug 2020 21:47:41 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edad5a87e6717b17b109e7c4181ce3bd137895c7b03457c41fde02ce7ccbcb69`  
		Last Modified: Wed, 19 Aug 2020 21:47:41 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:dc82a033948ee2312f60e0107f5c252ce9ad93567b8375f619876532aa7b6fe3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27443997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8fdae0869cff33323fa03d122802eb93629f0727d4690a3325c51bd43a3426`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:30:48 GMT
ADD file:a2368478f6147dfb550f11fd08fa580527841837e6de780105b0ee3c869e9045 in / 
# Wed, 19 Aug 2020 21:31:01 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:31:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:31:07 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:31:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:11602f8d9ef9a64d301368c826db17ed80fdaaa6895c8479600ecfb22906feec`  
		Last Modified: Mon, 17 Aug 2020 15:53:49 GMT  
		Size: 27.4 MB (27411937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9baf34eaf014c357d3680a1c3659aa57594a0cf1e8f13f3410ff6e659147f0`  
		Last Modified: Wed, 19 Aug 2020 21:32:46 GMT  
		Size: 31.0 KB (31023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f4efba19094c2a8cdccdb0aad9f813a4ae4c9ecbb8028522dfe7136037188c`  
		Last Modified: Wed, 19 Aug 2020 21:32:46 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61503eacf6a2d668185f96d1697af41f5c1798343a4903c2141b75db7ba35fb9`  
		Last Modified: Wed, 19 Aug 2020 21:32:46 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:db2a2f54ed366adb1dbd3757402b62c749ce74d6f7451219b1906178dc35b865
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 MB (33553433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a22152db5db55d0202d6d07dcc102eda850fb74d7ab81686303192664f819c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:16:10 GMT
ADD file:d2bdf56089aa739c01f4fea190a17051fbcd45e31fa5ba26d466921d4b528a06 in / 
# Wed, 19 Aug 2020 21:16:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:16:34 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:16:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:16:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bd233d33322880c9108ff9d4a2836417f422f1f76cea04cbce12861b48e4ec0a`  
		Last Modified: Mon, 17 Aug 2020 15:54:01 GMT  
		Size: 33.5 MB (33521520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948f26d4116ec9c2f8ce7b5d3765e3f977e8e62da7b636f40f1d3d554b6027e3`  
		Last Modified: Wed, 19 Aug 2020 21:19:34 GMT  
		Size: 30.9 KB (30877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2568d3b37f18de7a6f08771049d897ef5d8bdbf2ddba783262fee3d781a2c588`  
		Last Modified: Wed, 19 Aug 2020 21:19:33 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271de21485d292cc9b05d3b055184c64751e0cf915de5be7c595ef973f80d104`  
		Last Modified: Wed, 19 Aug 2020 21:19:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:b536185b225f0356e0d2b678da47051ea9da9df46c1f75b95a023ee3636af45e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28577930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849b2470e99451b67b1c616c26b5b8daf6db385464918792d2844b455a5b40e0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:10:31 GMT
ADD file:62afc24038998372a88abab1eb3c5eddd0c6551c6e5c56eb3f466ca26816e9c6 in / 
# Wed, 19 Aug 2020 21:10:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:10:36 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:10:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:10:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:920f4fc5f9a3eec734000cb609b35bce4bd842b886967e3f9242e9b1ef4c1851`  
		Last Modified: Mon, 17 Aug 2020 15:54:28 GMT  
		Size: 28.5 MB (28545182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b78dfbe3669075931a4f4250923d05bb9ee9276049becd7b75122e444faceb`  
		Last Modified: Wed, 19 Aug 2020 21:11:34 GMT  
		Size: 31.7 KB (31719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e366567dad155c04eedb45feb0b4c6afbb4832bac8ae3a9e60d49bf795c0d8c`  
		Last Modified: Wed, 19 Aug 2020 21:11:34 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa80c73ca70349d062cdd34084bd45aa84f9e86a5b141ca7244b26ec6e436590`  
		Last Modified: Wed, 19 Aug 2020 21:11:35 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
