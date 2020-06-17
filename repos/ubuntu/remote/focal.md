## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:52259450119427dab05c0c455121c48d7b04cee2d61b5dbdde1219b2163af572
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
$ docker pull ubuntu@sha256:93fd0705706e5bdda6cc450b384d8d5afb18fecc19e054fe3d7a2c8c2aeb2c83
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28589814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74435f89ab7825e19cf8c92c7b5c5ebd73ae2d0a2be16f49b3fb81c9062ab303`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:20:53 GMT
ADD file:b2342c7e6665d5ff3850d4f04e2521d1851eb2054f9a8d56fcf4e7c314b9f20e in / 
# Wed, 17 Jun 2020 01:20:54 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:20:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:20:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:20:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a4a2a29f9ba48efd3d2075f395538b2eec56fb1bedfb7aecf5e54174446f9e2a`  
		Last Modified: Sat, 06 Jun 2020 15:19:59 GMT  
		Size: 28.6 MB (28556492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127c9761dcbaa288abc58fc56437c2f2ffbe611b9f7f30e0b5b43cd348bb2094`  
		Last Modified: Wed, 17 Jun 2020 01:22:02 GMT  
		Size: 32.3 KB (32317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13bf203e905463e64d89b14509aafa983fb8baf7c1931fe0a65652aeb6c838f`  
		Last Modified: Wed, 17 Jun 2020 01:22:01 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4039240d2e0b4bcb42ccbce75bc54570e471ad81457478de35fbeef63536e9c0`  
		Last Modified: Wed, 17 Jun 2020 01:22:02 GMT  
		Size: 161.0 B  
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
$ docker pull ubuntu@sha256:a4bc8c3c9137c5dac97f7fe01c7a20e3f6d801cc5ce27ef806a7d8005e80ecdd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27193132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454b2a641b9d159a48e67e1436003babda46ac9858a8b094081e32b39bb18abb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:22 GMT
ADD file:6d1bd041dcbfb2d51c871c8eb820202f5597b37ac4e4b94ce976fbc157619c8e in / 
# Wed, 17 Jun 2020 01:43:25 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:63de6a4b0fc89f1aa36d95a840e6729cca22d2abaa887bfaf634c40ad4560ed4`  
		Last Modified: Sun, 07 Jun 2020 08:26:19 GMT  
		Size: 27.2 MB (27159755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243514e240f4c2654743395ffa5aed01b5eaf985f0118cdb2089629e0e9747d8`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 32.3 KB (32336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ba51c40fb5f743fb4a4050b63644e7727c21a1cffba4c4767ac41118ac6d3`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684e0fb606a03cddd5fc30fb6aee6055e851951eff13e4859295a3097063bba7`  
		Last Modified: Wed, 17 Jun 2020 01:45:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:44a663a43cbcc0d61bbe728fcc44882b73f2d4f023fc3032f81cd6d439e6974a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33311720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e72516910fa6818a846836da7932d742cd9601bbee5a2918f425a85e478555`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:25:08 GMT
ADD file:1218b62543f457165526a15dbd449c30449a7d481b5d4095ff39313c254d1cb9 in / 
# Wed, 17 Jun 2020 01:25:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:25:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:25:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:25:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1af88179c92bb1eaf179a905a94146fbc96900d091b6885a97ea2b36adb7204d`  
		Last Modified: Mon, 08 Jun 2020 15:49:18 GMT  
		Size: 33.3 MB (33278524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225d31ce61fc3542d2f2f42f95f9253d839a503cd4e8ddbee90e8e41d746d24f`  
		Last Modified: Wed, 17 Jun 2020 01:28:53 GMT  
		Size: 32.2 KB (32157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4817372593f6b4239eb9d7f57327510cceb0f7a4d469be9b51b40bb27de1eae0`  
		Last Modified: Wed, 17 Jun 2020 01:28:54 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bde024410c3e178191ea8c0f493ede5a8fc628112c6f2441f1f58eb1001c7ad`  
		Last Modified: Wed, 17 Jun 2020 01:28:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:1ee531025403c7682af5fb8fd87b1df1c037d7184fc30f155b7adb20660369e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27303525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872557817f5bf7f2725cada046f3da5e892106ee4110bcde5f7d2b2f545beaf5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:11 GMT
ADD file:0f436e9f094fe1b3df711f99328c816c0b29aad0270ab3b7f75dbcfdf9127e9d in / 
# Wed, 17 Jun 2020 01:42:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:14 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b0743f34f12abe35c28ee89eba07aeee055b4849cf98d248b342555c5bc35c8a`  
		Last Modified: Mon, 08 Jun 2020 15:54:28 GMT  
		Size: 27.3 MB (27269536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef681563df5986a5190736ce4a6a039ada68faea3c4e90a8568f467260e2922a`  
		Last Modified: Wed, 17 Jun 2020 01:43:17 GMT  
		Size: 33.0 KB (32956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f8724b94bcc6d19d145d9ea95632ec1f05130ad50f0fb386e6aa8b26022776`  
		Last Modified: Wed, 17 Jun 2020 01:43:17 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38394996142527765d189ed7cc0682e69c52ce9a77845b244c65212359f01208`  
		Last Modified: Wed, 17 Jun 2020 01:43:16 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
