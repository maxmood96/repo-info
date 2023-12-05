<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:4.8`](#crate48)
-	[`crate:4.8.4`](#crate484)
-	[`crate:5.2`](#crate52)
-	[`crate:5.2.10`](#crate5210)
-	[`crate:5.3`](#crate53)
-	[`crate:5.3.7`](#crate537)
-	[`crate:5.4`](#crate54)
-	[`crate:5.4.6`](#crate546)
-	[`crate:5.5`](#crate55)
-	[`crate:5.5.1`](#crate551)
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
$ docker pull crate@sha256:e7287935c9883406d10d73cb9f1bc90b292481d2e6bbd5b41d63d394d6b9ab85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.2` - linux; amd64

```console
$ docker pull crate@sha256:cab069bde517a4d3a854411be293a538b84a40921ac76a449cfbfc32187cf0c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304896196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11739580f17b5d45d477409e4df659f7fce8b548ec45f22e41779baed947299`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:50:24 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python3 python3-pip     && yum clean all     && rm -rf /var/cache/yum
# Tue, 28 Nov 2023 23:50:46 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.2.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.2.10.tar.gz.asc crate-5.2.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.2.10.tar.gz.asc     && tar -xf crate-5.2.10.tar.gz -C /crate --strip-components=1     && rm crate-5.2.10.tar.gz
# Tue, 28 Nov 2023 23:50:48 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 28 Nov 2023 23:50:48 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:50:48 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 28 Nov 2023 23:50:49 GMT
RUN mkdir -p /data/data /data/log
# Tue, 28 Nov 2023 23:50:49 GMT
VOLUME [/data]
# Tue, 28 Nov 2023 23:50:49 GMT
WORKDIR /data
# Tue, 28 Nov 2023 23:50:49 GMT
EXPOSE 4200 4300 5432
# Tue, 28 Nov 2023 23:50:49 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 28 Nov 2023 23:50:49 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 28 Nov 2023 23:50:49 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-12T15:07:59.910862 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.2.10
# Tue, 28 Nov 2023 23:50:50 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 28 Nov 2023 23:50:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:50:50 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:28130cb29ede9c7eb632516608f6be44c01d736736eb9f03846fb16c819426ae`  
		Last Modified: Tue, 28 Nov 2023 23:29:38 GMT  
		Size: 68.2 MB (68211613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e88b37c36ac28be31a7117edcd4f546a476c12a070fc3589cc37db76ba889f4`  
		Last Modified: Tue, 28 Nov 2023 23:52:33 GMT  
		Size: 7.6 MB (7631993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a71aba3b6906f7ed3137ff22093d5208c873a02d6ba9c88e235d7c5be075fa`  
		Last Modified: Tue, 28 Nov 2023 23:52:47 GMT  
		Size: 227.1 MB (227118972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5bfe354b2977f4a9648b906f7010ae3a237599647532e104eec1da17188da3b`  
		Last Modified: Tue, 28 Nov 2023 23:52:30 GMT  
		Size: 1.9 MB (1931732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039b22ec8bde411784e438d559aaccc91600820f4a97b3174935859c85ff2b0e`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ec734ff70cb18f9c901d138f4950134aa2e35f50eb260286dff7e53c17c23e`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e13c4b6213bf851235fd82ae5f264a40e8c5810f48dc3420f42ab7ee6e034da`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c3396fcf9a967214a76fff554be41fa5ea7ab7cdcf53260b99e875ebd7315a`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:91f2e9625bc59c85aa733085bf3f5c54003be2da1e7be4ecd9433af1ee48dd77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302363005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340bbf4379391607752b80741bc3b62351585523e306fd71bca700eb6fa8c409`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:18:09 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python3 python3-pip     && yum clean all     && rm -rf /var/cache/yum
# Wed, 29 Nov 2023 00:18:31 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.2.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.2.10.tar.gz.asc crate-5.2.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.2.10.tar.gz.asc     && tar -xf crate-5.2.10.tar.gz -C /crate --strip-components=1     && rm crate-5.2.10.tar.gz
# Wed, 29 Nov 2023 00:18:34 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 29 Nov 2023 00:18:34 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:18:34 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 29 Nov 2023 00:18:35 GMT
RUN mkdir -p /data/data /data/log
# Wed, 29 Nov 2023 00:18:35 GMT
VOLUME [/data]
# Wed, 29 Nov 2023 00:18:35 GMT
WORKDIR /data
# Wed, 29 Nov 2023 00:18:35 GMT
EXPOSE 4200 4300 5432
# Wed, 29 Nov 2023 00:18:35 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 29 Nov 2023 00:18:35 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 29 Nov 2023 00:18:35 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-12T15:07:59.910862 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.2.10
# Wed, 29 Nov 2023 00:18:35 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 29 Nov 2023 00:18:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:18:36 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c1500036e99b2f702d6379d090f3a4275a6e20d574bd82310d582cb60b2d1cf5`  
		Last Modified: Tue, 28 Nov 2023 23:43:55 GMT  
		Size: 67.1 MB (67090991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f804096b6187f46a18908e90329b82a2f8cafca25ef269a42d22649e1fefc5`  
		Last Modified: Wed, 29 Nov 2023 00:20:12 GMT  
		Size: 7.5 MB (7476469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5ac8c463650186dd41b280fd3cfe3bad91ea706d9b6db91e1bd028473b715a`  
		Last Modified: Wed, 29 Nov 2023 00:20:23 GMT  
		Size: 225.9 MB (225861933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05692d83977f5ca1036c8cf7003c52bc4680ca840344f739e0a7fe18ac96d711`  
		Last Modified: Wed, 29 Nov 2023 00:20:09 GMT  
		Size: 1.9 MB (1931729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78980644dea42a742f60af7cbb08e3da6bef329679848ccf61f7e7d88c479ba`  
		Last Modified: Wed, 29 Nov 2023 00:20:09 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf399494019c285079d06e548bfaa79dd175b5cca7f1318319d786372bd4d839`  
		Last Modified: Wed, 29 Nov 2023 00:20:08 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7997f2ae8e07754c98036eee920669039943e0d758310d08ab434854a09d3a`  
		Last Modified: Wed, 29 Nov 2023 00:20:08 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73e3fda0dcbb80768b2982f8c2250be5fbbe9c7b8bbdd242385daa8fa1e7948`  
		Last Modified: Wed, 29 Nov 2023 00:20:09 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.2.10`

```console
$ docker pull crate@sha256:e7287935c9883406d10d73cb9f1bc90b292481d2e6bbd5b41d63d394d6b9ab85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.2.10` - linux; amd64

```console
$ docker pull crate@sha256:cab069bde517a4d3a854411be293a538b84a40921ac76a449cfbfc32187cf0c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304896196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11739580f17b5d45d477409e4df659f7fce8b548ec45f22e41779baed947299`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:50:24 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python3 python3-pip     && yum clean all     && rm -rf /var/cache/yum
# Tue, 28 Nov 2023 23:50:46 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.2.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.2.10.tar.gz.asc crate-5.2.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.2.10.tar.gz.asc     && tar -xf crate-5.2.10.tar.gz -C /crate --strip-components=1     && rm crate-5.2.10.tar.gz
# Tue, 28 Nov 2023 23:50:48 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 28 Nov 2023 23:50:48 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:50:48 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 28 Nov 2023 23:50:49 GMT
RUN mkdir -p /data/data /data/log
# Tue, 28 Nov 2023 23:50:49 GMT
VOLUME [/data]
# Tue, 28 Nov 2023 23:50:49 GMT
WORKDIR /data
# Tue, 28 Nov 2023 23:50:49 GMT
EXPOSE 4200 4300 5432
# Tue, 28 Nov 2023 23:50:49 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 28 Nov 2023 23:50:49 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 28 Nov 2023 23:50:49 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-12T15:07:59.910862 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.2.10
# Tue, 28 Nov 2023 23:50:50 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 28 Nov 2023 23:50:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:50:50 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:28130cb29ede9c7eb632516608f6be44c01d736736eb9f03846fb16c819426ae`  
		Last Modified: Tue, 28 Nov 2023 23:29:38 GMT  
		Size: 68.2 MB (68211613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e88b37c36ac28be31a7117edcd4f546a476c12a070fc3589cc37db76ba889f4`  
		Last Modified: Tue, 28 Nov 2023 23:52:33 GMT  
		Size: 7.6 MB (7631993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a71aba3b6906f7ed3137ff22093d5208c873a02d6ba9c88e235d7c5be075fa`  
		Last Modified: Tue, 28 Nov 2023 23:52:47 GMT  
		Size: 227.1 MB (227118972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5bfe354b2977f4a9648b906f7010ae3a237599647532e104eec1da17188da3b`  
		Last Modified: Tue, 28 Nov 2023 23:52:30 GMT  
		Size: 1.9 MB (1931732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039b22ec8bde411784e438d559aaccc91600820f4a97b3174935859c85ff2b0e`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ec734ff70cb18f9c901d138f4950134aa2e35f50eb260286dff7e53c17c23e`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e13c4b6213bf851235fd82ae5f264a40e8c5810f48dc3420f42ab7ee6e034da`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c3396fcf9a967214a76fff554be41fa5ea7ab7cdcf53260b99e875ebd7315a`  
		Last Modified: Tue, 28 Nov 2023 23:52:29 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.2.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:91f2e9625bc59c85aa733085bf3f5c54003be2da1e7be4ecd9433af1ee48dd77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302363005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340bbf4379391607752b80741bc3b62351585523e306fd71bca700eb6fa8c409`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:18:09 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python3 python3-pip     && yum clean all     && rm -rf /var/cache/yum
# Wed, 29 Nov 2023 00:18:31 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.2.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.2.10.tar.gz.asc crate-5.2.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.2.10.tar.gz.asc     && tar -xf crate-5.2.10.tar.gz -C /crate --strip-components=1     && rm crate-5.2.10.tar.gz
# Wed, 29 Nov 2023 00:18:34 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 29 Nov 2023 00:18:34 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:18:34 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 29 Nov 2023 00:18:35 GMT
RUN mkdir -p /data/data /data/log
# Wed, 29 Nov 2023 00:18:35 GMT
VOLUME [/data]
# Wed, 29 Nov 2023 00:18:35 GMT
WORKDIR /data
# Wed, 29 Nov 2023 00:18:35 GMT
EXPOSE 4200 4300 5432
# Wed, 29 Nov 2023 00:18:35 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 29 Nov 2023 00:18:35 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 29 Nov 2023 00:18:35 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-12T15:07:59.910862 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.2.10
# Wed, 29 Nov 2023 00:18:35 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 29 Nov 2023 00:18:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:18:36 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c1500036e99b2f702d6379d090f3a4275a6e20d574bd82310d582cb60b2d1cf5`  
		Last Modified: Tue, 28 Nov 2023 23:43:55 GMT  
		Size: 67.1 MB (67090991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f804096b6187f46a18908e90329b82a2f8cafca25ef269a42d22649e1fefc5`  
		Last Modified: Wed, 29 Nov 2023 00:20:12 GMT  
		Size: 7.5 MB (7476469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5ac8c463650186dd41b280fd3cfe3bad91ea706d9b6db91e1bd028473b715a`  
		Last Modified: Wed, 29 Nov 2023 00:20:23 GMT  
		Size: 225.9 MB (225861933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05692d83977f5ca1036c8cf7003c52bc4680ca840344f739e0a7fe18ac96d711`  
		Last Modified: Wed, 29 Nov 2023 00:20:09 GMT  
		Size: 1.9 MB (1931729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78980644dea42a742f60af7cbb08e3da6bef329679848ccf61f7e7d88c479ba`  
		Last Modified: Wed, 29 Nov 2023 00:20:09 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf399494019c285079d06e548bfaa79dd175b5cca7f1318319d786372bd4d839`  
		Last Modified: Wed, 29 Nov 2023 00:20:08 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7997f2ae8e07754c98036eee920669039943e0d758310d08ab434854a09d3a`  
		Last Modified: Wed, 29 Nov 2023 00:20:08 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73e3fda0dcbb80768b2982f8c2250be5fbbe9c7b8bbdd242385daa8fa1e7948`  
		Last Modified: Wed, 29 Nov 2023 00:20:09 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.3`

```console
$ docker pull crate@sha256:c6a99f1a50ffa44317287c8f53170dd15618c9be2214efb412667e78ae339fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.3` - linux; amd64

```console
$ docker pull crate@sha256:7807e9690d453558282fd90145a2db1be585df5ac854e07ecb0c2b9b04a42957
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297906271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1594823da27aa654494820b29113021fde44b336b456d23e40673c7fc39eb065`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:48:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 28 Nov 2023 23:50:08 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.7.tar.gz.asc crate-5.3.7.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.7.tar.gz.asc     && tar -xf crate-5.3.7.tar.gz -C /crate --strip-components=1     && rm crate-5.3.7.tar.gz
# Tue, 28 Nov 2023 23:50:11 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 28 Nov 2023 23:50:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:50:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 28 Nov 2023 23:50:12 GMT
RUN mkdir -p /data/data /data/log
# Tue, 28 Nov 2023 23:50:12 GMT
VOLUME [/data]
# Tue, 28 Nov 2023 23:50:12 GMT
WORKDIR /data
# Tue, 28 Nov 2023 23:50:12 GMT
EXPOSE 4200 4300 5432
# Tue, 28 Nov 2023 23:50:12 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 28 Nov 2023 23:50:12 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 28 Nov 2023 23:50:12 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-12T16:00:23.375147 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.7
# Tue, 28 Nov 2023 23:50:12 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 28 Nov 2023 23:50:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:50:12 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:28130cb29ede9c7eb632516608f6be44c01d736736eb9f03846fb16c819426ae`  
		Last Modified: Tue, 28 Nov 2023 23:29:38 GMT  
		Size: 68.2 MB (68211613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474dd2aa9d062ecbc8a0eb11a10b354dea867214e1deec1655700136f902458e`  
		Last Modified: Tue, 28 Nov 2023 23:51:14 GMT  
		Size: 424.9 KB (424899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f46977c24873d5aecdffe04ed94071914f059bf01aa4f2db12085729a8c2bc`  
		Last Modified: Tue, 28 Nov 2023 23:52:21 GMT  
		Size: 227.3 MB (227336142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b44d85e4b0b4f140aad833205f216aa343902cfce78b0bfe3d08fa01c864e17`  
		Last Modified: Tue, 28 Nov 2023 23:52:03 GMT  
		Size: 1.9 MB (1931730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d41ed9efa79c623e737c72b4843e5510f3bd92311435ce16f97ab2c714de20`  
		Last Modified: Tue, 28 Nov 2023 23:52:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:defbf8a72f0834740f56806c4fb4ea7754290d5aaa3eb9d20e9526b01c9c093c`  
		Last Modified: Tue, 28 Nov 2023 23:52:03 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc190ac365ddd7c9a4afbc1613a97724603c35b845f0f7442068f7b258250f1a`  
		Last Modified: Tue, 28 Nov 2023 23:52:03 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb0115c460549c7783b4a1d146e770981d1b94abe39c7745db7fea74e6cc561`  
		Last Modified: Tue, 28 Nov 2023 23:52:03 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:7e2d0c36bd477e9e2e3b6ea712aae6fcb8188aa26d2eed917d6ce45ad0ab045d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295529510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371027a23f6fe3035199f93140e87e22ee0a5d77d387730d502559e374994656`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Wed, 29 Nov 2023 00:17:52 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.7.tar.gz.asc crate-5.3.7.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.7.tar.gz.asc     && tar -xf crate-5.3.7.tar.gz -C /crate --strip-components=1     && rm crate-5.3.7.tar.gz
# Wed, 29 Nov 2023 00:17:56 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 29 Nov 2023 00:17:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:17:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 29 Nov 2023 00:17:56 GMT
RUN mkdir -p /data/data /data/log
# Wed, 29 Nov 2023 00:17:56 GMT
VOLUME [/data]
# Wed, 29 Nov 2023 00:17:56 GMT
WORKDIR /data
# Wed, 29 Nov 2023 00:17:57 GMT
EXPOSE 4200 4300 5432
# Wed, 29 Nov 2023 00:17:57 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 29 Nov 2023 00:17:57 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 29 Nov 2023 00:17:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-12T16:00:23.375147 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.7
# Wed, 29 Nov 2023 00:17:57 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 29 Nov 2023 00:17:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:17:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c1500036e99b2f702d6379d090f3a4275a6e20d574bd82310d582cb60b2d1cf5`  
		Last Modified: Tue, 28 Nov 2023 23:43:55 GMT  
		Size: 67.1 MB (67090991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c229dddf1130365642b2edf5bbcf90362be62d41571e89dd36c74ef5831ba73f`  
		Last Modified: Wed, 29 Nov 2023 00:19:03 GMT  
		Size: 424.4 KB (424401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0350437d7e0f6274bd539222913e4c5848434925b82df4f59ac2ba4f90519285`  
		Last Modified: Wed, 29 Nov 2023 00:20:00 GMT  
		Size: 226.1 MB (226080518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7715c8d1a2e3873044560c27771875ab52af64fd1e2dccf887b76fec3cbb99f7`  
		Last Modified: Wed, 29 Nov 2023 00:19:46 GMT  
		Size: 1.9 MB (1931721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1915c799a25c52c770cb9ab2439001259a5951dd04703e26ec86d5ee25d67ab6`  
		Last Modified: Wed, 29 Nov 2023 00:19:45 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443779687db3222f21c01a630c838435d8fb58c69cf57ab78303635258141d29`  
		Last Modified: Wed, 29 Nov 2023 00:19:45 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af8e4aa7af301e41497fb1266bfd088abb88bd9a1b2fb3e27e2a229e6fefdee`  
		Last Modified: Wed, 29 Nov 2023 00:19:45 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e50b280d4d225bd65f1e61c7ab9a099031d80c5f95e50da5333de064db9a10`  
		Last Modified: Wed, 29 Nov 2023 00:19:45 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.3.7`

```console
$ docker pull crate@sha256:c6a99f1a50ffa44317287c8f53170dd15618c9be2214efb412667e78ae339fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.3.7` - linux; amd64

```console
$ docker pull crate@sha256:7807e9690d453558282fd90145a2db1be585df5ac854e07ecb0c2b9b04a42957
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297906271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1594823da27aa654494820b29113021fde44b336b456d23e40673c7fc39eb065`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:48:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 28 Nov 2023 23:50:08 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.7.tar.gz.asc crate-5.3.7.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.7.tar.gz.asc     && tar -xf crate-5.3.7.tar.gz -C /crate --strip-components=1     && rm crate-5.3.7.tar.gz
# Tue, 28 Nov 2023 23:50:11 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 28 Nov 2023 23:50:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Nov 2023 23:50:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 28 Nov 2023 23:50:12 GMT
RUN mkdir -p /data/data /data/log
# Tue, 28 Nov 2023 23:50:12 GMT
VOLUME [/data]
# Tue, 28 Nov 2023 23:50:12 GMT
WORKDIR /data
# Tue, 28 Nov 2023 23:50:12 GMT
EXPOSE 4200 4300 5432
# Tue, 28 Nov 2023 23:50:12 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 28 Nov 2023 23:50:12 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 28 Nov 2023 23:50:12 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-12T16:00:23.375147 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.7
# Tue, 28 Nov 2023 23:50:12 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 28 Nov 2023 23:50:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:50:12 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:28130cb29ede9c7eb632516608f6be44c01d736736eb9f03846fb16c819426ae`  
		Last Modified: Tue, 28 Nov 2023 23:29:38 GMT  
		Size: 68.2 MB (68211613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474dd2aa9d062ecbc8a0eb11a10b354dea867214e1deec1655700136f902458e`  
		Last Modified: Tue, 28 Nov 2023 23:51:14 GMT  
		Size: 424.9 KB (424899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f46977c24873d5aecdffe04ed94071914f059bf01aa4f2db12085729a8c2bc`  
		Last Modified: Tue, 28 Nov 2023 23:52:21 GMT  
		Size: 227.3 MB (227336142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b44d85e4b0b4f140aad833205f216aa343902cfce78b0bfe3d08fa01c864e17`  
		Last Modified: Tue, 28 Nov 2023 23:52:03 GMT  
		Size: 1.9 MB (1931730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d41ed9efa79c623e737c72b4843e5510f3bd92311435ce16f97ab2c714de20`  
		Last Modified: Tue, 28 Nov 2023 23:52:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:defbf8a72f0834740f56806c4fb4ea7754290d5aaa3eb9d20e9526b01c9c093c`  
		Last Modified: Tue, 28 Nov 2023 23:52:03 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc190ac365ddd7c9a4afbc1613a97724603c35b845f0f7442068f7b258250f1a`  
		Last Modified: Tue, 28 Nov 2023 23:52:03 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb0115c460549c7783b4a1d146e770981d1b94abe39c7745db7fea74e6cc561`  
		Last Modified: Tue, 28 Nov 2023 23:52:03 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.3.7` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:7e2d0c36bd477e9e2e3b6ea712aae6fcb8188aa26d2eed917d6ce45ad0ab045d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295529510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371027a23f6fe3035199f93140e87e22ee0a5d77d387730d502559e374994656`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Wed, 29 Nov 2023 00:17:52 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.7.tar.gz.asc crate-5.3.7.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.7.tar.gz.asc     && tar -xf crate-5.3.7.tar.gz -C /crate --strip-components=1     && rm crate-5.3.7.tar.gz
# Wed, 29 Nov 2023 00:17:56 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 29 Nov 2023 00:17:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Nov 2023 00:17:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 29 Nov 2023 00:17:56 GMT
RUN mkdir -p /data/data /data/log
# Wed, 29 Nov 2023 00:17:56 GMT
VOLUME [/data]
# Wed, 29 Nov 2023 00:17:56 GMT
WORKDIR /data
# Wed, 29 Nov 2023 00:17:57 GMT
EXPOSE 4200 4300 5432
# Wed, 29 Nov 2023 00:17:57 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 29 Nov 2023 00:17:57 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 29 Nov 2023 00:17:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-10-12T16:00:23.375147 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.7
# Wed, 29 Nov 2023 00:17:57 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 29 Nov 2023 00:17:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:17:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c1500036e99b2f702d6379d090f3a4275a6e20d574bd82310d582cb60b2d1cf5`  
		Last Modified: Tue, 28 Nov 2023 23:43:55 GMT  
		Size: 67.1 MB (67090991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c229dddf1130365642b2edf5bbcf90362be62d41571e89dd36c74ef5831ba73f`  
		Last Modified: Wed, 29 Nov 2023 00:19:03 GMT  
		Size: 424.4 KB (424401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0350437d7e0f6274bd539222913e4c5848434925b82df4f59ac2ba4f90519285`  
		Last Modified: Wed, 29 Nov 2023 00:20:00 GMT  
		Size: 226.1 MB (226080518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7715c8d1a2e3873044560c27771875ab52af64fd1e2dccf887b76fec3cbb99f7`  
		Last Modified: Wed, 29 Nov 2023 00:19:46 GMT  
		Size: 1.9 MB (1931721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1915c799a25c52c770cb9ab2439001259a5951dd04703e26ec86d5ee25d67ab6`  
		Last Modified: Wed, 29 Nov 2023 00:19:45 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443779687db3222f21c01a630c838435d8fb58c69cf57ab78303635258141d29`  
		Last Modified: Wed, 29 Nov 2023 00:19:45 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af8e4aa7af301e41497fb1266bfd088abb88bd9a1b2fb3e27e2a229e6fefdee`  
		Last Modified: Wed, 29 Nov 2023 00:19:45 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e50b280d4d225bd65f1e61c7ab9a099031d80c5f95e50da5333de064db9a10`  
		Last Modified: Wed, 29 Nov 2023 00:19:45 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.4`

```console
$ docker pull crate@sha256:95b74e844e768320633a7da2f3f050c614cd9d314fc32533c4867af8eb65f4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.4` - linux; amd64

```console
$ docker pull crate@sha256:6d43c0e3ce759f6a7979f82fbdadb6de6cce14a43c33b0a8434869c954adef4a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300128401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6792282e5d1f8ad600aa018fa413610c90fe2c3a007fa47de945dd82b6992fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:48:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 05 Dec 2023 18:45:47 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.6.tar.gz.asc crate-5.4.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.6.tar.gz.asc     && tar -xf crate-5.4.6.tar.gz -C /crate --strip-components=1     && rm crate-5.4.6.tar.gz
# Tue, 05 Dec 2023 18:45:51 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 05 Dec 2023 18:45:51 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 18:45:51 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 05 Dec 2023 18:45:52 GMT
RUN mkdir -p /data/data /data/log
# Tue, 05 Dec 2023 18:45:52 GMT
VOLUME [/data]
# Tue, 05 Dec 2023 18:45:52 GMT
WORKDIR /data
# Tue, 05 Dec 2023 18:45:52 GMT
EXPOSE 4200 4300 5432
# Tue, 05 Dec 2023 18:45:52 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 05 Dec 2023 18:45:52 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 05 Dec 2023 18:45:53 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-11-30T13:48:50.915165 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.6
# Tue, 05 Dec 2023 18:45:53 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 05 Dec 2023 18:45:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 18:45:53 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:28130cb29ede9c7eb632516608f6be44c01d736736eb9f03846fb16c819426ae`  
		Last Modified: Tue, 28 Nov 2023 23:29:38 GMT  
		Size: 68.2 MB (68211613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474dd2aa9d062ecbc8a0eb11a10b354dea867214e1deec1655700136f902458e`  
		Last Modified: Tue, 28 Nov 2023 23:51:14 GMT  
		Size: 424.9 KB (424899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63d7e8f44354f7cd891e5057ef226e85efdf4bbd754e1d04fe2034d6095db14`  
		Last Modified: Tue, 05 Dec 2023 18:46:57 GMT  
		Size: 229.6 MB (229558276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc7c969837a9843815e38b916066c6eda4d7137b90cbb1dda3660b78a8a1a28`  
		Last Modified: Tue, 05 Dec 2023 18:46:38 GMT  
		Size: 1.9 MB (1931731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2419e4828cafef71a608824989229ce7e346bc70c4ff2a7545608329aede4fe1`  
		Last Modified: Tue, 05 Dec 2023 18:46:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9caf41eb3d7e0b74fb43eb94aaf821ffc7f5507e3d8d60c69eedd961f8a5bd6`  
		Last Modified: Tue, 05 Dec 2023 18:46:38 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f134eb722c8a58bcded42705f68cc795756396a304ec0156538ace93c12ad6`  
		Last Modified: Tue, 05 Dec 2023 18:46:38 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9e030a0ba09a74c5f19ca02a89916ced62d5dfdf70026a47c9591963b49f44`  
		Last Modified: Tue, 05 Dec 2023 18:46:38 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:7c6aca5d999427dcccaaff3a222df4154ff78cbd3fe3c9181ae554ec1a30be31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297337199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681ad5d1eed304ed4dfd72d219d14a7649e1fb698f01c1a29f2015766f2e3218`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 05 Dec 2023 19:59:04 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.6.tar.gz.asc crate-5.4.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.6.tar.gz.asc     && tar -xf crate-5.4.6.tar.gz -C /crate --strip-components=1     && rm crate-5.4.6.tar.gz
# Tue, 05 Dec 2023 19:59:08 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 05 Dec 2023 19:59:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 19:59:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 05 Dec 2023 19:59:09 GMT
RUN mkdir -p /data/data /data/log
# Tue, 05 Dec 2023 19:59:09 GMT
VOLUME [/data]
# Tue, 05 Dec 2023 19:59:09 GMT
WORKDIR /data
# Tue, 05 Dec 2023 19:59:09 GMT
EXPOSE 4200 4300 5432
# Tue, 05 Dec 2023 19:59:09 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 05 Dec 2023 19:59:10 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 05 Dec 2023 19:59:10 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-11-30T13:48:50.915165 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.6
# Tue, 05 Dec 2023 19:59:10 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 05 Dec 2023 19:59:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:59:10 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c1500036e99b2f702d6379d090f3a4275a6e20d574bd82310d582cb60b2d1cf5`  
		Last Modified: Tue, 28 Nov 2023 23:43:55 GMT  
		Size: 67.1 MB (67090991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c229dddf1130365642b2edf5bbcf90362be62d41571e89dd36c74ef5831ba73f`  
		Last Modified: Wed, 29 Nov 2023 00:19:03 GMT  
		Size: 424.4 KB (424401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f976d4f47851d58234cac32b7a40bde19dac290762e464ffdbdf6cfaebba90`  
		Last Modified: Tue, 05 Dec 2023 20:00:06 GMT  
		Size: 227.9 MB (227888200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921ac46ffd5c8eaf082cf99c6f95afe5f92fdedd5178ac8617c3a2bda5ceaedb`  
		Last Modified: Tue, 05 Dec 2023 19:59:51 GMT  
		Size: 1.9 MB (1931727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565c8253aaeda8b727987070235211e31b2edea043514bb4d862746b74abb391`  
		Last Modified: Tue, 05 Dec 2023 19:59:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da09ce298d953ccea0a242b297fd88c00a90989d84b532a650afe2eb71bc5a2`  
		Last Modified: Tue, 05 Dec 2023 19:59:51 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b377ef953dbeca7a2cd31fda74da1b39842c631d79f285018bed8a4578359d10`  
		Last Modified: Tue, 05 Dec 2023 19:59:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d8c025fa9c73992359e82a532dadf7b13a38196b58d3d417a3122b2b70e100`  
		Last Modified: Tue, 05 Dec 2023 19:59:50 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.4.6`

```console
$ docker pull crate@sha256:95b74e844e768320633a7da2f3f050c614cd9d314fc32533c4867af8eb65f4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.4.6` - linux; amd64

```console
$ docker pull crate@sha256:6d43c0e3ce759f6a7979f82fbdadb6de6cce14a43c33b0a8434869c954adef4a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300128401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6792282e5d1f8ad600aa018fa413610c90fe2c3a007fa47de945dd82b6992fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:48:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 05 Dec 2023 18:45:47 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.6.tar.gz.asc crate-5.4.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.6.tar.gz.asc     && tar -xf crate-5.4.6.tar.gz -C /crate --strip-components=1     && rm crate-5.4.6.tar.gz
# Tue, 05 Dec 2023 18:45:51 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 05 Dec 2023 18:45:51 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 18:45:51 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 05 Dec 2023 18:45:52 GMT
RUN mkdir -p /data/data /data/log
# Tue, 05 Dec 2023 18:45:52 GMT
VOLUME [/data]
# Tue, 05 Dec 2023 18:45:52 GMT
WORKDIR /data
# Tue, 05 Dec 2023 18:45:52 GMT
EXPOSE 4200 4300 5432
# Tue, 05 Dec 2023 18:45:52 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 05 Dec 2023 18:45:52 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 05 Dec 2023 18:45:53 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-11-30T13:48:50.915165 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.6
# Tue, 05 Dec 2023 18:45:53 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 05 Dec 2023 18:45:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 18:45:53 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:28130cb29ede9c7eb632516608f6be44c01d736736eb9f03846fb16c819426ae`  
		Last Modified: Tue, 28 Nov 2023 23:29:38 GMT  
		Size: 68.2 MB (68211613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474dd2aa9d062ecbc8a0eb11a10b354dea867214e1deec1655700136f902458e`  
		Last Modified: Tue, 28 Nov 2023 23:51:14 GMT  
		Size: 424.9 KB (424899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63d7e8f44354f7cd891e5057ef226e85efdf4bbd754e1d04fe2034d6095db14`  
		Last Modified: Tue, 05 Dec 2023 18:46:57 GMT  
		Size: 229.6 MB (229558276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc7c969837a9843815e38b916066c6eda4d7137b90cbb1dda3660b78a8a1a28`  
		Last Modified: Tue, 05 Dec 2023 18:46:38 GMT  
		Size: 1.9 MB (1931731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2419e4828cafef71a608824989229ce7e346bc70c4ff2a7545608329aede4fe1`  
		Last Modified: Tue, 05 Dec 2023 18:46:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9caf41eb3d7e0b74fb43eb94aaf821ffc7f5507e3d8d60c69eedd961f8a5bd6`  
		Last Modified: Tue, 05 Dec 2023 18:46:38 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f134eb722c8a58bcded42705f68cc795756396a304ec0156538ace93c12ad6`  
		Last Modified: Tue, 05 Dec 2023 18:46:38 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9e030a0ba09a74c5f19ca02a89916ced62d5dfdf70026a47c9591963b49f44`  
		Last Modified: Tue, 05 Dec 2023 18:46:38 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.4.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:7c6aca5d999427dcccaaff3a222df4154ff78cbd3fe3c9181ae554ec1a30be31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297337199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681ad5d1eed304ed4dfd72d219d14a7649e1fb698f01c1a29f2015766f2e3218`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 05 Dec 2023 19:59:04 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.6.tar.gz.asc crate-5.4.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.6.tar.gz.asc     && tar -xf crate-5.4.6.tar.gz -C /crate --strip-components=1     && rm crate-5.4.6.tar.gz
# Tue, 05 Dec 2023 19:59:08 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 05 Dec 2023 19:59:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 19:59:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 05 Dec 2023 19:59:09 GMT
RUN mkdir -p /data/data /data/log
# Tue, 05 Dec 2023 19:59:09 GMT
VOLUME [/data]
# Tue, 05 Dec 2023 19:59:09 GMT
WORKDIR /data
# Tue, 05 Dec 2023 19:59:09 GMT
EXPOSE 4200 4300 5432
# Tue, 05 Dec 2023 19:59:09 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 05 Dec 2023 19:59:10 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 05 Dec 2023 19:59:10 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-11-30T13:48:50.915165 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.6
# Tue, 05 Dec 2023 19:59:10 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 05 Dec 2023 19:59:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:59:10 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c1500036e99b2f702d6379d090f3a4275a6e20d574bd82310d582cb60b2d1cf5`  
		Last Modified: Tue, 28 Nov 2023 23:43:55 GMT  
		Size: 67.1 MB (67090991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c229dddf1130365642b2edf5bbcf90362be62d41571e89dd36c74ef5831ba73f`  
		Last Modified: Wed, 29 Nov 2023 00:19:03 GMT  
		Size: 424.4 KB (424401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f976d4f47851d58234cac32b7a40bde19dac290762e464ffdbdf6cfaebba90`  
		Last Modified: Tue, 05 Dec 2023 20:00:06 GMT  
		Size: 227.9 MB (227888200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921ac46ffd5c8eaf082cf99c6f95afe5f92fdedd5178ac8617c3a2bda5ceaedb`  
		Last Modified: Tue, 05 Dec 2023 19:59:51 GMT  
		Size: 1.9 MB (1931727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565c8253aaeda8b727987070235211e31b2edea043514bb4d862746b74abb391`  
		Last Modified: Tue, 05 Dec 2023 19:59:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da09ce298d953ccea0a242b297fd88c00a90989d84b532a650afe2eb71bc5a2`  
		Last Modified: Tue, 05 Dec 2023 19:59:51 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b377ef953dbeca7a2cd31fda74da1b39842c631d79f285018bed8a4578359d10`  
		Last Modified: Tue, 05 Dec 2023 19:59:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d8c025fa9c73992359e82a532dadf7b13a38196b58d3d417a3122b2b70e100`  
		Last Modified: Tue, 05 Dec 2023 19:59:50 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.5`

```console
$ docker pull crate@sha256:a021eb33c93a2f5971482d2909c08328c21e5332b61122406a5201805c771aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.5` - linux; amd64

```console
$ docker pull crate@sha256:fa849e6f0b0ad647cf0ec35cdecbba65010466a33d262ee11227c0fc803f99e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186834922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3b36b991730c556cef17011b765b11cd770d0130455d1dc7c8ab8bb7ce9f0b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:48:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 05 Dec 2023 18:45:09 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.1.tar.gz.asc crate-5.5.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.1.tar.gz.asc     && tar -xf crate-5.5.1.tar.gz -C /crate --strip-components=1     && rm crate-5.5.1.tar.gz
# Tue, 05 Dec 2023 18:45:14 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 05 Dec 2023 18:45:14 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 18:45:14 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 05 Dec 2023 18:45:15 GMT
RUN mkdir -p /data/data /data/log
# Tue, 05 Dec 2023 18:45:15 GMT
VOLUME [/data]
# Tue, 05 Dec 2023 18:45:15 GMT
WORKDIR /data
# Tue, 05 Dec 2023 18:45:15 GMT
EXPOSE 4200 4300 5432
# Tue, 05 Dec 2023 18:45:15 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 05 Dec 2023 18:45:15 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 05 Dec 2023 18:45:15 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-11-30T15:07:15.982612 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.1
# Tue, 05 Dec 2023 18:45:16 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 05 Dec 2023 18:45:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 18:45:16 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:28130cb29ede9c7eb632516608f6be44c01d736736eb9f03846fb16c819426ae`  
		Last Modified: Tue, 28 Nov 2023 23:29:38 GMT  
		Size: 68.2 MB (68211613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474dd2aa9d062ecbc8a0eb11a10b354dea867214e1deec1655700136f902458e`  
		Last Modified: Tue, 28 Nov 2023 23:51:14 GMT  
		Size: 424.9 KB (424899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf2f6c9136cdcf1dc5ba701541575efaca1af3f1b788c6ff42f234b45a403de`  
		Last Modified: Tue, 05 Dec 2023 18:46:27 GMT  
		Size: 116.3 MB (116264793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899af45044bdaef382b30b6402e332276afe32c3300fd19c0e02183d5110f2c1`  
		Last Modified: Tue, 05 Dec 2023 18:46:17 GMT  
		Size: 1.9 MB (1931732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7e6edf18d3e6d56b01c244cbda768652f78084b2a861b22f91f390ca2442e1`  
		Last Modified: Tue, 05 Dec 2023 18:46:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab088500bd02789da3f0b4599c6ef8e307054bc6deddedf237d132d2add5cf2`  
		Last Modified: Tue, 05 Dec 2023 18:46:16 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a678bb9a6cfbbb0664334d1c78c6b44a679f01251aed34ce73d2a0b940dc95`  
		Last Modified: Tue, 05 Dec 2023 18:46:16 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4421ef744fcbd3d94586728c40d25fd66299442144669234e956ef2d7816d668`  
		Last Modified: Tue, 05 Dec 2023 18:46:17 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:36b996ce526ece98b24838ea5f90d645141ab897a1f80884e4ea36512c2c92ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185289559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f198fb3e11565edcd5bc1de31355378a0a3b209429b65fd062acbbab98ae8a8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 05 Dec 2023 19:58:33 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.1.tar.gz.asc crate-5.5.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.1.tar.gz.asc     && tar -xf crate-5.5.1.tar.gz -C /crate --strip-components=1     && rm crate-5.5.1.tar.gz
# Tue, 05 Dec 2023 19:58:36 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 05 Dec 2023 19:58:36 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 19:58:36 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 05 Dec 2023 19:58:36 GMT
RUN mkdir -p /data/data /data/log
# Tue, 05 Dec 2023 19:58:36 GMT
VOLUME [/data]
# Tue, 05 Dec 2023 19:58:36 GMT
WORKDIR /data
# Tue, 05 Dec 2023 19:58:36 GMT
EXPOSE 4200 4300 5432
# Tue, 05 Dec 2023 19:58:37 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 05 Dec 2023 19:58:37 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 05 Dec 2023 19:58:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-11-30T15:07:15.982612 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.1
# Tue, 05 Dec 2023 19:58:37 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 05 Dec 2023 19:58:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:58:37 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c1500036e99b2f702d6379d090f3a4275a6e20d574bd82310d582cb60b2d1cf5`  
		Last Modified: Tue, 28 Nov 2023 23:43:55 GMT  
		Size: 67.1 MB (67090991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c229dddf1130365642b2edf5bbcf90362be62d41571e89dd36c74ef5831ba73f`  
		Last Modified: Wed, 29 Nov 2023 00:19:03 GMT  
		Size: 424.4 KB (424401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6588a449ecb8b69496d6aebd3e16332f5e932f2894c3b4138135948853e214a0`  
		Last Modified: Tue, 05 Dec 2023 19:59:38 GMT  
		Size: 115.8 MB (115840560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8adfbc5d90a66c1b104a820ea0adea8e03ebb168f3699581d704a75dd2ef82`  
		Last Modified: Tue, 05 Dec 2023 19:59:30 GMT  
		Size: 1.9 MB (1931725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b17d0ab0def74db25e818b9238c113b0453045a580f1cfd181904c9e5d88451`  
		Last Modified: Tue, 05 Dec 2023 19:59:29 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738f0ee66d9b22f27447aa9c4c4a94813d593536c029ba74ca806e485b555b90`  
		Last Modified: Tue, 05 Dec 2023 19:59:29 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9738f7762829620158be7b8de49d61bd25a99cb6bfcb2d8871c1f67dbb9bc919`  
		Last Modified: Tue, 05 Dec 2023 19:59:29 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09314d41e3894c662e0fdc6bffdfb2f19a7b3f9aa9f45519a3b7e607af864e16`  
		Last Modified: Tue, 05 Dec 2023 19:59:29 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.5.1`

```console
$ docker pull crate@sha256:a021eb33c93a2f5971482d2909c08328c21e5332b61122406a5201805c771aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.5.1` - linux; amd64

```console
$ docker pull crate@sha256:fa849e6f0b0ad647cf0ec35cdecbba65010466a33d262ee11227c0fc803f99e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186834922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3b36b991730c556cef17011b765b11cd770d0130455d1dc7c8ab8bb7ce9f0b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:48:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 05 Dec 2023 18:45:09 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.1.tar.gz.asc crate-5.5.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.1.tar.gz.asc     && tar -xf crate-5.5.1.tar.gz -C /crate --strip-components=1     && rm crate-5.5.1.tar.gz
# Tue, 05 Dec 2023 18:45:14 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 05 Dec 2023 18:45:14 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 18:45:14 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 05 Dec 2023 18:45:15 GMT
RUN mkdir -p /data/data /data/log
# Tue, 05 Dec 2023 18:45:15 GMT
VOLUME [/data]
# Tue, 05 Dec 2023 18:45:15 GMT
WORKDIR /data
# Tue, 05 Dec 2023 18:45:15 GMT
EXPOSE 4200 4300 5432
# Tue, 05 Dec 2023 18:45:15 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 05 Dec 2023 18:45:15 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 05 Dec 2023 18:45:15 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-11-30T15:07:15.982612 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.1
# Tue, 05 Dec 2023 18:45:16 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 05 Dec 2023 18:45:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 18:45:16 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:28130cb29ede9c7eb632516608f6be44c01d736736eb9f03846fb16c819426ae`  
		Last Modified: Tue, 28 Nov 2023 23:29:38 GMT  
		Size: 68.2 MB (68211613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474dd2aa9d062ecbc8a0eb11a10b354dea867214e1deec1655700136f902458e`  
		Last Modified: Tue, 28 Nov 2023 23:51:14 GMT  
		Size: 424.9 KB (424899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf2f6c9136cdcf1dc5ba701541575efaca1af3f1b788c6ff42f234b45a403de`  
		Last Modified: Tue, 05 Dec 2023 18:46:27 GMT  
		Size: 116.3 MB (116264793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899af45044bdaef382b30b6402e332276afe32c3300fd19c0e02183d5110f2c1`  
		Last Modified: Tue, 05 Dec 2023 18:46:17 GMT  
		Size: 1.9 MB (1931732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7e6edf18d3e6d56b01c244cbda768652f78084b2a861b22f91f390ca2442e1`  
		Last Modified: Tue, 05 Dec 2023 18:46:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab088500bd02789da3f0b4599c6ef8e307054bc6deddedf237d132d2add5cf2`  
		Last Modified: Tue, 05 Dec 2023 18:46:16 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a678bb9a6cfbbb0664334d1c78c6b44a679f01251aed34ce73d2a0b940dc95`  
		Last Modified: Tue, 05 Dec 2023 18:46:16 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4421ef744fcbd3d94586728c40d25fd66299442144669234e956ef2d7816d668`  
		Last Modified: Tue, 05 Dec 2023 18:46:17 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.5.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:36b996ce526ece98b24838ea5f90d645141ab897a1f80884e4ea36512c2c92ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185289559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f198fb3e11565edcd5bc1de31355378a0a3b209429b65fd062acbbab98ae8a8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 05 Dec 2023 19:58:33 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.1.tar.gz.asc crate-5.5.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.1.tar.gz.asc     && tar -xf crate-5.5.1.tar.gz -C /crate --strip-components=1     && rm crate-5.5.1.tar.gz
# Tue, 05 Dec 2023 19:58:36 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 05 Dec 2023 19:58:36 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 19:58:36 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 05 Dec 2023 19:58:36 GMT
RUN mkdir -p /data/data /data/log
# Tue, 05 Dec 2023 19:58:36 GMT
VOLUME [/data]
# Tue, 05 Dec 2023 19:58:36 GMT
WORKDIR /data
# Tue, 05 Dec 2023 19:58:36 GMT
EXPOSE 4200 4300 5432
# Tue, 05 Dec 2023 19:58:37 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 05 Dec 2023 19:58:37 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 05 Dec 2023 19:58:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-11-30T15:07:15.982612 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.1
# Tue, 05 Dec 2023 19:58:37 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 05 Dec 2023 19:58:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:58:37 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c1500036e99b2f702d6379d090f3a4275a6e20d574bd82310d582cb60b2d1cf5`  
		Last Modified: Tue, 28 Nov 2023 23:43:55 GMT  
		Size: 67.1 MB (67090991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c229dddf1130365642b2edf5bbcf90362be62d41571e89dd36c74ef5831ba73f`  
		Last Modified: Wed, 29 Nov 2023 00:19:03 GMT  
		Size: 424.4 KB (424401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6588a449ecb8b69496d6aebd3e16332f5e932f2894c3b4138135948853e214a0`  
		Last Modified: Tue, 05 Dec 2023 19:59:38 GMT  
		Size: 115.8 MB (115840560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8adfbc5d90a66c1b104a820ea0adea8e03ebb168f3699581d704a75dd2ef82`  
		Last Modified: Tue, 05 Dec 2023 19:59:30 GMT  
		Size: 1.9 MB (1931725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b17d0ab0def74db25e818b9238c113b0453045a580f1cfd181904c9e5d88451`  
		Last Modified: Tue, 05 Dec 2023 19:59:29 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738f0ee66d9b22f27447aa9c4c4a94813d593536c029ba74ca806e485b555b90`  
		Last Modified: Tue, 05 Dec 2023 19:59:29 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9738f7762829620158be7b8de49d61bd25a99cb6bfcb2d8871c1f67dbb9bc919`  
		Last Modified: Tue, 05 Dec 2023 19:59:29 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09314d41e3894c662e0fdc6bffdfb2f19a7b3f9aa9f45519a3b7e607af864e16`  
		Last Modified: Tue, 05 Dec 2023 19:59:29 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:latest`

```console
$ docker pull crate@sha256:a021eb33c93a2f5971482d2909c08328c21e5332b61122406a5201805c771aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:fa849e6f0b0ad647cf0ec35cdecbba65010466a33d262ee11227c0fc803f99e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186834922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3b36b991730c556cef17011b765b11cd770d0130455d1dc7c8ab8bb7ce9f0b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:48:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 05 Dec 2023 18:45:09 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.1.tar.gz.asc crate-5.5.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.1.tar.gz.asc     && tar -xf crate-5.5.1.tar.gz -C /crate --strip-components=1     && rm crate-5.5.1.tar.gz
# Tue, 05 Dec 2023 18:45:14 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 05 Dec 2023 18:45:14 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 18:45:14 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 05 Dec 2023 18:45:15 GMT
RUN mkdir -p /data/data /data/log
# Tue, 05 Dec 2023 18:45:15 GMT
VOLUME [/data]
# Tue, 05 Dec 2023 18:45:15 GMT
WORKDIR /data
# Tue, 05 Dec 2023 18:45:15 GMT
EXPOSE 4200 4300 5432
# Tue, 05 Dec 2023 18:45:15 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 05 Dec 2023 18:45:15 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 05 Dec 2023 18:45:15 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-11-30T15:07:15.982612 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.1
# Tue, 05 Dec 2023 18:45:16 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 05 Dec 2023 18:45:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 18:45:16 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:28130cb29ede9c7eb632516608f6be44c01d736736eb9f03846fb16c819426ae`  
		Last Modified: Tue, 28 Nov 2023 23:29:38 GMT  
		Size: 68.2 MB (68211613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474dd2aa9d062ecbc8a0eb11a10b354dea867214e1deec1655700136f902458e`  
		Last Modified: Tue, 28 Nov 2023 23:51:14 GMT  
		Size: 424.9 KB (424899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf2f6c9136cdcf1dc5ba701541575efaca1af3f1b788c6ff42f234b45a403de`  
		Last Modified: Tue, 05 Dec 2023 18:46:27 GMT  
		Size: 116.3 MB (116264793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899af45044bdaef382b30b6402e332276afe32c3300fd19c0e02183d5110f2c1`  
		Last Modified: Tue, 05 Dec 2023 18:46:17 GMT  
		Size: 1.9 MB (1931732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7e6edf18d3e6d56b01c244cbda768652f78084b2a861b22f91f390ca2442e1`  
		Last Modified: Tue, 05 Dec 2023 18:46:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab088500bd02789da3f0b4599c6ef8e307054bc6deddedf237d132d2add5cf2`  
		Last Modified: Tue, 05 Dec 2023 18:46:16 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a678bb9a6cfbbb0664334d1c78c6b44a679f01251aed34ce73d2a0b940dc95`  
		Last Modified: Tue, 05 Dec 2023 18:46:16 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4421ef744fcbd3d94586728c40d25fd66299442144669234e956ef2d7816d668`  
		Last Modified: Tue, 05 Dec 2023 18:46:17 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:36b996ce526ece98b24838ea5f90d645141ab897a1f80884e4ea36512c2c92ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185289559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f198fb3e11565edcd5bc1de31355378a0a3b209429b65fd062acbbab98ae8a8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Tue, 05 Dec 2023 19:58:33 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.1.tar.gz.asc crate-5.5.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.1.tar.gz.asc     && tar -xf crate-5.5.1.tar.gz -C /crate --strip-components=1     && rm crate-5.5.1.tar.gz
# Tue, 05 Dec 2023 19:58:36 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.0.asc crash_standalone_0.30.0     && rm -rf "$GNUPGHOME" crash_standalone_0.30.0.asc     && mv crash_standalone_0.30.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 05 Dec 2023 19:58:36 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 19:58:36 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 05 Dec 2023 19:58:36 GMT
RUN mkdir -p /data/data /data/log
# Tue, 05 Dec 2023 19:58:36 GMT
VOLUME [/data]
# Tue, 05 Dec 2023 19:58:36 GMT
WORKDIR /data
# Tue, 05 Dec 2023 19:58:36 GMT
EXPOSE 4200 4300 5432
# Tue, 05 Dec 2023 19:58:37 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 05 Dec 2023 19:58:37 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 05 Dec 2023 19:58:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-11-30T15:07:15.982612 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.1
# Tue, 05 Dec 2023 19:58:37 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Tue, 05 Dec 2023 19:58:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:58:37 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c1500036e99b2f702d6379d090f3a4275a6e20d574bd82310d582cb60b2d1cf5`  
		Last Modified: Tue, 28 Nov 2023 23:43:55 GMT  
		Size: 67.1 MB (67090991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c229dddf1130365642b2edf5bbcf90362be62d41571e89dd36c74ef5831ba73f`  
		Last Modified: Wed, 29 Nov 2023 00:19:03 GMT  
		Size: 424.4 KB (424401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6588a449ecb8b69496d6aebd3e16332f5e932f2894c3b4138135948853e214a0`  
		Last Modified: Tue, 05 Dec 2023 19:59:38 GMT  
		Size: 115.8 MB (115840560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8adfbc5d90a66c1b104a820ea0adea8e03ebb168f3699581d704a75dd2ef82`  
		Last Modified: Tue, 05 Dec 2023 19:59:30 GMT  
		Size: 1.9 MB (1931725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b17d0ab0def74db25e818b9238c113b0453045a580f1cfd181904c9e5d88451`  
		Last Modified: Tue, 05 Dec 2023 19:59:29 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738f0ee66d9b22f27447aa9c4c4a94813d593536c029ba74ca806e485b555b90`  
		Last Modified: Tue, 05 Dec 2023 19:59:29 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9738f7762829620158be7b8de49d61bd25a99cb6bfcb2d8871c1f67dbb9bc919`  
		Last Modified: Tue, 05 Dec 2023 19:59:29 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09314d41e3894c662e0fdc6bffdfb2f19a7b3f9aa9f45519a3b7e607af864e16`  
		Last Modified: Tue, 05 Dec 2023 19:59:29 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
