## `neurodebian:groovy`

```console
$ docker pull neurodebian@sha256:08944f1f9da5dbe1d39803828ce7857fad7f7d6aa2e0d676e1286b47e18b030a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:groovy` - linux; amd64

```console
$ docker pull neurodebian@sha256:1b9ffc7c0428d46797ca946a0d9cadaf930708fae392893f02bd974a5fd2ac9b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37192676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e503306527d3d7a33aa3921095b0ec31b0566044694ff4c2ebb2710b44d5bea1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 May 2021 00:28:11 GMT
ADD file:5582a76cd73639bd7b5f941762801034fe6d3297d63d8333085c79c31b5e777a in / 
# Wed, 26 May 2021 00:28:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 26 May 2021 00:28:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 26 May 2021 00:28:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 26 May 2021 00:28:15 GMT
CMD ["/bin/bash"]
# Wed, 26 May 2021 00:58:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 May 2021 00:58:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 26 May 2021 00:58:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian groovy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel groovy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 26 May 2021 00:58:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0dfa4d6d32846900cdf518b31b7420c8e3bee78df56f061347f079b085e55eed`  
		Last Modified: Wed, 26 May 2021 00:29:22 GMT  
		Size: 31.3 MB (31339605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ba66a34e9b2cf96e7958749a4fdd29a90699b6cd7eb67976c266a8277a26b`  
		Last Modified: Wed, 26 May 2021 00:29:18 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6382425bb0d013b4122cc28ffc63f8bce680a6562260cb6fa715f6f16a59db`  
		Last Modified: Wed, 26 May 2021 00:29:17 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46eeeca4d4ce3cb659115e6dafd3f78aab2ed8ad58dec52d61da3f186af75956`  
		Last Modified: Wed, 26 May 2021 00:59:26 GMT  
		Size: 5.6 MB (5595458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea4e1905b6584552da34ba65770026f64c3f094c73ac304746b4a6936176dc1`  
		Last Modified: Wed, 26 May 2021 00:59:25 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7235b3be881d5d75d6ac61ca5f94d659eb3fe63b3bc25395155ef55eef66c3d5`  
		Last Modified: Wed, 26 May 2021 00:59:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186f0cfcb8025c470beed98ddaa8215b552aa5cf7abf1bd45afb3d01b1ddbf57`  
		Last Modified: Wed, 26 May 2021 00:59:25 GMT  
		Size: 254.6 KB (254567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
