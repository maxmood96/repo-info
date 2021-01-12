## `crate:latest`

```console
$ docker pull crate@sha256:868110399322d9533a356b8ed00cad8e38bb0df415f1b6b314838a4f9c436970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:e4e48cf462799666325b9a218cf1d2b22536249f73d9c899e60c8d6d04910ffe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.3 MB (331318122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe24633f6198d7d052e8f682e97beab5b85d1a60a4b58a6162df27579ae9921a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 14 Nov 2020 00:37:20 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Tue, 01 Dec 2020 23:38:47 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.3.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.3.2.tar.gz.asc crate-4.3.2.tar.gz     && rm -rf "$GNUPGHOME" crate-4.3.2.tar.gz.asc     && tar -xf crate-4.3.2.tar.gz -C /crate --strip-components=1     && rm crate-4.3.2.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Tue, 01 Dec 2020 23:38:50 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.26.0.asc crash_standalone_0.26.0     && rm -rf "$GNUPGHOME" crash_standalone_0.26.0.asc     && mv crash_standalone_0.26.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 01 Dec 2020 23:38:50 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Dec 2020 23:38:50 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 01 Dec 2020 23:38:51 GMT
RUN mkdir -p /data/data /data/log
# Tue, 01 Dec 2020 23:38:52 GMT
VOLUME [/data]
# Tue, 01 Dec 2020 23:38:52 GMT
WORKDIR /data
# Tue, 01 Dec 2020 23:38:52 GMT
EXPOSE 4200 4300 5432
# Tue, 01 Dec 2020 23:38:52 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 01 Dec 2020 23:38:53 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 01 Dec 2020 23:38:53 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-11-25T09:57:46.817607 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.3.2
# Tue, 01 Dec 2020 23:38:53 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 01 Dec 2020 23:38:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 01 Dec 2020 23:38:53 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51009734a299823465796326f91dc7b8be4a36f8102074b7d5682f4b160eef3d`  
		Last Modified: Sat, 14 Nov 2020 00:42:26 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766e8cfef878e317086938b66002779cd5748fccd3ec487db257fadf7a4c9349`  
		Last Modified: Tue, 01 Dec 2020 23:40:00 GMT  
		Size: 253.6 MB (253649071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be807bdf6bce92295f4d03818e54041ad5541b12023f28603351dcb0368fb44b`  
		Last Modified: Tue, 01 Dec 2020 23:39:33 GMT  
		Size: 1.6 MB (1567816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8c9cd6136e9257e718049f3d611f4f85b5cb62c4b33ef7881a816e5f0ff033`  
		Last Modified: Tue, 01 Dec 2020 23:39:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25428cb8fbb2e11cc4c5c61874e1d9be607e60d96ef40f51a169740db3d75eec`  
		Last Modified: Tue, 01 Dec 2020 23:39:33 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791f39137f502ec20734d23b400a27c47961359175d5ebf85d1972df59910941`  
		Last Modified: Tue, 01 Dec 2020 23:39:33 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2cddcf40dc480481a5e6e011c57ff531884c93906ba62b3458531640b875d0`  
		Last Modified: Tue, 01 Dec 2020 23:39:33 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:8223e2f6a253394aade82f137d4a4ee75850b3a10ac07f2f77d884818a6bc2aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.7 MB (361704668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f19b6ce48819d324fc8f34e1c3e5bf4ff0b859a9ca80fd7714b79072f469471`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Sat, 14 Nov 2020 00:40:26 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Sat, 14 Nov 2020 00:40:31 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:40:32 GMT
CMD ["/bin/bash"]
# Sat, 14 Nov 2020 00:57:11 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Mon, 11 Jan 2021 23:41:07 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.3.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.3.3.tar.gz.asc crate-4.3.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.3.3.tar.gz.asc     && tar -xf crate-4.3.3.tar.gz -C /crate --strip-components=1     && rm crate-4.3.3.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Mon, 11 Jan 2021 23:41:15 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.26.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.26.0.asc crash_standalone_0.26.0     && rm -rf "$GNUPGHOME" crash_standalone_0.26.0.asc     && mv crash_standalone_0.26.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 11 Jan 2021 23:41:16 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Jan 2021 23:41:17 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 11 Jan 2021 23:41:18 GMT
RUN mkdir -p /data/data /data/log
# Mon, 11 Jan 2021 23:41:19 GMT
VOLUME [/data]
# Mon, 11 Jan 2021 23:41:20 GMT
WORKDIR /data
# Mon, 11 Jan 2021 23:41:20 GMT
EXPOSE 4200 4300 5432
# Mon, 11 Jan 2021 23:41:21 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 11 Jan 2021 23:41:22 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 11 Jan 2021 23:41:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-01-06T13:49:59.918942 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.3.3
# Mon, 11 Jan 2021 23:41:23 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 11 Jan 2021 23:41:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 Jan 2021 23:41:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6312a055314d3cb5a347fd7eb62a5fb7ad8e03a999e1c964f320a28325cf017d`  
		Last Modified: Sat, 14 Nov 2020 01:06:26 GMT  
		Size: 2.3 KB (2254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6462066fbb7066c2d1d471f5f80480f5ab255c808156e607bba5ccdbb5645af9`  
		Last Modified: Mon, 11 Jan 2021 23:43:02 GMT  
		Size: 251.8 MB (251757765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b79aec7edb98837e07ce03e121c1e53fa2d7bd461ce193b97e53d9c9c25fef2`  
		Last Modified: Mon, 11 Jan 2021 23:42:22 GMT  
		Size: 1.6 MB (1567819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e6c15b4f707e090888017515775218b8607eb833fb5f8f69fd0aad6b85b1a1`  
		Last Modified: Mon, 11 Jan 2021 23:42:22 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0ec98997042e5a3a67e8be78395c2f4242a336757ec73072aee56374d9f30a`  
		Last Modified: Mon, 11 Jan 2021 23:42:23 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9060a930557208ce82b3093c151b1f99aac6babbb92ddc3a865600d7312173e0`  
		Last Modified: Mon, 11 Jan 2021 23:42:23 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cf77334e8035e468e8ef580cb7d57f9c9839781b851bd24558c207a1b6c26b`  
		Last Modified: Mon, 11 Jan 2021 23:42:24 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
