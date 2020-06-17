## `kong:ubuntu`

```console
$ docker pull kong@sha256:6222f8cb4f3dec2ad85cf009b6b730a7f9fd709cd767d103996b02d8a9c9f67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:6e7fc280432b51237a21c97dd07c51109d33ee3bbfbd1853d6311118ee05503d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94258837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b976ee092dd39308988372a5f626dc0e1cbac717718540d7ec5de2e140ce543`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Jun 2020 01:21:26 GMT
ADD file:52af30f80ba214985a59cb0ef7073c64f8514d58396c0de48f8d7056dec2a58a in / 
# Wed, 17 Jun 2020 01:21:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:21:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:21:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:41:23 GMT
ARG ASSET=ce
# Wed, 17 Jun 2020 03:41:23 GMT
ENV ASSET=ce
# Wed, 17 Jun 2020 03:41:23 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Wed, 17 Jun 2020 03:41:23 GMT
ARG KONG_VERSION=2.0.4
# Wed, 17 Jun 2020 03:41:23 GMT
ENV KONG_VERSION=2.0.4
# Wed, 17 Jun 2020 03:41:56 GMT
RUN set -ex;     if [ "$ASSET" = "local" ] ; then exit 0 ;     elif [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb &&         apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong
# Wed, 17 Jun 2020 03:41:57 GMT
COPY file:7cd3b30326ffeaddc1253699208f97fb54711d4ae930aeeeff1e19ebf51cb561 in /docker-entrypoint.sh 
# Wed, 17 Jun 2020 03:41:57 GMT
USER kong
# Wed, 17 Jun 2020 03:41:58 GMT
RUN kong version
# Wed, 17 Jun 2020 03:41:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:41:58 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 17 Jun 2020 03:41:58 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2020 03:41:58 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b5e173e44934e01d8d2674bc8b1da00f761c4fe796e0fb2bee1bd1129d2e4ae1`  
		Last Modified: Fri, 15 May 2020 13:20:22 GMT  
		Size: 44.3 MB (44320272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29047100b0407dff554ea80b8005380d62b13a66d7fe2e2adb07b9c091b9f2c0`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 531.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15743a713c2a4033877dab08fb3989280f8c856234227158a4011811c7991372`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bc9e2987763aa991b7dfd742be04c7b3bb04448982ffe88e58d55c93b76d4`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4343b29744d103aba382b3e0d1bb877f9ecd481767e889ab6c86d1875c6bad99`  
		Last Modified: Wed, 17 Jun 2020 03:44:14 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c77d810dd3c12a2c32a82bc3979848e8ffe74d88da00a775d5973e2e2303d18`  
		Last Modified: Wed, 17 Jun 2020 03:44:24 GMT  
		Size: 49.9 MB (49936157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c17c931a333f8e16904735f731b63e0b725c77ac98f4cb169e71a903211d53`  
		Last Modified: Wed, 17 Jun 2020 03:44:14 GMT  
		Size: 630.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad02e74085ded36213dfb17ff4f178ddef933eaed8d1cdda2638546c6946a638`  
		Last Modified: Wed, 17 Jun 2020 03:44:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:bfe55a1154736a2511706bf70738456beb92347076e4d77da757dea9dcc95b13
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87924719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd516ef147e5aaaf5b7bec7f6936d10ee29cbba55ed74531d95eeffbc2b11297`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Jun 2020 01:44:20 GMT
ADD file:e359a3b06531f763adba716802e252fa49b2e6126f0d3dae1451fc94f5617a13 in / 
# Wed, 17 Jun 2020 01:44:24 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:44:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:44:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:44:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:45:16 GMT
ARG ASSET=ce
# Wed, 17 Jun 2020 02:45:17 GMT
ENV ASSET=ce
# Wed, 17 Jun 2020 02:45:18 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Wed, 17 Jun 2020 02:45:19 GMT
ARG KONG_VERSION=2.0.4
# Wed, 17 Jun 2020 02:45:20 GMT
ENV KONG_VERSION=2.0.4
# Wed, 17 Jun 2020 02:46:17 GMT
RUN set -ex;     if [ "$ASSET" = "local" ] ; then exit 0 ;     elif [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb &&         apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong
# Wed, 17 Jun 2020 02:46:19 GMT
COPY file:7cd3b30326ffeaddc1253699208f97fb54711d4ae930aeeeff1e19ebf51cb561 in /docker-entrypoint.sh 
# Wed, 17 Jun 2020 02:46:20 GMT
USER kong
# Wed, 17 Jun 2020 02:46:23 GMT
RUN kong version
# Wed, 17 Jun 2020 02:46:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2020 02:46:26 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 17 Jun 2020 02:46:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2020 02:46:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:13340090a20bfb81868e7119dc439546fe30dcfccce42509f0fb4d998a1d1fee`  
		Last Modified: Fri, 15 May 2020 16:25:35 GMT  
		Size: 40.0 MB (40003935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75eea8c54eb3d5e45521f4ba5c57ede8436f58690cb8a37da90cfcda5efc25f7`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857f69e728f2821d6dce88bd1c73ebda9481628a80b563e677ec423b08fdba87`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b20459bfc0dfbc19d643cff0a457a117336e167bb8051554fb88aee48feff`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbc29ff205b221c87f413da3a2f3e77b0a8bd55423a1c457fa93d22615eaed3`  
		Last Modified: Wed, 17 Jun 2020 02:50:30 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0275674bb4421e953a1033181662ff0f986471cb8558a0a315ef33de0279d5f`  
		Last Modified: Wed, 17 Jun 2020 02:50:46 GMT  
		Size: 47.9 MB (47918437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81881d2e67473789d504c5467b5f509af8732e4972e825165e6735f065ca001d`  
		Last Modified: Wed, 17 Jun 2020 02:50:30 GMT  
		Size: 630.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99478ac15ba0dbc59c297073e133ea73e0459eb3b290ccaab1d5b0c61fa4bf7b`  
		Last Modified: Wed, 17 Jun 2020 02:50:31 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
