## `ubuntu:eoan`

```console
$ docker pull ubuntu@sha256:1780e594b61e73408e6f74988790f06a913c50ae4a9c7b51b7c1fb7130fb79b8
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
$ docker pull ubuntu@sha256:7ce552ad1c3e94a5c3d2bb24c07000c34a4bb43fd9b379652b2c80593a018e80
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28307689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ccb229a23d2d51da337c78c4ba1fd844f476e4639cd0c91099d1b62b8f8a45`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 19:20:34 GMT
ADD file:537f9883fb90d19383082b8ac20c17b581db9045a48fa28b83cab73fe317047d in / 
# Fri, 20 Mar 2020 19:20:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 19:20:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 19:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 19:20:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:eeacba527962683a1b026af611fe162d35281159762b699172caa48c69480f79`  
		Last Modified: Mon, 16 Mar 2020 15:44:17 GMT  
		Size: 28.3 MB (28276050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25405ed4f245fc5627d0b03996d04c11d492c7a9ff937f4562a18e8757c39434`  
		Last Modified: Fri, 20 Mar 2020 19:21:27 GMT  
		Size: 30.6 KB (30632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22752cd61bd53e9ac71e22fef539c165b3e11b368c1e54ca947260e317c4870a`  
		Last Modified: Fri, 20 Mar 2020 19:21:27 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9460de83957c509dd234ede9ea96d4d03b7f9cd252ef1497844f8450dedb6570`  
		Last Modified: Fri, 20 Mar 2020 19:21:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:eoan` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:a5df86ea40a8c36062fda6d31f176be51fd8f16a11cbb2f23fea90b97b526f8e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23767282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52c9ef9b7e3aaafafac771a3710e5bfc0167846cdad474c3a93fdfbde99d863`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 18:58:53 GMT
ADD file:d5ea94843f1a1e0976b02f8e02c5256c148157dd51f492da5181ad8753622ab4 in / 
# Fri, 20 Mar 2020 18:58:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:58:57 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:58:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:58:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2ea86edd9db57be0bd75bed151c49e031bd6699fcbd94130c3a8a8ab459692de`  
		Last Modified: Mon, 16 Mar 2020 15:44:38 GMT  
		Size: 23.7 MB (23735633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6c62210e628371fc8ed38017e5360a6a15489b56acd8dba096dc79768da4ca`  
		Last Modified: Fri, 20 Mar 2020 19:00:28 GMT  
		Size: 30.6 KB (30613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8325644a644873d31f1108862c1ed632f57c3fbc43ebe7603f57c2c0d39a3665`  
		Last Modified: Fri, 20 Mar 2020 19:00:28 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c4a05bf433715cda695415ab43dfdcae3e89606057e6ab273703fa768f4a6d`  
		Last Modified: Fri, 20 Mar 2020 19:00:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:eoan` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:21487bed47d1bba453146e98ab30e2ac831d6e84d3c570245ea0dd591ad78a29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26901016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f06251eef1ec510214999c71f10832a84509a6695c889b650d9113f5558f9c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 18:43:59 GMT
ADD file:908424aa468cb2a7000dd795511259c67a0f70d0bbafa4b05b405faf89be8a02 in / 
# Fri, 20 Mar 2020 18:44:01 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:44:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:44:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:44:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:20fe7914fb520387e59fda29e21ea64541bf9e7e95c9eef77a6ac68c18d23349`  
		Last Modified: Mon, 16 Mar 2020 15:44:48 GMT  
		Size: 26.9 MB (26869532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c6aa3850fcf8c6207823b79f1560303443a33d4fe996bf809b4dc7d00f7d35`  
		Last Modified: Fri, 20 Mar 2020 18:45:14 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02ac1bb4168bfb44e13693f63bd600c9230216a2443e5fb4839aedbb31635a2`  
		Last Modified: Fri, 20 Mar 2020 18:45:14 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1b98aacf49712db6881b4d4da724b4349964afa1b6e6b4e983b7465c028513`  
		Last Modified: Fri, 20 Mar 2020 18:45:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:eoan` - linux; 386

```console
$ docker pull ubuntu@sha256:ae9c75836a43c80842a753cacd6dc65269324d586eab540a71982d87bd6f2a42
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29076310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a84c33669ef39f9057a175b979f70cfd940fdc556774c24ff5d6aaa0365b858`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 18:39:08 GMT
ADD file:0e9faec03747f7230dbb61530a500027d8a504b2aa7edc19353d9d113a28b775 in / 
# Fri, 20 Mar 2020 18:39:09 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:39:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:39:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:39:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7ec2907f7e8e2aa58e6e8544a4c009b751bc4ffb0260097338c8af14584c359e`  
		Last Modified: Mon, 16 Mar 2020 15:45:02 GMT  
		Size: 29.0 MB (29044614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6611c39bb98f10485e66c9de26f541ea83047ec3a7c7c375b08960b001e976f7`  
		Last Modified: Fri, 20 Mar 2020 18:39:45 GMT  
		Size: 30.7 KB (30688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925c05ba7d1067bfcebc90f78d1d37877173cccaab5663827e1e19a564ae9064`  
		Last Modified: Fri, 20 Mar 2020 18:39:44 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de9c38a779a8dbacc0c634c58a8e8abbcb85229eac1910ff6d3fa00081dda86`  
		Last Modified: Fri, 20 Mar 2020 18:39:44 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:eoan` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:dd1f773bf12e6aafba4c4ee749e89888402b9edb0e3843372770451460ed93a5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33018242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5629624a6cd93f3abb8a0b6601a20e376558c22345b9d1651971ae66da16ca0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 19:23:08 GMT
ADD file:5f2d0c54e4b302f16104b557b94863ea583b0f5077cdba4a739077166e742286 in / 
# Fri, 20 Mar 2020 19:23:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 19:23:22 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 19:23:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 19:23:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ed545fde3a421d26f2fe47bd4ffaa6f5e4d1922ee226f849b9030af8e0469cb6`  
		Last Modified: Mon, 16 Mar 2020 15:46:10 GMT  
		Size: 33.0 MB (32986715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0dc90382a97787ce60215cad11117e850fe8c74a63cb5b8ce024645ea62b7a8`  
		Last Modified: Fri, 20 Mar 2020 19:25:21 GMT  
		Size: 30.5 KB (30494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c59e83ff7085e57aab1e4c48a50af629cf66f6ae0c896c7ca190d951b38b1f1`  
		Last Modified: Fri, 20 Mar 2020 19:25:21 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6ff0efafd163296380421cd94ed46d501335204734c716873fde2954ae4d84`  
		Last Modified: Fri, 20 Mar 2020 19:25:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:eoan` - linux; s390x

```console
$ docker pull ubuntu@sha256:aa80b2154ef971c51b31995b4896f5c089318841b8886d2e9a9ec988633ced20
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26714705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77233a456dc943fb20b126aeefeb3f9b827dfce8dee8741ab44f5fe7d8437a60`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:44 GMT
ADD file:590238292f6a053ea2bf6e08f583c7d381c15ead1a8a0f1bad600fca48d20648 in / 
# Thu, 23 Apr 2020 17:52:52 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4a7e39a0b3f9ba3421a213b5b6ae19b4ee4315b5aff0252496ef8117c7caae2e`  
		Last Modified: Mon, 13 Apr 2020 15:45:44 GMT  
		Size: 26.7 MB (26682562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15519bbe785a81349f4b9318ec98f07fb1d7ed9742eaf004a27806254935f5bf`  
		Last Modified: Thu, 23 Apr 2020 17:54:25 GMT  
		Size: 31.1 KB (31106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39a183d313a7aec756ef4cec9ebed83e7eefb892c64f68a74fb640abde8a647`  
		Last Modified: Thu, 23 Apr 2020 17:54:25 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0914614caf2827873d1d4b1f12426334285b8d984af44e48b64b7db18c3ee4fc`  
		Last Modified: Thu, 23 Apr 2020 17:54:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
