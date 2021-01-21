## `buildpack-deps:groovy-curl`

```console
$ docker pull buildpack-deps@sha256:2e6720a292fa840b4745a797fcebd17170b98347901d5633a4a7b6dcd01db3c9
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
$ docker pull buildpack-deps@sha256:8414cdbada56fe6972e8c2ef5f7f2ee5ae3b9aca908d392903cba86b0d5f01cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40394741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4163d807a1b90f9f0f29410067e477266bbeae327d4a96a02c44316b90bbb7fd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:40 GMT
ADD file:fbf1e6b04a66bc3f4ff7a5c599fa18604caee5c848328ae120a4a97d3e4636fe in / 
# Thu, 21 Jan 2021 03:38:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:44 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:49:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 07:49:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a09400eba642b8443b0196d54f94bd75bb9e0ca23fae24e945ce8ef12237f09e`  
		Last Modified: Mon, 18 Jan 2021 17:32:09 GMT  
		Size: 31.3 MB (31348186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdcab926b54c7b115b820e2ea38ae0a659bf65a31345459bd404c3780b024a6a`  
		Last Modified: Thu, 21 Jan 2021 03:40:49 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c1d05f510d7751d87a8115e0e927385901b2f17d1838902a51fd902cf855c3`  
		Last Modified: Thu, 21 Jan 2021 03:40:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78578fe43fdf0a8b1c19e360b81ecdffd87b0d6acfa1e800d36ab4f2636c1487`  
		Last Modified: Thu, 21 Jan 2021 08:02:46 GMT  
		Size: 5.4 MB (5399325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2271ea13f0fab7ee0a29b362f115c6accb1421f9faba4e395f39a32257d86bf`  
		Last Modified: Thu, 21 Jan 2021 08:02:46 GMT  
		Size: 3.6 MB (3646219 bytes)  
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
$ docker pull buildpack-deps@sha256:e631e9ef09b974af2e7b74e36c3d365cad3bf66411c783e49e9230d02fcecb44
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47090220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687be7047625788a37cc0aecf6053c0767930a285d3b91a65ec98fb9679763b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:51:12 GMT
ADD file:a10e8e48da10ced8afe769f787ff5a4ca06f4fbd9fa540fc352cb1532f5cf79a in / 
# Thu, 21 Jan 2021 03:51:33 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:51:39 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:51:47 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:51:51 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:15:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 07:16:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ef02a96d03691b901f9aaecbda4044e0a465bb09a96ec254a558f21aaa99d87d`  
		Last Modified: Mon, 18 Jan 2021 18:06:47 GMT  
		Size: 36.5 MB (36546462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb86170ee335cc78e8dba1ebc6578dda027cebcf94e0c218542c7bd56823df23`  
		Last Modified: Thu, 21 Jan 2021 03:55:20 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaa602367c34b7783eccd2b06110907f4ee35f7da6815511505d55c6a4ec4b4`  
		Last Modified: Thu, 21 Jan 2021 03:55:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699d439101b23a806560cdb986474df97e830feb91146f947cbec099e7eafdbb`  
		Last Modified: Thu, 21 Jan 2021 08:09:24 GMT  
		Size: 6.0 MB (6035868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98634b432b61959bbc5fbfa90c2bff853805200b53df947d94a0a421453a20e3`  
		Last Modified: Thu, 21 Jan 2021 08:09:23 GMT  
		Size: 4.5 MB (4506849 bytes)  
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
