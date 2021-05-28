## `kong:ubuntu`

```console
$ docker pull kong@sha256:14542b141a705483dddcc6f0eb9449bdbe1cc2714e2bb1d66dd8e6fdd77e9965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:21ca915f309f364e5ff5e1f9d2edaeff9eb19c5768b3ffbab2cc3311300bbe4c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139618284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3850c98bbfb5eb79f99f0c303aa16b44f4ebb4452a574c7b5c74ad010ca81b90`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 19 May 2021 19:45:15 GMT
ADD file:5dd161b04353d3cbc2b258d66ef3c79a8307faa944953a1c7920a3d97468520c in / 
# Wed, 19 May 2021 19:45:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:45:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 19:45:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:45:19 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 21:10:22 GMT
ARG ASSET=ce
# Wed, 19 May 2021 21:10:22 GMT
ENV ASSET=ce
# Wed, 19 May 2021 21:10:23 GMT
ARG EE_PORTS
# Wed, 19 May 2021 21:10:23 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 19 May 2021 21:10:23 GMT
ARG KONG_VERSION=2.4.1
# Wed, 19 May 2021 21:10:23 GMT
ENV KONG_VERSION=2.4.1
# Wed, 19 May 2021 21:10:52 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL 		https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-xenial/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 19 May 2021 21:10:53 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 19 May 2021 21:10:53 GMT
USER kong
# Wed, 19 May 2021 21:10:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 May 2021 21:10:54 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 19 May 2021 21:10:54 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 May 2021 21:10:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:80bce60046fa9e5ccbe54c9bd4bfa3f379ce7bc43bed493ae92389050de04024`  
		Last Modified: Thu, 29 Apr 2021 15:24:23 GMT  
		Size: 46.5 MB (46461779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a738a1554069bc9050c0a60b57fc93e98069e59822677a483cc74cafaf2bf7`  
		Last Modified: Wed, 19 May 2021 19:46:37 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19cf0706c6229033d11dbf952b3eb96ad70e1f32527960aeb3c83ad86f16551`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4cdd6c27d1f17cf5ff350e76b7efe80aceff4dc99fd518065bf048abd6494a`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d3c8daaad6d13ef4bf576ce9208152535e4bb46b3a9e3f074d4fd696a164e4`  
		Last Modified: Wed, 19 May 2021 21:14:26 GMT  
		Size: 25.1 MB (25081966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f9067a64751b93c660c5e8b46a054d9810743dbf9c38e7c62c0dbc5c2ee8e4`  
		Last Modified: Wed, 19 May 2021 21:14:36 GMT  
		Size: 68.1 MB (68072303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cae426332dcd3ec9ca6bd61a512c2157cb51dbe4fbb5eeb8ae451c05b0d6e0`  
		Last Modified: Wed, 19 May 2021 21:14:24 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1e44056c06a3f50632c15adf1078bb005ecd3f3c20b8245d0fa239b90c2e178f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129962210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77b237004f52ceb2de7c6167ed40055d47925da2d73ec5f618ed97e7cd9872b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 27 May 2021 12:30:43 GMT
ADD file:9417aaf175748bf02265b3fcffc4955c5521d4d51793d599f33e48b7960e453e in / 
# Thu, 27 May 2021 12:30:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:30:45 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 12:30:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:30:46 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:40:06 GMT
ARG ASSET=ce
# Thu, 27 May 2021 20:40:06 GMT
ENV ASSET=ce
# Thu, 27 May 2021 20:40:07 GMT
ARG EE_PORTS
# Thu, 27 May 2021 20:40:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 27 May 2021 20:40:07 GMT
ARG KONG_VERSION=2.4.1
# Thu, 27 May 2021 20:40:07 GMT
ENV KONG_VERSION=2.4.1
# Thu, 27 May 2021 20:40:33 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL 		https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-xenial/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Thu, 27 May 2021 20:40:34 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 27 May 2021 20:40:34 GMT
USER kong
# Thu, 27 May 2021 20:40:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 May 2021 20:40:34 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 27 May 2021 20:40:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 27 May 2021 20:40:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:58be9ce6be6955598846443a55535df82ab8b8489d8a09eb959abd45a368503b`  
		Last Modified: Thu, 29 Apr 2021 08:25:11 GMT  
		Size: 41.2 MB (41212503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2536079c067c30e81c2fd80224355786c22f125638814e45caa9357de3b332b`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1407aa15569186ac220ed788ef58c2821961717f50af3355e9302617acddbfb`  
		Last Modified: Thu, 27 May 2021 12:33:42 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566efc3b50d0a162192bf9a472fe8ff4e3d7be9791f42b800f9475188301ecac`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daaa1e99fdca50cd282dfb8cc289f5d81eb903a74599492defe4181c10b311a`  
		Last Modified: Thu, 27 May 2021 20:45:28 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e06679b2ae9cf23f51b8ceea4d7b2beb045963a724289ca2c70b548840c6972`  
		Last Modified: Thu, 27 May 2021 20:45:38 GMT  
		Size: 63.7 MB (63665573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afeeb9eb72768ba059fc31ec6033f2ade98ed22597d4e28bb70230d835041e20`  
		Last Modified: Thu, 27 May 2021 20:45:26 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
