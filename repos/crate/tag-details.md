<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:4.8`](#crate48)
-	[`crate:4.8.4`](#crate484)
-	[`crate:5.2`](#crate52)
-	[`crate:5.2.10`](#crate5210)
-	[`crate:5.3`](#crate53)
-	[`crate:5.3.7`](#crate537)
-	[`crate:5.4`](#crate54)
-	[`crate:5.4.5`](#crate545)
-	[`crate:5.5`](#crate55)
-	[`crate:5.5.0`](#crate550)
-	[`crate:latest`](#cratelatest)

## `crate:4.8`

```console
$ docker pull crate@sha256:fcfb1e26e4b6b84cf23bbb0de51a9671655d1e843b01cffea5984643727e021e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.8` - linux; amd64

```console
$ docker pull crate@sha256:ab33e064e23959eed997f0e9317a8ccb942974f7d3159ac464a5a3cb221e25c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.6 MB (366609762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849c866b7319b231f9f5482aef88650ec60dd6d7059a29de576cbd4b789bd3d1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Mon, 12 Sep 2022 19:20:47 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum upgrade -y     && yum install -y python3 openssl     && pip3 install --upgrade pip     && yum clean all     && rm -rf /var/cache/yum
# Tue, 20 Sep 2022 20:24:28 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.8.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.8.4.tar.gz.asc crate-4.8.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.8.4.tar.gz.asc     && tar -xf crate-4.8.4.tar.gz -C /crate --strip-components=1     && rm crate-4.8.4.tar.gz
# Tue, 20 Sep 2022 20:24:32 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 20 Sep 2022 20:24:32 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Sep 2022 20:24:32 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 20 Sep 2022 20:24:33 GMT
RUN mkdir -p /data/data /data/log
# Tue, 20 Sep 2022 20:24:33 GMT
VOLUME [/data]
# Tue, 20 Sep 2022 20:24:33 GMT
WORKDIR /data
# Tue, 20 Sep 2022 20:24:33 GMT
EXPOSE 4200 4300 5432
# Tue, 20 Sep 2022 20:24:33 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 20 Sep 2022 20:24:33 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 20 Sep 2022 20:24:33 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-09-15T10:52:50.199012 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.8.4
# Tue, 20 Sep 2022 20:24:33 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 20 Sep 2022 20:24:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 20 Sep 2022 20:24:34 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816162095613648af0045121a146a6ab058718d006d17f2ea25e169f0961b298`  
		Last Modified: Mon, 12 Sep 2022 19:22:25 GMT  
		Size: 77.1 MB (77149352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3bdb3f3876f51c5600bc5d5576e6c84959f5433fb375eb3a1b2798d93abc31`  
		Last Modified: Tue, 20 Sep 2022 20:25:15 GMT  
		Size: 211.7 MB (211650590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136d385fe2b73321323b7b11085d41441495146f7a18dbf421502225a9ff8656`  
		Last Modified: Tue, 20 Sep 2022 20:24:54 GMT  
		Size: 1.7 MB (1710779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c312f86d93dded0d735bc9b7234f64c5a8ff5bc82ffe1ce9ad869ed3a7b68c68`  
		Last Modified: Tue, 20 Sep 2022 20:24:53 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eeaec4222433c7af8e5220f511915ab8fb4049a7136fc371b5d2679811e34c4`  
		Last Modified: Tue, 20 Sep 2022 20:24:53 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed829b350fc610813c498009ca8aecf3b3e6184dfe54943a7d490e583e207f4`  
		Last Modified: Tue, 20 Sep 2022 20:24:53 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2994a6708f131a2fa358dbb8885094c2d552f7880f924a3b84048082560032f3`  
		Last Modified: Tue, 20 Sep 2022 20:24:53 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:54bb068652a7f229af18cc10ae7e5d94d19cbbf4952635694dc2e34df3502b56
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.5 MB (666503011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac29f1818d2fdc8991ad2484f8adac7e43311743dae8b71f35d1eda47c45be02`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Mon, 24 Oct 2022 21:41:05 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum upgrade -y     && yum install -y python3 openssl     && pip3 install --upgrade pip     && yum clean all     && rm -rf /var/cache/yum
# Mon, 24 Oct 2022 21:42:19 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.8.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.8.4.tar.gz.asc crate-4.8.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.8.4.tar.gz.asc     && tar -xf crate-4.8.4.tar.gz -C /crate --strip-components=1     && rm crate-4.8.4.tar.gz
# Mon, 24 Oct 2022 21:42:23 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 24 Oct 2022 21:42:23 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Oct 2022 21:42:23 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Oct 2022 21:42:24 GMT
RUN mkdir -p /data/data /data/log
# Mon, 24 Oct 2022 21:42:24 GMT
VOLUME [/data]
# Mon, 24 Oct 2022 21:42:24 GMT
WORKDIR /data
# Mon, 24 Oct 2022 21:42:24 GMT
EXPOSE 4200 4300 5432
# Mon, 24 Oct 2022 21:42:24 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 24 Oct 2022 21:42:24 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 24 Oct 2022 21:42:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-09-15T10:52:50.199012 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.8.4
# Mon, 24 Oct 2022 21:42:24 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 24 Oct 2022 21:42:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Oct 2022 21:42:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bd2dd4fe2ac3696c00e2e33054e11971bf81acb6591869e1d525feb18cceb3`  
		Last Modified: Mon, 24 Oct 2022 21:45:28 GMT  
		Size: 346.0 MB (345996846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5e7c58b367faadd294e7b188398fc564edf19271fac04a26b51637c28e43e6`  
		Last Modified: Mon, 24 Oct 2022 21:45:57 GMT  
		Size: 210.4 MB (210418568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b966a9d970d836ffb3ccc8dcca4ffd79e2f6334cb230e0617b25457394750b`  
		Last Modified: Mon, 24 Oct 2022 21:45:42 GMT  
		Size: 1.7 MB (1710769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286650217f63a621366b0d7e1115fa37df60654f36c5b556c3b2a5cf41e7f6cd`  
		Last Modified: Mon, 24 Oct 2022 21:45:41 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d1e66c86b54db4e4dc22fce8f33097dcad2745154e050210dacb713db2c232`  
		Last Modified: Mon, 24 Oct 2022 21:45:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a335f20bda4ea63d2b38a9c41ea60713b51e8b3816061c4067b7f69604ecf5f`  
		Last Modified: Mon, 24 Oct 2022 21:45:41 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293324d5cf1d0be9fc09670f9ab9249b7775dfb2a0c350042d4909228b55011f`  
		Last Modified: Mon, 24 Oct 2022 21:45:41 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.8.4`

```console
$ docker pull crate@sha256:fcfb1e26e4b6b84cf23bbb0de51a9671655d1e843b01cffea5984643727e021e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.8.4` - linux; amd64

```console
$ docker pull crate@sha256:ab33e064e23959eed997f0e9317a8ccb942974f7d3159ac464a5a3cb221e25c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.6 MB (366609762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849c866b7319b231f9f5482aef88650ec60dd6d7059a29de576cbd4b789bd3d1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Mon, 12 Sep 2022 19:20:47 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum upgrade -y     && yum install -y python3 openssl     && pip3 install --upgrade pip     && yum clean all     && rm -rf /var/cache/yum
# Tue, 20 Sep 2022 20:24:28 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.8.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.8.4.tar.gz.asc crate-4.8.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.8.4.tar.gz.asc     && tar -xf crate-4.8.4.tar.gz -C /crate --strip-components=1     && rm crate-4.8.4.tar.gz
# Tue, 20 Sep 2022 20:24:32 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 20 Sep 2022 20:24:32 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Sep 2022 20:24:32 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 20 Sep 2022 20:24:33 GMT
RUN mkdir -p /data/data /data/log
# Tue, 20 Sep 2022 20:24:33 GMT
VOLUME [/data]
# Tue, 20 Sep 2022 20:24:33 GMT
WORKDIR /data
# Tue, 20 Sep 2022 20:24:33 GMT
EXPOSE 4200 4300 5432
# Tue, 20 Sep 2022 20:24:33 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 20 Sep 2022 20:24:33 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 20 Sep 2022 20:24:33 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-09-15T10:52:50.199012 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.8.4
# Tue, 20 Sep 2022 20:24:33 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 20 Sep 2022 20:24:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 20 Sep 2022 20:24:34 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816162095613648af0045121a146a6ab058718d006d17f2ea25e169f0961b298`  
		Last Modified: Mon, 12 Sep 2022 19:22:25 GMT  
		Size: 77.1 MB (77149352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3bdb3f3876f51c5600bc5d5576e6c84959f5433fb375eb3a1b2798d93abc31`  
		Last Modified: Tue, 20 Sep 2022 20:25:15 GMT  
		Size: 211.7 MB (211650590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136d385fe2b73321323b7b11085d41441495146f7a18dbf421502225a9ff8656`  
		Last Modified: Tue, 20 Sep 2022 20:24:54 GMT  
		Size: 1.7 MB (1710779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c312f86d93dded0d735bc9b7234f64c5a8ff5bc82ffe1ce9ad869ed3a7b68c68`  
		Last Modified: Tue, 20 Sep 2022 20:24:53 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eeaec4222433c7af8e5220f511915ab8fb4049a7136fc371b5d2679811e34c4`  
		Last Modified: Tue, 20 Sep 2022 20:24:53 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed829b350fc610813c498009ca8aecf3b3e6184dfe54943a7d490e583e207f4`  
		Last Modified: Tue, 20 Sep 2022 20:24:53 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2994a6708f131a2fa358dbb8885094c2d552f7880f924a3b84048082560032f3`  
		Last Modified: Tue, 20 Sep 2022 20:24:53 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.8.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:54bb068652a7f229af18cc10ae7e5d94d19cbbf4952635694dc2e34df3502b56
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.5 MB (666503011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac29f1818d2fdc8991ad2484f8adac7e43311743dae8b71f35d1eda47c45be02`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Mon, 24 Oct 2022 21:41:05 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum upgrade -y     && yum install -y python3 openssl     && pip3 install --upgrade pip     && yum clean all     && rm -rf /var/cache/yum
# Mon, 24 Oct 2022 21:42:19 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.8.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.8.4.tar.gz.asc crate-4.8.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.8.4.tar.gz.asc     && tar -xf crate-4.8.4.tar.gz -C /crate --strip-components=1     && rm crate-4.8.4.tar.gz
# Mon, 24 Oct 2022 21:42:23 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 24 Oct 2022 21:42:23 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Oct 2022 21:42:23 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Oct 2022 21:42:24 GMT
RUN mkdir -p /data/data /data/log
# Mon, 24 Oct 2022 21:42:24 GMT
VOLUME [/data]
# Mon, 24 Oct 2022 21:42:24 GMT
WORKDIR /data
# Mon, 24 Oct 2022 21:42:24 GMT
EXPOSE 4200 4300 5432
# Mon, 24 Oct 2022 21:42:24 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 24 Oct 2022 21:42:24 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 24 Oct 2022 21:42:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-09-15T10:52:50.199012 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.8.4
# Mon, 24 Oct 2022 21:42:24 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 24 Oct 2022 21:42:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Oct 2022 21:42:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bd2dd4fe2ac3696c00e2e33054e11971bf81acb6591869e1d525feb18cceb3`  
		Last Modified: Mon, 24 Oct 2022 21:45:28 GMT  
		Size: 346.0 MB (345996846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5e7c58b367faadd294e7b188398fc564edf19271fac04a26b51637c28e43e6`  
		Last Modified: Mon, 24 Oct 2022 21:45:57 GMT  
		Size: 210.4 MB (210418568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b966a9d970d836ffb3ccc8dcca4ffd79e2f6334cb230e0617b25457394750b`  
		Last Modified: Mon, 24 Oct 2022 21:45:42 GMT  
		Size: 1.7 MB (1710769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286650217f63a621366b0d7e1115fa37df60654f36c5b556c3b2a5cf41e7f6cd`  
		Last Modified: Mon, 24 Oct 2022 21:45:41 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d1e66c86b54db4e4dc22fce8f33097dcad2745154e050210dacb713db2c232`  
		Last Modified: Mon, 24 Oct 2022 21:45:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a335f20bda4ea63d2b38a9c41ea60713b51e8b3816061c4067b7f69604ecf5f`  
		Last Modified: Mon, 24 Oct 2022 21:45:41 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293324d5cf1d0be9fc09670f9ab9249b7775dfb2a0c350042d4909228b55011f`  
		Last Modified: Mon, 24 Oct 2022 21:45:41 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.2`

```console
$ docker pull crate@sha256:25e5c1b4a34784f9a904cf1a62507defb7c111551bb9acf7e5042e9ce17079df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.2` - linux; amd64

```console
$ docker pull crate@sha256:d4a7b083294107fd25415afaebfffe001b11edb64ccfbe14ddf7187225b167ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304895926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19163e39620c7d080d4673d2941f43b0373c2e08e757065c8c09232b78ec3ae7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 23 Nov 2023 10:20:12 GMT
ADD file:9774d83eefdb6ff8836449ab084b6760986009214c66efe6487e25ea59e94903 in / 
# Thu, 23 Nov 2023 10:20:13 GMT
CMD ["/bin/bash"]
# Thu, 23 Nov 2023 11:02:20 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python3 python3-pip     && yum clean all     && rm -rf /var/cache/yum
# Thu, 23 Nov 2023 11:02:42 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.2.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.2.10.tar.gz.asc crate-5.2.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.2.10.tar.gz.asc     && tar -xf crate-5.2.10.tar.gz -C /crate --strip-components=1     && rm crate-5.2.10.tar.gz
# Thu, 23 Nov 2023 11:02:44 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 23 Nov 2023 11:02:44 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Nov 2023 11:02:44 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 23 Nov 2023 11:02:44 GMT
RUN mkdir -p /data/data /data/log
# Thu, 23 Nov 2023 11:02:45 GMT
VOLUME [/data]
# Thu, 23 Nov 2023 11:02:45 GMT
WORKDIR /data
# Thu, 23 Nov 2023 11:02:45 GMT
EXPOSE 4200 4300 5432
# Thu, 23 Nov 2023 11:02:45 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 23 Nov 2023 11:02:45 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 23 Nov 2023 11:02:45 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-12T15:07:59.910862 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.2.10
# Thu, 23 Nov 2023 11:02:45 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 23 Nov 2023 11:02:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Nov 2023 11:02:45 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:702739624a8da12ef7ff47788114676caab93f317dd8df05eae8c7f7e4e1dece`  
		Last Modified: Thu, 23 Nov 2023 10:21:27 GMT  
		Size: 68.2 MB (68211768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e0cf4df458cd4c7d8d6101bb566f3a575833be9fc256adfe0145bc0bb171ce`  
		Last Modified: Thu, 23 Nov 2023 11:04:23 GMT  
		Size: 7.6 MB (7631792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89df13535e8bf17bca4c7e8ed428fe77c90abab3671d64bc8b96a7dda68e8e5a`  
		Last Modified: Thu, 23 Nov 2023 11:04:38 GMT  
		Size: 227.1 MB (227118755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c096ceb94c6d9d573ccfc02b99fef1dece227dfd41ff04fa5eb68640c5c8295`  
		Last Modified: Thu, 23 Nov 2023 11:04:20 GMT  
		Size: 1.9 MB (1931729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe9db7548992ef537d0b5deaa0b5aa503c8b4b31589c101a16339dca41f5853`  
		Last Modified: Thu, 23 Nov 2023 11:04:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb29762b3fc508eac41cb600f3341814be307206a189baaac28048c00bff879`  
		Last Modified: Thu, 23 Nov 2023 11:04:20 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78223528d73446a47318f6973fb6b4f1bdc5f6d4fe280964c951b55c394ae219`  
		Last Modified: Thu, 23 Nov 2023 11:04:20 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159c205cae55a5182782d9c3d8414617b9df04deb939c7b5d4e4192fd7372760`  
		Last Modified: Thu, 23 Nov 2023 11:04:20 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:ff7ca05aef022e4ea1a85cab576403c8dc04efbf9ab6de35ba39c9980255ed42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302363612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94386d7fe200c92289b10f74b4ce2f37d1146699578438edaafcd3e61beea5a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 23 Nov 2023 09:40:02 GMT
ADD file:136bb7999312a4aab093582f3b001747f508e05bfaa261c00852d06c44b23a2b in / 
# Thu, 23 Nov 2023 09:40:05 GMT
CMD ["/bin/bash"]
# Thu, 23 Nov 2023 11:07:36 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python3 python3-pip     && yum clean all     && rm -rf /var/cache/yum
# Thu, 23 Nov 2023 11:07:58 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.2.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.2.10.tar.gz.asc crate-5.2.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.2.10.tar.gz.asc     && tar -xf crate-5.2.10.tar.gz -C /crate --strip-components=1     && rm crate-5.2.10.tar.gz
# Thu, 23 Nov 2023 11:08:02 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 23 Nov 2023 11:08:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Nov 2023 11:08:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 23 Nov 2023 11:08:02 GMT
RUN mkdir -p /data/data /data/log
# Thu, 23 Nov 2023 11:08:02 GMT
VOLUME [/data]
# Thu, 23 Nov 2023 11:08:02 GMT
WORKDIR /data
# Thu, 23 Nov 2023 11:08:02 GMT
EXPOSE 4200 4300 5432
# Thu, 23 Nov 2023 11:08:02 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 23 Nov 2023 11:08:03 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 23 Nov 2023 11:08:03 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-12T15:07:59.910862 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.2.10
# Thu, 23 Nov 2023 11:08:03 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 23 Nov 2023 11:08:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Nov 2023 11:08:03 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:414d55c697e2dfc577ea164980a2fcec75b4913627c6a8a06cba30b3255cefee`  
		Last Modified: Thu, 23 Nov 2023 09:41:07 GMT  
		Size: 67.1 MB (67091205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dc52344cd558a72dbd600be50312495ae4b9a6c8b05f52cd779db6a975290e`  
		Last Modified: Thu, 23 Nov 2023 11:09:33 GMT  
		Size: 7.5 MB (7476876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7250e2c537887ddb8c427c658db849dc808c503ff8bc4e5ea32775148078ba2c`  
		Last Modified: Thu, 23 Nov 2023 11:09:45 GMT  
		Size: 225.9 MB (225861926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0792771c7dfdc33ca13ce4e9dce789e708057c9a5ceb31c57fe7a27f3075619`  
		Last Modified: Thu, 23 Nov 2023 11:09:30 GMT  
		Size: 1.9 MB (1931722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d319285ba257392326bd9691e6832eabec946b33fb59e7e9bf3c62e435bb2d8`  
		Last Modified: Thu, 23 Nov 2023 11:09:30 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7340a65c396f693991567ed3d816e9517600fb00eed07acf0409fd67d194881e`  
		Last Modified: Thu, 23 Nov 2023 11:09:30 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bff242adc2d6c6ec753bb2ee3ba97394de368d4ea1461b87d782a6d3aa3bf70`  
		Last Modified: Thu, 23 Nov 2023 11:09:30 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1215d3539709f73bd02850ee6933d801acc3e374fc7d0272108a6fea9613a0e`  
		Last Modified: Thu, 23 Nov 2023 11:09:30 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.2.10`

```console
$ docker pull crate@sha256:25e5c1b4a34784f9a904cf1a62507defb7c111551bb9acf7e5042e9ce17079df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.2.10` - linux; amd64

```console
$ docker pull crate@sha256:d4a7b083294107fd25415afaebfffe001b11edb64ccfbe14ddf7187225b167ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304895926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19163e39620c7d080d4673d2941f43b0373c2e08e757065c8c09232b78ec3ae7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 23 Nov 2023 10:20:12 GMT
ADD file:9774d83eefdb6ff8836449ab084b6760986009214c66efe6487e25ea59e94903 in / 
# Thu, 23 Nov 2023 10:20:13 GMT
CMD ["/bin/bash"]
# Thu, 23 Nov 2023 11:02:20 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python3 python3-pip     && yum clean all     && rm -rf /var/cache/yum
# Thu, 23 Nov 2023 11:02:42 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.2.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.2.10.tar.gz.asc crate-5.2.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.2.10.tar.gz.asc     && tar -xf crate-5.2.10.tar.gz -C /crate --strip-components=1     && rm crate-5.2.10.tar.gz
# Thu, 23 Nov 2023 11:02:44 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 23 Nov 2023 11:02:44 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Nov 2023 11:02:44 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 23 Nov 2023 11:02:44 GMT
RUN mkdir -p /data/data /data/log
# Thu, 23 Nov 2023 11:02:45 GMT
VOLUME [/data]
# Thu, 23 Nov 2023 11:02:45 GMT
WORKDIR /data
# Thu, 23 Nov 2023 11:02:45 GMT
EXPOSE 4200 4300 5432
# Thu, 23 Nov 2023 11:02:45 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 23 Nov 2023 11:02:45 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 23 Nov 2023 11:02:45 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-12T15:07:59.910862 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.2.10
# Thu, 23 Nov 2023 11:02:45 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 23 Nov 2023 11:02:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Nov 2023 11:02:45 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:702739624a8da12ef7ff47788114676caab93f317dd8df05eae8c7f7e4e1dece`  
		Last Modified: Thu, 23 Nov 2023 10:21:27 GMT  
		Size: 68.2 MB (68211768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e0cf4df458cd4c7d8d6101bb566f3a575833be9fc256adfe0145bc0bb171ce`  
		Last Modified: Thu, 23 Nov 2023 11:04:23 GMT  
		Size: 7.6 MB (7631792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89df13535e8bf17bca4c7e8ed428fe77c90abab3671d64bc8b96a7dda68e8e5a`  
		Last Modified: Thu, 23 Nov 2023 11:04:38 GMT  
		Size: 227.1 MB (227118755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c096ceb94c6d9d573ccfc02b99fef1dece227dfd41ff04fa5eb68640c5c8295`  
		Last Modified: Thu, 23 Nov 2023 11:04:20 GMT  
		Size: 1.9 MB (1931729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe9db7548992ef537d0b5deaa0b5aa503c8b4b31589c101a16339dca41f5853`  
		Last Modified: Thu, 23 Nov 2023 11:04:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb29762b3fc508eac41cb600f3341814be307206a189baaac28048c00bff879`  
		Last Modified: Thu, 23 Nov 2023 11:04:20 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78223528d73446a47318f6973fb6b4f1bdc5f6d4fe280964c951b55c394ae219`  
		Last Modified: Thu, 23 Nov 2023 11:04:20 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159c205cae55a5182782d9c3d8414617b9df04deb939c7b5d4e4192fd7372760`  
		Last Modified: Thu, 23 Nov 2023 11:04:20 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.2.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:ff7ca05aef022e4ea1a85cab576403c8dc04efbf9ab6de35ba39c9980255ed42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302363612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94386d7fe200c92289b10f74b4ce2f37d1146699578438edaafcd3e61beea5a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 23 Nov 2023 09:40:02 GMT
ADD file:136bb7999312a4aab093582f3b001747f508e05bfaa261c00852d06c44b23a2b in / 
# Thu, 23 Nov 2023 09:40:05 GMT
CMD ["/bin/bash"]
# Thu, 23 Nov 2023 11:07:36 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python3 python3-pip     && yum clean all     && rm -rf /var/cache/yum
# Thu, 23 Nov 2023 11:07:58 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.2.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.2.10.tar.gz.asc crate-5.2.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.2.10.tar.gz.asc     && tar -xf crate-5.2.10.tar.gz -C /crate --strip-components=1     && rm crate-5.2.10.tar.gz
# Thu, 23 Nov 2023 11:08:02 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 23 Nov 2023 11:08:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Nov 2023 11:08:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 23 Nov 2023 11:08:02 GMT
RUN mkdir -p /data/data /data/log
# Thu, 23 Nov 2023 11:08:02 GMT
VOLUME [/data]
# Thu, 23 Nov 2023 11:08:02 GMT
WORKDIR /data
# Thu, 23 Nov 2023 11:08:02 GMT
EXPOSE 4200 4300 5432
# Thu, 23 Nov 2023 11:08:02 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 23 Nov 2023 11:08:03 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 23 Nov 2023 11:08:03 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-12T15:07:59.910862 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.2.10
# Thu, 23 Nov 2023 11:08:03 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 23 Nov 2023 11:08:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Nov 2023 11:08:03 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:414d55c697e2dfc577ea164980a2fcec75b4913627c6a8a06cba30b3255cefee`  
		Last Modified: Thu, 23 Nov 2023 09:41:07 GMT  
		Size: 67.1 MB (67091205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dc52344cd558a72dbd600be50312495ae4b9a6c8b05f52cd779db6a975290e`  
		Last Modified: Thu, 23 Nov 2023 11:09:33 GMT  
		Size: 7.5 MB (7476876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7250e2c537887ddb8c427c658db849dc808c503ff8bc4e5ea32775148078ba2c`  
		Last Modified: Thu, 23 Nov 2023 11:09:45 GMT  
		Size: 225.9 MB (225861926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0792771c7dfdc33ca13ce4e9dce789e708057c9a5ceb31c57fe7a27f3075619`  
		Last Modified: Thu, 23 Nov 2023 11:09:30 GMT  
		Size: 1.9 MB (1931722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d319285ba257392326bd9691e6832eabec946b33fb59e7e9bf3c62e435bb2d8`  
		Last Modified: Thu, 23 Nov 2023 11:09:30 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7340a65c396f693991567ed3d816e9517600fb00eed07acf0409fd67d194881e`  
		Last Modified: Thu, 23 Nov 2023 11:09:30 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bff242adc2d6c6ec753bb2ee3ba97394de368d4ea1461b87d782a6d3aa3bf70`  
		Last Modified: Thu, 23 Nov 2023 11:09:30 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1215d3539709f73bd02850ee6933d801acc3e374fc7d0272108a6fea9613a0e`  
		Last Modified: Thu, 23 Nov 2023 11:09:30 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.3`

```console
$ docker pull crate@sha256:a68b5a4f282d391583a38c89ab7ad77c09b57f6668ff8e77368b98a906dc2fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.3` - linux; amd64

```console
$ docker pull crate@sha256:10dc22e2ca521b0afa915904fa88970d4354e7c65b7e931ee46250a67147f572
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297906556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918d9d826215e7fb7b328d4603327abb2016ae1cfefda2e79e8fc62746624c7c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 23 Nov 2023 10:20:12 GMT
ADD file:9774d83eefdb6ff8836449ab084b6760986009214c66efe6487e25ea59e94903 in / 
# Thu, 23 Nov 2023 10:20:13 GMT
CMD ["/bin/bash"]
# Thu, 23 Nov 2023 11:00:44 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 23 Nov 2023 11:02:05 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.7.tar.gz.asc crate-5.3.7.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.7.tar.gz.asc     && tar -xf crate-5.3.7.tar.gz -C /crate --strip-components=1     && rm crate-5.3.7.tar.gz
# Thu, 23 Nov 2023 11:02:07 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 23 Nov 2023 11:02:07 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Nov 2023 11:02:07 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 23 Nov 2023 11:02:08 GMT
RUN mkdir -p /data/data /data/log
# Thu, 23 Nov 2023 11:02:08 GMT
VOLUME [/data]
# Thu, 23 Nov 2023 11:02:08 GMT
WORKDIR /data
# Thu, 23 Nov 2023 11:02:08 GMT
EXPOSE 4200 4300 5432
# Thu, 23 Nov 2023 11:02:08 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 23 Nov 2023 11:02:08 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 23 Nov 2023 11:02:08 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-12T16:00:23.375147 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.7
# Thu, 23 Nov 2023 11:02:08 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 23 Nov 2023 11:02:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Nov 2023 11:02:09 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:702739624a8da12ef7ff47788114676caab93f317dd8df05eae8c7f7e4e1dece`  
		Last Modified: Thu, 23 Nov 2023 10:21:27 GMT  
		Size: 68.2 MB (68211768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2cc9ba98637da7a92e64b23bc95a3aaad284b499d2a0a9c4ec13e6de9199a40`  
		Last Modified: Thu, 23 Nov 2023 11:03:07 GMT  
		Size: 425.0 KB (424997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33767fc98272f3e96292815515fd3a1e3b99d6880663a80c43630e9cbc3e6416`  
		Last Modified: Thu, 23 Nov 2023 11:04:10 GMT  
		Size: 227.3 MB (227336187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489a58e113625185954c79ae81eb0e5b3c3559d526347b47c3e4e9bb48966215`  
		Last Modified: Thu, 23 Nov 2023 11:03:52 GMT  
		Size: 1.9 MB (1931722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75ac1715c6d993f293a0dbe904bf16a8a424e993f5e4248b4828a0bf2134cea`  
		Last Modified: Thu, 23 Nov 2023 11:03:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18e383548156a7db35b81061dc74782e3c346ba36b545e85ee7c3bce4c10787`  
		Last Modified: Thu, 23 Nov 2023 11:03:52 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc82962db780951697d85165841155438b7443071283a3df5735f308d85f4a40`  
		Last Modified: Thu, 23 Nov 2023 11:03:52 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a43a19e762e9a00ab5ba6f81b7e136fe1fa485dea83151956021de17e77dcdf`  
		Last Modified: Thu, 23 Nov 2023 11:03:52 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:88215dc46ce7ccc4e017bf03b3a1d98077156169c8a9876a7674691be3cff16f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295529758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a5a3eea1e2faaa272d13ad6f80a5a9c1bc6186f943ddd34a3b58e263fbce35`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 23 Nov 2023 09:40:02 GMT
ADD file:136bb7999312a4aab093582f3b001747f508e05bfaa261c00852d06c44b23a2b in / 
# Thu, 23 Nov 2023 09:40:05 GMT
CMD ["/bin/bash"]
# Thu, 23 Nov 2023 11:06:02 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 23 Nov 2023 11:07:16 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.7.tar.gz.asc crate-5.3.7.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.7.tar.gz.asc     && tar -xf crate-5.3.7.tar.gz -C /crate --strip-components=1     && rm crate-5.3.7.tar.gz
# Thu, 23 Nov 2023 11:07:19 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 23 Nov 2023 11:07:20 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Nov 2023 11:07:20 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 23 Nov 2023 11:07:20 GMT
RUN mkdir -p /data/data /data/log
# Thu, 23 Nov 2023 11:07:20 GMT
VOLUME [/data]
# Thu, 23 Nov 2023 11:07:20 GMT
WORKDIR /data
# Thu, 23 Nov 2023 11:07:20 GMT
EXPOSE 4200 4300 5432
# Thu, 23 Nov 2023 11:07:20 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 23 Nov 2023 11:07:20 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 23 Nov 2023 11:07:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-12T16:00:23.375147 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.7
# Thu, 23 Nov 2023 11:07:21 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 23 Nov 2023 11:07:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Nov 2023 11:07:21 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:414d55c697e2dfc577ea164980a2fcec75b4913627c6a8a06cba30b3255cefee`  
		Last Modified: Thu, 23 Nov 2023 09:41:07 GMT  
		Size: 67.1 MB (67091205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf6609428d645c6b17eb0ec63fdef9acdf52fb086ebbc3683758c481450213c`  
		Last Modified: Thu, 23 Nov 2023 11:08:22 GMT  
		Size: 424.4 KB (424438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fbcbc7a37f871c9c677183c77f7058ca68ea2785398fbdf406f4fe0a307323`  
		Last Modified: Thu, 23 Nov 2023 11:09:21 GMT  
		Size: 226.1 MB (226080504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b302e37bc166c9f1e4c0d9d5a31c312da9eccbb13ae1e9b974a9e15bbd707574`  
		Last Modified: Thu, 23 Nov 2023 11:09:06 GMT  
		Size: 1.9 MB (1931729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c499c40e66fe2981d7d1bcf103583bd67258ab3c3d5feb0952d02e6a2e77d6f2`  
		Last Modified: Thu, 23 Nov 2023 11:09:05 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2dac11e41eb442f842d471c1fb70f6408e02c03544cf1bbd13696929ded56c`  
		Last Modified: Thu, 23 Nov 2023 11:09:05 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79a73011490d153e348d8355d4c61fed2d2b26417388367dda27ae3cea67c58`  
		Last Modified: Thu, 23 Nov 2023 11:09:05 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db6394d9e31a1708c7226e7cdafc321095671d117ebbed106e2474d3629f983`  
		Last Modified: Thu, 23 Nov 2023 11:09:05 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.3.7`

```console
$ docker pull crate@sha256:a68b5a4f282d391583a38c89ab7ad77c09b57f6668ff8e77368b98a906dc2fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.3.7` - linux; amd64

```console
$ docker pull crate@sha256:10dc22e2ca521b0afa915904fa88970d4354e7c65b7e931ee46250a67147f572
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297906556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918d9d826215e7fb7b328d4603327abb2016ae1cfefda2e79e8fc62746624c7c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 23 Nov 2023 10:20:12 GMT
ADD file:9774d83eefdb6ff8836449ab084b6760986009214c66efe6487e25ea59e94903 in / 
# Thu, 23 Nov 2023 10:20:13 GMT
CMD ["/bin/bash"]
# Thu, 23 Nov 2023 11:00:44 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 23 Nov 2023 11:02:05 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.7.tar.gz.asc crate-5.3.7.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.7.tar.gz.asc     && tar -xf crate-5.3.7.tar.gz -C /crate --strip-components=1     && rm crate-5.3.7.tar.gz
# Thu, 23 Nov 2023 11:02:07 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 23 Nov 2023 11:02:07 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Nov 2023 11:02:07 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 23 Nov 2023 11:02:08 GMT
RUN mkdir -p /data/data /data/log
# Thu, 23 Nov 2023 11:02:08 GMT
VOLUME [/data]
# Thu, 23 Nov 2023 11:02:08 GMT
WORKDIR /data
# Thu, 23 Nov 2023 11:02:08 GMT
EXPOSE 4200 4300 5432
# Thu, 23 Nov 2023 11:02:08 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 23 Nov 2023 11:02:08 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 23 Nov 2023 11:02:08 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-12T16:00:23.375147 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.7
# Thu, 23 Nov 2023 11:02:08 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 23 Nov 2023 11:02:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Nov 2023 11:02:09 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:702739624a8da12ef7ff47788114676caab93f317dd8df05eae8c7f7e4e1dece`  
		Last Modified: Thu, 23 Nov 2023 10:21:27 GMT  
		Size: 68.2 MB (68211768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2cc9ba98637da7a92e64b23bc95a3aaad284b499d2a0a9c4ec13e6de9199a40`  
		Last Modified: Thu, 23 Nov 2023 11:03:07 GMT  
		Size: 425.0 KB (424997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33767fc98272f3e96292815515fd3a1e3b99d6880663a80c43630e9cbc3e6416`  
		Last Modified: Thu, 23 Nov 2023 11:04:10 GMT  
		Size: 227.3 MB (227336187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489a58e113625185954c79ae81eb0e5b3c3559d526347b47c3e4e9bb48966215`  
		Last Modified: Thu, 23 Nov 2023 11:03:52 GMT  
		Size: 1.9 MB (1931722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75ac1715c6d993f293a0dbe904bf16a8a424e993f5e4248b4828a0bf2134cea`  
		Last Modified: Thu, 23 Nov 2023 11:03:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18e383548156a7db35b81061dc74782e3c346ba36b545e85ee7c3bce4c10787`  
		Last Modified: Thu, 23 Nov 2023 11:03:52 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc82962db780951697d85165841155438b7443071283a3df5735f308d85f4a40`  
		Last Modified: Thu, 23 Nov 2023 11:03:52 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a43a19e762e9a00ab5ba6f81b7e136fe1fa485dea83151956021de17e77dcdf`  
		Last Modified: Thu, 23 Nov 2023 11:03:52 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.3.7` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:88215dc46ce7ccc4e017bf03b3a1d98077156169c8a9876a7674691be3cff16f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295529758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a5a3eea1e2faaa272d13ad6f80a5a9c1bc6186f943ddd34a3b58e263fbce35`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 23 Nov 2023 09:40:02 GMT
ADD file:136bb7999312a4aab093582f3b001747f508e05bfaa261c00852d06c44b23a2b in / 
# Thu, 23 Nov 2023 09:40:05 GMT
CMD ["/bin/bash"]
# Thu, 23 Nov 2023 11:06:02 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 23 Nov 2023 11:07:16 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.7.tar.gz.asc crate-5.3.7.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.7.tar.gz.asc     && tar -xf crate-5.3.7.tar.gz -C /crate --strip-components=1     && rm crate-5.3.7.tar.gz
# Thu, 23 Nov 2023 11:07:19 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 23 Nov 2023 11:07:20 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Nov 2023 11:07:20 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 23 Nov 2023 11:07:20 GMT
RUN mkdir -p /data/data /data/log
# Thu, 23 Nov 2023 11:07:20 GMT
VOLUME [/data]
# Thu, 23 Nov 2023 11:07:20 GMT
WORKDIR /data
# Thu, 23 Nov 2023 11:07:20 GMT
EXPOSE 4200 4300 5432
# Thu, 23 Nov 2023 11:07:20 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 23 Nov 2023 11:07:20 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 23 Nov 2023 11:07:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-12T16:00:23.375147 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.7
# Thu, 23 Nov 2023 11:07:21 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 23 Nov 2023 11:07:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Nov 2023 11:07:21 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:414d55c697e2dfc577ea164980a2fcec75b4913627c6a8a06cba30b3255cefee`  
		Last Modified: Thu, 23 Nov 2023 09:41:07 GMT  
		Size: 67.1 MB (67091205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf6609428d645c6b17eb0ec63fdef9acdf52fb086ebbc3683758c481450213c`  
		Last Modified: Thu, 23 Nov 2023 11:08:22 GMT  
		Size: 424.4 KB (424438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fbcbc7a37f871c9c677183c77f7058ca68ea2785398fbdf406f4fe0a307323`  
		Last Modified: Thu, 23 Nov 2023 11:09:21 GMT  
		Size: 226.1 MB (226080504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b302e37bc166c9f1e4c0d9d5a31c312da9eccbb13ae1e9b974a9e15bbd707574`  
		Last Modified: Thu, 23 Nov 2023 11:09:06 GMT  
		Size: 1.9 MB (1931729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c499c40e66fe2981d7d1bcf103583bd67258ab3c3d5feb0952d02e6a2e77d6f2`  
		Last Modified: Thu, 23 Nov 2023 11:09:05 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2dac11e41eb442f842d471c1fb70f6408e02c03544cf1bbd13696929ded56c`  
		Last Modified: Thu, 23 Nov 2023 11:09:05 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79a73011490d153e348d8355d4c61fed2d2b26417388367dda27ae3cea67c58`  
		Last Modified: Thu, 23 Nov 2023 11:09:05 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db6394d9e31a1708c7226e7cdafc321095671d117ebbed106e2474d3629f983`  
		Last Modified: Thu, 23 Nov 2023 11:09:05 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.4`

```console
$ docker pull crate@sha256:1065df1b390749476d0860ed28ee12d5c6f671faad8480eacbacfd3922bbf04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.4` - linux; amd64

```console
$ docker pull crate@sha256:5651b56f4e6222c0781777f5ff3bc909fe32ce34d7e825aacb185ed6f01fc0e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300128031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52b6b0bfea4bd790d11e1280a4f59f02f9d479d9e89a7ce4065f9a7c45755df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 23 Nov 2023 10:20:12 GMT
ADD file:9774d83eefdb6ff8836449ab084b6760986009214c66efe6487e25ea59e94903 in / 
# Thu, 23 Nov 2023 10:20:13 GMT
CMD ["/bin/bash"]
# Thu, 23 Nov 2023 11:00:44 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 23 Nov 2023 11:01:31 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.5.tar.gz.asc crate-5.4.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.5.tar.gz.asc     && tar -xf crate-5.4.5.tar.gz -C /crate --strip-components=1     && rm crate-5.4.5.tar.gz
# Thu, 23 Nov 2023 11:01:34 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 23 Nov 2023 11:01:34 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Nov 2023 11:01:34 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 23 Nov 2023 11:01:34 GMT
RUN mkdir -p /data/data /data/log
# Thu, 23 Nov 2023 11:01:34 GMT
VOLUME [/data]
# Thu, 23 Nov 2023 11:01:35 GMT
WORKDIR /data
# Thu, 23 Nov 2023 11:01:35 GMT
EXPOSE 4200 4300 5432
# Thu, 23 Nov 2023 11:01:35 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 23 Nov 2023 11:01:35 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 23 Nov 2023 11:01:35 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-26T14:14:55.560128 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.5
# Thu, 23 Nov 2023 11:01:35 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 23 Nov 2023 11:01:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Nov 2023 11:01:35 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:702739624a8da12ef7ff47788114676caab93f317dd8df05eae8c7f7e4e1dece`  
		Last Modified: Thu, 23 Nov 2023 10:21:27 GMT  
		Size: 68.2 MB (68211768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2cc9ba98637da7a92e64b23bc95a3aaad284b499d2a0a9c4ec13e6de9199a40`  
		Last Modified: Thu, 23 Nov 2023 11:03:07 GMT  
		Size: 425.0 KB (424997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd028790fba234f235598623b9e1ee454c9249420008d2255b2b88386a30d916`  
		Last Modified: Thu, 23 Nov 2023 11:03:44 GMT  
		Size: 229.6 MB (229557658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523510cf67118b46b351d787ee1bd703efebbeee9d6c76a51a519114eceb2914`  
		Last Modified: Thu, 23 Nov 2023 11:03:26 GMT  
		Size: 1.9 MB (1931727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c58e76c5df427efa0c4a990dc0fc2f919565e24dbb9485480f8e06ce99f2f7`  
		Last Modified: Thu, 23 Nov 2023 11:03:26 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e466c62c3193d579094cee5a4da58a7ebcb2eced91e0a29e541a5d68aa26979`  
		Last Modified: Thu, 23 Nov 2023 11:03:26 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b5ddad4ea1aa035c2577450c65e93847bfd7f45bc3e83455ea058825bb8777`  
		Last Modified: Thu, 23 Nov 2023 11:03:26 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34fb4b5e4f2cb87994cdc9fbe3c49e487ba884affbb57e4c6cb213e669cf185`  
		Last Modified: Thu, 23 Nov 2023 11:03:26 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:39feabf8e89cbc59d7ab444ff0f30c390e3c891c39ed5be750e850a920ba4f70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297337845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c73193eb70f15c6fa019340717df5b340e9b8e4bf7150dfb7a038b7c37a057c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 23 Nov 2023 09:40:02 GMT
ADD file:136bb7999312a4aab093582f3b001747f508e05bfaa261c00852d06c44b23a2b in / 
# Thu, 23 Nov 2023 09:40:05 GMT
CMD ["/bin/bash"]
# Thu, 23 Nov 2023 11:06:02 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 23 Nov 2023 11:06:43 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.5.tar.gz.asc crate-5.4.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.5.tar.gz.asc     && tar -xf crate-5.4.5.tar.gz -C /crate --strip-components=1     && rm crate-5.4.5.tar.gz
# Thu, 23 Nov 2023 11:06:47 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 23 Nov 2023 11:06:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Nov 2023 11:06:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 23 Nov 2023 11:06:47 GMT
RUN mkdir -p /data/data /data/log
# Thu, 23 Nov 2023 11:06:47 GMT
VOLUME [/data]
# Thu, 23 Nov 2023 11:06:47 GMT
WORKDIR /data
# Thu, 23 Nov 2023 11:06:47 GMT
EXPOSE 4200 4300 5432
# Thu, 23 Nov 2023 11:06:47 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 23 Nov 2023 11:06:48 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 23 Nov 2023 11:06:48 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-26T14:14:55.560128 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.5
# Thu, 23 Nov 2023 11:06:48 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 23 Nov 2023 11:06:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Nov 2023 11:06:48 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:414d55c697e2dfc577ea164980a2fcec75b4913627c6a8a06cba30b3255cefee`  
		Last Modified: Thu, 23 Nov 2023 09:41:07 GMT  
		Size: 67.1 MB (67091205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf6609428d645c6b17eb0ec63fdef9acdf52fb086ebbc3683758c481450213c`  
		Last Modified: Thu, 23 Nov 2023 11:08:22 GMT  
		Size: 424.4 KB (424438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6bbd6bebb514fb226500e0ae6de76114f7205f90d5bf461ba00ddd1fbc1fb9`  
		Last Modified: Thu, 23 Nov 2023 11:08:57 GMT  
		Size: 227.9 MB (227888599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c5fa5e17a72c342d87407cdcd828f82964fda88b1660be7318c386ccbf0ccd`  
		Last Modified: Thu, 23 Nov 2023 11:08:41 GMT  
		Size: 1.9 MB (1931725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfc8bd58482d9518fdb4073d403c8ecda322acaf5544b4ca427a65eced583d3`  
		Last Modified: Thu, 23 Nov 2023 11:08:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833530f91b841d367d5d0ee68ce1fd8b3a2e84f5898769e6452e5f004574fbb0`  
		Last Modified: Thu, 23 Nov 2023 11:08:40 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10636ec7bdafac2651f849a80cbb741f3bd564c20db553310ad1feecbd9efc27`  
		Last Modified: Thu, 23 Nov 2023 11:08:41 GMT  
		Size: 953.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c99b29bf2dcc68a638a00e94f5c71ab2a42dd3989444755071e25e312da848`  
		Last Modified: Thu, 23 Nov 2023 11:08:40 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.4.5`

```console
$ docker pull crate@sha256:1065df1b390749476d0860ed28ee12d5c6f671faad8480eacbacfd3922bbf04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.4.5` - linux; amd64

```console
$ docker pull crate@sha256:5651b56f4e6222c0781777f5ff3bc909fe32ce34d7e825aacb185ed6f01fc0e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300128031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52b6b0bfea4bd790d11e1280a4f59f02f9d479d9e89a7ce4065f9a7c45755df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 23 Nov 2023 10:20:12 GMT
ADD file:9774d83eefdb6ff8836449ab084b6760986009214c66efe6487e25ea59e94903 in / 
# Thu, 23 Nov 2023 10:20:13 GMT
CMD ["/bin/bash"]
# Thu, 23 Nov 2023 11:00:44 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 23 Nov 2023 11:01:31 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.5.tar.gz.asc crate-5.4.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.5.tar.gz.asc     && tar -xf crate-5.4.5.tar.gz -C /crate --strip-components=1     && rm crate-5.4.5.tar.gz
# Thu, 23 Nov 2023 11:01:34 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 23 Nov 2023 11:01:34 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Nov 2023 11:01:34 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 23 Nov 2023 11:01:34 GMT
RUN mkdir -p /data/data /data/log
# Thu, 23 Nov 2023 11:01:34 GMT
VOLUME [/data]
# Thu, 23 Nov 2023 11:01:35 GMT
WORKDIR /data
# Thu, 23 Nov 2023 11:01:35 GMT
EXPOSE 4200 4300 5432
# Thu, 23 Nov 2023 11:01:35 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 23 Nov 2023 11:01:35 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 23 Nov 2023 11:01:35 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-26T14:14:55.560128 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.5
# Thu, 23 Nov 2023 11:01:35 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 23 Nov 2023 11:01:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Nov 2023 11:01:35 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:702739624a8da12ef7ff47788114676caab93f317dd8df05eae8c7f7e4e1dece`  
		Last Modified: Thu, 23 Nov 2023 10:21:27 GMT  
		Size: 68.2 MB (68211768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2cc9ba98637da7a92e64b23bc95a3aaad284b499d2a0a9c4ec13e6de9199a40`  
		Last Modified: Thu, 23 Nov 2023 11:03:07 GMT  
		Size: 425.0 KB (424997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd028790fba234f235598623b9e1ee454c9249420008d2255b2b88386a30d916`  
		Last Modified: Thu, 23 Nov 2023 11:03:44 GMT  
		Size: 229.6 MB (229557658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523510cf67118b46b351d787ee1bd703efebbeee9d6c76a51a519114eceb2914`  
		Last Modified: Thu, 23 Nov 2023 11:03:26 GMT  
		Size: 1.9 MB (1931727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c58e76c5df427efa0c4a990dc0fc2f919565e24dbb9485480f8e06ce99f2f7`  
		Last Modified: Thu, 23 Nov 2023 11:03:26 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e466c62c3193d579094cee5a4da58a7ebcb2eced91e0a29e541a5d68aa26979`  
		Last Modified: Thu, 23 Nov 2023 11:03:26 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b5ddad4ea1aa035c2577450c65e93847bfd7f45bc3e83455ea058825bb8777`  
		Last Modified: Thu, 23 Nov 2023 11:03:26 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34fb4b5e4f2cb87994cdc9fbe3c49e487ba884affbb57e4c6cb213e669cf185`  
		Last Modified: Thu, 23 Nov 2023 11:03:26 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.4.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:39feabf8e89cbc59d7ab444ff0f30c390e3c891c39ed5be750e850a920ba4f70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297337845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c73193eb70f15c6fa019340717df5b340e9b8e4bf7150dfb7a038b7c37a057c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 23 Nov 2023 09:40:02 GMT
ADD file:136bb7999312a4aab093582f3b001747f508e05bfaa261c00852d06c44b23a2b in / 
# Thu, 23 Nov 2023 09:40:05 GMT
CMD ["/bin/bash"]
# Thu, 23 Nov 2023 11:06:02 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 23 Nov 2023 11:06:43 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.5.tar.gz.asc crate-5.4.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.5.tar.gz.asc     && tar -xf crate-5.4.5.tar.gz -C /crate --strip-components=1     && rm crate-5.4.5.tar.gz
# Thu, 23 Nov 2023 11:06:47 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 23 Nov 2023 11:06:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Nov 2023 11:06:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 23 Nov 2023 11:06:47 GMT
RUN mkdir -p /data/data /data/log
# Thu, 23 Nov 2023 11:06:47 GMT
VOLUME [/data]
# Thu, 23 Nov 2023 11:06:47 GMT
WORKDIR /data
# Thu, 23 Nov 2023 11:06:47 GMT
EXPOSE 4200 4300 5432
# Thu, 23 Nov 2023 11:06:47 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 23 Nov 2023 11:06:48 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 23 Nov 2023 11:06:48 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-26T14:14:55.560128 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.5
# Thu, 23 Nov 2023 11:06:48 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 23 Nov 2023 11:06:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Nov 2023 11:06:48 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:414d55c697e2dfc577ea164980a2fcec75b4913627c6a8a06cba30b3255cefee`  
		Last Modified: Thu, 23 Nov 2023 09:41:07 GMT  
		Size: 67.1 MB (67091205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf6609428d645c6b17eb0ec63fdef9acdf52fb086ebbc3683758c481450213c`  
		Last Modified: Thu, 23 Nov 2023 11:08:22 GMT  
		Size: 424.4 KB (424438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6bbd6bebb514fb226500e0ae6de76114f7205f90d5bf461ba00ddd1fbc1fb9`  
		Last Modified: Thu, 23 Nov 2023 11:08:57 GMT  
		Size: 227.9 MB (227888599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c5fa5e17a72c342d87407cdcd828f82964fda88b1660be7318c386ccbf0ccd`  
		Last Modified: Thu, 23 Nov 2023 11:08:41 GMT  
		Size: 1.9 MB (1931725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfc8bd58482d9518fdb4073d403c8ecda322acaf5544b4ca427a65eced583d3`  
		Last Modified: Thu, 23 Nov 2023 11:08:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833530f91b841d367d5d0ee68ce1fd8b3a2e84f5898769e6452e5f004574fbb0`  
		Last Modified: Thu, 23 Nov 2023 11:08:40 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10636ec7bdafac2651f849a80cbb741f3bd564c20db553310ad1feecbd9efc27`  
		Last Modified: Thu, 23 Nov 2023 11:08:41 GMT  
		Size: 953.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c99b29bf2dcc68a638a00e94f5c71ab2a42dd3989444755071e25e312da848`  
		Last Modified: Thu, 23 Nov 2023 11:08:40 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.5`

```console
$ docker pull crate@sha256:4ab95576719003cb1b0cd86bf37b0673aa3d72af468e82b9208927253f417051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.5` - linux; amd64

```console
$ docker pull crate@sha256:3105e1f113c74c66a8ed5d8f7627fd9cbe2448d10bfd41028d23a90293fe77a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186689149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead61330ac1cbb1053d062ab872cf7bd07264102742f1cad71f159a80751315a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 23 Nov 2023 10:20:12 GMT
ADD file:9774d83eefdb6ff8836449ab084b6760986009214c66efe6487e25ea59e94903 in / 
# Thu, 23 Nov 2023 10:20:13 GMT
CMD ["/bin/bash"]
# Thu, 23 Nov 2023 11:00:44 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 23 Nov 2023 11:00:58 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.0.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.0.tar.gz.asc crate-5.5.0.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.0.tar.gz.asc     && tar -xf crate-5.5.0.tar.gz -C /crate --strip-components=1     && rm crate-5.5.0.tar.gz
# Thu, 23 Nov 2023 11:01:02 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 23 Nov 2023 11:01:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Nov 2023 11:01:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 23 Nov 2023 11:01:03 GMT
RUN mkdir -p /data/data /data/log
# Thu, 23 Nov 2023 11:01:03 GMT
VOLUME [/data]
# Thu, 23 Nov 2023 11:01:03 GMT
WORKDIR /data
# Thu, 23 Nov 2023 11:01:03 GMT
EXPOSE 4200 4300 5432
# Thu, 23 Nov 2023 11:01:03 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 23 Nov 2023 11:01:03 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 23 Nov 2023 11:01:03 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-27T11:44:30.874801 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.0
# Thu, 23 Nov 2023 11:01:04 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 23 Nov 2023 11:01:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Nov 2023 11:01:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:702739624a8da12ef7ff47788114676caab93f317dd8df05eae8c7f7e4e1dece`  
		Last Modified: Thu, 23 Nov 2023 10:21:27 GMT  
		Size: 68.2 MB (68211768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2cc9ba98637da7a92e64b23bc95a3aaad284b499d2a0a9c4ec13e6de9199a40`  
		Last Modified: Thu, 23 Nov 2023 11:03:07 GMT  
		Size: 425.0 KB (424997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c29e15dd9fc2223ccb821d710beb4f07d0517d00e4b6b8b7afe45b2c1575456`  
		Last Modified: Thu, 23 Nov 2023 11:03:15 GMT  
		Size: 116.1 MB (116118779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebf761091f8c2a16ec8f5550bb90a68bd177d4f161a5fac3822c8da5ea3707c`  
		Last Modified: Thu, 23 Nov 2023 11:03:05 GMT  
		Size: 1.9 MB (1931724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7fd2b03db89dde45a625e53287f0bad88e2173220febd18b3c31ddbdad2d84`  
		Last Modified: Thu, 23 Nov 2023 11:03:04 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc233f8ee4f77ece1671a2b54e0f9c3bd0ccfeb9ce1224d05885bb0128f4685`  
		Last Modified: Thu, 23 Nov 2023 11:03:04 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba430e16688b522aed75bf54741b7fe55d24f7af596b709c864476195c7cd92`  
		Last Modified: Thu, 23 Nov 2023 11:03:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191b64cacbd52dd455ae5d002aa47617a974de4a0a95c461e5f6baec2ce58ed4`  
		Last Modified: Thu, 23 Nov 2023 11:03:04 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:5fa7759d4f4bc571c1789ef554a5bbb25f64e6de498c0c130ce38e526addfdd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.1 MB (185110212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa50d23b982d5cdd0002ec885118f6693dab39dd9bb5145f9401182f60c9315b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 23 Nov 2023 09:40:02 GMT
ADD file:136bb7999312a4aab093582f3b001747f508e05bfaa261c00852d06c44b23a2b in / 
# Thu, 23 Nov 2023 09:40:05 GMT
CMD ["/bin/bash"]
# Thu, 23 Nov 2023 11:06:02 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 23 Nov 2023 11:06:15 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.0.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.0.tar.gz.asc crate-5.5.0.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.0.tar.gz.asc     && tar -xf crate-5.5.0.tar.gz -C /crate --strip-components=1     && rm crate-5.5.0.tar.gz
# Thu, 23 Nov 2023 11:06:17 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 23 Nov 2023 11:06:17 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Nov 2023 11:06:18 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 23 Nov 2023 11:06:18 GMT
RUN mkdir -p /data/data /data/log
# Thu, 23 Nov 2023 11:06:18 GMT
VOLUME [/data]
# Thu, 23 Nov 2023 11:06:18 GMT
WORKDIR /data
# Thu, 23 Nov 2023 11:06:18 GMT
EXPOSE 4200 4300 5432
# Thu, 23 Nov 2023 11:06:18 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 23 Nov 2023 11:06:18 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 23 Nov 2023 11:06:18 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-27T11:44:30.874801 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.0
# Thu, 23 Nov 2023 11:06:19 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 23 Nov 2023 11:06:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Nov 2023 11:06:19 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:414d55c697e2dfc577ea164980a2fcec75b4913627c6a8a06cba30b3255cefee`  
		Last Modified: Thu, 23 Nov 2023 09:41:07 GMT  
		Size: 67.1 MB (67091205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf6609428d645c6b17eb0ec63fdef9acdf52fb086ebbc3683758c481450213c`  
		Last Modified: Thu, 23 Nov 2023 11:08:22 GMT  
		Size: 424.4 KB (424438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cc112c8ea9ff316a690d0df3351fa5d0e8a860ad3f0417884328d9fbd320a8`  
		Last Modified: Thu, 23 Nov 2023 11:08:28 GMT  
		Size: 115.7 MB (115660955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d58fb829703d0cd42c741b0cbbbe897c4d6d10838fea9a5a6db54598942cdb4`  
		Last Modified: Thu, 23 Nov 2023 11:08:20 GMT  
		Size: 1.9 MB (1931732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f72d6cdcbce2041c2b88b3e95646d0dfd290d783aa0d3acc45bc18be3cfda53`  
		Last Modified: Thu, 23 Nov 2023 11:08:19 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4d4717f553eb7bf23bec25ba76f4e5664efcb85c7a627316a197b55a627271`  
		Last Modified: Thu, 23 Nov 2023 11:08:19 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591b57d53004fc3ae8717ba190fcf45d9cb5f57275eb5cc4b0e28d7e5ef1491d`  
		Last Modified: Thu, 23 Nov 2023 11:08:19 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38df6f10a57dcacaac066cb1c744dfc42c90e69f963096c71c76c7abea5d0a31`  
		Last Modified: Thu, 23 Nov 2023 11:08:19 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.5.0`

```console
$ docker pull crate@sha256:4ab95576719003cb1b0cd86bf37b0673aa3d72af468e82b9208927253f417051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.5.0` - linux; amd64

```console
$ docker pull crate@sha256:3105e1f113c74c66a8ed5d8f7627fd9cbe2448d10bfd41028d23a90293fe77a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186689149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead61330ac1cbb1053d062ab872cf7bd07264102742f1cad71f159a80751315a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 23 Nov 2023 10:20:12 GMT
ADD file:9774d83eefdb6ff8836449ab084b6760986009214c66efe6487e25ea59e94903 in / 
# Thu, 23 Nov 2023 10:20:13 GMT
CMD ["/bin/bash"]
# Thu, 23 Nov 2023 11:00:44 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 23 Nov 2023 11:00:58 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.0.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.0.tar.gz.asc crate-5.5.0.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.0.tar.gz.asc     && tar -xf crate-5.5.0.tar.gz -C /crate --strip-components=1     && rm crate-5.5.0.tar.gz
# Thu, 23 Nov 2023 11:01:02 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 23 Nov 2023 11:01:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Nov 2023 11:01:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 23 Nov 2023 11:01:03 GMT
RUN mkdir -p /data/data /data/log
# Thu, 23 Nov 2023 11:01:03 GMT
VOLUME [/data]
# Thu, 23 Nov 2023 11:01:03 GMT
WORKDIR /data
# Thu, 23 Nov 2023 11:01:03 GMT
EXPOSE 4200 4300 5432
# Thu, 23 Nov 2023 11:01:03 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 23 Nov 2023 11:01:03 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 23 Nov 2023 11:01:03 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-27T11:44:30.874801 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.0
# Thu, 23 Nov 2023 11:01:04 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 23 Nov 2023 11:01:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Nov 2023 11:01:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:702739624a8da12ef7ff47788114676caab93f317dd8df05eae8c7f7e4e1dece`  
		Last Modified: Thu, 23 Nov 2023 10:21:27 GMT  
		Size: 68.2 MB (68211768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2cc9ba98637da7a92e64b23bc95a3aaad284b499d2a0a9c4ec13e6de9199a40`  
		Last Modified: Thu, 23 Nov 2023 11:03:07 GMT  
		Size: 425.0 KB (424997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c29e15dd9fc2223ccb821d710beb4f07d0517d00e4b6b8b7afe45b2c1575456`  
		Last Modified: Thu, 23 Nov 2023 11:03:15 GMT  
		Size: 116.1 MB (116118779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebf761091f8c2a16ec8f5550bb90a68bd177d4f161a5fac3822c8da5ea3707c`  
		Last Modified: Thu, 23 Nov 2023 11:03:05 GMT  
		Size: 1.9 MB (1931724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7fd2b03db89dde45a625e53287f0bad88e2173220febd18b3c31ddbdad2d84`  
		Last Modified: Thu, 23 Nov 2023 11:03:04 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc233f8ee4f77ece1671a2b54e0f9c3bd0ccfeb9ce1224d05885bb0128f4685`  
		Last Modified: Thu, 23 Nov 2023 11:03:04 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba430e16688b522aed75bf54741b7fe55d24f7af596b709c864476195c7cd92`  
		Last Modified: Thu, 23 Nov 2023 11:03:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191b64cacbd52dd455ae5d002aa47617a974de4a0a95c461e5f6baec2ce58ed4`  
		Last Modified: Thu, 23 Nov 2023 11:03:04 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.5.0` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:5fa7759d4f4bc571c1789ef554a5bbb25f64e6de498c0c130ce38e526addfdd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.1 MB (185110212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa50d23b982d5cdd0002ec885118f6693dab39dd9bb5145f9401182f60c9315b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 23 Nov 2023 09:40:02 GMT
ADD file:136bb7999312a4aab093582f3b001747f508e05bfaa261c00852d06c44b23a2b in / 
# Thu, 23 Nov 2023 09:40:05 GMT
CMD ["/bin/bash"]
# Thu, 23 Nov 2023 11:06:02 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 23 Nov 2023 11:06:15 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.0.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.0.tar.gz.asc crate-5.5.0.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.0.tar.gz.asc     && tar -xf crate-5.5.0.tar.gz -C /crate --strip-components=1     && rm crate-5.5.0.tar.gz
# Thu, 23 Nov 2023 11:06:17 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 23 Nov 2023 11:06:17 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Nov 2023 11:06:18 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 23 Nov 2023 11:06:18 GMT
RUN mkdir -p /data/data /data/log
# Thu, 23 Nov 2023 11:06:18 GMT
VOLUME [/data]
# Thu, 23 Nov 2023 11:06:18 GMT
WORKDIR /data
# Thu, 23 Nov 2023 11:06:18 GMT
EXPOSE 4200 4300 5432
# Thu, 23 Nov 2023 11:06:18 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 23 Nov 2023 11:06:18 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 23 Nov 2023 11:06:18 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-27T11:44:30.874801 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.0
# Thu, 23 Nov 2023 11:06:19 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 23 Nov 2023 11:06:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Nov 2023 11:06:19 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:414d55c697e2dfc577ea164980a2fcec75b4913627c6a8a06cba30b3255cefee`  
		Last Modified: Thu, 23 Nov 2023 09:41:07 GMT  
		Size: 67.1 MB (67091205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf6609428d645c6b17eb0ec63fdef9acdf52fb086ebbc3683758c481450213c`  
		Last Modified: Thu, 23 Nov 2023 11:08:22 GMT  
		Size: 424.4 KB (424438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cc112c8ea9ff316a690d0df3351fa5d0e8a860ad3f0417884328d9fbd320a8`  
		Last Modified: Thu, 23 Nov 2023 11:08:28 GMT  
		Size: 115.7 MB (115660955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d58fb829703d0cd42c741b0cbbbe897c4d6d10838fea9a5a6db54598942cdb4`  
		Last Modified: Thu, 23 Nov 2023 11:08:20 GMT  
		Size: 1.9 MB (1931732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f72d6cdcbce2041c2b88b3e95646d0dfd290d783aa0d3acc45bc18be3cfda53`  
		Last Modified: Thu, 23 Nov 2023 11:08:19 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4d4717f553eb7bf23bec25ba76f4e5664efcb85c7a627316a197b55a627271`  
		Last Modified: Thu, 23 Nov 2023 11:08:19 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591b57d53004fc3ae8717ba190fcf45d9cb5f57275eb5cc4b0e28d7e5ef1491d`  
		Last Modified: Thu, 23 Nov 2023 11:08:19 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38df6f10a57dcacaac066cb1c744dfc42c90e69f963096c71c76c7abea5d0a31`  
		Last Modified: Thu, 23 Nov 2023 11:08:19 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:latest`

```console
$ docker pull crate@sha256:4ab95576719003cb1b0cd86bf37b0673aa3d72af468e82b9208927253f417051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:3105e1f113c74c66a8ed5d8f7627fd9cbe2448d10bfd41028d23a90293fe77a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186689149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead61330ac1cbb1053d062ab872cf7bd07264102742f1cad71f159a80751315a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 23 Nov 2023 10:20:12 GMT
ADD file:9774d83eefdb6ff8836449ab084b6760986009214c66efe6487e25ea59e94903 in / 
# Thu, 23 Nov 2023 10:20:13 GMT
CMD ["/bin/bash"]
# Thu, 23 Nov 2023 11:00:44 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 23 Nov 2023 11:00:58 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.0.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.0.tar.gz.asc crate-5.5.0.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.0.tar.gz.asc     && tar -xf crate-5.5.0.tar.gz -C /crate --strip-components=1     && rm crate-5.5.0.tar.gz
# Thu, 23 Nov 2023 11:01:02 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 23 Nov 2023 11:01:02 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Nov 2023 11:01:02 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 23 Nov 2023 11:01:03 GMT
RUN mkdir -p /data/data /data/log
# Thu, 23 Nov 2023 11:01:03 GMT
VOLUME [/data]
# Thu, 23 Nov 2023 11:01:03 GMT
WORKDIR /data
# Thu, 23 Nov 2023 11:01:03 GMT
EXPOSE 4200 4300 5432
# Thu, 23 Nov 2023 11:01:03 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 23 Nov 2023 11:01:03 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 23 Nov 2023 11:01:03 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-27T11:44:30.874801 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.0
# Thu, 23 Nov 2023 11:01:04 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 23 Nov 2023 11:01:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Nov 2023 11:01:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:702739624a8da12ef7ff47788114676caab93f317dd8df05eae8c7f7e4e1dece`  
		Last Modified: Thu, 23 Nov 2023 10:21:27 GMT  
		Size: 68.2 MB (68211768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2cc9ba98637da7a92e64b23bc95a3aaad284b499d2a0a9c4ec13e6de9199a40`  
		Last Modified: Thu, 23 Nov 2023 11:03:07 GMT  
		Size: 425.0 KB (424997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c29e15dd9fc2223ccb821d710beb4f07d0517d00e4b6b8b7afe45b2c1575456`  
		Last Modified: Thu, 23 Nov 2023 11:03:15 GMT  
		Size: 116.1 MB (116118779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebf761091f8c2a16ec8f5550bb90a68bd177d4f161a5fac3822c8da5ea3707c`  
		Last Modified: Thu, 23 Nov 2023 11:03:05 GMT  
		Size: 1.9 MB (1931724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7fd2b03db89dde45a625e53287f0bad88e2173220febd18b3c31ddbdad2d84`  
		Last Modified: Thu, 23 Nov 2023 11:03:04 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc233f8ee4f77ece1671a2b54e0f9c3bd0ccfeb9ce1224d05885bb0128f4685`  
		Last Modified: Thu, 23 Nov 2023 11:03:04 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba430e16688b522aed75bf54741b7fe55d24f7af596b709c864476195c7cd92`  
		Last Modified: Thu, 23 Nov 2023 11:03:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191b64cacbd52dd455ae5d002aa47617a974de4a0a95c461e5f6baec2ce58ed4`  
		Last Modified: Thu, 23 Nov 2023 11:03:04 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:5fa7759d4f4bc571c1789ef554a5bbb25f64e6de498c0c130ce38e526addfdd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.1 MB (185110212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa50d23b982d5cdd0002ec885118f6693dab39dd9bb5145f9401182f60c9315b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 23 Nov 2023 09:40:02 GMT
ADD file:136bb7999312a4aab093582f3b001747f508e05bfaa261c00852d06c44b23a2b in / 
# Thu, 23 Nov 2023 09:40:05 GMT
CMD ["/bin/bash"]
# Thu, 23 Nov 2023 11:06:02 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 23 Nov 2023 11:06:15 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.0.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.0.tar.gz.asc crate-5.5.0.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.0.tar.gz.asc     && tar -xf crate-5.5.0.tar.gz -C /crate --strip-components=1     && rm crate-5.5.0.tar.gz
# Thu, 23 Nov 2023 11:06:17 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 23 Nov 2023 11:06:17 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Nov 2023 11:06:18 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 23 Nov 2023 11:06:18 GMT
RUN mkdir -p /data/data /data/log
# Thu, 23 Nov 2023 11:06:18 GMT
VOLUME [/data]
# Thu, 23 Nov 2023 11:06:18 GMT
WORKDIR /data
# Thu, 23 Nov 2023 11:06:18 GMT
EXPOSE 4200 4300 5432
# Thu, 23 Nov 2023 11:06:18 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 23 Nov 2023 11:06:18 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 23 Nov 2023 11:06:18 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-27T11:44:30.874801 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.0
# Thu, 23 Nov 2023 11:06:19 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 23 Nov 2023 11:06:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Nov 2023 11:06:19 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:414d55c697e2dfc577ea164980a2fcec75b4913627c6a8a06cba30b3255cefee`  
		Last Modified: Thu, 23 Nov 2023 09:41:07 GMT  
		Size: 67.1 MB (67091205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf6609428d645c6b17eb0ec63fdef9acdf52fb086ebbc3683758c481450213c`  
		Last Modified: Thu, 23 Nov 2023 11:08:22 GMT  
		Size: 424.4 KB (424438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cc112c8ea9ff316a690d0df3351fa5d0e8a860ad3f0417884328d9fbd320a8`  
		Last Modified: Thu, 23 Nov 2023 11:08:28 GMT  
		Size: 115.7 MB (115660955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d58fb829703d0cd42c741b0cbbbe897c4d6d10838fea9a5a6db54598942cdb4`  
		Last Modified: Thu, 23 Nov 2023 11:08:20 GMT  
		Size: 1.9 MB (1931732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f72d6cdcbce2041c2b88b3e95646d0dfd290d783aa0d3acc45bc18be3cfda53`  
		Last Modified: Thu, 23 Nov 2023 11:08:19 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4d4717f553eb7bf23bec25ba76f4e5664efcb85c7a627316a197b55a627271`  
		Last Modified: Thu, 23 Nov 2023 11:08:19 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591b57d53004fc3ae8717ba190fcf45d9cb5f57275eb5cc4b0e28d7e5ef1491d`  
		Last Modified: Thu, 23 Nov 2023 11:08:19 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38df6f10a57dcacaac066cb1c744dfc42c90e69f963096c71c76c7abea5d0a31`  
		Last Modified: Thu, 23 Nov 2023 11:08:19 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
