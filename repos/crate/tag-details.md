<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:4.8`](#crate48)
-	[`crate:4.8.4`](#crate484)
-	[`crate:5.2`](#crate52)
-	[`crate:5.2.11`](#crate5211)
-	[`crate:5.3`](#crate53)
-	[`crate:5.3.9`](#crate539)
-	[`crate:5.4`](#crate54)
-	[`crate:5.4.8`](#crate548)
-	[`crate:5.5`](#crate55)
-	[`crate:5.5.5`](#crate555)
-	[`crate:5.6`](#crate56)
-	[`crate:5.6.1`](#crate561)
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
$ docker pull crate@sha256:fa88219443f9b3b4a07c6b990bf8da3cebaafce74ab18430c2567eb1c8be2965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.2` - linux; amd64

```console
$ docker pull crate@sha256:dcd0b77639efc8bda4c180d156cafca573bff7c6a44077a578fe7d5ada4938b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304918286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8022b1f51efe59386add96fe0bfc66fb9d01f34f1a136882d96be289f8a6241d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:50:24 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python3 python3-pip     && yum clean all     && rm -rf /var/cache/yum
# Fri, 22 Dec 2023 17:41:33 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.2.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.2.11.tar.gz.asc crate-5.2.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.2.11.tar.gz.asc     && tar -xf crate-5.2.11.tar.gz -C /crate --strip-components=1     && rm crate-5.2.11.tar.gz
# Fri, 22 Dec 2023 17:41:36 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.1     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.1.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.1.asc crash_standalone_0.30.1     && rm -rf "$GNUPGHOME" crash_standalone_0.30.1.asc     && mv crash_standalone_0.30.1 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 22 Dec 2023 17:41:36 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 17:41:36 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 22 Dec 2023 17:41:36 GMT
RUN mkdir -p /data/data /data/log
# Fri, 22 Dec 2023 17:41:37 GMT
VOLUME [/data]
# Fri, 22 Dec 2023 17:41:37 GMT
WORKDIR /data
# Fri, 22 Dec 2023 17:41:37 GMT
EXPOSE 4200 4300 5432
# Fri, 22 Dec 2023 17:41:37 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 22 Dec 2023 17:41:37 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 22 Dec 2023 17:41:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-12-21T22:23:59.881502 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.2.11
# Fri, 22 Dec 2023 17:41:37 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 22 Dec 2023 17:41:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 Dec 2023 17:41:37 GMT
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
	-	`sha256:73998c67972394f920e394236c9b6e646b47915c9835233fb40a7d60b606ea17`  
		Last Modified: Fri, 22 Dec 2023 17:43:30 GMT  
		Size: 227.1 MB (227118338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed06fd9479549db9babc3bd5defd2c4cd929404ba7f00564842f3e0331829e89`  
		Last Modified: Fri, 22 Dec 2023 17:43:13 GMT  
		Size: 2.0 MB (1954459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ad2d48901b62d452ebfdf1181fd2f3e5929c3d42fe64812e16e2ff0afc0c3f`  
		Last Modified: Fri, 22 Dec 2023 17:43:12 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71369e426eb744876fb67e6575ffd40a46f9c61b54a7b8aab4b24c8d3df6ce7c`  
		Last Modified: Fri, 22 Dec 2023 17:43:12 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bbf37580501f74d7d667b58a903c1118c94b1b5a4eb59d9e3acc503f4b4160`  
		Last Modified: Fri, 22 Dec 2023 17:43:12 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b493fd7210360356b806e897499106d909fd707bca5e7be77de17de883fbb8b2`  
		Last Modified: Fri, 22 Dec 2023 17:43:12 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:bb2cc3511fc0db954f3633003f999cd13ad856b1d718d598a7f730422b8a0d25
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302386287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288f24a8752e7a8a6483216aabc514a711d6c87c3d6a907929a42b75b42147ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:18:09 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python3 python3-pip     && yum clean all     && rm -rf /var/cache/yum
# Fri, 22 Dec 2023 16:42:22 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.2.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.2.11.tar.gz.asc crate-5.2.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.2.11.tar.gz.asc     && tar -xf crate-5.2.11.tar.gz -C /crate --strip-components=1     && rm crate-5.2.11.tar.gz
# Fri, 22 Dec 2023 16:42:26 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.1     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.1.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.1.asc crash_standalone_0.30.1     && rm -rf "$GNUPGHOME" crash_standalone_0.30.1.asc     && mv crash_standalone_0.30.1 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 22 Dec 2023 16:42:26 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 16:42:26 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 22 Dec 2023 16:42:27 GMT
RUN mkdir -p /data/data /data/log
# Fri, 22 Dec 2023 16:42:27 GMT
VOLUME [/data]
# Fri, 22 Dec 2023 16:42:27 GMT
WORKDIR /data
# Fri, 22 Dec 2023 16:42:27 GMT
EXPOSE 4200 4300 5432
# Fri, 22 Dec 2023 16:42:27 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 22 Dec 2023 16:42:27 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 22 Dec 2023 16:42:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-12-21T22:23:59.881502 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.2.11
# Fri, 22 Dec 2023 16:42:27 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 22 Dec 2023 16:42:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 Dec 2023 16:42:27 GMT
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
	-	`sha256:076fbd85ac340b0ce200b8a8d8e3f96994f244e6befdad5f45640f68e8388b12`  
		Last Modified: Fri, 22 Dec 2023 16:44:12 GMT  
		Size: 225.9 MB (225862476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8248ae993931cc052ef49a06139081896f10ab57e30f8f04b4b716c1853c9b8c`  
		Last Modified: Fri, 22 Dec 2023 16:43:57 GMT  
		Size: 2.0 MB (1954468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb53d8c3574a537d8ed8374bd27619066a0f2378ed505693916c45dccd21130`  
		Last Modified: Fri, 22 Dec 2023 16:43:57 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a9e523c7020d1d30f760dd234f14a9feedc6341569d0a1a386bbc2056cd582`  
		Last Modified: Fri, 22 Dec 2023 16:43:56 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac66466fcbd874375b213152887c029161d6b961455e397bc5fa7b4abe090251`  
		Last Modified: Fri, 22 Dec 2023 16:43:57 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3552d95f911a73741d911a7c58a437bc8b5b4a07784bd95323ae649418c426c`  
		Last Modified: Fri, 22 Dec 2023 16:43:57 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.2.11`

```console
$ docker pull crate@sha256:fa88219443f9b3b4a07c6b990bf8da3cebaafce74ab18430c2567eb1c8be2965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.2.11` - linux; amd64

```console
$ docker pull crate@sha256:dcd0b77639efc8bda4c180d156cafca573bff7c6a44077a578fe7d5ada4938b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304918286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8022b1f51efe59386add96fe0bfc66fb9d01f34f1a136882d96be289f8a6241d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:50:24 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python3 python3-pip     && yum clean all     && rm -rf /var/cache/yum
# Fri, 22 Dec 2023 17:41:33 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.2.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.2.11.tar.gz.asc crate-5.2.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.2.11.tar.gz.asc     && tar -xf crate-5.2.11.tar.gz -C /crate --strip-components=1     && rm crate-5.2.11.tar.gz
# Fri, 22 Dec 2023 17:41:36 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.1     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.1.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.1.asc crash_standalone_0.30.1     && rm -rf "$GNUPGHOME" crash_standalone_0.30.1.asc     && mv crash_standalone_0.30.1 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 22 Dec 2023 17:41:36 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 17:41:36 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 22 Dec 2023 17:41:36 GMT
RUN mkdir -p /data/data /data/log
# Fri, 22 Dec 2023 17:41:37 GMT
VOLUME [/data]
# Fri, 22 Dec 2023 17:41:37 GMT
WORKDIR /data
# Fri, 22 Dec 2023 17:41:37 GMT
EXPOSE 4200 4300 5432
# Fri, 22 Dec 2023 17:41:37 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 22 Dec 2023 17:41:37 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 22 Dec 2023 17:41:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-12-21T22:23:59.881502 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.2.11
# Fri, 22 Dec 2023 17:41:37 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 22 Dec 2023 17:41:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 Dec 2023 17:41:37 GMT
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
	-	`sha256:73998c67972394f920e394236c9b6e646b47915c9835233fb40a7d60b606ea17`  
		Last Modified: Fri, 22 Dec 2023 17:43:30 GMT  
		Size: 227.1 MB (227118338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed06fd9479549db9babc3bd5defd2c4cd929404ba7f00564842f3e0331829e89`  
		Last Modified: Fri, 22 Dec 2023 17:43:13 GMT  
		Size: 2.0 MB (1954459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ad2d48901b62d452ebfdf1181fd2f3e5929c3d42fe64812e16e2ff0afc0c3f`  
		Last Modified: Fri, 22 Dec 2023 17:43:12 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71369e426eb744876fb67e6575ffd40a46f9c61b54a7b8aab4b24c8d3df6ce7c`  
		Last Modified: Fri, 22 Dec 2023 17:43:12 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bbf37580501f74d7d667b58a903c1118c94b1b5a4eb59d9e3acc503f4b4160`  
		Last Modified: Fri, 22 Dec 2023 17:43:12 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b493fd7210360356b806e897499106d909fd707bca5e7be77de17de883fbb8b2`  
		Last Modified: Fri, 22 Dec 2023 17:43:12 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.2.11` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:bb2cc3511fc0db954f3633003f999cd13ad856b1d718d598a7f730422b8a0d25
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302386287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288f24a8752e7a8a6483216aabc514a711d6c87c3d6a907929a42b75b42147ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:18:09 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python3 python3-pip     && yum clean all     && rm -rf /var/cache/yum
# Fri, 22 Dec 2023 16:42:22 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.2.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.2.11.tar.gz.asc crate-5.2.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.2.11.tar.gz.asc     && tar -xf crate-5.2.11.tar.gz -C /crate --strip-components=1     && rm crate-5.2.11.tar.gz
# Fri, 22 Dec 2023 16:42:26 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.1     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.1.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.1.asc crash_standalone_0.30.1     && rm -rf "$GNUPGHOME" crash_standalone_0.30.1.asc     && mv crash_standalone_0.30.1 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 22 Dec 2023 16:42:26 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 16:42:26 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 22 Dec 2023 16:42:27 GMT
RUN mkdir -p /data/data /data/log
# Fri, 22 Dec 2023 16:42:27 GMT
VOLUME [/data]
# Fri, 22 Dec 2023 16:42:27 GMT
WORKDIR /data
# Fri, 22 Dec 2023 16:42:27 GMT
EXPOSE 4200 4300 5432
# Fri, 22 Dec 2023 16:42:27 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 22 Dec 2023 16:42:27 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 22 Dec 2023 16:42:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-12-21T22:23:59.881502 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.2.11
# Fri, 22 Dec 2023 16:42:27 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 22 Dec 2023 16:42:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 Dec 2023 16:42:27 GMT
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
	-	`sha256:076fbd85ac340b0ce200b8a8d8e3f96994f244e6befdad5f45640f68e8388b12`  
		Last Modified: Fri, 22 Dec 2023 16:44:12 GMT  
		Size: 225.9 MB (225862476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8248ae993931cc052ef49a06139081896f10ab57e30f8f04b4b716c1853c9b8c`  
		Last Modified: Fri, 22 Dec 2023 16:43:57 GMT  
		Size: 2.0 MB (1954468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb53d8c3574a537d8ed8374bd27619066a0f2378ed505693916c45dccd21130`  
		Last Modified: Fri, 22 Dec 2023 16:43:57 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a9e523c7020d1d30f760dd234f14a9feedc6341569d0a1a386bbc2056cd582`  
		Last Modified: Fri, 22 Dec 2023 16:43:56 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac66466fcbd874375b213152887c029161d6b961455e397bc5fa7b4abe090251`  
		Last Modified: Fri, 22 Dec 2023 16:43:57 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3552d95f911a73741d911a7c58a437bc8b5b4a07784bd95323ae649418c426c`  
		Last Modified: Fri, 22 Dec 2023 16:43:57 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.3`

```console
$ docker pull crate@sha256:2efc665ae8628c3013f3ee5ff22115934b89d333b6d2c12ea103b5e16bc9ddd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.3` - linux; amd64

```console
$ docker pull crate@sha256:72e1762efa5499cfa2f443e223f6f007fae992959c8a196701f3537f847ea32a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297930729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2ec8f908d3c36d86b9e00ed4945da77f2b2c26a799b4e9e84d26dd9055e43d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:48:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 22 Dec 2023 17:41:05 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.8.tar.gz.asc crate-5.3.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.8.tar.gz.asc     && tar -xf crate-5.3.8.tar.gz -C /crate --strip-components=1     && rm crate-5.3.8.tar.gz
# Fri, 22 Dec 2023 17:41:07 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.1     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.1.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.1.asc crash_standalone_0.30.1     && rm -rf "$GNUPGHOME" crash_standalone_0.30.1.asc     && mv crash_standalone_0.30.1 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 22 Dec 2023 17:41:07 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 17:41:07 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 22 Dec 2023 17:41:08 GMT
RUN mkdir -p /data/data /data/log
# Fri, 22 Dec 2023 17:41:08 GMT
VOLUME [/data]
# Fri, 22 Dec 2023 17:41:08 GMT
WORKDIR /data
# Fri, 22 Dec 2023 17:41:08 GMT
EXPOSE 4200 4300 5432
# Fri, 22 Dec 2023 17:41:08 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 22 Dec 2023 17:41:08 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 22 Dec 2023 17:41:08 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-12-21T21:59:09.428079 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.8
# Fri, 22 Dec 2023 17:41:08 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 22 Dec 2023 17:41:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 Dec 2023 17:41:09 GMT
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
	-	`sha256:ed71ed73d6d1e26b4598b27b6922a6dabb37dd18424875e3d4f9396abc851496`  
		Last Modified: Fri, 22 Dec 2023 17:43:03 GMT  
		Size: 227.3 MB (227337865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50efcce8b61ca8721ce1b2d5e24b2984385a945b1833478feb64b1d472f858a2`  
		Last Modified: Fri, 22 Dec 2023 17:42:45 GMT  
		Size: 2.0 MB (1954468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560afeeb50a963e328a353e75774e126d19b86475bdc6170cd6621d085711ab8`  
		Last Modified: Fri, 22 Dec 2023 17:42:44 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a9600ce990081a75d9ecc807b9e48bac0bf83f7c894a1290e13b60801071be`  
		Last Modified: Fri, 22 Dec 2023 17:42:44 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c529bd8d4f7f31fbe1aa5a635b231ad311bb88d524d300e46c39374b63ecbf39`  
		Last Modified: Fri, 22 Dec 2023 17:42:44 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfa368687e761bb921f314720c3f369725dd4acd812eaf49b02369217424e63`  
		Last Modified: Fri, 22 Dec 2023 17:42:44 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:0c29c3e17566fadf09d35b8d5f4ecf9410dafcb0e80aea3e48810375cabdae5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295536528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fb0ad923d19a2647a002b8ce21fb25cac8786c7c841bccf4454c349acda22d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 02 Feb 2024 19:41:09 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.9.tar.gz.asc crate-5.3.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.9.tar.gz.asc     && tar -xf crate-5.3.9.tar.gz -C /crate --strip-components=1     && rm crate-5.3.9.tar.gz
# Fri, 02 Feb 2024 19:41:13 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 02 Feb 2024 19:41:13 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:41:13 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 02 Feb 2024 19:41:14 GMT
RUN mkdir -p /data/data /data/log
# Fri, 02 Feb 2024 19:41:14 GMT
VOLUME [/data]
# Fri, 02 Feb 2024 19:41:14 GMT
WORKDIR /data
# Fri, 02 Feb 2024 19:41:14 GMT
EXPOSE 4200 4300 5432
# Fri, 02 Feb 2024 19:41:14 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 02 Feb 2024 19:41:14 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 02 Feb 2024 19:41:14 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:21:10.551998 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.9
# Fri, 02 Feb 2024 19:41:14 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 02 Feb 2024 19:41:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 19:41:15 GMT
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
	-	`sha256:7008b21a36f59421aa34b5133880f8db55f991c3c0c17010304f230f8e2d80a3`  
		Last Modified: Fri, 02 Feb 2024 19:42:57 GMT  
		Size: 226.1 MB (226079639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0649b35fe65ab29e8b2bdcfd5d93751391fee7cbffc92fdc42e4a5dd1585e6e4`  
		Last Modified: Fri, 02 Feb 2024 19:42:41 GMT  
		Size: 1.9 MB (1939617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc18d454ce9a92375340eab0386c1429deb281023c7d51acf41a0f9046ff3903`  
		Last Modified: Fri, 02 Feb 2024 19:42:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996563eac46296a062dc9296c1aa1c86dc89618a53e0b2827244270cc33fdff8`  
		Last Modified: Fri, 02 Feb 2024 19:42:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebc3e2f14052597c0e820b9029163e938225645f4938d83f90cb3db500eabba`  
		Last Modified: Fri, 02 Feb 2024 19:42:41 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70acc361644181c57fefbabfa6a3c2d7ca1f9495fd82516f53db8aca79116b45`  
		Last Modified: Fri, 02 Feb 2024 19:42:41 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.3.9`

```console
$ docker pull crate@sha256:e2c9385e9eb0c43bd3d248d9413e6fba3d5ae7612a8ea2ff10ec9761768f6c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `crate:5.3.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:0c29c3e17566fadf09d35b8d5f4ecf9410dafcb0e80aea3e48810375cabdae5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295536528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fb0ad923d19a2647a002b8ce21fb25cac8786c7c841bccf4454c349acda22d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 02 Feb 2024 19:41:09 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.9.tar.gz.asc crate-5.3.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.9.tar.gz.asc     && tar -xf crate-5.3.9.tar.gz -C /crate --strip-components=1     && rm crate-5.3.9.tar.gz
# Fri, 02 Feb 2024 19:41:13 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 02 Feb 2024 19:41:13 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:41:13 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 02 Feb 2024 19:41:14 GMT
RUN mkdir -p /data/data /data/log
# Fri, 02 Feb 2024 19:41:14 GMT
VOLUME [/data]
# Fri, 02 Feb 2024 19:41:14 GMT
WORKDIR /data
# Fri, 02 Feb 2024 19:41:14 GMT
EXPOSE 4200 4300 5432
# Fri, 02 Feb 2024 19:41:14 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 02 Feb 2024 19:41:14 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 02 Feb 2024 19:41:14 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:21:10.551998 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.9
# Fri, 02 Feb 2024 19:41:14 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 02 Feb 2024 19:41:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 19:41:15 GMT
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
	-	`sha256:7008b21a36f59421aa34b5133880f8db55f991c3c0c17010304f230f8e2d80a3`  
		Last Modified: Fri, 02 Feb 2024 19:42:57 GMT  
		Size: 226.1 MB (226079639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0649b35fe65ab29e8b2bdcfd5d93751391fee7cbffc92fdc42e4a5dd1585e6e4`  
		Last Modified: Fri, 02 Feb 2024 19:42:41 GMT  
		Size: 1.9 MB (1939617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc18d454ce9a92375340eab0386c1429deb281023c7d51acf41a0f9046ff3903`  
		Last Modified: Fri, 02 Feb 2024 19:42:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996563eac46296a062dc9296c1aa1c86dc89618a53e0b2827244270cc33fdff8`  
		Last Modified: Fri, 02 Feb 2024 19:42:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebc3e2f14052597c0e820b9029163e938225645f4938d83f90cb3db500eabba`  
		Last Modified: Fri, 02 Feb 2024 19:42:41 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70acc361644181c57fefbabfa6a3c2d7ca1f9495fd82516f53db8aca79116b45`  
		Last Modified: Fri, 02 Feb 2024 19:42:41 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.4`

```console
$ docker pull crate@sha256:632cd0d2781bccc48a0bab4a4bca606f62980b9d1721f8a83be4dc328a4e0db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.4` - linux; amd64

```console
$ docker pull crate@sha256:a8b52e1622cd8f696501beda0f0b0407c2de2204fc7981aa6982e63ae71d1ed0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.2 MB (300153147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b935eaf0589e861bfdf0e1376f93ff4e691ac40f3105e34d3ff32c7b1969db2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:48:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 22 Dec 2023 17:40:31 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.7.tar.gz.asc crate-5.4.7.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.7.tar.gz.asc     && tar -xf crate-5.4.7.tar.gz -C /crate --strip-components=1     && rm crate-5.4.7.tar.gz
# Fri, 22 Dec 2023 17:40:33 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.1     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.1.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.1.asc crash_standalone_0.30.1     && rm -rf "$GNUPGHOME" crash_standalone_0.30.1.asc     && mv crash_standalone_0.30.1 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 22 Dec 2023 17:40:33 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 17:40:33 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 22 Dec 2023 17:40:34 GMT
RUN mkdir -p /data/data /data/log
# Fri, 22 Dec 2023 17:40:34 GMT
VOLUME [/data]
# Fri, 22 Dec 2023 17:40:34 GMT
WORKDIR /data
# Fri, 22 Dec 2023 17:40:34 GMT
EXPOSE 4200 4300 5432
# Fri, 22 Dec 2023 17:40:34 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 22 Dec 2023 17:40:34 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 22 Dec 2023 17:40:35 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-12-21T20:14:00.920830 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.7
# Fri, 22 Dec 2023 17:40:35 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 22 Dec 2023 17:40:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 Dec 2023 17:40:35 GMT
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
	-	`sha256:7f4a11d5a208146a1413c9312b8b3ae9f0f743a8b8bf0b37860e7a1739061195`  
		Last Modified: Fri, 22 Dec 2023 17:42:33 GMT  
		Size: 229.6 MB (229560285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fdc87f9d3fedec199722b8607a5d9cde2f0ab32c23ecc03b96836be6e96dc0`  
		Last Modified: Fri, 22 Dec 2023 17:42:14 GMT  
		Size: 2.0 MB (1954464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ef12cc24ad2ec045f074030e945d692bcb1263feed8007276d1e4d1644bbfa`  
		Last Modified: Fri, 22 Dec 2023 17:42:14 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3063c57af558a333b596b3435a5e77c6bc5781cd806f2a51aa4db7e6617f81b5`  
		Last Modified: Fri, 22 Dec 2023 17:42:14 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5181a3aab72f48b38612daa5c8e5886690dff2fea350666861f2acd445c3c2`  
		Last Modified: Fri, 22 Dec 2023 17:42:14 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdacf193b85cff32dca85888845f02652365f9cd33bec411d217105cb1ae80ae`  
		Last Modified: Fri, 22 Dec 2023 17:42:14 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:d656c986391c85c05aff68cf1198367c555f91116fd4bd16e807103d42bbfc6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297345377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf3aea2585b5a7a1ae7cc979cd7645a8e022492d3ea863a728853130a07f392`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 02 Feb 2024 19:40:36 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Fri, 02 Feb 2024 19:40:40 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 02 Feb 2024 19:40:40 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:40:40 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 02 Feb 2024 19:40:40 GMT
RUN mkdir -p /data/data /data/log
# Fri, 02 Feb 2024 19:40:41 GMT
VOLUME [/data]
# Fri, 02 Feb 2024 19:40:41 GMT
WORKDIR /data
# Fri, 02 Feb 2024 19:40:41 GMT
EXPOSE 4200 4300 5432
# Fri, 02 Feb 2024 19:40:41 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 02 Feb 2024 19:40:41 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 02 Feb 2024 19:40:41 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Fri, 02 Feb 2024 19:40:41 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 02 Feb 2024 19:40:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 19:40:41 GMT
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
	-	`sha256:2e68902d7118bd0caf3a08e52244bb28722abc67a641cad543fb4fddc629c84b`  
		Last Modified: Fri, 02 Feb 2024 19:42:31 GMT  
		Size: 227.9 MB (227888484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26063e3be7e402998d414a768e4b0c3e99888b581600a175f8119a409d1af422`  
		Last Modified: Fri, 02 Feb 2024 19:42:16 GMT  
		Size: 1.9 MB (1939619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3562c2eff4166f9dceb602d682d97d03e0a789da6e2fbf568b5df7e227e44c80`  
		Last Modified: Fri, 02 Feb 2024 19:42:15 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a4ff9f5ac4c419037c9b3bf868889cf4f518f70a090e0497a2946025e4907b`  
		Last Modified: Fri, 02 Feb 2024 19:42:15 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0d01738270dd5442d8f1ae77834531c8594f37b5fe4970f4e90dba00d62eff`  
		Last Modified: Fri, 02 Feb 2024 19:42:15 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab623f974e09f711c789fdde33ca0037c53c22ed52e6fdea011b836cdd3d5b5c`  
		Last Modified: Fri, 02 Feb 2024 19:42:16 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.4.8`

```console
$ docker pull crate@sha256:aef7eaad90167e1d07bd2ecaadc09bb2cee38d2305a5244abbfafe36ed44f32f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `crate:5.4.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:d656c986391c85c05aff68cf1198367c555f91116fd4bd16e807103d42bbfc6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297345377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf3aea2585b5a7a1ae7cc979cd7645a8e022492d3ea863a728853130a07f392`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 02 Feb 2024 19:40:36 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Fri, 02 Feb 2024 19:40:40 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 02 Feb 2024 19:40:40 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:40:40 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 02 Feb 2024 19:40:40 GMT
RUN mkdir -p /data/data /data/log
# Fri, 02 Feb 2024 19:40:41 GMT
VOLUME [/data]
# Fri, 02 Feb 2024 19:40:41 GMT
WORKDIR /data
# Fri, 02 Feb 2024 19:40:41 GMT
EXPOSE 4200 4300 5432
# Fri, 02 Feb 2024 19:40:41 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 02 Feb 2024 19:40:41 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 02 Feb 2024 19:40:41 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Fri, 02 Feb 2024 19:40:41 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 02 Feb 2024 19:40:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 19:40:41 GMT
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
	-	`sha256:2e68902d7118bd0caf3a08e52244bb28722abc67a641cad543fb4fddc629c84b`  
		Last Modified: Fri, 02 Feb 2024 19:42:31 GMT  
		Size: 227.9 MB (227888484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26063e3be7e402998d414a768e4b0c3e99888b581600a175f8119a409d1af422`  
		Last Modified: Fri, 02 Feb 2024 19:42:16 GMT  
		Size: 1.9 MB (1939619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3562c2eff4166f9dceb602d682d97d03e0a789da6e2fbf568b5df7e227e44c80`  
		Last Modified: Fri, 02 Feb 2024 19:42:15 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a4ff9f5ac4c419037c9b3bf868889cf4f518f70a090e0497a2946025e4907b`  
		Last Modified: Fri, 02 Feb 2024 19:42:15 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0d01738270dd5442d8f1ae77834531c8594f37b5fe4970f4e90dba00d62eff`  
		Last Modified: Fri, 02 Feb 2024 19:42:15 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab623f974e09f711c789fdde33ca0037c53c22ed52e6fdea011b836cdd3d5b5c`  
		Last Modified: Fri, 02 Feb 2024 19:42:16 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.5`

```console
$ docker pull crate@sha256:72280e7ae6813493666d5cf169baf562ed75d37d81ac132967dc2cfe252c06a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.5` - linux; amd64

```console
$ docker pull crate@sha256:9f958a830953682f4ccd11af8ea934fb792629b6be73e8d3a41ddc5f820a5a88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186870503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f86ee3cb3413e75940da34eb557c55868f9d3ff2053a981782b9694ec91b821`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:48:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 22 Jan 2024 19:38:31 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.3.tar.gz.asc crate-5.5.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.3.tar.gz.asc     && tar -xf crate-5.5.3.tar.gz -C /crate --strip-components=1     && rm crate-5.5.3.tar.gz
# Mon, 22 Jan 2024 19:38:35 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.1     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.1.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.1.asc crash_standalone_0.30.1     && rm -rf "$GNUPGHOME" crash_standalone_0.30.1.asc     && mv crash_standalone_0.30.1 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 22 Jan 2024 19:38:35 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:38:35 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 22 Jan 2024 19:38:35 GMT
RUN mkdir -p /data/data /data/log
# Mon, 22 Jan 2024 19:38:35 GMT
VOLUME [/data]
# Mon, 22 Jan 2024 19:38:35 GMT
WORKDIR /data
# Mon, 22 Jan 2024 19:38:36 GMT
EXPOSE 4200 4300 5432
# Mon, 22 Jan 2024 19:38:36 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 22 Jan 2024 19:38:36 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 22 Jan 2024 19:38:36 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-17T13:51:08.432216 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.3
# Mon, 22 Jan 2024 19:38:36 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 22 Jan 2024 19:38:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:38:36 GMT
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
	-	`sha256:85f91ae4aa845d750268f9dab72264048a18c127e675954cc679ddcda1687a74`  
		Last Modified: Mon, 22 Jan 2024 19:39:11 GMT  
		Size: 116.3 MB (116277645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85a2368f5ae7b63abaccaa819c7f69cb3f68493079e438552c01fcecc82505`  
		Last Modified: Mon, 22 Jan 2024 19:39:00 GMT  
		Size: 2.0 MB (1954466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b33fda5199736a83b1af39bb08eb6e5e9ec4b9be4ae967e9b0dfb1d937c4a4`  
		Last Modified: Mon, 22 Jan 2024 19:38:59 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba12b4c41f7801f96610e4e9730bcd4ff7a36a7585c1d3288ad37cb18d33bab5`  
		Last Modified: Mon, 22 Jan 2024 19:38:59 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72532fc3f5543c472e129c401709aeac24a359be79725784bba85fc0f67e530b`  
		Last Modified: Mon, 22 Jan 2024 19:38:59 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6251c14959303ad5d41eb604b503f6ec87894ab0b408e4f8a7080ae3a02a570`  
		Last Modified: Mon, 22 Jan 2024 19:38:59 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:daa7929307eb30cbd91bf1b3b8b2f6cd47385c99fa34848ac73d1a0e866d3227
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185758997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581ce29672c6cf7e735526aaf89c0fe9993a1ceaae2598e05a22172d4c64cb16`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 02 Feb 2024 19:40:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Fri, 02 Feb 2024 19:40:09 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 02 Feb 2024 19:40:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:40:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 02 Feb 2024 19:40:10 GMT
RUN mkdir -p /data/data /data/log
# Fri, 02 Feb 2024 19:40:10 GMT
VOLUME [/data]
# Fri, 02 Feb 2024 19:40:10 GMT
WORKDIR /data
# Fri, 02 Feb 2024 19:40:10 GMT
EXPOSE 4200 4300 5432
# Fri, 02 Feb 2024 19:40:10 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 02 Feb 2024 19:40:10 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 02 Feb 2024 19:40:10 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Fri, 02 Feb 2024 19:40:10 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 02 Feb 2024 19:40:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 19:40:11 GMT
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
	-	`sha256:13154c493272245f778cf8550a7c76270148717b85acdfe67ff871933c516993`  
		Last Modified: Fri, 02 Feb 2024 19:42:06 GMT  
		Size: 116.3 MB (116302111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec45476da2cb4472f6b7ca93036e8647cec694600ef202a826cc4a1a2a57707`  
		Last Modified: Fri, 02 Feb 2024 19:41:57 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7bdbff0a05616a0adb5914af746c0fd2d2f3054b466ca8f7ed59e3bf099bd6`  
		Last Modified: Fri, 02 Feb 2024 19:41:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3592b40a987409a1cef456ec698ddf5c1042a6d6dd602ca0ddba3c0a615fc10`  
		Last Modified: Fri, 02 Feb 2024 19:41:57 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f77e3b6f35959c33068168534f681e498c05aa44b1e6de9e90935e24c77dcc`  
		Last Modified: Fri, 02 Feb 2024 19:41:57 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624cb721018ea071f6f8f31caf19caae4d71f6d1e87298a5487113bbe08362c1`  
		Last Modified: Fri, 02 Feb 2024 19:41:57 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.5.5`

```console
$ docker pull crate@sha256:481f8514e276e1c3cb6d7b8a4cf75711e19285be62236b322475597537a7099e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `crate:5.5.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:daa7929307eb30cbd91bf1b3b8b2f6cd47385c99fa34848ac73d1a0e866d3227
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185758997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581ce29672c6cf7e735526aaf89c0fe9993a1ceaae2598e05a22172d4c64cb16`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 02 Feb 2024 19:40:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Fri, 02 Feb 2024 19:40:09 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 02 Feb 2024 19:40:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:40:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 02 Feb 2024 19:40:10 GMT
RUN mkdir -p /data/data /data/log
# Fri, 02 Feb 2024 19:40:10 GMT
VOLUME [/data]
# Fri, 02 Feb 2024 19:40:10 GMT
WORKDIR /data
# Fri, 02 Feb 2024 19:40:10 GMT
EXPOSE 4200 4300 5432
# Fri, 02 Feb 2024 19:40:10 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 02 Feb 2024 19:40:10 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 02 Feb 2024 19:40:10 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Fri, 02 Feb 2024 19:40:10 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 02 Feb 2024 19:40:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 19:40:11 GMT
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
	-	`sha256:13154c493272245f778cf8550a7c76270148717b85acdfe67ff871933c516993`  
		Last Modified: Fri, 02 Feb 2024 19:42:06 GMT  
		Size: 116.3 MB (116302111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec45476da2cb4472f6b7ca93036e8647cec694600ef202a826cc4a1a2a57707`  
		Last Modified: Fri, 02 Feb 2024 19:41:57 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7bdbff0a05616a0adb5914af746c0fd2d2f3054b466ca8f7ed59e3bf099bd6`  
		Last Modified: Fri, 02 Feb 2024 19:41:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3592b40a987409a1cef456ec698ddf5c1042a6d6dd602ca0ddba3c0a615fc10`  
		Last Modified: Fri, 02 Feb 2024 19:41:57 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f77e3b6f35959c33068168534f681e498c05aa44b1e6de9e90935e24c77dcc`  
		Last Modified: Fri, 02 Feb 2024 19:41:57 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624cb721018ea071f6f8f31caf19caae4d71f6d1e87298a5487113bbe08362c1`  
		Last Modified: Fri, 02 Feb 2024 19:41:57 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.6`

```console
$ docker pull crate@sha256:9d7b5932caa4efaf78d8174851f32fe66e6f86d019bad6af45ca8c4af4bc9032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `crate:5.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:29af014af4ca44990ea7b866e12fa40f135532b860c542f8beac284a5b067472
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187428841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddbd6f9428c194610e1bb0aa05436eceacab9dee4702a1be20001849ac332b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 02 Feb 2024 19:39:44 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.1.tar.gz.asc crate-5.6.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.1.tar.gz.asc     && tar -xf crate-5.6.1.tar.gz -C /crate --strip-components=1     && rm crate-5.6.1.tar.gz
# Fri, 02 Feb 2024 19:39:49 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 02 Feb 2024 19:39:49 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:39:49 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 02 Feb 2024 19:39:50 GMT
RUN mkdir -p /data/data /data/log
# Fri, 02 Feb 2024 19:39:50 GMT
VOLUME [/data]
# Fri, 02 Feb 2024 19:39:50 GMT
WORKDIR /data
# Fri, 02 Feb 2024 19:39:50 GMT
EXPOSE 4200 4300 5432
# Fri, 02 Feb 2024 19:39:50 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 02 Feb 2024 19:39:50 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 02 Feb 2024 19:39:50 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T19:27:30.643907 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.1
# Fri, 02 Feb 2024 19:39:51 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 02 Feb 2024 19:39:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 19:39:51 GMT
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
	-	`sha256:d1eefb87b90b01bb7659ee9f8421262e383dd80d805ddd24b0048c7bd33b28a8`  
		Last Modified: Fri, 02 Feb 2024 19:41:45 GMT  
		Size: 118.0 MB (117971945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe1aabf07a32e19976f9af402d61787aefc03490e353e8003d91755255ae8c2`  
		Last Modified: Fri, 02 Feb 2024 19:41:36 GMT  
		Size: 1.9 MB (1939620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e16f4908665795d2bab19ee0de7cca1b7c9a4a880cc362edaa65f105716d6ea`  
		Last Modified: Fri, 02 Feb 2024 19:41:35 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a3d3e9154228d29d2170185c8d44a4c6219edf7866169d803f06129d6d3d53`  
		Last Modified: Fri, 02 Feb 2024 19:41:35 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3991c9b483f493e1ddc8e0f095a245ee3bd9f092108729d9668ac30af13f55d`  
		Last Modified: Fri, 02 Feb 2024 19:41:35 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149d664d1250e308308a65a76b90bc2c661ac145bd64dee9b3caf0d3c097276f`  
		Last Modified: Fri, 02 Feb 2024 19:41:35 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.6.1`

```console
$ docker pull crate@sha256:9d7b5932caa4efaf78d8174851f32fe66e6f86d019bad6af45ca8c4af4bc9032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `crate:5.6.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:29af014af4ca44990ea7b866e12fa40f135532b860c542f8beac284a5b067472
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187428841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddbd6f9428c194610e1bb0aa05436eceacab9dee4702a1be20001849ac332b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 02 Feb 2024 19:39:44 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.1.tar.gz.asc crate-5.6.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.1.tar.gz.asc     && tar -xf crate-5.6.1.tar.gz -C /crate --strip-components=1     && rm crate-5.6.1.tar.gz
# Fri, 02 Feb 2024 19:39:49 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 02 Feb 2024 19:39:49 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:39:49 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 02 Feb 2024 19:39:50 GMT
RUN mkdir -p /data/data /data/log
# Fri, 02 Feb 2024 19:39:50 GMT
VOLUME [/data]
# Fri, 02 Feb 2024 19:39:50 GMT
WORKDIR /data
# Fri, 02 Feb 2024 19:39:50 GMT
EXPOSE 4200 4300 5432
# Fri, 02 Feb 2024 19:39:50 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 02 Feb 2024 19:39:50 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 02 Feb 2024 19:39:50 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T19:27:30.643907 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.1
# Fri, 02 Feb 2024 19:39:51 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 02 Feb 2024 19:39:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 19:39:51 GMT
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
	-	`sha256:d1eefb87b90b01bb7659ee9f8421262e383dd80d805ddd24b0048c7bd33b28a8`  
		Last Modified: Fri, 02 Feb 2024 19:41:45 GMT  
		Size: 118.0 MB (117971945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe1aabf07a32e19976f9af402d61787aefc03490e353e8003d91755255ae8c2`  
		Last Modified: Fri, 02 Feb 2024 19:41:36 GMT  
		Size: 1.9 MB (1939620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e16f4908665795d2bab19ee0de7cca1b7c9a4a880cc362edaa65f105716d6ea`  
		Last Modified: Fri, 02 Feb 2024 19:41:35 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a3d3e9154228d29d2170185c8d44a4c6219edf7866169d803f06129d6d3d53`  
		Last Modified: Fri, 02 Feb 2024 19:41:35 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3991c9b483f493e1ddc8e0f095a245ee3bd9f092108729d9668ac30af13f55d`  
		Last Modified: Fri, 02 Feb 2024 19:41:35 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149d664d1250e308308a65a76b90bc2c661ac145bd64dee9b3caf0d3c097276f`  
		Last Modified: Fri, 02 Feb 2024 19:41:35 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:latest`

```console
$ docker pull crate@sha256:a8b677e16638e3e253400fb398d54fcc073bff8319589e1279b0376680bc95be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:9f958a830953682f4ccd11af8ea934fb792629b6be73e8d3a41ddc5f820a5a88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186870503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f86ee3cb3413e75940da34eb557c55868f9d3ff2053a981782b9694ec91b821`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:28:25 GMT
ADD file:9788b2efafa75575650a53daa65abb265da8eb6383be54f969f94c96c19ad82f in / 
# Tue, 28 Nov 2023 23:28:26 GMT
CMD ["/bin/bash"]
# Tue, 28 Nov 2023 23:48:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 22 Jan 2024 19:38:31 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.3.tar.gz.asc crate-5.5.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.3.tar.gz.asc     && tar -xf crate-5.5.3.tar.gz -C /crate --strip-components=1     && rm crate-5.5.3.tar.gz
# Mon, 22 Jan 2024 19:38:35 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.1     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.1.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.1.asc crash_standalone_0.30.1     && rm -rf "$GNUPGHOME" crash_standalone_0.30.1.asc     && mv crash_standalone_0.30.1 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 22 Jan 2024 19:38:35 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:38:35 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 22 Jan 2024 19:38:35 GMT
RUN mkdir -p /data/data /data/log
# Mon, 22 Jan 2024 19:38:35 GMT
VOLUME [/data]
# Mon, 22 Jan 2024 19:38:35 GMT
WORKDIR /data
# Mon, 22 Jan 2024 19:38:36 GMT
EXPOSE 4200 4300 5432
# Mon, 22 Jan 2024 19:38:36 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 22 Jan 2024 19:38:36 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 22 Jan 2024 19:38:36 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-17T13:51:08.432216 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.3
# Mon, 22 Jan 2024 19:38:36 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 22 Jan 2024 19:38:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:38:36 GMT
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
	-	`sha256:85f91ae4aa845d750268f9dab72264048a18c127e675954cc679ddcda1687a74`  
		Last Modified: Mon, 22 Jan 2024 19:39:11 GMT  
		Size: 116.3 MB (116277645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85a2368f5ae7b63abaccaa819c7f69cb3f68493079e438552c01fcecc82505`  
		Last Modified: Mon, 22 Jan 2024 19:39:00 GMT  
		Size: 2.0 MB (1954466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b33fda5199736a83b1af39bb08eb6e5e9ec4b9be4ae967e9b0dfb1d937c4a4`  
		Last Modified: Mon, 22 Jan 2024 19:38:59 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba12b4c41f7801f96610e4e9730bcd4ff7a36a7585c1d3288ad37cb18d33bab5`  
		Last Modified: Mon, 22 Jan 2024 19:38:59 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72532fc3f5543c472e129c401709aeac24a359be79725784bba85fc0f67e530b`  
		Last Modified: Mon, 22 Jan 2024 19:38:59 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6251c14959303ad5d41eb604b503f6ec87894ab0b408e4f8a7080ae3a02a570`  
		Last Modified: Mon, 22 Jan 2024 19:38:59 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:29af014af4ca44990ea7b866e12fa40f135532b860c542f8beac284a5b067472
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187428841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddbd6f9428c194610e1bb0aa05436eceacab9dee4702a1be20001849ac332b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 28 Nov 2023 23:42:55 GMT
ADD file:441d5753e358643a6d34ba14749df2f53865a75394abf02aaaf8f8cb75bd98eb in / 
# Tue, 28 Nov 2023 23:42:57 GMT
CMD ["/bin/bash"]
# Wed, 29 Nov 2023 00:16:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Fri, 02 Feb 2024 19:39:44 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.1.tar.gz.asc crate-5.6.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.1.tar.gz.asc     && tar -xf crate-5.6.1.tar.gz -C /crate --strip-components=1     && rm crate-5.6.1.tar.gz
# Fri, 02 Feb 2024 19:39:49 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 02 Feb 2024 19:39:49 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:39:49 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 02 Feb 2024 19:39:50 GMT
RUN mkdir -p /data/data /data/log
# Fri, 02 Feb 2024 19:39:50 GMT
VOLUME [/data]
# Fri, 02 Feb 2024 19:39:50 GMT
WORKDIR /data
# Fri, 02 Feb 2024 19:39:50 GMT
EXPOSE 4200 4300 5432
# Fri, 02 Feb 2024 19:39:50 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 02 Feb 2024 19:39:50 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 02 Feb 2024 19:39:50 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T19:27:30.643907 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.1
# Fri, 02 Feb 2024 19:39:51 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 02 Feb 2024 19:39:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 19:39:51 GMT
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
	-	`sha256:d1eefb87b90b01bb7659ee9f8421262e383dd80d805ddd24b0048c7bd33b28a8`  
		Last Modified: Fri, 02 Feb 2024 19:41:45 GMT  
		Size: 118.0 MB (117971945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe1aabf07a32e19976f9af402d61787aefc03490e353e8003d91755255ae8c2`  
		Last Modified: Fri, 02 Feb 2024 19:41:36 GMT  
		Size: 1.9 MB (1939620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e16f4908665795d2bab19ee0de7cca1b7c9a4a880cc362edaa65f105716d6ea`  
		Last Modified: Fri, 02 Feb 2024 19:41:35 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a3d3e9154228d29d2170185c8d44a4c6219edf7866169d803f06129d6d3d53`  
		Last Modified: Fri, 02 Feb 2024 19:41:35 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3991c9b483f493e1ddc8e0f095a245ee3bd9f092108729d9668ac30af13f55d`  
		Last Modified: Fri, 02 Feb 2024 19:41:35 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149d664d1250e308308a65a76b90bc2c661ac145bd64dee9b3caf0d3c097276f`  
		Last Modified: Fri, 02 Feb 2024 19:41:35 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
