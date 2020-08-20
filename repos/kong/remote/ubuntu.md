## `kong:ubuntu`

```console
$ docker pull kong@sha256:5afe419e4079e220bf7e21672960cd54cf9e5291363ab410609f134679ab5166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:eda4ea20ff5b5e5484be9bea18a17c1700c29b0701edd5abd46e7b0c1c736c32
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104238604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2368c102a732bbdce99b3c11a45c461981d3563eea57f260e08bff663d8d03a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 19 Aug 2020 21:16:18 GMT
ADD file:144835a276ed2d8eaf6e893d5560444fe0d6a6f9b9bdadec1eb56e7bd9814427 in / 
# Wed, 19 Aug 2020 21:16:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 21:16:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:16:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:16:22 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 23:17:58 GMT
ARG ASSET=ce
# Wed, 19 Aug 2020 23:17:58 GMT
ENV ASSET=ce
# Wed, 19 Aug 2020 23:17:58 GMT
ARG EE_PORTS
# Wed, 19 Aug 2020 23:17:59 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 19 Aug 2020 23:17:59 GMT
ARG KONG_VERSION=2.1.2
# Wed, 19 Aug 2020 23:17:59 GMT
ENV KONG_VERSION=2.1.2
# Wed, 19 Aug 2020 23:18:58 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git     && { apt-get install -y --no-install-recommends zlibc || true; }     && { apt-get install -y --no-install-recommends zlib1g-dev || true; }     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 19 Aug 2020 23:18:58 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 19 Aug 2020 23:18:58 GMT
USER kong
# Wed, 19 Aug 2020 23:18:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 Aug 2020 23:18:59 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 19 Aug 2020 23:18:59 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 Aug 2020 23:18:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8e097b52bfb8e743e52ccd2dfbd5a0363e48a00b06cdd3728a6fd4d1f3a34280`  
		Last Modified: Sat, 08 Aug 2020 13:20:06 GMT  
		Size: 44.4 MB (44447543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a613a9b4553ca86fac22546f2f79e2ff3d17d8d6aeea8b97d67862a5a40ad8ec`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc000f015361df35e770a910ce03d30691e35aa10d52f4a4f432f183a6c03db`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73eef93b7466c41f22f32d28aae5eb87e1ebc0c4d232c5f5e68c955d0e798dca`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d9e2e687753968754b433529f6c4aa4e47c99d475b990fac64438b40a5471b`  
		Last Modified: Wed, 19 Aug 2020 23:19:58 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15492c95039abdcd8fbab62d272bb8a2a8b1aa1b5a3008197a94f7ac311e634b`  
		Last Modified: Wed, 19 Aug 2020 23:20:09 GMT  
		Size: 59.8 MB (59788696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef77665f5d49107c82a4ac40811e9c796c0c620c796207cb8379c1c2de8584d2`  
		Last Modified: Wed, 19 Aug 2020 23:19:58 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:6ad55988e8b5f5a744c95ba1531a2f38e1c1978342b2b702419a240d1573a501
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96235375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a128ae77cc17d0e26571085ca1d84510eb43b5728d54a5a9c06ab041458b5e7e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 19 Aug 2020 21:31:42 GMT
ADD file:20ffb81d6b7edd3826c028369ed1774914394328d1ccef79ecee109f5cfbcc5f in / 
# Wed, 19 Aug 2020 21:31:45 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 21:31:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:31:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:31:52 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:17:19 GMT
ARG ASSET=ce
# Wed, 19 Aug 2020 22:17:19 GMT
ENV ASSET=ce
# Wed, 19 Aug 2020 22:17:20 GMT
ARG EE_PORTS
# Wed, 19 Aug 2020 22:17:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 19 Aug 2020 22:17:21 GMT
ARG KONG_VERSION=2.1.2
# Wed, 19 Aug 2020 22:17:22 GMT
ENV KONG_VERSION=2.1.2
# Wed, 19 Aug 2020 22:18:19 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git     && { apt-get install -y --no-install-recommends zlibc || true; }     && { apt-get install -y --no-install-recommends zlib1g-dev || true; }     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 19 Aug 2020 22:18:21 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 19 Aug 2020 22:18:22 GMT
USER kong
# Wed, 19 Aug 2020 22:18:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 Aug 2020 22:18:23 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 19 Aug 2020 22:18:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 Aug 2020 22:18:24 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3266c9b0302777bdc8ccdffab895ef058fb0777dc7600b0fe0b6c80dd3e71f9b`  
		Last Modified: Sat, 08 Aug 2020 00:25:28 GMT  
		Size: 40.1 MB (40073893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5240d1a89e17ed7dda51e3b38d3749e4ab3fb2fc2433de69ea23a838bb00c7`  
		Last Modified: Wed, 19 Aug 2020 21:33:04 GMT  
		Size: 469.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be065fa7bcd4d9f2540e1fec00c455a04755974444b17fb108b73cd4b15963a1`  
		Last Modified: Wed, 19 Aug 2020 21:33:04 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75305dc60d93c15276fd1b3dc21a09ef1ce9c248393c85eb1a5caf2be6e02671`  
		Last Modified: Wed, 19 Aug 2020 21:33:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45ba64437d430dfa5c413933a6334001af251dcf5e59d73ed032c39ba207c70`  
		Last Modified: Wed, 19 Aug 2020 22:19:41 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d1a341d3d3491c229b7166c33a07bc04ec9fa17f04a109373633d1f9c3565b`  
		Last Modified: Wed, 19 Aug 2020 22:19:59 GMT  
		Size: 56.2 MB (56159175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8cb576dfe603f00117ccf480ba8f013d52b7a1ee28c0f7bfdbb03d024b2024`  
		Last Modified: Wed, 19 Aug 2020 22:19:41 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
