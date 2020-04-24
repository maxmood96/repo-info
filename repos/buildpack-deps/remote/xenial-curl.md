## `buildpack-deps:xenial-curl`

```console
$ docker pull buildpack-deps@sha256:fad426cdc300b8e707abb686c4f4c8e1b5c797a8fb4a59dc3414ccb68b24ba69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:xenial-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4bafd979210b581f9ea1ecc2380cc56fd41d9c7e3c24fcea45b9d1dff9919bfb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51517928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc0befc51610f7ca77bc4f1e0df71d03b10eead4ad9f0edd0507f276f229610a`
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
# Fri, 21 Feb 2020 23:00:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:00:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
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
	-	`sha256:3331c6158137ed51eddd9309ab74a6fdb1353c9ea3e1c18a8ecd1936ee76cf64`  
		Last Modified: Fri, 21 Feb 2020 23:05:15 GMT  
		Size: 7.3 MB (7324657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:52e5af27b9f749fdab03026ffbf1cb55cbfeed17c0c22804e66a7b036df22ea6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45067740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbf401858eac0cee14b93a39fe74d496c52a7561237a4a45cead6eaac396c4c`
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
# Fri, 21 Feb 2020 23:20:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:21:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
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
	-	`sha256:f8acd864c4c16ff213b32f0fc5720f1744561665a9a078a6ec646be3e7d983ff`  
		Last Modified: Fri, 21 Feb 2020 23:27:07 GMT  
		Size: 6.2 MB (6175848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b87e3c322e7550c4ebbf8b9a50521b78adf5cf2df5ca5f3ae4fe6a49b4a8340a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46324553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51177d0079ee5314e970ce9f9fd74cfc21d4665efc237e7e2d4fafa881c376c`
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
# Fri, 21 Feb 2020 22:33:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:34:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
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
	-	`sha256:3ba97f922b0ec209301846d33d2a45b15f967e4d7d63c14ef550bfa3f856530d`  
		Last Modified: Fri, 21 Feb 2020 22:40:13 GMT  
		Size: 6.4 MB (6382693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:acd2b3be6e95855a6a481eb6b94792fe61de6ea2b0845cec9ec17cc377979441
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51644869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd80f7ef5c8cc99c33b0a2ea74586a7364dce32307b0b3654b8c5ca4ef3bac0`
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
# Fri, 21 Feb 2020 22:07:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:07:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
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
	-	`sha256:c7f41969dfee15c3a35241e28aa5a20cb836573655406395d0227ece58d39263`  
		Last Modified: Fri, 21 Feb 2020 22:12:58 GMT  
		Size: 7.5 MB (7470060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:eebeee0faf40aee97842079745c4d0880932907d74f93831011b7f55cb754d1b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53335708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00f4d5527a753ada95c0cc23ea6316098b55c6fffbe70dfeb96cd38a692f5e9`
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
# Fri, 21 Feb 2020 23:15:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:15:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
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
	-	`sha256:cc812dd911cb614e424234a7bb27e747987ac6092b1ec91b4970d97bbafdab75`  
		Last Modified: Fri, 21 Feb 2020 23:32:20 GMT  
		Size: 7.2 MB (7233311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:31b194f325b83e3a7fcf8296d6d737b1e261253c92cef01bf2e32bc8c81f61a5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49905779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2feead81f9fea37b3a9c0f6aff585b2f518b1c3239e3f237687e48f3d6a892`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 23 Apr 2020 17:53:43 GMT
ADD file:ed32a6507ce62172a75daf32a3e745ad7d8e5ec2c72a0dbeb1ad18af3be6cde8 in / 
# Thu, 23 Apr 2020 17:53:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 17:53:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:53:57 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:53:58 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:52:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 07:52:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c68931fb1bceafcc32dd3b6ff5116133bbd2be9aad34c04cc81a270dca82df13`  
		Last Modified: Mon, 30 Mar 2020 15:50:44 GMT  
		Size: 42.8 MB (42840710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febc54d02b58a20f824a7c8503ccc8d35a35482936d8dc59dfe0adc3359e1fb7`  
		Last Modified: Thu, 23 Apr 2020 17:54:52 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5aed9cad1309eeb57273b441dc4661e5f3dd6055d9960dad401eebfa93f6178`  
		Last Modified: Thu, 23 Apr 2020 17:54:52 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e342d8c62e47069f917221bdd6d21bf7ccab595f1d2feab7554cb3ae93d86b`  
		Last Modified: Thu, 23 Apr 2020 17:54:52 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d397414e6f5a0ba42f19b6dcbf646decbe786620da4f8de5865c81eeca24ca4b`  
		Last Modified: Fri, 24 Apr 2020 07:56:57 GMT  
		Size: 7.1 MB (7063576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
