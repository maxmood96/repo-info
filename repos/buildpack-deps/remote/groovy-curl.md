## `buildpack-deps:groovy-curl`

```console
$ docker pull buildpack-deps@sha256:616079d8ba7993ce08373a13262a0deb1ba44e0103009cb4a5b8cb21ea8d3d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:groovy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:266736dfc10d7851cb6b5fd2551b28ff257b2de393805ee4c6e8333245eddfbe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40381407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cff1e3b81f50e0ab9e8526661f26be09e92c6f9ed85223734e54d23628aa8f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:38 GMT
ADD file:6248e4aba6d7654cf97495ddc060cc9d68c5498500fe6ae03a10d955f0cc09b4 in / 
# Wed, 25 Nov 2020 22:25:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:40 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:42 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 17:11:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 17:12:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d8b994c442864dd519627740d3a4d134f385a2caa54b7f59bf9d372adcf7def0`  
		Last Modified: Wed, 25 Nov 2020 22:26:56 GMT  
		Size: 31.3 MB (31340118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0773f3f14174f9bc8047861c64c2aa0cc581e73b16b48194a2884ad3918d01b`  
		Last Modified: Wed, 25 Nov 2020 22:26:50 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b20aefff2dc282ec6e2f496acce5b228bd1dfc30057a8ed41eae0513191b312`  
		Last Modified: Wed, 25 Nov 2020 22:26:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc27e36b2d0ee938c0b5311d92b3ef7d48a86ab62b69c2e1773844ee2b73e823`  
		Last Modified: Thu, 17 Dec 2020 17:31:15 GMT  
		Size: 5.4 MB (5394338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77da74e5242a32079e203d6a25f429273cd9ee98a11e74fa79dbdad55f22c848`  
		Last Modified: Thu, 17 Dec 2020 17:31:14 GMT  
		Size: 3.6 MB (3645942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6472306e853317c225a2885b4559a7ddd48ccb0901bf2b4251eb031b8645c5c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34256081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbdb5a0e7f7724d0f183d069ef67b616902df43d5d149c6aed37a618ce81818`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:16:13 GMT
ADD file:80e3e615476328c1a866491506149109b9288c6fbf78c7d79027095f29b70bbc in / 
# Thu, 21 Jan 2021 03:16:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:16:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:16:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:16:22 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:01:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:01:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b0ce4bf9ceaa03e08560f7c9d42d32c4ddf828548e54ab8de5995560ab02d36e`  
		Last Modified: Thu, 21 Jan 2021 03:18:45 GMT  
		Size: 26.3 MB (26303232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a05aa6723d67ac51178e84d915f33ce8135dc8316286df199a36c53dd76e94`  
		Last Modified: Thu, 21 Jan 2021 03:18:39 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae60f7bca6f618ee79d283ea14533cb23828041bc4a8f2b3e62f7edcdfca8ea`  
		Last Modified: Thu, 21 Jan 2021 03:18:39 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33feb14c096fd2f78635259fb8f311a6b036e5127658c80f9a47624fb469e72d`  
		Last Modified: Thu, 21 Jan 2021 04:16:02 GMT  
		Size: 4.8 MB (4832361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fcff3f54da1627e5c9d56d84be22939a31935b6bc56aecfd6bf0c88407949d`  
		Last Modified: Thu, 21 Jan 2021 04:15:59 GMT  
		Size: 3.1 MB (3119447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1a8ff63bc9c6234012e0cacd3c7da6063dd7668c6766d7e9f57bf12f95acd755
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38880837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187f3b90c0e8b57170a814ea503970c47ef7a2e7aec81777c186f9accec89d0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:50:12 GMT
ADD file:1b147886fc9bab018dbd2bb3e83528e44f063a2f94b5eb7605735baf15e6e817 in / 
# Thu, 21 Jan 2021 03:50:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:50:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:50:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 06:08:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:08:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:37fd0b78a78cab203eb92c1165c2a208cebd097a17ae78667ff5956bcc8fc134`  
		Last Modified: Mon, 18 Jan 2021 17:31:55 GMT  
		Size: 29.9 MB (29878724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a235b21a23bebaf65f6e2a62bbd4e5eb7229529f72228bf9a297f56a18e1054e`  
		Last Modified: Thu, 21 Jan 2021 03:52:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3220b967683bf10e4caed4935b5ce42e8a07b2af8e3fb987508e58f6527fa1`  
		Last Modified: Thu, 21 Jan 2021 03:52:31 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7450c9743733d2b2aff29b2de8de11220a7e6c45444d3e9e00c14d7c22c346`  
		Last Modified: Thu, 21 Jan 2021 06:22:06 GMT  
		Size: 5.4 MB (5370315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb89bb68f94ffc08abaf380d7813901cb78973d5cffa8ca0e90fc6572fa118a9`  
		Last Modified: Thu, 21 Jan 2021 06:22:04 GMT  
		Size: 3.6 MB (3630759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:62f549a87f85346c3721565337b20715626d85ed8cff7737b0de98091e0dbbae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47098984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1838c0487ce02707975c1c769a31b124c3abb947740012e1dd512fe0081b93be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:23:53 GMT
ADD file:bd2b8fcd06cd2eb2cf7a28434e04fbbf862812835ae9891bcce13c78467f2065 in / 
# Wed, 25 Nov 2020 22:24:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:24:11 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:24:20 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:24:22 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 12:38:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 12:38:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:12b4d60f28ad6aeccaf03fc023c6279702739bb128bf2300f1294ccda567df49`  
		Last Modified: Wed, 25 Nov 2020 22:28:03 GMT  
		Size: 36.6 MB (36560461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8f98bb919b1ae08bf6f01e4adf4532b27a98bd02c5f15c22245aeb9bea5bef`  
		Last Modified: Wed, 25 Nov 2020 22:27:55 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee907fc457088dacd114983ba2b65ff886c02bfbf69bb3629a3f213cb44eb84e`  
		Last Modified: Wed, 25 Nov 2020 22:27:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352606e81d37cd930865d266dc5754ffae4c59b372a521b4b0d6f8b1ee04a7fb`  
		Last Modified: Thu, 17 Dec 2020 13:55:35 GMT  
		Size: 6.0 MB (6030921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfb72d0e13e43bd5e5c796dce1b4d2718bd26d1998ebe5189e5b96230d55ff0`  
		Last Modified: Thu, 17 Dec 2020 13:55:31 GMT  
		Size: 4.5 MB (4506566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b8ca8d64376c84e38729ca9ef136caf3110b535fbf121c4c854f92e877bd630f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40769143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2872267b87f7a3eb5d9be69774a937e3c74e6a588363c180a6a4532c9358848e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Jan 2021 04:01:34 GMT
ADD file:defba5f5671c8aed8054b5976546bf7670dc9e0478d234bed4094666c04faacc in / 
# Thu, 21 Jan 2021 04:01:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 04:01:43 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 04:01:45 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 04:01:45 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 05:22:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7444231bd1db8a6afa79e821daa78c79df88f83f3d33493669f35d540bd39095`  
		Last Modified: Mon, 18 Jan 2021 18:07:06 GMT  
		Size: 31.5 MB (31509336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9dea13eda213e3f3a4dcbddf25b319f2c2500b0ec786f9b716bf1187cd98f7c`  
		Last Modified: Thu, 21 Jan 2021 04:03:52 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74a4bfa27eae2dc6e6ec157abcdfd015736c68ed091b8c8214d6277240380fc`  
		Last Modified: Thu, 21 Jan 2021 04:03:51 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5da7f19270d659469e210e0e7f0f8fe29188bcd0a136725158ca4ef687178c7`  
		Last Modified: Thu, 21 Jan 2021 05:33:25 GMT  
		Size: 5.6 MB (5619257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906d04faffcd1afce212943a51f8b82454448497896fd4376d3ae50036cd1e0d`  
		Last Modified: Thu, 21 Jan 2021 05:33:26 GMT  
		Size: 3.6 MB (3639513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
