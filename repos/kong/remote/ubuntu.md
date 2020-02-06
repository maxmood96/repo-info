## `kong:ubuntu`

```console
$ docker pull kong@sha256:f4ee50737fcc050eb05744a0f151f7548b4ea7dfa320176757be84a47707cd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:18147ca4859050dec29255f10d2590fca192bb7bf3fff542661865c3baa6c62e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84715605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d46fabc7e4bcea9d89865f8f351c7d154235105ab0bdd3ad039b5527a66e6f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 16 Jan 2020 01:21:30 GMT
ADD file:4b2eb5cd0b37ca0154f3c5ad9212f5bc7244a35806395a9c76a96723d708b83a in / 
# Thu, 16 Jan 2020 01:21:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 01:21:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:21:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:21:32 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 03:58:01 GMT
LABEL maintainer=Kong Core Team <team-core@konghq.com>
# Wed, 05 Feb 2020 23:32:07 GMT
ENV KONG_VERSION=2.0.1
# Wed, 05 Feb 2020 23:32:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates curl perl unzip     && rm -rf /var/lib/apt/lists/*     && curl -fsSLo kong.deb https://bintray.com/kong/kong-deb/download_file?file_path=kong-${KONG_VERSION}.xenial.$(dpkg --print-architecture).deb     && apt-get purge -y --auto-remove ca-certificates curl 	&& dpkg -i kong.deb 	&& rm -rf kong.deb
# Wed, 05 Feb 2020 23:32:34 GMT
COPY file:a4763218d814cc99d340cb11497461af1e7b06c7ec7d19308fb1d59952ad34a4 in /docker-entrypoint.sh 
# Wed, 05 Feb 2020 23:32:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Feb 2020 23:32:34 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Feb 2020 23:32:34 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Feb 2020 23:32:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0a01a72a686c389637334de1e2d0012da298960366f6d8f358b8e10dc3b5e330`  
		Last Modified: Wed, 15 Jan 2020 14:20:15 GMT  
		Size: 44.1 MB (44149770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc899a5544da1a6cfb970d2484d32c063f8df26a430d92f39c98e72261e226f2`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 525.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19197c55075519928dd2ff059745665a2c9b72f4e8af6f7a1ce662e696d339bd`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716d454e56b61d1343a01f3b1829574333e2e3df20e77d1958d7b0b939ea1b61`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1147254588f53c4bbcb8460a8726e11dd5e78cefffee794650888d638749ef`  
		Last Modified: Wed, 05 Feb 2020 23:34:53 GMT  
		Size: 40.6 MB (40563989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27361b46944fe98dcaab7acabdbc3917f4bde6da7c591ee09d60df66b94844a4`  
		Last Modified: Wed, 05 Feb 2020 23:34:43 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:926b2afc390288bcebd6d71c32d211db1d2da059e38d6c434f70c16ef122a1d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79123998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0421830a7e7a199a795a1039d7ac99eca260e829c976c065eebc5d6e44cb19ed`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 16 Jan 2020 00:42:43 GMT
ADD file:d374c720bcf7aac426612a43ac539c3bb5b831a9a9e476a3919ed185eb77deca in / 
# Thu, 16 Jan 2020 00:42:53 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 00:42:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 00:43:02 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 00:43:03 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 01:26:42 GMT
LABEL maintainer=Kong Core Team <team-core@konghq.com>
# Thu, 06 Feb 2020 00:19:15 GMT
ENV KONG_VERSION=2.0.1
# Thu, 06 Feb 2020 00:19:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates curl perl unzip     && rm -rf /var/lib/apt/lists/*     && curl -fsSLo kong.deb https://bintray.com/kong/kong-deb/download_file?file_path=kong-${KONG_VERSION}.xenial.$(dpkg --print-architecture).deb     && apt-get purge -y --auto-remove ca-certificates curl 	&& dpkg -i kong.deb 	&& rm -rf kong.deb
# Thu, 06 Feb 2020 00:19:55 GMT
COPY file:a4763218d814cc99d340cb11497461af1e7b06c7ec7d19308fb1d59952ad34a4 in /docker-entrypoint.sh 
# Thu, 06 Feb 2020 00:19:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Feb 2020 00:19:56 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 06 Feb 2020 00:19:57 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Feb 2020 00:19:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:185661474c6b71ced0eb4cd45f81a17a651d404bfd04903ba0bf3eb815e2cc1d`  
		Last Modified: Thu, 16 Jan 2020 00:44:31 GMT  
		Size: 39.9 MB (39890711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053aaa7a7ba304aae4e3327a0d30a33f5c3fe9fca6e8ef86dd8226b13c29e28d`  
		Last Modified: Thu, 16 Jan 2020 00:44:20 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ccb1337bb94e5b9ea19de7478366666cde129fb3214d092d15ebcfb644d8bb`  
		Last Modified: Thu, 16 Jan 2020 00:44:20 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d1fb143b02bcaaba5f01be18d73c8072c3687fe6e24464871a825e90416f60`  
		Last Modified: Thu, 16 Jan 2020 00:44:20 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8263f1b4550e0ffe0a39226d7739be23db1db41a017799062818c4f78c8eaa08`  
		Last Modified: Thu, 06 Feb 2020 00:21:51 GMT  
		Size: 39.2 MB (39231489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d754d96ff8025da90db88a75fa623e93aceff18b5aba854695e00d0b07c3dab8`  
		Last Modified: Thu, 06 Feb 2020 00:21:36 GMT  
		Size: 311.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
