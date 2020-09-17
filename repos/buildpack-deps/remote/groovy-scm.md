## `buildpack-deps:groovy-scm`

```console
$ docker pull buildpack-deps@sha256:e247a6fda0d7e2c17020413fba823d963826cc7a5fe5dd6b7c8b6882b2b5a589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:groovy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7133d90d743acf348852f8999198169e563caf5a3a7f3650391bee1bb246b100
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94275718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a7c6f547ae4136decc8b9a93263163319cc76b543ed16d89c9a0d4a921ec41`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:15:22 GMT
ADD file:53ca8a3f446b0751019d522066ce844f6281ffb5b15e9605cd8940176abf4c76 in / 
# Wed, 19 Aug 2020 21:15:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:15:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:15:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:15:25 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:27:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:27:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 19 Aug 2020 22:28:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d94cf711eb1df9e05b5ab9c367f7417c481e9b5deee1724f93b96c77bff11c8f`  
		Last Modified: Mon, 17 Aug 2020 15:53:01 GMT  
		Size: 28.8 MB (28809294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc1ea4c1ef986e00d114cccc9e5fbbe6bd5b8f35145cacb0f12ae3389c4e0a2`  
		Last Modified: Wed, 19 Aug 2020 21:17:10 GMT  
		Size: 31.0 KB (31042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2147ebd301d69260017329191f4072fbb193e2c1c092542270947091c6eaa60c`  
		Last Modified: Wed, 19 Aug 2020 21:17:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2955d4b7554096a19ae03fac9a539a3106b871165d9beef32fb6f3b16bed6c4a`  
		Last Modified: Wed, 19 Aug 2020 21:17:10 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff92321eef344d6f7de248e128d72b31e764780d34efaa3ddd1379ab12aed1e`  
		Last Modified: Wed, 19 Aug 2020 22:36:01 GMT  
		Size: 6.9 MB (6863303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378b1e0fc390f4096ef8d0f7e763d0862ec62b697cf1bcc6e89a0e73fa780949`  
		Last Modified: Wed, 19 Aug 2020 22:36:00 GMT  
		Size: 3.6 MB (3586428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403a0f8b5c35d4f809b059fb0d3e8ad6ddb94f7050d41a689fd396fda1b3f784`  
		Last Modified: Wed, 19 Aug 2020 22:36:25 GMT  
		Size: 55.0 MB (54984639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ecc92cfd42bb2fc2bfeeabd4ff84937c238cae1a25d83416b60686ae9bb784e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83063077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439693e63f342ca255468b4ea73f3f93804cbb9c9dc852ab3a6dca9934ca2499`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Sep 2020 22:29:17 GMT
ADD file:5d040dcb9ecf5ea37a47528d7671364427c6db8500998cdd61b0d6197561327f in / 
# Wed, 16 Sep 2020 22:29:20 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:29:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:29:24 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:29:25 GMT
CMD ["/bin/bash"]
# Wed, 16 Sep 2020 23:09:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 23:09:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 16 Sep 2020 23:10:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fc3824011019fe6b44b5748af8b7264a274c0a308a19877b49366eca72e87c6f`  
		Last Modified: Mon, 14 Sep 2020 15:55:44 GMT  
		Size: 24.2 MB (24215640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6d99a2cc8e2dba749dca1fa6342625fb00d84d872023ff24b63cf05de7e300`  
		Last Modified: Wed, 16 Sep 2020 22:31:01 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31de15bc5097b24b529945a61185eddf0085a7c414695486a452ae14bbf76441`  
		Last Modified: Wed, 16 Sep 2020 22:31:01 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df75cbfcf2f91455215a85704a6718af9f113389d440c9945cf4a364a2b7e84f`  
		Last Modified: Wed, 16 Sep 2020 23:18:40 GMT  
		Size: 5.9 MB (5900389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da3018ef17ec885a89b88f73ffa69e4d81da2be4a4f3fc6e94eea3ce96e4f03`  
		Last Modified: Wed, 16 Sep 2020 23:18:37 GMT  
		Size: 3.1 MB (3059076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4f4563acb0571e477217543b72004e2084f79ad41f4e1a6ea0391056b724c4`  
		Last Modified: Wed, 16 Sep 2020 23:19:03 GMT  
		Size: 49.9 MB (49886934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e606703d00d3c6dbb9c9cef34852e6e4095bdab50883738f23813c8eca8c24c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92748729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44210e04013e14312abc6f2281ed92c83a3462be39ba0a2a9715dcb6f2d5cfc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:30:48 GMT
ADD file:a2368478f6147dfb550f11fd08fa580527841837e6de780105b0ee3c869e9045 in / 
# Wed, 19 Aug 2020 21:31:01 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:31:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:31:07 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:31:08 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:05:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:06:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 19 Aug 2020 22:06:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:11602f8d9ef9a64d301368c826db17ed80fdaaa6895c8479600ecfb22906feec`  
		Last Modified: Mon, 17 Aug 2020 15:53:49 GMT  
		Size: 27.4 MB (27411937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9baf34eaf014c357d3680a1c3659aa57594a0cf1e8f13f3410ff6e659147f0`  
		Last Modified: Wed, 19 Aug 2020 21:32:46 GMT  
		Size: 31.0 KB (31023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f4efba19094c2a8cdccdb0aad9f813a4ae4c9ecbb8028522dfe7136037188c`  
		Last Modified: Wed, 19 Aug 2020 21:32:46 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61503eacf6a2d668185f96d1697af41f5c1798343a4903c2141b75db7ba35fb9`  
		Last Modified: Wed, 19 Aug 2020 21:32:46 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959af42e9a96454cf5f9d0df1902056102efc1f8c5fce06fa385fc6234dc4e18`  
		Last Modified: Wed, 19 Aug 2020 22:14:37 GMT  
		Size: 6.7 MB (6727192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74393685c57568d31f3de5b52a660d8f421b7493deab4a65599fc6cafa475491`  
		Last Modified: Wed, 19 Aug 2020 22:14:37 GMT  
		Size: 3.6 MB (3570662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9200ef6e477aebe4b7e791f3d29f1cdfb8e61ca091a9fa5e63acb3b5db0551`  
		Last Modified: Wed, 19 Aug 2020 22:15:02 GMT  
		Size: 55.0 MB (55006878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:34fc3a3495a7ff8a15d4b459a63c6483ecd1efd3fff60609ffaf202727807e52
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109161545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701a1f5cdfc6c53cefb236bd347a775688a9c77695119fd6768d8ed74863c6ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:16:10 GMT
ADD file:d2bdf56089aa739c01f4fea190a17051fbcd45e31fa5ba26d466921d4b528a06 in / 
# Wed, 19 Aug 2020 21:16:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:16:34 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:16:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:16:49 GMT
CMD ["/bin/bash"]
# Thu, 20 Aug 2020 00:32:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 20 Aug 2020 00:33:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 20 Aug 2020 00:36:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bd233d33322880c9108ff9d4a2836417f422f1f76cea04cbce12861b48e4ec0a`  
		Last Modified: Mon, 17 Aug 2020 15:54:01 GMT  
		Size: 33.5 MB (33521520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948f26d4116ec9c2f8ce7b5d3765e3f977e8e62da7b636f40f1d3d554b6027e3`  
		Last Modified: Wed, 19 Aug 2020 21:19:34 GMT  
		Size: 30.9 KB (30877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2568d3b37f18de7a6f08771049d897ef5d8bdbf2ddba783262fee3d781a2c588`  
		Last Modified: Wed, 19 Aug 2020 21:19:33 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271de21485d292cc9b05d3b055184c64751e0cf915de5be7c595ef973f80d104`  
		Last Modified: Wed, 19 Aug 2020 21:19:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e242cd3731e0ee7c6107fbde83668bf7dbbc2f329278aa64548b8b6e69ca1e`  
		Last Modified: Thu, 20 Aug 2020 01:06:16 GMT  
		Size: 7.8 MB (7816668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0357a04a0eaa3f73a4e0de3317b10e7b6ee2cff741c22e8b4cd78cab3c8d0b77`  
		Last Modified: Thu, 20 Aug 2020 01:06:15 GMT  
		Size: 4.4 MB (4446779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4acf10fdc3db810bf8d904b3a9bf00377f86aa5ac5f0f7a7705f15edc031154`  
		Last Modified: Thu, 20 Aug 2020 01:06:41 GMT  
		Size: 63.3 MB (63344665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4bb143f925bc1b33b563f777c771fb0f407f75cf387d63203e129e0b497c8c83
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94268782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a447583931026cf8ce46529091b080d643e5d022a9f785aaf9e70efd3693af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Sep 2020 22:51:52 GMT
ADD file:8b60e925c7d1fc58aa03cec6200d56eb171cec4d8856766d062a02d6a9d35045 in / 
# Wed, 16 Sep 2020 22:51:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:51:55 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:51:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:51:56 GMT
CMD ["/bin/bash"]
# Wed, 16 Sep 2020 23:27:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 23:28:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 16 Sep 2020 23:28:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:526c3f0b06221923628388a7879c5dca9ad737704d8a5bb52f62eccb945d9eea`  
		Last Modified: Mon, 14 Sep 2020 15:56:09 GMT  
		Size: 28.7 MB (28685212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145f5fb5761ec5efa6c7cb81f5dc235263a5a2f9e47211b8f15246e0cb57e2ec`  
		Last Modified: Wed, 16 Sep 2020 22:52:44 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b29e60d7164662b93f8c1f52116015aa2b25b569943a2e639e113d24636e45`  
		Last Modified: Wed, 16 Sep 2020 22:52:44 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2f1d47f5fe9d42008269fa4e79252c02f5f254b095022a8fae3d641d3cb82b`  
		Last Modified: Wed, 16 Sep 2020 23:32:36 GMT  
		Size: 6.8 MB (6815484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfaad1df7e2e32fe332a0cb661fc000f23fc4e690bc709af6adc5c7b1bf48f57`  
		Last Modified: Wed, 16 Sep 2020 23:32:35 GMT  
		Size: 3.6 MB (3579356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41544c86e4dc24fbcf1c8586679a1d4d2a42fae5f691150b130b62e7e425e974`  
		Last Modified: Wed, 16 Sep 2020 23:32:50 GMT  
		Size: 55.2 MB (55187694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
