## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:da9741b5d651566e0a1d5608a06443f124aab1954f31dbec8b1aeb1f5f3bd0a2
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
$ docker pull ubuntu@sha256:d050ed7278c16ff627e4a70d7d353f1a2ec74d8a0b66e5a865356d92f5f6d87b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28394718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4d239ad3ccb463b7e5af60dea5d949669a57dfa35e12937821f9c2ef4ff1d8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 01:21:08 GMT
ADD file:6c8f103b672b6dc8b10903d40d33227d3b7a8e8df1af80e47142523f2b849adf in / 
# Thu, 16 Jan 2020 01:21:09 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 01:21:09 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:21:10 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:21:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8f6b7df711c8a4733138390ff2aba1bfeb755bf4736c39c6e4858076c40fb5eb`  
		Last Modified: Thu, 16 Jan 2020 01:22:19 GMT  
		Size: 28.4 MB (28363102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0703c52b8763604318dcbb1730c82ad276a487335ecabde2f43f69a6222e8090`  
		Last Modified: Thu, 16 Jan 2020 01:22:15 GMT  
		Size: 30.6 KB (30612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07304348ce1b6d24f136a3c4ebaa800297b804937a6942ce9e9fe0dac0b0ca74`  
		Last Modified: Thu, 16 Jan 2020 01:22:14 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4795dceb8869bdfa64f3742e1df492e6f31baf9cfc36f1a042a8f981607e99a2`  
		Last Modified: Thu, 16 Jan 2020 01:22:15 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:18100e418054ebe1be0fff4e514183f28088a0db409df081c3233dd22dcf4a15
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23866643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6279a48140d841fc9e2cb314144df2fc395505a11b76d3feb715abdcb24ab7e0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 01:01:57 GMT
ADD file:2d3ba051ed20fafa578680b18fbe731818ef6ab90ced4b0d6783816de70b6a6f in / 
# Thu, 16 Jan 2020 01:02:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 01:02:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:02:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:02:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fc4316c8e9493de0b0e1b0cc1c1b9b1fb58750baed7140f2fd1d7d964c601fc3`  
		Last Modified: Thu, 16 Jan 2020 01:05:12 GMT  
		Size: 23.8 MB (23835040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf21553c3db6ce4ac20d8a949658bc8bd42e4658e34d64017f3e117eb6da1c92`  
		Last Modified: Thu, 16 Jan 2020 01:05:06 GMT  
		Size: 30.6 KB (30569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2d0679b20cd11ff9c15f051b0c8be2781fdd2237f065c0be6336cfa58d0d9a`  
		Last Modified: Thu, 16 Jan 2020 01:05:06 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35042469e78e129ca9456d1cd736e5850df94ac632815d85a09777c32fb0082`  
		Last Modified: Thu, 16 Jan 2020 01:05:06 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:0551fb19b57011ba165f66399ca0e7e49402aa7cba6ba843a317f48e4cad9e35
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27160548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03158a6a8d98f77d01be4555b2453f43335571654ce2c1bf50042557eb7ffe0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 18:44:18 GMT
ADD file:627246f3025f0a9473866d1a3f837c7bc78c1bb64018aefa683ed63fd6b8affd in / 
# Fri, 20 Mar 2020 18:44:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:44:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:44:24 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:44:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9806bdadc1314b3e8b4d5249399ac07348da8dfd86b71f450d4a8d5bd672df12`  
		Last Modified: Fri, 20 Mar 2020 18:45:35 GMT  
		Size: 27.1 MB (27127860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004a0e1a95f5228adef261b8a421a32e0c6326702c2219757fd4c6ab176ae46d`  
		Last Modified: Fri, 20 Mar 2020 18:45:28 GMT  
		Size: 31.7 KB (31653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b08ae661b4f6495649f65df48cfe19cbbaada45e4c46064378e416fe5c68c11`  
		Last Modified: Fri, 20 Mar 2020 18:45:28 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e5fbabbfbbb4adc0246d014df57f1f8ed76e8f16b7cc3d313a1a7eafe628f7`  
		Last Modified: Fri, 20 Mar 2020 18:45:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:1773bf363b86cb6c1030c68927f945d541441a7e725c6854613c1963e12e90f1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 MB (33054624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2da1eb7687f4db5974f5d2a41cdadc44036d4cc62f6c9fe8cc88d929cad69df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 01:18:25 GMT
ADD file:6ea7cc645f3cc6826fa2b3c70b3bc62390b1db44144c2b8bf417293920c2c22f in / 
# Thu, 16 Jan 2020 01:18:30 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 01:18:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:18:39 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:18:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5bb2edf9d88cb6dcc362d13ede46c8731b8735b1677dedb332da930dd1930f62`  
		Last Modified: Thu, 16 Jan 2020 01:20:53 GMT  
		Size: 33.0 MB (33023125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbb237b90ca44381648c270622d286258f61e12b3d5d70ee1aa4b61d4b95d10`  
		Last Modified: Thu, 16 Jan 2020 01:20:46 GMT  
		Size: 30.5 KB (30460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a864feef47ddb01476b0cc027637e5002f74d5b728b88cc65b0d9c059788e1c3`  
		Last Modified: Thu, 16 Jan 2020 01:20:46 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582c7ec8f85b836afbb99e6f62565baf3fbc112eaadc54ceccfd29c874c3cba6`  
		Last Modified: Thu, 16 Jan 2020 01:20:45 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:5b078cef90be0c62cb568ecb3082a40aec4c4dec06b5e20a7ec7a8ee9b767640
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27237619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e91bf51008374529aea5705d41b18a65aa6573e3d7c90b7d1dcf446c09d33e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 18:42:29 GMT
ADD file:420ba790b06c89e0e028fee491442a3d61a67bb27d8b548820ed00940f41abb8 in / 
# Fri, 20 Mar 2020 18:42:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:42:33 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:42:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:42:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d55872e7f9efe88c9121c748ec231652e7bde16bce37c7d61bc808494cc99257`  
		Last Modified: Fri, 20 Mar 2020 18:43:16 GMT  
		Size: 27.2 MB (27204299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02987bfd1fe32596c731867a13d49a9152d762c34c69849dddaf97fb1704f27`  
		Last Modified: Fri, 20 Mar 2020 18:43:12 GMT  
		Size: 32.3 KB (32286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6459db5ba591c1c338d4d680ea401232e2def483b6e07db1bcf134e4df6bdbc2`  
		Last Modified: Fri, 20 Mar 2020 18:43:18 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6818c11522b95465a735052f0213a7a913b81557b6f5d42a7f21dbd25e0e36`  
		Last Modified: Fri, 20 Mar 2020 18:43:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
