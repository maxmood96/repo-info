<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:14.04`](#ubuntu1404)
-	[`ubuntu:16.04`](#ubuntu1604)
-	[`ubuntu:18.04`](#ubuntu1804)
-	[`ubuntu:19.10`](#ubuntu1910)
-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:bionic`](#ubuntubionic)
-	[`ubuntu:bionic-20200219`](#ubuntubionic-20200219)
-	[`ubuntu:devel`](#ubuntudevel)
-	[`ubuntu:eoan`](#ubuntueoan)
-	[`ubuntu:eoan-20200207`](#ubuntueoan-20200207)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20200115`](#ubuntufocal-20200115)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:rolling`](#ubunturolling)
-	[`ubuntu:trusty`](#ubuntutrusty)
-	[`ubuntu:trusty-20191217`](#ubuntutrusty-20191217)
-	[`ubuntu:xenial`](#ubuntuxenial)
-	[`ubuntu:xenial-20200212`](#ubuntuxenial-20200212)

## `ubuntu:14.04`

```console
$ docker pull ubuntu@sha256:ffc76f71dd8be8c9e222d420dc96901a07b61616689a44c7b3ef6a10b7213de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `ubuntu:14.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:bd0223687054d0f8884fc9e872392c6385a3195d612400495962e270b572ed06
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70764399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4f1fe62ff14a4c8119781d47a3739fa97c190e1df38e868794ad7a7cf50a48`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:23:42 GMT
ADD file:276b5d943a4d284f8a7b249176a31f93d95e852480c2b851de287e53ff622bba in / 
# Thu, 19 Dec 2019 04:23:43 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:23:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:23:45 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:23:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2e6e20c8e2e69fa5c3fcc310f419975cef5fbeb6f7f2fe1374071141281b6a06`  
		Last Modified: Wed, 18 Dec 2019 13:21:28 GMT  
		Size: 70.7 MB (70691577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30bb187ac3fc6c428f38d46409e7765a18dc6b59bc99914f0ba6936463307ec8`  
		Last Modified: Thu, 19 Dec 2019 04:25:41 GMT  
		Size: 72.7 KB (72659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a5bcc4a58aeed61f7dbe0a859aa4d37db24efd0c3ca58fb83605b5ad9044b5`  
		Last Modified: Thu, 19 Dec 2019 04:25:41 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:14.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:3fc5c28a28125d304462d5b9292d64a61041350304ac5deab416271b25d2e219
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64700967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67449d6018f689b7a2a501426015e0b13ada33b377c4c935c68453ce13706712`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:12:57 GMT
ADD file:e9d55e059869915743a8ca8e64582d23c48fe7e90e439daccd56d3e08e8673b4 in / 
# Thu, 19 Dec 2019 06:13:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:13:11 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:13:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:13:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0db3a87a3d7959895fd860c8b924980adda6e77f5d315b6676a4ac0e12518978`  
		Last Modified: Thu, 19 Dec 2019 06:16:01 GMT  
		Size: 64.6 MB (64624015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08b117a826b8d1ae5a5995f7eab5a89f5d582f24fa0016182b6502e42322179`  
		Last Modified: Thu, 19 Dec 2019 06:15:41 GMT  
		Size: 76.8 KB (76765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d5442ddd2dd606cb4dbd9c7243b10f6848c3ee77c176d1b0c667a2232b900c`  
		Last Modified: Thu, 19 Dec 2019 06:15:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:14.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:79b0f81ad6fc8f0bced3919beee0a79d60d1c8358911188d0787b1f155656d84
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66525501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104c127e75190df2e80d312958f30c9b7d2da0b5356f6c1e81e92dc85d3f9740`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:54:04 GMT
ADD file:b0eb0db52e323748ea9b8d7f8aecbc523a747619cd08663bab0fe60ab59bc60e in / 
# Thu, 19 Dec 2019 03:54:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:54:20 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:54:24 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:54:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d1a5a1e51f251c3431dec02e2cc8d157e92d1b46913708ce9e600747a6274977`  
		Last Modified: Thu, 19 Dec 2019 03:57:08 GMT  
		Size: 66.5 MB (66466219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9592077f8570e1222c5a6930a2fdc85b6b607b6c91230a5762c7bd6d84749e25`  
		Last Modified: Thu, 19 Dec 2019 03:56:48 GMT  
		Size: 59.1 KB (59094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b48639f381d2e2566e4c5bdb9792e8666ac2d2cc22918fda5751b8784ee5a5`  
		Last Modified: Thu, 19 Dec 2019 03:56:48 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:14.04` - linux; 386

```console
$ docker pull ubuntu@sha256:c8c1d2e6d53d94ef32e73354d146dc6e39c19ce8db2692356b3a6eef5a8ab956
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68445457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b01d68827fff530f34f6ff966823624238b7b90aec1bc82b2a9468da476d20e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:42:13 GMT
ADD file:e034601a525da53b0f39bb04d6e2264e2a592d0ae7c21e00697b9b62ca1efec9 in / 
# Thu, 19 Dec 2019 04:42:14 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:42:15 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:42:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:42:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:630712fe5783a35ad52a7026002143cb4f8fe65d34097dcaa4c4331b1b059a17`  
		Last Modified: Thu, 19 Dec 2019 04:44:02 GMT  
		Size: 68.4 MB (68380440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df46dbd3c04fd4a00981fd885f4d30a154ffa34bc8329bd448e9ca469df32e1`  
		Last Modified: Thu, 19 Dec 2019 04:43:42 GMT  
		Size: 64.9 KB (64855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4ca1e6e5f77f07de7e2107adcb062e1e72e84ce6ff83d5beeb5f84dfcc8418`  
		Last Modified: Thu, 19 Dec 2019 04:43:42 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:14.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:d00cd5726fb0c0523960683e45fe4bbb3807e68ef3edff693d44454aad69b85b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73443147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce257c90d69b5ed2a0955447f934ed3a9bc17c4f723fd6f61c0f55218e507b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:20:59 GMT
ADD file:581665e92c72c8638b40fe509de6479dc1a5d7b5ffe8d6706006178c406e35e2 in / 
# Thu, 19 Dec 2019 04:21:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bed4146d918c6c9a57bc3a8bf829e702975b0e53c7f25920fe9435b58ed6b64f`  
		Last Modified: Thu, 19 Dec 2019 04:26:52 GMT  
		Size: 73.4 MB (73379539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d17944a6ab7c0a73210db128de5b677c26f0d4c4c59f3bf6c76b7d1e847098`  
		Last Modified: Thu, 19 Dec 2019 04:26:36 GMT  
		Size: 63.4 KB (63423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d84211dbdd608b55c60bac1fab57fed3dd6de92653162fe123fd0154bcb03e`  
		Last Modified: Thu, 19 Dec 2019 04:26:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:16.04`

```console
$ docker pull ubuntu@sha256:e9938f45e51d9ff46e2b05a62e0546d0f07489b7f22fbc5288defe760599e38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:16.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:a98d9dcf3a34b2b78e78c61d003eb4d7a90d30fd54451686e2f0bd2ef5f602ac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44193271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77be327e4b63498e0faaa065d30d7c0e5499e42a09275ee19e27fd9a93cde7d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:22:27 GMT
ADD file:1f70668251e2e58cee0ff0c22ee805f8a269ac6f8934c07f7e89dca6cc1de3aa in / 
# Fri, 21 Feb 2020 22:22:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:22:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:22:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:22:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fe703b657a32e0046dce0ad2cb17172cbec8ba302edf370f5f28962bdb6216a9`  
		Last Modified: Thu, 13 Feb 2020 00:25:54 GMT  
		Size: 44.2 MB (44191726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df1fafd224fae3ba34a68dfc401f75bf6bc0c016fe36c61661ca5c7ad729ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a645a4b887f9613f80fae43432e46423f196a9952d11bb620bef2add7c4ed4ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57db7fe0b522b7a6069e769606e5ed0913a64e1e0d0030382a922ccf9449211e`  
		Last Modified: Fri, 21 Feb 2020 22:23:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:16.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:4faa0482a239dd826bab958f1ab22333568fcfa17a6a09c30806e69902878184
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38891892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6e0521581046453ce619849f0950fd5fe66a6fb5d85484f6b1b4b1191ca80f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:06:20 GMT
ADD file:7f245cd0bb5455d315f8d753720fab55e9ac41f68c7926b597663d3aeff3c8d4 in / 
# Fri, 21 Feb 2020 22:06:26 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:06:29 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:06:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:06:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:957d6015142d0d6fe598b45df39c8f36d0b86fe61fdb145603423c7d216e5f09`  
		Last Modified: Mon, 17 Feb 2020 15:45:30 GMT  
		Size: 38.9 MB (38890364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a31e0e10e55fa8dad735b48b598b86efb29be81ae44906466ea04a2fd13c6c7`  
		Last Modified: Fri, 21 Feb 2020 22:07:16 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c42599b1b7e867902cc3b4a6cd7cd76c9148ff337a0bc7861131b6176648b45`  
		Last Modified: Fri, 21 Feb 2020 22:07:16 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33654ecb4a4aa4b3b5b7f650b7aab38e3fe0d8d48d88c666f052f819016c3d55`  
		Last Modified: Fri, 21 Feb 2020 22:07:16 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:16.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:c7ca486dce6710697a81e2d08796a865f48c6525a3f81f3aa936a4905c9846be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39941860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f8c8b831940488436a2f3c43d61bac998bc01ed1dddf2a01c521ae8ea3f86c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:55:42 GMT
ADD file:61b91c95a686740a57740470b7a1fe64d2479c56c36c69ca1222d870e78d44cc in / 
# Fri, 21 Feb 2020 21:55:46 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 21:55:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:55:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:55:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a7bab9946de3c22ecccd832a0910adc2ffa82eea53f83c600d5ebce9e5422ad0`  
		Last Modified: Mon, 17 Feb 2020 15:45:27 GMT  
		Size: 39.9 MB (39940373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38630c4d9093f5b60806171ca7fa47a70d7ab28eeed25edfad43fb91d5f9f825`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef678cbe74d844c6a114c1158a8c8868b412b7c5ed3a4c159831975a4915db9`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78928743b0e778df64b15ac919705702ee0a080c2586f43c4349b35180de3c36`  
		Last Modified: Fri, 21 Feb 2020 21:56:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:16.04` - linux; 386

```console
$ docker pull ubuntu@sha256:f5c13e0e3239571970b3da937ff27b4062849f2764b23aa04e7127778370ad09
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44174809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1aa297bcabc1cab7710748f5ad4316c2717b5560feff4ecdaf0d57142c6579c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:39:40 GMT
ADD file:118ef8482188b21216adb7af11584f08a24c46958f4f3385032b371a60bb66e1 in / 
# Fri, 21 Feb 2020 21:39:41 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 21:39:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:39:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:39:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:968d3cde0fa07bedc833984b32995ad11d8a375f98616a4ff74ae3ee309ad1a2`  
		Last Modified: Mon, 17 Feb 2020 15:45:30 GMT  
		Size: 44.2 MB (44173277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d65b39906d3579ee3e992072b579dd8168fe81974a0428f27d1db39c6948dbc`  
		Last Modified: Fri, 21 Feb 2020 21:40:16 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd64e0411faf07b0fa30439f0364aa9ef2649b21bf88f1ee9f81cff5342eccad`  
		Last Modified: Fri, 21 Feb 2020 21:40:15 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888871f3d4aa08404cffac4c555fe0c9014444415fe65fad37a6a40d4965c5a2`  
		Last Modified: Fri, 21 Feb 2020 21:40:16 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:16.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a2658945e589dd8ec52d7374cc5d4c0a3391a9d9d2a69ac91bcb558bd8da6a31
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46102397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a12016288f21e2de76a81de4bc4029231976317d36f25be75701938e1fc0049`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:32:24 GMT
ADD file:7f14eb8a42273a36130d75b1d935b9617db245cb718ab5b6796ba53ab7a9aa05 in / 
# Fri, 21 Feb 2020 22:32:33 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:32:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:32:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:32:51 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0abc6f550884cf7de4f0adb093a671df9fbff6fa630d3c2bfb1fd80c04c51ad1`  
		Last Modified: Mon, 17 Feb 2020 15:46:15 GMT  
		Size: 46.1 MB (46100906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0741e5703c97bf375e97b9bee6d26a78eb4457d7e6d12661e23f7dd09f8d26b0`  
		Last Modified: Fri, 21 Feb 2020 22:33:56 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed4e13c7b7237db460c7250ffec446cd033597c349d538f1a3bef2c61936f89`  
		Last Modified: Fri, 21 Feb 2020 22:33:56 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9acb6be6f2007b0d8af5a84186b3d866dbcb1eec846431df08803f6f5fa62f9`  
		Last Modified: Fri, 21 Feb 2020 22:33:56 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:16.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:fbbecfc4f9fc56b050d0a8617ff5e0aecfa1bfc6e23c041a574c19c90183bc48
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42815078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99098b69958a3ec33c58573f85484e591633a9110eb2aa3faccb0e5cbdbbadf9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:58:38 GMT
ADD file:2da08b5719e8f84bf1322ff4b7babef0750ca9f09ec09fafb2dd49471656ab45 in / 
# Fri, 21 Feb 2020 21:58:47 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 21:58:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:58:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:58:51 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5d1c06e617a886003bdc553ea5fb88f3d1b9f090ccd01b8f11f59128221a248f`  
		Last Modified: Mon, 17 Feb 2020 15:46:24 GMT  
		Size: 42.8 MB (42813593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014396d85ca8cff40d6f829c1dd4b726456f22ed02b58fc32fda25427a08540b`  
		Last Modified: Fri, 21 Feb 2020 21:59:51 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd0d716f0f324aed318dd9aa0cbe1f47a5ac863a633df8d39b7760f74d2adff`  
		Last Modified: Fri, 21 Feb 2020 21:59:51 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb96b2c9e76d5516a980ea87b6cd16e5f0fd5b6b47b4f4d4a694aab15d36862`  
		Last Modified: Fri, 21 Feb 2020 21:59:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:18.04`

```console
$ docker pull ubuntu@sha256:04d48df82c938587820d7b6006f5071dbbffceb7ca01d2814f81857c631d44df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:18.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:0925d086715714114c1988f7c947db94064fd385e171a63c07730f1fa014e6f9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26728476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72300a873c2ca11c70d0c8642177ce76ff69ae04d61a5813ef58d40ff66e3e7c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:18.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:60a99a670b980963e4a9d882f631cba5d26ba5d14ccba2aa82a4e1f4d084fb1f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22312168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981c0bc3c335271c725c2d7097fbe843453458690f8016f18ea3e15139cba12d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:04:48 GMT
ADD file:548fc3249b705bf3e94efcc50c1c9141e03d1ce51edfc194a84bd631d1a7b6d4 in / 
# Fri, 21 Feb 2020 22:04:52 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:04:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:05:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:05:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b9b5ae93466ea2cca8f47e7e02dc1907faaaae6ed617360e47259eb4cac4d0a7`  
		Last Modified: Fri, 21 Feb 2020 22:06:53 GMT  
		Size: 22.3 MB (22275658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8983199234a3f5beecbe2be6e21b4a49e67dd5726e7080e999c6f2cea91bc2`  
		Last Modified: Fri, 21 Feb 2020 22:06:47 GMT  
		Size: 35.5 KB (35470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e76f87f706a4e3e6b5f3d9fabd021b46b875dc9058e26d31877057069115333`  
		Last Modified: Fri, 21 Feb 2020 22:06:47 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b196ba84f492bbca6bb4979ae6e8d2d3a952559cdf3dfd11e99c3a4c11aa0891`  
		Last Modified: Fri, 21 Feb 2020 22:06:47 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:18.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:fab7c78ecd4c52e801b8a597846ec5c00ff2e4f4d1d92f6af1c8390eabc1d2d5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23757379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c574f8f488657f27c856bda8b44aa9d0b5ad03e1fc6a88a19ec9e57e9624ab34`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:18.04` - linux; 386

```console
$ docker pull ubuntu@sha256:4d07b5b0cd47c06a3ca847536a3e05901c6bf9d9f52dbb0e6a7fff9141453f11
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27159454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d2962d1c2fb91f3b025c85a529da96d4a4788d8685e7aff66144510f0efec8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:39:03 GMT
ADD file:df203cc2574204629c69613fcea4942faa0f9224ff0c8bacb908b85d73604628 in / 
# Fri, 21 Feb 2020 21:39:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:39:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:39:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:39:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ddc482e6a4fa5e364980052ab9f5d236f29ae9b217ed672b3dba44669f4041de`  
		Last Modified: Fri, 21 Feb 2020 21:39:58 GMT  
		Size: 27.1 MB (27123823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d2b8bf2fa50513ca7c508e44ac1a15c7ec42b1a3369a91380663868309ab46`  
		Last Modified: Fri, 21 Feb 2020 21:39:52 GMT  
		Size: 34.6 KB (34625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84c193628e4067b419327ffa1bfef4b73161d9b1e3ce1e4ee83e714fd1d14e8`  
		Last Modified: Fri, 21 Feb 2020 21:39:52 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5271c42d486e4bb18cadbdf885d057c29384a032113047030f7c4bd6253bbf10`  
		Last Modified: Fri, 21 Feb 2020 21:39:52 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:18.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:1b3520a2868bd5d82cbf432931ffc3131d99af2d3157bdcf2757b2896e0be86b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30437337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0cab33facfc5176f669f524b4c2b170605e87fa05eeabe5203cbd84fbe52e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:18.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:a837741679960532ff2a22c9ba80964a8b0246add966521ffd5427487ea21011
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25402893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3990be7b573ae1044b44f6c43736c913c89b9ba25e781a196f4fc19687ded4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:57:46 GMT
ADD file:7925c9b35ffa1870e7d336ddcdd6c3434715178c7d08ff2ce9796b651302c347 in / 
# Fri, 21 Feb 2020 21:57:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:57:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:57:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:57:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b84fcb37dc33cf7416e0f1cf1219e16a15ab0d1c3aa4638d362f19c2679451de`  
		Last Modified: Fri, 21 Feb 2020 21:59:09 GMT  
		Size: 25.4 MB (25365672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9594931f903b7b3c4f5cb63196d29d715c50b567c128a5572131c12a25f04139`  
		Last Modified: Fri, 21 Feb 2020 21:59:06 GMT  
		Size: 36.2 KB (36186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66af13675c2330803d61d2198bb4f69c36bb7eed2d2b2bc3660fed8e873dce59`  
		Last Modified: Fri, 21 Feb 2020 21:59:11 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae0fb7b2ee5c5bc387374bdd08f53541bdfcf678d9b9f83489c3923af65fed0`  
		Last Modified: Fri, 21 Feb 2020 21:59:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:19.10`

```console
$ docker pull ubuntu@sha256:ed677609acf0dd2e785d7994dd4786ef64872dd26e3ab7fab716a5ba4002ac82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:19.10` - linux; amd64

```console
$ docker pull ubuntu@sha256:6dbeda79f38da94149cf5c3f75828df544f96491fe05c192094b965d0a16dfef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28308310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f82834f04c624aa37c017e808c8ff2083c10c7a0ac527550ea0cae73a7a9cf8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:21:11 GMT
ADD file:49bd1c0bfe89a93a193774bfd334bc1151f0dca95849f81d1ac353673399585c in / 
# Fri, 21 Feb 2020 22:21:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:21:14 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:21:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:21:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a9c68053c4b2379a9ad5b7306236a13f469cfd18e727dd4e76470af366445b45`  
		Last Modified: Mon, 10 Feb 2020 15:41:51 GMT  
		Size: 28.3 MB (28276663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9c43fe7e5dcfee42adb18336072154126bc052cc1c578e64d27a8aeaabc97`  
		Last Modified: Fri, 21 Feb 2020 22:23:01 GMT  
		Size: 30.6 KB (30633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90491034717d4c1d1e0b37a4bde4f3a0e26630af7d360b7c0248660ccbef59d5`  
		Last Modified: Fri, 21 Feb 2020 22:23:01 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781c6270286751c77c20928c68fa3edd532f0d3d11108db32020c8840f0ea6cb`  
		Last Modified: Fri, 21 Feb 2020 22:23:01 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:19.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d945255334dfa76d5f4a2371c88c4e03f01fe16e9d52cac0c25febf82661ca98
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23767910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a395321a14de7f7719c4d101b74b3f6c8e10e8a6469e417d02a4ed12198cb85`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:05:21 GMT
ADD file:cd4de1fcdceb95824a887d3d27d3c110261a719ded9d99031dd00e1568494c4a in / 
# Fri, 21 Feb 2020 22:05:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:05:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:05:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:05:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bd94fa49cb09c9859edca1e49f6f1cbac0fd492ae56f34b62332a783ad7b68d7`  
		Last Modified: Mon, 10 Feb 2020 15:42:56 GMT  
		Size: 23.7 MB (23736258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1ca8c199cca8211202b60f587659b529101b98194226cb6735febcac6db3f9`  
		Last Modified: Fri, 21 Feb 2020 22:07:02 GMT  
		Size: 30.6 KB (30612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefecf0dd0df3e68f7f80336d560e65ce665036fe83576e4f801047dfd4a9d9f`  
		Last Modified: Fri, 21 Feb 2020 22:07:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8017e57ad339bf8ddfdfd30a79d5096b13c3886781f1078e0303a89cb818f539`  
		Last Modified: Fri, 21 Feb 2020 22:07:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:19.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:5c60568f428d8e77e38adc410cd4b8cf02b96a2e9de93cbc829d83dc11d11df8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26901121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c984153802b54032ee6018f4f5156c8f0455ec3424e728366872907e7199b55`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:42 GMT
ADD file:29003dce8015529919e9efa92862cda5f1c4a394bebe00e7d9bca8894f23bad2 in / 
# Fri, 21 Feb 2020 21:54:45 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:79693b41cb22c8dae6603b2bf443392e179fff02152f5b8fb25e9ebc2f36ca37`  
		Last Modified: Mon, 10 Feb 2020 15:42:23 GMT  
		Size: 26.9 MB (26869627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085004cd2eaec5c5d7d85da739c356d4035b607ff5d3fa3de249827468ac04e4`  
		Last Modified: Fri, 21 Feb 2020 21:56:23 GMT  
		Size: 30.5 KB (30457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9727781305391dcb29dd0f8d61651a751c07d2a32abd0c1ce145117a9416eca`  
		Last Modified: Fri, 21 Feb 2020 21:56:23 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a75366ff852d9cfecac92c78537e6ac39629896a81c09dd9051a924c9363573`  
		Last Modified: Fri, 21 Feb 2020 21:56:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:19.10` - linux; 386

```console
$ docker pull ubuntu@sha256:a30685e91c6c7a9e84380699ab7c26cfb94cc690bc2e32295e3cdcdee483e096
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29076596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab681b0e86110fa97d2a102218e98b701d5dbd78677f73c8bf5d866d689f41f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:39:17 GMT
ADD file:8712d700c1cc817afa2abe23b077498c4ec2332067a7d38e5d3425454373e193 in / 
# Fri, 21 Feb 2020 21:39:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:39:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:39:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:39:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:df36fe298056793eae27d9efb7b1d54a4d69b16ad6a7d62fc186a8e7727db39f`  
		Last Modified: Mon, 10 Feb 2020 15:43:00 GMT  
		Size: 29.0 MB (29044887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b3578b2a446d70c838e7144c5d77d423461b43e78e2e75107f2764511bed0e`  
		Last Modified: Fri, 21 Feb 2020 21:40:03 GMT  
		Size: 30.7 KB (30699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb0394aa2bb495dd3bef1779832e0d27d6d292aaf3f2740c17564759aa47ef2`  
		Last Modified: Fri, 21 Feb 2020 21:40:04 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7e86bd657e678ce69ee3e2c2e502097c3353cd8484841245225e4d598489c3`  
		Last Modified: Fri, 21 Feb 2020 21:40:04 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:19.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:7aac2b62da78b633b56555f4b6ed263abd3f8508ed956dcabeb9911e49d21628
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33018012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b353da7a159efbc9b738e384fd723b7680fbf03f55399e3d8817abebee598bb3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:31:25 GMT
ADD file:d3168601bc3d213abcd3bb57ad2824d9099de51d8775c8d356460e12d15a26a1 in / 
# Fri, 21 Feb 2020 22:31:31 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:31:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:31:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:31:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:051dbc8b8e4ed99bbd1a698a7e4bd348c280e0ddaf417786fbedd99ca22cb144`  
		Last Modified: Mon, 10 Feb 2020 15:43:20 GMT  
		Size: 33.0 MB (32986499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f53f3c55500976229df5bc71ead0d2723cda57b2c606b6e906de3b7b5c2ad80`  
		Last Modified: Fri, 21 Feb 2020 22:33:32 GMT  
		Size: 30.5 KB (30477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8143f400347b6df364214d634dbcd1db12d526040a868183289501481e13f05`  
		Last Modified: Fri, 21 Feb 2020 22:33:32 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd6e204830d0f5b1439e36d1a6af90c8b04d96fb8b4bcacdd6f611706a97881`  
		Last Modified: Fri, 21 Feb 2020 22:33:33 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:19.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:61c91aa6c4837cd47a0b2d24c647e13cc37c89645193f627d40a7495bb65a82b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26714685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358f272d76821bf4cec9984f7c8909492a357d0cd192dd6dce48abe447f61792`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:58:06 GMT
ADD file:14df51909823644041c1e18fdd62b5c5598c3f037712b7a3db85d68d65c12f9a in / 
# Fri, 21 Feb 2020 21:58:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:58:14 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:58:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:58:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cb19e5b8123e1f3303c72ff2231d83a7282d4d798635f63093ee0c6329d5bf4b`  
		Last Modified: Mon, 10 Feb 2020 15:44:30 GMT  
		Size: 26.7 MB (26682544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ad82f1f4a65553adb6d26ef9b25aebaacb039124b98ba6867d7a27d8dc25f9`  
		Last Modified: Fri, 21 Feb 2020 21:59:28 GMT  
		Size: 31.1 KB (31106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2a7e86bc0f07353acc2cc206b74b5d9825041b4fbd0c0b8de71419ec7b661b`  
		Last Modified: Fri, 21 Feb 2020 21:59:33 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7cae483f07e12cbe0fc9a0bc8dceaecbe7ec0fa3ed9215d663ec3ac10210ab`  
		Last Modified: Fri, 21 Feb 2020 21:59:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:7922db6447e9d1470e3bf821e8ff228d70c3593e822e980c58bf9185821ac645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:20.04` - linux; amd64

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

### `ubuntu:20.04` - linux; arm variant v7

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

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:64a3d51cb381a58adf45f5037a03deee2e22668d8e2f19a222e78c16969229a6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26978462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb1d69f19cd3f982e87a8dfaf75277516c426a7b0f2b633ffa2607d61cc4346`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 00:42:08 GMT
ADD file:3f5a5ff4e005ffd96a9a56c4234117276101fd4cd6b87b503fad5d3f02319d92 in / 
# Thu, 16 Jan 2020 00:42:11 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 00:42:13 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 00:42:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 00:42:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d0804342421c30932eee7f90821efd1e7dac9398a9cac78b662e33b2a3faeeb3`  
		Last Modified: Thu, 16 Jan 2020 00:44:12 GMT  
		Size: 26.9 MB (26946995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d926bd5118332af73957eb2925d9433286ec09620aa22ed01eaca19e89d76a`  
		Last Modified: Thu, 16 Jan 2020 00:44:05 GMT  
		Size: 30.4 KB (30431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3420a5d9e296a9e1a3d258bef98c8dd8f40f3b0767cdb42b424acdee2b47b2b9`  
		Last Modified: Thu, 16 Jan 2020 00:44:05 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86fe98d56e47198b1f7b547c1dfac333460f1aa23177768180ca62714aaa1d2`  
		Last Modified: Thu, 16 Jan 2020 00:44:05 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:20.04` - linux; ppc64le

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

### `ubuntu:20.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:7345a0001b12b9d537ae2936205827ddd6a9aac6616943e67f9623d2ef338c52
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26957237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9394f7a1e4c93e9b65700e3412aff5cd02302a0d4db349809f9257fdd411c040`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 00:45:47 GMT
ADD file:5fbe981ed0834a4a7ca86c449eacf27c014fe832bba12eda0aa98718b927fc45 in / 
# Thu, 16 Jan 2020 00:45:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 00:45:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 00:45:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 00:45:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9718365a56944fa9db6c418110acfb6a7170f892e2f5d8bb0b66b3dbb538ad2a`  
		Last Modified: Thu, 16 Jan 2020 00:46:51 GMT  
		Size: 26.9 MB (26925143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1be672e2a8be868977dac18b2ad998262f7716cc1bda9f79c380e87d70c8d8`  
		Last Modified: Thu, 16 Jan 2020 00:46:44 GMT  
		Size: 31.1 KB (31089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08de0d4260b235271919468fdd3074a90da7692eb0d0575521cb1b18dd36525d`  
		Last Modified: Thu, 16 Jan 2020 00:46:44 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9d5d6c35a086753c3e88803888682d2da2f6cea21681a1d304e5cd8c8f0846`  
		Last Modified: Thu, 16 Jan 2020 00:46:44 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:bionic`

```console
$ docker pull ubuntu@sha256:04d48df82c938587820d7b6006f5071dbbffceb7ca01d2814f81857c631d44df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:bionic` - linux; amd64

```console
$ docker pull ubuntu@sha256:0925d086715714114c1988f7c947db94064fd385e171a63c07730f1fa014e6f9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26728476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72300a873c2ca11c70d0c8642177ce76ff69ae04d61a5813ef58d40ff66e3e7c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:60a99a670b980963e4a9d882f631cba5d26ba5d14ccba2aa82a4e1f4d084fb1f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22312168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981c0bc3c335271c725c2d7097fbe843453458690f8016f18ea3e15139cba12d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:04:48 GMT
ADD file:548fc3249b705bf3e94efcc50c1c9141e03d1ce51edfc194a84bd631d1a7b6d4 in / 
# Fri, 21 Feb 2020 22:04:52 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:04:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:05:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:05:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b9b5ae93466ea2cca8f47e7e02dc1907faaaae6ed617360e47259eb4cac4d0a7`  
		Last Modified: Fri, 21 Feb 2020 22:06:53 GMT  
		Size: 22.3 MB (22275658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8983199234a3f5beecbe2be6e21b4a49e67dd5726e7080e999c6f2cea91bc2`  
		Last Modified: Fri, 21 Feb 2020 22:06:47 GMT  
		Size: 35.5 KB (35470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e76f87f706a4e3e6b5f3d9fabd021b46b875dc9058e26d31877057069115333`  
		Last Modified: Fri, 21 Feb 2020 22:06:47 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b196ba84f492bbca6bb4979ae6e8d2d3a952559cdf3dfd11e99c3a4c11aa0891`  
		Last Modified: Fri, 21 Feb 2020 22:06:47 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:fab7c78ecd4c52e801b8a597846ec5c00ff2e4f4d1d92f6af1c8390eabc1d2d5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23757379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c574f8f488657f27c856bda8b44aa9d0b5ad03e1fc6a88a19ec9e57e9624ab34`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic` - linux; 386

```console
$ docker pull ubuntu@sha256:4d07b5b0cd47c06a3ca847536a3e05901c6bf9d9f52dbb0e6a7fff9141453f11
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27159454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d2962d1c2fb91f3b025c85a529da96d4a4788d8685e7aff66144510f0efec8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:39:03 GMT
ADD file:df203cc2574204629c69613fcea4942faa0f9224ff0c8bacb908b85d73604628 in / 
# Fri, 21 Feb 2020 21:39:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:39:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:39:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:39:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ddc482e6a4fa5e364980052ab9f5d236f29ae9b217ed672b3dba44669f4041de`  
		Last Modified: Fri, 21 Feb 2020 21:39:58 GMT  
		Size: 27.1 MB (27123823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d2b8bf2fa50513ca7c508e44ac1a15c7ec42b1a3369a91380663868309ab46`  
		Last Modified: Fri, 21 Feb 2020 21:39:52 GMT  
		Size: 34.6 KB (34625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84c193628e4067b419327ffa1bfef4b73161d9b1e3ce1e4ee83e714fd1d14e8`  
		Last Modified: Fri, 21 Feb 2020 21:39:52 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5271c42d486e4bb18cadbdf885d057c29384a032113047030f7c4bd6253bbf10`  
		Last Modified: Fri, 21 Feb 2020 21:39:52 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:1b3520a2868bd5d82cbf432931ffc3131d99af2d3157bdcf2757b2896e0be86b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30437337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0cab33facfc5176f669f524b4c2b170605e87fa05eeabe5203cbd84fbe52e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic` - linux; s390x

```console
$ docker pull ubuntu@sha256:a837741679960532ff2a22c9ba80964a8b0246add966521ffd5427487ea21011
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25402893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3990be7b573ae1044b44f6c43736c913c89b9ba25e781a196f4fc19687ded4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:57:46 GMT
ADD file:7925c9b35ffa1870e7d336ddcdd6c3434715178c7d08ff2ce9796b651302c347 in / 
# Fri, 21 Feb 2020 21:57:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:57:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:57:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:57:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b84fcb37dc33cf7416e0f1cf1219e16a15ab0d1c3aa4638d362f19c2679451de`  
		Last Modified: Fri, 21 Feb 2020 21:59:09 GMT  
		Size: 25.4 MB (25365672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9594931f903b7b3c4f5cb63196d29d715c50b567c128a5572131c12a25f04139`  
		Last Modified: Fri, 21 Feb 2020 21:59:06 GMT  
		Size: 36.2 KB (36186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66af13675c2330803d61d2198bb4f69c36bb7eed2d2b2bc3660fed8e873dce59`  
		Last Modified: Fri, 21 Feb 2020 21:59:11 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae0fb7b2ee5c5bc387374bdd08f53541bdfcf678d9b9f83489c3923af65fed0`  
		Last Modified: Fri, 21 Feb 2020 21:59:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:bionic-20200219`

```console
$ docker pull ubuntu@sha256:04d48df82c938587820d7b6006f5071dbbffceb7ca01d2814f81857c631d44df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:bionic-20200219` - linux; amd64

```console
$ docker pull ubuntu@sha256:0925d086715714114c1988f7c947db94064fd385e171a63c07730f1fa014e6f9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26728476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72300a873c2ca11c70d0c8642177ce76ff69ae04d61a5813ef58d40ff66e3e7c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic-20200219` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:60a99a670b980963e4a9d882f631cba5d26ba5d14ccba2aa82a4e1f4d084fb1f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22312168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981c0bc3c335271c725c2d7097fbe843453458690f8016f18ea3e15139cba12d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:04:48 GMT
ADD file:548fc3249b705bf3e94efcc50c1c9141e03d1ce51edfc194a84bd631d1a7b6d4 in / 
# Fri, 21 Feb 2020 22:04:52 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:04:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:05:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:05:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b9b5ae93466ea2cca8f47e7e02dc1907faaaae6ed617360e47259eb4cac4d0a7`  
		Last Modified: Fri, 21 Feb 2020 22:06:53 GMT  
		Size: 22.3 MB (22275658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8983199234a3f5beecbe2be6e21b4a49e67dd5726e7080e999c6f2cea91bc2`  
		Last Modified: Fri, 21 Feb 2020 22:06:47 GMT  
		Size: 35.5 KB (35470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e76f87f706a4e3e6b5f3d9fabd021b46b875dc9058e26d31877057069115333`  
		Last Modified: Fri, 21 Feb 2020 22:06:47 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b196ba84f492bbca6bb4979ae6e8d2d3a952559cdf3dfd11e99c3a4c11aa0891`  
		Last Modified: Fri, 21 Feb 2020 22:06:47 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic-20200219` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:fab7c78ecd4c52e801b8a597846ec5c00ff2e4f4d1d92f6af1c8390eabc1d2d5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23757379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c574f8f488657f27c856bda8b44aa9d0b5ad03e1fc6a88a19ec9e57e9624ab34`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic-20200219` - linux; 386

```console
$ docker pull ubuntu@sha256:4d07b5b0cd47c06a3ca847536a3e05901c6bf9d9f52dbb0e6a7fff9141453f11
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27159454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d2962d1c2fb91f3b025c85a529da96d4a4788d8685e7aff66144510f0efec8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:39:03 GMT
ADD file:df203cc2574204629c69613fcea4942faa0f9224ff0c8bacb908b85d73604628 in / 
# Fri, 21 Feb 2020 21:39:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:39:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:39:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:39:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ddc482e6a4fa5e364980052ab9f5d236f29ae9b217ed672b3dba44669f4041de`  
		Last Modified: Fri, 21 Feb 2020 21:39:58 GMT  
		Size: 27.1 MB (27123823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d2b8bf2fa50513ca7c508e44ac1a15c7ec42b1a3369a91380663868309ab46`  
		Last Modified: Fri, 21 Feb 2020 21:39:52 GMT  
		Size: 34.6 KB (34625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84c193628e4067b419327ffa1bfef4b73161d9b1e3ce1e4ee83e714fd1d14e8`  
		Last Modified: Fri, 21 Feb 2020 21:39:52 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5271c42d486e4bb18cadbdf885d057c29384a032113047030f7c4bd6253bbf10`  
		Last Modified: Fri, 21 Feb 2020 21:39:52 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic-20200219` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:1b3520a2868bd5d82cbf432931ffc3131d99af2d3157bdcf2757b2896e0be86b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30437337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0cab33facfc5176f669f524b4c2b170605e87fa05eeabe5203cbd84fbe52e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic-20200219` - linux; s390x

```console
$ docker pull ubuntu@sha256:a837741679960532ff2a22c9ba80964a8b0246add966521ffd5427487ea21011
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25402893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3990be7b573ae1044b44f6c43736c913c89b9ba25e781a196f4fc19687ded4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:57:46 GMT
ADD file:7925c9b35ffa1870e7d336ddcdd6c3434715178c7d08ff2ce9796b651302c347 in / 
# Fri, 21 Feb 2020 21:57:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:57:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:57:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:57:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b84fcb37dc33cf7416e0f1cf1219e16a15ab0d1c3aa4638d362f19c2679451de`  
		Last Modified: Fri, 21 Feb 2020 21:59:09 GMT  
		Size: 25.4 MB (25365672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9594931f903b7b3c4f5cb63196d29d715c50b567c128a5572131c12a25f04139`  
		Last Modified: Fri, 21 Feb 2020 21:59:06 GMT  
		Size: 36.2 KB (36186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66af13675c2330803d61d2198bb4f69c36bb7eed2d2b2bc3660fed8e873dce59`  
		Last Modified: Fri, 21 Feb 2020 21:59:11 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae0fb7b2ee5c5bc387374bdd08f53541bdfcf678d9b9f83489c3923af65fed0`  
		Last Modified: Fri, 21 Feb 2020 21:59:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:7922db6447e9d1470e3bf821e8ff228d70c3593e822e980c58bf9185821ac645
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
$ docker pull ubuntu@sha256:64a3d51cb381a58adf45f5037a03deee2e22668d8e2f19a222e78c16969229a6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26978462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb1d69f19cd3f982e87a8dfaf75277516c426a7b0f2b633ffa2607d61cc4346`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 00:42:08 GMT
ADD file:3f5a5ff4e005ffd96a9a56c4234117276101fd4cd6b87b503fad5d3f02319d92 in / 
# Thu, 16 Jan 2020 00:42:11 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 00:42:13 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 00:42:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 00:42:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d0804342421c30932eee7f90821efd1e7dac9398a9cac78b662e33b2a3faeeb3`  
		Last Modified: Thu, 16 Jan 2020 00:44:12 GMT  
		Size: 26.9 MB (26946995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d926bd5118332af73957eb2925d9433286ec09620aa22ed01eaca19e89d76a`  
		Last Modified: Thu, 16 Jan 2020 00:44:05 GMT  
		Size: 30.4 KB (30431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3420a5d9e296a9e1a3d258bef98c8dd8f40f3b0767cdb42b424acdee2b47b2b9`  
		Last Modified: Thu, 16 Jan 2020 00:44:05 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86fe98d56e47198b1f7b547c1dfac333460f1aa23177768180ca62714aaa1d2`  
		Last Modified: Thu, 16 Jan 2020 00:44:05 GMT  
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
$ docker pull ubuntu@sha256:7345a0001b12b9d537ae2936205827ddd6a9aac6616943e67f9623d2ef338c52
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26957237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9394f7a1e4c93e9b65700e3412aff5cd02302a0d4db349809f9257fdd411c040`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 00:45:47 GMT
ADD file:5fbe981ed0834a4a7ca86c449eacf27c014fe832bba12eda0aa98718b927fc45 in / 
# Thu, 16 Jan 2020 00:45:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 00:45:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 00:45:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 00:45:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9718365a56944fa9db6c418110acfb6a7170f892e2f5d8bb0b66b3dbb538ad2a`  
		Last Modified: Thu, 16 Jan 2020 00:46:51 GMT  
		Size: 26.9 MB (26925143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1be672e2a8be868977dac18b2ad998262f7716cc1bda9f79c380e87d70c8d8`  
		Last Modified: Thu, 16 Jan 2020 00:46:44 GMT  
		Size: 31.1 KB (31089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08de0d4260b235271919468fdd3074a90da7692eb0d0575521cb1b18dd36525d`  
		Last Modified: Thu, 16 Jan 2020 00:46:44 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9d5d6c35a086753c3e88803888682d2da2f6cea21681a1d304e5cd8c8f0846`  
		Last Modified: Thu, 16 Jan 2020 00:46:44 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:eoan`

```console
$ docker pull ubuntu@sha256:ed677609acf0dd2e785d7994dd4786ef64872dd26e3ab7fab716a5ba4002ac82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:eoan` - linux; amd64

```console
$ docker pull ubuntu@sha256:6dbeda79f38da94149cf5c3f75828df544f96491fe05c192094b965d0a16dfef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28308310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f82834f04c624aa37c017e808c8ff2083c10c7a0ac527550ea0cae73a7a9cf8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:21:11 GMT
ADD file:49bd1c0bfe89a93a193774bfd334bc1151f0dca95849f81d1ac353673399585c in / 
# Fri, 21 Feb 2020 22:21:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:21:14 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:21:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:21:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a9c68053c4b2379a9ad5b7306236a13f469cfd18e727dd4e76470af366445b45`  
		Last Modified: Mon, 10 Feb 2020 15:41:51 GMT  
		Size: 28.3 MB (28276663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9c43fe7e5dcfee42adb18336072154126bc052cc1c578e64d27a8aeaabc97`  
		Last Modified: Fri, 21 Feb 2020 22:23:01 GMT  
		Size: 30.6 KB (30633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90491034717d4c1d1e0b37a4bde4f3a0e26630af7d360b7c0248660ccbef59d5`  
		Last Modified: Fri, 21 Feb 2020 22:23:01 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781c6270286751c77c20928c68fa3edd532f0d3d11108db32020c8840f0ea6cb`  
		Last Modified: Fri, 21 Feb 2020 22:23:01 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:eoan` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d945255334dfa76d5f4a2371c88c4e03f01fe16e9d52cac0c25febf82661ca98
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23767910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a395321a14de7f7719c4d101b74b3f6c8e10e8a6469e417d02a4ed12198cb85`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:05:21 GMT
ADD file:cd4de1fcdceb95824a887d3d27d3c110261a719ded9d99031dd00e1568494c4a in / 
# Fri, 21 Feb 2020 22:05:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:05:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:05:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:05:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bd94fa49cb09c9859edca1e49f6f1cbac0fd492ae56f34b62332a783ad7b68d7`  
		Last Modified: Mon, 10 Feb 2020 15:42:56 GMT  
		Size: 23.7 MB (23736258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1ca8c199cca8211202b60f587659b529101b98194226cb6735febcac6db3f9`  
		Last Modified: Fri, 21 Feb 2020 22:07:02 GMT  
		Size: 30.6 KB (30612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefecf0dd0df3e68f7f80336d560e65ce665036fe83576e4f801047dfd4a9d9f`  
		Last Modified: Fri, 21 Feb 2020 22:07:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8017e57ad339bf8ddfdfd30a79d5096b13c3886781f1078e0303a89cb818f539`  
		Last Modified: Fri, 21 Feb 2020 22:07:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:eoan` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:5c60568f428d8e77e38adc410cd4b8cf02b96a2e9de93cbc829d83dc11d11df8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26901121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c984153802b54032ee6018f4f5156c8f0455ec3424e728366872907e7199b55`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:42 GMT
ADD file:29003dce8015529919e9efa92862cda5f1c4a394bebe00e7d9bca8894f23bad2 in / 
# Fri, 21 Feb 2020 21:54:45 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:79693b41cb22c8dae6603b2bf443392e179fff02152f5b8fb25e9ebc2f36ca37`  
		Last Modified: Mon, 10 Feb 2020 15:42:23 GMT  
		Size: 26.9 MB (26869627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085004cd2eaec5c5d7d85da739c356d4035b607ff5d3fa3de249827468ac04e4`  
		Last Modified: Fri, 21 Feb 2020 21:56:23 GMT  
		Size: 30.5 KB (30457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9727781305391dcb29dd0f8d61651a751c07d2a32abd0c1ce145117a9416eca`  
		Last Modified: Fri, 21 Feb 2020 21:56:23 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a75366ff852d9cfecac92c78537e6ac39629896a81c09dd9051a924c9363573`  
		Last Modified: Fri, 21 Feb 2020 21:56:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:eoan` - linux; 386

```console
$ docker pull ubuntu@sha256:a30685e91c6c7a9e84380699ab7c26cfb94cc690bc2e32295e3cdcdee483e096
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29076596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab681b0e86110fa97d2a102218e98b701d5dbd78677f73c8bf5d866d689f41f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:39:17 GMT
ADD file:8712d700c1cc817afa2abe23b077498c4ec2332067a7d38e5d3425454373e193 in / 
# Fri, 21 Feb 2020 21:39:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:39:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:39:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:39:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:df36fe298056793eae27d9efb7b1d54a4d69b16ad6a7d62fc186a8e7727db39f`  
		Last Modified: Mon, 10 Feb 2020 15:43:00 GMT  
		Size: 29.0 MB (29044887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b3578b2a446d70c838e7144c5d77d423461b43e78e2e75107f2764511bed0e`  
		Last Modified: Fri, 21 Feb 2020 21:40:03 GMT  
		Size: 30.7 KB (30699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb0394aa2bb495dd3bef1779832e0d27d6d292aaf3f2740c17564759aa47ef2`  
		Last Modified: Fri, 21 Feb 2020 21:40:04 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7e86bd657e678ce69ee3e2c2e502097c3353cd8484841245225e4d598489c3`  
		Last Modified: Fri, 21 Feb 2020 21:40:04 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:eoan` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:7aac2b62da78b633b56555f4b6ed263abd3f8508ed956dcabeb9911e49d21628
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33018012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b353da7a159efbc9b738e384fd723b7680fbf03f55399e3d8817abebee598bb3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:31:25 GMT
ADD file:d3168601bc3d213abcd3bb57ad2824d9099de51d8775c8d356460e12d15a26a1 in / 
# Fri, 21 Feb 2020 22:31:31 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:31:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:31:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:31:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:051dbc8b8e4ed99bbd1a698a7e4bd348c280e0ddaf417786fbedd99ca22cb144`  
		Last Modified: Mon, 10 Feb 2020 15:43:20 GMT  
		Size: 33.0 MB (32986499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f53f3c55500976229df5bc71ead0d2723cda57b2c606b6e906de3b7b5c2ad80`  
		Last Modified: Fri, 21 Feb 2020 22:33:32 GMT  
		Size: 30.5 KB (30477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8143f400347b6df364214d634dbcd1db12d526040a868183289501481e13f05`  
		Last Modified: Fri, 21 Feb 2020 22:33:32 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd6e204830d0f5b1439e36d1a6af90c8b04d96fb8b4bcacdd6f611706a97881`  
		Last Modified: Fri, 21 Feb 2020 22:33:33 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:eoan` - linux; s390x

```console
$ docker pull ubuntu@sha256:61c91aa6c4837cd47a0b2d24c647e13cc37c89645193f627d40a7495bb65a82b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26714685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358f272d76821bf4cec9984f7c8909492a357d0cd192dd6dce48abe447f61792`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:58:06 GMT
ADD file:14df51909823644041c1e18fdd62b5c5598c3f037712b7a3db85d68d65c12f9a in / 
# Fri, 21 Feb 2020 21:58:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:58:14 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:58:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:58:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cb19e5b8123e1f3303c72ff2231d83a7282d4d798635f63093ee0c6329d5bf4b`  
		Last Modified: Mon, 10 Feb 2020 15:44:30 GMT  
		Size: 26.7 MB (26682544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ad82f1f4a65553adb6d26ef9b25aebaacb039124b98ba6867d7a27d8dc25f9`  
		Last Modified: Fri, 21 Feb 2020 21:59:28 GMT  
		Size: 31.1 KB (31106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2a7e86bc0f07353acc2cc206b74b5d9825041b4fbd0c0b8de71419ec7b661b`  
		Last Modified: Fri, 21 Feb 2020 21:59:33 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7cae483f07e12cbe0fc9a0bc8dceaecbe7ec0fa3ed9215d663ec3ac10210ab`  
		Last Modified: Fri, 21 Feb 2020 21:59:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:eoan-20200207`

```console
$ docker pull ubuntu@sha256:ed677609acf0dd2e785d7994dd4786ef64872dd26e3ab7fab716a5ba4002ac82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:eoan-20200207` - linux; amd64

```console
$ docker pull ubuntu@sha256:6dbeda79f38da94149cf5c3f75828df544f96491fe05c192094b965d0a16dfef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28308310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f82834f04c624aa37c017e808c8ff2083c10c7a0ac527550ea0cae73a7a9cf8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:21:11 GMT
ADD file:49bd1c0bfe89a93a193774bfd334bc1151f0dca95849f81d1ac353673399585c in / 
# Fri, 21 Feb 2020 22:21:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:21:14 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:21:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:21:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a9c68053c4b2379a9ad5b7306236a13f469cfd18e727dd4e76470af366445b45`  
		Last Modified: Mon, 10 Feb 2020 15:41:51 GMT  
		Size: 28.3 MB (28276663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9c43fe7e5dcfee42adb18336072154126bc052cc1c578e64d27a8aeaabc97`  
		Last Modified: Fri, 21 Feb 2020 22:23:01 GMT  
		Size: 30.6 KB (30633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90491034717d4c1d1e0b37a4bde4f3a0e26630af7d360b7c0248660ccbef59d5`  
		Last Modified: Fri, 21 Feb 2020 22:23:01 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781c6270286751c77c20928c68fa3edd532f0d3d11108db32020c8840f0ea6cb`  
		Last Modified: Fri, 21 Feb 2020 22:23:01 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:eoan-20200207` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d945255334dfa76d5f4a2371c88c4e03f01fe16e9d52cac0c25febf82661ca98
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23767910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a395321a14de7f7719c4d101b74b3f6c8e10e8a6469e417d02a4ed12198cb85`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:05:21 GMT
ADD file:cd4de1fcdceb95824a887d3d27d3c110261a719ded9d99031dd00e1568494c4a in / 
# Fri, 21 Feb 2020 22:05:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:05:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:05:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:05:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bd94fa49cb09c9859edca1e49f6f1cbac0fd492ae56f34b62332a783ad7b68d7`  
		Last Modified: Mon, 10 Feb 2020 15:42:56 GMT  
		Size: 23.7 MB (23736258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1ca8c199cca8211202b60f587659b529101b98194226cb6735febcac6db3f9`  
		Last Modified: Fri, 21 Feb 2020 22:07:02 GMT  
		Size: 30.6 KB (30612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefecf0dd0df3e68f7f80336d560e65ce665036fe83576e4f801047dfd4a9d9f`  
		Last Modified: Fri, 21 Feb 2020 22:07:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8017e57ad339bf8ddfdfd30a79d5096b13c3886781f1078e0303a89cb818f539`  
		Last Modified: Fri, 21 Feb 2020 22:07:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:eoan-20200207` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:5c60568f428d8e77e38adc410cd4b8cf02b96a2e9de93cbc829d83dc11d11df8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26901121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c984153802b54032ee6018f4f5156c8f0455ec3424e728366872907e7199b55`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:42 GMT
ADD file:29003dce8015529919e9efa92862cda5f1c4a394bebe00e7d9bca8894f23bad2 in / 
# Fri, 21 Feb 2020 21:54:45 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:79693b41cb22c8dae6603b2bf443392e179fff02152f5b8fb25e9ebc2f36ca37`  
		Last Modified: Mon, 10 Feb 2020 15:42:23 GMT  
		Size: 26.9 MB (26869627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085004cd2eaec5c5d7d85da739c356d4035b607ff5d3fa3de249827468ac04e4`  
		Last Modified: Fri, 21 Feb 2020 21:56:23 GMT  
		Size: 30.5 KB (30457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9727781305391dcb29dd0f8d61651a751c07d2a32abd0c1ce145117a9416eca`  
		Last Modified: Fri, 21 Feb 2020 21:56:23 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a75366ff852d9cfecac92c78537e6ac39629896a81c09dd9051a924c9363573`  
		Last Modified: Fri, 21 Feb 2020 21:56:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:eoan-20200207` - linux; 386

```console
$ docker pull ubuntu@sha256:a30685e91c6c7a9e84380699ab7c26cfb94cc690bc2e32295e3cdcdee483e096
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29076596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab681b0e86110fa97d2a102218e98b701d5dbd78677f73c8bf5d866d689f41f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:39:17 GMT
ADD file:8712d700c1cc817afa2abe23b077498c4ec2332067a7d38e5d3425454373e193 in / 
# Fri, 21 Feb 2020 21:39:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:39:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:39:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:39:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:df36fe298056793eae27d9efb7b1d54a4d69b16ad6a7d62fc186a8e7727db39f`  
		Last Modified: Mon, 10 Feb 2020 15:43:00 GMT  
		Size: 29.0 MB (29044887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b3578b2a446d70c838e7144c5d77d423461b43e78e2e75107f2764511bed0e`  
		Last Modified: Fri, 21 Feb 2020 21:40:03 GMT  
		Size: 30.7 KB (30699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb0394aa2bb495dd3bef1779832e0d27d6d292aaf3f2740c17564759aa47ef2`  
		Last Modified: Fri, 21 Feb 2020 21:40:04 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7e86bd657e678ce69ee3e2c2e502097c3353cd8484841245225e4d598489c3`  
		Last Modified: Fri, 21 Feb 2020 21:40:04 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:eoan-20200207` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:7aac2b62da78b633b56555f4b6ed263abd3f8508ed956dcabeb9911e49d21628
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33018012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b353da7a159efbc9b738e384fd723b7680fbf03f55399e3d8817abebee598bb3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:31:25 GMT
ADD file:d3168601bc3d213abcd3bb57ad2824d9099de51d8775c8d356460e12d15a26a1 in / 
# Fri, 21 Feb 2020 22:31:31 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:31:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:31:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:31:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:051dbc8b8e4ed99bbd1a698a7e4bd348c280e0ddaf417786fbedd99ca22cb144`  
		Last Modified: Mon, 10 Feb 2020 15:43:20 GMT  
		Size: 33.0 MB (32986499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f53f3c55500976229df5bc71ead0d2723cda57b2c606b6e906de3b7b5c2ad80`  
		Last Modified: Fri, 21 Feb 2020 22:33:32 GMT  
		Size: 30.5 KB (30477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8143f400347b6df364214d634dbcd1db12d526040a868183289501481e13f05`  
		Last Modified: Fri, 21 Feb 2020 22:33:32 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd6e204830d0f5b1439e36d1a6af90c8b04d96fb8b4bcacdd6f611706a97881`  
		Last Modified: Fri, 21 Feb 2020 22:33:33 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:eoan-20200207` - linux; s390x

```console
$ docker pull ubuntu@sha256:61c91aa6c4837cd47a0b2d24c647e13cc37c89645193f627d40a7495bb65a82b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26714685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358f272d76821bf4cec9984f7c8909492a357d0cd192dd6dce48abe447f61792`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:58:06 GMT
ADD file:14df51909823644041c1e18fdd62b5c5598c3f037712b7a3db85d68d65c12f9a in / 
# Fri, 21 Feb 2020 21:58:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:58:14 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:58:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:58:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cb19e5b8123e1f3303c72ff2231d83a7282d4d798635f63093ee0c6329d5bf4b`  
		Last Modified: Mon, 10 Feb 2020 15:44:30 GMT  
		Size: 26.7 MB (26682544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ad82f1f4a65553adb6d26ef9b25aebaacb039124b98ba6867d7a27d8dc25f9`  
		Last Modified: Fri, 21 Feb 2020 21:59:28 GMT  
		Size: 31.1 KB (31106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2a7e86bc0f07353acc2cc206b74b5d9825041b4fbd0c0b8de71419ec7b661b`  
		Last Modified: Fri, 21 Feb 2020 21:59:33 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7cae483f07e12cbe0fc9a0bc8dceaecbe7ec0fa3ed9215d663ec3ac10210ab`  
		Last Modified: Fri, 21 Feb 2020 21:59:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:7922db6447e9d1470e3bf821e8ff228d70c3593e822e980c58bf9185821ac645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal` - linux; amd64

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

### `ubuntu:focal` - linux; arm variant v7

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

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:64a3d51cb381a58adf45f5037a03deee2e22668d8e2f19a222e78c16969229a6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26978462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb1d69f19cd3f982e87a8dfaf75277516c426a7b0f2b633ffa2607d61cc4346`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 00:42:08 GMT
ADD file:3f5a5ff4e005ffd96a9a56c4234117276101fd4cd6b87b503fad5d3f02319d92 in / 
# Thu, 16 Jan 2020 00:42:11 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 00:42:13 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 00:42:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 00:42:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d0804342421c30932eee7f90821efd1e7dac9398a9cac78b662e33b2a3faeeb3`  
		Last Modified: Thu, 16 Jan 2020 00:44:12 GMT  
		Size: 26.9 MB (26946995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d926bd5118332af73957eb2925d9433286ec09620aa22ed01eaca19e89d76a`  
		Last Modified: Thu, 16 Jan 2020 00:44:05 GMT  
		Size: 30.4 KB (30431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3420a5d9e296a9e1a3d258bef98c8dd8f40f3b0767cdb42b424acdee2b47b2b9`  
		Last Modified: Thu, 16 Jan 2020 00:44:05 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86fe98d56e47198b1f7b547c1dfac333460f1aa23177768180ca62714aaa1d2`  
		Last Modified: Thu, 16 Jan 2020 00:44:05 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; ppc64le

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

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:7345a0001b12b9d537ae2936205827ddd6a9aac6616943e67f9623d2ef338c52
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26957237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9394f7a1e4c93e9b65700e3412aff5cd02302a0d4db349809f9257fdd411c040`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 00:45:47 GMT
ADD file:5fbe981ed0834a4a7ca86c449eacf27c014fe832bba12eda0aa98718b927fc45 in / 
# Thu, 16 Jan 2020 00:45:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 00:45:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 00:45:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 00:45:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9718365a56944fa9db6c418110acfb6a7170f892e2f5d8bb0b66b3dbb538ad2a`  
		Last Modified: Thu, 16 Jan 2020 00:46:51 GMT  
		Size: 26.9 MB (26925143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1be672e2a8be868977dac18b2ad998262f7716cc1bda9f79c380e87d70c8d8`  
		Last Modified: Thu, 16 Jan 2020 00:46:44 GMT  
		Size: 31.1 KB (31089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08de0d4260b235271919468fdd3074a90da7692eb0d0575521cb1b18dd36525d`  
		Last Modified: Thu, 16 Jan 2020 00:46:44 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9d5d6c35a086753c3e88803888682d2da2f6cea21681a1d304e5cd8c8f0846`  
		Last Modified: Thu, 16 Jan 2020 00:46:44 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:focal-20200115`

```console
$ docker pull ubuntu@sha256:7922db6447e9d1470e3bf821e8ff228d70c3593e822e980c58bf9185821ac645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal-20200115` - linux; amd64

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

### `ubuntu:focal-20200115` - linux; arm variant v7

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

### `ubuntu:focal-20200115` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:64a3d51cb381a58adf45f5037a03deee2e22668d8e2f19a222e78c16969229a6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26978462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb1d69f19cd3f982e87a8dfaf75277516c426a7b0f2b633ffa2607d61cc4346`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 00:42:08 GMT
ADD file:3f5a5ff4e005ffd96a9a56c4234117276101fd4cd6b87b503fad5d3f02319d92 in / 
# Thu, 16 Jan 2020 00:42:11 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 00:42:13 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 00:42:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 00:42:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d0804342421c30932eee7f90821efd1e7dac9398a9cac78b662e33b2a3faeeb3`  
		Last Modified: Thu, 16 Jan 2020 00:44:12 GMT  
		Size: 26.9 MB (26946995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d926bd5118332af73957eb2925d9433286ec09620aa22ed01eaca19e89d76a`  
		Last Modified: Thu, 16 Jan 2020 00:44:05 GMT  
		Size: 30.4 KB (30431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3420a5d9e296a9e1a3d258bef98c8dd8f40f3b0767cdb42b424acdee2b47b2b9`  
		Last Modified: Thu, 16 Jan 2020 00:44:05 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86fe98d56e47198b1f7b547c1dfac333460f1aa23177768180ca62714aaa1d2`  
		Last Modified: Thu, 16 Jan 2020 00:44:05 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal-20200115` - linux; ppc64le

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

### `ubuntu:focal-20200115` - linux; s390x

```console
$ docker pull ubuntu@sha256:7345a0001b12b9d537ae2936205827ddd6a9aac6616943e67f9623d2ef338c52
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26957237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9394f7a1e4c93e9b65700e3412aff5cd02302a0d4db349809f9257fdd411c040`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 00:45:47 GMT
ADD file:5fbe981ed0834a4a7ca86c449eacf27c014fe832bba12eda0aa98718b927fc45 in / 
# Thu, 16 Jan 2020 00:45:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 00:45:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 00:45:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 00:45:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9718365a56944fa9db6c418110acfb6a7170f892e2f5d8bb0b66b3dbb538ad2a`  
		Last Modified: Thu, 16 Jan 2020 00:46:51 GMT  
		Size: 26.9 MB (26925143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1be672e2a8be868977dac18b2ad998262f7716cc1bda9f79c380e87d70c8d8`  
		Last Modified: Thu, 16 Jan 2020 00:46:44 GMT  
		Size: 31.1 KB (31089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08de0d4260b235271919468fdd3074a90da7692eb0d0575521cb1b18dd36525d`  
		Last Modified: Thu, 16 Jan 2020 00:46:44 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9d5d6c35a086753c3e88803888682d2da2f6cea21681a1d304e5cd8c8f0846`  
		Last Modified: Thu, 16 Jan 2020 00:46:44 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:04d48df82c938587820d7b6006f5071dbbffceb7ca01d2814f81857c631d44df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:latest` - linux; amd64

```console
$ docker pull ubuntu@sha256:0925d086715714114c1988f7c947db94064fd385e171a63c07730f1fa014e6f9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26728476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72300a873c2ca11c70d0c8642177ce76ff69ae04d61a5813ef58d40ff66e3e7c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:60a99a670b980963e4a9d882f631cba5d26ba5d14ccba2aa82a4e1f4d084fb1f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22312168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981c0bc3c335271c725c2d7097fbe843453458690f8016f18ea3e15139cba12d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:04:48 GMT
ADD file:548fc3249b705bf3e94efcc50c1c9141e03d1ce51edfc194a84bd631d1a7b6d4 in / 
# Fri, 21 Feb 2020 22:04:52 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:04:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:05:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:05:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b9b5ae93466ea2cca8f47e7e02dc1907faaaae6ed617360e47259eb4cac4d0a7`  
		Last Modified: Fri, 21 Feb 2020 22:06:53 GMT  
		Size: 22.3 MB (22275658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8983199234a3f5beecbe2be6e21b4a49e67dd5726e7080e999c6f2cea91bc2`  
		Last Modified: Fri, 21 Feb 2020 22:06:47 GMT  
		Size: 35.5 KB (35470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e76f87f706a4e3e6b5f3d9fabd021b46b875dc9058e26d31877057069115333`  
		Last Modified: Fri, 21 Feb 2020 22:06:47 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b196ba84f492bbca6bb4979ae6e8d2d3a952559cdf3dfd11e99c3a4c11aa0891`  
		Last Modified: Fri, 21 Feb 2020 22:06:47 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:fab7c78ecd4c52e801b8a597846ec5c00ff2e4f4d1d92f6af1c8390eabc1d2d5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23757379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c574f8f488657f27c856bda8b44aa9d0b5ad03e1fc6a88a19ec9e57e9624ab34`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:latest` - linux; 386

```console
$ docker pull ubuntu@sha256:4d07b5b0cd47c06a3ca847536a3e05901c6bf9d9f52dbb0e6a7fff9141453f11
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27159454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d2962d1c2fb91f3b025c85a529da96d4a4788d8685e7aff66144510f0efec8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:39:03 GMT
ADD file:df203cc2574204629c69613fcea4942faa0f9224ff0c8bacb908b85d73604628 in / 
# Fri, 21 Feb 2020 21:39:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:39:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:39:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:39:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ddc482e6a4fa5e364980052ab9f5d236f29ae9b217ed672b3dba44669f4041de`  
		Last Modified: Fri, 21 Feb 2020 21:39:58 GMT  
		Size: 27.1 MB (27123823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d2b8bf2fa50513ca7c508e44ac1a15c7ec42b1a3369a91380663868309ab46`  
		Last Modified: Fri, 21 Feb 2020 21:39:52 GMT  
		Size: 34.6 KB (34625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84c193628e4067b419327ffa1bfef4b73161d9b1e3ce1e4ee83e714fd1d14e8`  
		Last Modified: Fri, 21 Feb 2020 21:39:52 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5271c42d486e4bb18cadbdf885d057c29384a032113047030f7c4bd6253bbf10`  
		Last Modified: Fri, 21 Feb 2020 21:39:52 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:1b3520a2868bd5d82cbf432931ffc3131d99af2d3157bdcf2757b2896e0be86b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30437337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0cab33facfc5176f669f524b4c2b170605e87fa05eeabe5203cbd84fbe52e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:30:07 GMT
ADD file:fee193b50fa8dbda3e9dbec639709a18c062adef5add2fda1c8aa29e5a288d28 in / 
# Fri, 21 Feb 2020 22:30:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:30:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:30:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:30:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cfb81e1a655db6311df167d6e7259257ac1bec8fd6fa9eaef39c0661b1488490`  
		Last Modified: Fri, 21 Feb 2020 22:33:18 GMT  
		Size: 30.4 MB (30401091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815faea808b955284818fc847eb2d542dc550d92f5974023b34000a33302aed`  
		Last Modified: Fri, 21 Feb 2020 22:33:12 GMT  
		Size: 35.2 KB (35207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009f42ff24bbe56824bac50e1ba861b157cbf45a60e8e09ff1f4eee816a21a1`  
		Last Modified: Fri, 21 Feb 2020 22:33:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164e4ca1b0934007f85d8baa8c3041d64dcde54ccfa21f38a106d1b876a1c21`  
		Last Modified: Fri, 21 Feb 2020 22:33:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:a837741679960532ff2a22c9ba80964a8b0246add966521ffd5427487ea21011
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25402893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3990be7b573ae1044b44f6c43736c913c89b9ba25e781a196f4fc19687ded4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:57:46 GMT
ADD file:7925c9b35ffa1870e7d336ddcdd6c3434715178c7d08ff2ce9796b651302c347 in / 
# Fri, 21 Feb 2020 21:57:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:57:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:57:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:57:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b84fcb37dc33cf7416e0f1cf1219e16a15ab0d1c3aa4638d362f19c2679451de`  
		Last Modified: Fri, 21 Feb 2020 21:59:09 GMT  
		Size: 25.4 MB (25365672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9594931f903b7b3c4f5cb63196d29d715c50b567c128a5572131c12a25f04139`  
		Last Modified: Fri, 21 Feb 2020 21:59:06 GMT  
		Size: 36.2 KB (36186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66af13675c2330803d61d2198bb4f69c36bb7eed2d2b2bc3660fed8e873dce59`  
		Last Modified: Fri, 21 Feb 2020 21:59:11 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae0fb7b2ee5c5bc387374bdd08f53541bdfcf678d9b9f83489c3923af65fed0`  
		Last Modified: Fri, 21 Feb 2020 21:59:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:ed677609acf0dd2e785d7994dd4786ef64872dd26e3ab7fab716a5ba4002ac82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:rolling` - linux; amd64

```console
$ docker pull ubuntu@sha256:6dbeda79f38da94149cf5c3f75828df544f96491fe05c192094b965d0a16dfef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28308310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f82834f04c624aa37c017e808c8ff2083c10c7a0ac527550ea0cae73a7a9cf8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:21:11 GMT
ADD file:49bd1c0bfe89a93a193774bfd334bc1151f0dca95849f81d1ac353673399585c in / 
# Fri, 21 Feb 2020 22:21:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:21:14 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:21:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:21:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a9c68053c4b2379a9ad5b7306236a13f469cfd18e727dd4e76470af366445b45`  
		Last Modified: Mon, 10 Feb 2020 15:41:51 GMT  
		Size: 28.3 MB (28276663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9c43fe7e5dcfee42adb18336072154126bc052cc1c578e64d27a8aeaabc97`  
		Last Modified: Fri, 21 Feb 2020 22:23:01 GMT  
		Size: 30.6 KB (30633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90491034717d4c1d1e0b37a4bde4f3a0e26630af7d360b7c0248660ccbef59d5`  
		Last Modified: Fri, 21 Feb 2020 22:23:01 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781c6270286751c77c20928c68fa3edd532f0d3d11108db32020c8840f0ea6cb`  
		Last Modified: Fri, 21 Feb 2020 22:23:01 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d945255334dfa76d5f4a2371c88c4e03f01fe16e9d52cac0c25febf82661ca98
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23767910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a395321a14de7f7719c4d101b74b3f6c8e10e8a6469e417d02a4ed12198cb85`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:05:21 GMT
ADD file:cd4de1fcdceb95824a887d3d27d3c110261a719ded9d99031dd00e1568494c4a in / 
# Fri, 21 Feb 2020 22:05:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:05:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:05:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:05:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bd94fa49cb09c9859edca1e49f6f1cbac0fd492ae56f34b62332a783ad7b68d7`  
		Last Modified: Mon, 10 Feb 2020 15:42:56 GMT  
		Size: 23.7 MB (23736258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1ca8c199cca8211202b60f587659b529101b98194226cb6735febcac6db3f9`  
		Last Modified: Fri, 21 Feb 2020 22:07:02 GMT  
		Size: 30.6 KB (30612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefecf0dd0df3e68f7f80336d560e65ce665036fe83576e4f801047dfd4a9d9f`  
		Last Modified: Fri, 21 Feb 2020 22:07:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8017e57ad339bf8ddfdfd30a79d5096b13c3886781f1078e0303a89cb818f539`  
		Last Modified: Fri, 21 Feb 2020 22:07:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:5c60568f428d8e77e38adc410cd4b8cf02b96a2e9de93cbc829d83dc11d11df8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26901121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c984153802b54032ee6018f4f5156c8f0455ec3424e728366872907e7199b55`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:42 GMT
ADD file:29003dce8015529919e9efa92862cda5f1c4a394bebe00e7d9bca8894f23bad2 in / 
# Fri, 21 Feb 2020 21:54:45 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:79693b41cb22c8dae6603b2bf443392e179fff02152f5b8fb25e9ebc2f36ca37`  
		Last Modified: Mon, 10 Feb 2020 15:42:23 GMT  
		Size: 26.9 MB (26869627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085004cd2eaec5c5d7d85da739c356d4035b607ff5d3fa3de249827468ac04e4`  
		Last Modified: Fri, 21 Feb 2020 21:56:23 GMT  
		Size: 30.5 KB (30457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9727781305391dcb29dd0f8d61651a751c07d2a32abd0c1ce145117a9416eca`  
		Last Modified: Fri, 21 Feb 2020 21:56:23 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a75366ff852d9cfecac92c78537e6ac39629896a81c09dd9051a924c9363573`  
		Last Modified: Fri, 21 Feb 2020 21:56:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; 386

```console
$ docker pull ubuntu@sha256:a30685e91c6c7a9e84380699ab7c26cfb94cc690bc2e32295e3cdcdee483e096
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29076596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab681b0e86110fa97d2a102218e98b701d5dbd78677f73c8bf5d866d689f41f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:39:17 GMT
ADD file:8712d700c1cc817afa2abe23b077498c4ec2332067a7d38e5d3425454373e193 in / 
# Fri, 21 Feb 2020 21:39:18 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:39:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:39:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:39:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:df36fe298056793eae27d9efb7b1d54a4d69b16ad6a7d62fc186a8e7727db39f`  
		Last Modified: Mon, 10 Feb 2020 15:43:00 GMT  
		Size: 29.0 MB (29044887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b3578b2a446d70c838e7144c5d77d423461b43e78e2e75107f2764511bed0e`  
		Last Modified: Fri, 21 Feb 2020 21:40:03 GMT  
		Size: 30.7 KB (30699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb0394aa2bb495dd3bef1779832e0d27d6d292aaf3f2740c17564759aa47ef2`  
		Last Modified: Fri, 21 Feb 2020 21:40:04 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7e86bd657e678ce69ee3e2c2e502097c3353cd8484841245225e4d598489c3`  
		Last Modified: Fri, 21 Feb 2020 21:40:04 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:7aac2b62da78b633b56555f4b6ed263abd3f8508ed956dcabeb9911e49d21628
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33018012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b353da7a159efbc9b738e384fd723b7680fbf03f55399e3d8817abebee598bb3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:31:25 GMT
ADD file:d3168601bc3d213abcd3bb57ad2824d9099de51d8775c8d356460e12d15a26a1 in / 
# Fri, 21 Feb 2020 22:31:31 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:31:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:31:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:31:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:051dbc8b8e4ed99bbd1a698a7e4bd348c280e0ddaf417786fbedd99ca22cb144`  
		Last Modified: Mon, 10 Feb 2020 15:43:20 GMT  
		Size: 33.0 MB (32986499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f53f3c55500976229df5bc71ead0d2723cda57b2c606b6e906de3b7b5c2ad80`  
		Last Modified: Fri, 21 Feb 2020 22:33:32 GMT  
		Size: 30.5 KB (30477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8143f400347b6df364214d634dbcd1db12d526040a868183289501481e13f05`  
		Last Modified: Fri, 21 Feb 2020 22:33:32 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd6e204830d0f5b1439e36d1a6af90c8b04d96fb8b4bcacdd6f611706a97881`  
		Last Modified: Fri, 21 Feb 2020 22:33:33 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:61c91aa6c4837cd47a0b2d24c647e13cc37c89645193f627d40a7495bb65a82b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26714685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358f272d76821bf4cec9984f7c8909492a357d0cd192dd6dce48abe447f61792`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:58:06 GMT
ADD file:14df51909823644041c1e18fdd62b5c5598c3f037712b7a3db85d68d65c12f9a in / 
# Fri, 21 Feb 2020 21:58:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:58:14 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:58:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:58:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cb19e5b8123e1f3303c72ff2231d83a7282d4d798635f63093ee0c6329d5bf4b`  
		Last Modified: Mon, 10 Feb 2020 15:44:30 GMT  
		Size: 26.7 MB (26682544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ad82f1f4a65553adb6d26ef9b25aebaacb039124b98ba6867d7a27d8dc25f9`  
		Last Modified: Fri, 21 Feb 2020 21:59:28 GMT  
		Size: 31.1 KB (31106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2a7e86bc0f07353acc2cc206b74b5d9825041b4fbd0c0b8de71419ec7b661b`  
		Last Modified: Fri, 21 Feb 2020 21:59:33 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7cae483f07e12cbe0fc9a0bc8dceaecbe7ec0fa3ed9215d663ec3ac10210ab`  
		Last Modified: Fri, 21 Feb 2020 21:59:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:trusty`

```console
$ docker pull ubuntu@sha256:ffc76f71dd8be8c9e222d420dc96901a07b61616689a44c7b3ef6a10b7213de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `ubuntu:trusty` - linux; amd64

```console
$ docker pull ubuntu@sha256:bd0223687054d0f8884fc9e872392c6385a3195d612400495962e270b572ed06
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70764399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4f1fe62ff14a4c8119781d47a3739fa97c190e1df38e868794ad7a7cf50a48`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:23:42 GMT
ADD file:276b5d943a4d284f8a7b249176a31f93d95e852480c2b851de287e53ff622bba in / 
# Thu, 19 Dec 2019 04:23:43 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:23:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:23:45 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:23:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2e6e20c8e2e69fa5c3fcc310f419975cef5fbeb6f7f2fe1374071141281b6a06`  
		Last Modified: Wed, 18 Dec 2019 13:21:28 GMT  
		Size: 70.7 MB (70691577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30bb187ac3fc6c428f38d46409e7765a18dc6b59bc99914f0ba6936463307ec8`  
		Last Modified: Thu, 19 Dec 2019 04:25:41 GMT  
		Size: 72.7 KB (72659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a5bcc4a58aeed61f7dbe0a859aa4d37db24efd0c3ca58fb83605b5ad9044b5`  
		Last Modified: Thu, 19 Dec 2019 04:25:41 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:3fc5c28a28125d304462d5b9292d64a61041350304ac5deab416271b25d2e219
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64700967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67449d6018f689b7a2a501426015e0b13ada33b377c4c935c68453ce13706712`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:12:57 GMT
ADD file:e9d55e059869915743a8ca8e64582d23c48fe7e90e439daccd56d3e08e8673b4 in / 
# Thu, 19 Dec 2019 06:13:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:13:11 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:13:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:13:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0db3a87a3d7959895fd860c8b924980adda6e77f5d315b6676a4ac0e12518978`  
		Last Modified: Thu, 19 Dec 2019 06:16:01 GMT  
		Size: 64.6 MB (64624015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08b117a826b8d1ae5a5995f7eab5a89f5d582f24fa0016182b6502e42322179`  
		Last Modified: Thu, 19 Dec 2019 06:15:41 GMT  
		Size: 76.8 KB (76765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d5442ddd2dd606cb4dbd9c7243b10f6848c3ee77c176d1b0c667a2232b900c`  
		Last Modified: Thu, 19 Dec 2019 06:15:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:79b0f81ad6fc8f0bced3919beee0a79d60d1c8358911188d0787b1f155656d84
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66525501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104c127e75190df2e80d312958f30c9b7d2da0b5356f6c1e81e92dc85d3f9740`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:54:04 GMT
ADD file:b0eb0db52e323748ea9b8d7f8aecbc523a747619cd08663bab0fe60ab59bc60e in / 
# Thu, 19 Dec 2019 03:54:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:54:20 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:54:24 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:54:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d1a5a1e51f251c3431dec02e2cc8d157e92d1b46913708ce9e600747a6274977`  
		Last Modified: Thu, 19 Dec 2019 03:57:08 GMT  
		Size: 66.5 MB (66466219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9592077f8570e1222c5a6930a2fdc85b6b607b6c91230a5762c7bd6d84749e25`  
		Last Modified: Thu, 19 Dec 2019 03:56:48 GMT  
		Size: 59.1 KB (59094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b48639f381d2e2566e4c5bdb9792e8666ac2d2cc22918fda5751b8784ee5a5`  
		Last Modified: Thu, 19 Dec 2019 03:56:48 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty` - linux; 386

```console
$ docker pull ubuntu@sha256:c8c1d2e6d53d94ef32e73354d146dc6e39c19ce8db2692356b3a6eef5a8ab956
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68445457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b01d68827fff530f34f6ff966823624238b7b90aec1bc82b2a9468da476d20e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:42:13 GMT
ADD file:e034601a525da53b0f39bb04d6e2264e2a592d0ae7c21e00697b9b62ca1efec9 in / 
# Thu, 19 Dec 2019 04:42:14 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:42:15 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:42:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:42:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:630712fe5783a35ad52a7026002143cb4f8fe65d34097dcaa4c4331b1b059a17`  
		Last Modified: Thu, 19 Dec 2019 04:44:02 GMT  
		Size: 68.4 MB (68380440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df46dbd3c04fd4a00981fd885f4d30a154ffa34bc8329bd448e9ca469df32e1`  
		Last Modified: Thu, 19 Dec 2019 04:43:42 GMT  
		Size: 64.9 KB (64855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4ca1e6e5f77f07de7e2107adcb062e1e72e84ce6ff83d5beeb5f84dfcc8418`  
		Last Modified: Thu, 19 Dec 2019 04:43:42 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:d00cd5726fb0c0523960683e45fe4bbb3807e68ef3edff693d44454aad69b85b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73443147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce257c90d69b5ed2a0955447f934ed3a9bc17c4f723fd6f61c0f55218e507b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:20:59 GMT
ADD file:581665e92c72c8638b40fe509de6479dc1a5d7b5ffe8d6706006178c406e35e2 in / 
# Thu, 19 Dec 2019 04:21:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bed4146d918c6c9a57bc3a8bf829e702975b0e53c7f25920fe9435b58ed6b64f`  
		Last Modified: Thu, 19 Dec 2019 04:26:52 GMT  
		Size: 73.4 MB (73379539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d17944a6ab7c0a73210db128de5b677c26f0d4c4c59f3bf6c76b7d1e847098`  
		Last Modified: Thu, 19 Dec 2019 04:26:36 GMT  
		Size: 63.4 KB (63423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d84211dbdd608b55c60bac1fab57fed3dd6de92653162fe123fd0154bcb03e`  
		Last Modified: Thu, 19 Dec 2019 04:26:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:trusty-20191217`

```console
$ docker pull ubuntu@sha256:ffc76f71dd8be8c9e222d420dc96901a07b61616689a44c7b3ef6a10b7213de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `ubuntu:trusty-20191217` - linux; amd64

```console
$ docker pull ubuntu@sha256:bd0223687054d0f8884fc9e872392c6385a3195d612400495962e270b572ed06
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70764399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4f1fe62ff14a4c8119781d47a3739fa97c190e1df38e868794ad7a7cf50a48`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:23:42 GMT
ADD file:276b5d943a4d284f8a7b249176a31f93d95e852480c2b851de287e53ff622bba in / 
# Thu, 19 Dec 2019 04:23:43 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:23:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:23:45 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:23:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2e6e20c8e2e69fa5c3fcc310f419975cef5fbeb6f7f2fe1374071141281b6a06`  
		Last Modified: Wed, 18 Dec 2019 13:21:28 GMT  
		Size: 70.7 MB (70691577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30bb187ac3fc6c428f38d46409e7765a18dc6b59bc99914f0ba6936463307ec8`  
		Last Modified: Thu, 19 Dec 2019 04:25:41 GMT  
		Size: 72.7 KB (72659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a5bcc4a58aeed61f7dbe0a859aa4d37db24efd0c3ca58fb83605b5ad9044b5`  
		Last Modified: Thu, 19 Dec 2019 04:25:41 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty-20191217` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:3fc5c28a28125d304462d5b9292d64a61041350304ac5deab416271b25d2e219
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64700967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67449d6018f689b7a2a501426015e0b13ada33b377c4c935c68453ce13706712`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:12:57 GMT
ADD file:e9d55e059869915743a8ca8e64582d23c48fe7e90e439daccd56d3e08e8673b4 in / 
# Thu, 19 Dec 2019 06:13:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:13:11 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:13:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:13:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0db3a87a3d7959895fd860c8b924980adda6e77f5d315b6676a4ac0e12518978`  
		Last Modified: Thu, 19 Dec 2019 06:16:01 GMT  
		Size: 64.6 MB (64624015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08b117a826b8d1ae5a5995f7eab5a89f5d582f24fa0016182b6502e42322179`  
		Last Modified: Thu, 19 Dec 2019 06:15:41 GMT  
		Size: 76.8 KB (76765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d5442ddd2dd606cb4dbd9c7243b10f6848c3ee77c176d1b0c667a2232b900c`  
		Last Modified: Thu, 19 Dec 2019 06:15:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty-20191217` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:79b0f81ad6fc8f0bced3919beee0a79d60d1c8358911188d0787b1f155656d84
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66525501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104c127e75190df2e80d312958f30c9b7d2da0b5356f6c1e81e92dc85d3f9740`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:54:04 GMT
ADD file:b0eb0db52e323748ea9b8d7f8aecbc523a747619cd08663bab0fe60ab59bc60e in / 
# Thu, 19 Dec 2019 03:54:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:54:20 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:54:24 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:54:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d1a5a1e51f251c3431dec02e2cc8d157e92d1b46913708ce9e600747a6274977`  
		Last Modified: Thu, 19 Dec 2019 03:57:08 GMT  
		Size: 66.5 MB (66466219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9592077f8570e1222c5a6930a2fdc85b6b607b6c91230a5762c7bd6d84749e25`  
		Last Modified: Thu, 19 Dec 2019 03:56:48 GMT  
		Size: 59.1 KB (59094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b48639f381d2e2566e4c5bdb9792e8666ac2d2cc22918fda5751b8784ee5a5`  
		Last Modified: Thu, 19 Dec 2019 03:56:48 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty-20191217` - linux; 386

```console
$ docker pull ubuntu@sha256:c8c1d2e6d53d94ef32e73354d146dc6e39c19ce8db2692356b3a6eef5a8ab956
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68445457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b01d68827fff530f34f6ff966823624238b7b90aec1bc82b2a9468da476d20e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:42:13 GMT
ADD file:e034601a525da53b0f39bb04d6e2264e2a592d0ae7c21e00697b9b62ca1efec9 in / 
# Thu, 19 Dec 2019 04:42:14 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:42:15 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:42:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:42:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:630712fe5783a35ad52a7026002143cb4f8fe65d34097dcaa4c4331b1b059a17`  
		Last Modified: Thu, 19 Dec 2019 04:44:02 GMT  
		Size: 68.4 MB (68380440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df46dbd3c04fd4a00981fd885f4d30a154ffa34bc8329bd448e9ca469df32e1`  
		Last Modified: Thu, 19 Dec 2019 04:43:42 GMT  
		Size: 64.9 KB (64855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4ca1e6e5f77f07de7e2107adcb062e1e72e84ce6ff83d5beeb5f84dfcc8418`  
		Last Modified: Thu, 19 Dec 2019 04:43:42 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty-20191217` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:d00cd5726fb0c0523960683e45fe4bbb3807e68ef3edff693d44454aad69b85b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73443147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce257c90d69b5ed2a0955447f934ed3a9bc17c4f723fd6f61c0f55218e507b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:20:59 GMT
ADD file:581665e92c72c8638b40fe509de6479dc1a5d7b5ffe8d6706006178c406e35e2 in / 
# Thu, 19 Dec 2019 04:21:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bed4146d918c6c9a57bc3a8bf829e702975b0e53c7f25920fe9435b58ed6b64f`  
		Last Modified: Thu, 19 Dec 2019 04:26:52 GMT  
		Size: 73.4 MB (73379539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d17944a6ab7c0a73210db128de5b677c26f0d4c4c59f3bf6c76b7d1e847098`  
		Last Modified: Thu, 19 Dec 2019 04:26:36 GMT  
		Size: 63.4 KB (63423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d84211dbdd608b55c60bac1fab57fed3dd6de92653162fe123fd0154bcb03e`  
		Last Modified: Thu, 19 Dec 2019 04:26:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:xenial`

```console
$ docker pull ubuntu@sha256:e9938f45e51d9ff46e2b05a62e0546d0f07489b7f22fbc5288defe760599e38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:xenial` - linux; amd64

```console
$ docker pull ubuntu@sha256:a98d9dcf3a34b2b78e78c61d003eb4d7a90d30fd54451686e2f0bd2ef5f602ac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44193271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77be327e4b63498e0faaa065d30d7c0e5499e42a09275ee19e27fd9a93cde7d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:22:27 GMT
ADD file:1f70668251e2e58cee0ff0c22ee805f8a269ac6f8934c07f7e89dca6cc1de3aa in / 
# Fri, 21 Feb 2020 22:22:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:22:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:22:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:22:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fe703b657a32e0046dce0ad2cb17172cbec8ba302edf370f5f28962bdb6216a9`  
		Last Modified: Thu, 13 Feb 2020 00:25:54 GMT  
		Size: 44.2 MB (44191726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df1fafd224fae3ba34a68dfc401f75bf6bc0c016fe36c61661ca5c7ad729ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a645a4b887f9613f80fae43432e46423f196a9952d11bb620bef2add7c4ed4ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57db7fe0b522b7a6069e769606e5ed0913a64e1e0d0030382a922ccf9449211e`  
		Last Modified: Fri, 21 Feb 2020 22:23:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:4faa0482a239dd826bab958f1ab22333568fcfa17a6a09c30806e69902878184
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38891892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6e0521581046453ce619849f0950fd5fe66a6fb5d85484f6b1b4b1191ca80f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:06:20 GMT
ADD file:7f245cd0bb5455d315f8d753720fab55e9ac41f68c7926b597663d3aeff3c8d4 in / 
# Fri, 21 Feb 2020 22:06:26 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:06:29 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:06:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:06:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:957d6015142d0d6fe598b45df39c8f36d0b86fe61fdb145603423c7d216e5f09`  
		Last Modified: Mon, 17 Feb 2020 15:45:30 GMT  
		Size: 38.9 MB (38890364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a31e0e10e55fa8dad735b48b598b86efb29be81ae44906466ea04a2fd13c6c7`  
		Last Modified: Fri, 21 Feb 2020 22:07:16 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c42599b1b7e867902cc3b4a6cd7cd76c9148ff337a0bc7861131b6176648b45`  
		Last Modified: Fri, 21 Feb 2020 22:07:16 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33654ecb4a4aa4b3b5b7f650b7aab38e3fe0d8d48d88c666f052f819016c3d55`  
		Last Modified: Fri, 21 Feb 2020 22:07:16 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:c7ca486dce6710697a81e2d08796a865f48c6525a3f81f3aa936a4905c9846be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39941860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f8c8b831940488436a2f3c43d61bac998bc01ed1dddf2a01c521ae8ea3f86c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:55:42 GMT
ADD file:61b91c95a686740a57740470b7a1fe64d2479c56c36c69ca1222d870e78d44cc in / 
# Fri, 21 Feb 2020 21:55:46 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 21:55:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:55:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:55:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a7bab9946de3c22ecccd832a0910adc2ffa82eea53f83c600d5ebce9e5422ad0`  
		Last Modified: Mon, 17 Feb 2020 15:45:27 GMT  
		Size: 39.9 MB (39940373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38630c4d9093f5b60806171ca7fa47a70d7ab28eeed25edfad43fb91d5f9f825`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef678cbe74d844c6a114c1158a8c8868b412b7c5ed3a4c159831975a4915db9`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78928743b0e778df64b15ac919705702ee0a080c2586f43c4349b35180de3c36`  
		Last Modified: Fri, 21 Feb 2020 21:56:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial` - linux; 386

```console
$ docker pull ubuntu@sha256:f5c13e0e3239571970b3da937ff27b4062849f2764b23aa04e7127778370ad09
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44174809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1aa297bcabc1cab7710748f5ad4316c2717b5560feff4ecdaf0d57142c6579c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:39:40 GMT
ADD file:118ef8482188b21216adb7af11584f08a24c46958f4f3385032b371a60bb66e1 in / 
# Fri, 21 Feb 2020 21:39:41 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 21:39:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:39:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:39:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:968d3cde0fa07bedc833984b32995ad11d8a375f98616a4ff74ae3ee309ad1a2`  
		Last Modified: Mon, 17 Feb 2020 15:45:30 GMT  
		Size: 44.2 MB (44173277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d65b39906d3579ee3e992072b579dd8168fe81974a0428f27d1db39c6948dbc`  
		Last Modified: Fri, 21 Feb 2020 21:40:16 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd64e0411faf07b0fa30439f0364aa9ef2649b21bf88f1ee9f81cff5342eccad`  
		Last Modified: Fri, 21 Feb 2020 21:40:15 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888871f3d4aa08404cffac4c555fe0c9014444415fe65fad37a6a40d4965c5a2`  
		Last Modified: Fri, 21 Feb 2020 21:40:16 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a2658945e589dd8ec52d7374cc5d4c0a3391a9d9d2a69ac91bcb558bd8da6a31
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46102397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a12016288f21e2de76a81de4bc4029231976317d36f25be75701938e1fc0049`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:32:24 GMT
ADD file:7f14eb8a42273a36130d75b1d935b9617db245cb718ab5b6796ba53ab7a9aa05 in / 
# Fri, 21 Feb 2020 22:32:33 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:32:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:32:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:32:51 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0abc6f550884cf7de4f0adb093a671df9fbff6fa630d3c2bfb1fd80c04c51ad1`  
		Last Modified: Mon, 17 Feb 2020 15:46:15 GMT  
		Size: 46.1 MB (46100906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0741e5703c97bf375e97b9bee6d26a78eb4457d7e6d12661e23f7dd09f8d26b0`  
		Last Modified: Fri, 21 Feb 2020 22:33:56 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed4e13c7b7237db460c7250ffec446cd033597c349d538f1a3bef2c61936f89`  
		Last Modified: Fri, 21 Feb 2020 22:33:56 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9acb6be6f2007b0d8af5a84186b3d866dbcb1eec846431df08803f6f5fa62f9`  
		Last Modified: Fri, 21 Feb 2020 22:33:56 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial` - linux; s390x

```console
$ docker pull ubuntu@sha256:fbbecfc4f9fc56b050d0a8617ff5e0aecfa1bfc6e23c041a574c19c90183bc48
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42815078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99098b69958a3ec33c58573f85484e591633a9110eb2aa3faccb0e5cbdbbadf9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:58:38 GMT
ADD file:2da08b5719e8f84bf1322ff4b7babef0750ca9f09ec09fafb2dd49471656ab45 in / 
# Fri, 21 Feb 2020 21:58:47 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 21:58:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:58:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:58:51 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5d1c06e617a886003bdc553ea5fb88f3d1b9f090ccd01b8f11f59128221a248f`  
		Last Modified: Mon, 17 Feb 2020 15:46:24 GMT  
		Size: 42.8 MB (42813593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014396d85ca8cff40d6f829c1dd4b726456f22ed02b58fc32fda25427a08540b`  
		Last Modified: Fri, 21 Feb 2020 21:59:51 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd0d716f0f324aed318dd9aa0cbe1f47a5ac863a633df8d39b7760f74d2adff`  
		Last Modified: Fri, 21 Feb 2020 21:59:51 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb96b2c9e76d5516a980ea87b6cd16e5f0fd5b6b47b4f4d4a694aab15d36862`  
		Last Modified: Fri, 21 Feb 2020 21:59:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:xenial-20200212`

```console
$ docker pull ubuntu@sha256:e9938f45e51d9ff46e2b05a62e0546d0f07489b7f22fbc5288defe760599e38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:xenial-20200212` - linux; amd64

```console
$ docker pull ubuntu@sha256:a98d9dcf3a34b2b78e78c61d003eb4d7a90d30fd54451686e2f0bd2ef5f602ac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44193271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77be327e4b63498e0faaa065d30d7c0e5499e42a09275ee19e27fd9a93cde7d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:22:27 GMT
ADD file:1f70668251e2e58cee0ff0c22ee805f8a269ac6f8934c07f7e89dca6cc1de3aa in / 
# Fri, 21 Feb 2020 22:22:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:22:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:22:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:22:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fe703b657a32e0046dce0ad2cb17172cbec8ba302edf370f5f28962bdb6216a9`  
		Last Modified: Thu, 13 Feb 2020 00:25:54 GMT  
		Size: 44.2 MB (44191726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df1fafd224fae3ba34a68dfc401f75bf6bc0c016fe36c61661ca5c7ad729ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a645a4b887f9613f80fae43432e46423f196a9952d11bb620bef2add7c4ed4ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57db7fe0b522b7a6069e769606e5ed0913a64e1e0d0030382a922ccf9449211e`  
		Last Modified: Fri, 21 Feb 2020 22:23:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial-20200212` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:4faa0482a239dd826bab958f1ab22333568fcfa17a6a09c30806e69902878184
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38891892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6e0521581046453ce619849f0950fd5fe66a6fb5d85484f6b1b4b1191ca80f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:06:20 GMT
ADD file:7f245cd0bb5455d315f8d753720fab55e9ac41f68c7926b597663d3aeff3c8d4 in / 
# Fri, 21 Feb 2020 22:06:26 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:06:29 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:06:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:06:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:957d6015142d0d6fe598b45df39c8f36d0b86fe61fdb145603423c7d216e5f09`  
		Last Modified: Mon, 17 Feb 2020 15:45:30 GMT  
		Size: 38.9 MB (38890364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a31e0e10e55fa8dad735b48b598b86efb29be81ae44906466ea04a2fd13c6c7`  
		Last Modified: Fri, 21 Feb 2020 22:07:16 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c42599b1b7e867902cc3b4a6cd7cd76c9148ff337a0bc7861131b6176648b45`  
		Last Modified: Fri, 21 Feb 2020 22:07:16 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33654ecb4a4aa4b3b5b7f650b7aab38e3fe0d8d48d88c666f052f819016c3d55`  
		Last Modified: Fri, 21 Feb 2020 22:07:16 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial-20200212` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:c7ca486dce6710697a81e2d08796a865f48c6525a3f81f3aa936a4905c9846be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39941860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f8c8b831940488436a2f3c43d61bac998bc01ed1dddf2a01c521ae8ea3f86c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:55:42 GMT
ADD file:61b91c95a686740a57740470b7a1fe64d2479c56c36c69ca1222d870e78d44cc in / 
# Fri, 21 Feb 2020 21:55:46 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 21:55:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:55:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:55:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a7bab9946de3c22ecccd832a0910adc2ffa82eea53f83c600d5ebce9e5422ad0`  
		Last Modified: Mon, 17 Feb 2020 15:45:27 GMT  
		Size: 39.9 MB (39940373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38630c4d9093f5b60806171ca7fa47a70d7ab28eeed25edfad43fb91d5f9f825`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef678cbe74d844c6a114c1158a8c8868b412b7c5ed3a4c159831975a4915db9`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78928743b0e778df64b15ac919705702ee0a080c2586f43c4349b35180de3c36`  
		Last Modified: Fri, 21 Feb 2020 21:56:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial-20200212` - linux; 386

```console
$ docker pull ubuntu@sha256:f5c13e0e3239571970b3da937ff27b4062849f2764b23aa04e7127778370ad09
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44174809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1aa297bcabc1cab7710748f5ad4316c2717b5560feff4ecdaf0d57142c6579c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:39:40 GMT
ADD file:118ef8482188b21216adb7af11584f08a24c46958f4f3385032b371a60bb66e1 in / 
# Fri, 21 Feb 2020 21:39:41 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 21:39:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:39:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:39:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:968d3cde0fa07bedc833984b32995ad11d8a375f98616a4ff74ae3ee309ad1a2`  
		Last Modified: Mon, 17 Feb 2020 15:45:30 GMT  
		Size: 44.2 MB (44173277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d65b39906d3579ee3e992072b579dd8168fe81974a0428f27d1db39c6948dbc`  
		Last Modified: Fri, 21 Feb 2020 21:40:16 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd64e0411faf07b0fa30439f0364aa9ef2649b21bf88f1ee9f81cff5342eccad`  
		Last Modified: Fri, 21 Feb 2020 21:40:15 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888871f3d4aa08404cffac4c555fe0c9014444415fe65fad37a6a40d4965c5a2`  
		Last Modified: Fri, 21 Feb 2020 21:40:16 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial-20200212` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a2658945e589dd8ec52d7374cc5d4c0a3391a9d9d2a69ac91bcb558bd8da6a31
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46102397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a12016288f21e2de76a81de4bc4029231976317d36f25be75701938e1fc0049`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:32:24 GMT
ADD file:7f14eb8a42273a36130d75b1d935b9617db245cb718ab5b6796ba53ab7a9aa05 in / 
# Fri, 21 Feb 2020 22:32:33 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:32:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:32:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:32:51 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0abc6f550884cf7de4f0adb093a671df9fbff6fa630d3c2bfb1fd80c04c51ad1`  
		Last Modified: Mon, 17 Feb 2020 15:46:15 GMT  
		Size: 46.1 MB (46100906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0741e5703c97bf375e97b9bee6d26a78eb4457d7e6d12661e23f7dd09f8d26b0`  
		Last Modified: Fri, 21 Feb 2020 22:33:56 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed4e13c7b7237db460c7250ffec446cd033597c349d538f1a3bef2c61936f89`  
		Last Modified: Fri, 21 Feb 2020 22:33:56 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9acb6be6f2007b0d8af5a84186b3d866dbcb1eec846431df08803f6f5fa62f9`  
		Last Modified: Fri, 21 Feb 2020 22:33:56 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial-20200212` - linux; s390x

```console
$ docker pull ubuntu@sha256:fbbecfc4f9fc56b050d0a8617ff5e0aecfa1bfc6e23c041a574c19c90183bc48
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42815078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99098b69958a3ec33c58573f85484e591633a9110eb2aa3faccb0e5cbdbbadf9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:58:38 GMT
ADD file:2da08b5719e8f84bf1322ff4b7babef0750ca9f09ec09fafb2dd49471656ab45 in / 
# Fri, 21 Feb 2020 21:58:47 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 21:58:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:58:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:58:51 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5d1c06e617a886003bdc553ea5fb88f3d1b9f090ccd01b8f11f59128221a248f`  
		Last Modified: Mon, 17 Feb 2020 15:46:24 GMT  
		Size: 42.8 MB (42813593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014396d85ca8cff40d6f829c1dd4b726456f22ed02b58fc32fda25427a08540b`  
		Last Modified: Fri, 21 Feb 2020 21:59:51 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd0d716f0f324aed318dd9aa0cbe1f47a5ac863a633df8d39b7760f74d2adff`  
		Last Modified: Fri, 21 Feb 2020 21:59:51 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb96b2c9e76d5516a980ea87b6cd16e5f0fd5b6b47b4f4d4a694aab15d36862`  
		Last Modified: Fri, 21 Feb 2020 21:59:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
