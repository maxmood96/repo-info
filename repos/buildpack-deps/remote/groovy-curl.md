## `buildpack-deps:groovy-curl`

```console
$ docker pull buildpack-deps@sha256:0fd92b46205e493b33f106708af165219d2bcebc710ac965f45319aed454be38
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
$ docker pull buildpack-deps@sha256:423d4a0c2e6129b8f399761e325d4cbc0663aa0f40e22c332143fba7c4c7381d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38880122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058b7054c2bec1b39c3dafeb8950d97d210f9c98e11974718bcc8ec08299b592`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:43:30 GMT
ADD file:64620b7461f90248a314404599b9aa3b9b592786bcc8ed2cae9df8a7e1f15304 in / 
# Wed, 25 Nov 2020 22:43:33 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:43:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:43:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:43:38 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 10:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 10:24:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2769ac0e7b9ff64f87f3db82269939c4119f3e9b548bf84e398e068642e07624`  
		Last Modified: Wed, 25 Nov 2020 22:45:16 GMT  
		Size: 29.9 MB (29882425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b76975e3e10573aec5f323bc1d6dbc76af857b1dc3289a68a449dfb881dc2b6`  
		Last Modified: Wed, 25 Nov 2020 22:45:09 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958ead7f79658868738b309ef9d34e12c738ee519ace595275e35b3c7ea3a5c2`  
		Last Modified: Wed, 25 Nov 2020 22:45:09 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37af99f24ef95aad682c01e0bd626f4c7b41e9763b8b2f33d3cbbf740def505`  
		Last Modified: Thu, 17 Dec 2020 10:45:52 GMT  
		Size: 5.4 MB (5366390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81382319658dac003311ab8d6291f851b363207397e36de56af8614c123888d`  
		Last Modified: Thu, 17 Dec 2020 10:45:51 GMT  
		Size: 3.6 MB (3630272 bytes)  
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
$ docker pull buildpack-deps@sha256:c9c20696009ab44cf26018da9ba1f750d0c73aac77b380219a089d55eb876817
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40718074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe0c8cc2f2d8aa1ef4ec6fb843901265287ee7aa9c0e5730f642ce5deab76b9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:45:41 GMT
ADD file:af8181cb78887aa9e6aa7f7b33a8ef7b76b74cabc09f582883a8d3111c0fe9e9 in / 
# Wed, 25 Nov 2020 22:45:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:45:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:45:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:45:53 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 11:31:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 11:31:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:abd4319bb36506beca49a36e3151713760b1b1a72286ebd52ed6a0f8b037ef26`  
		Last Modified: Wed, 25 Nov 2020 22:47:37 GMT  
		Size: 31.5 MB (31461133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13be14e62d3b49d67b17ae821b83ac4bdfd2186f11cceaa27ea603582a04e6e6`  
		Last Modified: Wed, 25 Nov 2020 22:47:34 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285f4745ab7467cbae8d29dc6729e2735cabc05177631c8eb03cfafa79c8bd58`  
		Last Modified: Wed, 25 Nov 2020 22:47:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d16be2146ac592474064f3f720ae9c0c96bdd0d93bf161bcece2d2fe538546`  
		Last Modified: Thu, 17 Dec 2020 11:50:44 GMT  
		Size: 5.6 MB (5616689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc21125f338cd97f3a76cdd72b0de6e21c30b25a9b86e013b7e4c912e43c38a`  
		Last Modified: Thu, 17 Dec 2020 11:50:44 GMT  
		Size: 3.6 MB (3639220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
