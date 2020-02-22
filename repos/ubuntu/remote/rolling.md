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
