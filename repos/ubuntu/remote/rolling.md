## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:9eba4a1283c2647bda193baa6adf4a00e9c0b359db670d96ce75b79112e973ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:rolling` - linux; amd64

```console
$ docker pull ubuntu@sha256:91162f2808e0e07cb8b6836dbca59570b1b3c52ff88fd11daa1df633a2f02da3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.3 MB (29267156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274cadba4412e0da41432a07a7a248667123e08e70faec614efc63cf4c989645`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 May 2021 19:44:58 GMT
ADD file:218192f8ea2feaa779660a584c540d40170f0041f106bc6a2eb183bd548a588c in / 
# Wed, 19 May 2021 19:44:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:45:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 19:45:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:45:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9178282edeae5e16e92b9c38320ae3f6048d47692b4efefec09566a40ae534ab`  
		Last Modified: Fri, 14 May 2021 22:10:59 GMT  
		Size: 29.3 MB (29266114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ff34c1005ff0775ec131db9738e22f6c31292de462d7a6a28fbafd5114c240`  
		Last Modified: Wed, 19 May 2021 19:46:17 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6415519001ad74a1a9a1220da9f9c4e45de578fa0db8c5d4132860b64260b59d`  
		Last Modified: Wed, 19 May 2021 19:46:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2581c675b3727523ea723a0d9a99361a547d03743bd2820cbe58eb48355eac2c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24752518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0d7dd9f74332a1c61c6832ec49514acadb6838d0d8033d4e13496c52db4a4d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 May 2021 20:22:48 GMT
ADD file:e5870ac6e64d788a9ed34c217ecc70648386b8ffc1fb0bbba393155bb7f93437 in / 
# Wed, 19 May 2021 20:22:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 20:22:52 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 20:22:54 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 20:22:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bdd4355f13aa64cacc203ae21d7f6b50c13e90d4ddce9ce1e27ae5aa46cbdd31`  
		Last Modified: Wed, 19 May 2021 20:24:29 GMT  
		Size: 24.8 MB (24751484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8651e11b134edeb4fc951dd121afc6fedf7810f5b2cd90819169fe4abe4d7f`  
		Last Modified: Wed, 19 May 2021 20:24:23 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6614e7e3c4bd3c9c88b4b28c2ec82a93cf94d5d20cb70a3c944b0f0b2827234c`  
		Last Modified: Wed, 19 May 2021 20:24:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:0fb0d395bd896ff4670143d0515fb431c638cf9accc7f543114e33b392700eb2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27838449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ad5fe250d1b6d5ee7a6937868f72a4b5c385e983a2832f871091bd25e914dd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Apr 2021 22:48:37 GMT
ADD file:f6b776f11ca04a349ede73efde878cb528ec444a3a342a12ab4942dc9120a8d8 in / 
# Fri, 23 Apr 2021 22:48:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:48:44 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:48:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:48:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:30e34916c3b1ae71b2d4f4c80992d996fb7d9ed8857fa9da152f558e07ae5354`  
		Last Modified: Fri, 23 Apr 2021 22:50:42 GMT  
		Size: 27.8 MB (27837418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da710502d22348ee6d27834480cf8855c4332056fd5baafd5f8b6d4c91ab97e`  
		Last Modified: Fri, 23 Apr 2021 22:50:35 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c334551e118c3954ba6910ef0cf5783351985654b6102f50ec31460e7c0f671`  
		Last Modified: Fri, 23 Apr 2021 22:50:35 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:b480e89fe48efa2842583b639099b23320a1abebf4f08d3e8cc90deeca2637da
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34381953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a0f24e0c3ba4c7be5b46830f73596d84ea445e7393c7704bf305d4e4c13746`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 May 2021 21:30:35 GMT
ADD file:4e84ae3e96cf3af42c0e94a80152b5d84984338ccf12a12d57949418db463f75 in / 
# Wed, 19 May 2021 21:30:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 21:31:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 21:31:26 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 21:31:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4f63091d6b9ae5a35339207660148ee4ee33ae20a6eb7626d1e2b3469c26b69b`  
		Last Modified: Wed, 19 May 2021 21:34:46 GMT  
		Size: 34.4 MB (34380913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccab65e4ba2c5621eea660e6c57502dd2646ea3fb2da5c3753e68941413cb886`  
		Last Modified: Wed, 19 May 2021 21:34:36 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998975cb9643b2a2d855742e5f264bae1ed9b997fdbfe58d2ed467088f97150f`  
		Last Modified: Wed, 19 May 2021 21:34:36 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:9b2aaea0a99d241df88443c35e56cc8201f1b8e658aecd15eb375d84479ad832
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30109504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373aa7f91fa4aafbab457a00505fe1ef10bb3d728833457486c7fa60386434a9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 May 2021 23:29:24 GMT
ADD file:6f7dc43f7b51d3fb8c5308a181664b866f08c524964307f1ee563e0e5d6554c4 in / 
# Wed, 19 May 2021 23:29:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 23:29:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 23:29:34 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 23:29:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6b78ab758f4c2dca59b062c460d4d1965d254488e90f2821c5a7125ce4d11fa`  
		Last Modified: Wed, 19 May 2021 23:31:01 GMT  
		Size: 30.1 MB (30108470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b015a6402d4c7900ebd14e1951787987c07bd462db21f64d488a5e582fb6496`  
		Last Modified: Wed, 19 May 2021 23:30:57 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3db62be722a0e958087a8d44ad120a313ba0a048934086edc61aba61d608ae`  
		Last Modified: Wed, 19 May 2021 23:30:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
